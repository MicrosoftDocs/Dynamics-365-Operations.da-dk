---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (31. oktober 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303748"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="36403-103">Nyheder eller ændringer i Dynamics 365 for Talent Core HR (31. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="36403-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36403-104">**Build 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="36403-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="36403-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="36403-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="36403-106">Oprette links fra Talent til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36403-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="36403-107">Med denne nye navigationsfunktion kan du oprette en tilknytning fra Talent til Finance and Operations, så du kan navigere direkte på Finance and Operations-sider.</span><span class="sxs-lookup"><span data-stu-id="36403-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="36403-108">Når links er konfigureret, kan du angive navn og gruppe for linket, hvor linket skal vises i Talent, og den destinationsside, der skal åbnes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="36403-109">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="36403-109">Coming soon</span></span>
<span data-ttu-id="36403-110">Feltkontekst tilføjes senere, så det bliver muligt at navigere direkte til de tilsvarende poster i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="36403-111">Du kan f.eks. bruge **Link til felt** til at angive konteksten, så du kan gå direkte til en bestemt medarbejder eller placering i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="36403-112">Konfigurere destinationssystemer</span><span class="sxs-lookup"><span data-stu-id="36403-112">Configure target systems</span></span>

<span data-ttu-id="36403-113">I Talent kan systemadministratorer definere links, som de kan få vist via arbejdsområdet Systemadministration.</span><span class="sxs-lookup"><span data-stu-id="36403-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="36403-114">En del af konfigurationen er Finance and Operations-miljøer, som du vil navigere til som linkets "mål".</span><span class="sxs-lookup"><span data-stu-id="36403-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="36403-115">Det gør du ved at give målsystemet et navn og angive URL-adressen til Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="36403-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="36403-116">Her er et eksempel på en Finance and Operations URL-adresse, som du kan angive: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="36403-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="36403-117">Når du har konfigureret dine målsystemer, kan du definere dine links.</span><span class="sxs-lookup"><span data-stu-id="36403-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="36403-118">Konfigurer links</span><span class="sxs-lookup"><span data-stu-id="36403-118">Configure links</span></span>

<span data-ttu-id="36403-119">Hvert link, der oprettes, har følgende definerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36403-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="36403-120">Link - Navnet på det link, der kun bruges til identifikation.</span><span class="sxs-lookup"><span data-stu-id="36403-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="36403-121">Aktivér dette link - Indstil til **Ja**, hvis linket skal kunne ses af brugere af Talent.</span><span class="sxs-lookup"><span data-stu-id="36403-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="36403-122">Vist navn – Angiv det navn, der skal vises som et link til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="36403-123">Disse data oversættes ikke i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="36403-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="36403-124">Overfladelink i formular - Vælg, hvilken side linket skal vises på.</span><span class="sxs-lookup"><span data-stu-id="36403-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="36403-125">Gruppe - Grupper er ikke påkrævet, men hvis du vil organisere dine links ved hjælp af grupper, skal du vælge en eksisterende gruppe eller oprette en ny ved hjælp af feltet **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="36403-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="36403-126">Destinationssystem - Vælg det destinationssystem, der blev oprettet ved hjælp af indstillingen **Konfigurer destinationssystem**.</span><span class="sxs-lookup"><span data-stu-id="36403-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="36403-127">Det er dette Finance and Operations-miljø, der bliver brugt, når du navigerer ved hjælp af linket.</span><span class="sxs-lookup"><span data-stu-id="36403-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="36403-128">Brug brugerens aktuelle firma - Vælg **Ja**, hvis du vil bruge brugerens aktuelle regnskabskontekst, når du navigerer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="36403-129">Hvis **Nej** er markeret, kan du vælge det regnskab, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="36403-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="36403-130">Menupunktet Mål – Angiv det menupunkt fra Finance and Operations, som linket skal bruge til navigation.</span><span class="sxs-lookup"><span data-stu-id="36403-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="36403-131">De menupunkter, du direkte kan navigere til, er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="36403-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="36403-132">Du kan finde det ønskede menupunkt ved at åbne Finance and Operations og åbne den side, der er målet for navigationen.</span><span class="sxs-lookup"><span data-stu-id="36403-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="36403-133">Kopiér menupunktet fra URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="36403-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="36403-134">F.eks. hvis linket skal gå til listen over medarbejdere i Finance and Operations, skal du angive den værdi, der vises efter "&mi" i URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="36403-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="36403-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="36403-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="36403-136">Menupunktet, der bruges til at navigere til listesiden over medarbejdere, er i dette eksempel: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="36403-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="36403-137">Link til datakilde – Vælg datakilden, som linket refererer til.</span><span class="sxs-lookup"><span data-stu-id="36403-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="36403-138">De mest almindelige kilder som f.eks. **Arbejder** og **Stilling** er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="36403-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="36403-139">Link til felt - (kommer snart) Dette felt gør det muligt at navigere direkte fra en enkelt post i Talent til en enkelt post i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="36403-140">Adgang til links</span><span class="sxs-lookup"><span data-stu-id="36403-140">Access to links</span></span>

<span data-ttu-id="36403-141">Systemadministratorer ser de nyoprettede links på de definerede sider, også selvom der i indstillingen **Aktivér dette link** er valgt **Nej**.</span><span class="sxs-lookup"><span data-stu-id="36403-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="36403-142">Dette kan bruges til test af links, før de bliver gjort synlige for andre medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="36403-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="36403-143">Alle andre roller kan kun se de konfigurerede links, når der i indstillingen **Aktivér dette link** er valgt **Ja**.</span><span class="sxs-lookup"><span data-stu-id="36403-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="36403-144">Medarbejdere, der har adgang til de sider, hvor linkene vises, har adgang til linksene.</span><span class="sxs-lookup"><span data-stu-id="36403-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="36403-145">Brugere kan også have sikkerhedsrettigheder i Finance and Operations, der er defineret, så de giver adgang til sider i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36403-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="36403-146">Hvis ikke, vises en sikkerhedsdialogboks, når linket bruges.</span><span class="sxs-lookup"><span data-stu-id="36403-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="36403-147">Andre ændringer/rettelser</span><span class="sxs-lookup"><span data-stu-id="36403-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="36403-148">Stillinger med en fremtidig startdato kan ikke tildeles til en ny medarbejder</span><span class="sxs-lookup"><span data-stu-id="36403-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="36403-149">Der er foretaget ændringer for at tillade medarbejdertildelinger til stillinger, der er dateret i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="36403-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="36403-150">Stillinger, der har startdatoer i fremtiden, kan vælges, og medarbejdertildelingen kan foretages, når arbejdsgangen (hvis arbejdsgangen er aktiveret) gemmes eller fuldføres.</span><span class="sxs-lookup"><span data-stu-id="36403-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="36403-151">Ny medarbejder kan ikke tildeles eksisterende stilling</span><span class="sxs-lookup"><span data-stu-id="36403-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="36403-152">Er der foretaget ændringer, så nye medarbejdertildelinger nu kan tildeles til eksisterende stillinger.</span><span class="sxs-lookup"><span data-stu-id="36403-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="36403-153">Anciennitetsdato/kontorlokation forsvinder, når ansættelsesstartdatoen er passeret, og posten gemmes</span><span class="sxs-lookup"><span data-stu-id="36403-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="36403-154">Der er foretaget ændringer af synligheden af **Anciennitetsdato** og **Kontorlokation**, når ændringer for tidligere medarbejdere gemmes.</span><span class="sxs-lookup"><span data-stu-id="36403-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="36403-155">Det er ikke muligt at angive data for ansættelser, der er dateret ud i fremtiden, på siden Arbejder</span><span class="sxs-lookup"><span data-stu-id="36403-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="36403-156">Ansættelsesoplysninger for ansættelser, der er dateret i fremtiden, er blevet deaktiveret på hovedsiden over arbejdere.</span><span class="sxs-lookup"><span data-stu-id="36403-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="36403-157">Ansættelsesdata kan angives via **Datoadministrator**-siderne.</span><span class="sxs-lookup"><span data-stu-id="36403-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="36403-158">Der vil blive foretage yderligere ændringer i fremtidige versioner, så ansættelsesdata kan angives direkte under arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="36403-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="36403-159">Føje ValidFrom og ValidTo til HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="36403-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="36403-160">DMF-objektet (Data Management Framework) HcmPersonalContactPersonEntity er blevet opdateret, så det indeholder "gyldig fra"- og "gyldig til"-datoer og muliggør integration af frynsegoder i bestemte situationer.</span><span class="sxs-lookup"><span data-stu-id="36403-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="36403-161">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="36403-161">Known issue</span></span>
- <span data-ttu-id="36403-162">**Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet.</span><span class="sxs-lookup"><span data-stu-id="36403-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="36403-163">**Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket.</span><span class="sxs-lookup"><span data-stu-id="36403-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="36403-164">Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="36403-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="36403-165">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="36403-165">(This issue will be fixed in the next platform update.)</span></span>
