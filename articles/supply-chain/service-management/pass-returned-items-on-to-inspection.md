---
title: Sende returvarer videre til inspektion
description: "Når du registrerer en returvare, skal du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a60e6635e3bb1723ced7aba1a71135116b53272
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---


# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="25f30-103">Sende returvarer videre til inspektion</span><span class="sxs-lookup"><span data-stu-id="25f30-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="25f30-104">Når du registrerer en returvare, kan du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.</span><span class="sxs-lookup"><span data-stu-id="25f30-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="25f30-105">Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Varemodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="25f30-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="25f30-106">\-eller-</span><span class="sxs-lookup"><span data-stu-id="25f30-106">\-or-</span></span>
    
    <span data-ttu-id="25f30-107">Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Produktionsindlagring**.</span><span class="sxs-lookup"><span data-stu-id="25f30-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="25f30-108">Registrer modtagelsen af en vare som sædvanligt i formularen **Lokationskladde**.</span><span class="sxs-lookup"><span data-stu-id="25f30-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="25f30-109">Du kan finde oplysninger om registrering af modtagelsen af returnerede varer under <A href="register-the-receipt-of-returned-items.md">Registrere modtagelsen af returvarer</A></span><span class="sxs-lookup"><span data-stu-id="25f30-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="25f30-110">Under fanen **Standardværdier** i området **Håndteringsmåde** skal du markere feltet **Karantænestyring**.</span><span class="sxs-lookup"><span data-stu-id="25f30-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="25f30-111">Dette betyder, at systemet vil oprette en karantæneordre, og den person eller afdeling, der udfører inspektionerne, vil svare på denne ordre ved hjælp af formularen **Karantæneordre**.</span><span class="sxs-lookup"><span data-stu-id="25f30-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="25f30-112">Se også</span><span class="sxs-lookup"><span data-stu-id="25f30-112">See also</span></span>

[<span data-ttu-id="25f30-113">Føre returvarer gennem inspektion</span><span class="sxs-lookup"><span data-stu-id="25f30-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="25f30-114">Angive, hvordan returvarer skal kasseres</span><span class="sxs-lookup"><span data-stu-id="25f30-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

