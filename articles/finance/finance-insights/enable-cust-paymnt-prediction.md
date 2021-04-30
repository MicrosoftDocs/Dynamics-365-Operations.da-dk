---
title: Aktivere forudsigelser om debitorbetalinger (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights.
author: ShivamPandey-msft
ms.date: 05/27/2020
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
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0f972b6f3c0c7c4fcf69b3644a5e73d863cd817d
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897350"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="78977-103">Aktivere forudsigelser om debitorbetalinger (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="78977-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="78977-104">Dette emne forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="78977-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="78977-105">Du kan aktivere funktionen i arbejdsområdet **Administration af funktioner** og angive konfigurationsindstillingerne på siden **Finance Insights-parametre**.</span><span class="sxs-lookup"><span data-stu-id="78977-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="78977-106">Dette emne indeholder også oplysninger, der kan hjælpe dig med at bruge funktionen effektivt.</span><span class="sxs-lookup"><span data-stu-id="78977-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="78977-107">Før du fuldfører følgende trin, skal du sørge for at fuldføre de nødvendige trin i emnet [Konfigurere til Finance Insights](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="78977-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="78977-108">Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø.</span><span class="sxs-lookup"><span data-stu-id="78977-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="78977-109">Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="78977-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="78977-110">(Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)</span><span class="sxs-lookup"><span data-stu-id="78977-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="78977-111">Hvis din installation af Microsoft Dynamics 365 Finance er en Service Fabric-installation, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="78977-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="78977-112">Finance Insights-team burde allerede have aktiveret funktionen til dig.</span><span class="sxs-lookup"><span data-stu-id="78977-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="78977-113">Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="78977-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="78977-114">Slå funktionen til Indsigt i debitorbetalinger til:</span><span class="sxs-lookup"><span data-stu-id="78977-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="78977-115">Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="78977-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="78977-116">Find den funktion, der kaldes **Indsigt i debitorbetaling (prøveversoin)**.</span><span class="sxs-lookup"><span data-stu-id="78977-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="78977-117">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="78977-117">Select **Enable now**.</span></span>

    <span data-ttu-id="78977-118">Funktionen Indsigter i debitorbetaling er nu aktiveret og klar til at blive konfigureret.</span><span class="sxs-lookup"><span data-stu-id="78977-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="78977-119">Konfigurer funktionen til Indsigt i debitorbetalinger:</span><span class="sxs-lookup"><span data-stu-id="78977-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="78977-120">Gå til **Kredit og rykkere \> Opsætning \> Finance Insights \> Finance Insights-parametre**.</span><span class="sxs-lookup"><span data-stu-id="78977-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="78977-121">Siden [![Finance Insigths-parametre, før funktionen er konfigureret](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="78977-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="78977-122">På siden **Financial insights-parametre** på fanen **Indsigt i debitorbetalinger** skal du vælge **Vis de datafelter, der bruges i forudsigelsesmodellen**-linket for at åbne siden **Datafelterne til forudsigelsesmodel**.</span><span class="sxs-lookup"><span data-stu-id="78977-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="78977-123">Der kan du få vist standardlisten over felter, der bruges til at oprette en prognosemodel for kunstig intelligens (AI) for debitorbetalingsforudsigelser.</span><span class="sxs-lookup"><span data-stu-id="78977-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="78977-124">Hvis du vil bruge standardlisten over felter til at oprette forudsigelsesmodellen, skal du lukke siden **Datafelter til forudsigelsesmodel** og derefter på siden **Financial Insights-parametre** angive indstlilingen **Aktiver funktion** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="78977-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="78977-125">Angiv transaktionsperioden til "meget sent" for at definere, hvad forudsigelsen **Meget sent** betyder for virksomheden.</span><span class="sxs-lookup"><span data-stu-id="78977-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="78977-126">For hver åben faktura vil systemet estimere betalingssandsynligheden i tre filsæt: **Til tiden**, **Sent** og **Meget sent**.</span><span class="sxs-lookup"><span data-stu-id="78977-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="78977-127">**Til tiden** – Dette filsæt omfatter betalinger, der er angivet til betaling på eller før transaktionens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="78977-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="78977-128">**Sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen, men før starten af transaktionsperioden "Meget sent".</span><span class="sxs-lookup"><span data-stu-id="78977-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="78977-129">**Meget sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen "Meget sent".</span><span class="sxs-lookup"><span data-stu-id="78977-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="78977-130">Hvis du ændrer transaktions perioden "meget sent" og vælger **Skift sent-tærskel**, efter at der er oprettet en model til AI-forudsigelse for debitorbetalinger, slettes den eksisterende forudsigelsesmodel, og der oprettes en ny model.</span><span class="sxs-lookup"><span data-stu-id="78977-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="78977-131">Den nye prognosemodel flytter posteringerne til den "meget forsinkede" periode på baggrund af de indstillinger, der blev angivet for at definere den.</span><span class="sxs-lookup"><span data-stu-id="78977-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="78977-132">Når du er færdig med at definere transaktionsperioden "meget sent", skal du vælge **Opret forudsigelsesmodel** for at oprette forudsigelsesmodellen.</span><span class="sxs-lookup"><span data-stu-id="78977-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="78977-133">Afsnittet **Forudsigelsesmodel** på siden **Financial Insights-parametre** viser status for forudsigelsesmodellen.</span><span class="sxs-lookup"><span data-stu-id="78977-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="78977-134">Når forudsigelsesmodellen oprettes, kan du når som helst vælge **Nulstil modeloprettelse** for at genstarte processen.</span><span class="sxs-lookup"><span data-stu-id="78977-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="78977-135">Funktionen er nu konfigureret og klar til brug.</span><span class="sxs-lookup"><span data-stu-id="78977-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="78977-136">Når funktionen er slået til og konfigureret, og forudsigelsesmodellen er oprettet og fungerer, viser afsnittet **Forudsigelsesmodel** på siden **Financial Insights-parametre**, at modellen er nøjagtig, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="78977-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="78977-137">[![Nøjagtigheden af forudsigelsesmodellen på siden Financial Insights-parametre](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="78977-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="78977-138">Frigiv detaljer</span><span class="sxs-lookup"><span data-stu-id="78977-138">Release details</span></span>

<span data-ttu-id="78977-139">Financial Insights, offentlig prøveversion er tilgængelig for prøveimplementeringer i USA, Europa og Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="78977-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="78977-140">Microsoft tilføjer trinvist understøttelse af flere regioner.</span><span class="sxs-lookup"><span data-stu-id="78977-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="78977-141">De offentlige prøveversionsfunktioner kan og bør kun aktiveres i sandkasse miljøer i niveau 2.</span><span class="sxs-lookup"><span data-stu-id="78977-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="78977-142">Opsætnings- og AI-modeller, der er oprettet i et sandkassemiljø, kan ikke overføres til et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="78977-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="78977-143">Yderligere oplysninger finder du under [Supplerende vilkår for anvendelse af Microsoft Dynamics 365 Prøveversioner](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="78977-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="78977-144">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="78977-144">Privacy notice</span></span>

<span data-ttu-id="78977-145">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="78977-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]