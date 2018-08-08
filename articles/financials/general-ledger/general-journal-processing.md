---
title: "Finanskladdehåndtering"
description: "I denne artikel beskrives funktionerne i Microsoft Dynamics 365 for Finance and Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet."
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 82d08a76c0d52719330960b85b3cca9b1440406b
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="87c78-103">Finanskladdehåndtering</span><span class="sxs-lookup"><span data-stu-id="87c78-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87c78-104">I denne artikel beskrives funktionerne i Microsoft Dynamics 365 for Finance and Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet.</span><span class="sxs-lookup"><span data-stu-id="87c78-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="87c78-105">Kladdenavne</span><span class="sxs-lookup"><span data-stu-id="87c78-105">Journal names</span></span>

<span data-ttu-id="87c78-106">Et af de vigtigste områder, der skal konfigureres, er kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="87c78-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="87c78-107">Det er en god idé at definere bestemte kladdenavne til hvert formål, såsom intern, periodiseringsregulering og fejlretning.</span><span class="sxs-lookup"><span data-stu-id="87c78-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="87c78-108">Du kan skræddersy hvert kladdenavn for at gøre det nemt og sikkert at indtaste data til hvert formål.</span><span class="sxs-lookup"><span data-stu-id="87c78-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="87c78-109">Du kan konfigurere følgende elementer på siden **Kladdenavne**:</span><span class="sxs-lookup"><span data-stu-id="87c78-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="87c78-110">**Arbejdsgangsgodkendelse** – for at øge den interne kontrol skal du definere arbejdsgange, der fastsætter materialitetsgrænser for fremgangsmåder for gennemsyn og godkendelse, baseret på kriterier såsom samlet debetbeløb.</span><span class="sxs-lookup"><span data-stu-id="87c78-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="87c78-111">Du konfigurerer arbejdsgange for finanskladder på siden **Arbejdsgange i Finans**.</span><span class="sxs-lookup"><span data-stu-id="87c78-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="87c78-112">**Standardværdier** – vælg standardværdier for modkonti, valuta og økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="87c78-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="87c78-113">**Kladdekontrol** – du kan oprette begrænsninger på regnskabs- og kontotypen samt segmentværdier.</span><span class="sxs-lookup"><span data-stu-id="87c78-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="87c78-114">**Eksempler**</span><span class="sxs-lookup"><span data-stu-id="87c78-114">**Examples**</span></span>

<span data-ttu-id="87c78-115">Et kladdenavn kan kun anvendes til reguleringer.</span><span class="sxs-lookup"><span data-stu-id="87c78-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="87c78-116">I dette tilfælde kan du angive, at kun kontotypen **Finans** er gyldig på tværs af alle regnskaber.</span><span class="sxs-lookup"><span data-stu-id="87c78-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="87c78-117">[![Kontotyper for kladdekontrol](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="87c78-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="87c78-118">Et kladdenavn kan kun bruges til et bestemt segment eller til et interval for hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="87c78-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="87c78-119">[![Kladdekontrolsegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="87c78-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="87c78-120">Indstillingen **Automatisk tilbageførsel** er tilgængelig i finanskladder.</span><span class="sxs-lookup"><span data-stu-id="87c78-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="87c78-121">Du har for eksempel en periodiseringsregulering, hvor det faktiske dokuments endnu ikke er behandlet, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="87c78-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="87c78-122">[![Tilbageførsel af finanskladde](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="87c78-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="87c78-123">Microsoft Excel-tilføjelsesprogrammet til kladdepostering giver et ekstra niveau af automatisering og gør dataindtastningen lettere.</span><span class="sxs-lookup"><span data-stu-id="87c78-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="87c78-124">Handlingen **Åbn linjer i Excel** er tilgængelig på siden **Finanskladde** og **Kladdebilag**.</span><span class="sxs-lookup"><span data-stu-id="87c78-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="87c78-125">På siden **Periodiske kladder** kan du oprette gentagelseskladder for at automatisere behandling af finanskladder.</span><span class="sxs-lookup"><span data-stu-id="87c78-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="87c78-126">Du kan bruge bilagsskabeloner til enhver tid.</span><span class="sxs-lookup"><span data-stu-id="87c78-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="87c78-127">På siden **Finanskladder** findes handlingerne **Gem** og **Vælg bilagsskabelon** på siden **Kladdebilag** under **Funktioner** for bilagslinjerne.</span><span class="sxs-lookup"><span data-stu-id="87c78-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="87c78-128">Relateret opsætning</span><span class="sxs-lookup"><span data-stu-id="87c78-128">Related setup</span></span>
<span data-ttu-id="87c78-129">Følgende opsætning er ikke specifik for finanskladder men hjælper med at sikre, at data indtastes korrekt og nemt.</span><span class="sxs-lookup"><span data-stu-id="87c78-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="87c78-130">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="87c78-130">Main account</span></span>

<span data-ttu-id="87c78-131">Opsætningen af hovedkontoen giver mange muligheder for behandling af finanskladden:</span><span class="sxs-lookup"><span data-stu-id="87c78-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="87c78-132">**Krav til DC/CR** – brug denne indstilling, hvis en hovedkonto er begrænset til debet- eller kredittransaktioner.</span><span class="sxs-lookup"><span data-stu-id="87c78-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="87c78-133">Opsætningen kontrolleres, når en kladde valideres eller bogføres.</span><span class="sxs-lookup"><span data-stu-id="87c78-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="87c78-134">**Standardmodkonto**</span><span class="sxs-lookup"><span data-stu-id="87c78-134">**Default offset account**</span></span>
-   <span data-ttu-id="87c78-135">**Suspenderet** – suspenderer en hovedkonto, så der ikke kan indtastes data, på tværs af alle regnskaber eller for et bestemt regnskab eller for bestemte juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="87c78-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="87c78-136">**Tillad ikke manuel angivelse** – Sørg for, at brugere ikke kan angive en værdi for kontoen manuelt i kladder.</span><span class="sxs-lookup"><span data-stu-id="87c78-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="87c78-137">**Standard/Valider valuta**</span><span class="sxs-lookup"><span data-stu-id="87c78-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="87c78-138">**Tilsidesæt juridisk enhed** – denne opsætning er specifik for det definerede regnskab eller den juridiske enhed:</span><span class="sxs-lookup"><span data-stu-id="87c78-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="87c78-139">**Standard/Valider moms**</span><span class="sxs-lookup"><span data-stu-id="87c78-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="87c78-140">**Standarddimension** – **Ikke fast** eller **Fast værdi**.</span><span class="sxs-lookup"><span data-stu-id="87c78-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="87c78-141">**Fast værdi** hjælper med at sikre, at alle posteringer for denne hovedkonto altid bruger en dimensionsværdi, der er konfigureret som **fast**.</span><span class="sxs-lookup"><span data-stu-id="87c78-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="87c78-142">**Bogføringsvalidering**</span><span class="sxs-lookup"><span data-stu-id="87c78-142">**Posting validation**</span></span>
    -   <span data-ttu-id="87c78-143">**Validering af bruger** – denne indstilling styrer, hvilke brugere der har tilladelse til at bogføre på en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="87c78-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="87c78-144">**Validering af bogføringstype** – denne indstilling styrer, hvilke bogføringstyper der er tilladte for en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="87c78-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="87c78-145">Regnskabsmæssige strukturer og avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="87c78-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="87c78-146">Regnskabsmæssige strukturer og avancerede regelstrukturer er meget vigtige for at garantere, at de data, der kræves til økonomisk rapportering og sporing af ydeevne er hentet under behandling af finanskladde og enhver dokumentation.</span><span class="sxs-lookup"><span data-stu-id="87c78-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="87c78-147">Med regnskabsmæssige strukturer og avancerede regelstrukturer kan du skræddersy dataindtastningsoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="87c78-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="87c78-148">Du kan kun tillade dataindtastning for økonomiske dimensioner, der er relevante i hver situation, og kan også gennemtvinge kravet om, at obligatoriske og korrekte data altid registreres.</span><span class="sxs-lookup"><span data-stu-id="87c78-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="87c78-149">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="87c78-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="87c78-150">[Planlægning: Kontoplan](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="87c78-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="87c78-151">Oprette avancerede regler for kladder</span><span class="sxs-lookup"><span data-stu-id="87c78-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="87c78-152">Oprette en kladdepost ved hjælp af en skabelon</span><span class="sxs-lookup"><span data-stu-id="87c78-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="87c78-153">Oprette og kontrollere kladder</span><span class="sxs-lookup"><span data-stu-id="87c78-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="87c78-154">Bogføre periodiske kladder</span><span class="sxs-lookup"><span data-stu-id="87c78-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="87c78-155">Behandle finansfordelingskladde</span><span class="sxs-lookup"><span data-stu-id="87c78-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



