---
title: Installation med to skrivninger fra Lifecycle Services
description: I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998102"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="37543-103">Installation med to skrivninger fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="37543-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="37543-104">I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="37543-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37543-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="37543-105">Prerequisites</span></span>

<span data-ttu-id="37543-106">Du skal være administrator for at kunne konfigurere en forbindelse med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="37543-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="37543-107">Du skal have adgang lejeren.</span><span class="sxs-lookup"><span data-stu-id="37543-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="37543-108">Du skal være administrator i Finance and Operations-miljøer og Common Data Service-miljøer.</span><span class="sxs-lookup"><span data-stu-id="37543-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="37543-109">Oprette en forbindelse med to skrivninger</span><span class="sxs-lookup"><span data-stu-id="37543-109">Set up a dual-write connection</span></span>

<span data-ttu-id="37543-110">Følg disse trin for at oprette forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="37543-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="37543-111">Gå til dit projekt i LCS.</span><span class="sxs-lookup"><span data-stu-id="37543-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="37543-112">Vælg **Konfigurer** for at installere et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="37543-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="37543-113">Vælg versionen.</span><span class="sxs-lookup"><span data-stu-id="37543-113">Select the version.</span></span> 
4. <span data-ttu-id="37543-114">Vælg topologien.</span><span class="sxs-lookup"><span data-stu-id="37543-114">Select the topology.</span></span> <span data-ttu-id="37543-115">Hvis der kun er én tilgængelig topologi, vælges den automatisk.</span><span class="sxs-lookup"><span data-stu-id="37543-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="37543-116">Afslut de første trin i guiden **Installationsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="37543-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="37543-117">Udfør ét af følgende trin på fanen **Common Data Service** :</span><span class="sxs-lookup"><span data-stu-id="37543-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="37543-118">Hvis der allerede er klargjort et Common Data Service-miljø til din lejer, kan du vælge det.</span><span class="sxs-lookup"><span data-stu-id="37543-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="37543-119">Angiv indstillingen **Konfigurer Common Data Service** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="37543-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="37543-120">Vælg det miljø, der skal integreres med dine Finance and Operations-data, i feltet **Tilgængelige miljøer**.</span><span class="sxs-lookup"><span data-stu-id="37543-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="37543-121">Listen omfatter alle de miljøer, hvor du har administratorrettigheder.</span><span class="sxs-lookup"><span data-stu-id="37543-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="37543-122">Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="37543-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service-fanen, når et Common Data Service-miljø allerede er klargjort til din lejer](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="37543-124">Hvis din lejer ikke allerede har et Common Data Service-miljø, vil der blive klargjort et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="37543-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="37543-125">Angiv indstillingen **Konfigurer Common Data Service** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="37543-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="37543-126">Angiv et navn for Common Data Service-miljøet.</span><span class="sxs-lookup"><span data-stu-id="37543-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="37543-127">Vælg det område, som miljøet skal installeres i.</span><span class="sxs-lookup"><span data-stu-id="37543-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="37543-128">Vælg standardsprog og valuta for miljøet.</span><span class="sxs-lookup"><span data-stu-id="37543-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="37543-129">Du kan ikke ændre sproget og valutaen senere.</span><span class="sxs-lookup"><span data-stu-id="37543-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="37543-130">Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="37543-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service-fanen, når din lejer ikke allerede har et Common Data Service-miljø](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="37543-132">Afslut de resterende trin i guiden **Installationsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="37543-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="37543-133">Når miljøet har status **Installeret** , skal du åbne siden med miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="37543-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="37543-134">Afsnittet med **Common Data Service-miljøoplysninger** viser navnene på Finance and Operations-miljøet og det sammenkædede Common Data Service-miljø.</span><span class="sxs-lookup"><span data-stu-id="37543-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Afsnittet med Common Data Service-miljøoplysninger](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="37543-136">En administrator af Finance and Operations-miljøet skal logge på LCS og vælge **Link til CDS for Apps** for at fuldføre sammenkædningen.</span><span class="sxs-lookup"><span data-stu-id="37543-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="37543-137">På siden med miljødetaljer vises administratorens kontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="37543-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="37543-138">Når sammenkædningen er fuldført, opdateres status til **Miljøsammenkædning er fuldført**.</span><span class="sxs-lookup"><span data-stu-id="37543-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="37543-139">Hvis du vil åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og styre, hvilke skabeloner der findes, skal du vælge **Link til CDS For Apps**.</span><span class="sxs-lookup"><span data-stu-id="37543-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Knappen Link til CDS for Apps i området med Common Data Service-miljøoplysninger](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="37543-141">Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS.</span><span class="sxs-lookup"><span data-stu-id="37543-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="37543-142">Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="37543-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
