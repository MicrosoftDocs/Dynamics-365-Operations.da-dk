---
title: Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen
description: Denne artikel beskriver, hvordan du kan oprette og få vist brugerdefinerede instruktioner for hvert trin i hvert opgaveflow, som du konfigurerer for Warehouse Management-mobilappen.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: faa9bfa320823664603153601c56654170e7e23a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334470"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen

> [!IMPORTANT]
> De funktioner, der er beskrevet i denne artikel, gælder kun for den nye Warehouse Management-mobilapp. De påvirker ikke den gamle lagerstedsapp, der nu er udgået og frarådes.

Denne artikel beskriver, hvordan du kan oprette og få vist brugerdefinerede instruktioner for hvert trin i hvert opgaveflow, som du konfigurerer for Warehouse Management-mobilappen. Når lagerarbejdere modtager velskrevne instruktioner, kan de med det samme begynde at bruge nye flow uden at skulle oplæres inden. Denne funktion indeholder følgende fordele:

- **Kvalificer arbejdere hurtigere ved at lade dem følge simple instruktioner for hvert trin i opgaven.** Hvert trin i et flow indeholder instruktioner, der gør det muligt for frontlinjemedarbejdere at forstå opgaven.
- **Angiv instruktioner, der stemmer overens med dine egne processer.** Skriv dine egne instruktioner, der passer til virksomheden og lagerstedsprocesserne. Du kan f.eks. tilpasse terminologien , så den passer til det fysiske område og de lokale forkortelser.

## <a name="turn-the-warehouse-app-step-instructions-feature-on-or-off"></a>Slå funktionen til trininstruktioner for lagerstedsappen til eller fra

Før du kan bruge denne funktion, skal den være aktiveret for dit system. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Vejledninger til trin i lagerstedsapp* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="step-titles-and-step-instructions-in-the-app"></a>Titler og instruktioner for hvert trin i appen

Hvert trin i et opgaveflow i Warehouse Management-mobilappen er identificeret med et trin-id. Desuden har hvert trin en titel, et ikon og en instruktion. (Du kan finde flere oplysninger i [Tildele trinikoner og -titler for Warehouse Management-mobilappen](step-icons-titles.md)).

### <a name="step-titles"></a>Trintitler

En *trintitel* er en kort beskrivelse af, hvad en arbejder skal udføre for et trin. Den vises som en stor tekst øverst på skærmen som vist i følgende illustration.

![Eksempel på en trintitel i mobilappen Warehouse Management](media/wma-step-title.png "Eksempel på en trintitel i mobilappen Warehouse Management")

> [!TIP]
> På grund af den store tekststørrelse skal du forsøge at gøre trintitlerne så korte som muligt. Ellers kan teksten blive afkortet. Ved lange titler kan arbejderne dog stadig trykke på og holde titlen for at åbne en dialogboks, der viser hele teksten.

### <a name="step-instructions"></a>Trinvise vejledninger

En *trininstruktion* er en længere beskrivelse, der indeholder flere oplysninger om, hvad en arbejder skal udføre for et trin. Den vises i en pop op-dialogboks som vist i følgende illustration.

![Eksempel på en trininstruktion i mobilappen Warehouse Management](media/wma-step-instructions.png "Eksempel på en trininstruktion i mobilappen Warehouse Management")

Trininstruktionen vises automatisk, når et trin åbnes. Arbejdere kan afvise den ved at trykke et vilkårligt sted uden for pop op-dialogboksen. Dialogboksen indeholder desuden afkrydsningsfeltet **Vis ikke igen**, som arbejderne kan vælge for at forhindre, at instruktionerne vises, næste gang de udfører samme opgave.

## <a name="load-the-default-setup"></a>Indlæse standardopsætningen

Første gang du aktiverer funktionen *Trininstruktioner for lagerstedsapp*, indeholder systemet ingen trintitler eller instruktioner, der kan tilpasses. Det første, du skal gøre, er derfor at indlæse standardopsætningen. Standardopsætningen indeholder tekster til alle tilgængelige trin-id'er på alle understøttede sprog. Hvis du vil indlæse standardopsætningen, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.
1. Vælg **Opret standardkonfiguration** i handlingsruden. Siden udfyldes med standardtrinnene.

## <a name="customize-step-titles-and-instructions"></a>Tilpasse trintitler og -instruktioner

Hvis du vil tilpasse titlen og/eller instruktionen for et trin på et vilkårligt antal sprog, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.

    På siden **Trin for mobilenhed** vises alle trin, der er tilgængelige for systemet. Hvert trin-id kan deles mellem ethvert antal menupunkter for mobilenheden. Hvis et trin-id deles mellem flere menupunkter, vises samme titel og instruktion for alle disse menupunkter. Du kan dog benytte tilsidesættelse for at tilpasse titlen og instruktionen for bestemte menupunkter. (Du kan finde flere oplysninger i næste afsnit).

    Gitteret indeholder følgende kolonner:

    - **Navn på menupunkt** – Rækker, hvor denne kolonne er tom, skal du bruge den standardtrinstitel og -instruktion, der gælder for alle menupunkter for mobilenheden, hvor der ikke er defineret en tilsidesættelse. Rækker, hvor denne kolonne er angivet til navnet på et menupunkt, har tilsidesættelser, der kun gælder for det angivne menupunkt.
    - **Trin-id** – Det entydige id for trinnet.
    - **Titel til input** – Den titel, der vises, når appen anmoder om nye oplysninger. Typisk er felterne på siden tomme (dvs. at de ikke har foruddefinerede værdier).
    - **Titel til bekræftelse** – Den titel, der vises, når appen anmoder om bekræftelse af en værdi, som allerede er gemt i systemet. Typisk har felterne på siden foruddefinerede værdier.

1. Find kombinationen af værdier for **Trin-id** og **Menupunktnavn**, som du vil redigere, og vælg værdien i kolonnen **Trin-id**. På den side, der åbnes, vises alle de tilgængelige oversættelser af titlen og instruktionen for det valgte trin.
1. Følg et af disse trin for at tilpasse teksten for ethvert sprog. Begge indstillinger gør det muligt at redigere tekster på eksisterende sprog. Det er dog kun den første indstilling, der gør det muligt at tilføje tekster til nye sprog, mens det kun er den anden indstilling, der gør det muligt at få vist og redigere tekster for alle eksisterende menuspecifikke ændringer for det valgte sprog.

    - Vælg **Tilføj** på værktøjslinjen for at åbne en dialogboks, hvor du kan tilføje eller redigere tekster på ethvert understøttet sprog. Angiv feltet **Referencesprog** til det sprog, du vil have vist værdier for. Værdierne vises i venstre kolonne. Angiv feltet **Sprog for oversættelser** til det sprog, du vil tilføje eller tilpasse. I højre kolonne skal du efter behov redigere værdierne i felterne **Titel for input**, **Instruktion for input**, **Titel til bekræftelse** og **Instruktion for bekræftelse**. Vælg derefter **OK**.
    - Søg efter og vælg den række i gitteret, hvor feltet **Sprog** er angivet til det sprog, du vil redigere. Vælg **Vis &lt;sprog&gt; for oversættelser i dette trin** på værktøjslinjen for at åbne en dialogboks, hvor du kan redigere tekster for alle tilgængelige tilsidesættelser for det valgte sprog. Dialogboksen indeholder et gitter med rækker for begge standardtekster (hvor feltet **Menupunktnavn** er tomt) og for hver tilgængelig tilsidesættelsestekst (hvor feltet **Menupunktnavn** er angivet til navnet på det menupunkt, som tilsidesættelsen gælder for). Rediger efter behov værdierne for felterne **Titel for input**, **Instruktion for input**, **Titel til bekræftelse** og **Instruktion for bekræftelse**. Vælg derefter **OK**.

1. Fortsæt med at arbejde, indtil du har defineret hver krævet titel og instruktion for hvert påkrævet sprog.

## <a name="add-menu-specific-overrides"></a>Tilføje menuspecifikke tilsidesættelser

Som det blev nævnt i forrige afsnit, kan du oprette ethvert antal menuspecifikke tilsidesættelser for hvert trin-id. Du kan f.eks. bruge denne egenskab til at redigere og ændre instruktionen, så den passer bedre til din lokale forretningsproces for et bestemt menupunkt. Hvis firmaet i forbindelse med salgspluk f.eks. leverer arbejds-id'er til arbejdere på et udskrevet dokument, kan du give et tip om, at arbejdere skal starte med at scanne et arbejds-id.

Hver tilsidesættelse gælder for et bestemt menupunkt for mobilenheden og kan indeholde ethvert antal oversættelser. Hvis der ikke findes nogen tilsidesættelse for et menupunkt, bruger menupunktet standardteksterne. Hvis der ikke er defineret en tilsidesættelsesoversættelse for et sprog, bruges standardteksterne, også for menupunkter, hvor der er defineret en tilsidesættelse for andre sprog.

Hvis du vil oprette og konfigurere en tilsidesættelse, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.
1. Søg i gitteret og vælg den række, du vil oprette en tilsidesættelse for.
1. Vælg **Tilføj trinkonfiguration** i handlingsruden.
1. I dialogboksen **Tilføj trinkonfiguration** skal du angive feltet **Menupunkt** til navnet på det menupunkt for mobilenheden, som tilsidesættelsen gælder for. Vælg derefter **OK**.
1. Den side, der vises, viser alle de tekster, der er tilgængelige for den nye tilsidesæsttelse. I begyndelsen oprettes der kun ét sprog. Alle andre sprog vil fortsat bruge standardteksterne, medmindre du tilføjer disse sprog her. Rediger teksterne, og tilføj nye sprog efter behov, som beskrevet i forrige afsnit.
