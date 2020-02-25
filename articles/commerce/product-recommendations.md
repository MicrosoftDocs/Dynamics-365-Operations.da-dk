---
title: Oversigt over produktanbefalinger
description: Dette emne indeholder generelle oplysninger om produktanbefalinger. Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, og endda produkter, som de oprindeligt ikke havde tænkt sig at købe.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024973"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="ddb6c-104">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ddb6c-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddb6c-105">Microsoft Dynamics 365 Commerce kan bruges til at få vist produktanbefalinger på e-handels-webstedet og POS-enheden.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="ddb6c-106">Produktanbefalinger er varer, som en kunde kan være interesseret i.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="ddb6c-107">Anbefalingerne er baseret på indkøbstendenser fra andre kunder i onlinebutikker og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="ddb6c-108">Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, mens de har en god oplevelse.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="ddb6c-109">Krydssalg og mersalg kan også bruges til at hjælpe kunder med at finde flere produkter, end de oprindeligt havde tænkt sig at købe.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="ddb6c-110">Når anbefalingerne bruges som hjælp til produktregistrering, kan de skabe flere konverteringsmuligheder, bidrage til at øge salgsindtægterne og endda forbedre kundetilfredshed og -fastholdelse.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="ddb6c-111">I Commerce er produktanbefalingerne baseret på Microsofts anbefalinger fra teknologier for maskinel indlæring i stor målestok.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="ddb6c-112">Scenarier</span><span class="sxs-lookup"><span data-stu-id="ddb6c-112">Scenarios</span></span>

<span data-ttu-id="ddb6c-113">Produktanbefalinger er tilgængelige for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="ddb6c-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="ddb6c-114">**På en butiksside til gennemsyn eller landingsside i e-handel**: Hvis kunder eller butiksansatte besøger en butiks side, kan anbefalingsprogrammet foreslå produkter på de nye lister **Nyt**, **Mest solgte** og **Mest populære**.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="ddb6c-115">**På siden Produktdetaljer:** Hvis kunder eller butiksansatte besøger siden **Produktdetaljer**, foreslår anbefalingsprogrammet yderligere varer, der formentlig også er interessante at købe.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="ddb6c-116">Disse varer vises på listen **Personer synes også om**.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="ddb6c-117">**På siden Transaktion eller ved kassen:** Anbefalingsprogrammet foreslår varer på basis af hele listen med varer i kurven.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="ddb6c-118">Disse varer vises på listen **Ofte købt sammen**.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="ddb6c-119">**Personlige anbefalinger:** Forhandlere kan give logon-kunder en personligt **udvalgt** liste samt nye funktioner, der gør det muligt at tilpasse eksisterende listescenarier efter den pågældende kunde.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="ddb6c-120">Yderligere oplysninger finder du i funktionsdokumentationen: [aktivere tilpassede anbefalinger.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="ddb6c-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="ddb6c-121">Anbefalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="ddb6c-121">Recommendation service</span></span>

<span data-ttu-id="ddb6c-122">Produktanbefalinger bruger anbefalingerne fra teknologier for maskinel indlæring på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="ddb6c-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="ddb6c-123">Data i det format, der kræves af anbefalingstjenesten, udtrækkes fra Commerce-driftsdatabasen og sendes til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="ddb6c-124">Anbefalingstjenesten bruger dataene til at træne anbefalingsmodellerne for listerne **Personer synes også om**, **Ofte købt sammen**, **Nyt**, **Mest solgte** og **Mest populære**.</span><span class="sxs-lookup"><span data-stu-id="ddb6c-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddb6c-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ddb6c-125">Additional resources</span></span>

[<span data-ttu-id="ddb6c-126">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ddb6c-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ddb6c-127">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ddb6c-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ddb6c-128">Oversigt over modulet Produktsamling</span><span class="sxs-lookup"><span data-stu-id="ddb6c-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="ddb6c-129">Oprette overvågede lister med produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ddb6c-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ddb6c-130">Administrere resultater for AI-ML-baserede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ddb6c-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ddb6c-131">Tilføje lister med produktanbefalinger på sider</span><span class="sxs-lookup"><span data-stu-id="ddb6c-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
