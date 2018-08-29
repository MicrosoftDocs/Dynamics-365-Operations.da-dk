--- 
title: "Konfigurere parametre for Retail, der påvirker detailopgørelser"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="a9bd4-103">Konfigurere parametre for Retail, der påvirker detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="a9bd4-103">Configure Retail parameters that affect retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a9bd4-104">Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="a9bd4-105">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="a9bd4-106">Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="a9bd4-107">Klik på fanen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="a9bd4-108">Vælg "Ja", hvis du specifikt vil bogføre de periodiske rabatbeløb.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="a9bd4-109">Vælg "Standard" for at bruge standardkonti, eller Vælg "Periodisk", hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="a9bd4-110">Vælg "Oversigt", hvis lagerlinjer skal samles, når det er muligt.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="a9bd4-111">Vælg "Ja", hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="a9bd4-112">Vælg "Ja", hvis transaktioner med deponering til pengeskab skal samles.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="a9bd4-113">Vælg "Ja", hvis transaktioner med indsættelse i banken skal samles.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="a9bd4-114">Vælg "Ja" for at aktivere sammenlægning for bogføring af opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="a9bd4-115">Vælg "Ja" for at oprette og behandle ordrer parallelt, når opgørelser bogføres.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="a9bd4-116">Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="a9bd4-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a9bd4-117">Click Save.</span></span>


