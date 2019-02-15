---
title: Konsistenskontrol af detailtransaktion
description: Dette emne beskriver funktionen konsistenskontrol af detailtransaktion i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "302075"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="9f966-103">Konsistenskontrol af detailtransaktion</span><span class="sxs-lookup"><span data-stu-id="9f966-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="9f966-104">Dette emne beskriver funktionen konsistenskontrol af detailtransaktion, der blev introduceret i Microsoft Dynamics 365 for Finance and Operations, version 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="9f966-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="9f966-105">Konsistenskontrollen identificerer og isolerer inkonsistente posteringer, før de hentes af processen til bogføring af opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="9f966-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="9f966-106">Når en opgørelse bogføres i Retail, kan bogføringen mislykkes på grund af inkonsistente data i detailtransaktionstabellerne.</span><span class="sxs-lookup"><span data-stu-id="9f966-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="9f966-107">Dataproblemet kan skyldes uforudsete problemer med i POS-programmet, eller at transaktioner blev importeret forkert fra tredjeparts-POS-systemer.</span><span class="sxs-lookup"><span data-stu-id="9f966-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="9f966-108">Eksempler på, hvordan denne inkonsistens kan vise sig, omfatter:</span><span class="sxs-lookup"><span data-stu-id="9f966-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="9f966-109">Totalen for transaktionen i hovedtabellen stemmer ikke overens med transaktionstotalen på linjerne.</span><span class="sxs-lookup"><span data-stu-id="9f966-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="9f966-110">Linjeantallet i hovedtabellen stemmer ikke overens med antallet af linjer i transaktionstabellen.</span><span class="sxs-lookup"><span data-stu-id="9f966-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="9f966-111">Moms i hovedtabellen stemmer ikke overens med momsbeløb på linjerne.</span><span class="sxs-lookup"><span data-stu-id="9f966-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="9f966-112">Når inkonsistente transaktioner hentes af processen til bogføring af opgørelsen, oprettes der inkonsekvente salgsfakturaer og betalingskladder, og hele bogføringsprocessen for opgørelsen mislykkes derfor.</span><span class="sxs-lookup"><span data-stu-id="9f966-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="9f966-113">Gendannelsen af opgørelserne fra en sådan tilstand omfatter komplekse rettelser af data på tværs af flere transaktionstabeller.</span><span class="sxs-lookup"><span data-stu-id="9f966-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="9f966-114">Konsistenskontrollen af detailtransaktioner forhindrer sådanne problemer.</span><span class="sxs-lookup"><span data-stu-id="9f966-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="9f966-115">I følgende diagram illustreres bogføringsprocessen med konsistenskontrollen af transaktioner.</span><span class="sxs-lookup"><span data-stu-id="9f966-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="9f966-116">![Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner](./media/validchecker.png "Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner")</span><span class="sxs-lookup"><span data-stu-id="9f966-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="9f966-117">Batchprocessen **Valider butikstransaktioner** kontrollerer konsistensen af detailtransaktionstabellerne i følgende scenarier.</span><span class="sxs-lookup"><span data-stu-id="9f966-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="9f966-118">Debitorkonto - validerer, at debitorkontoen i detailtransaktionstabellerne findes i debitormasteren i hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="9f966-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="9f966-119">Linjetæller - validerer, at antallet af linjer, som er angivet i transaktionshovedtabellen, svarer til antallet af linjer i salgstransaktionstabellerne.</span><span class="sxs-lookup"><span data-stu-id="9f966-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="9f966-120">Konfigurere konsistenskontrollen</span><span class="sxs-lookup"><span data-stu-id="9f966-120">Set up the consistency checker</span></span>
<span data-ttu-id="9f966-121">Konfigurer batchprocessen "Valider butiksposteringer" på **Detail \> Detail-it \> POS- bogføring** til periodiske kørsler.</span><span class="sxs-lookup"><span data-stu-id="9f966-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="9f966-122">Batchjobbet kan planlægges ud fra butikkens organisationshierarki på samme måde som processerne "Beregn opgørelser i batch" og "Bogfør opgørelse i batch" er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="9f966-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="9f966-123">Det anbefales, at du konfigurerer denne batchproces til at køre flere gange i løbet af dagen og planlægger den, så den køres ved afslutningen af hver kørsel af P-job.</span><span class="sxs-lookup"><span data-stu-id="9f966-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="9f966-124">Resultater af valideringsprocessen</span><span class="sxs-lookup"><span data-stu-id="9f966-124">Results of validation process</span></span>
<span data-ttu-id="9f966-125">Resultaterne af valideringskontrollen af batchprocessen markeres på den relevante detailtransaktion.</span><span class="sxs-lookup"><span data-stu-id="9f966-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="9f966-126">Feltet **Valideringsstatus** på detailtransaktionsposten er enten angivet til **Fuldført** eller **Fejl**, og datoen for den seneste valideringskørsel vises i feltet **Sidste valideringstidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="9f966-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="9f966-127">For at få vist mere beskrivende fejltekst, der vedrører en valideringsfejl, skal du vælge den relevante detailbutikstransaktionspost og klikke på knappen **Valideringsfejl**.</span><span class="sxs-lookup"><span data-stu-id="9f966-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="9f966-128">Transaktioner, der ikke består valideringskontrollen, og transaktioner, der endnu ikke blevet valideret, trækkes ikke ind i opgørelser.</span><span class="sxs-lookup"><span data-stu-id="9f966-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="9f966-129">Under processen "Beregn opgørelse" får brugere besked, hvis der findes posteringer, der kunne have været medtaget i opgørelsen, men ikke blev det.</span><span class="sxs-lookup"><span data-stu-id="9f966-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="9f966-130">Hvis der findes en valideringsfejl, er den eneste måde at rette fejlen på, at kontakte Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="9f966-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="9f966-131">I en senere version vil der blive tilføjet en funktion, så brugerne kan rette de poster, hvor der opstod fejl, via brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="9f966-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="9f966-132">Logførings- og overvågningsfunktioner vil også blive tilgængelige, så historikken over ændringerne kan spores.</span><span class="sxs-lookup"><span data-stu-id="9f966-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="9f966-133">Der tilføjes yderligere valideringsregler for at understøtte flere scenarier i en senere version.</span><span class="sxs-lookup"><span data-stu-id="9f966-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
