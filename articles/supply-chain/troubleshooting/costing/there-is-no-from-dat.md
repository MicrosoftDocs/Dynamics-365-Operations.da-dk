---
title: Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris
description: Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026386"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="97a6c-103">Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris</span><span class="sxs-lookup"><span data-stu-id="97a6c-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="97a6c-104">KB-nummer: 4613548</span><span class="sxs-lookup"><span data-stu-id="97a6c-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="97a6c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="97a6c-105">Symptoms</span></span>

<span data-ttu-id="97a6c-106">Der er ingen værdi for **Fra-dato** under fanen **Aktive priser** på siden **Varepris**.</span><span class="sxs-lookup"><span data-stu-id="97a6c-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="97a6c-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="97a6c-107">Resolution</span></span>

<span data-ttu-id="97a6c-108">Værdien for **Fra dato** (ikrafttrædelsesdato), der er angivet på den ventende pris, overføres ikke til den aktive pris.</span><span class="sxs-lookup"><span data-stu-id="97a6c-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="97a6c-109">Når en vares omkostningspost angives først, har den status *Venter* og en ønsket ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="97a6c-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="97a6c-110">Når du aktiverer omkostningsposten, opdateres statussen til *Aktiv*, og ikrafttrædelsesdatoen opdateres til aktiveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="97a6c-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="97a6c-111">Aktiveringsdatoen for den aktive pris er derfor altid den faktiske dato for aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="97a6c-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="97a6c-112">Du kan finde flere oplysninger i [Oversigt over efterkalkulationsversioner](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="97a6c-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
