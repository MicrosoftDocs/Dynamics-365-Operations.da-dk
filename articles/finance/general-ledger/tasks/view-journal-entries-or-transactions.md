---
title: Se kladdeposter eller -posteringer
description: Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbeb5af9b14c409347f7f0ac2aeb045929619a3d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817023"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="771c5-103">Se kladdeposter eller -posteringer</span><span class="sxs-lookup"><span data-stu-id="771c5-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="771c5-104">Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner.</span><span class="sxs-lookup"><span data-stu-id="771c5-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="771c5-105">Gå til **Navigationsrude > Moduler > Finans > Forespørgsler og rapporter > Bilagstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="771c5-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="771c5-106">Vælg det felt, som du vil definere filtreringskriterier for.</span><span class="sxs-lookup"><span data-stu-id="771c5-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="771c5-107">Angiv dine filtreringskriterier for det markerede felt.</span><span class="sxs-lookup"><span data-stu-id="771c5-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="771c5-108">Du kan filtrere på en enkelt værdi eller et område.</span><span class="sxs-lookup"><span data-stu-id="771c5-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="771c5-109">Kontrollér, at den korrekte syntaks bruges, når du definerer et område.</span><span class="sxs-lookup"><span data-stu-id="771c5-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="771c5-110">Værdierne skal adskilles af en dobbelt punktum (..).</span><span class="sxs-lookup"><span data-stu-id="771c5-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="771c5-111">Klik på fanen **Joinforbindelser** for at tilføje flere tabeller, som skal filtreres.</span><span class="sxs-lookup"><span data-stu-id="771c5-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="771c5-112">Vælg **Tabeller/Finanskladdepostering** i træet.</span><span class="sxs-lookup"><span data-stu-id="771c5-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="771c5-113">Klik på **Tilføj tabeljoin**.</span><span class="sxs-lookup"><span data-stu-id="771c5-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="771c5-114">Klik på **Annuller**, hvis du beslutter, at du ikke vil tilføje en ekstra tabel.</span><span class="sxs-lookup"><span data-stu-id="771c5-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="771c5-115">Klik på fanen **Område**.</span><span class="sxs-lookup"><span data-stu-id="771c5-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="771c5-116">Kør forespørgslen ved at klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="771c5-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="771c5-117">Klik på **Posteringsgrundlag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="771c5-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="771c5-118">Forskellige knapper om gitteret kan bruges til at undersøge flere oplysninger om den valgte post i bilaget.</span><span class="sxs-lookup"><span data-stu-id="771c5-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="771c5-119">Nogle af knapperne er muligvis ikke tilgængelige, afhængigt af posteringstypen og posteringens egenskaber.</span><span class="sxs-lookup"><span data-stu-id="771c5-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="771c5-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="771c5-120">Close the page.</span></span>
12. <span data-ttu-id="771c5-121">Klik på **Originaldokument** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="771c5-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="771c5-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="771c5-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]