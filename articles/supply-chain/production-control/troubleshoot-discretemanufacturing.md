---
title: Foretage fejlfinding af diskret produktion
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med diskret produktion.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b9c43d59e8022a365853f4b9cbb32ac3c3074e3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810912"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Foretage fejlfinding af diskret produktion

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med diskret produktion.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Jeg modtager følgende fejlmeddelelse: "Lokationsstyringsprocesser er ved at blive anvendt. Hvis der endnu ikke er registreret arbejdslinjer, kan du annullere det oprettede arbejde og eventuelle last- og forsendelseslinjer og derefter fortsætte pluk- eller forsendelsesprocessen".

### <a name="issue-description"></a>Problembeskrivelse

Dette problem opstår, hvis du forsøger at reservere eller frigive arbejde for en linje, men lagertransaktionen har statussen *Plukket*, hvilket angiver, at materialet er plukket.

### <a name="issue-resolution"></a>Problemløsning

Følg et af disse trin for at løse dette problem.

- Skift status for produktionsordren tilbage til *Forkalkuleret* eller *Frigivet*.
- Åbn detaljesiden for den relevante produktionsordre. I handlingsruden under fanen **Lagersted** i gruppen **Stop** skal du vælge **Stop og fortryd pluk** for at fortryde alle plukkede transaktioner. Vælg derefter **Fjern stop** for at behandle produktionsordren.

Her er en forklaring på funktionerne *Fortryd pluk* og *Stop*:

- **Fortryd pluk** – Denne funktion tilbagefører status for lagertransaktioner for styklistelinjer formellinjer, der har status fra *Plukket* til *I bestilling*. Når arbejdet for pluk af råmaterialer er fuldført, angives status for linjerne til *Plukket*. Denne status forhindrer, at produktionsordren nulstilles til statussen *Oprettet*. I dette tilfælde kan du bruge funktionen *Fortryd pluk* til at tilbageføre transaktionerne fra *Plukket* status og derefter nulstille produktionsordren til statussen *Oprettet*.
- **Stop** – Denne funktion angiver et **Stoppet** flag på produktionsordren for at forhindre enhver statusopdatering på ordren. Du kan finde flaget **Stoppet** i oversigtspanelet **Lagersted** på siden med oplysninger om produktionsordre.

> [!NOTE]
>
> - Knapperne kan kun ses, når produktionsordren er oprettet for varer, der er aktiveret til lagerprocesser.
> - **Stop**-gruppen kan kun ses under fanen **Lagersted** i handlingsruden på siden med oplysninger om produktionsordre. Den vises ikke i oversigtspanelet **Lagersted** på listesiden **Produktionsordrer**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Det tilsvarende ressourcenavn opdateres ikke, efter at jeg har ændret et arbejdernavn i det globale adressekartotek.

### <a name="issue-description"></a>Problembeskrivelse

Det tilsvarende ressourcenavn opdateres ikke i ressourcegruppens master, hvis du ændrer et arbejdernavn i det globale adressekartotek.

### <a name="issue-resolution"></a>Problemløsning

Dette scenarie understøttes ikke i øjeblikket. Hvis du vil løse dette problem, skal du opdatere ressourcenavnet manuelt.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Når jeg opretter en ny produktionsordre, får jeg ikke vist følgende meddelelse: "Vil du indsætte den aktive version af styklisten og ruten?"

### <a name="issue-description"></a>Problembeskrivelse

Når du opretter en ny produktionsordre, når du angiver varenummeret, angives felterne **Lokation** og **Lagersted** automatisk til den standardlokation og det lagersted, der er defineret på siden **Standardordreindstillinger** for den færdige vare. Det aktive styklistenummer og rutenummeret angives desuden automatisk. Du får ikke vist følgende meddelelse, hvor du bliver bedt om at angive værdier:

> Vil du indsætte den aktive version af stykliste og rute?

### <a name="issue-resolution"></a>Problemløsning

Du bliver ikke bedt om at indsætte stykliste- og rutenumre, hvis du vælger et produkt, som der er defineret en lokation og et lagersted for, på siden **Standardordreindstillinger**. Du bliver kun spurgt, hvis disse værdier ikke er defineret for det valgte produkt.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Produktionsordrer vises ikke på siden Afmærkning.

### <a name="issue-description"></a>Problembeskrivelse

Nogle produktionsordrer vises ikke på siden **Afmærkning**.

### <a name="issue-resolution"></a>Problemløsning

Produkter, der har følgende konfiguration, er ikke tilgængelige til afmærkning. Derfor vil de ikke blive vist på siden **Afmærkning**:

- Produkterne defineres som produkter af typen *fastvægt*.
- De er aktiveret for de avancerede lagerprocesser.
- De konfigureres til at blive kontrolleret med *Standardomkostning*-princippet.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Når jeg forsøger at afslutte en produktionsordre, får jeg vist følgende fejlmeddelelse: "Beregningen af omkostningsværdien for styklistens forbrug skal være negativ ved afgang fra lageret".

Dette problem blev løst i version 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Når en produktionsordres status ændres fra Færdigmeldt til Afslut, vises følgende fejlmeddelelser: "Opdateringskonflikt. Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen" og " Der er opstået en kritisk fejl i funktionen InventCostMovement.checkVariance".

Dette problem opstår, fordi de underliggende data blev ændret af en anden proces. Processen vil forsøge at opdatere dataene op til fem gange. Hvis konflikten stadig findes efter fem forsøg, får du vist følgende fejlmeddelelser:

> Opdateringskonflikt. Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen.

> Der er opstået en alvorlig fejl i funktionen InventCostMovement.checkVariance.

Denne funktionsmåde er tilsigtet. Du kan afhjælpe problemet ved at fortsætte batchjobbet. Det skal fuldføre kørslen.

Hvis batchjobbet konstant mislykkes, efter at du har genoptaget det, skal du kontrollere, at afrundingspræcisionen for finansens standardvaluta er kompatibel med den afrunding, der anvendes på værdierne i tabellen InventSum. Hvis afrundingspræcisionen er ændret til en ikke-kompatibel værdi, skal du sandsynligvis ændre den tilbage til en kompatibel værdi. Søg efter **ModifiedDateTime**. I dette tilfælde vil værdien typisk vise, at afrundingspræcisionen er ændret for nylig.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Når jeg frigiver til et lagersted, får jeg vist følgende fejlmeddelelse: "Vare-RM kunne ikke reserveres fuldt ud. Sørg for, at hele antallet er tilgængeligt, eller reservér varerne manuelt, hvis feltet Reservation på styklistelinjen er angivet til Manuel eller Startet. Ordren kunne ikke frigives til lagersted, fordi nogle materialer ikke kunne reserveres". Status opdateres dog til Frigivet.

### <a name="issue-description"></a>Problembeskrivelse

Hvis ikke alle styklistelinjevarer er fysisk tilgængelige, når en produktionsordre frigives, og **Frigiv til lagersted**-politikken er angivet til *Kræv fuld reservation* på produktionsordren, vises følgende fejlmeddelelse:

> Vare-RM kunne ikke reserveres fuldt ud. Sørg for, at hele antallet er tilgængeligt, eller reservér varerne manuelt, hvis feltet Reservation på styklistelinjen er angivet til Manuel eller Startet. Ordren kunne ikke frigives til lagersted, fordi nogle materialer ikke kunne reserveres.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet og fungerer som forventet.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Når jeg forsøger at afslutte en produktionsordre og færdigmelde den, får jeg vist følgende fejlmeddelelse: "Det samlede antal gode varer, der er færdigmeldt for produktionen, vil være %1. På sidste operation er der i alt tilbagemeldt 0,00".

### <a name="issue-description"></a>Problembeskrivelse

Når du forsøger at bogføre en færdigmeldingskladde på en produktionsordre, får du vist følgende fejlmeddelelse:

> I alt færdigmeldt antal gode på produktionen bliver %1. På sidste operation er der i alt tilbagemeldt 0,00".

### <a name="possible-cause"></a>Mulig årsag

Dette problem opstår, hvis de antal, der blev bogført i de sidste operationer, var forkerte. Hvis f.eks. produktion er startet, men det antal, der skal sættes i gang, ikke er tildelt, vil rutekortkladden blive bogført uden nogen linjer. Hvis du vil bekræfte situationen, skal du åbne produktionsordren og derefter vælge **Rutekort** under fanen **Vis** i handlingsruden .

### <a name="workaround"></a>Løsning

Du kan løse dette problem ved at bogføre flere kladder for de operationer, som kladderne ikke er blevet bogført korrekt for. Genstart produktionsordren, og vælg at bogføre de ekstra kladder. Denne handling starter ikke produktionsordren, men den bogfører kladderne. På rutekortet vises derefter de antal, der er bogført, og du skal kunne afslutte produktionsordrerne korrekt.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Kan jeg færdigmelde en produktionsordre, mens jeg rapporterer antallet af fejl, men ikke mens jeg rapporterer tid eller materialeantal?

Du kan ikke rapportere antallet af fejl i en produktionsordre, medmindre du også rapporterer antallet af gode varer. Dette scenario understøttes **ikke**. Opdateringen af færdigmeldingen vil mislykkes, når du forsøger at afslutte produktionsordren, og du får vist følgende fejlmeddelelse:

> Færdigmeldingsantal mangler.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Kan jeg spore serienumrene på færdige varer mod serienumrene på forbrugte varer?

Du kan ikke spore serienumrene på færdigvarer mod serienumrene for materiale, som en produktionsordre bruger til at fremstille disse færdigvarer. Dette scenarie understøttes ikke i øjeblikket. Du kan løse problemet ved at oprette produktionsordrer for et antal på 1.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]