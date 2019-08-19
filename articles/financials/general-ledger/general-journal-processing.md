---
title: Finanskladdehåndtering
description: I dette emne beskrives funktionerne i Microsoft Dynamics 365 for Finance and Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839225"
---
# <a name="general-journal-processing"></a><span data-ttu-id="23fff-103">Finanskladdehåndtering</span><span class="sxs-lookup"><span data-stu-id="23fff-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23fff-104">I dette emne beskrives funktionerne i Microsoft Dynamics 365 for Finance and Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet.</span><span class="sxs-lookup"><span data-stu-id="23fff-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="23fff-105">Kladdenavne</span><span class="sxs-lookup"><span data-stu-id="23fff-105">Journal names</span></span>

<span data-ttu-id="23fff-106">Et af de vigtigste områder, der skal konfigureres, er kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="23fff-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="23fff-107">Det er en god idé at definere bestemte kladdenavne til hvert formål, såsom intern, periodiseringsregulering og fejlretning.</span><span class="sxs-lookup"><span data-stu-id="23fff-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="23fff-108">Du kan skræddersy hvert kladdenavn for at gøre det nemt og sikkert at indtaste data til hvert formål.</span><span class="sxs-lookup"><span data-stu-id="23fff-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="23fff-109">Du kan konfigurere følgende elementer på siden **Kladdenavne**:</span><span class="sxs-lookup"><span data-stu-id="23fff-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="23fff-110">**Arbejdsgangsgodkendelse** – for at øge den interne kontrol skal du definere arbejdsgange, der fastsætter materialitetsgrænser for fremgangsmåder for gennemsyn og godkendelse, baseret på kriterier såsom samlet debetbeløb.</span><span class="sxs-lookup"><span data-stu-id="23fff-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="23fff-111">Du konfigurerer arbejdsgange for finanskladder på siden **Arbejdsgange i Finans**.</span><span class="sxs-lookup"><span data-stu-id="23fff-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="23fff-112">**Standardværdier** – vælg standardværdier for modkonti, valuta og økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="23fff-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="23fff-113">**Kladdekontrol** – du kan oprette begrænsninger på regnskabs- og kontotypen samt segmentværdier.</span><span class="sxs-lookup"><span data-stu-id="23fff-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="23fff-114">**Eksempler**</span><span class="sxs-lookup"><span data-stu-id="23fff-114">**Examples**</span></span>

<span data-ttu-id="23fff-115">Et kladdenavn kan kun anvendes til reguleringer.</span><span class="sxs-lookup"><span data-stu-id="23fff-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="23fff-116">I dette tilfælde kan du angive, at kun kontotypen **Finans** er gyldig på tværs af alle regnskaber.</span><span class="sxs-lookup"><span data-stu-id="23fff-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="23fff-117">[![Kontotyper for kladdekontrol](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="23fff-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="23fff-118">Et kladdenavn kan kun bruges til et bestemt segment eller til et interval for hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="23fff-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="23fff-119">[![Kladdekontrolsegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="23fff-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="23fff-120">Indstillingen **Automatisk tilbageførsel** er tilgængelig i finanskladder.</span><span class="sxs-lookup"><span data-stu-id="23fff-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="23fff-121">Du har for eksempel en periodiseringsregulering, hvor det faktiske dokuments endnu ikke er behandlet, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="23fff-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="23fff-122">[![Tilbageførsel af finanskladde](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="23fff-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="23fff-123">Microsoft Excel-tilføjelsesprogrammet til kladdepostering giver et ekstra niveau af automatisering og gør dataindtastningen lettere.</span><span class="sxs-lookup"><span data-stu-id="23fff-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="23fff-124">Handlingen **Åbn linjer i Excel** er tilgængelig på siden **Finanskladde** og **Kladdebilag**.</span><span class="sxs-lookup"><span data-stu-id="23fff-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="23fff-125">På siden **Periodiske kladder** kan du oprette gentagelseskladder for at automatisere behandling af finanskladder.</span><span class="sxs-lookup"><span data-stu-id="23fff-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="23fff-126">Du kan bruge bilagsskabeloner til enhver tid.</span><span class="sxs-lookup"><span data-stu-id="23fff-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="23fff-127">På siden **Finanskladder** findes handlingerne **Gem** og **Vælg bilagsskabelon** på siden **Kladdebilag** under **Funktioner** for bilagslinjerne.</span><span class="sxs-lookup"><span data-stu-id="23fff-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="23fff-128">Relateret opsætning</span><span class="sxs-lookup"><span data-stu-id="23fff-128">Related setup</span></span>
<span data-ttu-id="23fff-129">Følgende opsætning er ikke specifik for finanskladder, men hjælper med at sikre, at data indtastes korrekt og nemt.</span><span class="sxs-lookup"><span data-stu-id="23fff-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="23fff-130">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="23fff-130">Main account</span></span>

<span data-ttu-id="23fff-131">Opsætningen af hovedkontoen giver mange muligheder for behandling af finanskladden:</span><span class="sxs-lookup"><span data-stu-id="23fff-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="23fff-132">**Krav til DC/CR** – brug denne indstilling, hvis en hovedkonto er begrænset til debet- eller kredittransaktioner.</span><span class="sxs-lookup"><span data-stu-id="23fff-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="23fff-133">Opsætningen kontrolleres, når en kladde valideres eller bogføres.</span><span class="sxs-lookup"><span data-stu-id="23fff-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="23fff-134">**Standardmodkonto**</span><span class="sxs-lookup"><span data-stu-id="23fff-134">**Default offset account**</span></span>
-   <span data-ttu-id="23fff-135">**Suspenderet** – suspenderer en hovedkonto, så der ikke kan indtastes data, på tværs af alle regnskaber eller for et bestemt regnskab eller en bestemt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="23fff-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="23fff-136">**Tillad ikke manuel angivelse** – Sørg for, at brugere ikke kan angive en værdi for kontoen manuelt i kladder.</span><span class="sxs-lookup"><span data-stu-id="23fff-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="23fff-137">**Standard/Valider valuta**</span><span class="sxs-lookup"><span data-stu-id="23fff-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="23fff-138">**Tilsidesæt juridisk enhed** – denne opsætning er specifik for det definerede regnskab eller den juridiske enhed:</span><span class="sxs-lookup"><span data-stu-id="23fff-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="23fff-139">**Standard/Valider moms**</span><span class="sxs-lookup"><span data-stu-id="23fff-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="23fff-140">**Standarddimension** – **Ikke fast** eller **Fast værdi**.</span><span class="sxs-lookup"><span data-stu-id="23fff-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="23fff-141">**Fast værdi** hjælper med at sikre, at alle posteringer for denne hovedkonto altid bruger en dimensionsværdi, der er konfigureret som **Fast**.</span><span class="sxs-lookup"><span data-stu-id="23fff-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="23fff-142">**Bogføringsvalidering**</span><span class="sxs-lookup"><span data-stu-id="23fff-142">**Posting validation**</span></span>
    -   <span data-ttu-id="23fff-143">**Validering af bruger** – denne indstilling styrer, hvilke brugere der har tilladelse til at bogføre på en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="23fff-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="23fff-144">**Validering af bogføringstype** – denne indstilling styrer, hvilke bogføringstyper der er tilladte for en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="23fff-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="23fff-145">Regnskabsmæssige strukturer og avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="23fff-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="23fff-146">Regnskabsmæssige strukturer og avancerede regelstrukturer er meget vigtige for at sikre, at de data, der kræves til økonomisk rapportering og sporing af ydeevne, er hentet under behandling af finanskladde og enhver dokumentation.</span><span class="sxs-lookup"><span data-stu-id="23fff-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="23fff-147">Med regnskabsmæssige strukturer og avancerede regelstrukturer kan du skræddersy dataindtastningsoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="23fff-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="23fff-148">Du kan kun tillade dataindtastning for økonomiske dimensioner, der er relevante i hver situation, og kan også gennemtvinge kravet om, at obligatoriske og korrekte data altid registreres.</span><span class="sxs-lookup"><span data-stu-id="23fff-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="23fff-149">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="23fff-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="23fff-150">[Planlægning: Kontoplan](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="23fff-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="23fff-151">Oprette avancerede regler for kladder</span><span class="sxs-lookup"><span data-stu-id="23fff-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="23fff-152">Oprette en kladdepost ved hjælp af en skabelon</span><span class="sxs-lookup"><span data-stu-id="23fff-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="23fff-153">Oprette og kontrollere kladder</span><span class="sxs-lookup"><span data-stu-id="23fff-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="23fff-154">Bogføre periodiske kladder</span><span class="sxs-lookup"><span data-stu-id="23fff-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="23fff-155">Behandle finansfordelingskladde</span><span class="sxs-lookup"><span data-stu-id="23fff-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="23fff-156">Simuler bogføring</span><span class="sxs-lookup"><span data-stu-id="23fff-156">Simulate posting</span></span>
<span data-ttu-id="23fff-157">Du kan finde **Simuler bogføring** i menuen **Valider** til de fleste kladder.</span><span class="sxs-lookup"><span data-stu-id="23fff-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="23fff-158">Når du validerer en kladde ved hjælp af **Valider**-funktionen, tester systemet kladden for bestemte fejlbetingelser.</span><span class="sxs-lookup"><span data-stu-id="23fff-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="23fff-159">Hvis du bruger **Simuler bogføring**-funktionen, vil systemet køre alle de samme processer, der køres under bogføringen, uden at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="23fff-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="23fff-160">Du kan derefter gennemse bogføringsmeddelelser, der vises, rette eventuelle fejl og derefter klikke på menuen **Bogfør** for at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="23fff-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="23fff-161">**Simuler bogføring** findes ikke til batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="23fff-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="23fff-162">Men der er kode til at simulere bogføringen i batch, og udviklere kan udvide koden, hvis de vil tilføje denne funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="23fff-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  
