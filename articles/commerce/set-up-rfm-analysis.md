---
title: Konfigurere RFM-analyse (Recency, Frequency, Monetary)
description: Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1f91a67ebac212f72b5524723ec0b8b4e0e3e99
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028269"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Konfigurere RFM-analyse (Recency, Frequency, Monetary)

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.

En RFM-analyse (Recency, Frequency, Monetary) er et marketingværktøj, som din organisation kan bruge til at evaluere de data, der genereres ved debitors køb. Når du har konfigureret RFM-analysen, får debitorer tildelt et beregnet RFM-point, når de foretager indkøb. RFM-resultatet kan være en trecifret vurdering eller et samlet tal, afhængigt af hvordan organisationen har konfigureret RFM-analysen. Her kan du se, hvordan vurderingen fungerer, hvis organisationen bruger en trecifret vurdering til pointene:

- Det første ciffer svarer til debitorens seneste klassificering, dvs. hvornår debitoren senest har foretaget et køb i din organisation.
- Det andet ciffer er debitorens frequency-vurdering, dvs. hvor ofte debitoren foretager køb i din organisation.
- Det tredje ciffer er debitorens monetary-vurdering, dvs. hvor mange penge, debitoren bruger, når vedkommende foretager køb fra din organisation.

Din organisation har f.eks. oprettet vurderingerne på en skala fra 1 til 5, hvor 5 er den højeste vurdering. I dette tilfælde fortæller en debitorvurdering på 535 dig følgende oplysninger om debitoren:

- **Recency-vurdering på 5** – Debitoren har foretaget et køb for nylig.
- **Frequency-vurdering på 3** – Debitoren køber produkter fra din organisation med moderat hyppighed.
- **Monetary-vurdering på 5** – Når debitoren foretager et køb, bruger vedkommende en betydelig mængde penge.

Hvis organisationen bruger en samlet tal for resultatet, lægges de enkelte vurderinger sammen. Debitoren har i samme eksempel en vurdering på 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Oprette RFM-analyse for kunderne i organisationen

1. Gå til **Callcenter** \> **Periodisk** \> **RFM-analyse**.
2. På siden **RFM-analyse** skal du vælge **Ny**. Indtast et beskrivende navn til RFM-definition i feltet **RFM-definition**. Du kunne f.eks. kalde definitionen RFM-A.
3. Angiv en startdato og slutdato for denne RFM-definition.
4. Benyt følgende fremgangsmåde i oversigtspanelet **Generelt**:

    - Hvis hver del af RFM-resultatet skal indeholde et lige antal debitorer, kan du markere afkrydsningsfeltet **Lige distribution**.
    - Markér afkrydsningsfeltet **Tilføj scorer** for at samle de tre resultater. Dette ville f.eks. give en debitor et RFM-resultat på 13 i stedet for 535.
    - Markér afkrydsningsfeltet **Gem historik** for at kræve, at systemet skal gemme de statistiske data for debitorer, så dataene kan bruges til at beregne RFM-resultatet.

5. Benyt følgende fremgangsmåde i oversigtspanelet **Recency**:

    - I feltet **Afdelinger** skal du angive antallet af afdelinger eller grupper, der skal bruges til at beregne recency-resultatet for debitorer. Hvis du f.eks. har 100 debitorer, betyder en opdeling af 5, at der er 20 debitorer for hvert resultat. De 20 kunder, der har foretaget de seneste køb, har et recency-resultat på 5. De næste 20 kunder har et recency-resultat på 4 osv. Hvis du har 50 debitorer, har 10 kunder et recency-resultat på 5, 10 har et recency-resultat på 4 osv.
    - I feltet **Prioritet** skal du vælge, hvor stor vægt der skal gives for parameteren recency i forhold til de andre parametre, når RFM-resultatet beregnes for en debitor. Det kunne f.eks. være, at du vil angive en større værdi for recency-resultatet end det pengemæssige resultat.
    - I feltet **Multiplikator** skal du angive den værdi, som recency-resultatet skal ganges med. Hvis du ikke angiver en værdi, multipliceres resultatet ikke.
    - I feltet **Periode** skal du vælge den tidsperiode, for hvilken recency-resultatet beregnes. F.eks. pr. uge eller pr. måned.

6. Benyt følgende fremgangsmåde i oversigtspanelet **Frekvens**:

    - I feltet **Afdelinger** skal du angive antallet af afdelinger eller grupper, der skal bruges til at beregne frekvensscore for debitorer.
    - I feltet **Prioritet** skal du vælge, hvor stor vægt der skal gives for parameteren frequency i forhold til de andre, når RFM-resultatet beregnes for en debitor.
    - I feltet **Multiplikator** skal du angive den værdi, som frekvensscore skal ganges med. Hvis du ikke angiver en værdi, multipliceres resultatet ikke.

7. Benyt følgende fremgangsmåde i oversigtspanelet **Monetær**:

    - I feltet **Afdelinger** skal du angive antallet af afdelinger eller grupper, der skal bruges til at beregne pengescoren for debitorer.
    - I feltet **Prioritet** skal du vælge, hvor stor vægt der skal gives for parameteren monetary i forhold til de andre, når RFM-resultatet beregnes for en debitor.
    - I feltet **Multiplikator** skal du angive den værdi, som pengescoren skal ganges med. Hvis du ikke angiver en værdi, multipliceres resultatet ikke.
    - I feltet **Brutto/netto** skal du angive, om debitors pengemæssige resultat skal beregnes ved hjælp af brutto- eller nettofakturabeløb.
    - Hvis en debitors returbeløb skal trækkes fra debitorens samlede faktura, skal du markere afkrydsningsfeltet **Fratræk returneringer**.

## <a name="view-a-customers-rfm-score"></a>Se en kundes RFM-score

Brug denne procedure til at få vist en kundes RFM-score.

1. Gå til **Callcenter** \> **Kladder** \> **Kundeservice**.
2. På siden **Kundeservice** i ruden **Kundeservice** skal du i søgefelterne vælge den nøgleordstype, der skal bruges til at søge efter, og skrive søgeteksten.
3. Vælg **Søg**.
4. På siden **Kundesøgning** skal du vælge den ønskede kundepost og derefter klikke på **Vælg debitor**.

RFM-scoren vises i gruppen **Ordrehistorik** i højre side af siden **Kundeservice**.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Vise eller rydde historikken for en RFM-analysepost

Du kan bruge denne procedure til at få vist eller rydde historikken for en RFM-analysepost.

1. Gå til **Callcenter** \> **Periodisk** \> **RFM-analyse**.
2. Vælg den post, du vil have vist, på siden **RFM-analyse**.
3. Vælg oversigtspanelet **Historik** for at få vist historikken for posten.
4. Vælg **Ryd historik** for at rydde historikken for posten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]