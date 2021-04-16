---
title: Indkøbsordrekoder i den offentlige sektor
description: Dette emne indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConfirmingPOCodes, PurchTableListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 27291
ms.assetid: 65032886-4dc6-4411-98c8-8969287fd7df
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07ac4ebfe73fd925b6f1d82dc83dcd05f8fe60e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814890"
---
# <a name="purchase-order-codes-in-the-public-sector"></a><span data-ttu-id="425d1-103">Indkøbsordrekoder i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="425d1-103">Purchase order codes in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="425d1-104">Denne artikel indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="425d1-104">This article provides information about the codes and special messages that can be used with confirming purchase orders.</span></span> <span data-ttu-id="425d1-105">En bekræftende indkøbsordre omgår den typiske indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="425d1-105">A confirming purchase order bypasses the typical purchasing process.</span></span>

<span data-ttu-id="425d1-106">I denne artikel beskrives funktionerne i de indkøbsordrekoder, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="425d1-106">This article describes the purchase order codes functionality available for the public sector.</span></span> <span data-ttu-id="425d1-107">Du skal først afgøre, hvad din koder og meddelelser skal være.</span><span class="sxs-lookup"><span data-stu-id="425d1-107">You must first determine what your codes and messages will be.</span></span> <span data-ttu-id="425d1-108">Du kan bruge siden **Bekræfter koder til indkøbsordrer** for at oprette koder og specielle meddelelser, der kan bruges til bekræftelse af indkøbsordrer (POs).</span><span class="sxs-lookup"><span data-stu-id="425d1-108">You can use the **Confirming PO codes** page to create codes and special messages that can be used with confirming purchase orders (POs).</span></span> <span data-ttu-id="425d1-109">En bekræftende indkøbsordre omgår den typiske indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="425d1-109">A confirming purchase order bypasses the typical purchasing process.</span></span> <span data-ttu-id="425d1-110">For eksempel skal du tillade en ikke-planlagt ordre ved hjælp af et PO-nummer på tidspunktet for et køb i stedet for ved hjælp af et dokument, der er leveret, før varen er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="425d1-110">For example, you must authorize an unplanned order by using a PO number at the time of a purchase, instead of by using a document that is provided before the item is required.</span></span> 

<span data-ttu-id="425d1-111">Når du har oprettet koderne, kan du tildele koderne til indkøbsordrer på siden **Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="425d1-111">After you set up the codes, you can assign the codes to purchase orders on the **All purchase orders** page.</span></span> 

<span data-ttu-id="425d1-112">Hvis du tildeler en bekræftende PO-kode til en indkøbsordre på oversigtspanelet **Ikke-planlagt køb** (for eksempel, når du opretter en ny indkøbsordre), bliver den meddelelse, der er knyttet til den bekræftende PO-kode, udskrevet øverst på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="425d1-112">If you assign a confirming PO code to a purchase order on the **Unplanned purchases** FastTab (for example, when you create a new purchase order), the message that is associated with the confirming PO code will be printed at the top of the purchase order.</span></span>

## <a name="tips"></a><span data-ttu-id="425d1-113">Tip!</span><span class="sxs-lookup"><span data-stu-id="425d1-113">Tips</span></span>
-   <span data-ttu-id="425d1-114">Hvis du ændrer en bekræftende PO-kode, der allerede er tildelt til en indkøbsordre, erstatter den nye kode den gamle.</span><span class="sxs-lookup"><span data-stu-id="425d1-114">If you change a confirming PO code that was already assigned to a purchase order, the new code will replace the old code.</span></span> <span data-ttu-id="425d1-115">Denne ændring påvirker både nye indkøbsordrer og produktionsordrer, der er bogført.</span><span class="sxs-lookup"><span data-stu-id="425d1-115">This change affects both new purchase orders and purchase orders that have been posted.</span></span> <span data-ttu-id="425d1-116">En indkøbsordre havde f.eks. en bekræftende PO-kode for **Bekræfter**, da den blev bogført, men den pågældende kode er senere ændret til **Nødstilfælde**.</span><span class="sxs-lookup"><span data-stu-id="425d1-116">For example, a purchase order had a confirming PO code of **Confirming** when it was posted, but that code is later changed to **Emergency**.</span></span> <span data-ttu-id="425d1-117">I dette tilfælde vil hver indkøbsordre, der havde koden **Bekræfter**, nu have koden **Nødstilfælde** i stedet.</span><span class="sxs-lookup"><span data-stu-id="425d1-117">In this case, every purchase order that had the **Confirming** code will now have the **Emergency** code instead.</span></span>
-   <span data-ttu-id="425d1-118">Du kan oprette meddelelser på forskellige sprog.</span><span class="sxs-lookup"><span data-stu-id="425d1-118">You can create messages in different languages.</span></span> <span data-ttu-id="425d1-119">Denne funktion kan være en hjælp, når du køber fra handlende i andre lande/områder.</span><span class="sxs-lookup"><span data-stu-id="425d1-119">This feature is helpful when you are purchasing from merchants in other countries or regions.</span></span> <span data-ttu-id="425d1-120">Organisationen har f.eks. hjemsted i et engelsktalende land eller område, og du vil oprette en spansk meddelelse for bekræftende indkøbsordrer, som har en bekræftende PO-kode **Bekræfter**.</span><span class="sxs-lookup"><span data-stu-id="425d1-120">For example, your organization is located in an English-speaking country or region, and you want to create a Spanish message for confirming purchase orders that have a confirming PO code **Confirming**.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]