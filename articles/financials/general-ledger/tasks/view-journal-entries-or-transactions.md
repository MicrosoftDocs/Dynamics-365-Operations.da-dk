--- 
title: Se kladdeposter eller -posteringer
description: "Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 53e966a4caf6ee8907b05b5fd9c0978187d64f1d
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="b3c14-103">Se kladdeposter eller -posteringer</span><span class="sxs-lookup"><span data-stu-id="b3c14-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3c14-104">Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner.</span><span class="sxs-lookup"><span data-stu-id="b3c14-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="b3c14-105">Gå til Finans > Forespørgsler og rapporter > Bilagstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b3c14-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="b3c14-106">Vælg det felt, som du vil definere filtreringskriterier for.</span><span class="sxs-lookup"><span data-stu-id="b3c14-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="b3c14-107">Angiv dine filtreringskriterier for det markerede felt.</span><span class="sxs-lookup"><span data-stu-id="b3c14-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="b3c14-108">Du kan filtrere på en enkelt værdi eller et område.</span><span class="sxs-lookup"><span data-stu-id="b3c14-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="b3c14-109">Kontrollér, at den korrekte syntaks bruges, når du definerer et område.</span><span class="sxs-lookup"><span data-stu-id="b3c14-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="b3c14-110">Værdierne skal adskilles af en dobbelt punktum (..).</span><span class="sxs-lookup"><span data-stu-id="b3c14-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="b3c14-111">Klik på fanen Joinforbindelser for at tilføje flere tabeller, som skal filtreres.</span><span class="sxs-lookup"><span data-stu-id="b3c14-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="b3c14-112">Vælg 'Tabeller\Finanskladdepostering' i træet.</span><span class="sxs-lookup"><span data-stu-id="b3c14-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="b3c14-113">Klik på Tilføj tabeljoin.</span><span class="sxs-lookup"><span data-stu-id="b3c14-113">Click Add table join.</span></span>
7. <span data-ttu-id="b3c14-114">Klik på Annuller, hvis du beslutter, at du ikke vil tilføje en ekstra tabel.</span><span class="sxs-lookup"><span data-stu-id="b3c14-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="b3c14-115">Klik på fanen Område.</span><span class="sxs-lookup"><span data-stu-id="b3c14-115">Click the Range tab.</span></span>
9. <span data-ttu-id="b3c14-116">Kør forespørgslen ved at klikke på OK.</span><span class="sxs-lookup"><span data-stu-id="b3c14-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="b3c14-117">Klik på Transaktionsoprindelse.</span><span class="sxs-lookup"><span data-stu-id="b3c14-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="b3c14-118">Forskellige knapper om gitteret kan bruges til at undersøge flere oplysninger om den valgte post i bilaget.</span><span class="sxs-lookup"><span data-stu-id="b3c14-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="b3c14-119">Nogle af knapperne er muligvis ikke tilgængelige, afhængigt af posteringstypen og posteringens egenskaber.</span><span class="sxs-lookup"><span data-stu-id="b3c14-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="b3c14-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b3c14-120">Close the page.</span></span>
12. <span data-ttu-id="b3c14-121">Klik på Originaldokument.</span><span class="sxs-lookup"><span data-stu-id="b3c14-121">Click Original document.</span></span>
13. <span data-ttu-id="b3c14-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b3c14-122">Close the page.</span></span>


