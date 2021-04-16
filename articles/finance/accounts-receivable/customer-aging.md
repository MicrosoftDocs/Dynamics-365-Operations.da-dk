---
title: Aldersfordelt saldoliste for kunder
description: I rapporten Aldersfordelt saldoliste for kunder vises de saldi, som forfalder fra kunder, der er sorteret efter datointerval eller forældelsesperiode.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b80345513d355115a182c108bf3843963e9a59d9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840335"
---
# <a name="customer-aging-report"></a><span data-ttu-id="2bb9d-103">Aldersfordelt saldoliste for kunder</span><span class="sxs-lookup"><span data-stu-id="2bb9d-103">Customer aging report</span></span> 

<span data-ttu-id="2bb9d-104">I rapporten **Aldersfordelt saldoliste for kunder** vises de saldi, som forfalder fra kunder, der er sorteret efter datointerval eller forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="2bb9d-105">Når du opretter denne rapport, vises følgende standardparametre.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="2bb9d-106">Du kan bruge disse parametre til at filtrere de data, der vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="2bb9d-107">Du kan finde flere oplysninger under [Konfigurere rykkere](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="2bb9d-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bb9d-108">Felt</span><span class="sxs-lookup"><span data-stu-id="2bb9d-108">Field</span></span></p></th>
<th><p><span data-ttu-id="2bb9d-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2bb9d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-110"><strong>Faktureringsklassifikation</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-111">Vælg en eller flere faktureringsklassifikationer, der skal medtages i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="2bb9d-112">**Bemærk:** Dette kontrolelement er kun tilgængeligt, hvis konfigurationsnøglen <STRONG>Offentlig sektor</STRONG> er valgt.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-113"><strong>Medtag transaktioner uden en faktureringsklassifikation</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-114">Hvis dette afkrydsningsfelt er markeret, bliver alle de posteringer, der ikke har nogen tilknyttet faktureringsklassifikation, vist i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="2bb9d-115">**Bemærk:** Dette kontrolelement er kun tilgængeligt, hvis konfigurationsnøglen <STRONG>Offentlig sektor</STRONG> er valgt.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-116"><strong>Aldersfordeling pr.</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-117">Angiv den dato, der skal bruges på det aktuelle aldersfordelte filsæt.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-118"><strong>Saldo pr.</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-119">Angiv den dato, der skal vises debitorsaldi for.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="2bb9d-120">Dette kaldes skæringsdatoen for transaktioner.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-121"><strong>Igangsæt dato</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-122">Angiv en dato, der ligger i det første periodeinterval eller den første forældelsesperiode, der skal medtages i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-123"><strong>Afgrænsning</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-124">Vælg den type dato, rapporten skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="2bb9d-125"><strong>Posteringsdato</strong> – Posteringsdatoen for transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="2bb9d-126">Det kan f.eks. være en fakturadato, der danner basis for beregningen af forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="2bb9d-127"><strong>Forfaldsdato</strong> – Forfaldsdatoen for transaktionerne baseret på betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="2bb9d-128"><strong>Dokumentdato</strong> – En brugerdefineret dokumentdato, der ligger til grund for beregningen af forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-129"><strong>Definition på forældelsesperiode</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-130">Vælg en definition af forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-130">Select an aging period definition.</span></span> <span data-ttu-id="2bb9d-131">Feltet <strong>Interval</strong> bruges ikke, hvis du vælger en definition af forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="2bb9d-132">Der kan ikke bruges definitioner af forældelsesperioder, der har mere end seks forældelsesperioder, i den udskrevne rapport.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="2bb9d-133">**Bemærk:** Du kan konfigurere forældelsesperioder på siden <STRONG>Definitioner af forældelsesperioder</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-134"><strong>Udskriv beskrivelse af forældelsesperiode</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-135">Vælg <strong>Ja</strong> for at medtage beskrivelser af forældelsesperioder øverst i hver enkelt kolonne for en forældelsesperiode i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="2bb9d-136">Vælg <strong>Nej</strong> for at udskrive rapporten uden kolonneoverskrifter.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-137"><strong>Interval</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-138">Definer den periode, der skal bruges, ved at angive antallet af dagsenheder eller månedsenheder i hver periode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="2bb9d-139">Hvis du f.eks. vil have vist oplysninger om forældelse efter uge, skal du angive 7 i dette felt og vælge <strong>Dag</strong> i feltet <strong>Dag/måned</strong>.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="2bb9d-140">**Bemærk:** De oplysninger, du angiver i dette felt, bruges kun, hvis du ikke har valgt en definition for forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="2bb9d-141">Ellers defineres udskriftsretningen i definitionen af forældelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-142"><strong>Dag/md</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-143">Vælg enhed, enten <strong>Dag</strong> eller <strong>Måned</strong>, som skal bruges til at definere perioden, i feltet <strong>Interval</strong>.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-144"><strong>Udskriftsretning</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-145">Vælg, om saldi skal beregnes, og forældelsesrapporten skal udskrives for tidligere eller fremtidige perioder.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="2bb9d-146">Datoerne evalueres i forhold til den dato, der er valgt i feltet <strong>Saldo som på</strong>.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="2bb9d-147">Vælg <strong>Bagud</strong> for at få vist oplysninger om tidligere perioder.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="2bb9d-148">Vælg <strong>Fremad</strong> for at få vist oplysninger om fremtidige perioder.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="2bb9d-149">
  
<STRONG>Bemærk:</STRONG> De oplysninger, du angiver i dette felt, bruges kun, hvis du ikke har valgt en definition for forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-150"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-151">Vælg dette for at få vist posteringer, der er medregnet i de saldi, som vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-152"><strong>Medtag beløb i transaktionsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-153">Vælg dette for at inkludere beløb i transaktionsvalutaen ud over beløb i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="2bb9d-154">Hvis dette afkrydsningsfelt ikke er markeret, vises beløbene i rapporten kun i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-155"><strong>Negativ saldo</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-156">Vælg dette for at medtage debitorkonti, der har negative saldi.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb9d-157"><strong>Udeluk nul-saldo-konti</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-158">Vælg dette for at udelukke debitorkonti, der har en nul-saldo.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb9d-159"><strong>Betalingspositionering</strong></span><span class="sxs-lookup"><span data-stu-id="2bb9d-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb9d-160">Vælg dette for at få vist betalinger, der ikke er udlignet.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="2bb9d-161">Disse vises i den første kolonne i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2bb9d-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]