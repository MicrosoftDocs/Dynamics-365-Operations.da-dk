---
title: Grænseflade til Report Designer
description: I denne artikel forklares, hvordan du navigerer gennem Report Designer, og hvordan du bruger de forskellige indstillinger til at opfylde dine specifikke krav.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e9b77e2b510a72d1e3fe3c68c997d58245a86a27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551572"
---
# <a name="report-designer-interface"></a>Grænseflade til Report Designer

[!include [banner](../includes/banner.md)]

I denne artikel forklares, hvordan du navigerer gennem Report Designer, og hvordan du bruger de forskellige indstillinger til at opfylde dine specifikke krav.

## <a name="report-designer-menu-commands"></a>Menukommandoer i Report Designer

I følgende tabel beskrives de menukommandoer og indstillinger, du kan bruge, når du designer økonomirapporter. Nogle menukommandoer og indstillinger er kun tilgængelige i bestemte sammenhænge. Kommandoer til at fremme og degradere rapporteringsenheder er eksempelvis kun tilgængelige, når du redigerer en rapporteringstrædefinition.

### <a name="file-menu"></a>Menuen Fil

Menuen **Filer** er tilgængelig for alle brugere og omfatter følgende kommandoer.

| Kommando                           | Beskrivelse |
|-----------------------------------|-------------|
| Ny                               | Opret en ny rapportdefinition, rækkedefinition, kolonnedefinition, rapporteringstrædefinition, rapportgruppedefinition eller mappe. Yderligere indstillinger er tilgængelige afhængigt af din brugerrolle. |
| Åbnet                              | Åbn en eksisterende rækkedefinition, kolonnedefinition, rapporteringstrædefinition eller rapportdefinition. |
| Afslutning                             | Luk den aktuelle byggesten. |
| Luk alle                         | Luk alle byggesten. |
| Gem                              | Gem den aktuelle rækkedefinition, kolonnedefinition, rapporteringstrædefinition eller rapportdefinition. |
| Gem som                           | Gem den aktuelle rækkedefinition, kolonnedefinition, rapporteringstrædefinition eller rapportdefinition under et nyt navn. |
| Egenskaber                        | Åbn dialogboksen **Egenskaber**, hvor du kan ændre navnet på og beskrivelsen af en rapport. |
| Generér                          | Generer den aktuelle rapport Denne kommando er tilgængelig fra en rapportdefinition. |
| Vis rapport                       | Åbn den seneste version af den genererede rapport i Finance and Operations. Denne kommando er tilgængelig fra en rapportdefinition, hvis du har oprettet mindst én rapport. |
| Seneste rapportdefinitioner         | Vis en liste over rapporter, der for nylig er oprettet eller ændret. Du kan derefter vælge en rapport på listen. |
| Seneste rækkedefinitioner            | Vis en liste over rækkedefinitioner, der for nylig er oprettet eller ændret. Du kan derefter vælge en rækkedefinition på listen. |
| Seneste kolonnedefinitioner         | Vis en liste over kolonnedefinitioner, der for nylig er oprettet eller ændret. Du kan derefter vælge en kolonnedefinition på listen. |
| Seneste rapporteringstrædefinitioner | Vis en liste over rapporteringstrædefinitioner, der for nylig er oprettet eller ændret. Du kan derefter vælge en rapporteringstrædefinition på listen. |
| Afslut                              | Afslut Report Designer. |

### <a name="edit-menu"></a>Menuen Rediger

Menuen **Rediger** er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. Menuen indeholder følgende komponenter.

| Kommando                                | Beskrivelse |
|----------------------------------------|-------------|
| Fortryd                                   | Fortryd den sidste handling. |
| Gentag                                   | Annuller den sidste fortrudte handling. |
| Klip                                    | Slet den markerede tekst, og kopiér den til Udklipsholder. |
| Kopier                                   | Kopiér det valgte tekst til Udklipsholder. |
| Indsæt                                  | Indsæt den senest klippede eller kopierede tekst fra Udklipsholder. |
| Ryd                                  | Slet indholdet af den valgte byggestenscelle. |
| Søg                                   | Åbn dialogboksen **Søg og Erstat**, hvor du kan søge efter tekst i visningsruden. |
| Erstatte                                | Åbn dialogboksen **Søg og Erstat**, hvor du kan søge efter og erstatte tekst i visningsruden. |
| Indsæt rækker fra dimensioner            | Åbn dialogboksen **Indsæt rækker fra dimensioner**, hvor du kan vælge de dimensionsværdier, der skal medtages i rækkedefinitionen. Denne kommando er tilgængelig fra en rækkedefinition. |
| Omnummerer rækker                          | Omnummerer alle numeriske rækkekoder. Denne kommando er tilgængelig fra en rækkedefinition. |
| Link til række                              | Åbn dialogboksen **Links til række**, hvor du kan angive kilder til datalinks i rækkedefinitioner og rapporteringstrædefinitioner. Denne kommando er tilgængelig fra en rækkedefinition. |
| Afrundingsdifference                    | Åbn dialogboksen **Afrundingsdifference**, hvor du kan angive parametrene for afrunding. Denne kommando er tilgængelig fra en rækkedefinition. |
| Administrer dimensionsopsætninger                  | Åbn dialogboksen **Dimensionsopsætninger,**, hvor du kan oprette og redigere dimensionsopsætninger. Denne kommando er tilgængelig fra en rækkedefinition eller rapporteringstrædefinition. |
| Indsæt række                             | Indsæt en tom række i rækkedefinitionen eller en tom kolonneoverskrift i kolonnedefinitionen. Denne kommando er tilgængelig fra en rækkedefinition eller kolonnedefinition. |
| Slet række                             | Slet den markerede række fra rækkedefinitionen eller den markerede kolonneoverskrift fra kolonnedefinitionen. Denne kommando er tilgængelig fra en rækkedefinition eller kolonnedefinition. |
| Indsæt kolonne                          | Indsæt en tom kolonne i kolonnedefinitionen. Denne kommando er tilgængelig fra en kolonnedefinition. |
| Slet kolonne                          | Slet den markerede kolonne i kolonnedefinitionen. Denne kommando er tilgængelig fra en kolonnedefinition. |
| Indsæt rapporteringsenheder fra dimensioner | Åbn dialogboksen **Indsæt rapporteringsenheder fra dimensioner**, hvor du kan vælge de dimensionsværdier, der skal medtages i rapporteringstrædefinitionen. Denne kommando er tilgængelig fra en rapporteringstrædefinition. |
| Importer hierarki for dimensionsopsætning         | Åbn dialogboksen **Hierarki for dimensionsopsætning**, hvor du kan importere et hierarki for dimensionsopsætning fra de økonomiske data. Denne kommando er tilgængelig fra en rapporteringstrædefinition for et ..\\financial-dimensions\\dimensionsbaseret system. |
| Indsæt enhed i trædiagram                  | Indsæt en tom række i definitionen af rapporteringstræet. Denne kommando er tilgængelig fra en rapporteringstrædefinition. |
| Slet rapporteringsenhed                  | Slet den markerede række for rapporteringsenhed fra definitionen af rapporteringstræ. Denne kommando er tilgængelig fra en trædiagramdefinition. |

### <a name="view-menu"></a>Menuen Vis

Menuen **Vis** er tilgængelig for alle brugere og omfatter følgende kommandoer.

| Kommando         | Beskrivelse                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigationsrude | Få vist eller skjule navigationsruden.                                      |
| Værktøjslinjer        | Vælg værktøjslinjer, der er synlige.                                  |
| Statuslinje      | Vise eller skjule oplysninger om status i det vinduet **Report Designer**. |
| Velkomstside    | Åbn siden **Velkommen**.                                             |

### <a name="format-menu"></a>Menuen Formater

Menuen **Formater** er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. Menuen indeholder følgende komponenter.

| Kommando               | Beskrivelse |
|-----------------------|-------------|
| Typografier og formatering | Åbn dialogboksen **Typografier og formatering**, hvor du kan oprette og ændre typografien for tekst i rækkedefinitioner og kolonnedefinitioner. Denne kommando er tilgængelig fra en rækkedefinition eller en kolonnedefinition. |
| Kolonnebredde          | Åbn dialogboksen **Kolonnebredde**, hvor du kan angive bredden af den valgte kolonne. Denne kommando er tilgængelig fra en rækkedefinition, en kolonnedefinition eller en rapporteringstrædefinition. |
| Skjul                  | Skjul den markerede kolonne. Denne kommando er tilgængelig fra en rækkedefinition, en kolonnedefinition eller en rapporteringstrædefinition. |
| Vis                | Gør skjulte kolonner mellem de markerede kolonner synlige. Denne kommando er tilgængelig fra en rækkedefinition, en kolonnedefinition eller en rapporteringstrædefinition. |

### <a name="company-menu"></a>Menuen Regnskab

Menuen **Regnskab** er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. Menuen indeholder følgende komponenter.

| Kommando               | Beskrivelse                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Regnskaber             | Åbn dialogboksen **Regnskaber**, hvor du kan oprette og redigere regnskaber.                                          |
| Dokumentkomponentgrupper | Åbn dialogboksen **Dokumentkomponentgrupper**, hvor du kan oprette, redigere, importere og eksportere dokumentkomponentgrupper. |

### <a name="go-menu"></a>Menuen Gå

Menuen **Søg** er tilgængelig for alle brugere, og den indeholder nedenstående kommandoer.

> [!NOTE]
> Disse kommandoer har ikke nogen synlig effekt, medmindre navigationsruden vises.

| Kommandoer                   | Beskrivelse                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Rapportdefinitioner         | Vis rapportdefinitioner i navigationsruden.                                    |
| Rækkedefinitioner            | Vis rækkedefinitioner i navigationsruden.                                       |
| Kolonnedefinitioner         | Vis kolonnedefinitioner i navigationsruden.                                    |
| Rapporteringstrædefinitioner | Vis rapporteringstrædefinitioner i navigationsruden.                            |
| Sikkerhed                   | Vis oplysninger om sikkerhed for brugere, grupper og virksomheder i navigationsruden. |

### <a name="tools-menu"></a>Menuen Funktioner

Menuen **Funktioner** er tilgængelig for alle brugere, men nogle kommandoer har begrænset tilgængelighed. Menuen indeholder følgende komponenter.

| Kommando                       | Beskrivelse |
|-------------------------------|-------------|
| Beskyt                       | Anvend en adgangskode til den aktuelle byggesten. Denne kommando er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| Status for rapportkø           | Åbn dialogboksen **Status for rapportkø**, hvor du kan se alle de senest oprettede rapporter og detaljer for hver rapport. |
| Oplysninger om kildesystem     | Vis indstillingerne for Microsoft Dynamics ERP-systemet. Denne kommando er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| Udtjekkede elementer             | Få vist rækkedefinitioner, kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, der er åbne. Denne kommando er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| Opdater cachelagrede økonomiske data | Opdater dataene i kolonnen med økonomiske dimensioner. |
| Indstilling                       | Åbn dialogboksen **Indstillinger**, hvor du kan ændre brugerindstillinger for Report Designer. |

### <a name="window-menu"></a>Menuen Vindue

Menuen **Vindue** er tilgængelig for alle brugere og omfatter følgende kommandoer.

| Kommando              | Beskrivelse |
|----------------------|-------------|
| Delt vandret    | Vis alle åbne vinduer ved siden af hinanden. |
| Delt lodret      | Vis alle åbne vinduer oven over hinanden. |
| Overlappet              | Placer alle åbne vinduer oven på hinanden, så titellinjen for hver vindue er synlig. |
| Frys vandret    | Fryse den markerede række så denne række fortsætter med at være synlig i vinduet, når du ruller. Denne kommando er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| Frys lodret      | Frys den markerede kolonne, så denne kolonne fortsætter med at være synlig i vinduet, når du ruller. Denne kommando er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| Liste over åbne vinduer | Vis en liste over vinduer, der er åbne. Vælg et vindue, der skal placeres forrest. |

### <a name="help-menu"></a>Menuen Hjælp

Menuen **Hjælp** er tilgængelig for alle brugere og omfatter følgende kommandoer.

| Kommando | Betegnelse                                                              |
|---------|--------------------------------------------------------------------------|
| Hjælp    | Åbn Finance and Operations-siden med Hjælp-emnet om økonomirapportering. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Knapper på værktøjslinjen i Report Designer
I følgende tabel beskrives de værktøjslinjeknapper, du kan bruge, når du opretter rapporter. Nogle værktøjslinjeknapper er kun tilgængelige under bestemte forhold. Knapperne til at fremme og degradere rapporteringsenheder er eksempelvis kun tilgængelige, når du redigerer en rapporteringstrædefinition.

### <a name="standard-toolbar"></a>Standardværktøjslinje

Standardværktøjslinjen giver hurtig adgang til fil- og redigeringskommandoer. Denne værktøjslinje indeholder følgende knapper.

| Knap                                                                                       | Beskrivelse |
|----------------------------------------------------------------------------------------------|-------------|
| [![Knappen Ny](./media/rowc130389.png)](./media/rowc130389.png)                              | Opret en ny (tom) rapportdefinition, rækkedefinition, kolonnedefinition eller rapporteringstrædefinition. |
| [![Knappen Åbn](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Åbn en eksisterende rækkedefinition, kolonnedefinition, rapporteringstrædefinition eller rapportdefinition. |
| [![Knappen Gem](./media/savec130389.png)](./media/savec130389.png)                           | Gem den aktuelle rækkedefinition, kolonnedefinition, rapporteringstrædefinition eller rapportdefinition. |
| [![Knappen Kopiér](./media/copyc130389.png)](./media/copyc130389.png)                           | Kopiér det valgte tekst til Udklipsholder. |
| [![Knappen Klip](./media/cutc130389.png)](./media/cutc130389.png)                              | Slet den markerede tekst, og kopiér den til Udklipsholder. |
| [![Knappen Sæt ind](./media/pastec130389.png)](./media/pastec130389.png)                        | Indsætte tekst fra Udklipsholder. |
| [![Knappen Fortryd](./media/undoc130389.png)](./media/undoc130389.png)                           | Fortryd den sidste handling. |
| [![Knappen Annuller Fortryd](./media/redoc130389.png)](./media/redoc130389.png)                           | Annuller den sidste fortrudte handling. |
| [![Knappen Søg](./media/findc130389.png)](./media/findc130389.png)                           | Åbn dialogboksen **Søg og erstat**, hvor du kan søge efter og erstatte tekst i det aktive vindue. |
| [![Knappen Indsæt række](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Indsæt en tom række i rækkedefinitionen eller en tom kolonneoverskrift i kolonnedefinitionen. Denne knap er tilgængelig fra en rækkedefinition eller kolonnedefinition. |
| [![Knappen Indsæt kolonne](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Indsæt en tom kolonne i kolonnedefinitionen. Denne knap er tilgængelig fra en kolonnedefinition. |
| [![Knappen Lås](./media/lockc130389.png)](./media/lockc130389.png)                           | Anvend en adgangskode til den aktuelle byggesten. Denne knap er tilgængelig for brugere, der har rollen **Designer** eller **Administrator**. |
| [![Knappen Link med række](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Åbn dialogboksen **Links til række**, hvor du kan angive kilder til datalinks i rækkedefinitioner og rapporteringstrædefinitioner. Denne knap er tilgængelig fra en rækkedefinition. |
| [![Knappen Hæv](./media/promotec130389.png)](./media/promotec130389.png)                  | Hæv en enhed for rapporteringtrædefinitionen. Når du vælger en underordnet enhed og derefter klikker på **Hæv**, flyttes den underordnede enhed til det samme niveau som den overordnede enhed. |
| [![Knappen Sænk](./media/demotec130389.png)](./media/demotec130389.png)                     | Sænk en enhed for rapporteringtrædefinitionen. Når du vælger en enhed og derefter klikker på **Sænk**, underordnes enheden den enhed, der står foran den. |
| [![Knappen Udvid](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Udvid alle enheder i rapporteringstrædefinitionen på niveauet for den valgte enhed. |
| [![Knappen Skjul](./media/collapsec130389.png)](./media/collapsec130389.png)               | Skjul rapporteringstræet. |
| [![Knappen Hjælp](./media/helpc130389.png)](./media/helpc130389.png)                           | Åbn Hjælp. |

### <a name="formatting-toolbar"></a>Formateringsværktøjslinje

Formateringsværktøjslinjen giver nem adgang til formateringskommandoer. Denne værktøjslinje indeholder følgende knapper.

| Knap                                                                                                       | Beskrivelse                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Knappen Typografi](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Anvend den valgte typografi på den aktuelle tekst.      |
| [![Knappen Skrifttype](./media/fonttype.png)](./media/fonttype.png)                                                 | Anvend den valgte typografi på den aktuelle tekst.              |
| [![Knappen Skriftstørrelse](./media/fontsize.png)](./media/fontsize.png)                                            | Anvend den valgte skriftstørrelse (i punkter) på den aktuelle tekst. |
| [![Knappen Fed](./media/boldc130389.png)](./media/boldc130389.png)                                           | Gør den aktuelle tekst fed.                             |
| [![Knappen Kursiv](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Kursiver den aktuelle tekst.                           |
| [![Knappen Understreg](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Understreg den aktuelle tekst.                             |
| [![Knappen Formindsk indrykning](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Formindsk indrykning for den aktuelle tekst.                |
| [![Knappen Forøg indrykning](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Forøg indrykning for den aktuelle tekst.                |
| [![Knappen Baggrundsfarve](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Rediger baggrundsfarven for den aktuelle celle.        |
| [![Knappen Skriftfarve](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Rediger farven for den aktuelle tekst.                   |

### <a name="report-designer-toolbar"></a>Værktøjslinjen i Report Designer

Report Designer-værktøjslinjen giver hurtig adgang til kommandoer til navigering i rapportdesigneren. Denne værktøjslinje indeholder følgende knapper.

| Knap                                                                                              | Beskrivelse |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Knappen Rapportdefinition](./media/reportc130389.png)](./media/reportc130389.png)                 | Vis den rapportdefinition, der er angivet i menuen **Vindue**. |
| [![Knappen Rækkedefinition](./media/rowc130389.png)](./media/rowc130389.png)                          | Vis den rækkedefinition, der er tilknyttet den aktive rapportdefinition. |
| [![Knappen kolonnedefinition](./media/columnc130389.png)](./media/columnc130389.png)                 | Vis den kolonnedefinition, der er tilknyttet den aktive rapportdefinition. |
| [![Knappen Rapporteringstrædefinition](./media/treec130389.png)](./media/treec130389.png)             | Vis den rapporteringstrædefinition, der er tilknyttet den aktive rapportdefinition. |
| [![Knappen Rapportfremviser](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Start Rapportfremviser, og vis den seneste version af den genererede rapport. Denne knap er tilgængelig fra en rapportdefinition, hvis du har oprettet mindst én rapport. |
| [![Knappen Generer rapport](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Generer en rapport fra den aktive rapportdefinition. Denne knap er tilgængelig fra en rapportdefinition. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Økonomirapportering](financial-reporting-intro.md)

[Generere en økonomirapport](generate-financial-report.md)
