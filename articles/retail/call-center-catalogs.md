---
title: Callcenter-kataloger
description: I denne artikel beskrives call center-specifikke funktioner for kataloger i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="1deb6-103">Callcenter-kataloger</span><span class="sxs-lookup"><span data-stu-id="1deb6-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1deb6-104">I denne artikel beskrives call center-specifikke funktioner for kataloger i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1deb6-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1deb6-105">I et call center kan du bruge produktkataloger til at identificere de produkter, du vil tilbyde kunderne.</span><span class="sxs-lookup"><span data-stu-id="1deb6-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="1deb6-106">Call centre bruger typisk trykte kataloger.</span><span class="sxs-lookup"><span data-stu-id="1deb6-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="1deb6-107">Udformning og produktion af et trykt katalog håndteres uden for Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1deb6-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="1deb6-108">Du kan dog oprette og gemme en digital udgave af et katalog ved hjælp af de samme sider, som du bruger til at konfigurere detailkataloger.</span><span class="sxs-lookup"><span data-stu-id="1deb6-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="1deb6-109">Før du kan oprette et katalog, skal du konfigurere produktsortimenter og tildele sortimenterne til et call center.</span><span class="sxs-lookup"><span data-stu-id="1deb6-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="1deb6-110">Derefter føjer du produkter til kataloget ved at vælge produkter fra disse sortimenter.</span><span class="sxs-lookup"><span data-stu-id="1deb6-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="1deb6-111">Når der er føjet produkter til kataloget, og kataloget er fuldført, skal du validere kataloget for at kontrollere dataene.</span><span class="sxs-lookup"><span data-stu-id="1deb6-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="1deb6-112">Derefter skal du sende kataloget til gennemsyn og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="1deb6-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="1deb6-113">Når kataloget er godkendt, kan det udgives.</span><span class="sxs-lookup"><span data-stu-id="1deb6-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="1deb6-114">Når der er oprettet et call center-katalog, kan du tage et øjebliksbillede af katalogdataene på det tidspunkt, hvor kataloget udgives.</span><span class="sxs-lookup"><span data-stu-id="1deb6-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="1deb6-115">Den funktion til øjebliksbillede giver dig adgang til en bestemt version af kataloget, selvom kataloget senere bliver ændret og opdateret.</span><span class="sxs-lookup"><span data-stu-id="1deb6-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="1deb6-116">Call center-kataloger kan også konfigureres til at medtage følgende valgfri funktioner:</span><span class="sxs-lookup"><span data-stu-id="1deb6-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="1deb6-117">**Kildekoder** – Kildekoder bruges til at spore kunderespons på bestemte katalogudsendelser.</span><span class="sxs-lookup"><span data-stu-id="1deb6-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="1deb6-118">**Gratis produkter** – Produkter,, der indgår i en kundes ordre uden merpris.</span><span class="sxs-lookup"><span data-stu-id="1deb6-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="1deb6-119">Disse produkter føjes automatisk til en ordre, når kildekoden til kataloget er angivet i orden.</span><span class="sxs-lookup"><span data-stu-id="1deb6-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="1deb6-120">**Scripts** – Scripts er tekster, som en arbejder i et callcenter læser op for en debitor, når der oprettes en ordre.</span><span class="sxs-lookup"><span data-stu-id="1deb6-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="1deb6-121">Scripts kan omfatte hilsener eller indkøbsforslag.</span><span class="sxs-lookup"><span data-stu-id="1deb6-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="1deb6-122">**Sidelayout** – Et sidelayout henter sideplacering af produkter i den trykte katalog.</span><span class="sxs-lookup"><span data-stu-id="1deb6-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="1deb6-123">Disse oplysninger bruges til analyserapporten af katalogområde.</span><span class="sxs-lookup"><span data-stu-id="1deb6-123">This information is used for the catalog area analysis report.</span></span>





