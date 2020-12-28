---
title: Automatisk autorisation med planlægningsoptimering
description: Dette emne beskriver, hvordan du bruger automatisk autorisation med Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 61e9e6aa660bc0828645c6bf1f2655539804831a
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594520"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="86229-103">Automatisk autorisation med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="86229-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86229-104">Ved automatisk autorisation kan du autorisere (dvs. frigive) ordreforslag som del af varedisponeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="86229-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="86229-105">Når ordreforslag autoriseres, omdannes de til faktiske indkøbsordrer, overførelsesordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="86229-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="86229-106">Når der bruges Planlægningsoptimering, autoriseres ordreforslag under en varedisponeringskørsel, når ordredatoen (dvs. startdatoen) ligger inden for tidshorisonten til autorisation.</span><span class="sxs-lookup"><span data-stu-id="86229-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="86229-107">Auto-autorisation af et indkøbsordreforslag kan kun forekomme, hvis varen er knyttet til en kreditor.</span><span class="sxs-lookup"><span data-stu-id="86229-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="86229-108">Aktivere automatisk autorisation</span><span class="sxs-lookup"><span data-stu-id="86229-108">Turn on autofirming</span></span>

<span data-ttu-id="86229-109">Udfør følgende trin for at aktivere automatisk autorisation.</span><span class="sxs-lookup"><span data-stu-id="86229-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="86229-110">I arbejdsområdet **Funktionsstyring** på fanen **Ny** skal du vælge **Auto-autorisering for Planlægningsoptimering** fra listen.</span><span class="sxs-lookup"><span data-stu-id="86229-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="86229-111">Hvis funktionen ikke vises under den fanen **Ny**, skal du se på fanerne **Ikke aktiverede** og **Alle**.</span><span class="sxs-lookup"><span data-stu-id="86229-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="86229-112">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="86229-112">Select **Enable now**.</span></span> <span data-ttu-id="86229-113">Du kan også vælge **Planlæg** og derefter vælge det tidspunkt, hvor funktionen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="86229-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="86229-114">Konfigurer autorisationens tidshorisont</span><span class="sxs-lookup"><span data-stu-id="86229-114">Set up the firming time fence</span></span>

<span data-ttu-id="86229-115">Autorisationstidshorisonten beregnes fremad fra datoen for kørslen af varedisponering.</span><span class="sxs-lookup"><span data-stu-id="86229-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="86229-116">Den defineres af det af dig indtastede antal af dage.</span><span class="sxs-lookup"><span data-stu-id="86229-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="86229-117">Du kan styre tidshorisonten for autorisationen på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="86229-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="86229-118">Hvis du vil definere standardautorisationstidshorisonten for en disponeringsgruppe, skal du gå til **Varedisponering** \> **Opsætning** \> **Disponering** \> **Disponeringsgrupper** og vælge en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="86229-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="86229-119">Derefter skal du angive antallet af dage i oversigtspanelet **Andet** i feltet **Automatisk autorisationstidshorisont (dage)**.</span><span class="sxs-lookup"><span data-stu-id="86229-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="86229-120">Hvis du vil overskrive den autorisationstidshorisont, der er defineret for disponeringsgruppen for en bestemt vare, skal du gå til **Administration af produktinformation** \> **Frigivne produkter**, og dernæst i handlingsruden vælge **Plan** og derefter vælge **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="86229-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="86229-121">I fanen **Generelt** skal du vælge **Overskriv tidshorisont** og i feltet **Automatisk autorisationstidshorisont (dage)** skal du angive antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="86229-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="86229-122">Hvis du vil overskrive den autorisationstidshorisont, der er defineret for disponeringsgruppen og varedisponeringen for en bestemt behovsplan, skal du gå til **Varedisponering** \> **Opsætning** \> **Behovsplan** og dernæst vælge en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="86229-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="86229-123">Derefter skal du i oversigtspanelet **Tidshorisont i dage** angive **Autorisation** til **Ja** og angivet antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="86229-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="86229-124">Hvis automatisk autorisation er aktiveret for en varedisponeringskørsel, der bruger Planlægningsoptimering, udføres den automatiske autorisationsproces i henhold til den automatiske autorisationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="86229-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="86229-125">Hvis automatisk autorisation ikke er slået til, eller hvis planlægningen startes fra siden **Nettokrav**, springes den automatiske autorisationsproces over.</span><span class="sxs-lookup"><span data-stu-id="86229-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="86229-126">Planlægsningsoptimering i forhold til det indbyggede planlægningsprogram for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="86229-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="86229-127">Både Planlægningsoptimering og planlægningsprogrammet, der er indbygget i Microsoft Dynamics 365 Supply Chain Management, kan bruges til automatisk autorisation af ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="86229-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="86229-128">Der er dog nogle vigtige forskelle.</span><span class="sxs-lookup"><span data-stu-id="86229-128">However, there are some important differences.</span></span> <span data-ttu-id="86229-129">I Planlægningsoptimering bruges ordredatoen (dvs. startdatoen) til at bestemme, hvilke ordreforslag der skal autoriseres, ved hjælp af behovsdatoen (dvs. slutdatoen) for det indbyggede planlægningsprogram for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="86229-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="86229-130">Her vises en oversigt over forskellene.</span><span class="sxs-lookup"><span data-stu-id="86229-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="86229-131">**Planlægningsoptimering**</span><span class="sxs-lookup"><span data-stu-id="86229-131">**Planning Optimization**</span></span>

- <span data-ttu-id="86229-132">Automatisk autorisation er baseret på ordredatoen (startdato).</span><span class="sxs-lookup"><span data-stu-id="86229-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="86229-133">Da ordredatoen (startdato) udløser en autorisation, behøver du ikke at overveje leveringstiden som en del af autorisations tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="86229-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="86229-134">Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal autorisationstidshorisonten være én uge.</span><span class="sxs-lookup"><span data-stu-id="86229-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="86229-135">**Indbygget planlægningsprogram for Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="86229-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="86229-136">Automatisk autorisation er baseret på behovsdatoen (slutdatoen).</span><span class="sxs-lookup"><span data-stu-id="86229-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="86229-137">For at sikre, at ordrer autoriseres rettidigt, skal autorisationstidshorisonten være længere end leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="86229-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="86229-138">Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal autorisationstidshorisonten være leveringstiden plus én uge.</span><span class="sxs-lookup"><span data-stu-id="86229-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
