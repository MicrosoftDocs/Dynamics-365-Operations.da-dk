---
title: Sende returvarer videre til inspektion
description: Når du registrerer en returvare, skal du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e8205db277715f4f4f9c1ee589f264c0ded6617
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424653"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="94433-103">Sende returvarer videre til inspektion</span><span class="sxs-lookup"><span data-stu-id="94433-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="94433-104">Når du registrerer en returvare, kan du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.</span><span class="sxs-lookup"><span data-stu-id="94433-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="94433-105">Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Varemodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="94433-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="94433-106">\-eller-</span><span class="sxs-lookup"><span data-stu-id="94433-106">\-or-</span></span>
    
    <span data-ttu-id="94433-107">Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Produktionsindlagring**.</span><span class="sxs-lookup"><span data-stu-id="94433-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="94433-108">Registrer modtagelsen af en vare som sædvanligt i formularen **Lokationskladde**.</span><span class="sxs-lookup"><span data-stu-id="94433-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="94433-109">Du kan finde oplysninger om registrering af modtagelsen af returnerede varer under <A href="register-the-receipt-of-returned-items.md">Registrere modtagelsen af returvarer</A></span><span class="sxs-lookup"><span data-stu-id="94433-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="94433-110">Under fanen **Standardværdier** i området **Håndteringsmåde** skal du markere feltet **Karantænestyring**.</span><span class="sxs-lookup"><span data-stu-id="94433-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="94433-111">Dette betyder, at systemet vil oprette en karantæneordre, og den person eller afdeling, der udfører inspektionerne, vil svare på denne ordre ved hjælp af formularen **Karantæneordre**.</span><span class="sxs-lookup"><span data-stu-id="94433-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="94433-112">Se også</span><span class="sxs-lookup"><span data-stu-id="94433-112">See also</span></span>

[<span data-ttu-id="94433-113">Føre returvarer gennem inspektion</span><span class="sxs-lookup"><span data-stu-id="94433-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="94433-114">Angive, hvordan returvarer skal kasseres</span><span class="sxs-lookup"><span data-stu-id="94433-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

