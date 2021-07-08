---
title: Transaktionsstatussen for annullerede produktkvitteringer opdateres ikke til Registreret
description: Når du har annulleret produktkvitteringerne ved en indgående last, opdaterer systemet automatisk lagertransaktionens status fra Modtaget til Bestilt.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294036"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="19419-103">Transaktionsstatussen for annullerede produktkvitteringer opdateres ikke til Registreret</span><span class="sxs-lookup"><span data-stu-id="19419-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="19419-104">Symptomer</span><span class="sxs-lookup"><span data-stu-id="19419-104">Symptoms</span></span>

<span data-ttu-id="19419-105">Når du har kørt handlingen **Annuller produktkvitteringer** ved en indgående last, opdaterer systemet automatisk lagertransaktionens status fra *Modtaget* til *Bestilt*.</span><span class="sxs-lookup"><span data-stu-id="19419-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="19419-106">Løsning</span><span class="sxs-lookup"><span data-stu-id="19419-106">Resolution</span></span>

<span data-ttu-id="19419-107">Når følgesedler annulleres ved udgående laster, forbliver statussen for lagertransaktioner *Plukket*.</span><span class="sxs-lookup"><span data-stu-id="19419-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="19419-108">Men når produktkvitteringer fra en indgående last annulleres, gendannes statussen for lagertransaktioner ikke til *Registreret*.</span><span class="sxs-lookup"><span data-stu-id="19419-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="19419-109">Når en produktkvittering fra en indgående last annulleres, skal lagerarbejderen derfor registrere vareantal for lasten igen.</span><span class="sxs-lookup"><span data-stu-id="19419-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="19419-110">Du kan finde flere oplysninger i [Registrere vareantal, der ankommer ved en indgående last](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="19419-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
