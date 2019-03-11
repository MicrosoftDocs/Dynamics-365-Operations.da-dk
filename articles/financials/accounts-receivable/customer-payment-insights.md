---
title: Indsigt i kundebetaling (eksempel)
description: Dette emne beskriver, hvordan indsigt i kundebetaling kan hjælpe med til at forudsige, hvornår en faktura bliver betalt, og det hjælper virksomheder med at oprette optimeringsstrategier, som kan forbedre sandsynligheden for, at der betales til tiden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "344656"
---
# <a name="customer-payment-insights-preview"></a>Indsigt i kundebetaling (eksempel)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Denne funktion er en del af en målrettet version og er kun tilgængelig for brugere, der har valgt at deltage i private prøveversioner. Denne funktion medtages i en kommende almindeligt tilgængelig version.

# <a name="overview"></a>Overblik

Organisationer finde ofte svært for at forudsige, hvornår en kunde betaler fakturaerne. Denne manglende indsigt kan resultere i forkerte likviditetsbudgetter, ineffektive rykkerprocesser og risikoen for, at ordrer udleveres til kunder, der kan udgøre en risiko. Indsigt i kundebetaling (eksempel) bruger maskinel indlæring til at forudsige, hvornår en faktura betales. Den indeholder også optimeringsstrategier, der kan tilpasses for at maksimere sandsynligheden for, at kunder betaler til tiden.

## <a name="predictions"></a>Forudsigelser

Betalingsforudsigelsen giver organisationerne mulighed for at forbedre deres forretningsprocesser ved at hjælpe med at:

-   Nemt identificere de fakturaer, der forventes at blive betalt for sent.
-   Træffe passende foranstaltninger til forbedring af chancen for at blive betalt til tiden.

Indsigt i kundebetaling (eksempel) bruger maskinel indlæring til at forudsige, hvornår en faktura betales. Bruger historiske faktura-, betalings- og kundedata til at oprette en model til maskinel læring, der bruges til at forudsige, hvornår en faktura bliver betalt.

For hver åben faktura forudsiger Indsigt i kundebetaling (eksempel) tre betalingssandsynligheder:

-  Sandsynligheden for betaling til tiden (inden for fakturaens forfaldsdato).
-  Sandsynligheden for betaling inden for 30 dage efter fakturaens forfaldsdato.
-  Sandsynligheden for betaling senere end 30 dage efter fakturaens forfaldsdato.

Sandsynligheden for at betalinger kan ses i afsnittet Forudsigelse.

[![Betalingsforudsigelser](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Hver faktura tildeles også en vindende sandsynlighed for betaling ved hjælp af et af tre forventede betalingssandsynlighedsscenarier, der er defineret ovenfor. Scenariet med den højeste sandsynlighed for betaling er det vindende scenario.


Lad os f.eks. antage at forudsigelsen for en faktura viser 71 % sandsynlighed for, at fakturaen betales til tiden, 13 % sandsynlighed for, at fakturaen betales inden for 30 dage efter forfald, og 16 % sandsynlighed for, at fakturaen betales mere end 30 dage efter forfaldsdatoen. Den største sandsynlighed viser, at fakturaen er i scenariet med betaling til tiden, så fakturaen skal mærkes med sandsynligheden for, at den betales til tiden.

[![Betalingsforudsigelser](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimeringsstrategier

Ud over prognoser for betaling kan Indsigt i kundebetaling (eksempel) bruge optimeringsstrategier til at forbedre chancerne for at modtage betaling til tiden. Dette giver organisationer mulighed for at foretage 'Hvad, hvis'-analyser ved at tillade brugerne at justere faktura- og kundeparametre og derefter sammenligne virkningen af sandsynligheden for at modtage betaling af fakturaer til tiden.

En organisation kan f.eks. evaluere effekten af opdatering af kasserabatten på fakturaer på sandsynligheden for modtagelse af betalingen til tiden. Når fakturaerne er optimeret til at bruge den nye rabat, kan brugerne gennemse resultatet af at anvende rabatten på sandsynligheden for modtagelse af betalinger for disse fakturaer til tiden. Hvis omkostningerne ved anvendelse af rabatten er minimal, sammenlignet med fordelene ved at få betaling til tiden, kan organisationen vælge at anvende den valgte rabat på alle fremtidige åbne ordrer.

> [!NOTE] 
> I øjeblikket er kun rabat tilgængelig som en optimeringsstrategi for Indsigt i kundebetaling (eksempel).

[![Optimerede forudsigelsen](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Sådan får du Indsigt i kundebetaling (eksempel)

Hvis du er interesseret i at prøve Indsigt i kundebetaling (eksempel), skal du sende en mail til [Finance Insights Preview team](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Erklæring om beskyttelse af personlige oplysninger

Eksempler gemmer kundedata i USA. Desuden kan eksempler (1) anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 for Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.
