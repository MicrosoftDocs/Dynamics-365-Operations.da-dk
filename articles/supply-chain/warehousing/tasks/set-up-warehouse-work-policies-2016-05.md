---
title: Konfigurere politikker for lagerstedsarbejde (program, maj 2016)
description: Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62fbf2f44216c300af5e092f5dbd05ef2239321b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216775"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="77855-103">Konfigurere politikker for lagerstedsarbejde (program, maj 2016)</span><span class="sxs-lookup"><span data-stu-id="77855-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77855-104">Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="77855-104">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="77855-105">Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og placering af færdigvarer på lager for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="77855-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="77855-106">USMF-demodatafirmaet blev brugt til at oprette denne registrering.</span><span class="sxs-lookup"><span data-stu-id="77855-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="77855-107">Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="77855-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="77855-108">Gå til Lagerstyring > Konfiguration > Arbejde > Arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="77855-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="77855-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="77855-109">Click New.</span></span>
3. <span data-ttu-id="77855-110">Skriv 'Ikke læg-på-lager-arbejde' i navnefeltet Arbejdspolitik.</span><span class="sxs-lookup"><span data-stu-id="77855-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="77855-111">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="77855-111">Click Save.</span></span>
5. <span data-ttu-id="77855-112">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="77855-112">Click Add.</span></span>
6. <span data-ttu-id="77855-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="77855-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="77855-114">Vælg 'Færdige varer lægges på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="77855-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="77855-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="77855-115">Click Add.</span></span>
9. <span data-ttu-id="77855-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="77855-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="77855-117">Vælg 'Samprodukter eller biprodukter, der er lagt på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="77855-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="77855-118">Udvid sektionen Lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="77855-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="77855-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="77855-119">Click Add.</span></span>
13. <span data-ttu-id="77855-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="77855-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="77855-121">Indtast '51' på lagerstedslisten.</span><span class="sxs-lookup"><span data-stu-id="77855-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="77855-122">Indtast eller vælg '001' i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="77855-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="77855-123">Udvid afsnittet Produkter.</span><span class="sxs-lookup"><span data-stu-id="77855-123">Expand the Products section.</span></span>
17. <span data-ttu-id="77855-124">Vælg 'Valgt' i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="77855-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="77855-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="77855-125">Click Add.</span></span>
19. <span data-ttu-id="77855-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="77855-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="77855-127">Indtast eller vælg 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="77855-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="77855-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="77855-128">Click Save.</span></span>

