---
title: Oversigt over påmindelser
description: Dette emne indeholder en generel beskrivelse af påmindelser. Du kan bruge påmindelser til at holde dig orienteret om de hændelser, du vil holde styr på i løbet af arbejdsdagen.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 755181e956a3d93d87e9e5d57622283ff7bf4944
ms.sourcegitcommit: f62c2151be477acfaeace73878471abb9b1b832d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/17/2020
ms.locfileid: "3602523"
---
# <a name="alerts-overview"></a><span data-ttu-id="62f4c-104">Oversigt over påmindelser</span><span class="sxs-lookup"><span data-stu-id="62f4c-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="62f4c-105">Om påmindelser</span><span class="sxs-lookup"><span data-stu-id="62f4c-105">About alerts</span></span>
<span data-ttu-id="62f4c-106">Påmindelser udgør et beskedsystem for kritiske hændelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="62f4c-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="62f4c-107">Du kan bruge påmindelser til at holde dig orienteret om de hændelser, du vil holde styr på i løbet af arbejdsdagen.</span><span class="sxs-lookup"><span data-stu-id="62f4c-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="62f4c-108">Du kan nemt oprette dit eget sæt påmindelsesregler, så du bliver påmindet om forfaldne leveringer, slettede ordrer, ændrede priser eller andre hændelser, du skal reagere på.</span><span class="sxs-lookup"><span data-stu-id="62f4c-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="62f4c-109">I ressourceplanlægning (ERP) er der flere typiske scenarier, hvor påmindelsesfunktionen kan bruges.</span><span class="sxs-lookup"><span data-stu-id="62f4c-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="62f4c-110">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="62f4c-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="62f4c-111">Scenarie 1: Opret en påmindelsesregel for nye salgsordrer</span><span class="sxs-lookup"><span data-stu-id="62f4c-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="62f4c-112">Åbn siden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="62f4c-113">I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret en brugerdefineret påmindelse**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="62f4c-114">I dialogboksen **Opret påmindelsesregel** under oversigtspanelet **Vis påmindelse, når** i feltet **Hændelse** skal du vælge **Posten er oprettet**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="62f4c-115">Scenarie 2: Opret en påmindelsesregel for udskydning af en leveringsdato</span><span class="sxs-lookup"><span data-stu-id="62f4c-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="62f4c-116">Åbn siden **Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="62f4c-117">Vælg en indkøbsordre-id for at få adgang til oplysningerne i indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="62f4c-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="62f4c-118">Udvid oversigtspanelet **Indkøbsordrehoved**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="62f4c-119">I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret en brugerdefineret påmindelse**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="62f4c-120">I dialogboksen **Opret påmindelsesregel** under oversigtspanelet **Vis påmindelse, når** i feltet **Felt** skal du vælge **Leveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="62f4c-121">I feltet **Hændelse** skal du vælge **er udsat**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="62f4c-122">Når du lukker dialogboksen **Opret påmindelsesregel**, vises reglen på siden **Administrer regler for påmindelser**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="62f4c-123">Du kan bruge siden **Administrer regler for påmindelser** til at opdatere de eksisterende påmindelsesregler.</span><span class="sxs-lookup"><span data-stu-id="62f4c-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="62f4c-124">Du kan f.eks. ændre hændelsesudløsere, opdatere hændelsesmeddelelser og opdatere udløbsdatoer.</span><span class="sxs-lookup"><span data-stu-id="62f4c-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="62f4c-125">Hvis du vil åbne siden **Administrer regler for påmindelser**, skal du bruge knappen **Påmind mig** under fanen **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="62f4c-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="62f4c-126">Hvad sker der, når der oprettes en påmindelse?</span><span class="sxs-lookup"><span data-stu-id="62f4c-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="62f4c-127">Når du opretter påmindelsesregler, kan du knytte en foruddefineret hændelse til et bestemt felt.</span><span class="sxs-lookup"><span data-stu-id="62f4c-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="62f4c-128">For eksempel, når den dato, der er angivet i feltet bliver nået, eller når indholdet af feltet ændres.</span><span class="sxs-lookup"><span data-stu-id="62f4c-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="62f4c-129">Du kan også knytte en hændelse til poster på en bestemt side.</span><span class="sxs-lookup"><span data-stu-id="62f4c-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="62f4c-130">For eksempel, når en post oprettes, eller når en post slettes.</span><span class="sxs-lookup"><span data-stu-id="62f4c-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="62f4c-131">Når den valgte hændelse indtræffer for feltet eller en post på siden, får du tilsendt en påmindelse.</span><span class="sxs-lookup"><span data-stu-id="62f4c-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="62f4c-132">Du opretter f.eks. en regel, hvor du knytter feltet **Leveringsdato** til en bestemt indkøbsordrelinje med hændelsen **forfald for så længe siden, som angivet her**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="62f4c-133">Du kan angive tidsintervallet til fem dage.</span><span class="sxs-lookup"><span data-stu-id="62f4c-133">You set the time frame to five days.</span></span> <span data-ttu-id="62f4c-134">I dette eksempel sendes en påmindelse fem dage efter leveringsdatoen for den pågældende indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="62f4c-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="62f4c-135">Du kan desuden forfine påmindelsesregler ved at angive betingelser.</span><span class="sxs-lookup"><span data-stu-id="62f4c-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="62f4c-136">Du kan for eksempel blive påmindet om nye indkøbsordrer, der oprettes for bestemt kreditorkonti.</span><span class="sxs-lookup"><span data-stu-id="62f4c-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="62f4c-137">Forberede til en påmindelse</span><span class="sxs-lookup"><span data-stu-id="62f4c-137">Preparing for an alert</span></span>

<span data-ttu-id="62f4c-138">Før du opretter en påmindelsesregel, skal du beslutte, hvornår og i hvilke situationer du vil modtage påmindelser.</span><span class="sxs-lookup"><span data-stu-id="62f4c-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="62f4c-139">Når du ved, hvilke hændelser du vil have besked om, skal du finde den side, hvor de data vises, der udløser den pågældende hændelse.</span><span class="sxs-lookup"><span data-stu-id="62f4c-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="62f4c-140">Hændelsen kan være en dato, der bliver nået, eller en bestemt ændring, der opstår.</span><span class="sxs-lookup"><span data-stu-id="62f4c-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="62f4c-141">Derfor skal du finde den side, hvor datoen er angivet, eller hvor det felt, der ændres, eller posten, der oprettes, bliver vist.</span><span class="sxs-lookup"><span data-stu-id="62f4c-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="62f4c-142">Når du har disse oplysninger, kan du oprette påmindelsesreglen.</span><span class="sxs-lookup"><span data-stu-id="62f4c-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="62f4c-143">Komponenter i en påmindelsesregel</span><span class="sxs-lookup"><span data-stu-id="62f4c-143">Components of an alert rule</span></span>

<span data-ttu-id="62f4c-144">En påmindelsesregel har fem komponenter</span><span class="sxs-lookup"><span data-stu-id="62f4c-144">An alert rule has five components:</span></span>

- <span data-ttu-id="62f4c-145">**Hændelse** – Den hændelse, der udløser en påmindelsesregel, kan være en dato eller en bestemt ændring, der opstår.</span><span class="sxs-lookup"><span data-stu-id="62f4c-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="62f4c-146">Du kan definere hændelser i oversigtspanelet **Send e-mail-påmindelser, når jobstatus ændres** i dialogboksen **Opret påmindelsesregel**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="62f4c-147">**Betingelse** – I oversigtspanelet **Påmind mig i** i dialogboksen **Opret påmindelsesregel** kan du vælge omfanget af betingelsen for at styre, hvornår du bliver påmindet om hændelser.</span><span class="sxs-lookup"><span data-stu-id="62f4c-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="62f4c-148">Du kan anvende reglen enten kun på den aktuelle post eller på alle de poster, der er synlige på siden.</span><span class="sxs-lookup"><span data-stu-id="62f4c-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="62f4c-149">Hvis reglen gælder på tværs af juridiske enheder, kan du angive indstillingen **Globalt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="62f4c-150">**Reglens udløb** – I oversigtspanelet **Påmind mig indtil** i dialogboksen **Opret påmindelsesregel** kan du angive, hvor længe påmindelsesreglen skal være aktiv.</span><span class="sxs-lookup"><span data-stu-id="62f4c-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="62f4c-151">**Indhold** – I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive den emnetekst og meddelelsestekst, der skal bruges i advarselsmeddelelserne.</span><span class="sxs-lookup"><span data-stu-id="62f4c-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="62f4c-152">**Bruger** – I oversigtspanelet **Hvem skal påmindes** i dialogboksen **Opret påmindelsesregel** kan du angive, hvilken bruger der skal modtage påmindelserne.</span><span class="sxs-lookup"><span data-stu-id="62f4c-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="62f4c-153">Dit bruger-ID er som standard markeret.</span><span class="sxs-lookup"><span data-stu-id="62f4c-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62f4c-154">Denne indstilling er begrænset til administratorer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="62f4c-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="62f4c-155">Videoer</span><span class="sxs-lookup"><span data-stu-id="62f4c-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="62f4c-156">Sådan bruges påmindelser til at overvåge filtrerede data</span><span class="sxs-lookup"><span data-stu-id="62f4c-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="62f4c-157">Videoen [Sådan bruges påmindelser til at overvåge filtrerede data](https://youtu.be/ZYKMcv6kl9s) (vises ovenfor) er inkluderet på afspilningslisten [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="62f4c-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="62f4c-158">Indstillinger for påmindelsesregel</span><span class="sxs-lookup"><span data-stu-id="62f4c-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="62f4c-159">Videoen [Indstillinger for påmindelsesregel](https://youtu.be/cpzimwOjicM) (vist ovenfor) er inkluderet på afspilningslisten [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="62f4c-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


