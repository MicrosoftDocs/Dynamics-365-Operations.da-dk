---
title: "Komponenter i økonomisk rapport"
description: "I denne artikel beskrives, hvordan komponenter, eller dokumentkomponenter, i rapportdefinitioner bruges til økonomirapportering. Disse komponenter omfatter rækkedefinitioner, kolonnedefinitioner og rapporteringstræ-definitioner. I artiklen forklares, hvordan du organiserer og låser komponenter, og hvordan du arbejder med dokumentkomponentgrupper."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 057c338c11518b3a1081223e432cbfd109d5e679
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="financial-report-components"></a>Komponenter i økonomisk rapport

[!include[banner](../includes/banner.md)]


I denne artikel beskrives, hvordan komponenter, eller dokumentkomponenter, i rapportdefinitioner bruges til økonomirapportering. Disse komponenter omfatter rækkedefinitioner, kolonnedefinitioner og rapporteringstræ-definitioner. I artiklen forklares, hvordan du organiserer og låser komponenter, og hvordan du arbejder med dokumentkomponentgrupper. 

Designfilosofien bag designeren til økonomirapporter er at opdele oplysninger i det mindste komponent eller dokumentkomponent og derefter mixe og matche komponenterne efter behov. Derfor er rapportformateringen adskilt fra de økonomiske data, og du kan ændre designet af en rapport uden at ændre de økonomiske data i Microsoft Dynamics ERP-systemet. Ved hjælp af denne metode med byggesten, kan du kombinere tekst, beløb og beregninger for at producere de rapporter, du har brug for. Desuden fremmer denne fleksibilitet kreativitet ved at gøre det nemt for dig at se dine handlinger på forskellige måder. De enkelte komponenter i en rapportdefinition svarer til et tredimensionalt regneark, men de er mere effektive. En rapportdefinition angiver den rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition, der skal bruges til rapporten. Den indeholder også oplysninger om, hvor rapporten, der genereres, skal gemmes, og hvordan den formateres. For at øge muligheden for genbrug og deling, kan du oprette en komponentgruppe, som er en samling af eksisterende rapportdefinitioner, rækkedefinitioner, kolonnedefinitioner, rapporteringstrædefinitioner og dimensionsopsætninger, der er tilknyttet en virksomhed.

## <a name="building-blocks-of-a-report"></a>Komponenter i en rapport
| Komponent            | Beskrivelse                                                                                                                                                                                                                                                                              | Hvis du vil have flere oplysninger                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Definition af række            | En rækkedefinition definerer de beskrivende linjer (f.eks. lønninger eller salg) i en rapport. Den viser også de segmentværdier eller dimensioner, der indeholder værdierne for hvert linjeelement og indeholder en rækkeformateringer og beregninger.                                                    | [Rækkedefinitioner](row-definitions-financial-reporting.md)                       |
| Kolonnedefinition         | En kolonnedefinition definerer den periode, der skal bruges, når data udtrækkes fra de økonomiske dimensioner. Den indeholder også kolonneformatering og beregninger.                                                                                                                                 | [Kolonnedefinitioner](column-definitions-financial-reports.md)         |
| Rapporteringstrædefinition | En rapporteringstrædefinition ligner et organisationsdiagram. Den indeholder individuelle rapporteringsenheder, der repræsenterer de enkelte bokse i diagrammet. Enhederne, der kan være enkelte afdelinger fra de økonomiske data eller enheder på et højere niveau, der opsummerer data fra andre rapporteringsenheder. | [Rapporteringstrædefinitioner](financial-reporting-tree-definitions.md) |
| Rapportdefinition         | En rapportdefinition anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at opbygge en rapport. Den indeholder også flere muligheder og indstillinger, som du kan bruge til at tilpasse en rapport.                                                                    | [Rapportdefinition](design-financial-report-definitions.md)                  |

Hvis du ikke er vant til at designe rapporter, vil du sikker finde det fordelagtigt at benytte rapportguiden til hurtigt at oprette en rapportdefinition, der kan tilpasses senere. Hvis du har erfaring med at designe rapporter og ønsker mere fleksibilitet for rapportdesign, kan du kombinere nye eller eksisterende komponenter for at oprette en ny rapportdefinition. Du behøver ikke fuldt ud at forstå alle tilgængelige rapportdefinitionsindstillinger til fremstilling af kvalitetsrapporter. Efterhånden som du bliver fortrolig med at designe rapporter, kan du udvide dine rapportdefinitioner for at drage fordel af mere avancerede funktioner. Når du har oprettet en grundlæggende rapport, kan du tilpasse rapportdefinitionen og komponenterne i rapportdefinitionen.

## <a name="organize-the-building-blocks"></a>Organisere komponenterne
Du kan bruge mapper til at organisere dine komponenter i Report Designer. Alle mapper er specifikke for den komponenttype, de indeholder. Alle mapper, der indeholder rækkedefinitioner, er for eksempel placeret i ruden **Rækkedefinitioner** i Report Designer.

### <a name="create-a-folder"></a>Oprette en mappe

1.  Vælg i Report Designer den type komponent, du vil organisere i navigationsruden. Hvis du for eksempel vil sortere en rækkedefinition, skal du klikke på **Rækkedefinitioner**.
2.  I navigationsruden skal du vælge den eksisterende mappe, som den nye mappe skal oprettes under, og derefter udføre et af disse trin:
    -   Højreklik på den overordnede mappe, og klik derefter på **Ny mappe**.
    -   Vælg den overordnede mappe, og klik på **Filer**, og klik derefter på **Ny mappe**.

3.  Når den nye mappe vises, skal du skrive navnet på den nye mappe, og derefter trykke på Enter.

## <a name="lock-a-building-block"></a>Låse en komponent
Du kan oprette en adgangskode for at låse og hjælpe med at beskytte en dokumentkomponent. På denne måde kan du føje en grad af sikkerhed til en rapportkomponent, uden at hele systemet beskyttes. En adgangskode kan medvirke til at beskytte komponentoplysninger, der er vigtige for rapporteringsprocessen i forbindelse med månedsafslutningen. En bruger med en rolle kan låse en dokumentkomponent. Andre brugere har dog altid skrivebeskyttet adgang til en låst komponent. Brugere kan åbne, redigere og gemme den låste komponent under et nyt navn. En bruger med rollen administrator kan altid få adgang til og ændre en låst komponent.
1.  Åbn den rapportkomponent, der skal låses, i Report Designer, for eksempel en rækkedefinition, kolonnedefinition, rapportdefinition eller rapporteringstrædefinition.
2.  Klik på **Beskyt/Fjern beskyttelse** i menuen **Værktøjer**. Du kan også klikke på **Beskyt/Fjern beskyttelse** (låseikonet) på værktøjslinjen.
3.  I dialogboksen **Beskyt** skal du indtaste og bekræfte en adgangskode og derefter klikke på **OK**. Låseikonet på værktøjslinjen er markeret, når en åben komponent er låst.

Hvis du vil låse en låst komponent op, skal du åbne komponenten og derefter klikke på **Beskyt/Fjern beskyttelse** på værktøjslinjen. Du kan også klikke på **Fjern beskyttelse** i menuen **Værktøjer**.

## <a name="building-block-groups"></a>Dokumentkomponentgrupper

Komponenter er de rækkedefinitioner, kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, du opretter for en rapport. Komponentgrupper er samlinger af de definitioner og dimensionsopsætninger, der er tilknyttet en virksomhed. Komponentgrupper kan være firmaspecifikke, eller flere firmaer kan dele det samme sæt komponenter. Hvis nogle af dine firmaer har en anden kontoplan, kan du evt. bruge en anden komponentgruppe for hvert firma. Alternativt kan du evt. give alle dine individuelle komponenter et navn, der afspejler, hvilket firma de er kompatible med.
### <a name="create-a-building-block-group"></a>Oprette komponentgruppe

1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  Klik på **Ny** i dialogboksen **Komponentgrupper**.
3.  Angiv et entydigt navn og en beskrivelse for komponentgruppen. Hvert felt kan indeholde op til 256 tegn. (Dette tal omfatter mellemrum).
4.  Klik på **OK** for at oprette den nye komponentgruppe.

### <a name="assign-a-building-block-group"></a>Tildel en komponentgruppe

Når du har en oprettet en komponentgruppe, skal du tildele den til mindst ét firma. Du kan derefter oprette rapport-, række-, kolonne- og rapporteringstrædefinitioner og gemme dem i komponentgruppen. Før du begynder nedenstående procedure, skal du lukke alle komponenter.
1.  Klik på **Firmaer** i menuen **Firma** i Report Designer.
2.  I dialogboksen **Regnskaber** skal du vælge det regnskab, som du vil tildele en komponentgruppe.
3.  Klik på **Rediger**.
4.  I dialogboksen **Rediger regnskab** i feltet **Komponentgruppe** skal du vælge den komponentgruppe, der skal tildeles virksomheden, eller du kan klikke på **Ny** for at oprette en ny komponentgruppe.
5.  Klik på **OK** for at tildele komponentgruppen.
6.  Klik på **Luk** for at lukke dialogboksen **Regnskaber**. Den komponentgruppe, du har valgt, er nu knyttet til virksomheden. Nu er alle nye rækkedefinitioner, kolonnedefinitioner osv., der er blevet oprettet, en del af den komponentgruppe, der er tildelt til denne virksomhed. Du kan også importere en .tdbx-fil eller rapport fra et andet system.

### <a name="view-a-building-block-group"></a>Vise en komponentgruppe

Når en dokumentkomponentgruppe er oprettet og taget i brug, kan du se alle de dokumentkomponenter, der er tildelt til den. Du kan også eksportere eller importere en dokumentkomponentgruppe og udføre yderligere vedligeholdelse på dokumentkomponentgrupper.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  I dialogboksen **Komponentgrupper** skal du vælge den komponent, du vil have vist.
3.  Klik på **Vis** for at åbne dialogboksen **Vis komponentgruppe**, hvor du kan få vist indholdet af komponentgruppen.
4.  Klik på **Luk** for at lukke dialogboksene.

### <a name="save-a-building-block-group-under-a-new-name"></a>Gemme en komponentgruppe under et nyt navn

Du kan gemme en eksisterende komponentgruppe under et nyt navn. Derefter kan du ændre den nye komponentgruppe uden at ændre den oprindelige komponentgruppe.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  I dialogboksen **Komponentgrupper** skal du vælge den komponentgruppe, der skal gemmes, under et nyt navn.
3.  Klik på **Gem som**.
4.  Angiv et nyt navn og en beskrivelse for komponentgruppen.
5.  Klik på **OK**. Den nye komponentgruppe vises i dialogboksen **Komponentgrupper**.

### <a name="export-a-building-block-group"></a>Eksportere en komponentgruppe

Du kan eksportere en dokumentkomponentgruppe eller bestemte rapportkomponenter i en dokumentkomponentgruppe. Du kan bruge den eksporterede dokumentkomponentgruppe som sikkerhedskopi. Du kan også kopiere de eksporterede data mellem komponentgrupper eller Dynamics 365 for Operations-installationer. Report Designer omfatter de refererede typografier og dimensionsopsætninger sammen med komponentgruppen.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  I dialogboksen **Komponentgrupper** skal du vælge den komponentgruppe, der skal eksporteres, og derefter klikke på **Eksportér**.
3.  I dialogboksen **Eksportér** skal du vælge de rapportdefinitioner, der skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer under en fane. **Bemærk:** Når du vælger rapporter til eksport, markeres de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.

4.  Når du er færdig med at markere elementer til eksport, skal du klikke på **Eksportér**.
5.  I dialogboksen **Gem som** skal du vælge den placering, som komponentgruppen skal eksporteres til.
6.  Angiv et navn til filen i feltet **Filnavn**. Report Designer tilføjer automatisk filtypenavnet .tdbx.
7.  Klik på **Gem**. Komponentgruppen gemmes på den placering, du har angivet.

### <a name="import-a-building-block-group"></a>Importere en komponentgruppe

Du kan importere en dokumentkomponentgruppe til en eksisterende dokumentkomponentgruppe, eller du kan oprette en ny dokumentkomponentgruppe til dataene. Alle importerede dokumentkomponentgrupper bevarer deres oprindelige typografier og firmareferencer og omfatter de relevante dimensionssæt.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  I dialogboksen **Komponentgrupper** skal du vælge den komponentgruppe, som en komponentgruppe skal importeres til, og derefter klikke på **Importér**.
3.  I dialogboksen **Åbn** skal du vælge den komponentgruppe, der skal importeres, og derefter klikke på **Åbn**.
4.  I dialogboksen **Importér** skal du vælge de rapportdefinitioner, der skal importeres:
    -   Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.

5.  Når du er færdig med at markere elementer til import, skal du klikke på **Importér**.

### <a name="undo-a-checkout-of-a-building-block"></a>Fortryde udtjekning af en komponent

Når du åbner en dokumentkomponent, kan andre brugere få skrivebeskyttet adgang til denne komponent. Nogle gange glemmer en bruger måske at lukke en komponent eller lukker sit system uden at lukke komponenten. Det indebærer, at komponenten forbliver tjekket ud, og at ingen andre brugere kan åbne den. I sådanne situationer kan en økonomirapporteringsadministrator bruge dialogboksen **Udtjekkede elementer** til at tjekke komponenter ind, som brugere har efterladt i udtjekket tilstand. **Bemærk**: Du skal have rollen administrator for at tjekke komponenter ind ved hjælp af dialogboksen **Udtjekkede elementer**.
1.  I Report Designer skal du klikke på **Udtjekkede elementer** i menuen **Funktioner**.
2.  I dialogboksen **Udtjekkede elementer** skal du vælge **Vis elementer fra alle brugere**. Listen opdateres, så alle de komponenter, der er checket ud, og de brugere, der har tjekket dem ud, vises.
3.  Vælg en komponent, og klik derefter på **Fortryd udtjekning**.
4.  Klik på **Ja** for at tjekke komponenten ind.

# <a name="see-also"></a>Se også

[Økonomirapportering](financial-reporting-intro.md)




