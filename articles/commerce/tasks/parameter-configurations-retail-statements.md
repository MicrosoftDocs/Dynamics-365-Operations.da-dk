---
title: Konfigurere parametre, som påvirker detailopgørelser
description: Dette emne viser konfigurationer for Commerce-parametre, der påvirker, hvordan opgørelser oprettes og bogføres.
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021987"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="0e92e-103">Konfigurere parametre, som påvirker detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="0e92e-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0e92e-104">Dette emne viser konfigurationer for Commerce-parametre, der påvirker, hvordan opgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="0e92e-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="0e92e-105">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="0e92e-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="0e92e-106">I navigationsruden skal du gå til **Moduler > Retail og Commerce > Konfiguration af hovedkontor > Parametre > Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="0e92e-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="0e92e-107">Vælg fanen **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="0e92e-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="0e92e-108">Vælg **Ja**, hvis du specifikt vil bogføre de periodiske rabatbeløb.</span><span class="sxs-lookup"><span data-stu-id="0e92e-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="0e92e-109">Vælg **Standard** for at bruge standardkonti, eller vælg **Periodisk**, hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.</span><span class="sxs-lookup"><span data-stu-id="0e92e-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="0e92e-110">Vælg **Oversigt**, hvis lagerlinjer skal samles, når det er muligt.</span><span class="sxs-lookup"><span data-stu-id="0e92e-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="0e92e-111">Vælg **Ja**, hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="0e92e-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="0e92e-112">Vælg **Ja**, hvis transaktioner med deponering til pengeskab skal samles.</span><span class="sxs-lookup"><span data-stu-id="0e92e-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="0e92e-113">Vælg **Ja**, hvis transaktioner med indsættelse i banken skal samles.</span><span class="sxs-lookup"><span data-stu-id="0e92e-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="0e92e-114">Vælg **Ja** for at aktivere sammenlægning for bogføring af opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="0e92e-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="0e92e-115">Vælg **Ja** for at oprette og behandle ordrer parallelt, når opgørelser bogføres.</span><span class="sxs-lookup"><span data-stu-id="0e92e-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="0e92e-116">Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.</span><span class="sxs-lookup"><span data-stu-id="0e92e-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="0e92e-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0e92e-117">Select **Save**.</span></span>

