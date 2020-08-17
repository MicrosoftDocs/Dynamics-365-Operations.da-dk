---
title: Forespørgsel på Schedule of Expenditures of Federal Awards
description: Dette emne giver oplysninger om forespørgslen Schedule of Expenditures of Federal Awards.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0b4228a9592efb54714186fc6b36276e915dc122
ms.sourcegitcommit: be51e892003778e71b67fb409a8e16965c89b5ac
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2020
ms.locfileid: "3618451"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cfcfe-103">Forespørgsel på Schedule of Expenditures of Federal Awards</span><span class="sxs-lookup"><span data-stu-id="cfcfe-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfcfe-104">Ifølge Office of Management og Budget Circular A-133 vil de agenturer, der modtager føderale midler, være underlagt revisionskrav, som også kaldes separate revisioner.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="cfcfe-105">Revisionsprocessen anvendes til at rapportere om indtægter og udgifter for føderale tilskud på tilbagevendende basis.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="cfcfe-106">En del af den separate revisionsrapport omfatter Schedule of Expenditures of Federal Awards (SEFA).</span><span class="sxs-lookup"><span data-stu-id="cfcfe-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="cfcfe-107">Forespørgslen Schedule of Expenditures of Federal Awards (SEFA) omfatter Catalog of Federal Domestic Assistance (CFDA) titel og nummer, tilskudsnummeret, tilskudsåret, navnet på den føderale myndighed, der udleverer midlerne, samt navnet på pass-through-enheden.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="cfcfe-108">Forespørgslen gælder for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="cfcfe-109">Denne periode er typisk den samme som regnskabsperioden, som er et regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="cfcfe-110">Forespørgslen omfatter tilskud, der har projektionsdatoer i det valgte datointerval.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="cfcfe-111">I forespørgselskolonnen **Udstederagentur** vises tilskudskunden eller udstederagenturet for et pass-through-tilskud.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="cfcfe-112">I forbindelse med et pass-through-tilskud viser kolonnen **Pass-through-agentur** tilskudskunden.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="cfcfe-113">Hvis det ikke er et pass-through-tilskud, er kolonnen **Pass-through-agentur** tom.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="cfcfe-114">Konfigurere CFDA-klynger</span><span class="sxs-lookup"><span data-stu-id="cfcfe-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="cfcfe-115">Du skal konfigurere de CFDA klynger, der kan knyttes til CFDA-numre i forespørgslen Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="cfcfe-116">Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Catalog of Federal Domestic Assistance-klynger**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="cfcfe-117">Vælg **Ny** for at oprette en CFDA-klynge.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="cfcfe-118">Angiv klyngens navn.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="cfcfe-119">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="cfcfe-120">Oprette CFDA-numre</span><span class="sxs-lookup"><span data-stu-id="cfcfe-120">Set up CFDA numbers</span></span>

<span data-ttu-id="cfcfe-121">Du skal konfigurere de CFDA-numre, der kan føjes til tiskud og medtages i forespørgslen Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="cfcfe-122">Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Catalog of Federal Domestic Assistance-numre**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="cfcfe-123">Vælg **Nyt** for at oprette et CFDA-nummer.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="cfcfe-124">Angiv CFDA-nummeret i feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="cfcfe-125">Tryk på **tabulatortasten**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="cfcfe-126">Angiv CFDA-titlen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="cfcfe-127">Tryk på **tabulatortasten**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="cfcfe-128">Valgfrit: Tilføj den relevante CFDA-klynge i feltet **Programklynge**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="cfcfe-129">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cfcfe-130">Konfigurere tilskud der skal indberettes for Schedule of Expenditures of Federal Awards-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="cfcfe-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="cfcfe-131">Gå til **Projektstyring og regnskab \> Tilskud \> Tilskud**, og vælg et eksisterende tilskud.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="cfcfe-132">Tildel CFDA nummeret i feltet **Catalog of Federal Domestic Assistance** i oversigtspanelet **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="cfcfe-133">CFDA nummeret på tilskuddet bestemmer CFDA-klyngen til rapportering.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="cfcfe-134">I oversigtspanelet **Kontaktoplysninger** skal du angive udstederoplysninger ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="cfcfe-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="cfcfe-135">Angiv den kunde, der er ansvarlig for tilskuddet, i feltet **Tilskudskunde**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="cfcfe-136">For et eksisterende tilskud kan disse oplysninger allerede være angivet.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="cfcfe-137">Angiv, om tilskudskunden er finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="cfcfe-138">Hvis tilskudskunden er finansieringskilde, skal du fjerne markeringen i afkrydsningsfeltet **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="cfcfe-139">Hvis en anden kunde er finansieringskilde, og tilskudskunden er ansvarlig for forbrug og sporing af penge, skal du markere afkrydsningsfeltet **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="cfcfe-140">Hvis du har markeret afkrydsningsfeltet **Pass-through** i det foregående trin, skal du angive den kunde, der har givet tilskuddet, i feltet **Udstederagentur**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="cfcfe-141">Udstederagenturet og tilskudskunden må ikke være den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="cfcfe-142">Her er et eksempel på et pass-through-tilskud:</span><span class="sxs-lookup"><span data-stu-id="cfcfe-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="cfcfe-143">Den føderale regering har finansieret et infrastrukturprojekt for en delstat.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="cfcfe-144">Den føderale regering gav pengene til delstatens forbrug.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="cfcfe-145">I dette tilfælde er den føderale regering udstederagenturet, og delstaten er tilskudskunden.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="cfcfe-146">Når du aktiverer funktionen første gang, vil de første CFDA-numre blive indsat ved hjælp af de eksisterende numre på tilskud.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="cfcfe-147">Udelade tilskud i SEFA-rapportering baseret på tilskudstypen</span><span class="sxs-lookup"><span data-stu-id="cfcfe-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="cfcfe-148">Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Tilskudstyper**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="cfcfe-149">I oversigtspanelet **Standardoplysninger** skal du markere afkrydsningsfeltet **Udelad i Schedule of Expenditures of Federal Awards**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="cfcfe-150">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cfcfe-151">Køre Schedule of Expenditures of Federal Awards-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="cfcfe-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="cfcfe-152">Gå til **Projektstyring og regnskab \> Forespørgsler og rapporter \> Tilskudsforespørgsel \> Schedule of Expenditures of Federal Awards**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="cfcfe-153">Benyt følgende fremgangsmåde i afsnittet **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="cfcfe-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="cfcfe-154">Vælg koden for datointervallet i feltet **Datointerval**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="cfcfe-155">Alternativt kan du i felterne **Fra dato** og **Til dato** definere datointervallet.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="cfcfe-156">Valgfrit: Hvis du kun vil medtage fakturerede posteringer som indtægt i forespørgslen, skal du angive indstillingen **Medtag kun fakturerede indtægter** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cfcfe-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="cfcfe-157">Søjler</span><span class="sxs-lookup"><span data-stu-id="cfcfe-157">Columns</span></span>

<span data-ttu-id="cfcfe-158">Schedule of Expenditures of Federal Awards-forespørgsler omfatter følgende kolonner:</span><span class="sxs-lookup"><span data-stu-id="cfcfe-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="cfcfe-159">Klyngenavn til Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="cfcfe-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="cfcfe-160">Tildelerbureau</span><span class="sxs-lookup"><span data-stu-id="cfcfe-160">Grantor agency</span></span>
- <span data-ttu-id="cfcfe-161">Gå gennem bureau</span><span class="sxs-lookup"><span data-stu-id="cfcfe-161">Pass-through agency</span></span>
- <span data-ttu-id="cfcfe-162">Tilskudsnavn</span><span class="sxs-lookup"><span data-stu-id="cfcfe-162">Grant name</span></span>
- <span data-ttu-id="cfcfe-163">Tilskuds-id</span><span class="sxs-lookup"><span data-stu-id="cfcfe-163">Grant ID</span></span>
- <span data-ttu-id="cfcfe-164">Id for tilskudsansøgning</span><span class="sxs-lookup"><span data-stu-id="cfcfe-164">Grant application ID</span></span>
- <span data-ttu-id="cfcfe-165">Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="cfcfe-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="cfcfe-166">Tilgange</span><span class="sxs-lookup"><span data-stu-id="cfcfe-166">Receipts</span></span>
- <span data-ttu-id="cfcfe-167">Udgifter</span><span class="sxs-lookup"><span data-stu-id="cfcfe-167">Expenditures</span></span>
