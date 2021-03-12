---
title: Ekstra lokationszoner
description: Dette emne indeholder en oversigt over de nye lokationszoner, der er føjet til Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996420"
---
# <a name="additional-location-zones"></a><span data-ttu-id="4c3e0-103">Ekstra lokationszoner</span><span class="sxs-lookup"><span data-stu-id="4c3e0-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c3e0-104">Der er tre nye zonefelter tilgængelige i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4c3e0-105">Lagerstedschefer kan bruge dem til at definere yderligere lagerstedsorganisationer eller -layout.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="4c3e0-106">De nye zonefelter kan enten angives manuelt eller ved hjælp af guiden **Konfiguration af lokation**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="4c3e0-107">De kan bruges i en forespørgsel eller filtrering, der bruger tabellen Lokationer.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="4c3e0-108">Der kræves ikke yderligere konfiguration for at kunne bruge zonefelterne.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="4c3e0-109">Aktivér funktionen Ekstra lokationszone</span><span class="sxs-lookup"><span data-stu-id="4c3e0-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="4c3e0-110">Før du kan bruge funktionen *Ekstra lokationszone*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="4c3e0-111">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4c3e0-112">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="4c3e0-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4c3e0-113">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="4c3e0-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4c3e0-114">**Funktionsnavn:** *Flere lokationszoner*</span><span class="sxs-lookup"><span data-stu-id="4c3e0-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="4c3e0-115">Bruge lokationszoner</span><span class="sxs-lookup"><span data-stu-id="4c3e0-115">Use location zones</span></span>

1. <span data-ttu-id="4c3e0-116">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Guiden Konfiguration af lokation**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="4c3e0-117">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="4c3e0-117">Set the following values:</span></span>

    - <span data-ttu-id="4c3e0-118">Vælg _62_ i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="4c3e0-119">Gå til feltet **Zone-id**, og vælg _PRODUKTION_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="4c3e0-120">Gå til feltet **Ekstra zone 1**, og vælg _PLUKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="4c3e0-121">Gå til feltet **Ekstra zone 2**, og vælg _WEBBUTIK1_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="4c3e0-122">Gå til feltet **Lokationsprofil-id**, og vælg _PRODUKTION_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="4c3e0-123">Vælg linjen **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="4c3e0-124">Gå til feltet **Fra nummer**, og angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="4c3e0-125">Gå til feltet **Til nummer**, og angiv _3_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="4c3e0-126">Vælg linjen **Gang**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="4c3e0-127">Gå til feltet **Fra nummer**, og angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="4c3e0-128">Gå til feltet **Til nummer**, og angiv _5_.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="4c3e0-129">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-129">Select **Create**.</span></span>
8. <span data-ttu-id="4c3e0-130">Du modtager meddelelser om, at der er tilføjet nye lokationer.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="4c3e0-131">Vælg knappen **Vis meddelelser** for at få vist meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="4c3e0-132">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.</span><span class="sxs-lookup"><span data-stu-id="4c3e0-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="4c3e0-133">De nye lokationer vises på listen, og alle zone felter er tilgængelige (dvs. det eksisterende zonefelt og de nye ekstra zonefelter).</span><span class="sxs-lookup"><span data-stu-id="4c3e0-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
