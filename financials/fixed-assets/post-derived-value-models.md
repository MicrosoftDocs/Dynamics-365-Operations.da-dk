---
title: "Bogfør med afledte bøger"
description: "I denne artikel beskrives det, hvordan afledte bøger bruges."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: aaacf596f2ea1107a53647d779e9d2b6c37ab530
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="post-with-derived-books"></a><span data-ttu-id="69718-103">Bogfør med afledte bøger</span><span class="sxs-lookup"><span data-stu-id="69718-103">Post with derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="69718-104">I denne artikel beskrives det, hvordan afledte bøger bruges.</span><span class="sxs-lookup"><span data-stu-id="69718-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="69718-105">Når du bogfører posteringerne for en bog, der indeholder afledte bøger, bogføres posteringerne for den afledte bog automatisk i kladder, indkøbsordrer eller fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="69718-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="69718-106">Men, hvis du forbereder posteringerne for den primære bog i anlægsaktivkladden , kan du se og redigere beløbene for de afledte posteringer, før de bogføres.</span><span class="sxs-lookup"><span data-stu-id="69718-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="69718-107">Visse konti, f.eks. moms og debitor- eller kreditorkonti, opdateres kun én gang af posteringer i den primære bog.</span><span class="sxs-lookup"><span data-stu-id="69718-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="69718-108">De afledte bogposteringer bogføres til de konti, der er defineret for den afledte bog på siden med posteringsprofiler for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="69718-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="69718-109">Anskaffelse bruges ofte som posteringstype for de afledte bøger.</span><span class="sxs-lookup"><span data-stu-id="69718-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="69718-110">Du kan bruge dette, når bogen og den afledte bog skal anvendes på anlægsaktivet fra anlægsaktivets anskaffelsestidspunkt.</span><span class="sxs-lookup"><span data-stu-id="69718-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="69718-111">Der kan også anvendes andre værdier for posteringstypen.</span><span class="sxs-lookup"><span data-stu-id="69718-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="69718-112">Hvis den primære bog og de afledte bøger f.eks. har de samme intervaller mht. salg og kassation, er alle posteringstyperne for anlægsaktiver tilgængelige ved oprettelse af en afledt bog.</span><span class="sxs-lookup"><span data-stu-id="69718-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="69718-113">De afskrivninger, der bogføres i den afledte bog, vil have samme beløb som dem, der blev bogført for den primære bog.</span><span class="sxs-lookup"><span data-stu-id="69718-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="69718-114">Hvis afskrivningsmetoderne er forskellige fra bog til bog, bør du ikke generere afskrivningsposteringer ved hjælp af den afledte proces.</span><span class="sxs-lookup"><span data-stu-id="69718-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="69718-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="69718-115">Example</span></span> 
<span data-ttu-id="69718-116">I følgende oplysninger kan du finde en beskrivelse af, hvordan du definerer anskaffelsesposteringer med brug af funktionerne til den afledte bog.</span><span class="sxs-lookup"><span data-stu-id="69718-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="69718-117">Opret bøgerne på siden Bøger.</span><span class="sxs-lookup"><span data-stu-id="69718-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="69718-118">Regnskabsbogen: VM 1, aktuelt posteringslag</span><span class="sxs-lookup"><span data-stu-id="69718-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="69718-119">Den skattemæssige bog: VM 2, skatteposteringslag</span><span class="sxs-lookup"><span data-stu-id="69718-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="69718-120">Klik på fanen Afledte bøger for VM 1.</span><span class="sxs-lookup"><span data-stu-id="69718-120">On VM 1, click the Derived books tab.</span></span> <span data-ttu-id="69718-121">Vælg VM 2 i feltet Bog og Anskaffelse i feltet Posteringstype.</span><span class="sxs-lookup"><span data-stu-id="69718-121">Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="69718-122">Bøgerne kan derefter tilknyttes bestemte anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="69718-122">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="69718-123">Når en anskaffelse bogføres som et anlægsaktiv med bog VM 1, bogføres anskaffelsen ikke kun for VM 1, men også for den afledte afskrivningsmodel VM 2.</span><span class="sxs-lookup"><span data-stu-id="69718-123">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="69718-124">Status for begge anlægsaktivbøger opdateres til Åben.</span><span class="sxs-lookup"><span data-stu-id="69718-124">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="69718-125">Hvis du ikke bruger afledte afledte bøger, skal du bogføre anskaffelsen af anlægsaktivet for både bogen VM 1 og bogen VM 2.</span><span class="sxs-lookup"><span data-stu-id="69718-125">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="69718-126">Du kan finde flere oplysninger under [Afledte bøger](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="69718-126">For more information, see [Derived books](derived-books.md)</span></span>




