---
title: Indsigt i debitorbetaling (prøveversion)
description: I dette emne beskrives muligheden for indsigt i betalinger, der hjælper med at forbedre forståelsen af individuelle kunders typiske betalingsmetoder. Funktionen kan hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end det, du måtte have udført.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
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
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644627"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="877dc-104">Indsigt i debitorbetaling (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="877dc-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="877dc-105">I dette emne beskrives muligheden for indsigt i betalinger, der hjælper med at forbedre forståelsen af individuelle kunders typiske betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="877dc-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="877dc-106">Funktionen kan hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end det, du måtte have udført.</span><span class="sxs-lookup"><span data-stu-id="877dc-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="877dc-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="877dc-107">Overview</span></span>

<span data-ttu-id="877dc-108">Det kan være svært at forudsige, hvornår kunder betaler fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="877dc-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="877dc-109">Denne manglende indsigt fører til mindre præcise likviditetsbudgetter, opkrævningsprocesser, der indledes for sent, og ordrer, der er frigivet til kunder, som kan være bagud med deres betaling.</span><span class="sxs-lookup"><span data-stu-id="877dc-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="877dc-110">Indsigt i kundebetaling (prøveversion) hjælper organisationer med at forudsige, hvornår en kundefaktura betales.</span><span class="sxs-lookup"><span data-stu-id="877dc-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="877dc-111">Disse oplysninger kan hjælpe organisationer med at oprette inkassostrategier, der forbedrer sandsynligheden for at de bliver betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="877dc-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="877dc-112">Forudsigelser</span><span class="sxs-lookup"><span data-stu-id="877dc-112">Predictions</span></span>

<span data-ttu-id="877dc-113">Betalingsprognoser giver organisationer mulighed for at forbedre deres forretningsprocesser ved at hjælpe dem med nemt at identificere de fakturaer, der sandsynligvis bliver betalt for sent, og med at træffe passende foranstaltninger, der kan forbedre sandsynligheden for at få betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="877dc-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="877dc-114">Ved hjælp af en model til maskinlæring, som udnytter historiske data for fakturaer, betalinger og kundedata, giver indsigt i debitorbetalinger (Forhåndsvisning) en mere præcis forudsigelse for, hvornår en kunde betaler en udestående faktura.</span><span class="sxs-lookup"><span data-stu-id="877dc-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="877dc-115">For hver åben faktura forudsiger Customer payment insights (prøveversion) tre betalingssandsynligheder:</span><span class="sxs-lookup"><span data-stu-id="877dc-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="877dc-116">Sandsynlighed for, at betaling sker til tiden</span><span class="sxs-lookup"><span data-stu-id="877dc-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="877dc-117">Sandsynlighed for, at der sker sen betaling</span><span class="sxs-lookup"><span data-stu-id="877dc-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="877dc-118">Sandsynlighed for, at der sker stor forsinkelse med betalingen</span><span class="sxs-lookup"><span data-stu-id="877dc-118">Probability of payment being made very late</span></span>

<span data-ttu-id="877dc-119">Customer payment insights (prøveversion) giver desuden en samlet visning over forventede betalingsbeløb, der kan hjælpe organisationer med at forstå det samlede betalingsbeløb , der kan forventes fra en kunde i en af følgende tre grupper, Til tiden, Sent og Meget sent.</span><span class="sxs-lookup"><span data-stu-id="877dc-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="877dc-120">[![Samlet visning af betalings forudsigelser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="877dc-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="877dc-121">Hver faktura tildeles desuden en sandsynlighed for, at der sker betaling til tiden.</span><span class="sxs-lookup"><span data-stu-id="877dc-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="877dc-122">Hvis sandsynligheden for betaling til tiden er mindre end 50 %, markeres fakturaerne med en rød cirkel for at angive, at disse fakturaer muligvis kræver opmærksomhed i relation til opkrævning.</span><span class="sxs-lookup"><span data-stu-id="877dc-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="877dc-123">[![Liste over sandsynlighed for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="877dc-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="877dc-124">Indsigt i debitorbetaling (Forhåndsvisning) indeholder også kontekstafhængige oplysninger, der forklarer forudsigelsen, f.eks. de primære faktorer, der har påvirket forudsigelserne, den aktuelle tilstand for erhvervsinteraktioner med kunden, og oplysninger om tidligere debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="877dc-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="877dc-125">I mange virksomheder er opkrævningsprocessen blevet en reaktivt aktivitet; opkrævningsprocessen starter ikke, før fakturaerne forfalder.</span><span class="sxs-lookup"><span data-stu-id="877dc-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="877dc-126">Med indsigt i debitorbetalinger (Forhåndsvisning) kan organisationer være mere proaktiv i forbindelse med opkrævninger.</span><span class="sxs-lookup"><span data-stu-id="877dc-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="877dc-127">De behøver ikke længere at vente på, at transaktionerne forfalder, før de indleder opkrævningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="877dc-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="877dc-128">De kan i stedet bruge funktionen betalingsforudsigelse til at bestemme, om proaktive opkrævninger vil forbedre sandsynligheden for at, der bliver betalt til tiden.</span><span class="sxs-lookup"><span data-stu-id="877dc-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="877dc-129">Betalingsforudsigelse giver også virksomhederne de oplysninger, der er nødvendige for, at opkrævningsprocessen kan påbegyndes tidligt.</span><span class="sxs-lookup"><span data-stu-id="877dc-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="877dc-130">Metode</span><span class="sxs-lookup"><span data-stu-id="877dc-130">Methodology</span></span>

<span data-ttu-id="877dc-131">Det er svært at udvikle og installere en AI-løsning.</span><span class="sxs-lookup"><span data-stu-id="877dc-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="877dc-132">Det kræver et team af dataforskere, eksperter på området og ingeniører, som arbejder i længere tid på at formulere, udvikle, implementere og vedligeholde en brugbar AI-løsning.</span><span class="sxs-lookup"><span data-stu-id="877dc-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="877dc-133">Vi gør det nemt at implementere og bruge AI-løsninger i Finance.</span><span class="sxs-lookup"><span data-stu-id="877dc-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="877dc-134">Vi pakker AI-løsninger på forhånd i Finance, der er bygget oven på Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="877dc-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="877dc-135">En slutbruger kan med et enkelt klik på knappen implementere AI-løsningen og begynde at udnytte fordelene ved intelligent forudsigelser.</span><span class="sxs-lookup"><span data-stu-id="877dc-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="877dc-136">Hvis en organisation ikke er tilfreds med nøjagtigheden af forudsigelserne, kan en superbruger, igen med blot et enkelt klik, angive erfaringen med udvidelsen AI Builder og derefter vælge eller fravælge de felter, der bruges til at oprette forudsigelser.</span><span class="sxs-lookup"><span data-stu-id="877dc-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="877dc-137">Når de er færdige, kan de øve sig i og udgive ændringerne, og den nyligt oplærte model vil automatisk blive hentet til brug for forudsigelser i Finance.</span><span class="sxs-lookup"><span data-stu-id="877dc-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="877dc-138">Sådan får du indsigt i debitorbetaling (Forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="877dc-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="877dc-139">Send email til [Customer payment insights (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at prøve Customer payment insights (prøveversion).</span><span class="sxs-lookup"><span data-stu-id="877dc-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="877dc-140">Privatlivserklæring</span><span class="sxs-lookup"><span data-stu-id="877dc-140">Privacy Notice</span></span>

<span data-ttu-id="877dc-141">Forhåndsvisning (1) kan eksempler (1) anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="877dc-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


