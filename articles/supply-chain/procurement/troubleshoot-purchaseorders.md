---
title: Lokalisere fejl i indkøbsordrer
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbsordrer.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 964f31c21faae6a947174f637624aca917881297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841449"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="46e4f-103">Lokalisere fejl i indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="46e4f-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="46e4f-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="46e4f-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="46e4f-105">En handling kan først fuldføres, når linjenummeret er fuldt fordelt.</span><span class="sxs-lookup"><span data-stu-id="46e4f-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="46e4f-106">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="46e4f-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="46e4f-107">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="46e4f-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="46e4f-108">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="46e4f-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="46e4f-109">Når indkøbsordrer importeres via datastyring, følger numrene på indkøbsordrelinjer ikke den forøgelse, der er defineret i systemparametrene.</span><span class="sxs-lookup"><span data-stu-id="46e4f-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-110">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-110">Issue description</span></span>

<span data-ttu-id="46e4f-111">Automatisk genererede linjenumre for indkøbsordrelinjer, der er importeret via *Indkøbsordrelinjer V2*-dataenhed, bruger som standard ikke det stigende systemlinjenummer, der er angivet i systemparametrene.</span><span class="sxs-lookup"><span data-stu-id="46e4f-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="46e4f-112">Hvis du opretter en indkøbsordre manuelt og tilføjer linjer via brugergrænsefladen, stiger linjenumrene korrekt.</span><span class="sxs-lookup"><span data-stu-id="46e4f-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="46e4f-113">Men hvis du bruger datastyringsstrukturen (DMF - Data Management Framework), stiger de ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="46e4f-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="46e4f-114">Dette problem opstår, fordi systemet bruger DMF-metoden til at tildele dem, når du importerer linjer via DMF, hvis de ikke allerede er tildelt i den importerede enhed.</span><span class="sxs-lookup"><span data-stu-id="46e4f-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="46e4f-115">Metoden øger altid linjenumrene med én.</span><span class="sxs-lookup"><span data-stu-id="46e4f-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="46e4f-116">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-116">Issue workaround</span></span>

<span data-ttu-id="46e4f-117">Sørg for, at de ønskede linjenumre allerede er angivet i felterne for linjenummer i dataenheden, når du importerer indkøbsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="46e4f-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="46e4f-118">I dette tilfælde overskriver DMF ikke linjenumrene.</span><span class="sxs-lookup"><span data-stu-id="46e4f-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="46e4f-119">Der udfyldes ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="46e4f-120">Hvis du bruger en fakturakonto, der er forskellig fra debitorkontoen, udfyldes der ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen, når der oprettes en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="46e4f-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="46e4f-121">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-121">This behavior is by design.</span></span> <span data-ttu-id="46e4f-122">Standardværdierne for momsgruppen, kasserabatter og andre prisoplysninger er baseret på debitorkontoen – ikke fakturakontoen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="46e4f-123">Jeg får vist fejlmeddelelsen "Objektreferencen er ikke angivet" under bekræftelse af indkøbsordren, eller der er opstået "Destinationen for en aktivering udløste en undtagelse" under bogføring af kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="46e4f-124">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="46e4f-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="46e4f-125">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="46e4f-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="46e4f-126">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="46e4f-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="46e4f-127">En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt.</span><span class="sxs-lookup"><span data-stu-id="46e4f-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-128">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-128">Issue description</span></span>

<span data-ttu-id="46e4f-129">Du får følgende fejl: "En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt".</span><span class="sxs-lookup"><span data-stu-id="46e4f-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e4f-130">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-130">Issue resolution</span></span>

<span data-ttu-id="46e4f-131">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="46e4f-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="46e4f-132">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="46e4f-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="46e4f-133">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="46e4f-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="46e4f-134">Kan jeg nøjes med at få vist de indkøbsordrer, jeg har oprettet?</span><span class="sxs-lookup"><span data-stu-id="46e4f-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="46e4f-135">Denne funktionalitet er ikke tilgængelig i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="46e4f-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="46e4f-136">Kan jeg reservere en lagerbeholdning og oprette transaktioner mod registreret lager på en indkøbsordre?</span><span class="sxs-lookup"><span data-stu-id="46e4f-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-137">Issue description</span></span>

<span data-ttu-id="46e4f-138">Selv når varer er i en *Registreret* tilstand på en indkøbsordre, kan du stadig reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="46e4f-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="46e4f-139">Du kan med andre ord oprette transaktioner mod det registrerede lager.</span><span class="sxs-lookup"><span data-stu-id="46e4f-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="46e4f-140">Genskabe problemet</span><span class="sxs-lookup"><span data-stu-id="46e4f-140">Reproduce the issue</span></span>

<span data-ttu-id="46e4f-141">Følgende procedurer viser en måde at genskabe problemet på.</span><span class="sxs-lookup"><span data-stu-id="46e4f-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="46e4f-142">Oprette en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="46e4f-142">Create a purchase order.</span></span>
2. <span data-ttu-id="46e4f-143">Registrér indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="46e4f-144">Bemærk, at du kan generere reservationer eller transaktioner mod det registrerede lager.</span><span class="sxs-lookup"><span data-stu-id="46e4f-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e4f-145">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-145">Issue resolution</span></span>

<span data-ttu-id="46e4f-146">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-146">This behavior is by design.</span></span> <span data-ttu-id="46e4f-147">Det forventes, at de registrerede varer er modtaget fysisk på lagerstedet eller lageret, og at de derfor er tilgængelige for reservation.</span><span class="sxs-lookup"><span data-stu-id="46e4f-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="46e4f-148">Indkøbsordrer afspejler ikke den juridiske enheds sprogindstillinger.</span><span class="sxs-lookup"><span data-stu-id="46e4f-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-149">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-149">Issue description</span></span>

<span data-ttu-id="46e4f-150">Produktnavnet på en indkøbsordre vises på systemsproget i stedet for det sprog, der er angivet for den juridiske enhed, hvor indkøbsordren er oprettet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="46e4f-151">Genskabe problemet</span><span class="sxs-lookup"><span data-stu-id="46e4f-151">Reproduce the issue</span></span>

<span data-ttu-id="46e4f-152">Følgende procedurer viser en måde at genskabe problemet på.</span><span class="sxs-lookup"><span data-stu-id="46e4f-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="46e4f-153">Indstil systemsproget til *EN-US* (amerikansk engelsk).</span><span class="sxs-lookup"><span data-stu-id="46e4f-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="46e4f-154">Sørg for, at der findes et produkt, hvor sprogene *EN-US* og *DK* (dansk) bruges til oversættelser af produktnavnet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="46e4f-155">Skift sproget for en juridisk enhed til *DK*.</span><span class="sxs-lookup"><span data-stu-id="46e4f-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="46e4f-156">Opret en indkøbsordre, der indeholder produktet, i den juridiske enhed, hvor *DK* er angivet som sprog.</span><span class="sxs-lookup"><span data-stu-id="46e4f-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="46e4f-157">Bemærk, at produktnavnet stadig vises på amerikansk engelsk (systemsproget).</span><span class="sxs-lookup"><span data-stu-id="46e4f-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e4f-158">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-158">Issue resolution</span></span>

<span data-ttu-id="46e4f-159">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-159">This behavior is by design.</span></span> <span data-ttu-id="46e4f-160">På indkøbsordrer vises produktet altid på systemsproget.</span><span class="sxs-lookup"><span data-stu-id="46e4f-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="46e4f-161">Indkøbsordresproget bruges, når der oprettes en bekræftelsesjournal.</span><span class="sxs-lookup"><span data-stu-id="46e4f-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="46e4f-162">Listen over godkendte kreditorer efter produktenhed tillader ikke, at ikrafttrædelsesdatoen ændres.</span><span class="sxs-lookup"><span data-stu-id="46e4f-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-163">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-163">Issue description</span></span>

<span data-ttu-id="46e4f-164">Et produkt har en godkendt kreditor, der f.eks. har ikrafttrædelsesdatoen 11. januar 2018 (*01/11/2018*) og udløbsdatoen *Aldrig*.</span><span class="sxs-lookup"><span data-stu-id="46e4f-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="46e4f-165">Hvis du forsøger at ændre ikrafttrædelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du vist følgende fejl:</span><span class="sxs-lookup"><span data-stu-id="46e4f-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="46e4f-166">Der kan ikke oprettes en post på listen over godkendte kreditorer (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="46e4f-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="46e4f-167">Værdien 'Udløb' skal være større end eller lig med værdien 'Gyldig fra'.</span><span class="sxs-lookup"><span data-stu-id="46e4f-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e4f-168">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-168">Issue resolution</span></span>

<span data-ttu-id="46e4f-169">Du kan kun udvide den periode, som kreditoren er godkendt til.</span><span class="sxs-lookup"><span data-stu-id="46e4f-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="46e4f-170">Der gælder følgende regler:</span><span class="sxs-lookup"><span data-stu-id="46e4f-170">The following rules apply:</span></span>

- <span data-ttu-id="46e4f-171">Hvis du vil ændre ikrafttrædelsesdatoen, så den er tidligere end nogen af de eksisterende poster (perioder) for varens leverandør, skal udløbsdatoen for den nye periode være før alle udløbsdatoerne i de eksisterende poster.</span><span class="sxs-lookup"><span data-stu-id="46e4f-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="46e4f-172">Hvis du vil ændre udløbsdatoen, så den er senere end nogen af de eksisterende perioder, skal ikrafttrædelsesdatoen være efter den seneste udløbsdato i en eksisterende post.</span><span class="sxs-lookup"><span data-stu-id="46e4f-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="46e4f-173">Hvis du vil reducere den overordnede periode, som kreditoren er godkendt for, skal du slette eller redigere eksisterende poster.</span><span class="sxs-lookup"><span data-stu-id="46e4f-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="46e4f-174">Du kan også bruge **afkort**-parameteren under importen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="46e4f-175">Denne parameter sletter alle eksisterende poster i tabellen for godkendte kreditorer efter vare.</span><span class="sxs-lookup"><span data-stu-id="46e4f-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="46e4f-176">I eksempelscenariet, der er beskrevet i problembeskrivelsen, hvor en post har ikrafttrædelsesdatoen *01/11/2018* og en udløbsdato på *Aldrig*, kan du importere en ny post, der har ikrafttrædelsesdatoen *01/10/2018* og en udløbsdato på *Aldrig*.</span><span class="sxs-lookup"><span data-stu-id="46e4f-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="46e4f-177">Du kan dog ikke reducere perioden, så ikrafttrædelsesdatoen opdateres til *01/12/2018* via Dataadministration.</span><span class="sxs-lookup"><span data-stu-id="46e4f-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="46e4f-178">Du skal foretage denne ændring via brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="46e4f-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="46e4f-179">Efter at jeg har ændret leveringsadressen på et indkøbsordrehoved, synkroniseres leveringsnavnet ikke.</span><span class="sxs-lookup"><span data-stu-id="46e4f-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e4f-180">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="46e4f-180">Issue description</span></span>

<span data-ttu-id="46e4f-181">Adressen på hovedet i en indkøbsordre opdateres til en adresse, der ikke er en leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="46e4f-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="46e4f-182">Selvom adressen opdateres på indkøbsordren, opdateres leveringsnavnet ikke på basis af den opdaterede adresse.</span><span class="sxs-lookup"><span data-stu-id="46e4f-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e4f-183">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="46e4f-183">Issue resolution</span></span>

<span data-ttu-id="46e4f-184">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="46e4f-184">This behavior is by design.</span></span> <span data-ttu-id="46e4f-185">Den valgte adresse skal klassificeres som en leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="46e4f-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="46e4f-186">Ellers opdateres leveringsnavnet ikke på basis af den valgte adresse.</span><span class="sxs-lookup"><span data-stu-id="46e4f-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="46e4f-187">Kan jeg finde den bruger, der har annulleret en indkøbsordre?</span><span class="sxs-lookup"><span data-stu-id="46e4f-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="46e4f-188">Disse oplysninger spores kun, hvis ændringsstyring er aktiveret for indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="46e4f-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="46e4f-189">Hvis du bruger ændringsstyring, kan du se, hvem der har afsendt ændringen (annulleringen), og hvem der har godkendt den.</span><span class="sxs-lookup"><span data-stu-id="46e4f-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]