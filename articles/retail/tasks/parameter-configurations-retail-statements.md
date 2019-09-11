---
title: Konfigurere Detailparametre, som påvirker detailopgørelser
description: Dette emne viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867265"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="4d076-103">Konfigurere Detailparametre, som påvirker detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="4d076-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4d076-104">Dette emne viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="4d076-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="4d076-105">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="4d076-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4d076-106">I navigationsruden skal du gå til **Moduler > Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre**.</span><span class="sxs-lookup"><span data-stu-id="4d076-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="4d076-107">Vælg fanen **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="4d076-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="4d076-108">Vælg **Ja**, hvis du specifikt vil bogføre de periodiske rabatbeløb.</span><span class="sxs-lookup"><span data-stu-id="4d076-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="4d076-109">Vælg **Standard** for at bruge standardkonti, eller vælg **Periodisk**, hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.</span><span class="sxs-lookup"><span data-stu-id="4d076-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="4d076-110">Vælg **Oversigt**, hvis lagerlinjer skal samles, når det er muligt.</span><span class="sxs-lookup"><span data-stu-id="4d076-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="4d076-111">Vælg **Ja**, hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="4d076-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="4d076-112">Vælg **Ja**, hvis transaktioner med deponering til pengeskab skal samles.</span><span class="sxs-lookup"><span data-stu-id="4d076-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="4d076-113">Vælg **Ja**, hvis transaktioner med indsættelse i banken skal samles.</span><span class="sxs-lookup"><span data-stu-id="4d076-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="4d076-114">Vælg **Ja** for at aktivere sammenlægning for bogføring af opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="4d076-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="4d076-115">Vælg **Ja** for at oprette og behandle ordrer parallelt, når opgørelser bogføres.</span><span class="sxs-lookup"><span data-stu-id="4d076-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="4d076-116">Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.</span><span class="sxs-lookup"><span data-stu-id="4d076-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="4d076-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="4d076-117">Select **Save**.</span></span>

