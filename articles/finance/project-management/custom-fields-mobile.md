---
title: Implementere brugerdefinerede felter for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emne indeholder almindelige mønstre til brug af udvidelser i forbindelse med implementering af brugerdefinerede felter.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174797"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementere brugerdefinerede felter for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android

[!include [banner](../includes/banner.md)]

Dette emne indeholder almindelige mønstre til brug af udvidelser i forbindelse med implementering af brugerdefinerede felter. Følgende emner behandles:

- De forskellige datatyper, som den brugerdefinerede feltstruktur understøtter
- Sådan får du vist skrivebeskyttede eller redigerbare felter på timeseddelposter og gemmer brugerleverede værdier i databasen igen
- Sådan får du vist skrivebeskyttede felter i timeseddelhovedet
- Sådan integrerer du anden brugerdefineret forretningslogik for at angive standardværdier i felter og foretage yderligere validering

## <a name="audience"></a>Målgruppe

Dette emne er henvendt til udviklere, der integrerer deres brugerdefinerede felter i det Microsoft Dynamics 365 Project Timesheet-mobilprogram, der er tilgængeligt for Apple IOS Android og Google. Forudsætningen er, at læserne kender til X++-udviklings- og projekttimeseddelfunktionerne.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datakontrakt – TSTimesheetCustomField X++-klasse

**TSTimesheetCustomField**-klassen er den X++-datakontraktklasse, der repræsenterer oplysninger om et brugerdefineret felt til timeseddelfunktionaliteten. Lister over brugerdefinerede feltobjekter overføres både til TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten, så der kan vises brugerdefinerede felter i mobilappen.

- **TSTimesheetDetails** - Timeseddel-hovedkontrakten.
- **TSTimesheetEntry** - Timeseddel-transaktionskontrakten. Grupper af disse objekter, der har samme projektoplysninger og **timesheetLineRecId**-værdi, udgør en linje.

### <a name="fieldbasetype-types"></a>fieldBaseType (typer)

Egenskaben **FieldBaseType** i objektet **TsTimesheetCustom** bestemmer, hvilken type felt der vises i appen. Følgende værdier for **Typer** understøttes.

| Typeværdi | Type              | Kommentarer |
|-------------|-------------------|-------|
| 0           | Streng (og fasttekst) | Feltet vises som et tekstfelt. |
| 1           | Heltal           | Værdien vises som et tal uden decimalpladser. |
| 2           | Kommatal              | Værdien vises som et tal, der har decimalpladser.<p>Hvis du vil vise kommatalsværdien som en valuta i appen, skal du bruge egenskaben **fieldExtenededType**. Du kan bruge egenskaben **numberOfDecimals** til at angive antallet af decimaler, der skal vises.</p> |
| 3           | Dato              | Datoformater bestemmes af brugerens indstilling for **Format for dato, klokkeslæt og tal**, der er angivet under **Præferencer af sprog og land/område** i **Brugerindstillinger**. |
| 4           | Boolesk           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Hvis egenskaben **stringOptions** ikke findes i objektet **TSTimesheetCustomField**, vises der et fritekstfelt for brugeren.

    Egenskaben **stringLength** kan bruges til at angive den maksimale strenglængde, som brugerne kan angive.

- Hvis egenskaben **stringOptions** findes i objektet **TSTimesheetCustomField**, er listeelementerne de eneste værdier, som brugerne kan vælge ved hjælp af alternativknapper.

    I dette tilfælde kan strengfeltet fungere som en fasttekstværdi med henblik på brugerindtastning. Hvis du vil gemme værdien i databasen som en fasttekst, skal du manuelt knytte strengværdien til fasttekstværdien igen, før du gemmer den i databasen, ved hjælp af kommandokæden (se eksemplet i afsnittet "Bruge kommandokæde på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen" senere i dette emne).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Du kan bruge denne egenskab til at formatere kommatalsværdier som valuta. Denne fremgangsmåde kan kun anvendes, hvis **fieldBaseType**-værdien er **Kommatal**.

- **TSCustomFieldExtendedType:None** – Der anvendes ingen formatering.
- **TSCustomFieldExtendedType::Currency** – Formatér værdien som valuta.

    Når valutaformatering er aktiv, kan feltet **stringValue** bruges til at overføre den valutakode, der skal vises i appen. Værdien er en skrivebeskyttet værdi.

    Feltet **realValue** indeholder det pengebeløb, der skal gemmes i databasen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Du kan bruge denne egenskab til at angive, hvor det brugerdefinerede felt skal vises i appen.

- **TSCustomFieldSection::Header** – Feltet vises i sektionen **Vis flere oplysninger** i appen. Disse felter er altid skrivebeskyttede.
- **TSCustomFieldSection::Line** – Feltet vises efter alle felter med out-of-box-linjer på timeseddelposter. Disse felter kan enten redigeres eller skrivebeskyttes.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Denne egenskab identificerer feltet, når de værdier, som appen angiver, gemmes i databasen.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Denne egenskab identificerer feltet, når de værdier, som appen angiver, gemmes i databasen.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelindtastningen skal kunne redigeres af brugerne. Indstil egenskaben til **Nej** for at gøre feltet skrivebeskyttet.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelindtastningen skal være obligatorisk.

### <a name="label-str"></a>label (str)

Denne egenskab specificerer den etiket, der vises ud for feltet i appen.

### <a name="stringoptions-list-of-strings"></a>stringOptions (liste over strenge)

Denne egenskab kan kun anvendes, når **fieldBaseType** er indstillet til **Streng**. Hvis **stringOptions** er valgt, er de strengværdier, der kan vælges via alternativknapper, angivet af strengene på listen. Hvis der ikke er angivet nogen strenge, er fritekstindtastning i strengfeltet tilladt (se eksemplet i afsnittet "Bruge kommandokæden på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen" senere i dette emne).

### <a name="stringlength-int"></a>stringLength (int)

Denne egenskab specificerer den maksimale længde for et strengfelt. Den kan kun anvendes, når **fieldBaseType** er indstillet til **Streng**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Denne egenskab specificerer det antal decimalpladser, der vises for et kommatalsfelt. Den kan kun anvendes, når **fieldBaseType** er indstillet til **Kommatal**.

### <a name="ordersequence-int"></a>orderSequence (int)

Denne egenskab styrer den rækkefølge, som de brugerdefinerede felter i appen vises i, når der er angivet mere end ét brugerdefineret felt. Felterne med de laveste numre vises først.

### <a name="booleanvalue-boolean"></a>booleanValue (boolesk)

For felter af typen **Boolesk** overfører denne egenskab den booleske værdi for feltet mellem serveren og appen.

### <a name="guidvalue-guid"></a>guidValue (GUID)

For felter af typen **GUID** overfører denne egenskab GUID-værdien (globally unique identifier) for feltet mellem serveren og appen.

### <a name="int64value-int64"></a>int64Value (Int64)

For felter af typen **Int64** overfører denne egenskab int64-værdien for feltet mellem serveren og appen.

### <a name="intvalue-int"></a>intValue (int)

For felter af typen **Int** overfører denne egenskab int-værdien for feltet mellem serveren og appen.

### <a name="realvalue-real"></a>realValue (real)

For felter af typen **Kommatal** overfører denne egenskab kommatalsværdien for feltet mellem serveren og appen.

### <a name="stringvalue-str"></a>stringValue (str)

For felter af typen **Streng** overfører denne egenskab strengværdien for feltet mellem serveren og appen. Den bruges også til felter af typen **Kommatal**, der er formateret som valuta. For disse felter bruges egenskaben til at overføre valutakoden til appen.

### <a name="datevalue-date"></a>dateValue (dato)

For felter af typen **Date** overfører denne egenskab datoværdien for feltet mellem serveren og appen.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Vise og gemme et brugerdefineret felt i sektionen til timeseddelindtastning

Nedenfor vises et skærmbillede fra mobilappen af oprettelse af en timeseddelpost. Den viser de indbyggede felter og et brugerdefineret felt i afsnittet "Tidsregistrering", der kaldes "Teststreng" med fasttekstværdien "Anden indstilling".

![Brugerdefineret felt til teststreng i appen](media/timesheet-entry.jpg)



Nedenfor vises et skærmbillede fra mobilappen af brugeren, der vælger en af de fasttekstindstillinger, der er tilgængelige for det brugerdefinerede felt "Teststreng".  De to indstillinger er "Første indstilling" og "Anden indstilling" vist som alternativknapper. Den anden indstilling er aktuelt markeret.

![Alternativknapper til det brugerdefinerede felt Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Udvide tabellen TSTimesheetLine, så den har et brugerdefineret felt

I typiske scenarier er det sandsynligt, at dataene til et brugerdefineret felt i sektionen til timeseddelindtastning gemmes i tabellen TSTimesheetLine. Der kan dog bruges andre tabeller, hvis dataene kan hentes på basis af en TSTimesheetTrans-post, der er angivet, eller hvis der ikke er angivet en bestemt postkontekst (hvis feltet f.eks. er skrivebeskyttet i projektparametrene).

Bemærk, at brugerdefinerede felter ikke behøver at have nogen understøttende databaseposter. De kan genereres dynamisk på basis af X++-logik. Denne fremgangsmåde kan være nyttig i skrivebeskyttede scenarier (se afsnittet "Bruge kommandokæde på klassen TSTimesheetDetails, buildCustomFieldListForHeader-metoden til at angive timeseddeloplysninger" for at få et eksempel på dynamisk genererede brugerdefinerede feltværdier).

Nedenfor vises et skærmbillede fra Visual Studio af applikationsobjekttræet. Billedet viser en udvidelse af tabellen TSTimesheetLine, hvor TestLineString-feltet er tilføjet som et brugerdefineret felt.

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Bruge kommandokæde på metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i sektionen timeseddelpost

Denne kode bestemmer visningsindstillingerne for feltet i appen. Den styrer f.eks. feltets type, etiketten, om feltet er obligatorisk, og hvilken sektion feltet vises i.

I følgende eksempel vises et strengfelt til tidsposter. Dette felt indeholder to indstillinger, **Første indstilling** og **Anden indstilling**, der er tilgængelige via alternativknapper. Feltet i appen er knyttet til feltet **TestLineString**, som føjes til tabellen TSTimesheetLine.

Bemærk brugen af metoden **TSTimesheetCustomField::newFromMetatdata ()**, der kan forenkle initialiseringen af egenskaberne for det brugerdefinerede felt: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**. Du kan også angive disse parametre manuelt, som du foretrækker.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Bruge kommandokæde på metoden buildCustomFieldListForEntry i klassen TSTimesheetEntry til at angive værdier i en timeseddelpost

Metoden **buildCustomFieldListForEntry** bruges til at angive værdier på de gemte timeseddellinjer i mobilappen. Det kræver en TSTimesheetTrans-post som parameter. Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Bruge kommandokæde på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen

Hvis du vil gemme et brugerdefineret felt i databasen igen ved normal brug, skal du udvide flere metoder:

- Metoden **timesheetLineNeedsUpdating** bruges til at bestemme, om linjeposten er ændret af brugeren i appen, og om den skal gemmes i databasen. Hvis ydeevnen ikke er noget problem, kan denne metode forenkles, så den altid returnerer **sand**.
- Metoderne **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan udvides, så de angiver værdier i TSTimesheetLine-databaseposten fra den leverede TSTimesheetEntry-datakontraktpost. I eksemplet nedenfor skal du lægge mærke til, hvordan tilknytningen mellem databasefeltet og indtastningsfeltet udføres manuelt via X++-kode.
- Metoden **populateTimesheetWeekFromEntry** kan også udvides, hvis det brugerdefinerede felt, der er knyttet til **TSTimesheetEntry**-objektet, skal skrive tilbage til TSTimesheetLineweek-databasetabellen.

> [!NOTE]
> I følgende eksempel gemmes den **firstOption**- eller **secondOption**-værdi, som brugeren vælger til databasen, som en rå strengværdi. Hvis databasefeltet er et felt af typen **Fasttekst**, kan disse værdier knyttes manuelt til en fasttekstværdi og derefter gemmes i et fasttekstfelt i databasetabellen.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Vise et brugerdefineret felt i hovedsektionen på timeseddel

Nedenfor vises et skærmbillede fra mobilappen af en bruger, der ser på en timeseddel. Knappen "Flere oplysninger" er valgt i øverste højre hjørne for at vise indstillingen "Vis flere oplysninger".  

![Kommandoen Vis flere oplysninger](media/show-more.png)



Nedenfor vises et skærmbillede fra mobilappen, der viser sektionen "Flere" på en timeseddel. Der er føjet et brugerdefineret felt med navnet "Udnyttelsesgraden for denne timeseddel (beregnet brugerdefineret felt)" til timesedlens hovedsektion. Der er angivet en skrivebeskyttet værdi, "0.667", i det brugerdefinerede felt.

![Sektionen Flere](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Udvide tabellen TSTimesheetTable, så den har et brugerdefineret felt

I typiske scenarier er det sandsynligt, at dataene til et brugerdefineret felt i hovedsektionen hentes fra tabellen TSTimesheetHeader. Der kan dog bruges andre tabeller, hvis dataene kan hentes på basis af en TSTimesheetTable-post, der er angivet, eller hvis der ikke er angivet en bestemt postkontekst (hvis feltet f.eks. er skrivebeskyttet i projektparametrene).

Bemærk, at brugerdefinerede felter ikke behøver at have nogen understøttende databaseposter. De kan genereres dynamisk på basis af X++-logik. I eksemplet nedenfor vises denne fremgangsmåde.

Felter i hovedsektionen er altid skrivebeskyttede i appen.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Bruge kommandokæde på metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i hovedsektionen

Denne kode bestemmer visningsindstillingerne for feltet i appen. Den styrer f.eks. feltets type, etiketten, om feltet er obligatorisk, og hvilken sektion feltet vises i.

Følgende eksempel viser en beregnet værdi i hovedsektionen i appen.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Bruge kommandokæde på metoden buildCustomFieldListForHeader i klassen TSTimesheetDetails til at angive oplysninger i en timeseddel

Metoden **buildCustomFieldListForHeader** bruges til at angive hovedoplysninger i mobilappen. Det kræver en TSTimesheetTable-post som parameter. Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen. I følgende eksempel læses der ikke værdier fra databasen. I stedet bruges X++-logik til at generere en beregnet værdi, der derefter vises i appen.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Andre muligheder for konfigurerbarhed/udvidelsesmuligheder

### <a name="adding-additional-validation-for-the-app"></a>Tilføje yderligere validering for appen

Eksisterende logik for timeseddelfunktionalitet på databaseniveau fungerer stadig som forventet. Hvis du vil afbryde udførelsen af gemme- eller sendehandlinger og vise en bestemt fejlmeddelelse, kan du føje **udløs fejl("meddelelse til bruger")** til koden via en kommandokædeudvidelse. Her er tre eksempler på nyttige udvidelsesmetoder:

- Hvis **validateWrite** i tabellen TSTimesheetLine returnerer **falsk** under en lagringshandling for en timeseddellinje, vises der en fejlmeddelelse i mobilappen.
- Hvis **validateSubmit** i tabellen TSTimesheetTable returnerer **falsk** under afsendelse af en timeseddel i appen, vises der en fejlmeddelelse for brugeren.
- Logik, der udfylder felter (f.eks. **Linjeegenskab**) under **indsæt**-metoden i TSTimesheetLine-tabellen, kører stadig.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skjule og markere out of box-felter som skrivebeskyttede via konfiguration

Fra projektparametrene kan du gøre out of box-felter skrivebeskyttede eller skjulte i mobilappen. Angiv indstillingerne i sektionen **Mobile timesedler** under fanen **Timeseddel** på siden **Parametre for projektstyring og regnskab**.

![Projektparametre](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Ændre de aktiviteter, der er tilgængelige for valg via udvidelser

De aktiviteter, der er tilgængelige for valg til et projekt, udfyldes via metoderne **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**. Du kan bruge kommandokæden til at ændre denne funktionalitet, så den svarer til firmascenariet for de aktiviteter, der er tilgængelige for valg til et bestemt projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Angive en standardprojektkategori på timeseddelposter

Indtastning af en standardprojektkategori på timeseddelposter sker på tre niveauer. Du kan bruge kommandokæden til at udvide funktionaliteten på et eller flere af disse niveauer for at opnå den ønskede funktionsmåde. Følgende hierarki bruges:

1. Appen forsøger at placere standardkategorien fra projektressourcen. Denne standardkategori er angivet i metoderne **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.
2. Hvis standardkategorien ikke findes på projektressourceniveau, forsøger appen at trække den fra projektaktiviteten. Denne standardkategori indstilles i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.
3. Hvis standardkategorien ikke findes på projektaktivitetsniveau, tages standardkategorien fra projektparametrene. Denne standardkategori indstilles i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.
