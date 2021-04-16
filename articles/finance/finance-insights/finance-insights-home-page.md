---
title: Startside for Finance Insights (prøveversion)
description: Med Finance Insights kan du konfigurere og udvide modeller, så du præcist og intelligent kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller.
author: ShivamPandey-msft
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 502205f76f1519153caf6e976ffbb5eb9412c4ea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818554"
---
# <a name="finance-insights-home-page-preview"></a>Startside for Finance Insights (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Med Finance Insights kan du konfigurere og udvide modeller, så du præcist og intelligent kan forudsige virksomhedens pengestrøm, forudsige, hvornår du vil modtage betaling for udestående tilgodehavender, og generere et budgetforslag, der kan gøre budgetteringsprocessen hurtigere. Alle disse funktioner er baseret på intelligente Machine Learning-modeller. Når disse nye muligheder kombineres med automatisering i kreditorbetalinger og -rykkere, indeholder de et omfattende og intelligent økonomisystem, der styrer beslutningstagningen og hjælper dig med at reagere effektivt på eksisterende og forventede forretningsudfordringer.

Financial Insights prøveversion er tilgængelig for prøveimplementeringer i USA, Europa og Storbritannien. Microsoft tilføjer trinvist understøttelse af flere regioner.

Prøveversionsfunktioner kan og bør kun aktiveres i sandkasse miljøer i niveau 2. Opsætnings- og kunstige AI-modeller, der er oprettet i et sandkassemiljø, kan ikke overføres til et produktionsmiljø. Yderligere oplysninger finder du under [Supplerende vilkår for anvendelse af Microsoft Dynamics 365 Prøveversioner](https://docs.microsoft.com/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.).

## <a name="prerequisites"></a>Forudsætninger

I dette afsnit beskrives kravene til brug af Finance Insights. Der gives så vidt muligt links til kilder til yderligere oplysninger.

### <a name="legal-requirements"></a>Juridiske krav

Hvis du vil anvende til prøveversionsprogrammet, skal du udfylde den [Finance Insights Prøveversion til Dynamics 365 Finance-aftale](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Systemkrav

Der kræves et niveau 2-sandkassemiljø (flere bokse) for at få vist Finance Insights. Du kan finde flere baggrundsoplysninger om miljøer under [Miljøplanlægning](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

### <a name="version-requirements"></a>Versionskrav

Dette dokument gælder for version 10.0.11 af Finance and Operations-apps (platformsopdatering 35) og nyere versioner.

### <a name="historical-data-requirements"></a>Historiske datakrav

Mindst et års antal kundefakturaer er påkrævet for at træne den maskinelle indlæringsmodel, der bruges til funktionen debitorbetalingsforudsigelser, korrekt.

Der findes eksempeldata til demosystemer, hvor Contoso-demonstrationsdata er angivet.

### <a name="role-and-permission-requirements"></a>Rolle- og tilladelseskrav

Der vil blive foretaget ændringer af Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS) Power Apps og Azure. Der kræves de rette tilladelser på tværs af disse miljøer. Her er nogle eksempler på de ændringer, der vil blive foretaget:

- Der oprettes et nyt miljø i Microsoft Power Platform.
- Der oprettes en lagerkonto, key vault og program i Azure.
- Active Directory-lejeradministratoren skal godkende programmet AI Builder for at få adgang til Data Lake.
- Funktionen vil blive slået til i Dynamics 365.

Det er en god ide at oprette og administrere ressourcer i Azure, Microsoft Dataverse, og LCS vil være nyttig, når du udfører denne proces.

## <a name="configure-finance-insights"></a>Konfigurere Finance Insights

Du skal fuldføre nogle konfigurationstrin, før du kan bruge Finance Insights. Du kan finde flere oplysninger om, hvordan du konfigurerer Finance Insights, i [Konfiguration af Finance Insights](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Oprette et dataintegratorprojekt

Du skal oprette et dataintegratorprojekt, så de data, som den maskinelle indlæringsmodel genererer, kan flyde ind i Dynamics 365 Finance. De trin, du skal oprette projektet for, finder du under [Opret et dataintegratorprojekt](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivere Finance Insights-funktioner

Når du har fuldført konfigurationstrinnene og konfigureret demodata, skal du aktivere og konfigurere hver egenskab, du vil bruge: Debitorbetalingsforudsigelser, likviditetsbudgettering og budgetforslag.

### <a name="enable-customer-payment-predictions"></a>Aktivere forudsigelser om debitorbetalinger
Hvis du bruger demodata til at teste kundens betalingsforudsigelser, kan det være nødvendigt at importere yderligere demodata for at oprette AI-modellen. De specifikke trin til import af demodata finder du i [Opsætning af demodata til betalingsforudsigelser](set-up-demo-data.md).

Hvis du vil aktivere funktionen til debitorbetalinger, skal du udføre et sæt trin for at opbygge en model til maskinel indlæring, der bruger organisationens data til organisationens data for at generere forudsigelser om, hvornår kunderne sandsynligvis vil betale udestående fakturaer, og hvornår der sandsynligvis vil blive betalt bestemte fakturaer. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Aktivere likviditetsbudget
Hvis du vil aktivere likviditetsbudgettering, skal du udføre et sæt trin for at bygge en model til maskinel indlæring, der bruger de organisationsdata, som organisationens data skal oprette likviditetsbudgetter til. Yderligere oplysninger og trin, der skal udføres, finder du i afsnittet [Aktivere likviditetsbudget](enable-cash-flow-forecasting.md). 

### <a name="set-up-and-use-cash-flow-forecasting"></a>Oprette og bruge likviditetsbudgettering
Du kan finde oplysninger om, hvordan du konfigurerer og bruger likviditetsbudgettering, i [Aktivere likviditetsbudget](enable-cash-flow-forecasting.md). Du kan finde flere oplysninger om, hvordan du bruger denne funktion i [Likviditetsbudget](cash-flow-forecast-intro.md).

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
- Du kan finde oplysninger om, hvordan du importerer eksterne data, så de medtages i disponeringsprognosen, i [Brug eksterne data i likviditetsbudgetter](external-data-in-cash-flow.md). 
- Du kan finde flere oplysninger om, hvordan du bruger en AI-model til en langsigtet likviditetsflow under [Oversigt for likviditetsbudgetter](cash-position.md).
- Du kan finde flere oplysninger om at gemme likviditetspositioner og likviditetsbudgetter som snapshots og til at sammenligne et snapshot med faktiske oplysninger i [Snapshots-oversigten](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bruge budgetforslag

Oplysninger om, hvordan du kan fremskynde oprettelsen af et budget, finder du i [Budgetforslag](budget-proposals.md). 

Demodata til budgetforslag:

## <a name="feedback-and-support"></a>Feedback og support

Send en e-mail til [Indsigt i debitorbetaling (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]