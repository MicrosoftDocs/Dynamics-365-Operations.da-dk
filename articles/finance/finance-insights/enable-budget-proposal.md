---
title: Aktivere budgetforslag (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222528"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="48699-103">Aktivere budgetforslag (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="48699-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="48699-104">Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="48699-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="48699-105">Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø.</span><span class="sxs-lookup"><span data-stu-id="48699-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="48699-106">Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="48699-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="48699-107">(Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)</span><span class="sxs-lookup"><span data-stu-id="48699-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="48699-108">Spring dette trin over, hvis du bruger version 10.0.20 eller senere, eller hvis du bruger en installation af Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="48699-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="48699-109">Finance Insights-team burde allerede have aktiveret funktionen til dig.</span><span class="sxs-lookup"><span data-stu-id="48699-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="48699-110">Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="48699-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="48699-111">Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="48699-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="48699-112">Vælg **Søg efter opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="48699-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="48699-113">Søg efter **Budgetforslag**, og aktiver funktionen.</span><span class="sxs-lookup"><span data-stu-id="48699-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="48699-114">Gå til **Budget \> Opsætning \> Grundlæggende budget \> Budgetforslag (prøveversion)**, og vælg **Aktiver funktion**.</span><span class="sxs-lookup"><span data-stu-id="48699-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
