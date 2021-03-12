---
title: Konfigurere regler for generel budgetreservation og reservationstyper
description: I dette emne beskrives, hvordan du kan konfigurere og redigere regler for generelle budgetreservationer og reservationstyper til den offentlige sektor.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN, BudgetReservationType_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: ec41dc28e9f833896e26f07f807c59f2423710ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978193"
---
# <a name="set-up-general-budget-reservation-rules-and-reservation-types"></a><span data-ttu-id="e9670-103">Konfigurere regler for generel budgetreservation og reservationstyper</span><span class="sxs-lookup"><span data-stu-id="e9670-103">Set up general budget reservation rules and reservation types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9670-104">Offentlige institutioner bruger ofte generelle budgetreservationer til at sætte budgetterede midler til side eller øremærke dem, så de ikke er tilgængelige til andre formål.</span><span class="sxs-lookup"><span data-stu-id="e9670-104">Public sector entities often use general budget reservations to set aside or earmark budgeted funds so that they aren't available for other purposes.</span></span> <span data-ttu-id="e9670-105">Hvis du vil bruge generelle budgetreservationer, skal du angive budgetregler, og du skal oprette mindst én generel budgetreservationstype.</span><span class="sxs-lookup"><span data-stu-id="e9670-105">To use general budget reservations, you must specify budgetary rules, and you must set up at least one general budget reservation type.</span></span>

> [!NOTE]
> <span data-ttu-id="e9670-106">Hvis din organisation er i Frankrig, bruger du forpligtelser i stedet for generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-106">If your organization is in France, you will use commitments instead of general budget reservations.</span></span>

<span data-ttu-id="e9670-107">Følgende illustration viser, hvordan du konfigurerer systemet til at bruge generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-107">The following illustration shows how to set up the system to use general budget reservations.</span></span> <span data-ttu-id="e9670-108">Hvert nummereret trin svarer til et afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="e9670-108">Each numbered step corresponds to a section of this topic.</span></span>

<span data-ttu-id="e9670-109">![Opsætning af generel budgetreservation](media/gbr-rules-reservations-process.jpg "Opsætning af generel budgetreservation")</span><span class="sxs-lookup"><span data-stu-id="e9670-109">![Setup for general budget reservation](media/gbr-rules-reservations-process.jpg "Setup for general budget reservation")</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e9670-110">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e9670-110">Prerequisites</span></span>

<span data-ttu-id="e9670-111">Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.</span><span class="sxs-lookup"><span data-stu-id="e9670-111">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e9670-112">Kategori</span><span class="sxs-lookup"><span data-stu-id="e9670-112">Category</span></span></th>
<th><span data-ttu-id="e9670-113">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="e9670-113">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e9670-114">Relaterede konfigurationsopgaver</span><span class="sxs-lookup"><span data-stu-id="e9670-114">Related configuration tasks</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9670-115">Du skal bruge bogføringsdefinitioner, medmindre du ikke aktiverer rammeaftaler.</span><span class="sxs-lookup"><span data-stu-id="e9670-115">You must use posting definitions, unless you don't activate commitment accounting.</span></span></li>
<li><span data-ttu-id="e9670-116">Konfiguration af budgetstyring skal være aktiveret, budgetstyring skal være slået til, og et oprindeligt budget skal være bekræftet.</span><span class="sxs-lookup"><span data-stu-id="e9670-116">Budget control configuration must be activated, budget control must be turned on, and an original budget must be confirmed.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-budgeting-parameters-for-regulatory-accounting"></a><span data-ttu-id="e9670-117">Konfigurere budgetparametre for lovmæssig regnskabsførelse</span><span class="sxs-lookup"><span data-stu-id="e9670-117">Set up budgeting parameters for regulatory accounting</span></span>

<span data-ttu-id="e9670-118">Benyt følgende fremgangsmåde for at konfigurere budgetparametre for lovmæssig regnskabsførelse.</span><span class="sxs-lookup"><span data-stu-id="e9670-118">To set up budgeting parameters for regulatory accounting, follow these steps.</span></span>

1. <span data-ttu-id="e9670-119">Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="e9670-119">Go to **Budgeting \> Setup \> Basic budgeting \> Budgeting parameters**.</span></span>
2. <span data-ttu-id="e9670-120">Under fanen **Budget** på oversigtspanelet **Lovpligtig** skal du vælge **Ja** i indstillingen **Generelle budgetreservationer**.</span><span class="sxs-lookup"><span data-stu-id="e9670-120">On the **Budget** tab, on the **Regulatory** FastTab, set the **General budget reservations** option to **Yes**.</span></span>
3. <span data-ttu-id="e9670-121">Valgfrit: I oversigtspanelet **Behæftelseskontrol** kan du vælge **Ja** i indstillingerne **Forhindre stigninger i overført behæftelse** og **Brug sessionsdato til GBR-regnskab**.</span><span class="sxs-lookup"><span data-stu-id="e9670-121">Optional: On the **Encumbrance control** FastTab, set the **Prevent carry-forward encumbrance increases** and **Use session date for GBR accounting** options to **Yes**.</span></span>
4. <span data-ttu-id="e9670-122">Valgfrit: Vælg **Ja** i indstillingen **Tillad rettelser i tidligere år** i oversigtspanelet **Rettelser i tidligere år af generel budgetreservation**.</span><span class="sxs-lookup"><span data-stu-id="e9670-122">Optional: On the **General budget reservation prior year corrections** FastTab, set the **Allow prior year corrections** option to **Yes**.</span></span>

## <a name="select-source-documents-for-budget-control"></a><span data-ttu-id="e9670-123">Vælg kildedokumenter til budgetstyring</span><span class="sxs-lookup"><span data-stu-id="e9670-123">Select source documents for budget control</span></span>

<span data-ttu-id="e9670-124">Du kan øremærke budgetmidler til denne indkøbsmetode ved at konfigurere den generelle budgetreservation som et kildedokument.</span><span class="sxs-lookup"><span data-stu-id="e9670-124">To earmark budget funds for this purchasing method, configure the general budget reservation as a source document.</span></span> 

<span data-ttu-id="e9670-125">Benyt følgende fremgangsmåde for at vælge kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="e9670-125">To select source documents, follow these steps.</span></span>

1. <span data-ttu-id="e9670-126">Gå til **Budgettering \> Opsætning \> Budgetstyring \> Konfiguration af budgetstyring**.</span><span class="sxs-lookup"><span data-stu-id="e9670-126">Go to **Budgeting \> Setup \> Budget control \> Budget control configuration**.</span></span>
2. <span data-ttu-id="e9670-127">Vælg **Opret kladde**.</span><span class="sxs-lookup"><span data-stu-id="e9670-127">Select **Create draft**.</span></span>
3. <span data-ttu-id="e9670-128">Under fanen **Dokumenter og kladder** skal du markere afkrydsningsfelterne **Generel budgetreservation** og **Kontroller på linjepost**.</span><span class="sxs-lookup"><span data-stu-id="e9670-128">On the **Documents and journals** tab, select the **General budget reservation** and **Check at line entry** check boxes.</span></span>
4. <span data-ttu-id="e9670-129">Under fanen **Aktivér budgetstyring** skal du vælge **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="e9670-129">On the **Activate budget control** tab, select **Activate**.</span></span>

<span data-ttu-id="e9670-130">Når du opretter en generel budgetreservation, oprettes der også budgetkildesporingsposter og ledsagende budgetkontrolresultater, og der forekommer budgetkontrol, når du opretter en linje eller bogfører en reservation.</span><span class="sxs-lookup"><span data-stu-id="e9670-130">When you create a general budget reservation, budget source-tracking entries and accompanying budget-checking results are also created, and budget checking occurs when you create a line or post a reservation.</span></span>

## <a name="set-up-general-ledger-information-for-general-budget-reservations"></a><span data-ttu-id="e9670-131">Konfigurere finanskontioplysninger for generelle budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="e9670-131">Set up general ledger information for general budget reservations</span></span>

<span data-ttu-id="e9670-132">Som et led i at sikre, at finanskonti er angivet korrekt, skal du konfigurere, hvordan generelle budgetreservationer bruges til at registrere regnskabsmæssige forpligtelser.</span><span class="sxs-lookup"><span data-stu-id="e9670-132">To help guarantee that general ledger accounts are correct, you must configure how general budget reservations are used to record accounting commitments.</span></span>

<span data-ttu-id="e9670-133">Benyt følgende fremgangsmåde for at konfigurere finanskontioplysninger for generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-133">To set up general ledger information for general budget reservations, follow these steps.</span></span>

1. <span data-ttu-id="e9670-134">Gå til **Finans \> Opsætning Finans \> Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="e9670-134">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="e9670-135">Under fanen **Finans** i oversigtspanelet **Konteringsregler** skal du vælge **Ja** i indstillingen **Brug bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="e9670-135">On the **Ledger** tab, on the **Accounting rules** FastTab, set the **Use posting definitions** option to **Yes**.</span></span> <span data-ttu-id="e9670-136">Vælg **Ja** i den bekræftelsesmeddelelsesboks, der vises.</span><span class="sxs-lookup"><span data-stu-id="e9670-136">Then, in the confirmation message box that appears, select **Yes**.</span></span>
3. <span data-ttu-id="e9670-137">Marker afkrydsningsfeltet **Generelle budgetreservationer**.</span><span class="sxs-lookup"><span data-stu-id="e9670-137">Select the **General budget reservations** check box.</span></span> <span data-ttu-id="e9670-138">Luk derefter beskeden.</span><span class="sxs-lookup"><span data-stu-id="e9670-138">Then close the notification.</span></span>

    <span data-ttu-id="e9670-139">Når du markerer afkrydsningsfeltet **Generelle budgetreservationer**, markeres afkrydsningsfelterne **Aktiver behæftelse** og **Aktivér proces for budgetreservationer** automatisk og er ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="e9670-139">When you select the **General budget reservations** check box, the **Enable encumbrance process** and **Enable pre-encumbrance process** check boxes are automatically selected and aren't available.</span></span> <span data-ttu-id="e9670-140">Disse to processer skal bruges, når der anvendes generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-140">These two processes are required when general budget reservations are used.</span></span>

## <a name="create-posting-definitions"></a><span data-ttu-id="e9670-141">Oprette bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="e9670-141">Create posting definitions</span></span>

<span data-ttu-id="e9670-142">Du kan konfigurere posteringsbogføringsdefinitioner for at opdatere forskellige finanskonti for forskellige typer af generel budgetreservation.</span><span class="sxs-lookup"><span data-stu-id="e9670-142">You can configure transaction posting definitions to update different general ledger accounts for different types of general budget reservation.</span></span>

<span data-ttu-id="e9670-143">Benyt følgende fremgangsmåde for at oprette bogføringsdefinitioner for generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-143">To create posting definitions for general budget reservations, follow these steps.</span></span>

1. <span data-ttu-id="e9670-144">Gå til **Finans \> Opsætning af bogføring \> Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="e9670-144">Go to **General ledger \> Posting setup \> Posting definitions**.</span></span>
2. <span data-ttu-id="e9670-145">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e9670-145">Select **New**.</span></span>
3. <span data-ttu-id="e9670-146">I feltet **Bogføringsdefinition** skal du angive en kort kode for definitionen (f.eks. **GBREnc**).</span><span class="sxs-lookup"><span data-stu-id="e9670-146">In the **Posting definition** field, enter a brief code for the definition (for example, **GBREnc**).</span></span>
4. <span data-ttu-id="e9670-147">Indtast en beskrivelse (f.eks. **GBR-behæftelse**) i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e9670-147">In the **Description** field, enter a description (for example, **GBR encumbrance**).</span></span>
5. <span data-ttu-id="e9670-148">Vælg **Budgetreservation** i feltet **Modul**.</span><span class="sxs-lookup"><span data-stu-id="e9670-148">In the **Module** field, select **Budget reservation**.</span></span>
6. <span data-ttu-id="e9670-149">Angiv de resterende felter på siden efter behov.</span><span class="sxs-lookup"><span data-stu-id="e9670-149">Set the remaining fields on the page as you require.</span></span>
7. <span data-ttu-id="e9670-150">Vælg **Definitioner af posteringsbogføring** i gruppen **Vis** under fanen **Bogføringsdefinition** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9670-150">On the Action Pane, on the **Posting definition** tab, in the **View** group, select **Transaction posting definitions**.</span></span>
8. <span data-ttu-id="e9670-151">På siden **Definitioner af posteringsbogføring** under fanen **Budgetreservation** i feltgruppen **Vælg** er **Generel budgetreservation** valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="e9670-151">On the **Transaction posting definitions** page, on the **Budget reservation** tab, in the **Select** field group, **General budget reservation** is selected by default.</span></span> <span data-ttu-id="e9670-152">Vælg **Ultimo ved årsafslutning for generel budgetreservation**, hvis denne indstilling er relevant.</span><span class="sxs-lookup"><span data-stu-id="e9670-152">Select **General budget reservation year-end close** if this option is appropriate.</span></span>
9. <span data-ttu-id="e9670-153">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e9670-153">Select **New**.</span></span>
10. <span data-ttu-id="e9670-154">Vælg en af følgende værdier i feltet **Reservationstype**.</span><span class="sxs-lookup"><span data-stu-id="e9670-154">In the **Reservation type** field, select one of the following values:</span></span>

    - <span data-ttu-id="e9670-155">Hvis du vil angive en ny posteringsbogføringsdefinition, der gælder for alle reservationstyper, skal du vælge **Alle**.</span><span class="sxs-lookup"><span data-stu-id="e9670-155">To enter a new transaction posting definition that applies to all reservation types, select **All**.</span></span> <span data-ttu-id="e9670-156">I feltet **Bogføringsdefinition** skal du vælge den definition, som du oprettede tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="e9670-156">Then, in the **Posting definition** field, select the definition that you created earlier.</span></span>
    - <span data-ttu-id="e9670-157">Hvis du vil angive en ny posteringsbogføringsdefinition, der gælder for en enkelt reservationstype, skal du vælge **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e9670-157">To enter a new transaction posting definition that applies to a single reservation type, select **Table**.</span></span> <span data-ttu-id="e9670-158">Vælg derefter skal du vælge en reservationstype i feltet **Reservationstyperelation**.</span><span class="sxs-lookup"><span data-stu-id="e9670-158">Then, in the **Reservation type relation** field, select a reservation type.</span></span> <span data-ttu-id="e9670-159">I feltet **Bogføringsdefinition** skal du derefter vælge den definition, som du oprettede tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="e9670-159">In the **Posting definition** field, select the definition that you created earlier.</span></span>

11. <span data-ttu-id="e9670-160">Gentag trin 2-10 for at oprette så mange andre bogføringsdefinitioner, som du har brug for, og vælg derefter **Luk**.</span><span class="sxs-lookup"><span data-stu-id="e9670-160">Repeat steps 2 through 10 to create as many additional posting definitions as you require, and then select **Close**.</span></span>

## <a name="set-up-the-reservation-number-sequence"></a><span data-ttu-id="e9670-161">Konfigurere nummerserie for reservation</span><span class="sxs-lookup"><span data-stu-id="e9670-161">Set up the reservation number sequence</span></span>

<span data-ttu-id="e9670-162">Benyt følgende fremgangsmåde, hvis du vil konfigurere den nummerserie, som generelle budgetreservationer bruger.</span><span class="sxs-lookup"><span data-stu-id="e9670-162">To set up the number sequence that general budget reservations use, follow these steps.</span></span>

1. <span data-ttu-id="e9670-163">Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="e9670-163">Go to **Budgeting \> Setup \> Basic budgeting \> Budgeting parameters**.</span></span>
2. <span data-ttu-id="e9670-164">Vælg posten for generelle budgetreservationer i kolonnen **Reference** under fanen **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="e9670-164">On the **Number sequences** tab, in the **Reference** column, select the entry for general budget reservations.</span></span>
3. <span data-ttu-id="e9670-165">Vælg en kode i kolonnen **Nummerseriekode**.</span><span class="sxs-lookup"><span data-stu-id="e9670-165">In the **Number sequence code** column, select a code.</span></span>

    <span data-ttu-id="e9670-166">Du kan også tildele entydige nummerserier efter reservationstype.</span><span class="sxs-lookup"><span data-stu-id="e9670-166">You can also assign unique number sequences by reservation type.</span></span>

## <a name="create-a-general-budget-reservation-type"></a><span data-ttu-id="e9670-167">Oprette en generel budgetreservationstype</span><span class="sxs-lookup"><span data-stu-id="e9670-167">Create a general budget reservation type</span></span>

<span data-ttu-id="e9670-168">Reservationstypen bestemmer arten af en generel budgetreservation, f.eks. den type dokument, der eftergiver budgetreservation, den arbejdsgang, der bruges til at godkende reservationen, og den nummerserie, der bruges.</span><span class="sxs-lookup"><span data-stu-id="e9670-168">The reservation type determines the nature of a general budget reservation, such as the type of document that relieves the budget reservation, the workflow that is used to approve the reservation, and the number sequence that is used.</span></span>

<span data-ttu-id="e9670-169">Benyt følgende fremgangsmåde, hvis du vil oprette en generel budgetreservationstype.</span><span class="sxs-lookup"><span data-stu-id="e9670-169">To create a general budget reservation type, follow these steps.</span></span>

1. <span data-ttu-id="e9670-170">Gå til **Budgettering \> Opsætning \> Generelle budgetreservationer \> Reservationstype**.</span><span class="sxs-lookup"><span data-stu-id="e9670-170">Go to **Budgeting \> Setup \> General budget reservations \> Reservation type**.</span></span>
2. <span data-ttu-id="e9670-171">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e9670-171">Select **New**.</span></span>
3. <span data-ttu-id="e9670-172">Angiv et navn til reservationstypen i feltet **Reservationstype**.</span><span class="sxs-lookup"><span data-stu-id="e9670-172">In the **Reservation type** field, enter a name for the reservation type.</span></span>
4. <span data-ttu-id="e9670-173">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e9670-173">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e9670-174">I feltet **Eftergivelsesdokument** er **Indkøbsrekvisition** valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="e9670-174">In the **Relieving document** field, **Purchase requisition** is selected by default.</span></span> <span data-ttu-id="e9670-175">Vælg en anden værdi efter behov.</span><span class="sxs-lookup"><span data-stu-id="e9670-175">Select a different value as you require.</span></span> <span data-ttu-id="e9670-176">I dette felt angives den type dokument, der skal eftergive den generelle budgetreservation.</span><span class="sxs-lookup"><span data-stu-id="e9670-176">This field specifies the type of document that will relieve the general budget reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9670-177">Når du har oprettet en generel budgetreservation ved hjælp af reservationstypen, kan du ikke ændre reservationen til en anden type.</span><span class="sxs-lookup"><span data-stu-id="e9670-177">After you create a general budget reservation by using the reservation type, you can't change the reservation to another type.</span></span>

6. <span data-ttu-id="e9670-178">I oversigtspanelet **Overført budget** skal du vælge **Ja** i indstillingen **Reducer overført budget**, hvis resterende overførte budget, der er knyttet til en generel budgetreservation, skal reduceres til 0 (nul), når reservationen er færdig.</span><span class="sxs-lookup"><span data-stu-id="e9670-178">On the **Carry-forward budget** FastTab, set the **Reduce carry-forward budget** option to **Yes** if any remaining carry-forward budget that is associated with a general budget reservation should be reduced to 0 (zero) when the reservation is finalized.</span></span>
7. <span data-ttu-id="e9670-179">Valgfrit: Hvis der kræves en godkendelsesopgave eller en anden opgave, før reservationen kan bogføres, skal du vælge en arbejdsgang for generel budgetreservation i feltet **Arbejdsgang** i oversigtspanelet **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="e9670-179">Optional: If an approval task or other task is required before the reservation can be posted, on the **Workflow** FastTab, in the **Workflow** field, select a general budget reservation workflow.</span></span> <span data-ttu-id="e9670-180">Hvis du ikke udfylder dette felt, er en arbejdsgang ikke påkrævet for at kunne bogføre generelle budgetreservationer af denne type.</span><span class="sxs-lookup"><span data-stu-id="e9670-180">If you leave this field blank, a workflow isn't required in order to post general budget reservations of this type.</span></span>
8. <span data-ttu-id="e9670-181">Valgfrit: Hvis der er flere reservationstyper med entydige nummerserier, skal du vælge den nummerseriekode, som denne reservationstype skal bruge, i oversigtspanelet **Nummerserie** i feltet **Nummerseriekode**.</span><span class="sxs-lookup"><span data-stu-id="e9670-181">Optional: If different reservation types use unique number sequences, on the **Number sequence** FastTab, in the **Number sequence code** field, select the number sequence code that this reservation type should use.</span></span>

    <span data-ttu-id="e9670-182">Hvis der ikke er konfigureret en nummerserie til en reservationstype, bruges nummerserien for budgetparametre.</span><span class="sxs-lookup"><span data-stu-id="e9670-182">If a number sequence isn't configured for a reservation type, the budget parameters number sequence is used.</span></span>

9. <span data-ttu-id="e9670-183">Gentag trin 2-8 for at oprette evt. yderligere reservationstyper, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="e9670-183">Repeat steps 2 through 8 to create any additional reservations types that you require.</span></span>

## <a name="next-step"></a><span data-ttu-id="e9670-184">Næste trin</span><span class="sxs-lookup"><span data-stu-id="e9670-184">Next step</span></span>

<span data-ttu-id="e9670-185">Når du har oprettet regler, kan du oprette generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="e9670-185">After you've set up rules, you can create general budget reservations.</span></span> <span data-ttu-id="e9670-186">De generelle budgetreservationer gælder for de dokumenter, der er nødvendige for den indkøbsmetode, som du vælger (indkøbsrekvisition, indkøbsordre eller kreditorfaktura).</span><span class="sxs-lookup"><span data-stu-id="e9670-186">The reservations will apply to the documents that are required for the purchasing method that you select (purchase requisition, purchase order, or vendor invoice).</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="e9670-187">Tekniske oplysninger til systemadministratorer</span><span class="sxs-lookup"><span data-stu-id="e9670-187">Technical information for system administrators</span></span>

<span data-ttu-id="e9670-188">Hvis du ikke har adgang til de sider, der bruges til at fuldføre denne opgave, skal du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e9670-188">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

| <span data-ttu-id="e9670-189">Kategori</span><span class="sxs-lookup"><span data-stu-id="e9670-189">Category</span></span>                  | <span data-ttu-id="e9670-190">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="e9670-190">Prerequisite</span></span>                                                  |
|---------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e9670-191">Licenskonfigurationsnøgle</span><span class="sxs-lookup"><span data-stu-id="e9670-191">License configuration key</span></span> | <span data-ttu-id="e9670-192">Offentlig sektor \> Generel budgetreservation</span><span class="sxs-lookup"><span data-stu-id="e9670-192">Public sector \> General budget reservation</span></span>                   |
| <span data-ttu-id="e9670-193">Sikkerhedsroller</span><span class="sxs-lookup"><span data-stu-id="e9670-193">Security roles</span></span>            | <span data-ttu-id="e9670-194">Du skal være medlem af sikkerhedsrollen **Budgetchef**.</span><span class="sxs-lookup"><span data-stu-id="e9670-194">You must be a member of the **Budget manager** security role.</span></span> |
