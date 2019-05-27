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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566231"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="5f02d-103">Indsigt i kundebetaling (eksempel)</span><span class="sxs-lookup"><span data-stu-id="5f02d-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="5f02d-104">Denne funktion er en del af en målrettet version og er kun tilgængelig for brugere, der har valgt at deltage i private prøveversioner.</span><span class="sxs-lookup"><span data-stu-id="5f02d-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="5f02d-105">Denne funktion medtages i en kommende almindeligt tilgængelig version.</span><span class="sxs-lookup"><span data-stu-id="5f02d-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="5f02d-106">Overblik</span><span class="sxs-lookup"><span data-stu-id="5f02d-106">Overview</span></span>

<span data-ttu-id="5f02d-107">Organisationer finde ofte svært for at forudsige, hvornår en kunde betaler fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="5f02d-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="5f02d-108">Denne manglende indsigt kan resultere i forkerte likviditetsbudgetter, ineffektive rykkerprocesser og risikoen for, at ordrer udleveres til kunder, der kan udgøre en risiko.</span><span class="sxs-lookup"><span data-stu-id="5f02d-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="5f02d-109">Indsigt i kundebetaling (eksempel) bruger maskinel indlæring til at forudsige, hvornår en faktura betales.</span><span class="sxs-lookup"><span data-stu-id="5f02d-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="5f02d-110">Den indeholder også optimeringsstrategier, der kan tilpasses for at maksimere sandsynligheden for, at kunder betaler til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="5f02d-111">Forudsigelser</span><span class="sxs-lookup"><span data-stu-id="5f02d-111">Predictions</span></span>

<span data-ttu-id="5f02d-112">Betalingsforudsigelsen giver organisationerne mulighed for at forbedre deres forretningsprocesser ved at hjælpe med at:</span><span class="sxs-lookup"><span data-stu-id="5f02d-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="5f02d-113">Nemt identificere de fakturaer, der forventes at blive betalt for sent.</span><span class="sxs-lookup"><span data-stu-id="5f02d-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="5f02d-114">Træffe passende foranstaltninger til forbedring af chancen for at blive betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="5f02d-115">Indsigt i kundebetaling (eksempel) bruger maskinel indlæring til at forudsige, hvornår en faktura betales.</span><span class="sxs-lookup"><span data-stu-id="5f02d-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="5f02d-116">Bruger historiske faktura-, betalings- og kundedata til at oprette en model til maskinel læring, der bruges til at forudsige, hvornår en faktura bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="5f02d-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="5f02d-117">For hver åben faktura forudsiger Indsigt i kundebetaling (eksempel) tre betalingssandsynligheder:</span><span class="sxs-lookup"><span data-stu-id="5f02d-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="5f02d-118">Sandsynligheden for betaling til tiden (inden for fakturaens forfaldsdato).</span><span class="sxs-lookup"><span data-stu-id="5f02d-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="5f02d-119">Sandsynligheden for betaling inden for 30 dage efter fakturaens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="5f02d-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="5f02d-120">Sandsynligheden for betaling senere end 30 dage efter fakturaens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="5f02d-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="5f02d-121">Sandsynligheden for at betalinger kan ses i afsnittet Forudsigelse.</span><span class="sxs-lookup"><span data-stu-id="5f02d-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="5f02d-122">[![Betalingsforudsigelser](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="5f02d-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="5f02d-123">Hver faktura tildeles også en vindende sandsynlighed for betaling ved hjælp af et af tre forventede betalingssandsynlighedsscenarier, der er defineret ovenfor.</span><span class="sxs-lookup"><span data-stu-id="5f02d-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="5f02d-124">Scenariet med den højeste sandsynlighed for betaling er det vindende scenario.</span><span class="sxs-lookup"><span data-stu-id="5f02d-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="5f02d-125">Lad os f.eks. antage at forudsigelsen for en faktura viser 71 % sandsynlighed for, at fakturaen betales til tiden, 13 % sandsynlighed for, at fakturaen betales inden for 30 dage efter forfald, og 16 % sandsynlighed for, at fakturaen betales mere end 30 dage efter forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f02d-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="5f02d-126">Den største sandsynlighed viser, at fakturaen er i scenariet med betaling til tiden, så fakturaen skal mærkes med sandsynligheden for, at den betales til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="5f02d-127">[![Betalingsforudsigelser](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="5f02d-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="5f02d-128">Optimeringsstrategier</span><span class="sxs-lookup"><span data-stu-id="5f02d-128">Optimization strategies</span></span>

<span data-ttu-id="5f02d-129">Ud over prognoser for betaling kan Indsigt i kundebetaling (eksempel) bruge optimeringsstrategier til at forbedre chancerne for at modtage betaling til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="5f02d-130">Dette giver organisationer mulighed for at foretage 'Hvad, hvis'-analyser ved at tillade brugerne at justere faktura- og kundeparametre og derefter sammenligne virkningen af sandsynligheden for at modtage betaling af fakturaer til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="5f02d-131">En organisation kan f.eks. evaluere effekten af opdatering af kasserabatten på fakturaer på sandsynligheden for modtagelse af betalingen til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="5f02d-132">Når fakturaerne er optimeret til at bruge den nye rabat, kan brugerne gennemse resultatet af at anvende rabatten på sandsynligheden for modtagelse af betalinger for disse fakturaer til tiden.</span><span class="sxs-lookup"><span data-stu-id="5f02d-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="5f02d-133">Hvis omkostningerne ved anvendelse af rabatten er minimal, sammenlignet med fordelene ved at få betaling til tiden, kan organisationen vælge at anvende den valgte rabat på alle fremtidige åbne ordrer.</span><span class="sxs-lookup"><span data-stu-id="5f02d-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="5f02d-134">I øjeblikket er kun rabat tilgængelig som en optimeringsstrategi for Indsigt i kundebetaling (eksempel).</span><span class="sxs-lookup"><span data-stu-id="5f02d-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="5f02d-135">[![Optimerede forudsigelsen](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="5f02d-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="5f02d-136">Sådan får du Indsigt i kundebetaling (eksempel)</span><span class="sxs-lookup"><span data-stu-id="5f02d-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="5f02d-137">Hvis du er interesseret i at prøve Indsigt i kundebetaling (eksempel), skal du sende en mail til [Finance Insights Preview team](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="5f02d-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="5f02d-138">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="5f02d-138">Privacy Statement</span></span>

<span data-ttu-id="5f02d-139">Eksempler gemmer kundedata i USA.</span><span class="sxs-lookup"><span data-stu-id="5f02d-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="5f02d-140">Desuden kan eksempler (1) anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 for Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="5f02d-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
