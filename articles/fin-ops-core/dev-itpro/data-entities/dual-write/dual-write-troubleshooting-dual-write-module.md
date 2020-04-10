---
title: Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med dobbeltskrivningsmodulet i Finance and Operations-apps.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172754"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="53464-103">Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="53464-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="53464-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="53464-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="53464-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med **dobbeltskrivningsmodulet** i Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="53464-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53464-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="53464-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="53464-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="53464-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="53464-108">Du kan ikke indlæse dobbeltskrivningsmodulet i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="53464-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="53464-109">Hvis du ikke kan åbne **Dobbeltskrivning**-siden ved at vælge titlen **Dobbeltskrivning** i **Datastyring**-arbejdsområdet, er dataintegrationstjenesten sandsynligvis nede.</span><span class="sxs-lookup"><span data-stu-id="53464-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="53464-110">Opret en supportanmodning for at anmode om genstart af dataintegrationstjenesten.</span><span class="sxs-lookup"><span data-stu-id="53464-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="53464-111">Fejl, når du forsøger at oprette en ny enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="53464-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="53464-112">**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator</span><span class="sxs-lookup"><span data-stu-id="53464-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="53464-113">Du kan få vist følgende fejlmeddelelse, når du forsøger at konfigurere en ny enhed til dobbeltskrivning:</span><span class="sxs-lookup"><span data-stu-id="53464-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="53464-114">*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 401 (uautoriseret)*</span><span class="sxs-lookup"><span data-stu-id="53464-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="53464-115">Denne fejl opstår, fordi det kun er en Azure AD-lejeradministrator, der kan tilføje en ny enhedstilknytning.</span><span class="sxs-lookup"><span data-stu-id="53464-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="53464-116">Du kan løse problemet ved at logge på Finance and Operations-appen som Azure AD-lejeradministrator.</span><span class="sxs-lookup"><span data-stu-id="53464-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="53464-117">Du skal også gå til web.PowerApps.com og validere forbindelsen igen.</span><span class="sxs-lookup"><span data-stu-id="53464-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="53464-118">Fejl, når du åbner brugergrænsefladen til dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="53464-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="53464-119">Du kan få vist følgende fejlmeddelelse, når du forsøger at få adgang til dobbeltskrivning fra arbejdsområdet **Datastyring**:</span><span class="sxs-lookup"><span data-stu-id="53464-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="53464-120">*login.microsoftonline.com afviste at oprette forbindelse.*</span><span class="sxs-lookup"><span data-stu-id="53464-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="53464-121">Du kan løse problemet ved at logge på ved hjælp af et InPrivate-vindue i Microsoft Edge, et incognito-vindue i Chromium eller et incognito-vindue i Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="53464-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="53464-122">Du skal også fjerne blokeringen af eller rydde tredjepartscookies.</span><span class="sxs-lookup"><span data-stu-id="53464-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="53464-123">Fejl under sammenkædning af miljøet ved dobbeltskrivning eller tilføjelse af en ny enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="53464-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="53464-124">**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator</span><span class="sxs-lookup"><span data-stu-id="53464-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="53464-125">Der kan opstå følgende fejl under sammenkædning eller oprettelse af tilknytninger:</span><span class="sxs-lookup"><span data-stu-id="53464-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="53464-126">*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (tokenexchange).<br> Sessions-id: \<dit sessions-id\><br> Rodaktivitets-id: \<dit rod-aktivitets-id\>*</span><span class="sxs-lookup"><span data-stu-id="53464-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="53464-127">Denne fejl kan forekomme, hvis du ikke har de nødvendige rettigheder til at sammenkæde dobbeltskrivning eller oprette tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="53464-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="53464-128">Du skal bruge en Azure AD-lejeradministratorkonto for at kunne sammenkæde miljøer og tilføje nye enhedstilknytninger.</span><span class="sxs-lookup"><span data-stu-id="53464-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="53464-129">Men når du har udført installationen, kan du bruge en ikke-administratorkonto til at overvåge status og redigere tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="53464-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="53464-130">Fejl, når du stopper tilknytningen af enheder</span><span class="sxs-lookup"><span data-stu-id="53464-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="53464-131">Du kan få vist følgende fejlmeddelelse, når du forsøger at standse tilknytninger af enheder:</span><span class="sxs-lookup"><span data-stu-id="53464-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="53464-132">*\[Forbudt\], \[{"status": 403, "kilde": "","meddelelse":"Fejl fra tokenudveksling: Brugeren har ikke adgang til forbindelsen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], fjernserveren returnerede en fejl: (403) forbudt.*</span><span class="sxs-lookup"><span data-stu-id="53464-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="53464-133">Denne fejl opstår, når det sammenkædede Common Data Service-miljø ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="53464-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="53464-134">Du kan løse problemet ved at oprette en supportanmodning til dataintegrationsteamet.</span><span class="sxs-lookup"><span data-stu-id="53464-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="53464-135">Tilknyt netværkssporingen, så dataintegrationsteamet kan markere tilknytningerne som **Kører ikke** i backend.</span><span class="sxs-lookup"><span data-stu-id="53464-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
