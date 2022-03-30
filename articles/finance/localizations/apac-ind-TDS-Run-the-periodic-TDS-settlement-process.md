---
title: Køre den periodiske skatteudligningsproces
description: Dette emne forklarer, hvordan du udligner periodisk kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b4c3a83f3fed0907dacd415f5aff9fad3c10bc6
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408374"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Køre den periodiske skatteudligningsproces

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du udligner periodisk kildeskat (TDS – Tax Deducted at Source).

1. Gå til **Skat \> Angivelser \> A-skat \> Betaling af A-skat**.

    [![Dialogboksen Betaling af A-skat.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Vælg **Kildeskat** i feltet **Skattetype** i dialogboksen **Betaling af A-skat**.
3. Vælg det skattekontonummer (TAN), som udligningsprocessen skal køres for, i feltet **Skattekontonummer (TAN)**.
4. Vælg den skattekomponentgruppe, der skal køres udligningsproces for, i feltet **Komponentgruppe for A-skat**.
5. I feltet **Udligningsperiode** skal du vælge den skatteudligningsperiode, som udligningsprocessen skal køres for.

    > [!NOTE]
    > Skatteudligningsprocessen køres for alle perioder, der er konfigureret for skatteudligningsperioden under fanen **Perioder** på siden **Udligningsperioder for A-skat** (**Skat \> Indirekte skatter \> A-skat \> Udligningsperioder for A-skat**).

6. I feltet **Fra dato** skal du vælge den startdato, som skatteudligningsprocessen skal køres fra.

    For en bestemt periode i udligningsperioden tages den startdato, der er defineret for perioden, som "Fra"-datoen. Skatteudligningsperioden har f.eks. to perioder: 1. april til og med 30. april 2009 og 1. maj til og med 31. maj 2009. Hvis du vælger **04/06/2009** (6. april 2009) som startdato i feltet **Fra dato**, køres udligningsprocessen stadig fra 1. april 2009.

    Hvis du angiver en senere periode i feltet **Fra dato**, men uden at udligne en tidligere periode inden for udligningsperioden, vil udligningen ikke finde sted for nogen tidligere perioder. Skatteudligningsperioden har f.eks. tre perioder: 1. april til og med 30. april 2009, 1. maj til og med 31. maj 2009 og 1. juni til og med 30. juni 2009. Hvis du vælger **05/01/2009** (1. maj 2009) som startdato i feltet **Fra dato**, køres udligningsprocessen kun fra 1. maj til og med 31. maj 2009. Udligningen foretages ikke for 1. april til og med 30. april 2009.

7. I feltet **Transaktionsdato** skal du vælge den dato, hvor du vil bogføre transaktionen for skatteudligningen.
8. Vælg skatteudligningsversionen i feltet **Betalingsversion for A-skat**.

     - **Original** – Brug denne indstilling til at køre skatteudligningsprocessen første gang. Den oprindelige betalingsversion bruges kun én gang til at køre skatteudligningsprocessen for en kombination af et skattekontonummer, en komponentgruppe for A-skat og en udligningsperiode for A-skat.
    - **Seneste versioner** – Brug denne indstilling, hvis skatteudligningsprocessen allerede er kørt for den angivne periode. Medtag tilbagedaterede transaktioner, der er bogført, efter den tidligere kørsel af udligningsprocessen for perioden. Du kan bruge denne indstilling til at køre udligningsprocessen flere gange.

9. Markér afkrydsningsfeltet **Opdater** for at køre skatteudligningsprocessen og bogføre beløbene på finanskontiene. Hvis afkrydsningsfeltet ikke er markeret, køres udligningsprocessen ikke, og der genereres ikke finansposter.
10. Vælg **OK** for at køre skatteudligningsprocessen og generere betalingsrapporten for A-skat. Status for skattetransaktioner, der er inkluderet i udligningsprocessen, vises som **Udlignet** på siden **Udligning** (gå til **Kreditor \> Betalinger \> Kreditorbetalingskladde**, vælg **Linjer**, vælg **Funktioner**, og vælg derefter **Udligning**).

### <a name="important-points"></a>Vigtige punkter

- Hvis en komponentgruppe for A-skat ikke er valgt under udligningsprocessen, foretages udligningen for alle komponentgrupper for A-skat for det skattekontonummer og den udligningsperiode, der er valgt. Der oprettes en separat linje for hver komponentgruppe for A-skat på siden **Åbenpost-redigering**.
- Udligningsprocessen baseres på arten af vurderingskategorien for en udligningsperiode. De transaktioner, hvor arten af vurderingskategorien er **Virksomhed**, udlignes og vises som én linje på siden **Åbenpost-redigering**. De transaktioner, hvor arten af vurderingskategorien er noget andet end **Virksomhed**, udlignes og vises som én linje på siden **Åbenpost-redigering**.
- Forfaldsdatoen for de udlignede skattetransaktionslinjer på siden **Åbenpost-redigering** er baseret på de betalingsbetingelser, der er defineret for skattemyndighedskreditoren på siden **Kreditorer**. Hvis betalingsbetingelserne ikke er defineret for skattemyndighedskreditoren, vises den sidste dag i udligningsperioden som forfaldsdatoen.
