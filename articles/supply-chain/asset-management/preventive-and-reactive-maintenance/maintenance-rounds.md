---
title: Vedligeholdelsesrunder
description: I dette emne beskrives vedligeholdelsesrunder i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 63cb2614b2037fac1129c7d2f82a26dac41a3490
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889955"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="3fa4e-103">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="3fa4e-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3fa4e-104">I **Styring af aktiver** kan du oprette vedligeholdelsesrunder for forskellige aktiver, hvor du skal udføre en lignende opgave med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="3fa4e-105">Det kan f.eks. være smøreopgaver eller sikkerhedsinspektioner, der skal udføres på en række maskiner inden for de samme intervaller.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="3fa4e-106">Første trin er at oprette en vedligeholdelsesrunde, herunder aktiver, der kræver samme type vedligeholdelsesjob.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="3fa4e-107">Derefter skal du planlægge vedligeholdelsesrunderne.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="3fa4e-108">Når du har fuldført tidsplanen for vedligeholdelsesrunderne, kan du se alle de jobposter, der vedrører runden i **Alle vedligeholdelsestidsplaner** og **Åbne vedligeholdelsestidsplanslinjer**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="3fa4e-109">Vedligeholdelsesrunder kan også konfigureres på arbejdssteder og fuldføres på de aktiver, der er installeret på arbejdsstedet på tidspunktet for oprettelsen af den rundebaserede arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="3fa4e-110">Se under [Oprette arbejdssteder](../functional-locations/create-functional-locations.md) for at få yderligere oplysninger om konfiguration af vedligeholdelsesrunder på arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="3fa4e-111">Opsætning af vedligeholdelsesrunde</span><span class="sxs-lookup"><span data-stu-id="3fa4e-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="3fa4e-112">Klik på **Styring af aktiver** > **Opsætning** > **Forebyggende vedligeholdelse** > **Vedligeholdelsesrunder**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="3fa4e-113">Klik på **Ny** for at oprette en ny vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="3fa4e-114">Indsæt et id i feltet **Vedligeholdelsesrunde** og et navn til vedligeholdelsesrunden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="3fa4e-115">Vælg en startdato for runden i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="3fa4e-116">I felterne **Afslut inden for dage** og **Afslut inden for timer** kan du indsætte den forventede slutdato i dage eller timer.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="3fa4e-117">Den forventede slutdato beregnes i forhold til den startdato, som beregnes, når der oprettes vedligeholdelsestidsplanlinjer.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="3fa4e-118">Du kan f.eks. indsætte "7" i feltet **Afslut inden for dage** for at angive, at det relaterede job skal fuldføres inden for en uge fra startdatoen.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="3fa4e-119">Vælg "Ja" på til/fra-knappen **Automatisk oprettelse**, hvis der automatisk skal oprettes arbejdsordrer fra de vedligeholdelsestidsplanlinjer, der oprettes ud fra denne vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="3fa4e-120">Vælg i feltet **Arbejdsordretype**, den arbejdsordretype, der skal bruges på arbejdsordrer, der er oprettes ud fra denne vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="3fa4e-121">I feltet **Serviceniveau** skal du vælge det serviceniveau for arbejdsordren, der skal bruges på arbejdsordrer, der er oprettes ud fra denne vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="3fa4e-122">I oversigtspanelet **Aktivlinjer** skal du klikke på **Tilføj** for at føje et aktiv til vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="3fa4e-123">Et linjenummer indsættes automatisk i feltet **Linjenummer** for at angive rækkefølgen for aktiverne i vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="3fa4e-124">Vælg aktivet i feltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="3fa4e-125">Vælg vedligeholdelsesjobtypen for aktivet i feltet **Vedligeholdelsesjobtype**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="3fa4e-126">Vælg om nødvendigt **Variant af vedligeholdelsesjobtype** og **Fag**, der har relation til typen af vedligeholdelsesjobbet.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="3fa4e-127">Vælg gentagelse (dag, uge osv.) i feltet **Periodetype**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="3fa4e-128">Indsæt antallet af gentagelser for vedligeholdelsesrunden i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="3fa4e-129">Eksempel: Hvis du har valgt "Dag" i feltet **Periodetype**, og du indsætter tallet "7" i dette felt, oprettes der nye vedligeholdelsesrundelinjer under forebyggende vedligeholdelsesplanlægning en gang om ugen.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="3fa4e-130">Vælg en startdato for det aktiv, der skal inkluderes i vedligeholdelsesrunden i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="3fa4e-131">Denne dato kan være en anden end den startdato, der er angivet i vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="3fa4e-132">Gentag trin 9-16, hvis du vil føje flere aktiver til vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="3fa4e-133">I oversigtspanelet **Arbejdsstedslinjer** skal du klikke på **Tilføj** for at føje et arbejdssted til vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="3fa4e-134">Se beskrivelsen af de relaterede felter ovenfor.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="3fa4e-135">De samme felter er tilgængelige som ved oprettelse af en aktivlinje, men du kan også vælge **Producent** og **Model** til et arbejdssted, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="3fa4e-136">Hvis du kun vælger et arbejdssted på en linje, men ikke vælger **Aktivtype**, **Producent** **Model** **Vedligeholdelsesjobtype**, **Variant af vedligeholdelsesjobtype** og **Fag**, bliver alle de aktiver, der er relateret til det pågældende arbejdssted på tidspunktet for vedligeholdelsesplanlægningen, medtaget i vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="3fa4e-137">I oversigtspanelet **Puljer** skal du klikke på **Tilføj** for at vælge en arbejdsordrepulje, der skal inkluderes i vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="3fa4e-138">Der kan knyttes flere ordrepuljer til en vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="3fa4e-139">Gem din opsætning.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="3fa4e-140">Felterne **Aktiver** og **Linjer**, der findes i gruppen **Detaljer** i oversigtspanelet **Hoved**, viser det samlede antal aktiver og linjer, der er relateret til den valgte vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="3fa4e-141">Illustrationen nedenfor viser et eksempel på en vedligeholdelsesrunde, der indeholder tre aktiver.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Figur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="3fa4e-143">Planlæg vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="3fa4e-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="3fa4e-144">Når du har konfigureret en vedligeholdelsesrunde, skal du køre et tidsplanlægningsjob for at planlægge alle job, der er relateret til vedligeholdelsesrunden.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="3fa4e-145">Klik på **Styring af aktiver** > **Periodisk** > **Forebyggende vedligeholdelse** > **Planlæg vedligeholdelsesrunder** eller **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller på **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer** > vælg vedligeholdelsestidsplanslinje på listen > knappen **Vedligeholdelsesrunder**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="3fa4e-146">Vælg den periodetype, der skal bruges til planlægningsjobbet, i feltet **Periode**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="3fa4e-147">Indsæt det antal perioder, der skal medtages i Planlægningsjobbet, i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="3fa4e-148">Startdatoen for planlægningen er dags dato.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="3fa4e-149">Vælg "ja" på knappen **Automatisk oprettelse**, hvis der automatisk skal oprettes en arbejdsordre ud fra en vedligeholdelsesrunde.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="3fa4e-150">Hvis denne til/fra-knap er indstillet til "ja", og til/fra-knappen **Automatisk oprettelse** også er indstillet til "ja" i vedligeholdelsesrunden i formularen **Vedligeholdelsesrunder**, oprettes arbejdsordrer baseret på vedligeholdelsesrundelinjerne, og der oprettes også vedligeholdelsestidsplanslinjer med status "Oprettet af arbejdsordre ".</span><span class="sxs-lookup"><span data-stu-id="3fa4e-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="3fa4e-151">Hvis kun en af de til/fra-knapper til **Automatisk oprettelse** er indstillet til "ja" i denne rulleliste eller i **Vedligeholdelsesrunder**, oprettes kun vedligeholdelsestidsplanslinjer med status "Oprettet".</span><span class="sxs-lookup"><span data-stu-id="3fa4e-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="3fa4e-152">Hvis det er tilfældet, oprettes der ingen arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="3fa4e-153">Hvis det er nødvendigt, kan du vælge bestemte runder eller en anden startdato for planlægningsjobbet.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="3fa4e-154">Klik på **Filter**, og tilføj de runder, der skal medtages.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="3fa4e-155">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-155">Click **OK**.</span></span>

7. <span data-ttu-id="3fa4e-156">Du kan nu se vedligeholdelsesrundejob i **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="3fa4e-157">Hvis de planlagte runder er forbundet til en arbejdsordrepulje, kan du også se vedligeholdelsestidsplanslinjer i **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="3fa4e-158">Vedligeholdelsestidsplanslinjer, der er oprettet ud fra en runde, har referencetypen "Vedligeholdelsesrunder".</span><span class="sxs-lookup"><span data-stu-id="3fa4e-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="3fa4e-159">De to illustrationer nedenfor viser et planlægningsjob i dialogboksen **Planlæg vedligeholdelsesrunder** og vedligeholdelsestidsplanslinjer, der er oprettet i **Hele vedligeholdelsestidsplanen** baseret på det pågældende planlægningsjob.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Figur 2](media/14-preventive-maintenance.png)

![Figur 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="3fa4e-162">Når der oprettes arbejdsordrer manuelt for aktiver, der er dækket af en leverandørgaranti, vises der en dialogboks for at gøre brugeren opmærksom på garantien.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="3fa4e-163">Oprettelsen af arbejdsordren kan derefter annulleres.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="3fa4e-164">Kontrollen af en garantirelation udelades for arbejdsordrer, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="3fa4e-165">Du kan oprette et batchjob i oversigtspanelet **Kør i baggrunden** for at planlægge runder med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="3fa4e-166">Hvis en runde er medtaget i flere arbejdsordrepuljer (referer til [Arbejdsordrepuljer](../work-orders/work-order-pools.md)), vises der én post for hver pulje i **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="3fa4e-167">Dette gøres for at optimere filtreringsindstillingerne for arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-167">This is done to optimize the filtering options for work order pools.</span></span>

