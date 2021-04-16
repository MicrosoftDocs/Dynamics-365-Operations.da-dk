---
title: Afledte bøger
description: Denne artikel indeholder en oversigt over funktionerne til afledte bøger.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c53d72220890803d561ebe057acfdf0974bd421b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826900"
---
# <a name="derived-books"></a><span data-ttu-id="f8942-103">Afledte bøger</span><span class="sxs-lookup"><span data-stu-id="f8942-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8942-104">Denne artikel indeholder en oversigt over funktionerne til afledte bøger.</span><span class="sxs-lookup"><span data-stu-id="f8942-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="f8942-105">Formålet med afledte bøger er at forenkle bogføringen af transaktioner for aktivbog, der er planlagt til at finde sted med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="f8942-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="f8942-106">Du skal vælge en bog som den primære bog.</span><span class="sxs-lookup"><span data-stu-id="f8942-106">You choose one book as the primary book.</span></span> <span data-ttu-id="f8942-107">Dette er normalt den bog, der bruges til regnskabsmæssige afskrivninger.</span><span class="sxs-lookup"><span data-stu-id="f8942-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="f8942-108">Du kan derefter knytte den til andre bøger, der er konfigureret til at bogføre transaktioner i de samme som den primære bog.</span><span class="sxs-lookup"><span data-stu-id="f8942-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="f8942-109">Bøger til skattemæssig afskrivning angives ofte som afledte bøger.</span><span class="sxs-lookup"><span data-stu-id="f8942-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="f8942-110">De mest almindelige transaktioner, der angives, så der bogføres til afledte bøger, er anskaffelser, anskaffelsesreguleringer og afhændelser.</span><span class="sxs-lookup"><span data-stu-id="f8942-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="f8942-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f8942-111">Example</span></span>

<span data-ttu-id="f8942-112">Bog B og bog C er konfigureret som afledte bøger for bog A til posteringstypen Anskaffelse.</span><span class="sxs-lookup"><span data-stu-id="f8942-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="f8942-113">I bog A skal du angive en anskaffelsespostering for aktiv 123 på 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="f8942-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="f8942-114">Ved posteringen oprettes der en anskaffelsespostering, som bogføres i aktiv 123 for bog B og i aktiv 123 for bog C med en værdi på 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="f8942-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="f8942-115">Når du forbereder transaktionerne til den primære bog for bogføring i anlægsaktivkladden, kan du også se og redigere transaktionerne til de afledte afskrivningsmodeller.</span><span class="sxs-lookup"><span data-stu-id="f8942-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="f8942-116">Hvis du forbereder transaktionerne til den primære bog i en anden kladde, kan du ikke få vist posteringerne for den afledte værdi.</span><span class="sxs-lookup"><span data-stu-id="f8942-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="f8942-117">De bogføres i stedet på de relevante konti og posteringslag, når du bogfører posteringer til den primære bog.</span><span class="sxs-lookup"><span data-stu-id="f8942-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="f8942-118">Bøger, der er konfigureret, så posteringer bogføres med andre intervaller end dem, der er angivet for den primære bog, skal tilknyttes anlægsaktivet som separate bøger og ikke som afledte bøger.</span><span class="sxs-lookup"><span data-stu-id="f8942-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="f8942-119">Du kan finde flere oplysninger under [Bogfør med afledte bøger](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="f8942-119">For more information, see [Post with derived books](post-derived-value-models.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]