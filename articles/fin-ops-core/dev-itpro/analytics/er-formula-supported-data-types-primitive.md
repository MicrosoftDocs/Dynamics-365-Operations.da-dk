---
title: Understøttede basisdatatyper til elektroniske rapporteringsformler
description: Dette emne indeholder oplysninger om basisdatatyper, der understøttes i formler til elektronisk rapportering (ER).
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e1c70dd0fa89c6cc5a8b4778b073d1cf4a3dadd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355316"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Understøttede basisdatatyper til elektroniske rapporteringsformler

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om basisdatatyper, der understøttes i udtryk til [elektronisk rapportering (ER)](general-electronic-reporting.md). Her er en liste over basisdatatyper:

- [boolesk](#boolean)
- [dato](#date)
- [dato/klokkeslæt](#datetime)
- [fasttekst](#enumeration)
- [guid](#guid)
- [heltal](#integer)
- [int64](#int64)
- [real](#real)
- [streng](#string)

## <a name="boolean"></a><a name="boolean"></a>Boolesk

Den *booleske* basisdatatype indeholder en værdi, der evalueres som enten *sand* eller *falsk*. Du kan bruge de reserverede konstante nøgleord **Sand** og **Falsk**, hvor der forventes et *boolesk* udtryk. Standardværdien er *falsk*.

Den interne repræsentation af en *boolesk* værdi er et *heltal*. *Heltal*-værdien 0 (nul) evalueres som *falsk*, og alle andre *heltalsværdier* evalueres som *sande*. Når du [validerer](general-electronic-reporting-formula-designer.md#TestFormula) et konfigureret udtryk, der returnerer en *boolesk* værdi i [ER-formeldesigneren](er-advanced-formula-editor.md), vil testresultatruden vise *0* (nul), når udtrykket returnerer *falsk*. Ellers vises *1* i ruden til testresultat.

En *boolesk* værdi har ingen konverteringer. Du kan dog bruge funktionen [TEXT](er-functions-text-text.md) til eksplicit at konvertere en *boolesk* værdi til en *streng*:

- Værdien *falsk* konverteres til tekststrengen **Falsk**.
- Værdien *sand* konverteres til tekststrengen **Sand**.

> [!NOTE]
> Denne konvertering afhænger ikke af den angivne sprog- og kultur-[kontekst](er-design-multilingual-reports.md).

Sammenlignings-[operatorer](er-formula-language.md#Operators) er den eneste type operator, der kan bruges med den *booleske* datatype. Følgende operatorer kan bruges til at sammenligne to *booleske* værdier: \<\> og =.

## <a name="date"></a><a name="date"></a>Dato

Basisdatatypen *dato* gemmer en dag, en måned og et år. Datoer kan startes ved hjælp af følgende funktioner:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

*Dato*-datatypen kan indeholde datoer mellem 1. januar 1900 og 31. december 2154. Standardværdien er **null**, og den interne præsentation er datoen 1. januar 1900.

En *dato* har ingen implicitte konverteringer. Du kan dog bruge følgende eksplicitte konverteringsfunktioner:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Du kan bruge funktionen [ADDDAYS](er-functions-datetime-adddays.md) til at tilføje og trække dage fra datoer. På denne måde kan du flytte datoen et bestemt antal dage ind i fremtiden og fortiden. Funktionen [DAYS](er-functions-datetime-days.md) giver dig mulighed for at trække datoer fra hinanden og beregne forskellen i dage. Yderligere oplysninger om transformation af *dato*-værdier finder du i [Liste over ER-funktioner i kategorien Dato og klokkeslæt](er-functions-category-datetime.md).

Sammenlignings-[operatorer](er-formula-language.md#Operators) er den eneste type operator, der kan bruges med *dato*-datatypen. Følgende operatorer kan bruges til at sammenligne to *dato*-værdier: \<\>, \<, \<=, =, \> og \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Basisdatatypen *datetime* kombinerer *dato*-typen og en værdi, der repræsenterer den tid, der er gået siden midnat. Tiden angives i timer, minutter, sekunder og brøkdele af et sekund. En *datetime*-værdi indeholder også oplysninger om tidszonen.

Datatypen *datetime* kan indeholde datoer mellem 1. januar 1900 (1900-01-01T00:00:00.0000000+00:00 i rundturs-[formatet](/dotnet/standard/base-types/standard-date-and-time-format-strings)) og 31. december 2154 (2154/12/31T11:59:59.9999999+00:00 i rundtursformatet). Den mindste tidsenhed for *datetime* er en tiende milliontedel af et sekund.

> [!NOTE]
> Når **hh**-[specifikatoren](/dotnet/standard/base-types/standard-date-and-time-format-strings) bruges til timer, kan tidsværdier over 12:59:59:9999999 ikke fortolkes som gyldige tider.
>
> Når **HH**-specifikatoren bruges til timer, kan tidsværdier over 23:59:59:9999999 ikke fortolkes som gyldige tider.

Standardværdien er **null**, og den interne repræsentation er datoen 1. januar, 1900 (1900-01-01T00:00:00.0000000+00:00 i rundtursformatet).

Datetime kan startes ved hjælp af følgende funktioner:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

En *datetime* har ingen implicitte konverteringer. Du kan dog bruge følgende eksplicitte konverteringsfunktioner:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Yderligere oplysninger om transformation af *datetime*-værdier finder du i [Liste over ER-funktioner i kategorien Dato og klokkeslæt](er-functions-category-datetime.md).

Sammenlignings-[operatorer](er-formula-language.md#Operators) er den eneste type operator, der kan bruges med *datetime*-datatypen. Følgende operatorer kan bruges til at sammenligne to *datetime*-værdier: \<\>, \<, \<=, =, \> og \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Fasttekst

Basisdatatypen *fasttekst* er en liste over konstanter. Du kan bruge fasttekster, der er defineret i programmets [kildekode](../dev-ref/xpp-data-primitive.md#enum). Du kan også introducere dine fastttekster i [ER-datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components) og [ER-format](general-electronic-reporting.md#FormatComponentOutbound)-komponenterne.

Et programs *fasttekst* kan bruges i udtryk med alle ER-modeltilknytninger og ER-formater.

I følgende illustration vises, hvordan du kan føje **CustVendCorrectiveReasonCode**-modelfastteksten til den redigerbare ER-datamodel.

[![Konfigurere en modelfasttekst i ER-datamodeldesigneren.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

En models *fasttekst* kan bruges i udtryk med alle ER-modeltilknytnings- og ER-formater, der blev oprettet under en datamodel, hvor *fasttekst* blev indført.

I følgende illustration vises, hvordan du kan føje en **Liste over Natura-underkategorier med modtagerbetaling** til det redigerbare ER-format.

[![Konfigurere en formatfasttekst i ER-formatdesigneren.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

En format *fasttekst* kan kun bruges i udtryk i ER-format, hvor *fasttekst* blev indført.

Du skal bruge den relevante type ER-datakilde for at få en bestemt fasttekst til en konfigureret ER-komponent som en konstant eller som en værdi, som den bruger, der kører en ER-løsning, definerer i dialogboksen under kørslen.

- Der er adgang til programfasttekster ved hjælp af datakilderne for **Dynamics 365 for Operations \ Fasttekst** og **Generelt \ Brugerinputparametre**. I følgende illustration vises, hvordan du kan føje datakilderne **appenumNoYes** og **uipNoYes** til det redigerbare ER-format, der refererer til programfastteksten **NoYes**.

    [![Tilføje datakilder for programfasttekster i ER-formatdesigneren.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Der er adgang til datamodelfasttekster ved hjælp af datakilderne for **Datamodel \ Fasttekst** og **Datamodel \ Brugerinputparametre til fasttekst**. I følgende illustration vises, hvordan du kan føje datakilden **CustVendCorrectiveReasonCode**, der refererer til datamodelfastteksten **CustVendCorrectiveReasonCode**, til det redigerbare ER-format.

    [![Tilføje datakilder for modelfasttekst i ER-formatdesigneren.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Der er adgang til formatfasttekster ved hjælp af datakilderne for **Format \ Fasttekst** og **Format \ Brugerinputparametre til fasttekst**. I følgende illustration vises, hvordan du kan føje datakilden **NaturaReverseCharge**, der refererer til formatfastteksten **Natura-underkategorier med modtagerbetaling**, til det redigerbare ER-format.

    [![Tilføje datakilder for formatfasttekst i ER-formatdesigneren.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

En *fasttekst*-værdi har ingen implicitte konverteringer. Du kan dog bruge funktionen [TEXT](er-functions-text-text.md) til at konvertere en *fasttekst* til en tekststreng. Denne konvertering er ikke sprogafhængig. Du kan få mere at vide om, hvordan du knytter en *fasttekst*-værdi til de relevante sprogspecifikke navne i eksemplerne på brug af funktionerne [LISTOFFIELDS](er-functions-list-listoffields.md) og [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md).

Sammenlignings-[operatorer](er-formula-language.md#Operators) er den eneste type operator, der kan bruges med *fasttekst*-datatypen. Følgende operatorer kan bruges til at sammenligne to *fasttekst*-værdier: \<\> og =.

## <a name="guid"></a><a name="guid"></a>Guid

Basisdatatypen *guid* indeholder en Globally Unique Identifier-værdi (GUID). En GUID er en værdi, der kan bruges på tværs af alle computere og netværk, hvor der kræves et entydigt id. Det er usandsynligt, at nummeret bliver duplikeret. Et gyldigt GUID opfylder alle følgende specifikationer:

- Der skal være 32 hexadecimale cifre.
- Derudover skal der være fire bindestregtegn, der er indsat følgende steder: 8-4-4-4-12.
- Der kan desuden tilføjes valgfrie klammeparenteser \{\} i starten og slutningen af strengen. For eksempel er både **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** og **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** gyldige GUID-strenge.
- Derfor skal der i alt være 36 eller 38 tegn, afhængigt af om der skal tilføjes klammeparenteser.
- De bogstaver, der bruges som hexadecimale cifre, kan være med store bogstaver (A–F), små bogstaver (a-f) eller blandet.

Du kan bruge følgende eksplicitte konverteringsfunktioner:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Sammenlignings-[operatorer](er-formula-language.md#Operators) er den eneste type operator, der kan bruges med *guid*-datatypen. Følgende operatorer kan bruges til at sammenligne to *guid*-værdier: \<\> og =.

## <a name="integer"></a><a name="integer"></a>Heltal

Basisdatatypen *heltal* repræsenterer et tal uden decimaler. Heltal bruges som kontrolvariabler i gentagne sætninger eller som indekser på postlister.

Et *heltal* er en bogstavelig værdi, som er angivet direkte i et [ER-udtryk](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formel), f.eks. **12345**. Et *heltal* har en bredde på 32 bit. Standardværdien er **0**, og den interne præsentation er et langt tal. Et *heltal* konverteres automatisk til en *real*-værdi.

Du kan også bruge følgende eksplicitte konverteringsfunktioner:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Intervallet for et *heltal* er \[-2.147.483.647 : 2.147.483.647\]. Alle heltal i dette interval kan bruges som konstanter.

Alle sammenlignings- og matematiske [operatorer](er-formula-language.md#Operators) kan bruges med datatypen *Heltal*.

## <a name="int64"></a><a name="int64"></a>Int64

Basisdatatypen *int64* repræsenterer et tal uden decimaler. *int64* bruges som kontrolvariabler i gentagne sætninger eller som postidentifikatorer.

Et *int64* har en bredde på 64 bit. Standardværdien er **0**, og den interne præsentation er et langt tal. Et *int64* konverteres automatisk til en *real*-værdi.

Du kan også bruge følgende eksplicitte konverteringsfunktioner:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Intervallet for et *int64* er \[-9.223.372.036.854.775.807 : 9.223.372.036.854.775.807\].

Alle sammenlignings- og matematiske [operatorer](er-formula-language.md#Operators) kan bruges med datatypen *int64*.

## <a name="real"></a><a name="real"></a>Kommatal

Basisdatatypen *real* kan indeholde decimalværdier ud over heltal. Du kan bruge decimalkonstanter overalt, hvor der forventes en *real*. En decimalkonstant er decimalen, som den er angivet direkte i kode, f.eks. **2,19**.

> [!NOTE]
> I ER-udtryk bruges altid et punktum (.) som decimalseparator.

Real-værdier kan bruges i alle udtryk, og de kan bruges med både sammenlignings- og matematiske operatorer. En *real*-værdi har en præcision på 16 betydende cifre. Standardværdien for en *real* er **0,0**, og den interne repræsentation er et binært kodet digitaltal (BCD). BCD-kodningen giver mulighed for nøjagtige repræsentationer af værdier, der er multiplum af 0,1. Intervallet for en *real*-variabel er -(10)<sup>127</sup> til (10)<sup>127</sup>. Alle real-værdier i dette interval kan bruges som konstanter i ER-udtryk.

En *real* har ingen implicitte konverteringer. Du kan dog bruge følgende funktioner til eksplicit at konvertere en *real* til andre datatyper og andre datatyper til en *real*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Alle sammenlignings- og matematiske [operatorer](er-formula-language.md#Operators) kan bruges med datatypen *real*.

## <a name="string"></a><a name="string"></a>Streng

Basisdatatypen *streng* repræsenterer en række tegn, der bruges som tekster, kontonumre, adresser og telefonnumre.

*Streng*-konstanter er tegn, der er indsat i anførselstegn (""). *Streng*-konstanter kan bruges alle de steder, hvor der forventes *streng*-værdier i ER-udtryk. Du kan bruge strenge i logiske udtryk, f.eks. sammenligninger. Du kan også sammenkæde *streng*-værdier ved at bruge operatoren **\&** eller funktionen [CONCATENATE](er-functions-text-concatenate.md).

> [!NOTE]
> Hvis du sammenkæder to *streng*-værdier, og den *streng*, der er resultatet, skal strække sig over mere end én linje, skal du bruge separatoren for linjeskift mellem værdierne. For TEXT-outputtet kan denne separator være et tegn, der genereres ved hjælp af udtrykket [CHAR](er-functions-text-char.md)(10) eller CHAR(13). Til HTML kan det være tag **\<br\>**.

Standardværdien for en *streng* er en tom tekststreng uden tegn, og den interne repræsentation er en liste over tegn.

Der er ingen automatiske konverteringer for strenge. Du kan dog bruge følgende eksplicitte konverteringsfunktioner:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Yderligere oplysninger om transformation af *streng*-værdier finder du i [Liste over ER-funktioner i tekstkategorien](er-functions-category-text.md).

En *streng* kan indeholde et ubegrænset antal tegn.

Alle sammenlignings- og matematiske [operatorer](er-formula-language.md#Operators) kan bruges med datatypen *streng*.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelsprog i elektronisk rapportering](er-formula-language.md)
- [Understøttede sammensatte datatyper](er-formula-supported-data-types-composite.md)
