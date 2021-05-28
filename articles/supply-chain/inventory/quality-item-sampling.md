---
title: Varestikprøve for kvalitetsstyring
description: Dette emne beskriver, hvordan du konfigurerer varestikprøver.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022222"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="d820d-103">Varestikprøve for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="d820d-103">Quality management item sampling</span></span>

<span data-ttu-id="d820d-104">Varestikprøver bruges som del af kvalitetssikringen.</span><span class="sxs-lookup"><span data-stu-id="d820d-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="d820d-105">Den definerer mængden af det aktuelle fysiske lager, som skal inspiceres.</span><span class="sxs-lookup"><span data-stu-id="d820d-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="d820d-106">Varestikprøver kan baseres på faste antal, en procentdel eller hele varenummeret.</span><span class="sxs-lookup"><span data-stu-id="d820d-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="d820d-107">Konfigurer vareprøve</span><span class="sxs-lookup"><span data-stu-id="d820d-107">Set up item sampling</span></span>

<span data-ttu-id="d820d-108">Benyt følgende fremgangsmåde for at konfigurere varestikprøve.</span><span class="sxs-lookup"><span data-stu-id="d820d-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="d820d-109">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="d820d-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="d820d-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d820d-110">Select **New**.</span></span>
1. <span data-ttu-id="d820d-111">Indtast en værdi i feltet **Varestikprøve**.</span><span class="sxs-lookup"><span data-stu-id="d820d-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="d820d-112">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d820d-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="d820d-113">Angiv et tal i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="d820d-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="d820d-114">Denne værdi er relateret til den angivne værdi for det antal, der er valgt i det tilstødende felt.</span><span class="sxs-lookup"><span data-stu-id="d820d-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="d820d-115">Markér afkrydsningsfeltet **Fuld blokering** i sektionen **Proces**, hvis hele parti- eller ordrelinjeantallet skal blokeres, når en test er mislykket.</span><span class="sxs-lookup"><span data-stu-id="d820d-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="d820d-116">Hvis dette afkrydsningsfelt ikke er markeret, blokeres kun varerne i kvalitetsordren, når en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="d820d-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="d820d-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d820d-117">Select **Save**.</span></span>
1. <span data-ttu-id="d820d-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d820d-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="d820d-119">Funktionen *Kvalitetsstyring for lagerstedsprocesser* indeholder yderligere vareprøveegenskaber.</span><span class="sxs-lookup"><span data-stu-id="d820d-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="d820d-120">Den tilføjer et begreb for *varestikprøves omfang* og gør det muligt at definere et helt varenummer som specifikation af antallet.</span><span class="sxs-lookup"><span data-stu-id="d820d-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="d820d-121">Hvis du har aktiveret denne funktion, skal du se [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="d820d-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
