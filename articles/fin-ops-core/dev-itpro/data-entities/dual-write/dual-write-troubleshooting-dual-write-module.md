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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997368"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="3d469-103">Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3d469-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d469-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3d469-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3d469-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med **dobbeltskrivningsmodulet** i Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="3d469-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d469-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="3d469-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3d469-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="3d469-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="3d469-108">Du kan ikke indlæse dobbeltskrivningsmodulet i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3d469-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="3d469-109">Hvis du ikke kan åbne **Dobbeltskrivning** -siden ved at vælge titlen **Dobbeltskrivning** i **Datastyring** -arbejdsområdet, er dataintegrationstjenesten sandsynligvis nede.</span><span class="sxs-lookup"><span data-stu-id="3d469-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="3d469-110">Opret en supportanmodning for at anmode om genstart af dataintegrationstjenesten.</span><span class="sxs-lookup"><span data-stu-id="3d469-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="3d469-111">Fejl, når du forsøger at oprette en ny enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="3d469-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="3d469-112">**Påkrævede legitimationsoplysninger for at løse problemet:** Den samme bruger, der har konfigureret dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="3d469-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="3d469-113">Du kan få vist følgende fejlmeddelelse, når du forsøger at konfigurere en ny enhed til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="3d469-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="3d469-114">Den eneste bruger, der kan oprette en tilknytning, er den bruger, der har konfigureret dobbeltskrivningsforbindelsen.</span><span class="sxs-lookup"><span data-stu-id="3d469-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="3d469-115">*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 401 (uautoriseret)*</span><span class="sxs-lookup"><span data-stu-id="3d469-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="3d469-116">Fejl, når du åbner brugergrænsefladen til dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="3d469-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="3d469-117">Du kan få vist følgende fejlmeddelelse, når du forsøger at få adgang til dobbeltskrivning fra arbejdsområdet **Datastyring** :</span><span class="sxs-lookup"><span data-stu-id="3d469-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="3d469-118">*login.microsoftonline.com afviste at oprette forbindelse.*</span><span class="sxs-lookup"><span data-stu-id="3d469-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="3d469-119">Du kan løse problemet ved at logge på ved hjælp af et InPrivate-vindue i Microsoft Edge, et incognito-vindue i Chromium eller et incognito-vindue i Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="3d469-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="3d469-120">Du skal også fjerne blokeringen af eller rydde tredjepartscookies.</span><span class="sxs-lookup"><span data-stu-id="3d469-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="3d469-121">Fejl under sammenkædning af miljøet ved dobbeltskrivning eller tilføjelse af en ny enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="3d469-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="3d469-122">**Påkrævet rolle for at løse problemet:** Systemadministrator i både Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3d469-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="3d469-123">Der kan opstå følgende fejl under sammenkædning eller oprettelse af tilknytninger:</span><span class="sxs-lookup"><span data-stu-id="3d469-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="3d469-124">*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (tokenexchange).<br> Sessions-id: \<your session id\><br> Rodaktivitets-id: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="3d469-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="3d469-125">Denne fejl kan forekomme, hvis du ikke har de nødvendige rettigheder til at sammenkæde dobbeltskrivning eller oprette tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="3d469-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="3d469-126">Denne fejl kan også opstå, hvis Common Data Service-miljøet blev nulstillet uden at fjerne tilknytningen til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="3d469-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="3d469-127">Enhver bruger med rollen Systemadministrator i både Finance and Operations-apps og Common Data Service kan sammenkæde miljøerne.</span><span class="sxs-lookup"><span data-stu-id="3d469-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="3d469-128">Kun den bruger, der har konfigureret dobbeltskrivningsforbindelsen, kan tilføje nye enhedstilknytninger.</span><span class="sxs-lookup"><span data-stu-id="3d469-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="3d469-129">Efter installationen kan enhver bruger med rollen Systemadministrator overvåge status og redigere tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="3d469-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="3d469-130">Fejl, når du stopper tilknytningen af enheder</span><span class="sxs-lookup"><span data-stu-id="3d469-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="3d469-131">Du kan få vist følgende fejlmeddelelse, når du forsøger at standse tilknytninger af enheder:</span><span class="sxs-lookup"><span data-stu-id="3d469-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="3d469-132">*\[Forbudt\], \[{"status": 403, "kilde": "","meddelelse":"Fejl fra tokenudveksling: Brugeren har ikke adgang til forbindelsen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], fjernserveren returnerede en fejl: (403) forbudt.*</span><span class="sxs-lookup"><span data-stu-id="3d469-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="3d469-133">Denne fejl opstår, når det sammenkædede Common Data Service-miljø ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="3d469-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="3d469-134">Du kan løse problemet ved at oprette en supportanmodning til dataintegrationsteamet.</span><span class="sxs-lookup"><span data-stu-id="3d469-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="3d469-135">Tilknyt netværkssporingen, så dataintegrationsteamet kan markere tilknytningerne som **Kører ikke** i backend.</span><span class="sxs-lookup"><span data-stu-id="3d469-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="3d469-136">Der opstod en fejl under forsøg på at starte en enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="3d469-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="3d469-137">Du kan få vist en fejl som følgende, når du forsøger at angive denne tilstand for en tilknytning til **Kører** :</span><span class="sxs-lookup"><span data-stu-id="3d469-137">You might receive an error like the following when you try to set that state of a mapping to **Running** :</span></span>

<span data-ttu-id="3d469-138">*Den indledende datasynkronisering kan ikke fuldføres. Fejl: dobbeltskrivningsfejl - plugin-registrering mislykkedes: Der kan ikke oprettes metadata til dobbeltskrivningsopslag. Objektreference er ikke indstillet til en forekomst af et objekt.*</span><span class="sxs-lookup"><span data-stu-id="3d469-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="3d469-139">Rettelsen til denne fejl afhænger af årsagen til fejlen:</span><span class="sxs-lookup"><span data-stu-id="3d469-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="3d469-140">Hvis tilknytningen har afhængige tilknytninger, skal du sørge for at aktivere de afhængige tilknytninger for denne enhedstilknytning.</span><span class="sxs-lookup"><span data-stu-id="3d469-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="3d469-141">Tilknytningen mangler muligvis kilde- eller destinationsfelter.</span><span class="sxs-lookup"><span data-stu-id="3d469-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="3d469-142">Hvis der mangler et felt i Finance and Operations-appen, skal du følge trinnene i afsnittet [Problemer med manglende enhedsfelter i tilknytninger](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="3d469-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="3d469-143">Hvis der mangler et felt i Common Data Service, skal du klikke på knappen **Opdater enheder** på tilknytningen, så felterne automatisk udfyldes i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="3d469-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
