--- 
title: " Gemme konfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: jashanno
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ab1ee4a3273c162e94452a63891963922947c26c
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="404bb-103"> Gemme konfigurationer for detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="404bb-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="404bb-104">Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="404bb-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="404bb-105">Økonomiske dimensioner i detailbutikker er omfattet af en anden procedure.</span><span class="sxs-lookup"><span data-stu-id="404bb-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="404bb-106">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="404bb-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="404bb-107">Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="404bb-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="404bb-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="404bb-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="404bb-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="404bb-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="404bb-110">Indstillingerne i sektionen Opgørelse/ultimo påvirker oprettelse, validering og bogføring af opgørelsen for butikken.</span><span class="sxs-lookup"><span data-stu-id="404bb-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="404bb-111">Åbn sektionen Opgørelse/Ultimo.</span><span class="sxs-lookup"><span data-stu-id="404bb-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="404bb-112">Vælg den metode, du vil bruge til at gruppere linjerne i opgørelsen efter.</span><span class="sxs-lookup"><span data-stu-id="404bb-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="404bb-113">Vælg "Ja", hvis der kun skal oprettes én opgørelse pr. dag, når der oprettes opgørelser fra batchjobbet til oprettelse af opgørelser.</span><span class="sxs-lookup"><span data-stu-id="404bb-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="404bb-114">Feltet Beregning af kasseoptælling definerer, om kasseoptællinger skal lægges sammen, eller om den sidste skal bruges.</span><span class="sxs-lookup"><span data-stu-id="404bb-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="404bb-115">Vælg finanskontoen, som afrundingsdifferencer skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="404bb-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="404bb-116">I feltet Maksimal afrundingsdifference kan du angive den afrundingsdifference, der maksimalt tillades.</span><span class="sxs-lookup"><span data-stu-id="404bb-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="404bb-117">I feltet Bogføring kan du angive den maksimale samlede bogføringsdifference, der er tilladt for en opgørelse.</span><span class="sxs-lookup"><span data-stu-id="404bb-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="404bb-118">I feltet Skift kan du angive den maksimale samlede difference i et skift i en opgørelse.</span><span class="sxs-lookup"><span data-stu-id="404bb-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="404bb-119">I feltet Transaktion kan du angive den maksimale samlede difference på en linje i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="404bb-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="404bb-120">I feltet Lukkemetode kan du definere, om transaktioner, der skal medtages i en opgørelse, skal være en del af et lukket skift, eller om de kan være alle transaktioner inden for det definerede interval for dato/klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="404bb-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="404bb-121">I feltet Afslutning på forretningsdag kan du angive et tidspunkt, hvis transaktioner, der foregår efter midnat, skal bogføres med et tidspunkt den foregående dag.</span><span class="sxs-lookup"><span data-stu-id="404bb-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="404bb-122">Vælg "Ja", hvis transaktioner, der foregår efter midnat, skal bogføres som en del af den foregående dag.</span><span class="sxs-lookup"><span data-stu-id="404bb-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="404bb-123">Vælg "Ja" for at få oprettet opgørelser for hver defineret opgørelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="404bb-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="404bb-124">Dette kan være nyttigt, hvis bogføringens ydeevne skal forbedres for butikker med store transaktionsmængder, da den opretter mange mindre opgørelser, som kan behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="404bb-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="404bb-125">I feltet Standardkunde kan du vælge den debitorkonto, der skal bruges til salg til kunder, der kommer ind fra gaden.</span><span class="sxs-lookup"><span data-stu-id="404bb-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


