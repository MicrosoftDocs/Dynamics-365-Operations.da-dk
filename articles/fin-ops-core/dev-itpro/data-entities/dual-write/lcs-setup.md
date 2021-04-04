---
title: Konfiguration af dobbeltskrivning fra Lifecycle Services
description: Dette emne beskriver, hvordan du konfigurerer en forbindelse med dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567714"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="31a35-103">Konfiguration af dobbeltskrivning fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="31a35-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="31a35-104">I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Dataverse-miljø fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="31a35-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="31a35-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="31a35-105">Prerequisites</span></span>

<span data-ttu-id="31a35-106">Du skal være administrator for at kunne konfigurere en forbindelse med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="31a35-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="31a35-107">Du skal have adgang lejeren.</span><span class="sxs-lookup"><span data-stu-id="31a35-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="31a35-108">Du skal være administrator i Finance and Operations-miljøer og Dataverse-miljøer.</span><span class="sxs-lookup"><span data-stu-id="31a35-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="31a35-109">Oprette en forbindelse med to skrivninger</span><span class="sxs-lookup"><span data-stu-id="31a35-109">Set up a dual-write connection</span></span>

<span data-ttu-id="31a35-110">Følg disse trin for at oprette forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="31a35-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="31a35-111">Gå til dit projekt i LCS.</span><span class="sxs-lookup"><span data-stu-id="31a35-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="31a35-112">Vælg **Konfigurer** for at installere et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="31a35-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="31a35-113">Vælg versionen.</span><span class="sxs-lookup"><span data-stu-id="31a35-113">Select the version.</span></span> 
4. <span data-ttu-id="31a35-114">Vælg topologien.</span><span class="sxs-lookup"><span data-stu-id="31a35-114">Select the topology.</span></span> <span data-ttu-id="31a35-115">Hvis der kun er én tilgængelig topologi, vælges den automatisk.</span><span class="sxs-lookup"><span data-stu-id="31a35-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="31a35-116">Afslut de første trin i guiden **Installationsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="31a35-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="31a35-117">Udfør ét af følgende trin på fanen **Dataverse**:</span><span class="sxs-lookup"><span data-stu-id="31a35-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="31a35-118">Hvis der allerede er klargjort et Dataverse-miljø til din lejer, kan du vælge det.</span><span class="sxs-lookup"><span data-stu-id="31a35-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="31a35-119">Angiv indstillingen **Konfigurer Dataverse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31a35-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="31a35-120">Vælg det miljø, der skal integreres med dine Finance and Operations-data, i kolonnen **Tilgængelige miljøer**.</span><span class="sxs-lookup"><span data-stu-id="31a35-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="31a35-121">Listen omfatter alle de miljøer, hvor du har administratorrettigheder.</span><span class="sxs-lookup"><span data-stu-id="31a35-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="31a35-122">Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="31a35-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse-fanen, når et Dataverse-miljø allerede er klargjort til din lejer](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="31a35-124">Hvis din lejer ikke allerede har et Dataverse-miljø, vil der blive klargjort et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="31a35-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="31a35-125">Angiv indstillingen **Konfigurer Dataverse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31a35-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="31a35-126">Angiv et navn for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="31a35-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="31a35-127">Vælg det område, som miljøet skal installeres i.</span><span class="sxs-lookup"><span data-stu-id="31a35-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="31a35-128">Vælg standardsprog og valuta for miljøet.</span><span class="sxs-lookup"><span data-stu-id="31a35-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="31a35-129">Du kan ikke ændre sproget og valutaen senere.</span><span class="sxs-lookup"><span data-stu-id="31a35-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="31a35-130">Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="31a35-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse-fanen, når din lejer ikke allerede har et Dataverse-miljø](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="31a35-132">Afslut de resterende trin i guiden **Installationsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="31a35-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="31a35-133">Når miljøet har status **Installeret**, skal du åbne siden med miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="31a35-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="31a35-134">Afsnittet med **Power Platform Integration** viser navnene på Finance and Operations-miljøet og det sammenkædede Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="31a35-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Afsnittet Power Platform Integration](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="31a35-136">En administrator af Finance and Operations-miljøet skal logge på LCS og vælge **Link til CDS for Apps** for at fuldføre sammenkædningen.</span><span class="sxs-lookup"><span data-stu-id="31a35-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="31a35-137">På siden med miljødetaljer vises administratorens kontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="31a35-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="31a35-138">Når sammenkædningen er fuldført, opdateres status til **Miljøsammenkædning er fuldført**.</span><span class="sxs-lookup"><span data-stu-id="31a35-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="31a35-139">Hvis du vil åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og styre, hvilke skabeloner der findes, skal du vælge **Link til CDS For Apps**.</span><span class="sxs-lookup"><span data-stu-id="31a35-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Knappen Link til CDS for Apps i afsnittet Power Platform Integration](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="31a35-141">Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS.</span><span class="sxs-lookup"><span data-stu-id="31a35-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="31a35-142">Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="31a35-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]