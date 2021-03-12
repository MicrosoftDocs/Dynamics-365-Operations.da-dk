---
title: Firmakoncept i Dataverse
description: I dette emne beskrives integrationen af virksomhedsdata mellem Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: bbe634b87b3cb30ed993f9b3afeb4321d70f07e6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744873"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="95dce-103">Firmakoncept i Dataverse</span><span class="sxs-lookup"><span data-stu-id="95dce-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="95dce-104">I Finance and Operations er konceptet et *firma* både en juridisk konstruktion og en forretningskonstruktion.</span><span class="sxs-lookup"><span data-stu-id="95dce-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="95dce-105">Det er også en sikkerheds- og synlighedsgrænse for data.</span><span class="sxs-lookup"><span data-stu-id="95dce-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="95dce-106">Brugere arbejder altid i konteksten af et enkelt firma, og de fleste data stripes (spredes) af firmaet.</span><span class="sxs-lookup"><span data-stu-id="95dce-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="95dce-107">Dataverse har ikke et tilsvarende koncept.</span><span class="sxs-lookup"><span data-stu-id="95dce-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="95dce-108">Det tætteste koncept er *virksomhedsenhed*, som primært er en sikkerheds- og synlighedsgrænse for brugerdata.</span><span class="sxs-lookup"><span data-stu-id="95dce-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="95dce-109">Dette koncept har ikke samme juridiske eller forretningsmæssige implikationer som firmakonceptet.</span><span class="sxs-lookup"><span data-stu-id="95dce-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="95dce-110">Da virksomhedsenhed og firma ikke er tilsvarende koncepter, er det ikke muligt at gennemtvinge en en-til-en (1:1) tilknytning mellem dem med henblik på Dataverse-integration.</span><span class="sxs-lookup"><span data-stu-id="95dce-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="95dce-111">Men da brugere som standard skal kunne se de samme rækker i programmet og Dataverse, har Microsoft introduceret en ny tabel i Dataverse, der hedder cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="95dce-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="95dce-112">Denne tabel svarer til tabellen Firma i programmet.</span><span class="sxs-lookup"><span data-stu-id="95dce-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="95dce-113">For at hjælpe med at sikre, at synlighed af rækker som standard er ens mellem programmet og Dataverse, anbefaler vi følgende opsætning af data i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="95dce-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="95dce-114">For hver firmarække i Finance and Operations, der er aktiveret til dobbeltskrivning, oprettes der en tilknyttet cdm\_Company-række.</span><span class="sxs-lookup"><span data-stu-id="95dce-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="95dce-115">Når en cdm\_Company-række oprettes og aktiveres til dobbeltskrivning oprettes der en standardvirksomhedsenhed med samme navn.</span><span class="sxs-lookup"><span data-stu-id="95dce-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="95dce-116">Selvom der automatisk oprettes et standardteam for denne virksomhedsenhed, bruges virksomhedsenheden ikke.</span><span class="sxs-lookup"><span data-stu-id="95dce-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="95dce-117">Der oprettes et separat ejerteam med samme navn.</span><span class="sxs-lookup"><span data-stu-id="95dce-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="95dce-118">Det er også tilknyttet virksomhedsenheden.</span><span class="sxs-lookup"><span data-stu-id="95dce-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="95dce-119">Som standard angives ejeren af enhver række, der oprettes og dobbeltskrives til Dataverse, til "DW-ejer"-teamet, der er knyttet til den tilknyttede virksomhedsenhed.</span><span class="sxs-lookup"><span data-stu-id="95dce-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="95dce-120">I følgende illustration vises et eksempel på denne dataopsætning i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95dce-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Dataopsætning i Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="95dce-122">På grund af denne konfiguration ejes alle rækker, der er relateret til USMF-firmaet, af et team, der er knyttet til USMF-virksomhedsenheden i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95dce-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="95dce-123">Derfor kan alle brugere, der har adgang til den pågældende virksomhedsenhed via en sikkerhedsrolle, der er angivet til synlighed på virksomhedsenhedsniveau, nu se disse rækker.</span><span class="sxs-lookup"><span data-stu-id="95dce-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="95dce-124">Følgende eksempel viser, hvordan teams kan bruges til at give den korrekte adgang til disse rækker.</span><span class="sxs-lookup"><span data-stu-id="95dce-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="95dce-125">Rollen "Sales Manager" er tildelt medlemmer af teamet "USMF Sales".</span><span class="sxs-lookup"><span data-stu-id="95dce-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="95dce-126">Brugere, der har rollen "Sales Manager", kan få adgang til alle firmarækker, der er medlem af den samme virksomhedsenhed, som de er medlem af.</span><span class="sxs-lookup"><span data-stu-id="95dce-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="95dce-127">Teamet "USMF Sales" er knyttet til den USMF-virksomhedsenhed, der er nævnt tidligere.</span><span class="sxs-lookup"><span data-stu-id="95dce-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="95dce-128">Derfor kan medlemmer af teamet "USMF Sales" se enhver konto, der ejes af brugeren "USMF DW", som ville være kommet fra USMF-firmatabellen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95dce-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Sådan kan teams bruges](media/dual-write-company-2.png)

<span data-ttu-id="95dce-130">Som den foregående illustration viser, er denne 1:1-tilknytning mellem virksomhedsenhed, firma og team blot et udgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="95dce-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="95dce-131">I dette eksempel oprettes der manuelt en ny "Europe"-virksomhedsenhed i Dataverse som overordnet til både DEMF og ESMF.</span><span class="sxs-lookup"><span data-stu-id="95dce-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="95dce-132">Denne nye rodvirksomhedsenhed er ikke relateret til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="95dce-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="95dce-133">Den kan dog bruges til at give medlemmerne af "EUR Sales"-teamet adgang til kontodata i både DEMF og ESMF ved at indstille datasynlighed til **Parent/Child BU** i den tilknyttede sikkerhedsrolle.</span><span class="sxs-lookup"><span data-stu-id="95dce-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="95dce-134">Et sidste emne, der skal omtales, er, hvordan dobbeltskrivning afgør, hvilket ejerteam det skal tildeles rækker.</span><span class="sxs-lookup"><span data-stu-id="95dce-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="95dce-135">Denne funktionsmåde styres af kolonnen **Standardejerteam** på cdm\_Company-rækken.</span><span class="sxs-lookup"><span data-stu-id="95dce-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="95dce-136">Når en cdm\_Company-række er aktiveret til dobbeltskrivning, opretter en plug-in automatisk den tilknyttede virksomhedsenhed og ejerteamet (hvis den ikke allerede findes) og indstiller kolonnen **Standardejerteam**.</span><span class="sxs-lookup"><span data-stu-id="95dce-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="95dce-137">Administratoren kan ændre denne kolonne til en anden værdi.</span><span class="sxs-lookup"><span data-stu-id="95dce-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="95dce-138">Men administratoren kan ikke rydde kolonnen, så længe tabellen er aktiveret til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="95dce-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="95dce-139">![Kolonnen Standardejerteam](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="95dce-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="95dce-140">Firma-striping og bootstrapping</span><span class="sxs-lookup"><span data-stu-id="95dce-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="95dce-141">Dataverse-integration giver firmaparitet ved at bruge en firmaidentifikator til at stripe data.</span><span class="sxs-lookup"><span data-stu-id="95dce-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="95dce-142">Som det fremgår af følgende illustration, udvides alle firmaspecifikke tabeller, så de har en mange-til-en-relation (N:1) med tabellen cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="95dce-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="95dce-143">![N:1-relation mellem en firmaspecifik tabel og tabellen cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="95dce-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="95dce-144">Når et firma er tilføjet og gemt i rækker, bliver værdien skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="95dce-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="95dce-145">Derfor skal brugerne sørge for, at de vælger det rigtige firma.</span><span class="sxs-lookup"><span data-stu-id="95dce-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="95dce-146">Kun rækker, der har firmadata, er kvalificerede til dobbeltskrivning mellem programmet og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95dce-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="95dce-147">For eksisterende Dataverse-data vil en administrativ bootstrapping-oplevelse snart være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="95dce-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="95dce-148">Udfylde firmanavn automatisk i kundeengagementapps</span><span class="sxs-lookup"><span data-stu-id="95dce-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="95dce-149">Du kan automatisk udfylde firmanavnet i kundeengagementapps på flere måder.</span><span class="sxs-lookup"><span data-stu-id="95dce-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="95dce-150">Hvis du er systemadministrator, kan du angive standardfirmaet ved at navigere til **Avancerede indstillinger > System > Sikkerhed > Brugere**.</span><span class="sxs-lookup"><span data-stu-id="95dce-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="95dce-151">Åbn formularen **Bruger**, og angiv i sektionen **Organisationsoplysninger** værdien **Firmastandard på formularer**.</span><span class="sxs-lookup"><span data-stu-id="95dce-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Angiv standardfirma i sektionen Organisationsoplysninger.":::

+ <span data-ttu-id="95dce-153">Hvis du har **Skrive**-adgang til tabellen **SystemUser** for **Afdeling**-niveauet, kan du ændre standardfirmaet i en hvilken som helst formular ved at vælge et firma i rullemenuen **Firma**.</span><span class="sxs-lookup"><span data-stu-id="95dce-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ændre firmanavnet på en ny konto.":::

+ <span data-ttu-id="95dce-155">Hvis du har **skrive**-adgang til data i mere end ét firma, kan du ændre standardfirmaet ved at vælge en række, der tilhører et andet firma.</span><span class="sxs-lookup"><span data-stu-id="95dce-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Når du vælger en række, ændres standardfirmaet.":::

+ <span data-ttu-id="95dce-157">Hvis du er systemkonfigurator eller -administrator, og du vil udfylde firmadata automatisk i en brugerdefineret formular, kan du bruge [formularhændelser](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="95dce-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="95dce-158">Føj en JavaScript-reference til **msdyn_/DefaultCompany.js**, og brug følgende hændelser.</span><span class="sxs-lookup"><span data-stu-id="95dce-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="95dce-159">Du kan bruge enhver standardformular, f.eks. formularen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="95dce-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="95dce-160">Hændelsen **OnLoad** for formularen: Angiv kolonnen **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="95dce-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="95dce-161">Hændelsen **OnChange** for kolonnen **Firma**: Angiv kolonnen **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="95dce-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="95dce-162">Anvende filtrering baseret på firmakontekst</span><span class="sxs-lookup"><span data-stu-id="95dce-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="95dce-163">Hvis du vil anvende filtrering baseret på firmakonteksten i de brugerdefinerede formularer eller på brugerdefinerede opslagskolonner, der er føjet til standardformularer, skal du åbne formularen og bruge sektionen **Filtrering af relaterede poster** til at anvende firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="95dce-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="95dce-164">Du skal angive dette for hver opslagskolonne, der kræver filtrering, på baggrund af det underliggende firma på en bestemt række.</span><span class="sxs-lookup"><span data-stu-id="95dce-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="95dce-165">Indstillingen vises for **Konto** i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="95dce-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Anvende firmakontekst":::

