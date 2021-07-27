---
title: Årsafslutning mangler startsaldi
description: I dette emne beskrives det, hvorfor der muligvis mangler startsaldi, når du lukker et år, og hvordan du kan gendanne disse saldi, hvis de mangler.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bebf35a8959d4f72d46d4b40e5487f499b2756d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356646"
---
# <a name="year-end-close-missing-opening-balances"></a>Årsafslutning mangler startsaldi

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvorfor der muligvis mangler startsaldi, når du lukker et år, og hvordan du kan gendanne disse saldi, hvis de mangler.

### <a name="symptom"></a>Symptom

Hvorfor findes der ingen startsaldi, efter at du har kørt afslutning af finansåret? 

### <a name="resolution"></a>Løsning

Du skal kontrollere følgende, hvis du har lukket et år i Finans og derefter genereret en råbalance, der ikke viser startsaldi for det næste regnskabsår.

Hvis feltet **Fortryd forrige afslutning** er angivet til **Ja**, tilbageføres den forrige ultimoafslutning for det samme regnskabsår. Når du kører en proces til at fortryde årsafslutningen, slettes alle poster for ultimo- og startsaldierne, som om året aldrig er blevet lukket. Bilagene slettes også. Årsafslutningen køres ikke automatisk igen. Du skal starte processen igen, og denne gang skal du opdatere valget **Fortryd forrige lukning** til **Nej**.

Dette scenario er dækket i emnet for ofte stillede spørgsmål om årsafslutning. Du kan finde yderligere oplysninger i [Ofte stillede spørgsmål om årsafslutning](faq-year-end-activities.md).

### <a name="symptom"></a>Symptom

Jeg har kørt årsafslutningen med indstillingen **Fortryd forrige lukning** angivet til **Nej**, og jeg har stadig ikke startsaldi for mit regnskabsår.

### <a name="resolution"></a>Løsning

Kontrollér først status af det valgte batchjob. Lukning af et år omfatter et antal separate opgaver, men det vigtigste trin er batchopgaven med opgavebeskrivelsen **Trin 5.0.0**. Bogføring af primotransaktionerne, og eventuelt ultimotransaktionerne, til Finans, sker i løbet af dette trin. 

[![Liste over batchhistorik.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Hvis dette trin blev afsluttet uden fejl, men startsaldi ikke vises på siden **Forespørgsel om råbalance** (**Finans > Forespørgsler og rapporter > Prøvesaldo**), kan du gennemse resultaterne af batchjobbet for årsafslutning for at se, om trinnet Genberegn saldi er fuldført korrekt.

[![Resultater af batchjob for årsafslutning.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Hvis dette trin af en eller anden grund ikke er lykkedes, er det sandsynligt, at primotransaktionerne (og eventuelt ultimo) er blevet bogført korrekt. Du kan kontrollere, at finanstransaktionerne er bogført korrekt ved hjælp af siden **Forespørgsel om bilagstransaktioner** ved at angive det bilagsnummer og den dato, der er angivet i dialogboksen for årsafslutningen af det år, du lukkede, (**Finans > Forespørgsler og rapporter > Bilagstransaktioner**).

[![Forespørgsel om bilagstransaktioner.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Hvis der findes primobilag (og eventuelt ultimo), behøver du ikke at køre årsafslutningen igen. Du kan i stedet gå til næste afsnit for at få oplysninger om, hvad du skal gøre herefter.

### <a name="symptom"></a>Symptom

Trinnet "Gendan saldi" i årsafslutningen mislykkedes. Skal jeg køre hele årsafslutningen igen?

### <a name="resolution"></a>Løsning

I trinnet Generer saldi opdateres de finanssaldi, der bruges, når der genereres en forespørgsel om råbalance.  Det er det sidste trin i årsafslutningen.  Hvis dette trin er det eneste trin, der mislykkes, er bogføringen af finanstransaktionerne gennemført.  Du behøver ikke at køre årsafslutningen igen. Du kan køre processen for at gendanne saldi manuelt ved hjælp af siden **Økonomiske dimensionsopsætninger** (**Finans > Kontoplan > Dimensioner > Økonomiske dimensionssæt**).

[![Knappen Gendan saldi på siden Økonomiske dimensionssæt.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Hvis det tager lang tid at behandle dette trin, anbefaler vi, at du gennemser de bedste praksis for økonomiske dimensionssæt som beskrevet i [Bedste praksis til opdatering af økonomiske dimensionssæt](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

