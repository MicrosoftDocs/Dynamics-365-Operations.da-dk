---
title: Behandle rabatter for betaling
description: Denne fremgangsmåde viser, hvordan godkendte og behandlede kunderabatter konverteres til kreditnotaer.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980688"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="2b4c3-103">Behandle rabatter for betaling</span><span class="sxs-lookup"><span data-stu-id="2b4c3-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b4c3-104">Denne fremgangsmåde viser, hvordan godkendte og behandlede kunderabatter konverteres til kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="2b4c3-105">Du kan bruge denne guide i USMF-demofirmaet.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="2b4c3-106">Forudsætningen for denne guide er at have en eller flere rabatkrav med status "Markér".</span><span class="sxs-lookup"><span data-stu-id="2b4c3-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="2b4c3-107">Hvis du bruger USMF, skal du køre guiden "Generer og behandl kunderabatter", før du starter guiden.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="2b4c3-108">Konverter rabatkrav til kreditnota</span><span class="sxs-lookup"><span data-stu-id="2b4c3-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="2b4c3-109">Gå til Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-109">Go to All customers.</span></span>
2. <span data-ttu-id="2b4c3-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2b4c3-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2b4c3-112">Klik på Indsaml i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="2b4c3-113">Klik på Udlign transaktioner.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="2b4c3-114">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-114">Click Functions.</span></span>
7. <span data-ttu-id="2b4c3-115">Klik på Rabatprogram.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-115">Click Rebate program.</span></span>
    * <span data-ttu-id="2b4c3-116">Siden Rabatter angiver de rabatkrav, du har behandlet i kunderabatpanelet, og som er i status Markér.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="2b4c3-117">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-117">Click Edit.</span></span>
    * <span data-ttu-id="2b4c3-118">Sæt hak i feltet Markér for krav, der skal indgå i kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="2b4c3-119">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-119">Click Functions.</span></span>
10. <span data-ttu-id="2b4c3-120">Klik på Opret kreditnota.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-120">Click Create credit note.</span></span>
    * <span data-ttu-id="2b4c3-121">Der vises en meddelelse for at informere dig om, at der er bogført en kladde (dette er debitorforbrugskladden, som er angivet på siden Debitorparametre).</span><span class="sxs-lookup"><span data-stu-id="2b4c3-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="2b4c3-122">Dette medfører, at det reelle skyldige beløb (kredit) skal flyttes til debitorsaldoen.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="2b4c3-123">Det betyder, at kundens konto er blevet krediteret, og periodiseringskontoen for rabatten er krediteret.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="2b4c3-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-124">Close the page.</span></span>
12. <span data-ttu-id="2b4c3-125">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-125">Click Cancel.</span></span>
    * <span data-ttu-id="2b4c3-126">Dette opdaterer siden, så du kan se opdateringerne.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="2b4c3-127">Klik på Indsaml i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="2b4c3-128">Klik på Udlign transaktioner.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="2b4c3-129">Bemærk, at en transaktion for negative beløb, der repræsenterer det samlede rabatbeløb uden fakturareference, er blevet tilføjet debitorbalancen.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="2b4c3-130">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-130">Click Cancel.</span></span>

