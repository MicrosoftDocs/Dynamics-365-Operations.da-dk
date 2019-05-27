---
title: Amortisere konstante omkostninger for en produceret vare
description: En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 7ccd5ce3e2ed58db8f13eebbcfa6fe5fb544d6c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564218"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="e6e81-103">Amortisere konstante omkostninger for en produceret vare</span><span class="sxs-lookup"><span data-stu-id="e6e81-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6e81-104">En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.</span><span class="sxs-lookup"><span data-stu-id="e6e81-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="e6e81-105">Begrebet efterkalkulationslotstørrelse bruges til at amortisere disse konstante omkostninger i den beregnede kostpris for en produceret vare.</span><span class="sxs-lookup"><span data-stu-id="e6e81-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="e6e81-106">Der er adskillige synonymer til begrebet, et af dem regnskabsmæssig lotstørrelse.</span><span class="sxs-lookup"><span data-stu-id="e6e81-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="e6e81-107">Begrebet amortisering af konstante omkostninger har også adskillige synonymer, hvoraf et er proportionale konstante omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e6e81-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="e6e81-108">Antallet i en efterkalkulationslotstørrelsen for en produceret vare bruges i en styklistekalkulation.</span><span class="sxs-lookup"><span data-stu-id="e6e81-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="e6e81-109">Antallet afhænger af, hvordan du starter og udfører styklistekalkulationen, som det vises af følgende:</span><span class="sxs-lookup"><span data-stu-id="e6e81-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="e6e81-110">Standardberegningsmængden i styklistekalkulationen for en vare – Standardordreantallet for lager for varen fungerer som efterkalkulationslotstørrelse, men standardværdien kan være et større antal, sådan at den afspejler kvoten for varens ordreantal.</span><span class="sxs-lookup"><span data-stu-id="e6e81-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="e6e81-111">Varens standardordreantal og -kvote kan angives inden for varens standardordreindstillinger eller lokationsspecifikke ordreindstillinger.</span><span class="sxs-lookup"><span data-stu-id="e6e81-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="e6e81-112">Angivet beregningsantal i styklistekalkulationen for en vare − Den angivne beregningsmængde fungerer som efterkalkulationslotstørrelse for varen.</span><span class="sxs-lookup"><span data-stu-id="e6e81-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="e6e81-113">Antallet for beregningsmængden bruger først varens standardordreantal, men standardværdien kan tilsidesættes manuelt.</span><span class="sxs-lookup"><span data-stu-id="e6e81-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="e6e81-114">Den angivne beregningsmængde repræsenterer efterkalkulationslotstørrelsen for den angivne vare og for fremstillede komponenter, der har en styklistelinje af typen produktion.</span><span class="sxs-lookup"><span data-stu-id="e6e81-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="e6e81-115">Det er fordi, det antages, at komponenten skal fremstilles i nøjagtigt antal.</span><span class="sxs-lookup"><span data-stu-id="e6e81-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="e6e81-116">Efterkalkulationslotstørrelsen for andre fremstillede komponenter, der har styklistelinjetypen Vare, vil afspejle deres standardordreantal.</span><span class="sxs-lookup"><span data-stu-id="e6e81-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="e6e81-117">Angiven beregningsmængde for Fremstil til ordre i styklistekalkulationen for en vare – Den angivne beregningsmængde fungerer som efterkalkulationslotstørrelse for varen og dens fremstillede komponenter, når styklistekalkulationer bruger udfoldningstilstanden Fremstil til ordre.</span><span class="sxs-lookup"><span data-stu-id="e6e81-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="e6e81-118">De forudsættes, at de fremstillede komponenter vil blive fremstillet i nøjagtigt antal på samme måde som en fremstillet komponent, der har styklistetypen Produktion.</span><span class="sxs-lookup"><span data-stu-id="e6e81-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="e6e81-119">Den angivne beregningsmængde i en ordrespecifik styklistekalkulation – Der kan udføres en ordrespecifik styklistekalkulation for en varelinje på en salgsordre, et salgstilbud eller en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="e6e81-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="e6e81-120">Antallet for den angivne beregningsmængde bruger antallet på den oprindelige varelinje, men standardantallet kan tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="e6e81-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="e6e81-121">Du kan vælge, om den ordrespecifikke styklistekalkulation bruger udfoldningstilstanden Fremstil til ordre eller Flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="e6e81-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="e6e81-122">Det beregnede beløb af en produceret vares amortiserede konstante omkostninger kaldes gebyrer.</span><span class="sxs-lookup"><span data-stu-id="e6e81-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





