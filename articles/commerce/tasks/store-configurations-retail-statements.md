---
title: Gemme konfigurationer for detailopgørelser
description: Denne procedure viser konfigurationer for butikken, der påvirker, hvordan Commerce-opgørelser oprettes og bogføres.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021977"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="4abdd-103">Gemme konfigurationer for detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="4abdd-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4abdd-104">Denne procedure viser konfigurationer for butikken, der påvirker, hvordan Commerce-opgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="4abdd-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="4abdd-105">Økonomiske dimensioner i butikker er omfattet af en anden procedure.</span><span class="sxs-lookup"><span data-stu-id="4abdd-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="4abdd-106">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="4abdd-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4abdd-107">I **navigationsruden** skal du gå til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="4abdd-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="4abdd-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4abdd-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4abdd-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4abdd-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4abdd-110">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="4abdd-110">Click **Edit**.</span></span>
5. <span data-ttu-id="4abdd-111">Indstillingerne i oversigtspanelet **Opgørelse/ultimo** påvirker oprettelse, validering og bogføring af opgørelsen for butikken.</span><span class="sxs-lookup"><span data-stu-id="4abdd-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="4abdd-112">Udvid oversigtspanelet **Opgørelse/ultimo**.</span><span class="sxs-lookup"><span data-stu-id="4abdd-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="4abdd-113">I feltet **Opgørelse/ultimo** skal du vælge den metode, du vil bruge til at gruppere linjerne i opgørelsen efter.</span><span class="sxs-lookup"><span data-stu-id="4abdd-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="4abdd-114">Vælg "Ja" i **Én opgørelse pr. dag**, hvis der kun skal oprettes én opgørelse pr. dag, når der oprettes opgørelser fra batchjobbet til oprettelse af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="4abdd-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="4abdd-115">Feltet **Beregning af kasseoptælling** definerer, om kasseoptællinger skal lægges sammen, eller om den sidste skal bruges.</span><span class="sxs-lookup"><span data-stu-id="4abdd-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="4abdd-116">I feltet **Afrunding** skal du vælge finanskontoen, som afrundingsdifferencer skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="4abdd-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="4abdd-117">I feltet **Maksimal afrundingsdifference** skal du angive den afrundingsdifference, der maksimalt tillades.</span><span class="sxs-lookup"><span data-stu-id="4abdd-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="4abdd-118">I feltet **Bogføring** skal du angive den maksimale samlede bogføringsdifference, der er tilladt for en opgørelse.</span><span class="sxs-lookup"><span data-stu-id="4abdd-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="4abdd-119">I feltet **Skift** skal du angive den maksimale samlede difference i et skift i en opgørelse.</span><span class="sxs-lookup"><span data-stu-id="4abdd-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="4abdd-120">I feltet **Transaktion** skal du angive den maksimale samlede difference på en linje i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="4abdd-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="4abdd-121">I feltet **Lukkemetode** skal du definere, om transaktioner, der skal medtages i en opgørelse, skal være en del af et lukket skift, eller om de kan være alle transaktioner inden for det definerede interval for dato/klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="4abdd-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="4abdd-122">I feltet **Afslutning på forretningsdag** skal du angive et tidspunkt, hvis transaktioner, der foregår efter midnat, skal bogføres med et tidspunkt den foregående dag.</span><span class="sxs-lookup"><span data-stu-id="4abdd-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="4abdd-123">Vælg "Ja" i **Bogfør som arbejdsdag**, hvis transaktioner, der foregår efter midnat, skal bogføres som en del af den foregående dag.</span><span class="sxs-lookup"><span data-stu-id="4abdd-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="4abdd-124">Vælg "Ja" i **Opdel efter opgørelsesmetode** for at få oprettet opgørelser for hver defineret opgørelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="4abdd-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="4abdd-125">Dette kan være nyttigt, hvis bogføringens ydeevne skal forbedres for butikker med store transaktionsmængder, da den opretter mange mindre opgørelser, som kan behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="4abdd-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="4abdd-126">I feltet **Standardkunde** i oversigtspanelet **Generelt** skal du vælge den debitorkonto, der skal bruges til salg til kunder, der kommer ind fra gaden.</span><span class="sxs-lookup"><span data-stu-id="4abdd-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

