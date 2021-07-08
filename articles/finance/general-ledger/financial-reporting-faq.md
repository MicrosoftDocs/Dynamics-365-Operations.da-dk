---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder svar på nogle ofte stillede spørgsmål om Økonomirapportering.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266627"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="32d83-103">Ofte stillede spørgsmål vedrørende Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="32d83-103">Financial reporting FAQ</span></span>

<span data-ttu-id="32d83-104">Dette emne indeholder svar på ofte stillede spørgsmål om Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="32d83-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="32d83-105">Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?</span><span class="sxs-lookup"><span data-stu-id="32d83-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="32d83-106">I følgende eksempel vises, hvordan du kan begrænse adgangen til en rapport ved hjælp af sikkerhedstræet.</span><span class="sxs-lookup"><span data-stu-id="32d83-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="32d83-107">USMF-demofirmaet indeholder rapporten **Finansbalance**, som ikke alle brugere af Økonomirapportering bør have adgang til.</span><span class="sxs-lookup"><span data-stu-id="32d83-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="32d83-108">Du kan bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun specifikke brugere kan få adgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="32d83-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="32d83-109">Log på Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="32d83-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="32d83-110">Vælg **Fil \> Ny \> Trædiagramdefinition** for at oprette en ny trædiagramdefinition.</span><span class="sxs-lookup"><span data-stu-id="32d83-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="32d83-111">Tryk to gange (eller dobbeltklik) på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="32d83-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="32d83-112">Vælg **Brugere og Grupper**.</span><span class="sxs-lookup"><span data-stu-id="32d83-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="32d83-113">Vælg de brugere eller grupper, der kræver adgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="32d83-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="32d83-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="32d83-114">Select **Save**.</span></span>
7. <span data-ttu-id="32d83-115">Tilføj den nye trædefinition i rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="32d83-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="32d83-116">Vælg **Indstilling** i trædefinitionen.</span><span class="sxs-lookup"><span data-stu-id="32d83-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="32d83-117">Vælg derefter **Medtag alle enheder** under **Valg af rapporteringsenhed**.</span><span class="sxs-lookup"><span data-stu-id="32d83-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="32d83-118">Hvordan identificerer jeg, hvilke konti der ikke svarer til mine saldi?</span><span class="sxs-lookup"><span data-stu-id="32d83-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="32d83-119">Når du har en rapport, der ikke har tilsvarende saldi, kan du bruge følgende procedurer til at identificere hver konto og afvigelse.</span><span class="sxs-lookup"><span data-stu-id="32d83-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="32d83-120">I Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="32d83-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="32d83-121">Opret en ny rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="32d83-121">Create a new row definition.</span></span>
2. <span data-ttu-id="32d83-122">Vælg **Rediger \> Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="32d83-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="32d83-123">Vælg **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="32d83-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="32d83-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32d83-124">Select **OK**.</span></span>
5. <span data-ttu-id="32d83-125">Gem rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="32d83-125">Save the row definition.</span></span>
6. <span data-ttu-id="32d83-126">Opret en ny kolonnedefinition.</span><span class="sxs-lookup"><span data-stu-id="32d83-126">Create a new column definition.</span></span>
7. <span data-ttu-id="32d83-127">Opret en ny rapportdefinition.</span><span class="sxs-lookup"><span data-stu-id="32d83-127">Create a new report definition.</span></span>
8. <span data-ttu-id="32d83-128">Vælg **Indstillinger**, og fjern markering af denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="32d83-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="32d83-129">Opret rapporten.</span><span class="sxs-lookup"><span data-stu-id="32d83-129">Generate the report.</span></span> 
10. <span data-ttu-id="32d83-130">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="32d83-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="32d83-131">I Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="32d83-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="32d83-132">Gå til **Finans \> Forespørgsler og rapporter \> Råbalance**.</span><span class="sxs-lookup"><span data-stu-id="32d83-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="32d83-133">Angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="32d83-133">Set the following fields:</span></span>

    - <span data-ttu-id="32d83-134">**Fra dato** – Angiv startdatoen for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="32d83-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="32d83-135">**Til dato** – Angiv den dato, rapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="32d83-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="32d83-136">**Økonomisk dimension** – Angiv dette felt til **Hovedkontosæt**.</span><span class="sxs-lookup"><span data-stu-id="32d83-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="32d83-137">Vælg **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="32d83-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="32d83-138">Eksporter rapporten til Excel.</span><span class="sxs-lookup"><span data-stu-id="32d83-138">Export the report to Excel.</span></span>

<span data-ttu-id="32d83-139">Du skal nu kunne kopiere data fra Excel-rapporten i Financial Reporter til rapporten **Råbalance**, så du kan sammenligne kolonnerne **Ultimosaldo**.</span><span class="sxs-lookup"><span data-stu-id="32d83-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="32d83-140">Når jeg designer en rapport i Report Designer, eller når jeg opretter en økonomisk rapport, får jeg følgende meddelelse: "Operationen kunne ikke fuldføres pga. problemer i dataproviderstrukturen."</span><span class="sxs-lookup"><span data-stu-id="32d83-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="32d83-141">Hvordan skal jeg svare?</span><span class="sxs-lookup"><span data-stu-id="32d83-141">How should I respond?</span></span>

<span data-ttu-id="32d83-142">Meddelelsen angiver, at der opstod et problem, da systemet forsøgte at hente økonomiske metadata fra datacentret, mens du brugte Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="32d83-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="32d83-143">Du kan løse dette problem på to måder:</span><span class="sxs-lookup"><span data-stu-id="32d83-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="32d83-144">Gennemse dataintegrationsstatus ved at gå til **Værktøjer \> Integrationsstatus** i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="32d83-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="32d83-145">Hvis integrationen ikke er fuldført, skal du vente, indtil den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="32d83-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="32d83-146">Derefter skal du prøve at gentage det, du var i gang med, da du modtog meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="32d83-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="32d83-147">Kontakt Support for at identificere og arbejde dig gennem problemet.</span><span class="sxs-lookup"><span data-stu-id="32d83-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="32d83-148">Der kan være uoverensstemmende data i systemet.</span><span class="sxs-lookup"><span data-stu-id="32d83-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="32d83-149">Supportteknikere kan hjælpe dig med at identificere dette problem på serveren og finde de specifikke data, der muligvis skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="32d83-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
