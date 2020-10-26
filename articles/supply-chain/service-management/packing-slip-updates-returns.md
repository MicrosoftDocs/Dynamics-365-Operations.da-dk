---
title: Følgeseddelopdateringer til returneringer
description: Før returnerede varer kan modtages på lager, skal følgesedlen til den ordre, de tilhører, være opdateret.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7f5bf5adb603d7edb40960b70cb71e25a2f0456
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983861"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="79e4e-103">Følgeseddelopdateringer til returneringer</span><span class="sxs-lookup"><span data-stu-id="79e4e-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="79e4e-104">Før returnerede varer kan modtages på lager, skal følgesedlen til den ordre, de tilhører, være opdateret.</span><span class="sxs-lookup"><span data-stu-id="79e4e-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="79e4e-105">Ligesom fakturaopdateringsprocessen er opdateringen af den økonomiske transaktion, er opdateringsprocessen for følgesedlen den fysiske opdatering af lagerposten, så ændringerne foretages på lageret.</span><span class="sxs-lookup"><span data-stu-id="79e4e-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="79e4e-106">Ved returneringer bliver de trin, der tildeles dispositionshandlingen, implementeret under opdateringen af følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="79e4e-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="79e4e-107">Opdateringen af følgesedlen kan behandles i varemodtagelseskladden eller returordren.</span><span class="sxs-lookup"><span data-stu-id="79e4e-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="79e4e-108">Som en del af posteringsprocessen for følgesedlen kan følgesedlens referencenummer fra kundens forsendelsesdokumenter knyttes til ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="79e4e-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="79e4e-109">Denne tilknytning er valgfri og kun til orientering.</span><span class="sxs-lookup"><span data-stu-id="79e4e-109">This association is optional and for reference only.</span></span> <span data-ttu-id="79e4e-110">Den opretter ikke nogen transaktionsopdateringer.</span><span class="sxs-lookup"><span data-stu-id="79e4e-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="79e4e-111">Hvis ikke alle de forventede returvarer er ankommet, skal du kun medtage det antal, der er modtaget, i følgeseddelopdateringen.</span><span class="sxs-lookup"><span data-stu-id="79e4e-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="79e4e-112">Lad de øvrige varer blive i ordren, indtil resten af returforsendelsen er ankommet.</span><span class="sxs-lookup"><span data-stu-id="79e4e-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="79e4e-113">Hvis en vare er sendt tilbage fra karantæne til forsendelses- og modtagelsesafdelingen, f.eks. når karantænekontrolløren ikke ved, hvor varen skal placeres på lageret, skal den tilsvarende følgeseddel opdateres for korrekt at registrere og udføre handlingen for den dispositionskode, der er anført som resultat af karantænen.</span><span class="sxs-lookup"><span data-stu-id="79e4e-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="79e4e-114">Når du opdaterer en følgeseddel for en returneret vare, der er fra en salgsaftale, opdateres salgsaftaleforpligtelsen for varen automatisk for at afspejle ændringer i antal eller beløb.</span><span class="sxs-lookup"><span data-stu-id="79e4e-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="79e4e-115">Se også</span><span class="sxs-lookup"><span data-stu-id="79e4e-115">See also</span></span>

[<span data-ttu-id="79e4e-116">Udføre fakturaopdateringer til returneringer</span><span class="sxs-lookup"><span data-stu-id="79e4e-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


