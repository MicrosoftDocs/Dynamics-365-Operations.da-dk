---
title: Oprette lagersteder for flytteordrer
description: I dette emne beskrives, hvordan du kan konfigurere lagersteder for flytteordrer.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e482567eb92b9ab891d41d82d10cbb87f9b7fb01
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425010"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="ba6ac-103">Oprette lagersteder for flytteordrer</span><span class="sxs-lookup"><span data-stu-id="ba6ac-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba6ac-104">Du kan bruge lagerstedsniveauer til at oprette et hierarki, der understøtter flytteforslag mellem lagerstederne.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="ba6ac-105">På baggrund af denne opsætning beregner behovsplanlægningen varebehov på de enkelte lagerstedsniveauer, og der genereres flytteforslag fra et tilknyttet kildelagersted, der skal opfylde disse forslag.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="ba6ac-106">Klik på **Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="ba6ac-107">Vælg det lagersted, der skal opfyldes.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="ba6ac-108">I oversigtspanelet **Varedisponering** skal du markere afkrydsningsfeltet **Opfyldning**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="ba6ac-109">Vælg i feltet **Hovedlagersted** det lagersted, du vil tilknytte som opfyldningslagerstedet.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="ba6ac-110">I behovsplanlægningen beregnes et flyttebehov for det valgte lagersted, og der oprettes et flytteordreforslag fra det tilknyttede **Hovedlagersted**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="ba6ac-111">Hvis du fjerner markeringen i feltet <STRONG>Opfyldning</STRONG>, tildeles det valgte lagersted et lagerstedsniveau i forbindelse med <STRONG>Hovedlagersted</STRONG>, men <STRONG>Hovedlagersted</STRONG> konfigureres ikke som et opfyldningslagersted.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="ba6ac-112">Luk siden for at anvende den nye konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="ba6ac-113">Hvis du vil angive et lagersted til opfyldning, skal du først oprette lagerstedet som en lagringsdimension på siden <STRONG>Lagringsdimensionsgrupper</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="ba6ac-114">På denne side skal du markere feltet <STRONG>Aktiv</STRONG> og feltet <STRONG>Disponer pr. dimension</STRONG> for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="ba6ac-115">Angive leveringstid for transport</span><span class="sxs-lookup"><span data-stu-id="ba6ac-115">Set up transport lead time</span></span>

<span data-ttu-id="ba6ac-116">Du skal også angive transportleveringstiden mellem lagerstederne på siden **Transportdage**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="ba6ac-117">Gå til **Lagerstyring > Opsætning > Distribution > Transportdage**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="ba6ac-118">Vælg **lagersted** i feltet **Tilgangssted**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="ba6ac-119">Vælg **Forsendelseslagersted**, **Tilgangslagersted** og **Transportdage**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="ba6ac-120">(Valgfrit) Du kan også angive transporttiden, afhængigt af leveringsmåden, under fanen **Transportdage pr. leveringsmåde**.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
