---
title: Lokalisere fejl i indkøbs- og forsyningsarbejdsgange
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbs- og forsyningsarbejdsgange.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d5d688c5769a62580e48908117d0562b26eab10a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222819"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="3dc0b-103">Lokalisere fejl i indkøbs- og forsyningsarbejdsgange</span><span class="sxs-lookup"><span data-stu-id="3dc0b-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="3dc0b-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbs- og forsyningsarbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="3dc0b-105">Fejl ved genafsendelse af en indkøbsordre til arbejdsgangen efter en ændring: "Ændringer af indkøbsordre X er kun tilladt i kladdetilstand, når ændringsstyring er aktiveret"</span><span class="sxs-lookup"><span data-stu-id="3dc0b-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="3dc0b-106">Dette problem opstår kun, hvis indkøbsordren var i en *Bekræftet* tilstand, før du anmodede om ændringer.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="3dc0b-107">Hvis du anmoder om ændringer, mens indkøbsordren er i *Godkendt* tilstand, kan arbejdsgangen behandles uden fejl.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="3dc0b-108">Fejlbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3dc0b-108">Error description</span></span>

<span data-ttu-id="3dc0b-109">Følgende fejl opstår i arbejdsgangen, når en indkøbsordre sendes igen efter en ændring:</span><span class="sxs-lookup"><span data-stu-id="3dc0b-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="3dc0b-110">Stoppet (fejl): X++ undtagelse: Ændringer af indkøbsordre PO0000569 er kun tilladt i kladdetilstand, når ændringsstyring er aktiveret ved</span><span class="sxs-lookup"><span data-stu-id="3dc0b-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="3dc0b-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="3dc0b-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="3dc0b-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="3dc0b-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="3dc0b-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="3dc0b-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="3dc0b-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="3dc0b-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3dc0b-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="3dc0b-115">Issue resolution</span></span>

<span data-ttu-id="3dc0b-116">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3dc0b-117">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3dc0b-118">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="3dc0b-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="3dc0b-119">Problemet vil blive løst i [denne artikel i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="3dc0b-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="3dc0b-120">En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="3dc0b-121">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3dc0b-122">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3dc0b-123">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="3dc0b-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="3dc0b-124">Hvis en leveringsrest annulleres på en indkøbsordre, hvor ændringsstyring er aktiveret, går indkøbsordren til en bekræftet tilstand.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3dc0b-125">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3dc0b-125">Issue description</span></span>

<span data-ttu-id="3dc0b-126">I forbindelse med en indkøbsordre, der er underlagt ændringsstyring, og hvis den eneste anmodede ændring er at annullere en leveringsrest på en eller flere af linjerne, går indkøbsordren direkte til en *Bekræftet* tilstand, når den godkendes, og der oprettes ikke en kladde.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3dc0b-127">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="3dc0b-127">Issue resolution</span></span>

<span data-ttu-id="3dc0b-128">Annullering af en leveringsrest påvirker ikke indholdet af bekræftelsesjournalen.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="3dc0b-129">Denne funktionalitet skal bruges, når linjen er blevet delvist modtaget, og restantallet skal annulleres i procestrinnet, når indkøbsordren er blevet bekræftet af leverandøren.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="3dc0b-130">Hvis dette skal afspejles i indkøbsordrebekræftelsen, skal antallet justeres på indkøbsordrelinjen, så bekræftelsen bliver påkrævet.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="3dc0b-131">Hvis der ikke er modtaget noget på linjen, kan du også fjerne antallet.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="3dc0b-132">I dette tilfælde er ny bekræftelse påkrævet.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="3dc0b-133">Annullerede indkøbsordrer vises på kladdelisten i arbejdsområdet til forberedelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3dc0b-134">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3dc0b-134">Issue description</span></span>

<span data-ttu-id="3dc0b-135">Når du har annulleret indkøbsordrer, der er i en *Bekræftet* tilstand, vises de annullerede indkøbsordrer stadig på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3dc0b-136">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="3dc0b-136">Issue resolution</span></span>

<span data-ttu-id="3dc0b-137">Dette problem opstår kun ved indkøbsordrer, der er omfattet af en ændringsstyring.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="3dc0b-138">Det sker, fordi annulleringen betragtes som en ændring, der skal godkendes.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="3dc0b-139">Godkendelsen kan foretages automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="3dc0b-140">Derfor er processen at sende den annullerede indkøbsordre til godkendelsesarbejdsgangen, så den kan gå til en *Godkendt* tilstand.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="3dc0b-141">På dette tidspunkt vises indkøbsordren ikke længere på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="3dc0b-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]