---
title: Oprette og anskaffe aktiver fra Kreditor
description: Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "316412"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="a87f8-103">Oprette og anskaffe aktiver fra Kreditor</span><span class="sxs-lookup"><span data-stu-id="a87f8-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a87f8-104">Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen.</span><span class="sxs-lookup"><span data-stu-id="a87f8-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="a87f8-105">Den bruger bogholder- og kreditorassistenter og demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a87f8-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="a87f8-106">Konfigurere parametre for anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="a87f8-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="a87f8-107">Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre.</span><span class="sxs-lookup"><span data-stu-id="a87f8-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="a87f8-108">Udvis eller skjul sektionen Indkøbsordrer .</span><span class="sxs-lookup"><span data-stu-id="a87f8-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="a87f8-109">Markér afkrydsningsfeltet Tillad aktivanskaffelse fra Indkøb.</span><span class="sxs-lookup"><span data-stu-id="a87f8-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="a87f8-110">Markér afkrydsningsfeltet Opret aktiv under bogføring af produktkvittering eller faktura</span><span class="sxs-lookup"><span data-stu-id="a87f8-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="a87f8-111">Opret en ny kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="a87f8-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="a87f8-112">Gå til Kreditor > Arbejdsområder > Kreditorfakturapostering.</span><span class="sxs-lookup"><span data-stu-id="a87f8-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="a87f8-113">Klik på Ny kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="a87f8-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="a87f8-114">Klik på rullelisten i feltet Fakturakonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f8-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a87f8-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a87f8-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a87f8-116">Skriv en værdi i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="a87f8-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="a87f8-117">Angiv en dato i feltet Bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="a87f8-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="a87f8-118">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="a87f8-118">Click Add line.</span></span>
8. <span data-ttu-id="a87f8-119">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f8-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a87f8-120">Ikke-lagerførte varer eller indkøbskategorier kan bruges til anskaffelse af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="a87f8-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="a87f8-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a87f8-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a87f8-122">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="a87f8-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a87f8-123">En fakturalinje opretter kun ét anlægsaktiv uanset antal.</span><span class="sxs-lookup"><span data-stu-id="a87f8-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="a87f8-124">Feltværdien Fakturaantal overføres til anlægsaktivantallet.</span><span class="sxs-lookup"><span data-stu-id="a87f8-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="a87f8-125">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="a87f8-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="a87f8-126">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="a87f8-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="a87f8-127">Klik på fanen Anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="a87f8-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="a87f8-128">Markér afkrydsningsfeltet Opret et nyt anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="a87f8-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="a87f8-129">Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f8-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="a87f8-130">Vælg på listen den anlægsaktivgruppe, der skal bruges ved oprettelse af det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="a87f8-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="a87f8-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a87f8-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="a87f8-132">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="a87f8-132">Click Post.</span></span>
    * <span data-ttu-id="a87f8-133">Anlægsaktivet oprettes og anskaffes, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="a87f8-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

