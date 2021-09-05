---
title: Startside for Finance insights
description: Med Finance Insights kan du konfigurere og udvide modeller, så du præcist og intelligent kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: 4b77b7872ed163a94ab57e4efea8fe0fbca22156
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386380"
---
# <a name="finance-insights-home-page"></a>Startside for Finance insights

[!include [banner](../includes/banner.md)]

Med Finance Insights kan du konfigurere og udvide modeller, så du præcist og intelligent kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller. Når disse nye muligheder kombineres med automatisering i kreditorbetalinger og -rykkere, indeholder de et omfattende og intelligent økonomisystem, der styrer beslutningstagningen og hjælper dig med at reagere effektivt på eksisterende og forventede forretningsudfordringer.

> [!NOTE]
> Financial Insights, offentlig prøveversion er tilgængelig for implementering i USA, Canada, Storbritannien, Europa, Asien og Stillehavsområdet, Australien og New Zealand. Microsoft tilføjer trinvist understøttelse af flere regioner. Hvis du vil aktivere Økonomiindsigt i produktionsmiljøer, skal egenskaberne [Eksporter til Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) først aktiveres i produktionsmiljøet.

> [!NOTE]
> Denne funktionalitet tilbydes som en række prøveversionsfunktioner. Under kørsel af en prøveversionsfunktion bør du ikke bruge de oprettede modeller til maskinel indlæring til at danne grundlag for eller påvirke virksomhedens beslutninger eller budgetteringsforslag. Din brug af funktionen styres af [supplerende vilkår for anvendelse](https://go.microsoft.com/fwlink/?linkid=2105274).

## <a name="prerequisites"></a>Forudsætninger

I dette afsnit beskrives kravene til brug af Finance Insights. Der gives så vidt muligt links til kilder til yderligere oplysninger.

### <a name="legal-requirements"></a>Juridiske krav

Hvis du vil anvende til prøveversionsprogrammet, skal du udfylde den [Finance Insights Prøveversion til Dynamics 365 Finance-aftale](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Systemkrav

Der kræves et niveau 2-miljø (flere bokse) for at få vist Finance Insights. Du kan finde flere baggrundsoplysninger om miljøer under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versionskrav

Dette dokument gælder for version 10.0.11 af Finance and Operations-apps (platformsopdatering 35) og nyere versioner.

### <a name="historical-data-requirements"></a>Historiske datakrav

Mindst et års antal kundefakturaer er påkrævet for at træne den maskinelle indlæringsmodel, der bruges til funktionen debitorbetalingsforudsigelser, korrekt.

### <a name="role-and-permission-requirements"></a>Rolle- og tilladelseskrav

Der vil blive foretaget ændringer af Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS) Power Apps og Azure. Der kræves de rette tilladelser på tværs af disse miljøer. Her er nogle eksempler på de ændringer, der vil blive foretaget:

- Der oprettes et nyt miljø i Microsoft Power Platform.
- Der oprettes en lagerkonto, key vault og program i Azure.
- Active Directory-lejeradministratoren skal godkende programmet AI Builder for at få adgang til Data Lake.
- Funktionen vil blive slået til i Dynamics 365.

Det er en god ide at oprette og administrere ressourcer i Azure, Microsoft Dataverse, og LCS vil være nyttig, når du udfører denne proces.

## <a name="configure-finance-insights"></a>Konfigurere Finance Insights

Du skal fuldføre nogle konfigurationstrin, før du kan bruge Finance Insights. Du kan finde flere oplysninger om, hvordan du kan konfigurere Finance Insights, i:
  - For versioner op til 10.0.19: [Konfiguration for Finance insights (forhåndsversion) - versioner op til 10.0.19](configure-for-fin-insites.md).
  - For version 10.0.20 og senere: [Konfiguration for Finance Insights (forhåndsversion) - version 10.0.20 og senere](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Oprette et dataintegratorprojekt

Du skal oprette et dataintegratorprojekt, så de data, som den maskinelle indlæringsmodel genererer, kan flyde ind i Dynamics 365 Finance. De trin, du skal oprette projektet for, finder du under [Opret et dataintegratorprojekt](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivere Finance Insights-funktioner

Når du har fuldført konfigurationstrinnene og konfigureret demodata, skal du aktivere og konfigurere hver egenskab, du vil bruge: Debitorbetalingsforudsigelser, likviditetsbudgettering og budgetforslag.

### <a name="enable-customer-payment-predictions"></a>Aktivere forudsigelser om debitorbetalinger
Hvis du bruger demodata til at teste kundens betalingsforudsigelser, kan det være nødvendigt at importere yderligere demodata for at oprette AI-modellen. 

Hvis du vil aktivere funktionen til debitorbetalinger, skal du udføre et sæt trin for at opbygge en model til maskinel indlæring, der bruger organisationens data til organisationens data for at generere forudsigelser om, hvornår kunderne sandsynligvis vil betale udestående fakturaer, og hvornår der sandsynligvis vil blive betalt bestemte fakturaer. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Aktivere likviditetsbudget
Hvis du vil aktivere likviditetsbudgettering, skal du udføre et sæt trin for at bygge en model til maskinel indlæring, der bruger din organisations data til at oprette likviditetsbudgetter. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere likviditetsbudget](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Aktivere likviditetsforslag

Funktionen budgetforslag bruger en model til maskinel indlæring sammen med organisationens historiske data til at generere et budgetforslag. Det genererede forslag kan hjælpe dig med at påbegynde en budgetteringsproces, der er mere effektiv end en manuel proces. Du kan finde bestemte trin til aktivering af denne funktion under [Aktivere budgetforslag](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Bruge funktionerne til Finance Insights

### <a name="using-customer-payment-predictions"></a>Bruge forudsigelser om debitorbetalinger

Intelligent likviditetsbudgettering er bygget oven på eksisterende funktionen til likviditetsbudgettering i Dynamics 365 Finance. Gennemse den eksisterende funktion i [likviditetsbudgettering](../cash-bank-management/cash-flow-forecasting.md).

- Du kan få mere at vide om, hvordan du får de nødvendige oplysninger til at indsamle aktiviteter i forbindelse med indsamling af kundebetalinger i [Brug af debitorbetalingsforudsigelser](use-customer-payment-predictions.md).
- Oplysninger, der kan hjælpe dig med at evaluere forudsigelsesmodellens effektivitet, når du har startet med funktionen, finder du i [Evaluering af den indledende debitorbetalingsmodel](evaluate-payment-prediction.md).
- Oplysninger, der kan hjælpe dig med at justere de data, der bruges til at opbygge prognosen og dermed forbedre effektiviteten, finder du i afsnittet [Forbedring af forudsigelsesmodellen](improve-model.md).

Du kan finde flere oplysninger om resultaterne af AI-forudsigelsesmodeller i [Resultater af maskinel indlæringsmodeller](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Bruge Likviditetsbudget

Likviditetsbudgettet kan hjælpe dig med mere nøjagtigt at vurdere din likvide situation. 

- Få mere at vide om de nye muligheder i likviditetsbudgetter under [Likviditetsbudget](cash-flow-forecast-intro.md).
- Du kan finde oplysninger om, hvordan du importerer eksterne data, så de medtages i dækningsprognosen, i [Brug eksterne data i likviditetsbudgetter](external-data-in-cash-flow.md). 
- Du kan finde flere oplysninger om, hvordan du bruger en AI-model til kortsigtet likviditet, under [Likviditet](cash-position.md).
- Du kan finde flere oplysninger om at gemme likviditetspositioner og likviditetsbudgetter som snapshots og til at sammenligne et snapshot med faktiske oplysninger i [Snapshots-oversigten](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bruge budgetforslag

Oplysninger om, hvordan du kan fremskynde oprettelsen af et budget, finder du i [Budgetforslag](budget-proposals.md). 

## <a name="feedback-and-support"></a>Feedback og support

Send en email til [Indsigt i debitorbetaling (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
