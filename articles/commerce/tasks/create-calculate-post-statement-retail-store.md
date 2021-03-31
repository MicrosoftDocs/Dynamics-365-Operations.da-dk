---
title: Oprette, beregne og bogføre opgørelser for en detailbutik
description: Dette emne gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 455dee5a14ca0c44ba823a467baa78352b367ec8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221299"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="78e0b-103">Oprette, beregne og bogføre opgørelser for en detailbutik</span><span class="sxs-lookup"><span data-stu-id="78e0b-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78e0b-104">Dette emne gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik.</span><span class="sxs-lookup"><span data-stu-id="78e0b-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="78e0b-105">Der er også batchjob, der kan konfigureres for de samme opgaver.</span><span class="sxs-lookup"><span data-stu-id="78e0b-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="78e0b-106">Trin til konfiguration og kørsel af batchjob findes i andre emner.</span><span class="sxs-lookup"><span data-stu-id="78e0b-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="78e0b-107">Hvis du vil fuldføre denne procedure, skal du have transaktioner, der blev fuldført i POS og derefter hentet ind i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78e0b-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="78e0b-108">Denne registrering bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="78e0b-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="78e0b-109">Vælg **Butiksregnskab** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="78e0b-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="78e0b-110">Vælg **Ny opgørelse**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-110">Select **New statement**.</span></span>
3. <span data-ttu-id="78e0b-111">Vælg en indstilling på rullelisten i feltet **Butiksnummer**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="78e0b-112">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-112">Select **OK**.</span></span>
5. <span data-ttu-id="78e0b-113">Gruppen **Konfiguration** har de indstillinger, der styrer, hvilke transaktioner der medtages i opgørelsen, og hvordan de grupperes på linjer i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="78e0b-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="78e0b-114">Du kan åbne gruppen **Konfiguration** og ændre disse indstillinger, eller du kan bruge standardindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="78e0b-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="78e0b-115">Feltet **Opgørelsesmetode** definerer, hvordan opgørelseslinjerne grupperes.</span><span class="sxs-lookup"><span data-stu-id="78e0b-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="78e0b-116">Vælg en medarbejder eller et kasseapparat i feltet **Medarb./kasse**, hvis du kun vil beregne en opgørelse for den specifikke medarbejder eller det specifikke kasseapparat.</span><span class="sxs-lookup"><span data-stu-id="78e0b-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="78e0b-117">Vælg en indstilling i feltet **Lukkemetode**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="78e0b-118">Vælg **Beregn opgørelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78e0b-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="78e0b-119">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-119">Select **Yes**.</span></span>
    - <span data-ttu-id="78e0b-120">Når du har beregnet opgørelsen, skal der være linjer, der er oprettet med samlede beløb for hver betalingsmetode og opgørelsesmetode, der blev brugt.</span><span class="sxs-lookup"><span data-stu-id="78e0b-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="78e0b-121">Angiv et optalt beløb på hver linje, hvis det skal angives eller opdateres.</span><span class="sxs-lookup"><span data-stu-id="78e0b-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="78e0b-122">Det optalte felt udfyldes med beløb fra kasseoptællinger udført i POS.</span><span class="sxs-lookup"><span data-stu-id="78e0b-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="78e0b-123">Vælg **Bogfør opgørelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78e0b-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="78e0b-124">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-124">Select **Close**.</span></span>
11. <span data-ttu-id="78e0b-125">Luk ruden.</span><span class="sxs-lookup"><span data-stu-id="78e0b-125">Close the pane.</span></span>
12. <span data-ttu-id="78e0b-126">Vælg **Butiksregnskab** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="78e0b-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="78e0b-127">Vælg fanen **Bogførte opgørelser**.</span><span class="sxs-lookup"><span data-stu-id="78e0b-127">Select the **Posted statements** tab.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]