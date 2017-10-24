--- 
title: "Oprette, beregne og bogføre et opgørelse for en detailbutik"
description: "Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="a7f68-103">Oprette, beregne og bogføre et opgørelse for en detailbutik</span><span class="sxs-lookup"><span data-stu-id="a7f68-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a7f68-104">Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik.</span><span class="sxs-lookup"><span data-stu-id="a7f68-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="a7f68-105">Der er også batchjob, der kan konfigureres for de samme opgaver.</span><span class="sxs-lookup"><span data-stu-id="a7f68-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="a7f68-106">Trin til konfiguration og kørsel af batchjob findes i andre emner.</span><span class="sxs-lookup"><span data-stu-id="a7f68-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="a7f68-107">Hvis du vil fuldføre denne procedure, skal du have transaktioner, der blev fuldført i POS og derefter hentet ind i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a7f68-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="a7f68-108">Denne registrering bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="a7f68-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="a7f68-109">Denne procedure henviser måske til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a7f68-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="a7f68-110">Bemærk, at Dynamics AX nu kaldes Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="a7f68-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="a7f68-111">Gå til Alle arbejdsområder > ..</span><span class="sxs-lookup"><span data-stu-id="a7f68-111">Go to All workspaces > ..</span></span> <span data-ttu-id="a7f68-112">> Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="a7f68-112">> Retail store financials.</span></span>
2. <span data-ttu-id="a7f68-113">Klik på Ny opgørelse.</span><span class="sxs-lookup"><span data-stu-id="a7f68-113">Click New statement.</span></span>
3. <span data-ttu-id="a7f68-114">Klik på rullelisten i feltet Butiksnummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a7f68-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a7f68-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a7f68-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a7f68-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a7f68-116">Click OK.</span></span>
    * <span data-ttu-id="a7f68-117">Gruppe til opsætning har de indstillinger, der styrer, hvilke transaktioner der medtages i opgørelsen, og hvordan de grupperes på linjer i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="a7f68-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="a7f68-118">Du kan åbne gruppen til opsætning og ændre disse indstillinger, eller du kan bruge standardindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="a7f68-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="a7f68-119">Feltet Opgørelsesmetode definerer, hvordan opgørelseslinjerne grupperes.</span><span class="sxs-lookup"><span data-stu-id="a7f68-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="a7f68-120">Vælg en medarbejder eller et kasseapparat, hvis du kun vil beregne en opgørelse for den specifikke medarbejder eller det specifikke kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="a7f68-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="a7f68-121">Vælg en indstilling i feltet Lukkemetode.</span><span class="sxs-lookup"><span data-stu-id="a7f68-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="a7f68-122">Klik på Beregn opgørelse.</span><span class="sxs-lookup"><span data-stu-id="a7f68-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="a7f68-123">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="a7f68-123">Click Yes.</span></span>
    * <span data-ttu-id="a7f68-124">Når du har beregnet opgørelsen, skal der være linjer, der er oprettet med samlede beløb for hver betalingsmetode og opgørelsesmetode, der blev brugt.</span><span class="sxs-lookup"><span data-stu-id="a7f68-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="a7f68-125">Angiv et optalt beløb på hver linje, hvis det skal angives eller opdateres.</span><span class="sxs-lookup"><span data-stu-id="a7f68-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="a7f68-126">Det optalte felt udfyldes med beløb fra kasseoptællinger udført i POS.</span><span class="sxs-lookup"><span data-stu-id="a7f68-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="a7f68-127">Klik på Bogfør opgørelse.</span><span class="sxs-lookup"><span data-stu-id="a7f68-127">Click Post statement.</span></span>
10. <span data-ttu-id="a7f68-128">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="a7f68-128">Click Close.</span></span>
11. <span data-ttu-id="a7f68-129">Gå til Detail og handel > Kanaler > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="a7f68-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="a7f68-130">Klik på fanen Bogførte opgørelser.</span><span class="sxs-lookup"><span data-stu-id="a7f68-130">Click the Posted statements tab.</span></span>


