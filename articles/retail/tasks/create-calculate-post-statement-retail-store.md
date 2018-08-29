--- 
title: "Oprette, beregne og bogføre opgørelser for en detailbutik"
description: "Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1c31c849c4c72762f0fdeb3f1d256cd3529394b2
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="5096e-103">Oprette, beregne og bogføre opgørelser for en detailbutik</span><span class="sxs-lookup"><span data-stu-id="5096e-103">Create, calculate, and post statements for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5096e-104">Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik.</span><span class="sxs-lookup"><span data-stu-id="5096e-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="5096e-105">Der er også batchjob, der kan konfigureres for de samme opgaver.</span><span class="sxs-lookup"><span data-stu-id="5096e-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="5096e-106">Trin til konfiguration og kørsel af batchjob findes i andre emner.</span><span class="sxs-lookup"><span data-stu-id="5096e-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="5096e-107">Hvis du vil fuldføre denne procedure, skal du have transaktioner, der blev fuldført i POS og derefter hentet ind i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5096e-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="5096e-108">Denne registrering bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="5096e-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="5096e-109">Denne procedure henviser måske til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5096e-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="5096e-110">Bemærk, at Dynamics AX nu kaldes Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="5096e-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="5096e-111">Gå til Alle arbejdsområder > ..</span><span class="sxs-lookup"><span data-stu-id="5096e-111">Go to All workspaces > ..</span></span> <span data-ttu-id="5096e-112">> Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="5096e-112">> Retail store financials.</span></span>
2. <span data-ttu-id="5096e-113">Klik på Ny opgørelse.</span><span class="sxs-lookup"><span data-stu-id="5096e-113">Click New statement.</span></span>
3. <span data-ttu-id="5096e-114">Klik på rullelisten i feltet Butiksnummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5096e-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5096e-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5096e-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5096e-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5096e-116">Click OK.</span></span>
    * <span data-ttu-id="5096e-117">Gruppe til opsætning har de indstillinger, der styrer, hvilke transaktioner der medtages i opgørelsen, og hvordan de grupperes på linjer i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="5096e-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="5096e-118">Du kan åbne gruppen til opsætning og ændre disse indstillinger, eller du kan bruge standardindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="5096e-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="5096e-119">Feltet Opgørelsesmetode definerer, hvordan opgørelseslinjerne grupperes.</span><span class="sxs-lookup"><span data-stu-id="5096e-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="5096e-120">Vælg en medarbejder eller et kasseapparat, hvis du kun vil beregne en opgørelse for den specifikke medarbejder eller det specifikke kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="5096e-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="5096e-121">Vælg en indstilling i feltet Lukkemetode.</span><span class="sxs-lookup"><span data-stu-id="5096e-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="5096e-122">Klik på Beregn opgørelse.</span><span class="sxs-lookup"><span data-stu-id="5096e-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="5096e-123">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="5096e-123">Click Yes.</span></span>
    * <span data-ttu-id="5096e-124">Når du har beregnet opgørelsen, skal der være linjer, der er oprettet med samlede beløb for hver betalingsmetode og opgørelsesmetode, der blev brugt.</span><span class="sxs-lookup"><span data-stu-id="5096e-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="5096e-125">Angiv et optalt beløb på hver linje, hvis det skal angives eller opdateres.</span><span class="sxs-lookup"><span data-stu-id="5096e-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="5096e-126">Det optalte felt udfyldes med beløb fra kasseoptællinger udført i POS.</span><span class="sxs-lookup"><span data-stu-id="5096e-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="5096e-127">Klik på Bogfør opgørelse.</span><span class="sxs-lookup"><span data-stu-id="5096e-127">Click Post statement.</span></span>
10. <span data-ttu-id="5096e-128">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="5096e-128">Click Close.</span></span>
11. <span data-ttu-id="5096e-129">Gå til Detail og handel > Kanaler > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="5096e-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="5096e-130">Klik på fanen Bogførte opgørelser.</span><span class="sxs-lookup"><span data-stu-id="5096e-130">Click the Posted statements tab.</span></span>


