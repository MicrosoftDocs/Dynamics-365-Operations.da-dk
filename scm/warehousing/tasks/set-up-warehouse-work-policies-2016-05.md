--- 
title: 'Konfigurere politikker for lagerstedsarbejde '
description: Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="8d003-103">Konfigurere politikker for lagerstedsarbejde </span><span class="sxs-lookup"><span data-stu-id="8d003-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d003-104">Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="8d003-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="8d003-105">Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og placering af færdigvarer på lager for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="8d003-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="8d003-106">USMF-demodatafirmaet blev brugt til at oprette denne registrering.</span><span class="sxs-lookup"><span data-stu-id="8d003-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="8d003-107">Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8d003-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="8d003-108">Gå til Lagerstyring > Konfiguration > Arbejde > Arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="8d003-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="8d003-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8d003-109">Click New.</span></span>
3. <span data-ttu-id="8d003-110">Skriv 'Ikke læg-på-lager-arbejde' i navnefeltet Arbejdspolitik.</span><span class="sxs-lookup"><span data-stu-id="8d003-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="8d003-111">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8d003-111">Click Save.</span></span>
5. <span data-ttu-id="8d003-112">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8d003-112">Click Add.</span></span>
6. <span data-ttu-id="8d003-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8d003-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="8d003-114">Vælg 'Færdige varer lægges på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="8d003-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="8d003-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8d003-115">Click Add.</span></span>
9. <span data-ttu-id="8d003-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8d003-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="8d003-117">Vælg 'Samprodukter eller biprodukter, der er lagt på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="8d003-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="8d003-118">Udvid sektionen Lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="8d003-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="8d003-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8d003-119">Click Add.</span></span>
13. <span data-ttu-id="8d003-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8d003-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="8d003-121">Indtast '51' på lagerstedslisten.</span><span class="sxs-lookup"><span data-stu-id="8d003-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="8d003-122">Indtast eller vælg '001' i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="8d003-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="8d003-123">Udvid afsnittet Produkter.</span><span class="sxs-lookup"><span data-stu-id="8d003-123">Expand the Products section.</span></span>
17. <span data-ttu-id="8d003-124">Vælg 'Valgt' i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="8d003-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="8d003-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8d003-125">Click Add.</span></span>
19. <span data-ttu-id="8d003-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8d003-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="8d003-127">Indtast eller vælg 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="8d003-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="8d003-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8d003-128">Click Save.</span></span>


