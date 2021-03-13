---
title: Foretage fejlfinding af problemer under den indledende opsætning
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: cfbc1ab3ef6d47f6ec2d8ca4ca4b8940784e6e49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129975"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="25f29-103">Foretage fejlfinding af problemer under den indledende opsætning</span><span class="sxs-lookup"><span data-stu-id="25f29-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="25f29-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="25f29-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="25f29-105">Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.</span><span class="sxs-lookup"><span data-stu-id="25f29-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25f29-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="25f29-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="25f29-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="25f29-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="25f29-108">Du kan ikke sammenkæde en Finance and Operations-app med Dataverse</span><span class="sxs-lookup"><span data-stu-id="25f29-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="25f29-109">**Påkrævet rolle for at konfigurere dobbeltskrivning:** Systemadministrator i Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="25f29-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="25f29-110">Fejl på siden **Opsætning af sammenkædning til Dataverse** er normalt forårsaget af ufuldstændige opsætnings- eller rettighedsproblemer.</span><span class="sxs-lookup"><span data-stu-id="25f29-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="25f29-111">Kontroller, at hele tilstandskontrollen bliver gennemført tilfredsstillende på siden **Opsætning af sammenkædning til Dataverse**, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="25f29-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="25f29-112">Du kan ikke sammenkæde med Dobbeltskrivning, medmindre hele tilstandskontrollen gennemføres tilfredsstillende.</span><span class="sxs-lookup"><span data-stu-id="25f29-112">You can't link dual-write unless the whole health check passes.</span></span>

![Vellykket tilstandskontrol](media/health_check.png)

<span data-ttu-id="25f29-114">Du skal have rettigheder som Azure AD-lejeradministrator for at kunne sammenkæde Finance and Operations- og Dataverse-miljøer.</span><span class="sxs-lookup"><span data-stu-id="25f29-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="25f29-115">Når du har kædet miljøerne sammen, kan brugerne logge på ved hjælp af deres legitimationsoplysninger til deres konto og opdatere en eksisterende tabeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="25f29-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="25f29-116">Fejl, når du åbner siden Sammenkædning med Dataverse</span><span class="sxs-lookup"><span data-stu-id="25f29-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="25f29-117">**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator</span><span class="sxs-lookup"><span data-stu-id="25f29-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="25f29-118">Du kan få vist følgende fejlmeddelelse, når du åbner **Sammenkædning med Dataverse** i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="25f29-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="25f29-119">*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 404 (Ikke fundet).*</span><span class="sxs-lookup"><span data-stu-id="25f29-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="25f29-120">Denne fejl opstår, når samtykketrinnet ikke blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="25f29-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="25f29-121">Hvis du vil validere, om samtykketrinnet er fuldført, skal du logge på portal.Azure.com ved hjælp af Azure AD-lejeradministratorkontoen og se, om den tredjepartsapp, der har id'et **33976c19-1db5-4c02-810e-c243db79efde**, vises på listen over Azure AD **virksomhedsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="25f29-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="25f29-122">Hvis ikke, skal du give samtykke til appen.</span><span class="sxs-lookup"><span data-stu-id="25f29-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="25f29-123">Du kan give appsamtykke ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="25f29-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="25f29-124">Åbn følgende URL-adresse ved hjælp af dine administratorlegitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="25f29-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="25f29-125">Du bliver bedt om at give dit samtykke.</span><span class="sxs-lookup"><span data-stu-id="25f29-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="25f29-126">Vælg **Accepter** for at angive, at du giver samtykke til at installere appen, der har id'et **33976c19-1db5-4c02-810e-c243db79efde** i din lejer.</span><span class="sxs-lookup"><span data-stu-id="25f29-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="25f29-127">Denne app kræves for at kunne oprette sammenkæde Dataverse- og Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="25f29-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="25f29-128">Hvis du har problemer med dette trin, skal du åbne browseren i Incognito-tilstand (i Google Chrome) eller i InPrivate-tilstand (i Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="25f29-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="25f29-129">Kontrollere, at firmadata og dobbeltskrivningsteams er konfigureret korrekt under sammenkædning</span><span class="sxs-lookup"><span data-stu-id="25f29-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="25f29-130">For at sikre, at dobbeltskrivningen fungerer korrekt, oprettes de firmaer, du vælger under konfigurationen, i Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="25f29-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="25f29-131">Disse firmaer er som standard skrivebeskyttede, og egenskaben **IsDualWriteEnable** er indstillet til **True**.</span><span class="sxs-lookup"><span data-stu-id="25f29-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="25f29-132">Derudover oprettes standardejer-virksomhedsenheden og -teamet og inkluderer firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="25f29-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="25f29-133">Før du aktiverer tilknytningerne, skal du kontrollere, at standardteamejeren er angivet.</span><span class="sxs-lookup"><span data-stu-id="25f29-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="25f29-134">Udfør følgende trin for at finde tabellen **Firmaer (CDM\_Firma)**.</span><span class="sxs-lookup"><span data-stu-id="25f29-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="25f29-135">I den modelbaserede app i Dynamics 365 skal du vælge filteret i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="25f29-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="25f29-136">Vælg **Firma** på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="25f29-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="25f29-137">Vælg **Kør** for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="25f29-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="25f29-138">Vælg det regnskab, der blev sammenkædet, da du konfigurerede dobbelt skrivning.</span><span class="sxs-lookup"><span data-stu-id="25f29-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="25f29-139">Kontroller, at der er en værdi i kolonnen **Standardejerteam**.</span><span class="sxs-lookup"><span data-stu-id="25f29-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="25f29-140">I følgende illustration er kolonnen **Standardejerteam** indstillet til **USMF-dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="25f29-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Kontrollere standardejerteamet](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="25f29-142">Finde grænsen for antallet af juridiske tabeller eller firmaer, der kan sammenkædes ved dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="25f29-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="25f29-143">Du kan få vist følgende fejlmeddelelse, når du forsøger at aktivere tilknytninger:</span><span class="sxs-lookup"><span data-stu-id="25f29-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="25f29-144">*Fejl under dobbeltskrivning – plugin-registrering mislykkedes: \[(det er ikke muligt at hente partitionstilknytningen for projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Fejl: Overstiger det maksimale antal partitioner, der er tilladt for tilknytning af DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Der opstod en eller flere fejl.*</span><span class="sxs-lookup"><span data-stu-id="25f29-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="25f29-145">Den aktuelle grænse, når du sammenkæder miljøerne, er ca. 40 juridiske tabeller.</span><span class="sxs-lookup"><span data-stu-id="25f29-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="25f29-146">Denne fejl opstår, hvis du forsøger at aktivere tilknytninger, og mere end 40 juridiske tabeller sammenkædes mellem miljøerne.</span><span class="sxs-lookup"><span data-stu-id="25f29-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>
