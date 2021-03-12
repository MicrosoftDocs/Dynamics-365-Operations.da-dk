---
title: Fastlægge fælles værdier til styring af tekniske ændringer
description: Dette emne beskriver, hvordan du kan oprette fælles værdier, der bruges til parametre i forskellige dele af styring af tekniske ændringer.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425082"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="713f7-103">Fastlægge fælles værdier til styring af tekniske ændringer</span><span class="sxs-lookup"><span data-stu-id="713f7-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="713f7-104">Når du konfigurerer styring af tekniske ændringer, skal du oprette flere samlinger af værdier, der skal bruges til at udfylde rullelisterne i andre dele af brugergrænsefladen (UI).</span><span class="sxs-lookup"><span data-stu-id="713f7-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="713f7-105">Du skal angive disse værdier i henhold til de produkttyper, du producerer, og dine specifikke forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="713f7-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="713f7-106">Tekniske ændringskategorier</span><span class="sxs-lookup"><span data-stu-id="713f7-106">Engineering change categories</span></span>

<span data-ttu-id="713f7-107">Du kan bruge tekniske ændringskategorier til at organisere dine tekniske ændringsordrer, så de er nemmere at administrere og gennemgå.</span><span class="sxs-lookup"><span data-stu-id="713f7-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="713f7-108">Det kan f.eks. være nyttigt at oprette en arbejdsproces, hvor, afhængigt af kategorien, en bestemt afdeling skal gennemgå de foreslåede ændringer.</span><span class="sxs-lookup"><span data-stu-id="713f7-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="713f7-109">Den tekniske ændringsordre omfatter derfor et **Kategori**-felt.</span><span class="sxs-lookup"><span data-stu-id="713f7-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="713f7-110">Hvis du vil oprette en samling af tekniske ændringskategorier, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringskategorier**.</span><span class="sxs-lookup"><span data-stu-id="713f7-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="713f7-111">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="713f7-112">Tekniske ændringsprioriteter</span><span class="sxs-lookup"><span data-stu-id="713f7-112">Engineering change priorities</span></span>

<span data-ttu-id="713f7-113">Du kan bruge tekniske ændringsprioriteter til at angive vigtigheden eller prioriteten af en teknisk ændringsordre.</span><span class="sxs-lookup"><span data-stu-id="713f7-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="713f7-114">De kan hjælpe dig med at holde styr på vigtigheden af en teknisk ændringsordre, så du nemt kan identificere, hvilke ordrer der skal behandles først, og hvor hurtigt.</span><span class="sxs-lookup"><span data-stu-id="713f7-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="713f7-115">Hvis du vil oprette en samling af tekniske ændringsprioriteter, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringsprioriteter**.</span><span class="sxs-lookup"><span data-stu-id="713f7-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="713f7-116">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="713f7-117">Årsager til den tekniske ændring</span><span class="sxs-lookup"><span data-stu-id="713f7-117">Engineering change reasons</span></span>

<span data-ttu-id="713f7-118">Tekniske ændringsårsager angiver årsagen til eller arten af ændringen i ændringsordren.</span><span class="sxs-lookup"><span data-stu-id="713f7-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="713f7-119">Hvis du vil oprette en samling af tekniske ændringsårsager, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringsårsager**.</span><span class="sxs-lookup"><span data-stu-id="713f7-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="713f7-120">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="713f7-121">Koder for afskaffelse af materiale</span><span class="sxs-lookup"><span data-stu-id="713f7-121">Material disposal codes</span></span>

<span data-ttu-id="713f7-122">Du kan bruge materialekassationskoder til at kategorisere materialer, der bruges i færdigvarerne, eller komponenter, der skal kasseres på en bestemt måde eller kræver en vis håndtering, før de flyttes til den almindelige papirkurv.</span><span class="sxs-lookup"><span data-stu-id="713f7-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="713f7-123">Når du føjer et relevant produkt til en teknisk ændringsordre, kan du tildele en kassationskode som en del af ændringsoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="713f7-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="713f7-124">Hvis du vil oprette en samling af materialekassationskoder, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Materialekassationskoder**.</span><span class="sxs-lookup"><span data-stu-id="713f7-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="713f7-125">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="713f7-126">Modtagne kundegodkendelser</span><span class="sxs-lookup"><span data-stu-id="713f7-126">Received customer approval</span></span>

<span data-ttu-id="713f7-127">Når du designer produkter til en bestemt kunde, skal designet og specifikationerne ofte valideres, før produktet kan angives som klar.</span><span class="sxs-lookup"><span data-stu-id="713f7-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="713f7-128">Feltet **Modtaget kundegodkendelse** giver dig mulighed for at angive, hvor langt i kundegodkendelsesprocessen produktet er, og/eller om godkendelsen er modtaget.</span><span class="sxs-lookup"><span data-stu-id="713f7-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="713f7-129">Hvis du vil oprette en samling af værdier for modtaget kundegodkendelse, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Modtaget kundegodkendelse**.</span><span class="sxs-lookup"><span data-stu-id="713f7-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="713f7-130">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="713f7-131">Teknisk ændring – Miljømæssige tilstands- og sikkerhedskoder</span><span class="sxs-lookup"><span data-stu-id="713f7-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="713f7-132">Hvis der skal tages hensyn til standardmiljøets tilstands- og sikkerhedsforskrifter eller firmaspecifikke forordninger eller procedurer i fremstillingen af et produkt, kan du bruge miljøets tilstands- og sikkerhedskoder til at definere dem.</span><span class="sxs-lookup"><span data-stu-id="713f7-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="713f7-133">I den tekniske ændringsordre kan du angive, hvilke koder der gælder for fremstillingen af et produkt, mens du redigerer oplysningerne om det berørte produkt.</span><span class="sxs-lookup"><span data-stu-id="713f7-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="713f7-134">Hvis du vil oprette en samling af sundheds- og sikkerhedsværdier, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Teknisk ændring - Miljømæssige tilstands- og sikkerhedskoder**.</span><span class="sxs-lookup"><span data-stu-id="713f7-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="713f7-135">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="713f7-136">Tekniske ændrings alvorsgrad</span><span class="sxs-lookup"><span data-stu-id="713f7-136">Engineering change severities</span></span>

<span data-ttu-id="713f7-137">Du kan bruge tekniske ændringers alvorsgrader til at angive det niveau af virkninger, der gælder for produkterne i en teknisk ændringsordre.</span><span class="sxs-lookup"><span data-stu-id="713f7-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="713f7-138">Hvis du vil oprette en samling af tekniske ændringers alvorsgrader, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringers alvorsgrader**.</span><span class="sxs-lookup"><span data-stu-id="713f7-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="713f7-139">Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.</span><span class="sxs-lookup"><span data-stu-id="713f7-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="713f7-140">Du kan oprette regler, der gælder for hvert af de niveauer af alvorsgrad, du opretter.</span><span class="sxs-lookup"><span data-stu-id="713f7-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="713f7-141">Du kan finde flere oplysninger om, hvordan du tildeler disse regler, i næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="713f7-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="713f7-142">Regelsæt for alvorsgraden af den tekniske ændring</span><span class="sxs-lookup"><span data-stu-id="713f7-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="713f7-143">Du kan bruge de tekniske ændringers regelsæt for alvorsgrad til at oprette en gruppe regler, som du bruger til automatisk at beregne alvorsgraden af ændringsordren, baseret på typen af ændringer i de berørte produkter.</span><span class="sxs-lookup"><span data-stu-id="713f7-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="713f7-144">Hvis du vil bruge regler for alvorsgraden, skal du åbne siden **Parametre for styring af tekniske ændringer** og angive feltet **Regel for alvorsgrad** til *Beregn* eller *Beregn automatisk*.</span><span class="sxs-lookup"><span data-stu-id="713f7-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="713f7-145">Når systemet evaluerer alvorsgraden, behandler det reglerne i den rækkefølge, som de vises på siden, oppefra og ned.</span><span class="sxs-lookup"><span data-stu-id="713f7-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="713f7-146">For at en regel kan vælges og få dens prioritet fastlagt skal alle reglerne i et regelsæt opfyldes.</span><span class="sxs-lookup"><span data-stu-id="713f7-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="713f7-147">Hvis du vil oprette de regler, der gælder for hver enkelt ændrings niveau af alvorsgrad, du har defineret, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringers regelsæt for alvorsgrad**.</span><span class="sxs-lookup"><span data-stu-id="713f7-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="713f7-148">Udfør derefter ét af følgende trin.</span><span class="sxs-lookup"><span data-stu-id="713f7-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="713f7-149">Hvis du vil oprette et nyt regelsæt, skal du vælge **Nyt** i handlingsruden og derefter angive felterne som beskrevet senere i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="713f7-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="713f7-150">Hvis du vil redigere et eksisterende regelsæt, skal du vælge det i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet senere i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="713f7-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="713f7-151">Hvis du vil slette et eksisterende regelsæt, skal du vælge det i listeruden og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="713f7-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="713f7-152">Hvis du vil omarrangere listen med regelsæt, skal du vælge et regelsæt i listeruden og derefter bruge knapperne **Op** og **Ned** i handlingsruden til at flytte det.</span><span class="sxs-lookup"><span data-stu-id="713f7-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="713f7-153">For hvert regelsæt skal du angive følgende felt:</span><span class="sxs-lookup"><span data-stu-id="713f7-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="713f7-154">**Alvorsgrad** – Vælg det niveau af alvorsgrad, der skal oprettes regler for.</span><span class="sxs-lookup"><span data-stu-id="713f7-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="713f7-155">Du kan bruge siden **Tekniske ændringers alvorsgrader** til at oprette og navngive niveauerne.</span><span class="sxs-lookup"><span data-stu-id="713f7-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="713f7-156">(Se det forrige afsnit for at få flere oplysninger).</span><span class="sxs-lookup"><span data-stu-id="713f7-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="713f7-157">Brug knapperne i oversigtspanelet **Regler** til at tilføje eller fjerne en regel for den aktuelle indstilling af alvorsgrad.</span><span class="sxs-lookup"><span data-stu-id="713f7-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="713f7-158">Hver regel har et **Regel**-felt og et **Navn**-felt.</span><span class="sxs-lookup"><span data-stu-id="713f7-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="713f7-159">Reglerne oprettes af systemet og angiver de typer af ændringer, et produkt kan have.</span><span class="sxs-lookup"><span data-stu-id="713f7-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="713f7-160">Navnet angiver ændringstypen.</span><span class="sxs-lookup"><span data-stu-id="713f7-160">The name indicates the type of change.</span></span>