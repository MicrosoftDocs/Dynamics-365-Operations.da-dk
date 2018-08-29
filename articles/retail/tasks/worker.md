--- 
title: Konfigurere detailarbejdere
description: "Denne fremgangsmåde viser, hvordan du konfigurerer en detailarbejder som en sælger, der er berettiget til provision på salg i POS."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: f583c421c2f6dfd019d9586cb7d14f3298127d94
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-workers"></a><span data-ttu-id="9126b-103">Konfigurere detailarbejdere</span><span class="sxs-lookup"><span data-stu-id="9126b-103">Configure retail workers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9126b-104">Denne fremgangsmåde viser, hvordan du konfigurerer en detailarbejder som en sælger, der er berettiget til provision på salg i POS.</span><span class="sxs-lookup"><span data-stu-id="9126b-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="9126b-105">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="9126b-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="9126b-106">Opret en provisionssalgsgruppe for arbejderen</span><span class="sxs-lookup"><span data-stu-id="9126b-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="9126b-107">Gå til Salg og marketing > Provisioner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9126b-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="9126b-108">Arbejdere kan tildeles til en eller flere salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9126b-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="9126b-109">I POS kan du vælge en salgsgruppe, der indeholder arbejdere fra butikkens adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="9126b-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="9126b-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9126b-110">Click New.</span></span>
3. <span data-ttu-id="9126b-111">Skriv en værdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9126b-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="9126b-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9126b-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9126b-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9126b-113">Click Save.</span></span>
6. <span data-ttu-id="9126b-114">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9126b-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="9126b-115">Klik på Sælger.</span><span class="sxs-lookup"><span data-stu-id="9126b-115">Click Sales rep.</span></span>
    * <span data-ttu-id="9126b-116">En salgsgruppe kan indeholde mere end én medarbejder.</span><span class="sxs-lookup"><span data-stu-id="9126b-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="9126b-117">Provisioner kan opdeles mellem arbejdere baseret på, hvordan du definerer kommissionen.</span><span class="sxs-lookup"><span data-stu-id="9126b-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="9126b-118">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9126b-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="9126b-119">Angiv et tal i feltet Provisionsandel.</span><span class="sxs-lookup"><span data-stu-id="9126b-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="9126b-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9126b-120">Click Save.</span></span>
11. <span data-ttu-id="9126b-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9126b-121">Close the page.</span></span>
12. <span data-ttu-id="9126b-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9126b-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="9126b-123">Tildel standardsalgsgruppen for arbejdere</span><span class="sxs-lookup"><span data-stu-id="9126b-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="9126b-124">Gå til Detail og handel > Medarbejdere > Alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="9126b-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="9126b-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9126b-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9126b-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9126b-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9126b-127">Klik på fanen Detail.</span><span class="sxs-lookup"><span data-stu-id="9126b-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="9126b-128">En arbejder kan tildeles til en standardsalgsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9126b-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="9126b-129">Standardsalgsgruppen føjes automatisk til salgslinjerne i POS, hvis indstillingen er aktiveret i funktionalitetsprofilen for butikken.</span><span class="sxs-lookup"><span data-stu-id="9126b-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="9126b-130">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="9126b-130">Click Edit.</span></span>
6. <span data-ttu-id="9126b-131">Indtast eller vælg en værdi i feltet Standardgruppe.</span><span class="sxs-lookup"><span data-stu-id="9126b-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="9126b-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9126b-132">Click Save.</span></span>


