---
title: Manuelt oprettede arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer manuelt i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875566"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="73ba6-103">Manuelt oprettede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="73ba6-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="73ba6-104">Du kan oprette arbejdsordre manuelt på to måder:</span><span class="sxs-lookup"><span data-stu-id="73ba6-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="73ba6-105">i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**</span><span class="sxs-lookup"><span data-stu-id="73ba6-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="73ba6-106">i **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="73ba6-107">Opret arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="73ba6-107">Create work order</span></span>

1. <span data-ttu-id="73ba6-108">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="73ba6-109">Klik på knappen **Nyt**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-109">Click the **New** button.</span></span>

3. <span data-ttu-id="73ba6-110">Vælg en arbejdsordretype på rullelisten **Opret arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="73ba6-111">Vælg evt. en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="73ba6-111">If required, select a description.</span></span>

5. <span data-ttu-id="73ba6-112">Vælg aktivet for arbejdsordren samt en vedligeholdelsesjobtype.</span><span class="sxs-lookup"><span data-stu-id="73ba6-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="73ba6-113">Når du vælger et aktiv, er der som regel tre tilgængelige faner: Fanen **Mine aktiver** indeholder aktiver, der er relateret til de arbejdssteder, som du (den vedligeholdelsesarbejder, som er logget på systemet) kan allokeres til (konfigureres i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="73ba6-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="73ba6-114">Hvis der ikke er konfigureret noget arbejdssted for en arbejder i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md), er fanen **Mine aktiver** ikke synlig.</span><span class="sxs-lookup"><span data-stu-id="73ba6-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="73ba6-115">Fanen **Aktive aktiver** indeholder en liste over alle aktiver med status som "Aktiv" for aktivers livscyklus.</span><span class="sxs-lookup"><span data-stu-id="73ba6-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="73ba6-116">Fanen **Aktiv visning** viser en trævisning af arbejdssteder og aktiver, der er installeret på disse steder.</span><span class="sxs-lookup"><span data-stu-id="73ba6-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="73ba6-117">Vælg om nødvendigt **Vedligeholdelsesjobtypevariant** og **Fag**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="73ba6-118">Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="73ba6-119">Vælg de forventede start- og slutdatoer i de relaterede felter.</span><span class="sxs-lookup"><span data-stu-id="73ba6-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="73ba6-120">Klik på **OK** for at oprette en ny arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="73ba6-121">Rediger evt. arbejdsordren i **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="73ba6-122">I **Alle arbejdsordrer** kan du føje flere anlægsaktiver til en arbejdsordre i visningen Detaljer ved at tilføje linjer i oversigtspanelet **Vedligeholdelsesjob for arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="73ba6-123">I et anlægsaktiv kan du kun vælge de vedligeholdelsesjobtyper, der er defineret i den aktivtype, der er valgt for aktivet.</span><span class="sxs-lookup"><span data-stu-id="73ba6-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="73ba6-124">Hvis du har ændret et aktivs serviceniveau eller et aktiv kritisk, efter at du har brugt dem i en arbejdsordre (se [Serviceniveauer for aktiv](../setup-for-objects/object-priorities.md) og [Kritikaliteter for aktiver](../setup-for-objects/object-criticalities.md)), opdateres serviceniveauet eller kritikaliteten for arbejdsordren ikke tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="73ba6-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="73ba6-125">Kritikaliteten på en arbejdsordre genberegnes, hver gang en arbejdsordrelinje føjes til eller slettes fra arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="73ba6-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="73ba6-126">I detaljevisningen **Alle arbejdsordrer** > visningen **Hoved** > oversigtspanelet **Tidsplan** kan du vælge en ansvarlig medarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder i feltet **Ansvarlig gruppe** eller **Ansvarlig**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="73ba6-127">Disse indstillinger kan ændres, så længe arbejdsordren er aktiv, f.eks. når livscyklustilstanden for arbejdsordren ændres.</span><span class="sxs-lookup"><span data-stu-id="73ba6-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="73ba6-128">Det automatiske valg, der foretages under oprettelsen af en arbejdsordre, baseres på opsætningen af **Ansvarlige vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="73ba6-129">Hvis du tilføjer eller fjerner arbejdsordrejob, efter at du har oprettet en arbejdsordre, og feltet **Ansvarlig gruppe** og feltet **Ansvarlig** er tomme, når du opdaterer arbejdsordren, søger funktionen til administration af aktiver efter et muligt match i opsætningsformularen for en ansvarlig medarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="73ba6-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="73ba6-130">Hvis feltet **Ansvarlig gruppe** eller feltet **Ansvarlig** allerede er udfyldt, når du opdaterer arbejdsordren, foretages der ingen ændringer.</span><span class="sxs-lookup"><span data-stu-id="73ba6-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="73ba6-131">I **Vedligeholdelsesstatus** kan du foretage en beregning for at få en oversigt over arbejdsbyrder i forbindelse med indgående og fuldførte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="73ba6-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="73ba6-132">I oversigtspanelet **Linjedetaljer** kan du bruge felterne **Breddegrad** og **Længdegrad** til at tilføje geografiske koordinater for det aktiv, der er valgt i arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="73ba6-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="73ba6-133">Opret relateret arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="73ba6-133">Create related work order</span></span>

<span data-ttu-id="73ba6-134">Du kan oprette en relateret arbejdsordre til en eksisterende arbejdsordre, hvis du f.eks. vil arbejde med primære og sekundære arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="73ba6-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="73ba6-135">En ny arbejdsordre er baseret på et arbejdsordrejob fra en eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="73ba6-136">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="73ba6-137">Vælg den arbejdsordre, som du vil oprette en relateret arbejdsordre for.</span><span class="sxs-lookup"><span data-stu-id="73ba6-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="73ba6-138">Klik på **Relateret ordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="73ba6-139">I rulledialogboksen **Opret relateret arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette en relateret arbejdsordre for, i feltet **Arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="73ba6-140">Vælg en vedligeholdelsesjobtype feltet **Vedligeholdelsesjobtype** og, hvis det er nødvendigt, en relateret variant af vedligeholdelsesjobtypen og -faget i felterne **Vedligeholdelsesjobtypevariant** og **Fag**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="73ba6-141">Hvis dette er den første relaterede arbejdsordre, du opretter, skal du klikke på alternativknappen **Ny arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="73ba6-142">Vælg en **Arbejdsordretype** og en **Beskrivelse** i de relaterede felter.</span><span class="sxs-lookup"><span data-stu-id="73ba6-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="73ba6-143">Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="73ba6-144">Indsæt de forventede start- og slutdatoer i de relaterede felter.</span><span class="sxs-lookup"><span data-stu-id="73ba6-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="73ba6-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-145">Click **OK**.</span></span> <span data-ttu-id="73ba6-146">Den nye relaterede arbejdsordre vises på listen **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="73ba6-147">Hvis du opretter en relateret arbejdsordre på en arbejdsordre, der allerede har relaterede arbejdsordrer, kan du føje arbejdsordrejobbet til en allerede relateret arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="73ba6-148">Dette gøres ved at klikke på alternativknappen **Føj til relateret arbejdsordre** i trin 6.</span><span class="sxs-lookup"><span data-stu-id="73ba6-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="73ba6-149">Derefter skal du vælge den relaterede arbejdsordre, som du vil føje et nyt arbejdsordrejob til.</span><span class="sxs-lookup"><span data-stu-id="73ba6-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="73ba6-150">Rediger felterne **Serviceniveau**, **Forventet startdato** og **Forventet slutdato** efter behov, og klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="73ba6-151">Arbejdsordrejobbet føjes til den eksisterende relaterede arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-151">The work order job is added to the existing related work order.</span></span>


![Figur 1](media/03-work-orders.png)

<span data-ttu-id="73ba6-153">**Bemærk!** Hvis du har oprettet en relateret arbejdsordremaske i **Parametre til aktivstyring** > **Arbejdsordrer**-linket > feltet **Relateret arbejdsordremaske**, oprettes arbejdsordre-id'er i overensstemmelse med maskeopsætningen.</span><span class="sxs-lookup"><span data-stu-id="73ba6-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="73ba6-154">Hvis der ikke er konfigureret nogen tilknyttet arbejdsordremaske, bruges det næste tilgængelige ordre-id til relaterede arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="73ba6-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="73ba6-155">Kopiér arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="73ba6-155">Copy work order</span></span>

<span data-ttu-id="73ba6-156">Det er muligt hurtigt at oprette en ny arbejdsordre ud fra en eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="73ba6-157">Denne måde at arbejde med arbejdsordrer på er ikke den samme, som når du opretter arbejdsordrer på basis af vedligeholdelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="73ba6-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="73ba6-158">Den er nyttig, hvis du f.eks. har en arbejdsordre, der indeholder mange arbejdsordrejob med forskellige job på forskellige aktiver, der skal udføres med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="73ba6-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="73ba6-159">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="73ba6-160">Vælg den arbejdsordre, du vil kopiere indhold fra.</span><span class="sxs-lookup"><span data-stu-id="73ba6-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="73ba6-161">Klik på **Kopiér arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-161">Click **Copy work order**.</span></span> <span data-ttu-id="73ba6-162">Arbejdsordreopsætningen fra den valgte arbejdsordre vises.</span><span class="sxs-lookup"><span data-stu-id="73ba6-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="73ba6-163">Hvis det er nødvendigt, kan du redigere nogle af felterne.</span><span class="sxs-lookup"><span data-stu-id="73ba6-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="73ba6-164">Klik på **OK** for at oprette den nye arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="73ba6-165">Rediger evt. arbejdsordren i **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="73ba6-166">Når den nye arbejdsordre oprettes, kopieres nogle oplysninger direkte fra den eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="73ba6-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="73ba6-167">Oplysninger om prognoser, værktøjer, vedligeholdelsestjeklister, arbejdssted, adresser og planlægning kopieres ikke, men initialiseres fra den aktuelle opsætning i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="73ba6-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="73ba6-168">Det betyder, at hvis der er foretaget ændringer i disse data fra tidspunktet for oprettelsen af den første arbejdsordre, indtil du tog en kopi af arbejdsordren, medtages disse ændringer i den nye arbejdsordre, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="73ba6-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="73ba6-169">Eksempler er ændringer i prognoser eller opdaterede vedligeholdelsestjeklister.</span><span class="sxs-lookup"><span data-stu-id="73ba6-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Figur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="73ba6-171">Oprette en arbejdsordre baseret på en vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="73ba6-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="73ba6-172">Klik på **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsesanmodninger** > **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="73ba6-173">Vælg de vedligeholdelsesanmodninger, du vil oprette en arbejdsordre for, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="73ba6-174">I **Alle anmodninger** skal du klikke på **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="73ba6-175">Udfyld rullelisten **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="73ba6-176">Hvis der er valgt en vedligeholdelsesjobtype i vedligeholdelsesanmodningen, kan du vælge en anden type vedligeholdelsesjob, hvis det er nødvendigt, når du opretter arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="73ba6-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="73ba6-177">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-177">Click **OK**.</span></span> <span data-ttu-id="73ba6-178">Der vises en meddelelse om, at arbejdsordren er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="73ba6-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="73ba6-179">Hvis du vil se, hvilke arbejdsordrer der er knyttet til en vedligeholdelsesanmodning, skal du vælge vedligeholdelsesanmodningen på listen **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** og klikke på knappen **Arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="73ba6-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Figur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="73ba6-181">Du kan også oprette arbejdsordrer automatisk ved at planlægge vedligeholdelsesplanjob eller ved at konfigurere "Automatisk oprettelse" af vedligeholdelsesplaner eller vedligeholdelsesrunder for et aktiv.</span><span class="sxs-lookup"><span data-stu-id="73ba6-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="73ba6-182">Arbejdsordrer, der er oprettet ud fra vedligeholdelsesanmodninger i **Vedligeholdelsestidsplan**, oprettes med de vedligeholdelsesjobtyper, der er valgt i vedligeholdelsesanmodningerne.</span><span class="sxs-lookup"><span data-stu-id="73ba6-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

