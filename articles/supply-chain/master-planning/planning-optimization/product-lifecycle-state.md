---
title: Udelukke produkter, der har specifikke livscyklustilstande
description: Dette emne forklarer, hvordan du kan udelukke produkter baseret på deres livscyklustilstand, når planlægningsoptimeringsfunktionen bruges.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645085"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="aa414-103">Udelukke produkter, der har specifikke livscyklustilstande</span><span class="sxs-lookup"><span data-stu-id="aa414-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa414-104">Frigivne produkter og frigivne produktversioner indeholder feltet **Status for produktlivscyklus**.</span><span class="sxs-lookup"><span data-stu-id="aa414-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="aa414-105">I dette felt kan du blandt andet kontrollere, hvilke produkter der indgår i varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="aa414-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="aa414-106">Du kan tilføje, fjerne og redigere livscyklustilstande efter behov ved at gå til **Administration af produktoplysninger \> Konfiguration \> Status for produktlivscyklus**.</span><span class="sxs-lookup"><span data-stu-id="aa414-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="aa414-107">For hver produktlivscyklustilstand skal du angive indstillingen **Er aktiv for planlægning** til *Ja*, hvis produkter, der har den pågældende tilstand, skal medtages under varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="aa414-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="aa414-108">Når indstillingen er angivet til *Nej*, udelukkes de tilknyttede produkter og varianter fra alle varedisponeringer og alle beregninger på styklisteniveau.</span><span class="sxs-lookup"><span data-stu-id="aa414-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="aa414-109">Frigivne produkter og varianter, hvor feltet **Produktets livscyklustilstand** er tomt, behandles, som om der er en produktlivscyklustilstand, hvor indstillingen **Er aktiv for planlægning** angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="aa414-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="aa414-110">De vil med andre ord blive medtaget under varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="aa414-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="aa414-111">For at undgå unødvendige leveringsforslag anbefaler vi på det kraftigste, at du knytter alle forældede frigivne produkter og varianter sammen med en produktlivscyklustilstand, hvor indstillingen **Er aktiv for planlægning** er angivet til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="aa414-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="aa414-112">Denne fremgangsmåde er særlig vigtig, når du arbejder med produktkonfigurationsvarianter, der ikke kan genbruges, fordi den vil hjælpe med at forhindre spild.</span><span class="sxs-lookup"><span data-stu-id="aa414-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="aa414-113">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="aa414-113">Related resources</span></span>

<span data-ttu-id="aa414-114">Yderligere oplysninger om produktlivscyklustilstand finder du under [Oversigt over produktlivscyklustilstand](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="aa414-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="aa414-115">Du kan finde detaljerede oplysninger om, hvordan du kan bruge statusser for produktlivscyklus til at udelukke produkter fra varedisponering og beregning af styklisteniveau, under [Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="aa414-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
