---
title: Varestikprøve for kvalitetsstyring
description: Dette emne beskriver, hvordan du konfigurerer varestikprøver.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956587"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="52c10-103">Varestikprøve for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="52c10-103">Quality management item sampling</span></span>

<span data-ttu-id="52c10-104">Varestikprøver bruges som del af kvalitetssikringen.</span><span class="sxs-lookup"><span data-stu-id="52c10-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="52c10-105">Den definerer mængden af det aktuelle fysiske lager, som skal inspiceres.</span><span class="sxs-lookup"><span data-stu-id="52c10-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="52c10-106">Varestikprøver kan baseres på faste antal, en procentdel eller hele varenummeret.</span><span class="sxs-lookup"><span data-stu-id="52c10-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="52c10-107">Konfigurer vareprøve</span><span class="sxs-lookup"><span data-stu-id="52c10-107">Set up item sampling</span></span>

<span data-ttu-id="52c10-108">Benyt følgende fremgangsmåde for at konfigurere varestikprøve.</span><span class="sxs-lookup"><span data-stu-id="52c10-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="52c10-109">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="52c10-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="52c10-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52c10-110">Select **New**.</span></span>
1. <span data-ttu-id="52c10-111">Indtast en værdi i feltet **Varestikprøve**.</span><span class="sxs-lookup"><span data-stu-id="52c10-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="52c10-112">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="52c10-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="52c10-113">Angiv et tal i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="52c10-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="52c10-114">Denne værdi er relateret til den angivne værdi for det antal, der er valgt i det tilstødende felt.</span><span class="sxs-lookup"><span data-stu-id="52c10-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="52c10-115">Markér afkrydsningsfeltet **Fuld blokering** i sektionen **Proces**, hvis hele parti- eller ordrelinjeantallet skal blokeres, når en test er mislykket.</span><span class="sxs-lookup"><span data-stu-id="52c10-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="52c10-116">Hvis dette afkrydsningsfelt ikke er markeret, blokeres kun varerne i kvalitetsordren, når en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="52c10-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="52c10-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="52c10-117">Select **Save**.</span></span>
1. <span data-ttu-id="52c10-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="52c10-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="52c10-119">Funktionen *Kvalitetsstyring for lagerstedsprocesser* indeholder yderligere vareprøveegenskaber.</span><span class="sxs-lookup"><span data-stu-id="52c10-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="52c10-120">Den tilføjer et begreb for *varestikprøves omfang* og gør det muligt at definere et helt varenummer som specifikation af antallet.</span><span class="sxs-lookup"><span data-stu-id="52c10-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="52c10-121">Hvis du har aktiveret denne funktion, skal du se [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="52c10-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
