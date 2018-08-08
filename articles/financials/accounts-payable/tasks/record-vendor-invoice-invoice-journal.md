--- 
title: Registrere en kreditorfaktura i fakturakladden
description: "Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5711bd71f3da13c05a8bd6dc6756e648c302b5ef
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="2be52-103">Registrere en kreditorfaktura i fakturakladden</span><span class="sxs-lookup"><span data-stu-id="2be52-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2be52-104">Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="2be52-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="2be52-105">Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.</span><span class="sxs-lookup"><span data-stu-id="2be52-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="2be52-106">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="2be52-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="2be52-107">Gå til Kreditor > Arbejdsområder > Kreditorfakturapostering.</span><span class="sxs-lookup"><span data-stu-id="2be52-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="2be52-108">Klik på Ny fakturakladde.</span><span class="sxs-lookup"><span data-stu-id="2be52-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="2be52-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2be52-109">Click New.</span></span>
4. <span data-ttu-id="2be52-110">Indtast kladdenavnet eller klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be52-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="2be52-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2be52-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2be52-112">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="2be52-112">Click Lines.</span></span>
    * <span data-ttu-id="2be52-113">Indtast den bogføringsdato, der opdaterer Finans, i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="2be52-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="2be52-114">Angiv kreditorkontoen i feltet Konto.</span><span class="sxs-lookup"><span data-stu-id="2be52-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="2be52-115">Angiv fakturanummeret i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="2be52-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="2be52-116">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2be52-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="2be52-117">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="2be52-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="2be52-118">Indtast kontonummeret, eller klik på rullelisten i feltet Modkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be52-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="2be52-119">Momsgruppen hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="2be52-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="2be52-120">Varemomsgruppen hentes som standard fra den hovedkonto, der er angivet i feltet Modkonto.</span><span class="sxs-lookup"><span data-stu-id="2be52-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="2be52-121">Forfaldsdatoen beregnes på basis af betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="2be52-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="2be52-122">Kasserabatten hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="2be52-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="2be52-123">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="2be52-123">Click Post.</span></span>
13. <span data-ttu-id="2be52-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2be52-124">Close the page.</span></span>


