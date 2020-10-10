---
title: Sikkerhedsmargener
description: Dette emne beskriver, hvordan sikkerhedsmargener kan bruges sammen med tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
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
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8ab5f1c3cdfa990a73951ddc5a7469644954d5c2
ms.sourcegitcommit: 646a0e7c8b8a7f2d00a50eddfa65500d0f8afbaf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814894"
---
# <a name="safety-margins"></a><span data-ttu-id="5f642-103">Sikkerhedsmargener</span><span class="sxs-lookup"><span data-stu-id="5f642-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f642-104">Dette emne beskriver, hvordan sikkerhedsmargener kan bruges sammen med tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5f642-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="5f642-105">Oversigt over sikkerhedsmargener</span><span class="sxs-lookup"><span data-stu-id="5f642-105">Safety margins overview</span></span>

<span data-ttu-id="5f642-106">Formålet med sikkerhedsmargener er at aktivere en opsætning, der giver en vis buffertid ud over den normale gennemløbstid.</span><span class="sxs-lookup"><span data-stu-id="5f642-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="5f642-107">Når materialerne f.eks. skal pakkes ud eller inspiceres, efter at de er modtaget fra leverandøren, kan du ikke bare lægge den ekstra tid til indkøbets leveringstid, da denne fremgangsmåde giver den ekstra buffertid til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="5f642-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="5f642-108">I dette eksempel kan modtagelsesmargenen bruges til at sikre, at leverandøren leverer tidligere.</span><span class="sxs-lookup"><span data-stu-id="5f642-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="5f642-109">Denne fremgangsmåde giver buffertid, så varerne kan håndteres internt.</span><span class="sxs-lookup"><span data-stu-id="5f642-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="5f642-110">Der er tre typer sikkerhedsmargener:</span><span class="sxs-lookup"><span data-stu-id="5f642-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="5f642-111">**Bestillingsmargen** – Buffertiden for afgivelse af forsyningsordren</span><span class="sxs-lookup"><span data-stu-id="5f642-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="5f642-112">**Modtagelsesmargen** – Buffertiden for håndtering af indgående forsyning</span><span class="sxs-lookup"><span data-stu-id="5f642-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="5f642-113">**Afgangsmargen** – Buffertiden for ekspedition af forsendelser</span><span class="sxs-lookup"><span data-stu-id="5f642-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="5f642-114">I følgende illustration vises, hvordan disse sikkerhedsmargener anvendes over tid.</span><span class="sxs-lookup"><span data-stu-id="5f642-114">The following illustration shows how these safety margins apply over time.</span></span>

![Sikkerhedsmargener](media/safety-margins-1.png)

<span data-ttu-id="5f642-116">Alle margener defineres i dage.</span><span class="sxs-lookup"><span data-stu-id="5f642-116">All margins are defined in days.</span></span> <span data-ttu-id="5f642-117">Standardværdieb på *0* (nul) angiver, at ingen standardmargen bruges.</span><span class="sxs-lookup"><span data-stu-id="5f642-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="5f642-118">Hvis du konfigurerer flere margener, vil de alle blive føjet til den samlede tid fra forsyningens *ordredato* til *behovsdatoen*.</span><span class="sxs-lookup"><span data-stu-id="5f642-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="5f642-119">En opsætning har f.eks. ikke en leveringstid, og alle tre margentyper er angivet til én dag.</span><span class="sxs-lookup"><span data-stu-id="5f642-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="5f642-120">I dette tilfælde vil der være tre dage mellem forsyningens ordredato og behovsdatoen, så hvis ordredatoen er 1. juli, vil behovsdatoen være den 4.</span><span class="sxs-lookup"><span data-stu-id="5f642-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="5f642-121">Modtagelsesmargen</span><span class="sxs-lookup"><span data-stu-id="5f642-121">Receipt margin</span></span>

<span data-ttu-id="5f642-122">Modtagelsesmargen er sandsynligvis den mest anvendte af de tre sikkerhedsmargener.</span><span class="sxs-lookup"><span data-stu-id="5f642-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="5f642-123">Den anvendes på *leveringsdatoen* og bagud fra *behovsdatoen*.</span><span class="sxs-lookup"><span data-stu-id="5f642-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="5f642-124">Produkterne bør med andre ord modtages i det angivne antal dage inden for modtagelsesmargen, før de er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="5f642-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="5f642-125">I følgende illustration fremhæves modtagelsesmargenen.</span><span class="sxs-lookup"><span data-stu-id="5f642-125">The following illustration highlights the receipt margin.</span></span>

![Modtagelsesmargen](media/safety-margins-2.png)

<span data-ttu-id="5f642-127">Modtagelsesmargenen bruges typisk som en buffer til at sikre tid nok til lagerregistrering eller andre tidskrævende processer, der ikke medtages som en del af den generelle leveringstid i systemet.</span><span class="sxs-lookup"><span data-stu-id="5f642-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="5f642-128">I forbindelse med indkøb er det en fordel, at *leveringsdatoen* for indkøbsordren flyttes tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="5f642-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="5f642-129">Hvis du øger leveringstiden i stedet for at bruge en sikkerhedsmargen, bliver leverandøren stadig bedt om at levere i sidste øjeblik.</span><span class="sxs-lookup"><span data-stu-id="5f642-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="5f642-130">Bemærk, at modtagelsesmargenen ikke ændrer *behovsdatoen* for forsyningen.</span><span class="sxs-lookup"><span data-stu-id="5f642-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="5f642-131">Derfor er modtagelsesmargenen ikke direkte synlig, når behovsdatoer for udbud og efterspørgsel sammenlignes (f.eks. på siden **Nettobehov**).</span><span class="sxs-lookup"><span data-stu-id="5f642-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="5f642-132">Hvis modtagelsesmargenen f.eks. er angivet til fire dage, og en indkøbsordrelinje er planlagt til modtagelse den 15. i måneden, beregner behovsplanlægningen den justerede modtagelsesdato som den 19. i måneden.</span><span class="sxs-lookup"><span data-stu-id="5f642-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="5f642-133">Bemærk, at der ikke anvendes modtagelsesmargen, når der bruges en disponibel lagerbeholdning som forsyning.</span><span class="sxs-lookup"><span data-stu-id="5f642-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="5f642-134">Alle disponible lagerbeholdninger antages at være til rådighed med det samme, uanset hvornår den faktisk blev modtaget.</span><span class="sxs-lookup"><span data-stu-id="5f642-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="5f642-135">Bestillingsmargen</span><span class="sxs-lookup"><span data-stu-id="5f642-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="5f642-136">**Kommer snart:** Denne funktion understøttes endnu ikke for planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="5f642-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="5f642-137">Indtil den understøttes, behandles alle de værdier, der er angivet for **Bestillingsmargen tilføjet til varens leveringstid**, som *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="5f642-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="5f642-138">I følgende illustration fremhæves bestillingsmargen.</span><span class="sxs-lookup"><span data-stu-id="5f642-138">The following illustration highlights the reorder margin.</span></span>

![Bestillingsmargen](media/safety-margins-3.png)

<span data-ttu-id="5f642-140">Bestillingsmargen lægges til før varens leveringstid for alle ordreforslag under behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="5f642-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="5f642-141">Derfor sikrer den, at der er mere tid til at afgive en forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="5f642-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="5f642-142">Denne margen bruges typisk som en buffer til at sikre tid nok til godkendelsesprocesser eller andre interne processer, der er nødvendige i forbindelse med oprettelsen af forsyningsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f642-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="5f642-143">Bestillingsmargenen sættes mellem forsyningens *ordredato* og *startdato*.</span><span class="sxs-lookup"><span data-stu-id="5f642-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="5f642-144">Afgangsmargen</span><span class="sxs-lookup"><span data-stu-id="5f642-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="5f642-145">**Kommer snart:** Denne funktion understøttes endnu ikke for planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="5f642-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="5f642-146">Indtil den understøttes, behandles alle de værdier, der er angivet for **Afgangsmargen trukket fra behovsdato**, som *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="5f642-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="5f642-147">I følgende illustration fremhæves afgangsmargen.</span><span class="sxs-lookup"><span data-stu-id="5f642-147">The following illustration highlights the issue margin.</span></span>

![Afgangsmargen](media/safety-margins-4.png)

<span data-ttu-id="5f642-149">Afgangsmargenen trækkes fra behovsdatoen ved varedisponering.</span><span class="sxs-lookup"><span data-stu-id="5f642-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="5f642-150">Det er med til at sikre, at du har tid til at reagere på og afsende indgående behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f642-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="5f642-151">Denne margen bruges typisk som en buffer til at sikre tid til forsendelse og relaterede udgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="5f642-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="5f642-152">Bemærk, at de relaterede udbud og efterspørgselskrav ikke stemmer overens, når der anvendes en afgangsmargen.</span><span class="sxs-lookup"><span data-stu-id="5f642-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="5f642-153">De afviger i stedet med afgangsmargenen, fordi afgangsmargenen tilføjes mellem forsyningens *behovsdato* og efterspørgslens *behovsdato*.</span><span class="sxs-lookup"><span data-stu-id="5f642-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="5f642-154">Angive sikkerhedsmargener</span><span class="sxs-lookup"><span data-stu-id="5f642-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="5f642-155">Slå sikkerhedsmargener til i Funktionsstyring</span><span class="sxs-lookup"><span data-stu-id="5f642-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="5f642-156">Før du kan bruge denne funktion sammen med Planlægningsoptimering, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="5f642-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="5f642-157">Administratorer kan bruge området [Funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="5f642-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5f642-158">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5f642-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5f642-159">**Modul:** _Varedisponering_</span><span class="sxs-lookup"><span data-stu-id="5f642-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="5f642-160">**Funktionsnavn:** _Margener for planlægningsoptimering_</span><span class="sxs-lookup"><span data-stu-id="5f642-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="5f642-161">Definere sikkerhedsmargener</span><span class="sxs-lookup"><span data-stu-id="5f642-161">Define safety margins</span></span>

<span data-ttu-id="5f642-162">Sikkerhedsmargener har en fleksibel opsætning.</span><span class="sxs-lookup"><span data-stu-id="5f642-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="5f642-163">De kan angives for både *disponeringsgruppe* og *behovsplan*.</span><span class="sxs-lookup"><span data-stu-id="5f642-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="5f642-164">Det er vigtigt, at du forstår, at margenerne lægges sammen oven på hinanden.</span><span class="sxs-lookup"><span data-stu-id="5f642-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="5f642-165">En modtagelsesmargen på to dage i disponeringsgruppen og tre dage på behovsplanen vil f.eks. give en faktisk modtagelsesmargen på fem dage.</span><span class="sxs-lookup"><span data-stu-id="5f642-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="5f642-166">Muligheden for at angive margen på behovsplanen kan være nyttig, når du vil simulere længere leveringstider eller usikkerhed for en bestemt plan, men uden at påvirke den daglige planlægning.</span><span class="sxs-lookup"><span data-stu-id="5f642-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="5f642-167">Sikkerhedsmargener for disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="5f642-167">Coverage group safety margins</span></span>

<span data-ttu-id="5f642-168">Hvis du vil anvende en sikkerhedsmargen på en disponeringsgruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5f642-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="5f642-169">Gå til **Varedisponering \> Opsætning \> Disponeringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="5f642-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="5f642-170">Vælg den ønskede disponeringsgruppe i listeruden.</span><span class="sxs-lookup"><span data-stu-id="5f642-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="5f642-171">I sektionen **Sikkerhedsmargener i dage** i oversigtspanel **Andet** skal du bruge følgende felter til at angive de nødvendige sikkerhedsmargener (i dage):</span><span class="sxs-lookup"><span data-stu-id="5f642-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="5f642-172">Modtagelsesmargen lagt til behovsdato</span><span class="sxs-lookup"><span data-stu-id="5f642-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="5f642-173">Afgangsmargen trukket fra behovsdato</span><span class="sxs-lookup"><span data-stu-id="5f642-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="5f642-174">Bestillingsmargen tilføjet til varens leveringstid</span><span class="sxs-lookup"><span data-stu-id="5f642-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="5f642-175">Sikkerhedsmargener for behovsplan</span><span class="sxs-lookup"><span data-stu-id="5f642-175">Master plan safety margins</span></span>

<span data-ttu-id="5f642-176">Hvis du vil anvende en sikkerhedsmargen på en behovsplan, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5f642-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="5f642-177">Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="5f642-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="5f642-178">Vælg den ønskede behovsplan i listeruden.</span><span class="sxs-lookup"><span data-stu-id="5f642-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="5f642-179">I oversigtspanelet **Sikkerhedsmargener i dage** skal du bruge følgende felter til at angive de nødvendige sikkerhedsmargener (i dage):</span><span class="sxs-lookup"><span data-stu-id="5f642-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="5f642-180">Modtagelsesmargen lagt til behovsdato</span><span class="sxs-lookup"><span data-stu-id="5f642-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="5f642-181">Afgangsmargen trukket fra behovsdato</span><span class="sxs-lookup"><span data-stu-id="5f642-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="5f642-182">Bestillingsmargen tilføjet til varens leveringstid</span><span class="sxs-lookup"><span data-stu-id="5f642-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="5f642-183">Angive, om beregninger er baseret på kalenderdage eller arbejdsdage</span><span class="sxs-lookup"><span data-stu-id="5f642-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="5f642-184">Du kan angive alle sikkerhedsmargener, så de beregnes på basis af enten kalenderdage eller arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="5f642-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="5f642-185">Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="5f642-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="5f642-186">Under fanen **Generelt** skal du i afsnittet **Sikkerhedsmargener i dage** angive indstillingen **Arbejdsdage** til *Ja* for at beregne margener baseret på arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="5f642-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="5f642-187">Angiv indstillingen til *Nej* for at beregne margener baseret på kalenderdage.</span><span class="sxs-lookup"><span data-stu-id="5f642-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="5f642-188">En kalender kan f.eks. være åben fra mandag til fredag og være lukket lørdag og søndag.</span><span class="sxs-lookup"><span data-stu-id="5f642-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="5f642-189">Hvis der er en modtagelsesmargen på én dag, opretter en behovsdato på en mandag en leveringsdato på den forrige fredag, fordi lørdag og søndag ikke er arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="5f642-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="5f642-190">Den kalender, der bruges til at bestemme arbejdsdage, afhænger af opsætningen og forsyningstypen.</span><span class="sxs-lookup"><span data-stu-id="5f642-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="5f642-191">Den kan styres af kalenderne i disponeringsgruppen, lagerstedet og leverandøren.</span><span class="sxs-lookup"><span data-stu-id="5f642-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="5f642-192">Hvis *lagerstedet* ikke indgår i disponeringsdimensionen (dvs. planlægningen kun er baseret på *lokationen*), bruges lagerstedskalenderen ikke.</span><span class="sxs-lookup"><span data-stu-id="5f642-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="5f642-193">Systemet kan håndtere en opsætning, hvor der er defineret en eller flere kalendere.</span><span class="sxs-lookup"><span data-stu-id="5f642-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="5f642-194">I følgende underafsnit beskrives de mulige kombinationer, der kan bruges til at kontrollere resultatet.</span><span class="sxs-lookup"><span data-stu-id="5f642-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="5f642-195">Kalender, der bruges til varigheden</span><span class="sxs-lookup"><span data-stu-id="5f642-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="5f642-196">De definerede kalendere styrer den faktiske samlede leveringstid i kalenderdage fra forsyningsordredatoen til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f642-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="5f642-197">Følgende kalenderprioritering bruges:</span><span class="sxs-lookup"><span data-stu-id="5f642-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="5f642-198">**Leveringstid for indkøb** – Det er kun disponeringsgruppekalenderen, der tages i betragtning.</span><span class="sxs-lookup"><span data-stu-id="5f642-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="5f642-199">**Modtagelsesmargen** – Der bruges en disponeringsgruppekalender, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-200">Ellers bruges lagerstedskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="5f642-201">**Afgangsmargen** – Der bruges en disponeringsgruppekalender, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-202">Ellers bruges lagerstedskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="5f642-203">**Ordremargen** – Det er kun disponeringsgruppekalenderen, der tages i betragtning.</span><span class="sxs-lookup"><span data-stu-id="5f642-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="5f642-204">Kalender, der bruges til slutdatoen</span><span class="sxs-lookup"><span data-stu-id="5f642-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="5f642-205">Følgende regler bruges til at bestemme, om planlægningsprogrammet kan bruge en bestemt dato for en given datotype:</span><span class="sxs-lookup"><span data-stu-id="5f642-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="5f642-206">**Modtagelsesdato for indkøb** – Leverandørkalenderen bruges, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-207">Ellers bruges disponeringsgruppekalenderen, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-208">Hvis ingen af disse kalendere er defineret, bruges lagerstedskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="5f642-209">**Modtagelsesdato for flytteordre** – Der bruges en disponeringsgruppekalender, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-210">Ellers bruges lagerstedskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="5f642-211">**Modtagelsesdato for produktion** – Der bruges en disponeringsgruppekalender, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-212">Ellers bruges lagerstedskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="5f642-213">**Åbningsdag for behovsafgang** – Der bruges en lagerstedskalender, hvis den er defineret.</span><span class="sxs-lookup"><span data-stu-id="5f642-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="5f642-214">Ellers bruges disponeringsgruppekalenderen.</span><span class="sxs-lookup"><span data-stu-id="5f642-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="5f642-215">**Åbningsdag for ordre** – En kombination (skæringspunkt) af disponeringsgruppekalenderen og leverandørkalenderen bruges.</span><span class="sxs-lookup"><span data-stu-id="5f642-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="5f642-216">Begge kalendere skal være åbne for at kunne bruge datoen.</span><span class="sxs-lookup"><span data-stu-id="5f642-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="5f642-217">Hvis kun en af disse kalendere er defineret, bruges kalenderen alene.</span><span class="sxs-lookup"><span data-stu-id="5f642-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="5f642-218">Oversigtsmatrix for kalenderopsætning</span><span class="sxs-lookup"><span data-stu-id="5f642-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="5f642-219">I følgende illustration vises en matrix, der opsummerer, hvilke kalendere der anvendes, når der beregnes sikkerhedsmargener.</span><span class="sxs-lookup"><span data-stu-id="5f642-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="5f642-220">(Vælg billedet for at åbne en version af det med høj opløsning). Følgende forkortelser og farver bruges til at angive, hvor de enkelte typer kalendere er specificeret:</span><span class="sxs-lookup"><span data-stu-id="5f642-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="5f642-221">**Disponeringsgruppe (CG):** grøn</span><span class="sxs-lookup"><span data-stu-id="5f642-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="5f642-222">**Lagersted (WH):** gul</span><span class="sxs-lookup"><span data-stu-id="5f642-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="5f642-223">**Leverandør (V):** blå</span><span class="sxs-lookup"><span data-stu-id="5f642-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="5f642-224">[![Oversigtsmatrix for kalenderopsætning](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="5f642-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="5f642-225">Beregning af forsinkelser</span><span class="sxs-lookup"><span data-stu-id="5f642-225">Calculating delays</span></span>

<span data-ttu-id="5f642-226">Alle tre typer sikkerhedsmargener medtages, når systemet bestemmer, om en ordre er forsinket.</span><span class="sxs-lookup"><span data-stu-id="5f642-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="5f642-227">En vare har f.eks. en leveringstid på én dag og en modtagelsesmargen på tre dage.</span><span class="sxs-lookup"><span data-stu-id="5f642-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="5f642-228">En salgsordre for denne vare angives som påkrævet i dag.</span><span class="sxs-lookup"><span data-stu-id="5f642-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="5f642-229">I dette tilfælde beregnes forsinkelsen som *leveringstid* + *modtagelsesmargen* = fire dage.</span><span class="sxs-lookup"><span data-stu-id="5f642-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="5f642-230">Hvis dags dato f.eks. er 14. august, skaber de fire dages forsinkelse en levering den 18. august.</span><span class="sxs-lookup"><span data-stu-id="5f642-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="5f642-231">Følgende illustration viser dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="5f642-231">The following illustration shows this example.</span></span>

![Eksempelberegning af forsinkelse](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="5f642-233">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5f642-233">Additional resources</span></span>

[<span data-ttu-id="5f642-234">Kom i gang med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="5f642-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5f642-235">Analyse af tilpasning af planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="5f642-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
