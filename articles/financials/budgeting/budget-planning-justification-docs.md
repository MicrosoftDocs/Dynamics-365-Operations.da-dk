---
title: "Berettigelsesdokumenter til budgetplanlægning"
description: "Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget, som kan forklare, hvorfor det er nødvendigt med et specifikt budget."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38050e8a792622b772882ec4a0cddce8661a720
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="ea42e-103">Berettigelsesdokumenter til budgetplanlægning</span><span class="sxs-lookup"><span data-stu-id="ea42e-103">Budget planning justification documents</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ea42e-104">Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget, som kan forklare, hvorfor det er nødvendigt med et specifikt budget.</span><span class="sxs-lookup"><span data-stu-id="ea42e-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="ea42e-105">En budgetplansskabelon oprettes af budgetadministratoren i Microsoft Word og knyttes til den aktuelle proces i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="ea42e-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="ea42e-106">Ejere af budgettet kan derefter åbne skabelonen og automatisk få udfyldt felter i Word med data baseret på deres budgetanmodning.</span><span class="sxs-lookup"><span data-stu-id="ea42e-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="ea42e-107">De kan derefter tilføje yderligere tekst eller data, før deres personlige berettigelsesdokument gemmes og knyttes til deres budgetplan.</span><span class="sxs-lookup"><span data-stu-id="ea42e-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="ea42e-108">Konfigurere Microsoft Dynamics Office-tilføjelsesprogrammet til Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="ea42e-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="ea42e-109">Åbn et nyt Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="ea42e-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="ea42e-110">Klik på **Indsæt** på båndet, og klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="ea42e-111">Søg efter Microsoft Dynamics Office-tilføjelsesprogrammet, og klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="ea42e-112">I Word, i højre rude, skal du klikke på **Tilføj serveroplysninger**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="ea42e-113">Skriv eller indsæt webadressen til serveren, og klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="ea42e-114">Definere berettigelsesskabelonen i Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="ea42e-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="ea42e-115">Klik på **Design** i Microsoft Dynamics Office-tilføjelsesprogrammet, når du har logget.</span><span class="sxs-lookup"><span data-stu-id="ea42e-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="ea42e-116">Til headeroplysninger skal du bruge knappen **Tilføj felter**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="ea42e-117">Vælg BudgetPlanJustification for enhedsdatakilden, og klik på **Næste**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="ea42e-118">**Bemærk:** Denne enhed er påkrævet for alle berettigelsesdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ea42e-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="ea42e-119">Andre enheder kan bruges, men overførslen tilbage til Microsoft Dynamics 365 for Finance and Operations mislykkes, hvis denne enhed ikke medtages.</span><span class="sxs-lookup"><span data-stu-id="ea42e-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="ea42e-120">Tilføj BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber-etiketter og værdier i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="ea42e-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="ea42e-121">**Bemærk:** Du kan bruge dine egne etiketter i stedet for standardetiketterne, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="ea42e-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="ea42e-122">Klik på **Udført** for at fuldføre headersektionen.</span><span class="sxs-lookup"><span data-stu-id="ea42e-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="ea42e-123">Du kan angive detaljer for budgetplanbeløb på linjeniveau ved at klikke på **Tilføj tabel**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="ea42e-124">Vælg igen BudgetPlanJustification som datakilde for enheden, og klik på **Næste**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="ea42e-125">Tilføj felter for EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="ea42e-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="ea42e-126">**Bemærk:** Hvis der kan tilføjes kommentarer i individuelle budgetplanlinjer, kan de føjes til tabellen her.</span><span class="sxs-lookup"><span data-stu-id="ea42e-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="ea42e-127">Tilføj eventuelle yderligere anvisninger til slutbrugeren, og udfør evt. formatering eller lignende ændringer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="ea42e-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="ea42e-128">Gem dokumentet på din lokale computer, og luk filen, før du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="ea42e-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="ea42e-129">Konfigurere budgetplanlægningsprocessen til at bruge berettigelsesskabelonen</span><span class="sxs-lookup"><span data-stu-id="ea42e-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="ea42e-130">Gå i Finance and Operations til **Budgettering** &gt; **Opsætning** &gt; **Budgetplanlægning** &gt; **Skabeloner for berettigelsesdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="ea42e-131">Klik på **Ny**, og gå til det nyoprettede Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="ea42e-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="ea42e-132">Angiv et visningsnavn og en beskrivelse til skabelonen.</span><span class="sxs-lookup"><span data-stu-id="ea42e-132">Enter a template display name and description.</span></span> <span data-ttu-id="ea42e-133">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-133">Click **OK**.</span></span>
4.  <span data-ttu-id="ea42e-134">Gå til **Budgettering** &gt; **Opsætning** &gt; **Budgetplanlægning** &gt; **Budgetplanlægningsproces**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="ea42e-135">Vælg den proces, hvor berettigelsesskabelonen skal bruges, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="ea42e-136">Vælg den relevante skabelon i feltet **Skabelon for berettigelsesdokument**, og Gem.</span><span class="sxs-lookup"><span data-stu-id="ea42e-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="ea42e-137">Redigere og gemme personligt tilpassede berettigelsesdokumenter</span><span class="sxs-lookup"><span data-stu-id="ea42e-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="ea42e-138">Opret en ny budgetplan i Finance and Operations, eller åbn en eksisterende budgetplan.</span><span class="sxs-lookup"><span data-stu-id="ea42e-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="ea42e-139">Vælg **Opret ny berettigelse** i rullemenuen **Berettigelse**.</span><span class="sxs-lookup"><span data-stu-id="ea42e-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="ea42e-140">Når du har angivet detaljerne, skal du vælge at overføre det personligt tilpassede dokument fra **Berettigelse**-rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="ea42e-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





