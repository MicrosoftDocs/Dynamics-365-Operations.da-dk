---
title: Startside for Finance insights
description: Med Finance Insights kan du konfigurere og udvide modeller, så du præcist og intelligent kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3c6320043000dc07eea3128a10c16cfd54b13334
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752850"
---
# <a name="finance-insights-home-page"></a>Startside for Finance insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Med Finance Insights kan du konfigurere og udvide modeller, så du på intelligent vis kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller. Når disse nye muligheder kombineres med automatisering i kreditorbetalinger og -rykkere, indeholder de et omfattende og intelligent økonomisystem, der styrer beslutningstagningen og hjælper dig med at reagere effektivt på eksisterende og forventede forretningsudfordringer.

> [!NOTE]
> Finance Insights, offentlig prøveversion er tilgængelig for implementering i Amerikas Forenede Stater, Canada, Storbritannien, Europa, Asien og Stillehavsområdet, Japan, Australien og New Zealand. Microsoft tilføjer trinvist understøttelse af flere regioner.

## <a name="prerequisites"></a>Forudsætninger

I dette afsnit beskrives kravene til brug af Finance Insights. Der gives så vidt muligt links til kilder til yderligere oplysninger.

### <a name="legal-requirements"></a>Juridiske krav

Hvis du vil anvende til prøveversionsprogrammet, skal du udfylde den [Finance Insights Prøveversion til Dynamics 365 Finance-aftale](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Systemkrav

Der kræves et niveau 2-miljø (flere bokse) for at få vist Finance Insights. Du kan finde flere baggrundsoplysninger om miljøer under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versionskrav

Dette emne gælder for Microsoft Dynamics 365 Finance version 10.0.21 og senere.

### <a name="historical-data-requirements"></a>Historiske datakrav

Mindst et års antal kundefakturaer er påkrævet for at træne den maskinelle indlæringsmodel, der bruges til funktionen debitorbetalingsforudsigelser, korrekt. Tre års historikdata anbefales til likviditetsbudgetter. Tre års historisk budget og/eller faktiske værdier anbefales til intelligente budgetforslag.

## <a name="configure-finance-insights"></a>Konfigurere Finance Insights

Du skal fuldføre konfigurationstrin, før du kan bruge Finance Insights. Du kan finde flere oplysninger om, hvordan du konfigurerer Finance Insights, i [Konfiguration af Finance Insights](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Oprette et dataintegratorprojekt

Du skal oprette et dataintegratorprojekt, så de data, som den maskinelle indlæringsmodel genererer, kan flyde ind i Dynamics 365 Finance. De trin, du skal oprette projektet for, finder du under [Opret et dataintegratorprojekt](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivere Finance Insights-funktioner

Når du har fuldført konfigurationstrinnene og konfigureret demodata, skal du aktivere og konfigurere hver egenskab, du vil bruge: Debitorbetalingsforudsigelser, likviditetsbudgettering og budgetforslag.

### <a name="enable-customer-payment-predictions"></a>Aktivere forudsigelser om debitorbetalinger
Hvis du bruger demodata til at teste kundens betalingsforudsigelser, kan det være nødvendigt at importere yderligere demodata for at oprette AI-modellen. 

Hvis du vil aktivere funktionen til debitorbetalinger, skal du udføre et sæt trin for at opbygge en model til maskinel indlæring, der bruger din organisations data til at generere forudsigelser om, hvornår kunderne sandsynligvis vil betale udestående fakturaer, og hvornår der sandsynligvis vil blive betalt bestemte fakturaer. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Aktivere likviditetsbudget
Hvis du vil aktivere likviditetsbudgettering, skal du udføre et sæt trin for at bygge en model til maskinel indlæring, der bruger din organisations data til at oprette likviditetsbudgetter. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere likviditetsbudget](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Aktivere likviditetsforslag

Funktionen budgetforslag bruger en model til maskinel indlæring sammen med organisationens historiske data til at generere et budgetforslag. Det genererede forslag kan hjælpe dig med at påbegynde en budgetteringsproces, der er mere effektiv end en manuel proces. Du kan finde bestemte trin til aktivering af denne funktion under [Aktivere budgetforslag](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Bruge funktionerne til Finance Insights

### <a name="using-customer-payment-predictions"></a>Bruge forudsigelser om debitorbetalinger

- Du kan få mere at vide om, hvordan du får de nødvendige oplysninger til at indsamle aktiviteter i forbindelse med forudsigelse af kundebetalinger i [Bruge forudsigelser om debitorbetalinger](use-customer-payment-predictions.md).
- Oplysninger, der kan hjælpe dig med at evaluere forudsigelsesmodellens effektivitet, når du har startet med funktionen, finder du i [Evaluering af den indledende debitorbetalingsmodel](evaluate-payment-prediction.md).
- Oplysninger, der kan hjælpe dig med at justere de data, der bruges til at opbygge prognosen og dermed forbedre effektiviteten, finder du i afsnittet [Forbedring af forudsigelsesmodellen](improve-model.md).
- Du kan finde flere oplysninger om resultaterne af AI-forudsigelsesmodeller i [Resultater af maskinel indlæringsmodeller](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Bruge Likviditetsbudget

Likviditetsbudgettet kan hjælpe dig med mere nøjagtigt at vurdere din likvide situation. Intelligent likviditetsbudgettering er bygget oven på den eksisterende funktion til likviditetsbudgettering i Dynamics 365 Finance. Gennemse den eksisterende funktion i [likviditetsbudgettering](../cash-bank-management/cash-flow-forecasting.md).

- Få mere at vide om de nye muligheder i likviditetsbudgetter under [Likviditetsbudget](cash-flow-forecast-intro.md).
- Du kan finde oplysninger om, hvordan du importerer eksterne data, så de medtages i dækningsprognosen, i [Brug eksterne data i likviditetsbudgetter](external-data-in-cash-flow.md). 
- Du kan finde flere oplysninger om, hvordan du bruger en AI-model til kortsigtet likviditet, under [Likviditet](cash-position.md).
- Du kan finde flere oplysninger om at gemme likviditetspositioner og likviditetsbudgetter som snapshots og til at sammenligne et snapshot med faktiske oplysninger i [Snapshots-oversigten](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bruge budgetforslag

Oplysninger om, hvordan du kan fremskynde oprettelsen af et budget, finder du i [Budgetforslag](budget-proposals.md). 

## <a name="feedback-and-support"></a>Feedback og support

Send en mail til [Finance Insights](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
