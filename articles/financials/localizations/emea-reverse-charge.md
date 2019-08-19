---
title: Modtagermoms
description: I dette emne beskrives, hvordan du konfigurerer modtagermoms for europæiske lande, Saudi-Arabien og Singapore.
author: epodkolz
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 530ff52abb1dd36c473ae436d61ea925c5696a30
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852417"
---
# <a name="reverse-charge-vat"></a><span data-ttu-id="3b0e5-103">Modtagermoms</span><span class="sxs-lookup"><span data-stu-id="3b0e5-103">Reverse charge VAT</span></span>


[!include [banner](../includes/banner.md)]


<span data-ttu-id="3b0e5-104">I dette emne beskrives den generelle tilgang til konfiguration af modtagermoms moms for Saudi-Arabien, Singapore og europæiske lande.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia, Singapore, and European countries.</span></span>

<span data-ttu-id="3b0e5-105">Modtagermoms er et momsskema, der flytter ansvaret for momsregnskab og rapportering af moms fra sælgeren til køberen af varer og/eller tjenesteydelser.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="3b0e5-106">Derfor registrerer modtagere af varer og/eller ydelser både udgående moms (i rollen som sælger) og indgående moms (i rollen som køber) i deres momsangivelse.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="3b0e5-107">I nogle lande eller områder implementeres modtagermomsskemaet kun for nogle varer og/eller ydelser, og der er yderligere betingelser eller grænser for salgsbeløb.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="3b0e5-108">I andre lande eller områder afhænger ansvaret for momsbetalingen af leverandørens og køberens status.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="3b0e5-109">Hvis køberen skal betale moms, skal denne oplysning tydeligt fremgå af fakturaen, som leverandøren udsteder.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="3b0e5-110">Fakturaen skal f.eks. indeholde ordet "modtagermoms" ("Reverse charge") og skal angive, hvilke stillinger der er underlagt modtagermomsskemaet.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="3b0e5-111">Når du vil anvende modtagermoms, skal du udføre følgende konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="3b0e5-112">Konfigurer momskoder</span><span class="sxs-lookup"><span data-stu-id="3b0e5-112">Set up sales tax codes</span></span>
<span data-ttu-id="3b0e5-113">Det anbefales at bruge separate momskoder til henholdsvis salgs- og indkøbsoperationer.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="3b0e5-114"><strong>Momskode for salg</strong></span><span class="sxs-lookup"><span data-stu-id="3b0e5-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="3b0e5-115">Opret en momskode for salgsoperationer med modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momskoder</strong>).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b0e5-116"><strong>Momskode for køb</strong></span><span class="sxs-lookup"><span data-stu-id="3b0e5-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="3b0e5-117">Opret positive og negative momskoder for modtagermoms for køb (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momskoder</strong>).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="3b0e5-118">Opret en momskode, der har en positiv værdi.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="3b0e5-119">Opret en momskode, der har en negativ værdi.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="3b0e5-120">Angiv <strong>Ja</strong> for indstillingen <strong>Tillad en negativ momsprocent</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="3b0e5-121">Du skal tildele denne negative momskode til en varemomsgruppe og derefter knytte varemomsgruppen til varer, der er omfattet af modtagermomsen.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="3b0e5-122">Du kan finde flere oplysninger i det næste afsnit &quot;Konfigurer momsgrupper og varemomsgrupper&quot;.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="3b0e5-123">Konfigurere momsgrupper og varemomsgrupper</span><span class="sxs-lookup"><span data-stu-id="3b0e5-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="3b0e5-124">Det anbefales at bruge separate momsgrupper til henholdsvis salgs- og indkøbsoperationer.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="3b0e5-125"><strong>Momsgrupper for salg</strong></span><span class="sxs-lookup"><span data-stu-id="3b0e5-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="3b0e5-126">Opret en momsgruppe for salgsoperationer, der har modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momsgrupper</strong>).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3b0e5-127">Under fanen <strong>Opsætning</strong> kan du medtage momskoden for modtagermoms i denne gruppe.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="3b0e5-128">Markér afkrydsningsfelterne <strong>Frit</strong> og <strong>Modtagermoms</strong> for momskoden.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b0e5-129"><strong>Varemomsgrupper for køb</strong></span><span class="sxs-lookup"><span data-stu-id="3b0e5-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="3b0e5-130">Opret en momsgruppe for købsoperationer, der har modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momsgrupper</strong>).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3b0e5-131">Under fanen <strong>Opsætning</strong> kan du medtage både positive og negative momskoder i denne gruppe.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="3b0e5-132">Markér afkrydsningsfelt <strong>Modtagermoms</strong> for den momskode, der har en negativ værdi.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3b0e5-133"><strong>Varemomsgrupper</strong></span><span class="sxs-lookup"><span data-stu-id="3b0e5-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="3b0e5-134">Opret eller opdater varemomsgruppen med den momskode, der har en negativ værdi (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Varemomsgrupper</strong>).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="3b0e5-135">Du skal tildele standardvaremomsgruppen til de produkter og kategorier, der er omfattet af modtagermomsen.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="3b0e5-136">Konfigurere modtagermomsgrupper</span><span class="sxs-lookup"><span data-stu-id="3b0e5-136">Set up reverse charge groups</span></span>
<span data-ttu-id="3b0e5-137">På siden **Varegrupper med modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Varegrupper med modtagermoms**) kan du definere grupper af produkter eller tjenester eller individuelle produkter eller tjenester, som modtagermomsen kan pålægges.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="3b0e5-138">For hver varegruppe med modtagermoms skal du definere listen over varer, varegrupper og kategorier for salg og/eller køb.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="3b0e5-139">Konfigurere regler for modtagermoms</span><span class="sxs-lookup"><span data-stu-id="3b0e5-139">Set up reverse charge rules</span></span>
<span data-ttu-id="3b0e5-140">På siden **Regler for modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Regler for modtagermoms**) kan du definere anvendelighedsregler til købs- og salgsformål.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="3b0e5-141">Du kan konfigurere et sæt regler for anvendelse af modtagermoms.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="3b0e5-142">For hvert regelsæt skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="3b0e5-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="3b0e5-143">**Dokumenttype** – Vælg **Indkøbsordre**, **Kreditorfakturajournal**, **Salgsordre**, **Fritekstfaktura**, **Debitorfakturajournal** og/eller **Kreditorfaktura**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="3b0e5-144">**Lande-/områdetype for partneren** – Vælg **Indenlandsk**, **EU** eller **Udenlandsk**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="3b0e5-145">Alternativt, hvis reglen kan anvendes på alle samarbejdspartnere, uanset landet eller området i deres adresse, skal du vælge **Alle**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="3b0e5-146">**Indenlandsk leveringsadresse** – Marker dette afkrydsningsfelt for at anvende reglen på leveringer i det samme land eller område.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="3b0e5-147">Dette afkrydsningsfelt kan ikke markeres for dokumenttyperne **Kreditorfakturajournal** og **Debitorfakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="3b0e5-148">**Varegruppe med modtagermoms** – Vælg den gruppe, som reglen kan anvendes på.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="3b0e5-149">**Tærskelbeløb** – Skemaet for modtagermoms anvendes kun på en faktura, hvis værdien af varer og/eller tjenesteydelser, der er medtaget i varegruppen med modtagermoms, overskrider den grænse, du angiver her.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="3b0e5-150">Du kan også bruge felterne **Ikrafttrædelsesdato** og **Udløbsdato** til at definere den periode, hvor reglen er i kraft.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="3b0e5-151">Derudover kan du angive, om der skal vises en besked, og om dokumentlinjen skal opdateres med standardmomsgruppen for modtagermoms, hvis betingelsen for den pågældende dokumentlinje er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="3b0e5-152">Følgende valgmuligheder er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="3b0e5-152">The following options are available:</span></span>

- <span data-ttu-id="3b0e5-153">**Ingen** – Bilagslinjen opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="3b0e5-154">**Spørg** – Der vises en besked for at bekræfte, at der kan anvendes modtagermoms.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="3b0e5-155">**Indstil** – Dokumentlinjen opdateres uden yderligere besked.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="3b0e5-156">Konfigurere standardparametre</span><span class="sxs-lookup"><span data-stu-id="3b0e5-156">Set up default parameters</span></span>
<span data-ttu-id="3b0e5-157">Du aktiverer funktionen for modtagermoms på siden **Finansparametre** under fanen **Modtagermoms** at vælge **Ja** for indstillingen **Aktiver tilbageført gebyr**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="3b0e5-158">I felterne **Indkøbsordremomsgruppe** og **Salgsordremomsgruppe** skal du vælge standardmomsgrupperne.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="3b0e5-159">Når en betingelse for anvendelse af modtagermoms er opfyldt, opdateres salgs- eller købsordrelinjen med disse momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="3b0e5-160">Modtagermoms på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="3b0e5-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="3b0e5-161">Sælgeren opkræver ikke moms for salg, der er angivet i modtagermomsskemaet.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="3b0e5-162">I stedet angives både de varer, som er genstand for modtagermomsen, og det samlede beløb for modtagermomsen på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="3b0e5-163">Når en salgsfaktura med modtagermoms bogføres, har momstransaktionerne momsretningen **Udgående moms** og ingen moms, og afkrydsningsfeltet **Modtagermoms** er markeret.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="3b0e5-164">Modtagermoms på en købsfaktura</span><span class="sxs-lookup"><span data-stu-id="3b0e5-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="3b0e5-165">For køb under modtagermomsskemaet skal den køber, der modtager fakturaen med modtagermoms, fungere som køber og sælger i momsregnskabsmæssig sammenhæng.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="3b0e5-166">Når en købsfaktura med modtagermoms bogføres, oprettes der to momsposteringer.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="3b0e5-167">Den ene postering har momsretningen **Indgående moms**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="3b0e5-168">Den anden postering har momsretningen **Udgående moms**, og afkrydsningsfeltet **Modtagermoms** er markeret.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="3b0e5-169">På følgende skærmbillede har den ene transaktion retningen **Indgående moms** og den anden transaktion har retningen **Udgående moms**.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![Bogført moms](media/apac-sau-posted-sales-tax.png)
