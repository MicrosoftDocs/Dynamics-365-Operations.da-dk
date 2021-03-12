---
title: Aktivere budgetforslag (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995134"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="084e9-103">Aktivere budgetforslag (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="084e9-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="084e9-104">Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="084e9-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="084e9-105">Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø.</span><span class="sxs-lookup"><span data-stu-id="084e9-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="084e9-106">Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="084e9-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="084e9-107">(Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)</span><span class="sxs-lookup"><span data-stu-id="084e9-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="084e9-108">Hvis din installation af Microsoft Dynamics 365 Finance er en Service Fabric-installation, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="084e9-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="084e9-109">Finance Insights-team burde allerede have aktiveret funktionen til dig.</span><span class="sxs-lookup"><span data-stu-id="084e9-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="084e9-110">Hvis du ikke kan se funktionen i arbejdsområdet **Administration af funktioner**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du sende en e-mail til [Finance Insights Preview team](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="084e9-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="084e9-111">Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="084e9-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="084e9-112">Vælg **Søg efter opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="084e9-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="084e9-113">Søg efter **Budgetforslag**, og aktiver funktionen.</span><span class="sxs-lookup"><span data-stu-id="084e9-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="084e9-114">Gå til **Budget \> Opsætning \> Grundlæggende budget \> Budgetforslag (prøveversion)**, og vælg **Aktiver funktion**.</span><span class="sxs-lookup"><span data-stu-id="084e9-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="084e9-115">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="084e9-115">Privacy notice</span></span>
<span data-ttu-id="084e9-116">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="084e9-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
