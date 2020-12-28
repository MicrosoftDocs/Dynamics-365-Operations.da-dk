---
title: Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø
description: Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til evalueringsversionen af Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410978"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="81cd5-103">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81cd5-104">Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til evalueringsversionen af Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="81cd5-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="81cd5-105">**Kan vi bruge miljøet til evalueringsversionen af Commerce som en e-handel-butiksfacade for kunder, der i øjeblikket implementerer Retail?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="81cd5-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="81cd5-106">No.</span></span> <span data-ttu-id="81cd5-107">Commerce-evalueringsmiljøet er kun til evaluering.</span><span class="sxs-lookup"><span data-stu-id="81cd5-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="81cd5-108">Hvis du har brug for et miljø til en kunde, der implementerer Retail, skal du kontakte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81cd5-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="81cd5-109">**Kan evalueringsmiljøet til af Commerce bruges til at klargøre e-handel-funktionerne oven på et eksisterende program/miljø, der implementerer Retail?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="81cd5-110">Nej (hovedsageligt).</span><span class="sxs-lookup"><span data-stu-id="81cd5-110">No (mostly).</span></span> <span data-ttu-id="81cd5-111">Commerce-evalueringskomponenterne er kun tilgængelige for de miljøer, der svarer til de konfigurationer, der er angivet i guiden for forudsætninger og klargøring.</span><span class="sxs-lookup"><span data-stu-id="81cd5-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="81cd5-112">Derudover er de nødvendige grundlæggende demonstrationsdata ikke tilgængelige i miljøer, der er implementeret med en første udgivelse, der er tidligere end 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="81cd5-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="81cd5-113">**Hvilke omkostninger er der forbundet med implementeringen af evalueringsmiljøet til Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="81cd5-114">Et traditionelt demonstrationsmiljø for Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce-hovedkontoret (virtuel maskine \[VM\]) hostes i dit Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="81cd5-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="81cd5-115">Du kan bruge [Azure prisberegneren](https://azure.microsoft.com/pricing/calculator/) til at anslå denne omkostning.</span><span class="sxs-lookup"><span data-stu-id="81cd5-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="81cd5-116">Andre komponenter som f. eks. Commerce Scale Unit, Commerce Site Builder, og dit e-handels-websted vil være tilgængeligt som software som en tjeneste (SaaS) og hostes af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81cd5-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="81cd5-117">**Hvilke geografiske Azure-områder understøttes i øjeblikket for evalueringsmiljøet til Commerce?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="81cd5-118">Evalueringsmiljøet til Commerce kan kun implementeres i det nordamerikanske område.</span><span class="sxs-lookup"><span data-stu-id="81cd5-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="81cd5-119">**Findes der en virtuel harddisk (VHD), der kan downloades, og som har den komplette indstilling for en virtuel maskine med én boks (VM)?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="81cd5-120">Dynamics 365 Commerce og Commerce Scale Unit er udelukkende software som en service (SaaS) og skal være hostet i skyen.</span><span class="sxs-lookup"><span data-stu-id="81cd5-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="81cd5-121">**Hvor længe kan evalueringsmiljøet til Commerce bruges?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="81cd5-122">Der er en frist på 30 dage for Commerce-evalueringsmiljøet fra den dato, hvor SaaS-komponenter som f.eks. Commerce Scale Unit, Commerce-webstedsgenerator og dit e-handelssted klargøres.</span><span class="sxs-lookup"><span data-stu-id="81cd5-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="81cd5-123">**Kan jeg forlænge fristen for mit evalueringsmiljø til Commerce?**</span><span class="sxs-lookup"><span data-stu-id="81cd5-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="81cd5-124">Forlængelsen af tidsfristen er en undtagelse fra normen og tages i betragtning ved hvert enkelt tilfælde.</span><span class="sxs-lookup"><span data-stu-id="81cd5-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="81cd5-125">Du skal rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="81cd5-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81cd5-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="81cd5-126">Additional resources</span></span>

[<span data-ttu-id="81cd5-127">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="81cd5-128">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="81cd5-129">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="81cd5-130">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="81cd5-131">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="81cd5-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
