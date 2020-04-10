---
title: " Konfigurere en arbejder"
description: Denne fremgangsmåde viser, hvordan du konfigurerer en arbejder som en sælger, der er berettiget til provision på salg i POS.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd437f549ffc1f8879ce3814ace1193040b280e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140672"
---
# <a name="configure-a-worker"></a><span data-ttu-id="d67b8-103"> Konfigurere en arbejder</span><span class="sxs-lookup"><span data-stu-id="d67b8-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d67b8-104">Denne fremgangsmåde viser, hvordan du konfigurerer en arbejder som en sælger, der er berettiget til provision på salg i POS.</span><span class="sxs-lookup"><span data-stu-id="d67b8-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="d67b8-105">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d67b8-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="d67b8-106">Opret en provisionssalgsgruppe for arbejderen</span><span class="sxs-lookup"><span data-stu-id="d67b8-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="d67b8-107">Gå til Salg og marketing > Provisioner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d67b8-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="d67b8-108">Arbejdere kan tildeles til en eller flere salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d67b8-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="d67b8-109">I POS kan du vælge en salgsgruppe, der indeholder arbejdere fra butikkens adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="d67b8-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="d67b8-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d67b8-110">Click New.</span></span>
3. <span data-ttu-id="d67b8-111">Skriv en værdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d67b8-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="d67b8-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d67b8-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d67b8-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d67b8-113">Click Save.</span></span>
6. <span data-ttu-id="d67b8-114">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d67b8-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="d67b8-115">Klik på Sælger.</span><span class="sxs-lookup"><span data-stu-id="d67b8-115">Click Sales rep.</span></span>
    * <span data-ttu-id="d67b8-116">En salgsgruppe kan indeholde mere end én medarbejder.</span><span class="sxs-lookup"><span data-stu-id="d67b8-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="d67b8-117">Provisioner kan opdeles mellem arbejdere baseret på, hvordan du definerer kommissionen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="d67b8-118">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d67b8-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="d67b8-119">Angiv et tal i feltet Provisionsandel.</span><span class="sxs-lookup"><span data-stu-id="d67b8-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="d67b8-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d67b8-120">Click Save.</span></span>
11. <span data-ttu-id="d67b8-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d67b8-121">Close the page.</span></span>
12. <span data-ttu-id="d67b8-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d67b8-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="d67b8-123">Tildel standardsalgsgruppen for arbejdere</span><span class="sxs-lookup"><span data-stu-id="d67b8-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="d67b8-124">Gå til Retail og Commerce > Medarbejdere > Arbejdere.</span><span class="sxs-lookup"><span data-stu-id="d67b8-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="d67b8-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d67b8-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d67b8-127">Klik på fanen Commerce.</span><span class="sxs-lookup"><span data-stu-id="d67b8-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="d67b8-128">En arbejder kan tildeles til en standardsalgsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d67b8-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="d67b8-129">Standardsalgsgruppen føjes automatisk til salgslinjerne i POS, hvis indstillingen er aktiveret i funktionalitetsprofilen for butikken.</span><span class="sxs-lookup"><span data-stu-id="d67b8-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="d67b8-130">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d67b8-130">Click Edit.</span></span>
6. <span data-ttu-id="d67b8-131">Indtast eller vælg en værdi i feltet Standardgruppe.</span><span class="sxs-lookup"><span data-stu-id="d67b8-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="d67b8-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d67b8-132">Click Save.</span></span>

