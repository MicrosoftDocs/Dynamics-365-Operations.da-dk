---
title: Varen kan ikke have en stykliste eller formel
description: Når du forsøger at autorisere en ordre, modtager du en fejlmeddelelse under varevalidering. Den angiver, at varen ikke kan have en stykliste eller formel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294038"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="76077-104">Varen kan ikke have en stykliste eller formel</span><span class="sxs-lookup"><span data-stu-id="76077-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="76077-105">Fejlkode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="76077-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="76077-106">Symptomer</span><span class="sxs-lookup"><span data-stu-id="76077-106">Symptoms</span></span>

<span data-ttu-id="76077-107">Når du forsøger at autorisere en ordre, modtager du følgende fejlmeddelelse under varevalidering:</span><span class="sxs-lookup"><span data-stu-id="76077-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="76077-108">Varen kan ikke have en stykliste eller formel</span><span class="sxs-lookup"><span data-stu-id="76077-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="76077-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="76077-109">Resolution</span></span>

<span data-ttu-id="76077-110">Varer, der har en stykliste eller formel, skal være af typen *Planlægningsvare*, *Stykliste* eller *Formel*.</span><span class="sxs-lookup"><span data-stu-id="76077-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="76077-111">Benyt følgende fremgangsmåde for at ændre typen af vare.</span><span class="sxs-lookup"><span data-stu-id="76077-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="76077-112">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="76077-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="76077-113">Åbn det relevante produkt.</span><span class="sxs-lookup"><span data-stu-id="76077-113">Open the relevant product.</span></span>
1. <span data-ttu-id="76077-114">I oversigtspanelet **Opret** skal du angive feltet **Produktionstype** til *Planlægsningsvare*, *Stykliste* eller *Formel*.</span><span class="sxs-lookup"><span data-stu-id="76077-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
