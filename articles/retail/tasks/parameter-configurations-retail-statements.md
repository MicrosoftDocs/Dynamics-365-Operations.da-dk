--- 
title: "Parameterkonfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0c93633e92221264cc6a67c74d62edaa59bdbd2f
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="67f66-103">Parameterkonfigurationer for detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="67f66-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="67f66-104">Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="67f66-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="67f66-105">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="67f66-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="67f66-106">Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.</span><span class="sxs-lookup"><span data-stu-id="67f66-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="67f66-107">Klik på fanen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="67f66-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="67f66-108">Vælg "Ja", hvis du specifikt vil bogføre de periodiske rabatbeløb.</span><span class="sxs-lookup"><span data-stu-id="67f66-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="67f66-109">Vælg "Standard" for at bruge standardkonti, eller Vælg "Periodisk", hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.</span><span class="sxs-lookup"><span data-stu-id="67f66-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="67f66-110">Vælg "Oversigt", hvis lagerlinjer skal samles, når det er muligt.</span><span class="sxs-lookup"><span data-stu-id="67f66-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="67f66-111">Vælg "Ja", hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="67f66-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="67f66-112">Vælg "Ja", hvis transaktioner med deponering til pengeskab skal samles.</span><span class="sxs-lookup"><span data-stu-id="67f66-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="67f66-113">Vælg "Ja", hvis transaktioner med indsættelse i banken skal samles.</span><span class="sxs-lookup"><span data-stu-id="67f66-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="67f66-114">Vælg "Ja" for at aktivere sammenlægning for bogføring af opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="67f66-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="67f66-115">Vælg "Ja" for at oprette og behandle ordrer parallelt, når opgørelser bogføres.</span><span class="sxs-lookup"><span data-stu-id="67f66-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="67f66-116">Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.</span><span class="sxs-lookup"><span data-stu-id="67f66-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="67f66-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="67f66-117">Click Save.</span></span>


