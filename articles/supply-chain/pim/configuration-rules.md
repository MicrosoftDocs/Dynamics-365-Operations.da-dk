---
title: Variantregler
description: Denne artikel indeholder generelle oplysninger om variantregler. Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 87927f5bddbf11c224c77cff7c5355f2cd1317a6
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="76d5e-104">Variantregler</span><span class="sxs-lookup"><span data-stu-id="76d5e-104">Configuration rules</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="76d5e-105">Denne artikel indeholder generelle oplysninger om variantregler.</span><span class="sxs-lookup"><span data-stu-id="76d5e-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="76d5e-106">Variantregler definerer relationer mellem elementer i en stykliste i styklisten for produkter, der bruger teknologien Dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76d5e-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="76d5e-107">Variantregler er tilgængelige, når du definerer modeller for dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76d5e-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="76d5e-108">Variantregler anvendes til enten at gennemtvinge eller forbyde specifikke varekombinationer på en stykliste.</span><span class="sxs-lookup"><span data-stu-id="76d5e-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="76d5e-109">Når en stykliste er blevet oprettet, og de pågældende varer er blevet tildelt til deres respektive variantgrupper, kan der defineres en eller flere variantregler.</span><span class="sxs-lookup"><span data-stu-id="76d5e-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="76d5e-110">Hvis to varer hører sammen, bruges operatoren **Vælg** til at sikre medtagelse.</span><span class="sxs-lookup"><span data-stu-id="76d5e-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="76d5e-111">Hvis to varer gensidigt udelukker hinanden, bruges operatoren **Fravælg** til at sikre udelukkelse.</span><span class="sxs-lookup"><span data-stu-id="76d5e-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="76d5e-112">**Bemærk!** Disse oplysninger gælder kun for produktmasters, der bruger teknologien til dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76d5e-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="76d5e-113">Eksisterende varianter påvirkes ikke af efterfølgende ændringer af variantreglerne.</span><span class="sxs-lookup"><span data-stu-id="76d5e-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="76d5e-114">Men det er vigtigt, at du opretter reglerne, før du definerer en ny variant, og at du kontrollerer reglerne, hvis du tror, at de er ændret.</span><span class="sxs-lookup"><span data-stu-id="76d5e-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="76d5e-115">**Bemærk!** Metoden **Vælg** betyder, at den afledte variantgruppe, varenummer og variant vælges automatisk.</span><span class="sxs-lookup"><span data-stu-id="76d5e-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="76d5e-116">Metoden **Fravælg** betyder, at den afledte variantgruppe, varenummer og variant ikke kan vælges.</span><span class="sxs-lookup"><span data-stu-id="76d5e-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="76d5e-117">Se også</span><span class="sxs-lookup"><span data-stu-id="76d5e-117">See also</span></span>
--------

[<span data-ttu-id="76d5e-118">Dimensionsbaseret produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="76d5e-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




