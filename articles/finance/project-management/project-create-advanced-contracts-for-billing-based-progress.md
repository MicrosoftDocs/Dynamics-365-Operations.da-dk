---
title: Oprette avancerede kontrakter til fakturering baseret på status
description: Dette emne forklarer, hvordan du opretter projektkontrakter, så du kan generere fakturaer for debitorer baseret på en procentdel af det udførte arbejde.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282817"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Oprette avancerede kontrakter til fakturering baseret på status
[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for debitorer baseret på en procentdel af det udførte arbejde. Fakturabeløb beregnes automatisk for de budgetkategorier, som du opretter for det arbejde, du konfigurerer for et projekt. Tidspunktet for fakturaen angives, når du forhandler projektkontrakten med kunden.

Benyt fremgangsmåderne i dette emne til at oprette en kontrakt, et tilhørende projekt og de regler for fakturering, der skal bruges til beregning af fakturabeløbene for de budgetkategorier, som du opretter for arbejde på projektet.

Når du har oprettet kontrakten og projektet, kan du angive projektdetaljerne. Du kan for eksempel definere aktiviteter og tildele projektet arbejdere.

## <a name="example"></a>Eksempel

Din organisation udvikler software. Du aftaler at udvikle en pakkeløsning med et system til lønningsregnskab for en kunde for i alt 20.000 kr. Din organisation accepterer at fakturere kunden, efterhånden som du fuldfører de angivne procentdele af arbejdet på projektet. Du konfigurerer følgende projektkategorier for arbejdet, så du kan bruge dem i faktureringsprocessen:

- Rådgivning
- Design
- Installation

Du opretter også regler for fakturering, så fakturabeløbene beregnes automatisk for den procentdel af arbejdet, der er fuldført inden for hver kategori.

Budgetadministratoren opretter et budget for projektkategorierne. Beløbet for udført arbejde beregnes automatisk som en procentdel af det faktiske arbejde sammenlignet med de budgetterede beløb.

## <a name="prerequisites"></a>Forudsætninger

Før du opretter et projekt, der bruger faktureringsregler, skal du konfigurere nummerserierne for faktureringsregler og en gebyrkladde, der bruges til at bogføre statusfaktureringer.

1. Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
2. På siden **Parametre for projektstyring og regnskab** skal du under fanen **Nummerserier** du angive den nummerserie, du vil bruge, når der oprettes faktureringsregler.
3. Gå til **Projektstyring og regnskab** \> **Kladder** \> **Gebyr**.
4. Vælg **Ny** på siden **Gebyrkladde**, og angiv kladdenavnet.

## <a name="create-a-contract-for-progress-billings"></a>Oprette en kontrakt for statusfaktureringer

Brug denne fremgangsmåde til at oprette en projektkontrakt til et fastprisprojekt. Du opretter en projektfaktura, når det arbejde, der er udført på projektet, når en bestemt procentdel.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.
2. På siden **Projektkontrakter** skal du vælge **Ny**.
3. Angiv følgende felter i dialogboksen **Ny projektkontrakt**:

    - **Navn**
    - **Finansieringstype**
    - **Finansieringskilde**
    - **Salgsvaluta** – Det er den valuta, der som standard skal bruges til debitorfakturaer, som er knyttet til projektkontrakten. Du kan dog ændre salgsvalutaen på en bestemt debitorfaktura.

4. Vælg **OK**. Oplysningerne kopieres til hovedet på siden **Projektkontrakter**.
5. Udfyld resten af de nødvendige oplysninger om projektet på siden **Projektkontrakter**.

## <a name="create-a-project-for-progress-billings"></a>Oprette et projekt for statusfaktureringer

Brug følgende procedure til at oprette et projekt og eventuelle underprojekter, der er tilknyttet en projektkontrakt.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. På siden **Alle projekter** skal du vælge **Ny**.
3. Vælg **Tid og materiale** i feltet **Projekttype** i dialogboksen **Nyt projekt**.
4. Vælg en projektgruppe. En projektgruppe definerer posteringsoplysninger for de projekter, der er tildelt gruppen.
5. Vælg **Opret projekt**.
6. Når du har oprettet projektet, skal du angive projektstadiet til **Igangværende**.

## <a name="create-a-budget-for-a-project"></a>Oprette et budget til et projekt

Budgetkategorierne bruges til automatisk beregning af fakturabeløb for den procentdel af arbejdet, der er fuldført i hver kategori. Udfør følgende trin for at oprette budgetkategorier for de forkalkulerede omkostninger.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. Vælg og åbn det ønskede projekt på siden **Alle projekter**.
3. Vælg **Projektbudget** i gruppen **Budget** under fanen **Plan** i handlingsruden på siden **Projekter**.
4. Angiv en forkalkuleret omkostning for hver kategori i projektet på siden **Projektbudget**.

## <a name="create-billing-rules-for-progress-billings"></a>Oprette faktureringsregler for statusfaktureringer

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.
2. Vælg og åbn en projektkontrakt på siden **Projektkontrakter**.
3. Vælg **Tilføj** i oversigtspanelet **Faktureringsregler** på siden Projektkontrakt.
4. Vælg **Status** i feltet **Linjetype** på siden **Faktureringsregel**.
5. Angiv kontraktens samlede beløb i feltet **Kontraktværdi** i oversigtspanelet **Faktureringsregellinjer - detaljer**.
6. Vælg den kategori, som gebyrtransaktionen skal bogføres i, i feltet **Kategori**.
7. Vælg det projekt, der bruger denne faktureringsregel, i feltet **Projekt**.
8. Valgfrit: Tildel faktureringsreglen flere projekter. Vælg et projekt i sektionen **Tilgængelige projekter** i oversigtspanelet **Projekt**, og vælg derefter den højre pileknap for at føje projektet til sektionen **Valgte projekter**.
9. Valgfrit: Beregn det procentvise beløb, som kunden holder tilbage fra betalinger på en faktura. Vælg finansieringskilden i oversigtspanelet **Betingelser for tilbageholdelse af betaling**, og angiv derefter tilbageholdelsesprocenten i feltet **Tilbageholdelsesprocent**.
10. Gentag disse trin, hvis du vil oprette flere faktureringsregler for projektkontrakten.
