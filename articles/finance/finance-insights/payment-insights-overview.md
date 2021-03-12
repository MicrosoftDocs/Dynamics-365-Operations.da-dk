---
title: Forudsigelser for debitorbetaling (prøveversion)
description: I dette emne beskrives muligheden for forudsigelse af betalinger, der hjælper med at forbedre forståelsen af kunders typiske betalingsmetoder. Denne funktion kan også hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end normalt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: b321fdc185e175d9fe2673c9f1e16486efd8e798
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645667"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="f9f06-104">Forudsigelser for debitorbetaling (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="f9f06-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f9f06-105">I dette emne beskrives muligheden for forudsigelse af betalinger, der hjælper med at forbedre forståelsen af kunders typiske betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="f9f06-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="f9f06-106">Denne funktion kan også hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end normalt.</span><span class="sxs-lookup"><span data-stu-id="f9f06-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="f9f06-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="f9f06-107">Overview</span></span>

<span data-ttu-id="f9f06-108">Organisationer finde ofte svært for at forudsige, hvornår kunder betaler fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="f9f06-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="f9f06-109">Denne manglende indsigt kan forårsage følgende problemer:</span><span class="sxs-lookup"><span data-stu-id="f9f06-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="f9f06-110">Mindre præcise likviditetsbudgetter</span><span class="sxs-lookup"><span data-stu-id="f9f06-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="f9f06-111">Rykkerprocesser, der starter for sent</span><span class="sxs-lookup"><span data-stu-id="f9f06-111">Collections processes that start too late</span></span>
- <span data-ttu-id="f9f06-112">Ordrer, der er frigivet til kunder, som kan have standard på deres betaling</span><span class="sxs-lookup"><span data-stu-id="f9f06-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="f9f06-113">Customer payment predictions (prøveversion) hjælper organisationer med at forudsige, hvornår en kundefaktura betales.</span><span class="sxs-lookup"><span data-stu-id="f9f06-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="f9f06-114">De kan derfor oprette inkassostrategier, der medvirker til at øge sandsynligheden for, at de vil blive betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="f9f06-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="f9f06-115">Forudsigelser</span><span class="sxs-lookup"><span data-stu-id="f9f06-115">Predictions</span></span>

<span data-ttu-id="f9f06-116">Med kontant forudsigelser kan organisationer forbedre deres forretningsprocesser ved at hjælpe dem med at identificere de fakturaer, der forventes betalt for sent.</span><span class="sxs-lookup"><span data-stu-id="f9f06-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="f9f06-117">Organisationen kan bruge disse oplysninger til at udføre handlinger, der forbedrer risikoen for, at de vil blive betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="f9f06-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="f9f06-118">Med Customer payment predictions-funktionen bruges en maskinel indlæringsmodel til at forudsige mere præcist, hvornår en kunde vil betale en udestående faktura.</span><span class="sxs-lookup"><span data-stu-id="f9f06-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="f9f06-119">Denne maskinelle indlæringsmodel omfatter historiske fakturaer, betalinger og debitordata.</span><span class="sxs-lookup"><span data-stu-id="f9f06-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="f9f06-120">For hver åben faktura tildeler funktionen tre betalingssandsynligheder:</span><span class="sxs-lookup"><span data-stu-id="f9f06-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="f9f06-121">Sandsynligheden for, at betalingen vil blive betalt til tiden</span><span class="sxs-lookup"><span data-stu-id="f9f06-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="f9f06-122">Sandsynligheden for, at betalingen vil blive betalt senere</span><span class="sxs-lookup"><span data-stu-id="f9f06-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="f9f06-123">Sandsynligheden for, at betalingen vil blive betalt meget senere</span><span class="sxs-lookup"><span data-stu-id="f9f06-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="f9f06-124">Funktionen indeholder også en samlet visning af forventede betalinger.</span><span class="sxs-lookup"><span data-stu-id="f9f06-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="f9f06-125">[![Samlet visning af betalings forudsigelser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="f9f06-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="f9f06-126">Hver faktura tildeles en sandsynlighed for, at der sker betaling til tiden.</span><span class="sxs-lookup"><span data-stu-id="f9f06-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="f9f06-127">Fakturaer med en sandsynlighed for betaling til tiden er mindre end 50 %, markeres med en rød cirkel for at angive, at disse fakturaer muligvis kræver opmærksomhed i relation til opkrævning.</span><span class="sxs-lookup"><span data-stu-id="f9f06-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="f9f06-128">[![Liste over sandsynlighed for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="f9f06-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="f9f06-129">Customer payment predictions-funktionen indeholder også kontekstafhængige oplysninger, der forklarer forudsigelse.</span><span class="sxs-lookup"><span data-stu-id="f9f06-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="f9f06-130">Disse oplysninger omfatter de bedste faktorer, der har påvirket prognosen, den aktuelle forretningstilstand for kunden og detaljer om kundens historiske betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="f9f06-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="f9f06-131">I mange virksomheder er rykkerprocessen blevet en reaktiv aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f9f06-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="f9f06-132">Med andre ord starter rykkerprocessen først, når fakturaerne er forfaldne.</span><span class="sxs-lookup"><span data-stu-id="f9f06-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="f9f06-133">Med Customer payment predictions kan organisationer være mere proaktiv i forbindelse med opkrævninger.</span><span class="sxs-lookup"><span data-stu-id="f9f06-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="f9f06-134">De behøver ikke længere at vente på, at transaktionerne forfalder, før de indleder opkrævningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f9f06-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="f9f06-135">De kan i stedet bruge funktionen betalingsforudsigelse til at bestemme, om proaktive opkrævninger vil forbedre sandsynligheden for at, der bliver betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="f9f06-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="f9f06-136">Metode</span><span class="sxs-lookup"><span data-stu-id="f9f06-136">Methodology</span></span>

<span data-ttu-id="f9f06-137">Tidligere har det ofte været vanskeligt at udvikle og installere en kunstig intelligens (AI)-løsning.</span><span class="sxs-lookup"><span data-stu-id="f9f06-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="f9f06-138">Processen har krævet et team, der omfatter dataforskere, eksperter på området (SME'er) og ingeniører, der arbejder i længere tid på at formulere, udvikle, implementere og vedligeholde en brugbar AI-løsning.</span><span class="sxs-lookup"><span data-stu-id="f9f06-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="f9f06-139">Med kundens betalingsforudsigelser er det nemt at implementere og bruge en AI-løsning i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f9f06-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f9f06-140">Microsoft pakker AI-løsninger på forhånd, der er bygget oven på Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="f9f06-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="f9f06-141">Brugerne kan derfor anvende AI-løsningen med et enkelt klik med musen for at udnytte fordelene ved intelligent forudsigelser.</span><span class="sxs-lookup"><span data-stu-id="f9f06-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="f9f06-142">Hvis du ikke er tilfreds med nøjagtigheden af forudsigelserne, kan en superbruger (igen med blot et enkelt klik) angive erfaringen med udvidelsen AI Builder og derefter vælge eller fravælge de felter, der bruges til at oprette forudsigelser.</span><span class="sxs-lookup"><span data-stu-id="f9f06-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="f9f06-143">Når du er færdig, kan du "træne" modellen og udgive ændringerne.</span><span class="sxs-lookup"><span data-stu-id="f9f06-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="f9f06-144">Den nyoplærte model vil automatisk blive valgt til at generere forudsigelser i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f9f06-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="f9f06-145">Frigiv detaljer</span><span class="sxs-lookup"><span data-stu-id="f9f06-145">Release details</span></span>

<span data-ttu-id="f9f06-146">Financial Insights, offentlig prøveversion er tilgængelig for prøveimplementeringer i USA, Europa og Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="f9f06-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="f9f06-147">Microsoft tilføjer trinvist understøttelse af yderligere områder.</span><span class="sxs-lookup"><span data-stu-id="f9f06-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="f9f06-148">De offentlige prøveversionsfunktioner kan og bør kun aktiveres i sandkassemiljøer i niveau 2.</span><span class="sxs-lookup"><span data-stu-id="f9f06-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="f9f06-149">Opsætnings- og AI-modeller, der er oprettet i et sandkassemiljø, kan ikke overføres til et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="f9f06-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="f9f06-150">Yderligere oplysninger finder du under [Supplerende vilkår for anvendelse af Microsoft Dynamics 365 Prøveversioner](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="f9f06-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f9f06-151">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="f9f06-151">Privacy notice</span></span>

<span data-ttu-id="f9f06-152">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="f9f06-152">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>