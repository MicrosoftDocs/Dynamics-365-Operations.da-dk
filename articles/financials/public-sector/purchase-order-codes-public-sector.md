---
title: Indkøbsordrekoder i den offentlige sektor
description: Denne artikel indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer. En bekræftende indkøbsordre omgår den typiske indkøbsproces.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConfirmingPOCodes, PurchTableListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27291
ms.assetid: 65032886-4dc6-4411-98c8-8969287fd7df
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5163f41c5bfa1b88d949c7539bd5712dd7356fd6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550222"
---
# <a name="purchase-order-codes-in-the-public-sector"></a><span data-ttu-id="cd476-104">Indkøbsordrekoder i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="cd476-104">Purchase order codes in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd476-105">Denne artikel indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="cd476-105">This article provides information about the codes and special messages that can be used with confirming purchase orders.</span></span> <span data-ttu-id="cd476-106">En bekræftende indkøbsordre omgår den typiske indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="cd476-106">A confirming purchase order bypasses the typical purchasing process.</span></span>

<span data-ttu-id="cd476-107">I denne artikel beskrives funktionerne i de indkøbsordrekoder, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="cd476-107">This article describes the purchase order codes functionality available for the public sector.</span></span> <span data-ttu-id="cd476-108">Du skal først afgøre, hvad din koder og meddelelser skal være.</span><span class="sxs-lookup"><span data-stu-id="cd476-108">You must first determine what your codes and messages will be.</span></span> <span data-ttu-id="cd476-109">Du kan bruge siden **Bekræfter koder til indkøbsordrer** for at oprette koder og specielle meddelelser, der kan bruges til bekræftelse af indkøbsordrer (POs).</span><span class="sxs-lookup"><span data-stu-id="cd476-109">You can use the **Confirming PO codes** page to create codes and special messages that can be used with confirming purchase orders (POs).</span></span> <span data-ttu-id="cd476-110">En bekræftende indkøbsordre omgår den typiske indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="cd476-110">A confirming purchase order bypasses the typical purchasing process.</span></span> <span data-ttu-id="cd476-111">For eksempel skal du tillade en ikke-planlagt ordre ved hjælp af et PO-nummer på tidspunktet for et køb i stedet for ved hjælp af et dokument, der er leveret, før varen er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="cd476-111">For example, you must authorize an unplanned order by using a PO number at the time of a purchase, instead of by using a document that is provided before the item is required.</span></span> 

<span data-ttu-id="cd476-112">Når du har oprettet koderne, kan du tildele koderne til indkøbsordrer på siden **Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cd476-112">After you set up the codes, you can assign the codes to purchase orders on the **All purchase orders** page.</span></span> 

<span data-ttu-id="cd476-113">Hvis du tildeler en bekræftende PO-kode til en indkøbsordre på oversigtspanelet **Ikke-planlagt køb** (for eksempel, når du opretter en ny indkøbsordre), bliver den meddelelse, der er knyttet til den bekræftende PO-kode, udskrevet øverst på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="cd476-113">If you assign a confirming PO code to a purchase order on the **Unplanned purchases** FastTab (for example, when you create a new purchase order), the message that is associated with the confirming PO code will be printed at the top of the purchase order.</span></span>

## <a name="tips"></a><span data-ttu-id="cd476-114">Tip!</span><span class="sxs-lookup"><span data-stu-id="cd476-114">Tips</span></span>
-   <span data-ttu-id="cd476-115">Hvis du ændrer en bekræftende PO-kode, der allerede er tildelt til en indkøbsordre, erstatter den nye kode den gamle.</span><span class="sxs-lookup"><span data-stu-id="cd476-115">If you change a confirming PO code that was already assigned to a purchase order, the new code will replace the old code.</span></span> <span data-ttu-id="cd476-116">Denne ændring påvirker både nye indkøbsordrer og produktionsordrer, der er bogført.</span><span class="sxs-lookup"><span data-stu-id="cd476-116">This change affects both new purchase orders and purchase orders that have been posted.</span></span> <span data-ttu-id="cd476-117">En indkøbsordre havde f.eks. en bekræftende PO-kode for **Bekræfter**, da den blev bogført, men den pågældende kode er senere ændret til **Nødstilfælde**.</span><span class="sxs-lookup"><span data-stu-id="cd476-117">For example, a purchase order had a confirming PO code of **Confirming** when it was posted, but that code is later changed to **Emergency**.</span></span> <span data-ttu-id="cd476-118">I dette tilfælde vil hver indkøbsordre, der havde koden **Bekræfter**, nu have koden **Nødstilfælde** i stedet.</span><span class="sxs-lookup"><span data-stu-id="cd476-118">In this case, every purchase order that had the **Confirming** code will now have the **Emergency** code instead.</span></span>
-   <span data-ttu-id="cd476-119">Du kan oprette meddelelser på forskellige sprog.</span><span class="sxs-lookup"><span data-stu-id="cd476-119">You can create messages in different languages.</span></span> <span data-ttu-id="cd476-120">Denne funktion kan være en hjælp, når du køber fra handlende i andre lande/områder.</span><span class="sxs-lookup"><span data-stu-id="cd476-120">This feature is helpful when you are purchasing from merchants in other countries or regions.</span></span> <span data-ttu-id="cd476-121">Organisationen har f.eks. hjemsted i et engelsktalende land eller område, og du vil oprette en spansk meddelelse for bekræftende indkøbsordrer, som har en bekræftende PO-kode **Bekræfter**.</span><span class="sxs-lookup"><span data-stu-id="cd476-121">For example, your organization is located in an English-speaking country or region, and you want to create a Spanish message for confirming purchase orders that have a confirming PO code **Confirming**.</span></span>





