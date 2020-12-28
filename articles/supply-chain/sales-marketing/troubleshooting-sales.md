---
title: Lokalisere fejl i salgsordrer
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgsordrer.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424585"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="08bed-103">Lokalisere fejl i salgsordrer</span><span class="sxs-lookup"><span data-stu-id="08bed-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="08bed-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="08bed-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="08bed-105">Oplysningerne om moms opdateres ikke, hvis jeg ændrer placeringen på et salgsordrehoved.</span><span class="sxs-lookup"><span data-stu-id="08bed-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="08bed-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="08bed-106">Issue description</span></span>

<span data-ttu-id="08bed-107">Hvis stedet, lagerstedet eller leveringsadressen ændres enten på et salgsordrehoved eller på linjeniveau, opdateres momsoplysningerne ikke automatisk for linjerne.</span><span class="sxs-lookup"><span data-stu-id="08bed-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="08bed-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="08bed-108">Issue resolution</span></span>

<span data-ttu-id="08bed-109">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="08bed-109">This behavior is by design.</span></span> <span data-ttu-id="08bed-110">Problemet opstår, fordi leveringsadressen, stedet og lagerstedet ikke ændres automatisk på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="08bed-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="08bed-111">Du skal opdatere dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="08bed-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="08bed-112">Hvis der er to samhandelsaftaler for samme periode eller overlappende perioder, er den samme aftalelinje altid valgt.</span><span class="sxs-lookup"><span data-stu-id="08bed-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="08bed-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="08bed-113">Issue description</span></span>

<span data-ttu-id="08bed-114">Hvis der er defineret to samhandelsaftaler for samme periode eller overlappende perioder, ser den samme samhandelsaftale ud til at blive valgt, hver gang du opretter salgsordrelinjer, der indeholder de pågældende varer.</span><span class="sxs-lookup"><span data-stu-id="08bed-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="08bed-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="08bed-115">Issue resolution</span></span>

<span data-ttu-id="08bed-116">Hvis der er mere end én samhandelsaftale for en given dato, vil den samhandelsaftale, der har den laveste pris, altid blive valgt.</span><span class="sxs-lookup"><span data-stu-id="08bed-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="08bed-117">Du kan finde flere oplysninger ved at hente følgende hvidbog: [Samhandelsaftaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="08bed-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="08bed-118">Kan jeg knytte en indkøbsordre til en salgsordre for at opfylde efterspørgslen?</span><span class="sxs-lookup"><span data-stu-id="08bed-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="08bed-119">Du kan oprette en indkøbsordre ud fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="08bed-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="08bed-120">Du kan finde flere oplysninger i [Oprette en indkøbsordre fra en salgsordre](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="08bed-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="08bed-121">Jeg kan ikke annullere eller slette en returordre eller salgsordre.</span><span class="sxs-lookup"><span data-stu-id="08bed-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="08bed-122">Du kan kun annullere salgsordrer og returordrer, der er i *Oprettet* tilstand.</span><span class="sxs-lookup"><span data-stu-id="08bed-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="08bed-123">Du kan finde flere oplysninger under [Annullere en returordre](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="08bed-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="08bed-124">Når jeg forsøger at annullere en salgsordre, modtager jeg fejlen "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, der er afhængig af reservationerne".</span><span class="sxs-lookup"><span data-stu-id="08bed-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="08bed-125">Hvis arbejdet er knyttet til en salgsordre, kan du ikke annullere salgsordren, før arbejdet er annulleret og tilbageført.</span><span class="sxs-lookup"><span data-stu-id="08bed-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="08bed-126">Dette krav gælder, selvom det arbejde, der er tilknyttet salgsordren, er lukket.</span><span class="sxs-lookup"><span data-stu-id="08bed-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="08bed-127">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="08bed-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="08bed-128">Annuller arbejdet, og læg lageret tilbage på den ønskede lokation.</span><span class="sxs-lookup"><span data-stu-id="08bed-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="08bed-129">Gå til den relevante last af salgsordren, og vælg enten **Reducer plukket antal** på lastlinjen eller **Tilbagefør arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="08bed-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="08bed-130">Arbejdet har nu statussen *Annulleret*, og der oprettes og behandles automatisk nyt arbejde for lagerbevægelse for at bringe lagerbeholdningen tilbage til den lokation, der blev angivet, da den blev tilbageført.</span><span class="sxs-lookup"><span data-stu-id="08bed-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="08bed-131">Slet lasten.</span><span class="sxs-lookup"><span data-stu-id="08bed-131">Delete the load.</span></span> <span data-ttu-id="08bed-132">Forsendelsen slettes også.</span><span class="sxs-lookup"><span data-stu-id="08bed-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="08bed-133">Du skulle nu kunne gå til salgsordren og annullere den.</span><span class="sxs-lookup"><span data-stu-id="08bed-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="08bed-134">Jeg kan ikke annullere en intern indkøbsordre, der er knyttet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="08bed-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="08bed-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="08bed-135">Issue description</span></span>

<span data-ttu-id="08bed-136">Hvis du forsøger at annullere en intern indkøbsordre, der er knyttet til en salgsordre, kan du få vist følgende fejlmeddelelse: "Antal kan ikke nedsættes, da restopdateringsantallet skifter fortegn".</span><span class="sxs-lookup"><span data-stu-id="08bed-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="08bed-137">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="08bed-137">Issue resolution</span></span>

<span data-ttu-id="08bed-138">Dette problem blev løst i Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="08bed-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="08bed-139">I denne version og senere versioner kan du nu annullere en intern indkøbsordre, der er knyttet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="08bed-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="08bed-140">Kan jeg gendanne en faktureret salgsordre, der er slettet?</span><span class="sxs-lookup"><span data-stu-id="08bed-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="08bed-141">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="08bed-141">Issue description</span></span>

<span data-ttu-id="08bed-142">En faktureret salgsordre blev slettet ved en fejl, og du vil gendanne den eller se oplysningerne om den.</span><span class="sxs-lookup"><span data-stu-id="08bed-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="08bed-143">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="08bed-143">Issue resolution</span></span>

<span data-ttu-id="08bed-144">Hvis den slettede salgsordre allerede er faktureret, skal du gå til **Debitorkonto \> Transaktioner \> Oprindeligt dokument \> Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="08bed-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="08bed-145">Find den faktura, du leder efter, og vælg den for at få vist oplysninger om den.</span><span class="sxs-lookup"><span data-stu-id="08bed-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="08bed-146">Disse oplysninger omfatter referencen til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="08bed-146">These details include the sales order reference.</span></span> <span data-ttu-id="08bed-147">Du skulle også kunne få adgang til salgsordreoplysningerne fra den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="08bed-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="08bed-148">Fristen for et salgsordrehoved blev ikke fundet i dataobjektet SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="08bed-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="08bed-149">Feltet Frist findes ikke i *SalesOrderHeaderV2Entity*-enheden.</span><span class="sxs-lookup"><span data-stu-id="08bed-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="08bed-150">Jeg skal slette poster for tabte salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="08bed-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="08bed-151">Hvis du vil rydde op i tabte salgsordreposter, skal du køre det periodiske job *Sletning af salgsordre* ved at gå til et af følgende steder:</span><span class="sxs-lookup"><span data-stu-id="08bed-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="08bed-152">Salg og markering \> Periodiske opgaver \> Oprydning \> Slet salgsordrer</span><span class="sxs-lookup"><span data-stu-id="08bed-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="08bed-153">Detail og handel \> Retail og Commerce IT \> Oprydning \> Slet salgsordrer</span><span class="sxs-lookup"><span data-stu-id="08bed-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="08bed-154">Er det muligt at beregne provision på fakturaer, der allerede er bogført?</span><span class="sxs-lookup"><span data-stu-id="08bed-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="08bed-155">Supply Chain Management understøtter i øjeblikket ikke beregningen af provisioner for bogførte fakturaer.</span><span class="sxs-lookup"><span data-stu-id="08bed-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="08bed-156">En bundtvare understøttes ikke i en intern proces.</span><span class="sxs-lookup"><span data-stu-id="08bed-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="08bed-157">Bundtvaren er ikke tilgængelig for indkøbsordren, fordi antallet er *0* (nul) på salgsordrelinjerne for bundtvaren, og status er *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="08bed-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="08bed-158">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="08bed-158">This behavior is by design.</span></span> <span data-ttu-id="08bed-159">Salgsordren køber kun komponenterne i bundtvaren.</span><span class="sxs-lookup"><span data-stu-id="08bed-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="08bed-160">Den køber ikke selve bundtvaren.</span><span class="sxs-lookup"><span data-stu-id="08bed-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="08bed-161">Hvis du skal købe et bundt, skal du overveje, om du vil markere det som en bundtvare, da denne funktionalitet faktisk er udviklet til scenarier for indtægtsføring.</span><span class="sxs-lookup"><span data-stu-id="08bed-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="08bed-162">Yderligere oplysninger om bundtvarer finder du under [Bundter](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="08bed-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
