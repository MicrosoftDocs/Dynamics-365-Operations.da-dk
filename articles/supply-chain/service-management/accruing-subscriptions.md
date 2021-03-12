---
title: Periodisering af abonnementer
description: Med serviceabonnementer periodiserer du omsætning manuelt i de perioder, der kommer efter den dato, hvor du har faktureret en gebyrtransaktion.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0d6c25cc8a19f5ebea3477cd2c957876752fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966074"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="a5d74-103">Periodisering af abonnementer</span><span class="sxs-lookup"><span data-stu-id="a5d74-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a5d74-104">Med serviceabonnementer periodiserer du omsætning manuelt i de perioder, der kommer efter den dato, hvor du har faktureret en gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="a5d74-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="a5d74-105">Der oprettes periodiseringsperioder for den fakturaperiode, som du opretter til abonnementsgebyret. Periodiseringsperioderne er baseret på abonnementets periodekode.</span><span class="sxs-lookup"><span data-stu-id="a5d74-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="a5d74-106">Du kan periodisere og tilbageføre periodiseret omsætning.</span><span class="sxs-lookup"><span data-stu-id="a5d74-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="a5d74-107">Tilbageføre periodiseringer af kreditbeløb</span><span class="sxs-lookup"><span data-stu-id="a5d74-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="a5d74-108">Hvis du krediterer fakturerede abonnementsbeløb, er der to metoder, du kan bruge til at tilbageføre de periodiserede beløb:</span><span class="sxs-lookup"><span data-stu-id="a5d74-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="a5d74-109">Du kan tilbageføre hver enkelt postering for periodiseret omsætning individuelt, før du opretter kreditnotaforslaget til posteringen.</span><span class="sxs-lookup"><span data-stu-id="a5d74-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="a5d74-110">Dette er den manuelle fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="a5d74-110">This is the manual method.</span></span> <span data-ttu-id="a5d74-111">(manuel)</span><span class="sxs-lookup"><span data-stu-id="a5d74-111">(manual)</span></span>

  - <span data-ttu-id="a5d74-112">Du kan lade de periodiserede beløb tilbageføre på den dato, hvor kreditnotaen er bogført eller på den oprindelige bogføringsdato for periodiseringen.</span><span class="sxs-lookup"><span data-stu-id="a5d74-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="a5d74-113">Du kan finde flere oplysninger i [Abonnementsparametre (formular)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="a5d74-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="a5d74-114">Konfigurer behov</span><span class="sxs-lookup"><span data-stu-id="a5d74-114">Setup requirements</span></span>

<span data-ttu-id="a5d74-115">Hvis du vil periodisere omsætning, skal du sørge for, at følgende datakrav er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="a5d74-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="a5d74-116">Kontoopsætning</span><span class="sxs-lookup"><span data-stu-id="a5d74-116">Account setup</span></span>

<span data-ttu-id="a5d74-117">Kontiene **IGVA - Abonnement** og **Periodiseret omsætning - abonnement** skal være oprettet i modulet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="a5d74-118">Når du bogfører periodiseret omsætning, debiteres kontoen **IGVA - Abonnement** med det periodiserede beløb, mens kontoen **Periodiseret omsætning - abonnement** krediteres med det periodiserede beløb.</span><span class="sxs-lookup"><span data-stu-id="a5d74-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="a5d74-119">Oprette konti til periodisering af abonnementsindtægt</span><span class="sxs-lookup"><span data-stu-id="a5d74-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="a5d74-120">Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Bogføring** \> **Opsætning af finanskontering**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="a5d74-121">Klik på fanen **Omsætningskonti**, og vælg **IGVA - abonnement** eller **Periodiseret omsætning - abonnement** for at konfigurere kontiene.</span><span class="sxs-lookup"><span data-stu-id="a5d74-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="a5d74-122">Oprette abonnementsgrupper</span><span class="sxs-lookup"><span data-stu-id="a5d74-122">Subscription group setup</span></span>

<span data-ttu-id="a5d74-123">Hvis omsætning for abonnementer skal kunne periodiseres, skal afkrydsningsfeltet **Periodiser omsætning** være markeret.</span><span class="sxs-lookup"><span data-stu-id="a5d74-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="a5d74-124">Feltet findes i formularen **Abonnementsgrupper** for den gruppe, som er knyttet til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="a5d74-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="a5d74-125">Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="a5d74-126">Aktivere omsætningsperiodisering for en abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="a5d74-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="a5d74-127">Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="a5d74-128">Perioder</span><span class="sxs-lookup"><span data-stu-id="a5d74-128">Periods</span></span>

<span data-ttu-id="a5d74-129">Du skal oprette en periodekode til fakturering.</span><span class="sxs-lookup"><span data-stu-id="a5d74-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="a5d74-130">Medmindre du vil periodisere omsætning i de samme tidsperioder, som du bruger til fakturering, skal du også oprette en periodiseringsperiode.</span><span class="sxs-lookup"><span data-stu-id="a5d74-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="a5d74-131">I oversigten nedenfor kan du se, hvilke periodiseringsperioder du kan oprette til hver enkelt faktureringsperiode:</span><span class="sxs-lookup"><span data-stu-id="a5d74-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5d74-132">Faktureringstermin</span><span class="sxs-lookup"><span data-stu-id="a5d74-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="a5d74-133">Periodiseringsperiode</span><span class="sxs-lookup"><span data-stu-id="a5d74-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5d74-134"><strong>År</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a5d74-135"><strong>År</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-136"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-137"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-138"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5d74-139"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a5d74-140"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-141"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-142"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5d74-143"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a5d74-144"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="a5d74-145"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5d74-146"><strong>Uge</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a5d74-147"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5d74-148"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a5d74-149"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="a5d74-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5d74-150">Opsætning af faktureringsperioden er en obligatorisk del af den generelle opsætning af abonnementsgrupper.</span><span class="sxs-lookup"><span data-stu-id="a5d74-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="a5d74-151">Du kan bestemme, om der også skal oprettes en periodiseringsperiode for abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a5d74-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="a5d74-152">Hvis du opretter en periodiseringsgruppe til abonnementsgruppen, foreslås denne periode i feltet **Periodekode**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="a5d74-153">Feltet findes i formularen **Periodiser abonnementsindtægt**, når du periodiserer abonnementsindtægt.</span><span class="sxs-lookup"><span data-stu-id="a5d74-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="a5d74-154">Det er dog valgfrit, om du vil angive en periodiseringsperiode til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a5d74-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a5d74-155">Brug følgende sti til at åbne formularen <STRONG>Periodiser abonnementsindtægt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a5d74-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="a5d74-156">Klik på <STRONG>Servicestyring</STRONG> &gt; <STRONG>Periodisk</STRONG> &gt; <STRONG>Serviceabonnementer</STRONG> &gt; <STRONG>Periodiser abonnementsindtægt</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a5d74-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="a5d74-157">Poster</span><span class="sxs-lookup"><span data-stu-id="a5d74-157">Transactions</span></span>

<span data-ttu-id="a5d74-158">Du kan styre antallet af finansposteringer, der oprettes, når du bogfører periodiseret omsætning.</span><span class="sxs-lookup"><span data-stu-id="a5d74-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="a5d74-159">I forbindelse med abonnementer skal du definere, om finansposteringer skal oprettes som en total eller pr. linje.</span><span class="sxs-lookup"><span data-stu-id="a5d74-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="a5d74-160">Angive, hvor detaljerede bogføringsoplysninger der skal vises om periodiserede posteringer</span><span class="sxs-lookup"><span data-stu-id="a5d74-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="a5d74-161">Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="a5d74-162">Under fanen **Økonomisk** i feltet **Faktura** skal du vælge **Total** eller **Linje**.</span><span class="sxs-lookup"><span data-stu-id="a5d74-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="a5d74-163">Se også</span><span class="sxs-lookup"><span data-stu-id="a5d74-163">See also</span></span>

[<span data-ttu-id="a5d74-164">Periodiser abonnementsindtægt</span><span class="sxs-lookup"><span data-stu-id="a5d74-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


