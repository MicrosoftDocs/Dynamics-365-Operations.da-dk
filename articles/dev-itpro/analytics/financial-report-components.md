---
title: "Komponenter i økonomisk rapport"
description: "I denne artikel beskrives, hvordan komponenter, eller dokumentkomponenter, i rapportdefinitioner bruges til økonomirapportering. Disse komponenter omfatter rækkedefinitioner, kolonnedefinitioner og rapporteringstræ-definitioner. I artiklen forklares, hvordan du organiserer og låser komponenter, og hvordan du arbejder med dokumentkomponentgrupper."
author: aprilolson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b283b8550bd7e5eff969d45c761d0a54d93a33e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="financial-report-components"></a>Komponenter i økonomisk rapport

[!include[banner](../includes/banner.md)]


I denne artikel beskrives, hvordan komponenter, eller dokumentkomponenter, i rapportdefinitioner bruges til økonomirapportering. Disse komponenter omfatter rækkedefinitioner, kolonnedefinitioner og rapporteringstræ-definitioner. I denne artikel forklares, hvordan du organiserer og låser rapportkomponentgrupper. 

Designfilosofien bag designeren til økonomirapporter er at opdele oplysninger i det mindste komponent eller dokumentkomponent og derefter mixe og matche komponenterne efter behov. Derfor er rapportformateringen adskilt fra de økonomiske data, og du kan ændre designet af en rapport uden at ændre de økonomiske data i Microsoft Dynamics ERP-systemet. Ved hjælp af denne metode med byggesten, kan du kombinere tekst, beløb og beregninger for at producere de rapporter, du har brug for. Desuden fremmer denne fleksibilitet kreativitet ved at gøre det nemt for dig at se dine handlinger på forskellige måder. De enkelte komponenter i en rapportdefinition svarer til et tredimensionalt regneark, men de er mere effektive. En rapportdefinition angiver den rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition, der skal bruges til rapporten. Den indeholder også oplysninger om, hvor rapporten, der genereres, skal gemmes, og hvordan den formateres. 

## <a name="building-blocks-of-a-report"></a>Komponenterne i en rapport
| Komponent            | Betegnelse                     | Hvis du vil have flere oplysninger                                    |
|---------------------------|---------------------------------|---------------------------------------------------------|
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

Komponenter er de rækkedefinitioner, kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, du opretter for en rapport. Rapportkomponentgrupper er samlinger af definitioner og dimensionsgrupper. 


### <a name="view-a-building-block-group"></a>Få vist en rapportkomponentgruppe

Du kan få vist alle de rapportkomponenter, der er knyttet til en rapportkomponentgruppe. Du kan også eksportere eller importere en rapportkomponentgruppe.
1.  Klik på **Rapportkomponentgrupper** i menuen **Firma** i Rapportdesigner.
2.  I dialogboksen **Komponentgrupper** skal du vælge den komponent, du vil have vist.
3.  Klik på **Vis** for at åbne dialogboksen **Vis komponentgruppe**, hvor du kan få vist indholdet af komponentgruppen.
4.  Klik på **Luk** for at lukke dialogboksene.

### <a name="export-a-building-block-group"></a>Eksportere en rapportkomponentgruppe

Du kan eksportere en rapportkomponentgruppe eller bestemte rapportkomponenter i en rapportkomponentgruppe. Du kan bruge den eksporterede rapportkomponentgruppe som en sikkerhedskopi. Du kan også kopiere de eksporterede data mellem installationer af Finance and Operations. Report Designer omfatter de refererede typografier og dimensionsopsætninger sammen med komponentgruppen.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  Markér den rapportkomponentgruppe, du vil eksportere, i dialogboksen **Rapportkomponentgrupper**, og klik derefter på **Eksportér**.
3.  I dialogboksen **Eksportér** skal du vælge de rapportdefinitioner, der skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane. **Bemærk:** Når du vælger rapporter til eksport, vælges de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.

4.  Når du er færdig med at markere elementer til eksport, skal du klikke på **Eksportér**.
5.  I dialogboksen **Gem som** skal du vælge den placering, som komponentgruppen skal eksporteres til.
6.  Angiv et navn til filen i feltet **Filnavn**. Report Designer tilføjer automatisk filtypenavnet .tdbx.
7.  Klik på **Gem**. Komponentgruppen gemmes på den placering, du har angivet.

### <a name="import-a-building-block-group"></a>Importere en komponentgruppe

Du kan importere en rapportkomponentgruppe til en eksisterende rapportkomponentgruppe. Alle importerede dokumentkomponentgrupper bevarer deres oprindelige typografier og firmareferencer og omfatter de relevante dimensionssæt.
1.  Klik på **Komponentgrupper** i menuen **Regnskab** i Report Designer.
2.  Markér den rapportkomponent, du vil importere en rapportkomponentgruppe til, i dialogboksen **Rapportkomponentgrupper**, og klik derefter på **Importér**.
3.  Markér den rapportkomponentgruppe, der skal importeres, i dialogboksen **Åbn**, og klik derefter på **Åbn**.
4.  I dialogboksen **Importér** skal du vælge de rapportdefinitioner, der skal importeres:
    -   Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.

5.  Når du er færdig med at markere elementer til import, skal du klikke på **Importér**.

### <a name="undo-a-checkout-of-a-building-block"></a>Fortryde udtjekning af en komponent

Når du åbner en dokumentkomponent, kan andre brugere få skrivebeskyttet adgang til denne komponent. Nogle gange glemmer en bruger måske at lukke en komponent eller lukker sit system uden at lukke komponenten. Det indebærer, at komponenten forbliver tjekket ud, og at ingen andre brugere kan åbne den. I disse situationer kan en administrator for økonomisk rapportering bruge dialogboksen **Elementer, der er tjekket ud** til at tjekke byggesten ind, som brugere har efterladt som tjekket ud. **Bemærk:** Du skal have rollen som administrator for at tjekke byggesten ind ved hjælp af dialogboksen **Elementer, der er tjekket ud**.
1.  I Report Designer skal du klikke på **Udtjekkede elementer** i menuen **Funktioner**.
2.  Vælg **Vis elementer fra alle brugere** i dialogboksen **Elementer, der er tjekket ud**. Listen opdateres, så den viser alle de rapportkomponenter, der er tjekket ud, og de brugere, der har tjekket dem ud.
3.  Vælg en komponent, og klik derefter på **Fortryd udtjekning**.
4.  Klik på **Ja** for at tjekke komponenten ind.

## <a name="see-also"></a>Se også

[Økonomirapportering](financial-reporting-intro.md)




