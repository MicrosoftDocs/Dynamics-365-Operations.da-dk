---
title: Genopfyldning med udbetalingskanbans
description: I dette emne beskrives, hvordan udbetalingskanban bruges til materialegenopfyldning under produktionsaktiviteter.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c8a6b4152215bc912d99f2f4c250defa75278c3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356921"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Genopfyldning med udbetalingskanbans

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan udbetalingskanban bruges til materialegenopfyldning under produktionsaktiviteter.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Arbejdsgang for materialegenopfyldning, der bruger udbetalingskanban

Udbetalingskanban kan bruges til at flytte en kanban for en enkelt vare mellem lagersteder og produktionslokationer, hvor materialet skal forbruges. Udbetalingskanban understøtter en pull-baseret løsning til materialegenopfyldning, hvor der kræves et pull-signal for at udløse leveringer til bestemte behov. 

I følgende scenario vises et pull-baseret genopfyldningssystem, hvor et pull-signal udløser oprettelse af en kanban til genopfyldning af materialet for en produktionsproces. 

[![Pull-signal udløser oprettelsen af en kanban til genopfyldning af materialet for en proces.](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Udbetalingskanban
2.  Kanban "fra"-lokation og placeringslokation for lagerstedsarbejde
3.  Kanban "til"-placering og produktionsindlagringslokation
4.  Produktionsproces
5.  Lagerstedsarbejde til kanban-pluk
6.  Lagerstedslokationer for råmateriale
7.  Materialelagersted
8.  Produktionslagersted

I dette scenario forbruger en produktionsproces (4) materiale fra en produktionsindlagringslokation (3) på produktionslagerstedet (8). Når en materialehåndteringsenhed (kanban) er forbrugt, registreres den som tom. Et signal til genopfyldning oprettes for varens oprindelse, og der oprettes en ny kanban (1). I dette tilfælde består varens oprindelse af lokaliteter på materialelagerstedet (7). Materialet til denne kanban plukkes og placeres på en lokalitet (2) på samme lagersted. Når materialet er plukket, er det klar til at blive overført fra lokation 2 til produktionsindlagringslokationen (3) på produktionslagerstedet (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Konfigurere lagerstedsarbejde for kanban-pluk til udbetalingskanban

For at aktivere plukning af råvarer til udbetalingskanban skal du konfigurere bølgeskabeloner, arbejdsskabeloner og lokationsvejledninger for arbejdsordretypen **Kanban-pluk**. Denne arbejdsordretype understøtter ikke blot plukprocessen for udbetalingskanban. Den understøtter også plukprocessen til produktionskanban. Du kan dog konfigurere en separat plukproces for hver type kanban ved at adskille de bølgeskabelonerne, arbejdsskabelonerne og lokationsvejledninger. Hvis du vil adskille bølgeskabelonerne, arbejdsskabelonerne og lokationsvejledningerne, kan du angive kriterier for aktivitetstypen (**Proces** eller **Overfør**) i forespørgslerne til disse enheder.

## <a name="configure-the-withdrawal-kanban"></a>Konfigurere udbetalings-kanban

Den overførselsaktivitet, der bruges til udbetalingskanban, er konfigureret som en del af en aktiveret aktivitetsplan i et Lean produktionsflow. Som led i konfigurationen af overførselsaktiviteten kan du angive "fra"- og "til"-placeringer for overførslen. Når du har konfigureret overførselsaktiviteten, kan du tildele den til en kanban-regel af typen **Udtræk**. Kanban-reglen angiver politikker og konfigurationer for udbetalings-kanban. Kanbanantallet definerer, hvor mange enheder af materialehåndteringsenheden kanban'en udfører under overførslen. Det faste kanbanantal bruges, når den faste genopfyldningsstrategi er valgt. Dette antal definerer, hvor mange kanbans der kræves for at undgå, at lagerbeholdning eller opbygge lageret udløber ved behovskilden. Det faste antal kan beregnes baseret på faktisk behov, historisk behov og serviceniveauer. Følgende to scenarier beskriver, hvordan du kan administrere materialegenopfyldning, der bruger udbetalings-kanban.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Eksempel 1: Genopfylde en produktionsindlagringslokation ved hjælp af en fast udbetalings-kanban

En produktionsproces forbruger et indkøbt råmateriale fra en produktionsindlagringslokation, som findes på produktionslagerstedet. Når råmaterialet modtages fra leverandøren, gemmes det i lokationer på materialelagerstedet. Eftersom behovet for materialet opfattes som stabilt over en periode, er det konfigureret til at forsyne produktionen i en kanban-proces med en fast mængde. Når en kanban er forbrugt på produktionsindlagringslokationen, registreres et tom-signal, og der føjes en ny kanban af samme type til processen. 

Tom-signalet kan konfigureres, så det aktiveres automatisk, når en kanban er fuldført. Tom-signalet kan også konfigureres som en manuel interaktion, der er afgives fra enten kanban-overførselsområdet eller fra en menu på den håndholdte enhed. Kanban-overførselsområdet er det arbejdsområde, hvor alle aktiviteter i kanban-livscyklus administreres. 

Når den pågældende kanban oprettes, føjes en bølgelinje for råmaterialet til en kanbanbølge for materialelagerstedet. I pluklisteafsnittet over kanban-overførselsområdet kan status for materialet og relaterede lagerstedsprocesser overvåges fra oprettelse af bølgen til arbejdsoprettelse, indtil materialet er disponibelt på "overførsel fra"-placeringen og er klar til at blive overført til produktionsindlagringslokationerne. En kanban kan fuldføres fra kanban-overførselsområdet eller fra en menu på den håndholdte enhed. 

I dette scenario behandles plukarbejdet på materialelagerstedet som én aktivitet. Overførselsaktiviteten mellem materialelagerstedet og produktionslagerstedet behandles som en særskilt aktivitet. Denne fremgangsmåde kan være nyttigt, hvis der f.eks. er en stor fysisk afstand mellem de to lagersteder. I så fald kan kanban-overførselsaktiviteten repræsentere lastning af en lastbil. 

Hvis afstanden mellem lokationer på lagerstedet og produktionsindlagringslokationen er kort, kan det være mere effektivt at medtage overførselsaktiviteten i plukprocessen. Derefter, når materialet er plukket, kan det placeres direkte på produktionsindlagringslokationen. For at understøtte denne proces kan du konfigurere overførselsaktiviteten, så den fuldføres automatisk, når plukarbejdet på udbetalings-kanban'en behandles.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Eksempel 2: Automatisk fuldføre overførselsaktiviteten ved behandling af kanban-plukarbejde

I følgende eksempel er overførselsaktiviteten for udbetalingskanban'en konfigureret til overførsel mellem to steder på samme lagersted. Overførselsaktivitet for udbetalings-kanbanen er konfigureret, så den fuldføres automatisk. 

[![Overførselsaktiviteten fuldføres automatisk ved behandling af kanban-plukarbejde.](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Delt lagersted for råmaterialer og produktion
2.  Lagerstedslokationer for råmaterialer
3.  Kanban "fra"-lokation og placeringslokation for lagerstedsarbejde
4.  Udbetalingskanban
5.  Produktionsindlagringslokation
6.  Produktionsproces

Når en kanban er forbrugt på produktionsindlagringslokationen, rapporteres den som tom, og der føjes en ny kanban til processen. Når den pågældende kanban oprettes, føjes en bølgelinje til en kanbanbølge. Når kanbanbølgen behandles, oprettes lagerstedsarbejde til kanbanpluk. Lagerstedsmedarbejderen behandler arbejdet til kanbanpluk og får under arbejdet anvisning på at plukke materialet til kanban'en på en lagerstedslokation. Når lagermedarbejderen bekræfter plukket, fuldføres kanban'en automatisk, og lagermedarbejderen modtager instruks om at placere materialet på produktionsindlagringslokationen.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]