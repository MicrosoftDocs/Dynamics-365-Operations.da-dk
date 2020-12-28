---
title: Føre returvarer gennem inspektion
description: Føre returvarer gennem inspektion.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424789"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="4ec71-103">Føre returvarer gennem inspektion</span><span class="sxs-lookup"><span data-stu-id="4ec71-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="4ec71-104">Klik på **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karantæneordrer**.</span><span class="sxs-lookup"><span data-stu-id="4ec71-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="4ec71-105">Find den ordrelinje, der svarer til den returnerede vare, du undersøger.</span><span class="sxs-lookup"><span data-stu-id="4ec71-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="4ec71-106">En karantæneordre kan kun knyttes til et enkelt varenummer.</span><span class="sxs-lookup"><span data-stu-id="4ec71-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="4ec71-107">Hvis der returneres ti varer med forskellige varenumre i en enkelt forsendelse, og de sendes i karantæne, oprettes der ti forskellige karantæneordrer.</span><span class="sxs-lookup"><span data-stu-id="4ec71-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="4ec71-108">Når varen er undersøgt, skal du foretage et valg i feltet **Dispositionskode** for at angive, hvad der skal ske med varen, og hvordan den relaterede økonomiske transaktion skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="4ec71-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="4ec71-109">Varen kan f.eks. returneres til lager, samtidig med at kunden refunderes, varen kan kasseres, samtidig med at der sendes en erstatning til kunden, eller varen kan returneres til kunden uden kredit.</span><span class="sxs-lookup"><span data-stu-id="4ec71-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="4ec71-110">Hvis flere varer i en enkelt varenummerbatch ikke kan knyttes til samme dispositionskode, skal du opdele karantæneordren (<STRONG>Funktioner</STRONG> &gt; <STRONG>Opdel</STRONG>) for at tildele en anden dispositionskode til de enkelte underbatch.</span><span class="sxs-lookup"><span data-stu-id="4ec71-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="4ec71-111">Når du er færdig med inspektionen, skal du klikke på **Færdigmeld** for at frigive de returnerede varer og oprette en varemodtagelseskladdepostering.</span><span class="sxs-lookup"><span data-stu-id="4ec71-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="4ec71-112">Den person eller afdeling, der modtager varerne, skal behandle kladden for de varer, som skal returneres til lageret.</span><span class="sxs-lookup"><span data-stu-id="4ec71-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="4ec71-113">eller</span><span class="sxs-lookup"><span data-stu-id="4ec71-113">–or–</span></span>
    
    <span data-ttu-id="4ec71-114">Afslut karantæneordren, og flyt varerne tilbage til lageret direkte ved hjælp af en af funktionerne for **Lager**.</span><span class="sxs-lookup"><span data-stu-id="4ec71-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="4ec71-115">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="4ec71-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ec71-116">Se også</span><span class="sxs-lookup"><span data-stu-id="4ec71-116">See also</span></span>

[<span data-ttu-id="4ec71-117">Angive, hvordan returvarer skal kasseres</span><span class="sxs-lookup"><span data-stu-id="4ec71-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


