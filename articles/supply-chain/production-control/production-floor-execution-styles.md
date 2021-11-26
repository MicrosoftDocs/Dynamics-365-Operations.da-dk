---
title: Designe grænsefladen til produktionsudførelse
description: I emnet forklares, hvordan du konfigurerer formkontrolelementer, så standardtypografierne til produktionsudførelse anvendes på dem.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790884"
---
# <a name="style-the-production-floor-execution-interface"></a>Designe grænsefladen til produktionsudførelse

[!include [banner](../includes/banner.md)]

I emnet forklares, hvordan du konfigurerer formkontrolelementer, så standardtypografierne til produktionsudførelse anvendes på dem.

## <a name="forms-and-dialogs"></a>Formularer og dialogbokse

Typografier kan kun anvendes på en formular eller dialogboks, hvis følgende krav er opfyldt:

- Hvis formularen skal ligne den eksisterende formular til rapportstatus, skal navnet på formularen eller dialogboksen starte med `JmgProductionFloorExecutionCustomInputDialog`.
- Formularen eller dialogboksen kan indeholde en detaljeret formulardel. Hvis du vil anvende typografier på den, skal navnet på detaljeformulardelen starte med `JmgProductionFloorExecutionCustomDetailsDialog`.
- Hvis formularen eller dialogboksen skal have en simpel visning, skal navnet på den simple visning starte med `JmgProductionFloorExecutionCustomDialog`. Eksempler på formularer, der har en simpel visning, omfatter startformen og formularen med indirekte aktiviteter.
- Alle kontrolelementer i dialogboksen skal være konfigureret som beskrevet i dette emne.

> [!IMPORTANT]
> De funktioner, der nævnes i de første to punkttegn på denne liste, kræver Supply Chain Management version 10.0.19 eller nyere.

Typografier kan kun anvendes på knappen **OK** i en dialogboks, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `OkButtonGroup`.

Typografier kan kun anvendes på knappen **Annuller** i en dialogboks, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `CancelButtonGroup`.

### <a name="header"></a>Overordnet

I følgende illustration vises en typisk formular- eller dialogboksoverskrift.

![Typisk formular- eller dialogboksoverskrift.](media/pfe-styles-header.png "Typisk formular- eller dialogboksoverskrift")

I Visual Studio oprettes overskrifter ved hjælp af en struktur som f.eks. den, der vises i følgende illustration.

![Typisk kodestruktur til oprettelse af en overskrift.](media/pfe-styles-header-code-structure.png "Typisk kodestruktur til oprettelse af en overskrift")

Hvis du vil føje tekst til overskriften, skal du bruge kode som f.eks. følgende.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Når du skriver overskriftskoden, skal du anvende følgende regler:

- Navnet på hovedgruppen skal være `TableRowHeaderGroup`.
- Hver tekstblok (adskilt af punkttegn) skal starte med `HeaderFieldWithSeparatorText`.
- Det sidste tekstnavn skal starte med `HeaderFieldText`.
- `CaptionImage` kan springes over.

### <a name="progress-indicator"></a>Statusindikator

Du kan medtage en statusindikator, som vises til højre for overskriften. I følgende illustration vises en statusindikator.

![Typisk statusindikator.](media/pfe-styles-header-progress.png "Typisk statusindikator")

Tekstfeltet skal navngives `ShowProgress` for at få vist statusindikatoren.

## <a name="grid"></a>Gitter

Typografier anvendes automatisk. Der kræves ikke nogen specifik konfiguration.

Gitteret skal have en `TabularView`-typografi, og metoden `run()` i den brugerdefinerede formular skal overskrives, da et nyt gitter endnu ikke understøttes. Tilføj følgende kode.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Hvis du vil opdatere data i en hovedvisning, kan det være en god ide at bruge noget som `this.parmParentForm().updateLayout();` i en `click`-handlingsmetode. (Se klassen `JmgProductionFloorExecutionReportFeedbackAction` for at få et eksempel). Du skal blot sikre dig, at `parmDataSource` er angivet i `init`-metoden til den nye formular (`formCaller.parmDataSource(this.dataSource(1));`). Du kan se et eksempel på `JmgProductionFloorExecutionMainGrid`-formularen.

## <a name="card-view"></a>Kortvisning

Typografier kan kun anvendes på kontrolelementer til kortvisning, hvis følgende krav er opfyldt:

- Hver kortvisning er indeholdt i en formulargruppe.
- Gruppenavnet starter med `CardGroup` (f.eks. `CardGroupJobsView`).

I følgende illustration vises en kortvisning, der ikke indeholder nogen kontrolelementer.

![Kortvisning uden elementer.](media/pfe-styles-empty-card.png)

I følgende illustration vises kortvisninger, der indeholder kontrolelementer.

![Kort med elementer, der viser Hz.](media/pfe-styles-elements.png)

![Kort med elementer for en vedligeholdelsesanmodning.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visitkort

Typografier kan kun anvendes på kontrolelementer i visitkort, hvis følgende krav er opfyldt:

- Hvert visitkort er indeholdt i en formulargruppe.
- Gruppenavnet starter med `BusinessCardGroup` (f.eks. `BusinessCardGroupJobsList`).

Angiv følgende egenskaber på visitkortet:

- **Typografi:** *liste*
- **Udvidet typografi:** *cardList*
- **Flere val:g** *Nej*
- **Vis kolonneetiketter:** *Nej*

![Visitkort.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Alternativknap

Typografier kan kun anvendes på alternativknapper, hvis følgende krav er opfyldt:

- De enkelte alternativknapper er indeholdt i en formulargruppe.
- Gruppenavnet starter med `RadioTextBelow` eller `RadioTextRight`, afhængigt af hvor teksten skal vises.

Angiv følgende egenskaber på alternativknappen:

- **Til/fra-knap:** *Markér*
- **Til/fra-værdi:** *Til*, hvis alternativknappen skal være valgt, ellers *Fra*

I følgende illustration vises et eksempel, hvor teksten vises under alternativknapperne.

![Alternativknapper med tekst under.](media/pfe-styles-radio-text-below.png)

I følgende illustration vises et eksempel, hvor teksten vises til højre for alternativknapperne.

![Alternativknapper med tekst til højre.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Alternativknapper i Internet Explorer

Typografier for alternativknapper understøttes ikke i Internet Explorer. I følgende illustration vises, hvordan alternativknapper ser ud i Internet Explorer.

![Alternativknapper i Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Knapper

Typografier kan kun anvendes på knapper, hvis følgende krav er opfyldt:

- De grupper af knapper er indeholdt i en formulargruppe. Alle knapperne i gruppen har samme typografi.
- Der er ingen krav til navnet på gruppen.

Angiv følgende egenskaber på knapperne:

- **Knapvisning:** *TextWithImageLeft*
- **Normalt billede:** Denne egenskab må ikke være tom. Du kan for eksempel bruge *CoffeeScript*.
- **Tekst:** Denne egenskab må ikke være tom. Du kan for eksempel bruge *Start Break*.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Højde:** *Automatisk* eller *SizeToContent*

### <a name="primary-button"></a>Primær knap

Typografier kan kun anvendes på en primær knap, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `DefaultButtonGroup` eller `PrimaryButtonGroup` (f.eks. `DefaultButtonGroup10`).

![Primær knap.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundær knap

Typografier kan kun anvendes på en sekundær knap, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppen hedder **Højre panel**, eller gruppenavnet starter med `SecondaryButtonGroup`.

![Sekundær knap.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Tredje knap i gruppen

Typografier kan kun anvendes på tredje knap i gruppen, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppen hedder **Venstre panel**, eller gruppenavnet starter med `ThirdButtonGroup`.

![Tredje knap i gruppen.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Fjerde knap i gruppen

Typografier kan kun anvendes på fjerde knap i gruppen, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `FourthButtonGroup`.

Angiv følgende egenskaber på knappen:

- **Knapvisning:** *TextOnly*
- **Normalt billede:** Denne egenskab skal være tom.
- **Tekst:** Denne egenskab må ikke være tom. Du kan for eksempel bruge *Vis* eller *Rediger*.
- **Bredde:** *Automatisk*
- **Højde:** *Automatisk*

![Fjerde knap i gruppen.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Flad knap

Typografier kan kun anvendes på en flad knap, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `FlatButtonGroup`.

Angiv følgende egenskaber på knappen:

- **Knapvisning:** *ImageOnly*
- **Normalt billede:** Denne egenskab må ikke være tom. Du kan for eksempel bruge *CoffeeScript*.
- **Tekst:** Denne egenskab skal være tom.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Højde:** *Automatisk* eller *SizeToContent*

![Flad knap.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Knappen Fortsæt

Typografier kan kun anvendes på en Fortsæt-knap, hvis følgende krav er opfyldt:

- Knappen er indeholdt i en formulargruppe.
- Gruppenavnet starter med `ContinueButtonGroup`.

Angiv følgende egenskaber på knappen:

- **Knapvisning:** *ImageOnly*
- **Normalt billede:** *Fremad*
- **Tekst:** Denne egenskab skal være tom.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Højde:** *Automatisk* eller *SizeToContent*

![Knappen Fortsæt.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Kombinationsboks

Et kombinationsfelt er en kombination af tre kontrolelementer: et inputkontrolelement, en knap, der rydder inputkontrolelementet, og en knap, der kører en søgning.

Typografier kan kun anvendes på et kombinationsfelt, hvis følgende krav er opfyldt:

- Kombinationsfeltet er indeholdt i en formulargruppe.
- Gruppenavnet starter med `Combobox`.
- I gruppen er det første kontrolelement et af typen `AxFormStringControl`. Dette kontrolelement viser den aktuelle værdi, og det er her, brugeren angiver den ønskede værdi.
- Det andet kontrolelement er af typen `CommonButton`, og navnet starter med `ClearButton`. Denne knap skal indeholde kode, der bruger egenskaben `enable` til at vise eller skjule knappen. Hvis du for eksempel vil have vist eller skjule knappen **Ryd**, mens brugeren skriver oplysninger i inputkontrolelementet, kan du bruge følgende kode.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Du skal have én metode, hvor dataene angives i inputkontrolelementet. Aktivér knappen **Ryd** i denne metode. Her er et eksempel.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Brug følgende kode for metoden `clicked` for knappen **Ryd**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Angiv værdien for inputkontrolelementet, `AxFormStringControl`, når formularen initialiseres ved hjælp af metoden `init`. Hvis værdien ikke er tom, skal du aktivere knappen **Ryd**. Hvis værdien er tom, skal du deaktivere knappen **Ryd**.

- Det tredje kontrolelement er af typen `CommonButton`, og navnet starter med `SearchButton`.

I følgende illustration vises to kontrolelementer af typen kombinationsfelt. Kombinationsfeltet til venstre har et tomt tekstfelt, og knappen **Ryd** er deaktiveret. Kombinationsfeltet til højre har tekst i tekstfeltet, og knappen **Ryd** er aktiveret.

![Kombinationsfelter med og uden knappen Ryd.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Lynfiltrering

Kontrolelementet Lynfiltrering føjer et søgefelt til siden. Du kan anvende typografier på Lynfiltrering, hvis følgende krav er opfyldt:

- Lynfiltrering er indeholdt i en formulargruppe.
- Gruppenavnet starter med `SearchInputGroup`.
- I gruppen er det første kontrolelement af typen `QuickFilter`. (Her skal brugeren indtaste søgestrengen).
- Det andet kontrolelement er et `FormStaticTextControl` med navnet `NumberOfResults`. (Dette kontrolelement er valgfrit. Hvis det medtages, vises antallet af fundne elementer.)
- Det tredje kontrolelement er af typen `CommonButton`, og navnet starter med `ClearButton`.

I følgende illustration vises to kontrolelementer af typen lynfiltrering. Lynfiltrering til venstre har et tomt lynfilter, og antallet af resultater er ikke synligt. Lynfiltrering til højre indeholder en søgestreng og viser antallet af resultater.

![Eksempler på et kontrolelement af typen Lynfiltrering med og uden en søgestreng.](media/pfe-styles-quick-filter.png "Eksempler på et kontrolelement af typen Lynfiltrering med og uden en søgestreng")

## <a name="center-align-elements-on-a-tab"></a>Centrere elementer under en fane

Hvis du vil justere elementer i midten af en fane, skal gruppenavnet starte med `TabContentGroup`, og gruppen skal have følgende egenskaber:

- **Breddetilstand:** `SizeToAvailable`
- **Højdetilstand:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Justere et gitter, en detaljedel og et lynfilter

Hvis du vil arrangere et tilpasset gitter, en detaljedel og et lynfilter, så de ligner standarddesignet, skal du huske på følgende, når du sætter dem alle sammen:

- Hvis gitteret har et lynfilter, skal både gitteret og lynfilteret være i den gruppe, der har et navn, der starter med `GridGroup`.
- Hvis du vil anvende typografier på en detaljedel, skal gruppenavnet starte med `DetailInformationGroup`.

I følgende illustration vises et typisk gitter med et lynfilter og en detaljedel til højre.

![Typisk gitter med en detaljedel og et lynfilter.](media/pfe-styles-align-grid.png "Typisk gitter med en detaljedel og et lynfilter")

I Visual Studio kan et gitter, en detaljedel og et lynfilter oprettes ved hjælp af en struktur som f.eks. den, der vises i følgende illustration.

![Typisk kodestruktur, der justerer et gitter, en detaljedel og et lynfilter.](media/pfe-styles-header-code-structure2.png "Typisk kodestruktur, der justerer et gitter, en detaljedel og et lynfilter")

## <a name="additional-resources"></a>Yderligere ressourcer

- [Tilpasse grænsefladen til produktionsudførelse](production-floor-execution-customize.md)
- [Designe grænsefladen til produktionsudførelse](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
