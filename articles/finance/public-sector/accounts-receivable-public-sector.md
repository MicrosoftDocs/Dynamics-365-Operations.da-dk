---
title: Oversigt over Debitor i den offentlige sektor
description: I dette emne beskrives de funktioner for Debitorer, som er tilgængelige for den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceJournal, CustParameters, CustTradingPartnerCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26281
ms.assetid: a411ec87-a209-471c-a141-5f5a92f2e45e
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 954cb02e42871faac2f0bd7269af2531d5e5591b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174607"
---
# <a name="accounts-receivable-in-the-public-sector-overview"></a><span data-ttu-id="0c51d-103">Oversigt over Debitor i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="0c51d-103">Accounts receivable in the public sector overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c51d-104">I dette emne beskrives de funktioner for Debitorer, som er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="0c51d-104">This topic describes the Accounts receivable functionality that is available for the public sector.</span></span>

<a name="how-do-i-set-accounts-receivable-parameters-for-the-public-sector"></a><span data-ttu-id="0c51d-105">Hvordan indstiller jeg Debitorparametre for den offentlige sektor?</span><span class="sxs-lookup"><span data-stu-id="0c51d-105">How do I set Accounts receivable parameters for the public sector?</span></span>
------------------------------------------------------------------

<span data-ttu-id="0c51d-106">De fleste Debitorparametre angives på samme måde, uanset om du er i den offentlige sektor eller private sektor.</span><span class="sxs-lookup"><span data-stu-id="0c51d-106">Most Accounts receivable parameters are set the same way whether you’re in the public sector or the private sector.</span></span> <span data-ttu-id="0c51d-107">De parametre, der kræves til faktureringsklassifikationer og faktureringskoder, bruges imidlertid kun af den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="0c51d-107">However, the parameters that are required for billing classifications and billing codes are used only by the public sector.</span></span> <span data-ttu-id="0c51d-108">Du kan få flere oplysninger i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0c51d-108">For more information, see [Billing classifications and billing codes in the public sector](billing-classifications-billing-codes-public-sector.md).</span></span>

-   <span data-ttu-id="0c51d-109">Du kan aktivere brugen af faktureringsklassifikationer og faktureringskoder i afsnittet **Generelt** på oversigtspanelet **Salgsopsætning** og ved at vælge **Brug faktureringsklassifikationer**.</span><span class="sxs-lookup"><span data-stu-id="0c51d-109">To enable the use of billing classifications and billing codes, in the **General** section, on the **Sales setup** FastTab, select **Use billing classifications**.</span></span>
-   <span data-ttu-id="0c51d-110">For at prioritere udligningen af fritekstfakturaer skal du se de påkrævede parameterindstillinger i [Udligningsprioritet i den offentlige sektor](settlement-priority-public-sector.md) og [Fritekstfakturaer i den offentlige sektor](free-text-invoices-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0c51d-110">To prioritize the settlement of free text invoices, see the required parameter settings in [Settlement priority in the public sector](settlement-priority-public-sector.md) and [Free text invoices in the public sector](free-text-invoices-public-sector.md).</span></span>
-   <span data-ttu-id="0c51d-111">Hvis du vil bruge faktureringskoder med Projektregnskab, skal du vælge indstillingen til at få vist projektrelaterede felter på fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c51d-111">To use billing codes with Project accounting, select the option to display project-related fields on free text invoices.</span></span> <span data-ttu-id="0c51d-112">Når du gør det, sker der to ting:</span><span class="sxs-lookup"><span data-stu-id="0c51d-112">When you do this, two things happen:</span></span>
    -   <span data-ttu-id="0c51d-113">Projektrelaterede felter vises både på fritekstfakturaer og faktureringskoder.</span><span class="sxs-lookup"><span data-stu-id="0c51d-113">Project-related fields are displayed both on free text invoices and on billing codes.</span></span>
    -   <span data-ttu-id="0c51d-114">Den finanskonto, der er knyttet til projektet, anvendes automatisk på fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="0c51d-114">The ledger account related to the project is automatically used on the free text invoice.</span></span> <span data-ttu-id="0c51d-115">Vælg indstillingen for at tillade finanskontonummeret at blive redigeret for at tillade brugere at ændre finanskontoen på fritekstfakturaen og i regnskabsfordelinger.</span><span class="sxs-lookup"><span data-stu-id="0c51d-115">To allow users to change the ledger account on the free text invoice and in the accounting distributions, select the option to allow the ledger account number to be changed.</span></span>

## <a name="how-do-i-control-the-settlement-order-for-accounts-receivable-transactions"></a><span data-ttu-id="0c51d-116">Hvordan styrer jeg udligningsrækkefølgen for debitorposteringer?</span><span class="sxs-lookup"><span data-stu-id="0c51d-116">How do I control the settlement order for Accounts receivable transactions?</span></span>
<span data-ttu-id="0c51d-117">Du kan bruge faktureringsklassifikationer sammen med andre faktureringsattributter til at styre den rækkefølge, der er udlignet i dine debitorposteringer.</span><span class="sxs-lookup"><span data-stu-id="0c51d-117">You can use billing classifications along with other billing attributes to control the order that your Accounts receivable transactions are settled in.</span></span> <span data-ttu-id="0c51d-118">Du kan få flere oplysninger i [Udligningsprioritet i den offentlige sektor](settlement-priority-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0c51d-118">For details, see [Settlement priority in the public sector](settlement-priority-public-sector.md).</span></span>

## <a name="is-there-an-easy-way-to-review-reimbursement-transactions"></a><span data-ttu-id="0c51d-119">Er der en nem måde at gennemgå refusionsposteringer på?</span><span class="sxs-lookup"><span data-stu-id="0c51d-119">Is there an easy way to review reimbursement transactions?</span></span>
<span data-ttu-id="0c51d-120">Du kan bruge faktureringsklassifikationer til at oprette en separat refusionstransaktion for hver faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="0c51d-120">You can use billing classifications to create a separate reimbursement transaction for each billing classification.</span></span> <span data-ttu-id="0c51d-121">Når du gør det, grupperes refusionsposteringer efter den entydige bogføringstype for debitorsaldo og faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="0c51d-121">When you do this, reimbursement transactions are grouped by the unique customer balance posting type entry and billing classification.</span></span> <span data-ttu-id="0c51d-122">Du kan få flere oplysninger i [Udligninger i den offentlige sektor](reimbursements-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0c51d-122">For details, see [Reimbursements in the public sector](reimbursements-public-sector.md).</span></span>

## <a name="where-are-the-trading-partner-codes-that-i-need-for-gfrs-and-facts-i-reporting"></a><span data-ttu-id="0c51d-123">Hvor er de handelspartnerkoder, jeg skal bruge til GFRS- og FACTS I-rapportering?</span><span class="sxs-lookup"><span data-stu-id="0c51d-123">Where are the trading partner codes that I need for GFRS and FACTS I reporting?</span></span>
<span data-ttu-id="0c51d-124">De handelspartnerkoder, som er nødvendige for GFRS- og FACTS I-rapportering, bliver fastlagt af det amerikanske finans- og skatteministerium.</span><span class="sxs-lookup"><span data-stu-id="0c51d-124">The trading partner codes required for GFRS and FACTS I reporting are established by the US Department of the Treasury.</span></span> <span data-ttu-id="0c51d-125">Enhver virksomhed, der følger amerikanske statslige rapporteringsregler for debitorer, bør tilføje handelspartnerkoder til deres debitorkontooplysninger for de organer, som de gør forretninger med.</span><span class="sxs-lookup"><span data-stu-id="0c51d-125">Any organization that follows U.S. governmental reporting rules for accounts receivables should add trading partner codes to their customer account information for the agencies they do business with.</span></span> <span data-ttu-id="0c51d-126">For eksempel hvis kontoret handler med Federal Trade Commission, skal du gå til siden **Handelspartnerkoder** og oprette handelspartnerkode 29.</span><span class="sxs-lookup"><span data-stu-id="0c51d-126">For example, if your agency does business with the Federal Trade Commission, you’d go to the **Trading partner codes** page and create trading partner code 29.</span></span> <span data-ttu-id="0c51d-127">Derefter, på siden med kundedetaljer for FTC, skal du skrive 29 i feltet **Handelspartnerkode**.</span><span class="sxs-lookup"><span data-stu-id="0c51d-127">Then, on the customer detail page for the FTC, you’d enter 29 in the **Trading partner code** field.</span></span>

### <a name="i-created-default-financial-dimensions-for-a-customer-group-but-one-customer-in-the-group-needs-a-different-value-for-one-of-the-financial-dimensions-whats-the-easiest-way-to-handle-this"></a><span data-ttu-id="0c51d-128">Jeg har oprettet økonomiske standarddimensioner for en debitorgruppe, men én kunde i gruppen skal have en anden værdi for en af de økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="0c51d-128">I created default financial dimensions for a customer group, but one customer in the group needs a different value for one of the financial dimensions.</span></span> <span data-ttu-id="0c51d-129">Hvad er den nemmeste måde at håndtere dette på?</span><span class="sxs-lookup"><span data-stu-id="0c51d-129">What’s the easiest way to handle this?</span></span>

<span data-ttu-id="0c51d-130">Du kan bevare de økonomiske standarddimensioner for debitorgruppen.</span><span class="sxs-lookup"><span data-stu-id="0c51d-130">You can keep the default financial dimensions for the customer group.</span></span> <span data-ttu-id="0c51d-131">Bare gå til kundeposten for den debitor, der skal have en anden værdi, og angiv de økonomiske standarddimensioner for debitoren.</span><span class="sxs-lookup"><span data-stu-id="0c51d-131">Just go to the customer record for the customer that needs a different value, and enter default financial dimensions for the customer.</span></span> <span data-ttu-id="0c51d-132">Kundens økonomiske standarddimensioner tilsidesætter de økonomiske standarddimensioner, der er angivet for debitorgruppen.</span><span class="sxs-lookup"><span data-stu-id="0c51d-132">The customer’s default financial dimensions will override the default financial dimensions that were set for the customer group.</span></span>

## <a name="what-can-i-use-accounts-receivable-posting-definitions-for"></a><span data-ttu-id="0c51d-133">Hvad kan jeg bruge bogføringsdefinitioner for debitor til?</span><span class="sxs-lookup"><span data-stu-id="0c51d-133">What can I use Accounts receivable posting definitions for?</span></span>
<span data-ttu-id="0c51d-134">Du kan bruge bogføringsdefinitioner til at oprette reskontrokladdelinjer til kildetransaktioner, der opfylder de valgte kriterier – f.eks. til at generere flere, afstemte finansposter baseret på attributter, som f.eks. transaktionstyper og konti.</span><span class="sxs-lookup"><span data-stu-id="0c51d-134">You can use posting definitions to create subledger journal lines for originating transactions that meet selected criteria - for example, to generate multiple, balanced, ledger entries based on attributes such as transaction types and accounts.</span></span> <span data-ttu-id="0c51d-135">Hvis du vil vide mere om bogføringsdefinitioner, skal du se [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="0c51d-135">To learn more about posting definitions, see [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="0c51d-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0c51d-136">Additional resources</span></span>
--------

[<span data-ttu-id="0c51d-137">Debitorer</span><span class="sxs-lookup"><span data-stu-id="0c51d-137">Accounts receivable</span></span>](../accounts-receivable/accounts-receivable.md)

[<span data-ttu-id="0c51d-138">Oprette en faktureringskode</span><span class="sxs-lookup"><span data-stu-id="0c51d-138">Create a billing code</span></span>](tasks/create-billing-code-public-sector.md)

[<span data-ttu-id="0c51d-139">Oprette en faktureringsklassifikation</span><span class="sxs-lookup"><span data-stu-id="0c51d-139">Create a billing classification</span></span>](tasks/create-billing-classification-public-sector.md)

[<span data-ttu-id="0c51d-140">Oprette og tildele en handelspartnerkode</span><span class="sxs-lookup"><span data-stu-id="0c51d-140">Create and assign a trading partner code</span></span>](tasks/create-assign-trading-partner-code-public-sector.md)


