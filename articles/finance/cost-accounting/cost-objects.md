---
title: Dimensioner for omkostningsobjekt
description: Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til. Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger. Dette emne indeholder oplysninger om omkostningsobjektdimensioner.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a090ecae2aadf1d0e08dd6127f831abdbf4a6b0a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976421"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="e7965-105">Dimensioner for omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7965-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7965-106">Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til.</span><span class="sxs-lookup"><span data-stu-id="e7965-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="e7965-107">Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7965-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="e7965-108">Dette emne indeholder oplysninger om omkostningsobjektdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e7965-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="e7965-109">Et omkostningsobjekt kan være en hvilken som helst type objekt, du vil vurdere, allokere omkostninger til eller måle direkte.</span><span class="sxs-lookup"><span data-stu-id="e7965-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="e7965-110">Typiske omkostningsobjekter omfatter produkter, projekter, ressourcer, afdelinger, bærere og geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="e7965-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="e7965-111">Ledelsen bruger omkostningsobjekter til at kvantificere omkostninger og oprette rentabilitetsanalyser.</span><span class="sxs-lookup"><span data-stu-id="e7965-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="e7965-112">Omkostningsobjektdimensioner og omkostningsobjekters dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="e7965-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="e7965-113">Omkostningsobjekter er kendt som *omkostningsobjektdimensioner*.</span><span class="sxs-lookup"><span data-stu-id="e7965-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="e7965-114">Når du har besluttet, hvilkel enhed omkostningsobjektdimensionen skal referere til, skal du angive de enkelte dimensionsværdier eller importere dem til omkostningsregnskabet fra andre kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="e7965-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="e7965-115">De enkelte dimensionsværdier kaldes *omkostningsobjekters dimensionsmedlemmer*.</span><span class="sxs-lookup"><span data-stu-id="e7965-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="e7965-116">For eksempel vil du bruge den økonomiske dimension, der hedder Bærer, som omkostningsobjektdimensionen.</span><span class="sxs-lookup"><span data-stu-id="e7965-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="e7965-117">Hvis du vil se, hvordan omkostninger flyder til de enkelte bærer, skal du importere omkostningsobjektets dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e7965-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="e7965-118">I dette tilfælde er omkostningsobjektets dimensionsmedlemmer faktiske bærere som salg, produktion, administration og geografiske placeringer.</span><span class="sxs-lookup"><span data-stu-id="e7965-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="e7965-119">Følgende skærmbillede vises et eksempel på bærere som omkostningsobjekdimension med dets faktiske bærere som dimensionsmedlemmer af omkostningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="e7965-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="e7965-120">[![Skærmbillede, der viser Bærer som omkostningsobjektdimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="e7965-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="e7965-121">Importere omkostningsobjekters dimensionsmedlemmer gennem dataconnectorer</span><span class="sxs-lookup"><span data-stu-id="e7965-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="e7965-122">For at gøre import af omkostningsobjekters dimensionsmedlemmer nemmere kan du bruge dataconnectorer til at hente værdierne fra de enheder, du vil bruge som omkostningsobjektdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e7965-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="e7965-123">Du kan bruge de færdigbyggede dataforbindelser eller tilpassede dataconnectorer, du bygger.</span><span class="sxs-lookup"><span data-stu-id="e7965-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



