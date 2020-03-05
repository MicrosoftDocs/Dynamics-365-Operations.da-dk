---
title: Vis ordrebeskeder på POS
description: I dette emne beskrives, hvordan du aktiverer ordrebeskeder på salgsstedet (POS) og i beskedstrukturen.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 04dd57aabcbdf5291f06317800b69f29f15d2763
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021944"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a><span data-ttu-id="2210b-103">Vis ordrebeskeder på POS</span><span class="sxs-lookup"><span data-stu-id="2210b-103">Show order notifications in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2210b-104">I det moderne detailmiljø tildeles medarbejderne i butikken forskellige opgaver, f.eks. at hjælpe kunder, indtaste transaktioner, udføre optællinger af lagerbeholdninger og modtage ordrer i butikken.</span><span class="sxs-lookup"><span data-stu-id="2210b-104">In the modern retail environment, store associates are assigned various tasks, such as helping customers, entering transactions, doing stock counts, and receiving orders in the store.</span></span> <span data-ttu-id="2210b-105">POS-klienten leverer ét enkelt program, hvor medarbejderne kan udføre alle disse og mange andre opgaver.</span><span class="sxs-lookup"><span data-stu-id="2210b-105">The point of sale (POS) client provides a single application where associates can perform all these tasks and many others.</span></span> <span data-ttu-id="2210b-106">Da der skal udføres forskellige opgaver i løbet af dagen, skal medarbejderne evt. have besked, når noget kræver deres opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="2210b-106">Because various tasks must be performed during the day, associates might have to be notified when something requires their attention.</span></span> <span data-ttu-id="2210b-107">Beskedstrukturen på POS'et er en hjælp, fordi forhandlere kan bruge den til at konfigurere rollebaserede beskeder.</span><span class="sxs-lookup"><span data-stu-id="2210b-107">The notification framework in the POS helps by letting retailers configure role-based notifications.</span></span> <span data-ttu-id="2210b-108">Fra og med Dynamics 365 for Retail med programopdatering 5 kan disse meddelelser kun konfigureres for POS-handlinger.</span><span class="sxs-lookup"><span data-stu-id="2210b-108">As of Dynamics 365 for Retail with application update 5, these notifications can be configured only for POS operations.</span></span>


<span data-ttu-id="2210b-109">På nuværende tidspunkt kan systemet kun vise beskeder for ordreopfyldningsoperationer.</span><span class="sxs-lookup"><span data-stu-id="2210b-109">Currently, the system can show notifications only for order fulfillment operations.</span></span> <span data-ttu-id="2210b-110">Fordi strukturen er udviklet til at kunne udvides, vil udviklere dog senere kunne skrive en beskedbehandler for operationer og få vist beskederne for den pågældende operation i POS'et.</span><span class="sxs-lookup"><span data-stu-id="2210b-110">However, because the framework is designed to be extensible, developers will eventually be able to write a notification handler for any operation and show the notifications for that operation in the POS.</span></span>

## <a name="enable-notifications-for-order-fulfillment-operations"></a><span data-ttu-id="2210b-111">Aktivere beskeder for ordreopfyldningsoperationer</span><span class="sxs-lookup"><span data-stu-id="2210b-111">Enable notifications for order fulfillment operations</span></span>

<span data-ttu-id="2210b-112">Hvis du vil aktivere beskeder for ordreopfyldningsoperationer, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2210b-112">To enable notifications for order fulfillment operations, follow these steps.</span></span>

1. <span data-ttu-id="2210b-113">Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="2210b-113">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Operations**.</span></span>
2. <span data-ttu-id="2210b-114">Søg efter **Ordreopfyldning**-operationen, og marker afkrydsningsfeltet **Aktiver beskeder** ud for indstillingen for at angive, at beskedstrukturen skal lytte til behandleren for denne operation.</span><span class="sxs-lookup"><span data-stu-id="2210b-114">Search for the **Order fulfillment** operation, and select the **Enable notifications** check box for it to specify that the notification framework should listen to the handler for this operation.</span></span> <span data-ttu-id="2210b-115">Hvis behandleren er implementeret, vises beskeder for denne operation derefter i POS.</span><span class="sxs-lookup"><span data-stu-id="2210b-115">If the handler is implemented, notifications for this operation will then be shown in the POS.</span></span>
3. <span data-ttu-id="2210b-116">Gå til **Retail og Commerce** &gt; **Medarbejdere** &gt; **Arbejdere** &gt;. Under fanen Commerce skal du åbne de POS-rettigheder, der er knyttet til arbejderen.</span><span class="sxs-lookup"><span data-stu-id="2210b-116">Go to **Retail and Commerce** &gt; **Employees** &gt; **Workers** &gt;, under Commerce tab, open the POS permissions associated with the worker.</span></span> <span data-ttu-id="2210b-117">Udvid oversigtspanelet **Beskeder**, tilføj operationen **Ordreopfyldning**, og indstil feltet **Visningsrækkefølge** til **1**.</span><span class="sxs-lookup"><span data-stu-id="2210b-117">Expand the **Notifications** FastTab, add the **Order fulfillment** operation, and set the **Display order** field to **1**.</span></span> <span data-ttu-id="2210b-118">Hvis mere end én besked er konfigureret, kan dette felt bruges til at arrangere beskeder.</span><span class="sxs-lookup"><span data-stu-id="2210b-118">If more than one notification is configured, this field is used to arrange the notifications.</span></span> <span data-ttu-id="2210b-119">Beskeder, der har en lavere værdi for **Visningsrækkefølge**, vises over beskeder, der har en højere værdi.</span><span class="sxs-lookup"><span data-stu-id="2210b-119">Notifications that have a lower **Display order** value appear above notifications that have a higher value.</span></span> <span data-ttu-id="2210b-120">Beskeder, der har en **Visningsrækkefølge**-værdi på **1**, findes øverst.</span><span class="sxs-lookup"><span data-stu-id="2210b-120">Notifications that have a **Display order** value of **1** are at the top.</span></span>

    <span data-ttu-id="2210b-121">Beskeder vises kun for operationer, der er tilføjet i oversigtspanelet **Beskeder**, og du kan kun tilføje operationer der, hvis afkrydsningsfeltet **Aktiver beskeder** for disse operationer er markeret på siden **POS-operationer**.</span><span class="sxs-lookup"><span data-stu-id="2210b-121">Notifications are shown only for operations that are added on the **Notifications** FastTab, and you can add operations there only if the **Enable notifications** check box for those operations has been selected on the **POS operations** page.</span></span> <span data-ttu-id="2210b-122">Derudover vises beskeder for en operation kun for arbejdere, hvis operationen føjes til POS-rettighederne for disse arbejdere.</span><span class="sxs-lookup"><span data-stu-id="2210b-122">Additionally, notifications for an operation are shown to workers only if the operation is added to the POS permissions for those workers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2210b-123">Beskeder kan tilsidesættes på brugerniveau.</span><span class="sxs-lookup"><span data-stu-id="2210b-123">Notifications can be overridden at the user level.</span></span> <span data-ttu-id="2210b-124">Åbn arbejderens post, vælg **POS-rettigheder**, og rediger derefter brugerens beskedabonnement.</span><span class="sxs-lookup"><span data-stu-id="2210b-124">Open the worker's record, select **POS permissions**, and then edit the user's notification subscription.</span></span>

4. <span data-ttu-id="2210b-125">Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="2210b-125">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="2210b-126">I feltet **Beskedinterval** skal du angive, hvor ofte beskeder skal udtrækkes.</span><span class="sxs-lookup"><span data-stu-id="2210b-126">In the **Notification interval** field, specify how often notifications should be pulled.</span></span> <span data-ttu-id="2210b-127">For nogle beskeder skal POS foretage kald i realtid til back-office-programmet.</span><span class="sxs-lookup"><span data-stu-id="2210b-127">For some notifications, the POS must make real-time calls to the back-office application.</span></span> <span data-ttu-id="2210b-128">Disse kald forbruger databehandlingskapaciteten fra back-office-programmet.</span><span class="sxs-lookup"><span data-stu-id="2210b-128">These calls consume the compute capacity of your back-office application.</span></span> <span data-ttu-id="2210b-129">Når du indstiller beskedintervallet, skal du derfor overveje både virksomhedens behov og virkningen af kald i realtid til back-office-programmet.</span><span class="sxs-lookup"><span data-stu-id="2210b-129">Therefore, when you set the notification interval, you should consider both your business requirements and the impact of real-time calls to the back-office application.</span></span> <span data-ttu-id="2210b-130">En værdi på **0** (nul) deaktiverer beskeder.</span><span class="sxs-lookup"><span data-stu-id="2210b-130">A value of **0** (zero) turns off notifications.</span></span>
5. <span data-ttu-id="2210b-131">Gå til **Retail og Commerce** &gt; **Retail og Commerce IT** &gt; **Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="2210b-131">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span> <span data-ttu-id="2210b-132">Vælg tidsplanen **1060** (**personale**) for at synkronisere indstillinger for beskedabonnementet, og vælg derefter **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="2210b-132">Select the **1060** (**Staff**) schedule to synchronize notification subscription settings, and then select **Run now**.</span></span> <span data-ttu-id="2210b-133">Vælg derefter tidsplanen **1070** (**kanalkonfiguration**) for at synkronisere rettighedsintervallet, og vælg derefter **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="2210b-133">Next, select the **1070** (**Channel configuration**) schedule to synchronize the permission interval, and then select **Run now**.</span></span>

## <a name="view-notifications-in-the-pos"></a><span data-ttu-id="2210b-134">Vise beskeder i POS'et</span><span class="sxs-lookup"><span data-stu-id="2210b-134">View notifications in the POS</span></span>

<span data-ttu-id="2210b-135">Når du har fuldført de foregående trin, kan arbejderne se beskederne i POS'et.</span><span class="sxs-lookup"><span data-stu-id="2210b-135">After you complete the preceding steps, the workers will be able to view the notifications in the POS.</span></span> <span data-ttu-id="2210b-136">Tryk på beskedikonet i øverste højre hjørne i POS'et for at få vist beskederne.</span><span class="sxs-lookup"><span data-stu-id="2210b-136">To view notifications, press the notification icon in the top right corner of the POS.</span></span> <span data-ttu-id="2210b-137">Der vises et beskedcenter med beskederne for ordreopfyldningsoperationen.</span><span class="sxs-lookup"><span data-stu-id="2210b-137">A notification center appears and shows notifications for the order fulfillment operation.</span></span> <span data-ttu-id="2210b-138">Beskedcenteret skal vise følgende grupper i ordreopfyldningsoperationen:</span><span class="sxs-lookup"><span data-stu-id="2210b-138">The notification center should show the following groups in the order fulfillment operation:</span></span>

- <span data-ttu-id="2210b-139">**Afhentning i butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Afhentning**, og som er planlagt til afhentning fra den aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="2210b-139">**Store pickup** – This group shows the count of orders that have a delivery mode of **Pickup**, and that are scheduled for pickup from the current store.</span></span> <span data-ttu-id="2210b-140">Du kan trykke på nummeret på gruppen for at åbne siden **Ordreopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="2210b-140">You can press the number on the group to open the **Order fulfillment** page.</span></span> <span data-ttu-id="2210b-141">I dette tilfælde filtreres på siden, så den kun viser de aktive ordrer, der er konfigureret til afhentning fra det aktuelle lager.</span><span class="sxs-lookup"><span data-stu-id="2210b-141">In this case, the page will be filtered so that it shows only the active orders that are set up for pickup from the current store.</span></span>
- <span data-ttu-id="2210b-142">**Afsend fra butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Levering**, og som er planlagt til forsendelse fra den aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="2210b-142">**Ship from store** – This group shows the count of orders that have the delivery mode of **Shipping**, and that are scheduled for shipment from the current store.</span></span> <span data-ttu-id="2210b-143">Du kan trykke på nummeret på gruppen for at åbne siden **Ordreopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="2210b-143">You can press the number on the group to open the **Order fulfillment** page.</span></span> <span data-ttu-id="2210b-144">I dette tilfælde filtreres på siden, så den kun viser de aktive ordrer, der er konfigureret til forsendelse fra det aktuelle lager.</span><span class="sxs-lookup"><span data-stu-id="2210b-144">In this case, the page will be filtered so that it shows only the active orders that are set up for shipment from the current store.</span></span>

<span data-ttu-id="2210b-145">Hvis der tildeles nye ordrer til butikken til opfyldelse, ændres beskedikonet, så det angiver, at der er nye beskeder, og antallet af de relevante grupper opdateres.</span><span class="sxs-lookup"><span data-stu-id="2210b-145">When new orders are assigned to the store for fulfillment, the notification icon changes to indicate that there are new notifications, and the count for the appropriate groups is updated.</span></span> <span data-ttu-id="2210b-146">Selvom grupperne opdateres med jævne mellemrum, kan POS-brugere manuelt opdatere grupperne til enhver tid ved at vælge knappen **Opdater** ud for gruppen.</span><span class="sxs-lookup"><span data-stu-id="2210b-146">Even though the groups are refreshed at regular intervals however, POS users can manually refresh the groups at any time by selecting the **Refresh** button next to the group.</span></span> <span data-ttu-id="2210b-147">Endelig, hvis en gruppe har en ny vare, som den aktuelle arbejder ikke har fået vist, viser gruppen et burst-symbol for at angive nyt indhold.</span><span class="sxs-lookup"><span data-stu-id="2210b-147">Lastly, if a group has a new item, that the current worker hasn't viewed, then the group shows a burst symbol to indicate new content.</span></span>

## <a name="enable-live-content-on-pos-buttons"></a><span data-ttu-id="2210b-148">Aktivere dynamisk indhold på POS-knapper</span><span class="sxs-lookup"><span data-stu-id="2210b-148">Enable live content on POS buttons</span></span>

<span data-ttu-id="2210b-149">POS-knapper kan nu vise en optælling, så arbejderne nemmere kan bestemme, hvilke opgaver der kræver deres omgående opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="2210b-149">POS buttons can now show a count to help workers easily determine which tasks require their immediate attention.</span></span> <span data-ttu-id="2210b-150">For at vise dette nummer på en POS-knap skal du fuldføre opsætningen af beskeder, der er beskrevet tidligere i dette emne, (det vil sige, du skal aktivere beskeder for en operation, oprette et beskedinterval og opdatere POS-rettighedsgruppen for arbejderen).</span><span class="sxs-lookup"><span data-stu-id="2210b-150">To show this number on a POS button, you must complete the notification setup that is described earlier in this topic (that is, you must enable notifications for an operation, set up a notification interval, and update the POS permission group for the worker).</span></span> <span data-ttu-id="2210b-151">Derudover skal du åbne knapgitterdesigneren, se knappens egenskaber og markere afkrydsningsfeltet **Aktiver dynamisk indhold**.</span><span class="sxs-lookup"><span data-stu-id="2210b-151">Additionally, you must open the button grid designer, view the button's properties, and select the **Enable live content** check box.</span></span> <span data-ttu-id="2210b-152">I feltet **Justering af indhold** kan du vælge, om antallet skal vises i øverste højre hjørne af knappen (**Øverst til højre**) eller i midten (**Centreret**).</span><span class="sxs-lookup"><span data-stu-id="2210b-152">In the **Content alignment** field, you can select whether the count appears in the upper-right corner of the button (**Top right**) or in the center (**Center**).</span></span>

> [!NOTE]
> <span data-ttu-id="2210b-153">Dynamisk indhold kan kun aktiveres for operationer, hvis afkrydsningsfeltet **Aktiver beskeder** er markeret for dem på siden **POS-handlinger** som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="2210b-153">The live content can be enabled for operations only if the **Enable notifications** check box has been selected for them on the **POS operations** page, as described earlier in this topic.</span></span>

<span data-ttu-id="2210b-154">I følgende illustration vises indstillingerne for dynamisk indhold i knapgitterdesigneren.</span><span class="sxs-lookup"><span data-stu-id="2210b-154">The following illustration shows the live content settings in the button grid designer.</span></span>

<span data-ttu-id="2210b-155">![Indstillinger for dynamisk indhold i knapgitterdesigneren](./media/ButtonGridDesigner.png "Indstillinger for dynamisk indhold i knapgitterdesigneren")</span><span class="sxs-lookup"><span data-stu-id="2210b-155">![Live content settings in the button grid designer](./media/ButtonGridDesigner.png "Live content settings in the button grid designer")</span></span>

<span data-ttu-id="2210b-156">Hvis du vil have vist antallet af beskeder på en knap, skal du sikre dig, at det korrekte skærmlayout opdateres.</span><span class="sxs-lookup"><span data-stu-id="2210b-156">To show the notification count on a button, you need to ensure that the correct screen layout is being updated.</span></span> <span data-ttu-id="2210b-157">Hvis du vil fastlægge, hvilket skærmlayout der bruges af POS, skal du vælge ikonet **Indstillinger** i øverste højre hjørne og notere **Skærmlayout-id** og **Layoutopløsning**.</span><span class="sxs-lookup"><span data-stu-id="2210b-157">To determine the screen layout that is being used by the POS, select the **Settings** icon in upper-right corner and note the **Screen layout ID** and **Layout resolution**.</span></span> <span data-ttu-id="2210b-158">Brug nu Edge-browseren, og gå til siden **Skærmlayout**, find det **Skærmlayout-id** og den **Layoutopløsning**, der blev identificeret ovenfor, og markér afkrydsningsfeltet **Aktivér dynamisk indhold**.</span><span class="sxs-lookup"><span data-stu-id="2210b-158">Now using Edge browser, go to the **Screen layout** page, find the **Screen layout ID** and **Layout resolution** identified above and select the **Enable live content** check box.</span></span> <span data-ttu-id="2210b-159">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**, og kør jobbet 1090 (Kasseapparater) for at synkronisere ændringer af layoutet.</span><span class="sxs-lookup"><span data-stu-id="2210b-159">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule** and run the 1090 (Registers) job to synchronize layout changes.</span></span>


<span data-ttu-id="2210b-160">![Finde det skærmlayout, der bruges af POS](./media/Choose_screen_layout.png "Finde skærmlayoutet")</span><span class="sxs-lookup"><span data-stu-id="2210b-160">![Find the screen layout used by POS](./media/Choose_screen_layout.png "Find the screen layout")</span></span>

<span data-ttu-id="2210b-161">I følgende illustration viser effekten af at vælge **Øverst til højre** og **Centreret** i feltet **Justering af indhold** for knapper i forskellige størrelser.</span><span class="sxs-lookup"><span data-stu-id="2210b-161">The following illustration shows the effect of selecting **Top right** versus **Center** in the **Content alignment** field for buttons of various sizes.</span></span>

<span data-ttu-id="2210b-162">![Dynamisk indhold på POS-knapper](./media/ButtonsWithLiveContent.png "Dynamisk indhold på POS-knapper")</span><span class="sxs-lookup"><span data-stu-id="2210b-162">![Live content on POS buttons](./media/ButtonsWithLiveContent.png "Live content on POS buttons")</span></span>