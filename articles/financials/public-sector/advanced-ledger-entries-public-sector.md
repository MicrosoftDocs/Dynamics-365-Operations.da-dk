---
title: Avancerede finansposter i den offentlige sektor
description: "Organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter. For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AdvancedLedgerEntry, BudgetControlConfiguration, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 19511
ms.assetid: 3db0233e-d767-4dc0-b008-733098b6ca70
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 67d16fab07e943cfeb35d405358e06d55d6cbd9c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-ledger-entries-in-the-public-sector"></a><span data-ttu-id="cc5c2-104">Avancerede finansposter i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="cc5c2-104">Advanced ledger entries in the public sector</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cc5c2-105">Organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-105">Public-sector organizations can use advanced ledger entries to create, adjust, and reverse ledger entries.</span></span> <span data-ttu-id="cc5c2-106">For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-106">For example, advanced ledger entries can be used to reclassify expenditures if invoices are mistakenly posted to the wrong account or project.</span></span>

<a name="how-do-i-set-up-advanced-ledger-entries"></a><span data-ttu-id="cc5c2-107">Hvordan konfigurerer jeg avancerede finansposter?</span><span class="sxs-lookup"><span data-stu-id="cc5c2-107">How do I set up advanced ledger entries?</span></span>
----------------------------------------

<span data-ttu-id="cc5c2-108">Kontroller, at nøglen **Licenskonfiguration** for **Avanceret finanspost** er valgt på siden **Licenskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-108">Verify that the **Advanced ledger entry** **License configuration** key is selected in the **License configuration** page.</span></span> <span data-ttu-id="cc5c2-109">Avancerede finansposter kræver bogføringsdefinitioner til Finans.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-109">Advanced ledger entries require General ledger posting definitions.</span></span> <span data-ttu-id="cc5c2-110">Disse bogføringsdefinitioner kan indstilles til at generere flere, afstemte finansposter baseret på finanskontoen, der er angivet på siden **Avancerede finansposter**.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-110">These posting definitions can be set up to generate multiple, balanced ledger entries based on the ledger account entered in the **Advanced ledger entries** page.</span></span> <span data-ttu-id="cc5c2-111">Du kan finde flere oplysninger om bogføringsdefinitioner for avancerede finansposter under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="cc5c2-111">For more information about posting definitions for advanced ledger entries, see [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>

## <a name="can-i-use-budget-control-with-advanced-ledger-entries"></a><span data-ttu-id="cc5c2-112">Kan jeg bruge budgetstyring med avancerede finansposter?</span><span class="sxs-lookup"><span data-stu-id="cc5c2-112">Can I use budget control with advanced ledger entries?</span></span>
<span data-ttu-id="cc5c2-113">Ja.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-113">Yes.</span></span> <span data-ttu-id="cc5c2-114">Hvis organisationen bruger budgetstyring, kan du aktivere budgetstyring for avancerede finansposter på siden **Konfiguration af budgetstyring**.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-114">If your organization uses budget control, you can enable budget control for advanced ledger entries on the **Budget control configuration** page.</span></span>

## <a name="can-i-use-advanced-ledger-entries-with-projects"></a><span data-ttu-id="cc5c2-115">Kan jeg bruge avancerede finansposter i projekter?</span><span class="sxs-lookup"><span data-stu-id="cc5c2-115">Can I use advanced ledger entries with projects?</span></span>
<span data-ttu-id="cc5c2-116">Ja.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-116">Yes.</span></span> <span data-ttu-id="cc5c2-117">Hvis du ønsker, at brugere skal kunne ændre de økonomiske dimensioner for et projekt på den avancerede finanspostlinje, skal du vælge indstillingen **Tillad redigering af økonomiske dimensioner i formen for avanceret finanspostering** på siden **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-117">If you want users to be able to change the financial dimensions for a project on the advanced ledger entry line, you’ll need to select the **Allow the financial dimensions to be edited on the advanced ledger entry form** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="cc5c2-118">Hvis du ikke vælger denne indstilling, kan brugere kun ændre de økonomiske dimensioner i feltet **Finanskonto**, hvis de økonomiske dimensioner ikke er de økonomiske standarddimensioner for et projekt.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-118">If you don’t select this option, users can change the financial dimensions in the **Ledger account** field only if the financial dimensions are not the default financial dimensions for a project.</span></span>

## <a name="how-do-i-use-advanced-ledger-entries-to-record-yearend-accrual-entries"></a><span data-ttu-id="cc5c2-119">Hvordan bruger jeg avancerede finansposter til at registrere årsafslutning periodiseringsposter?</span><span class="sxs-lookup"><span data-stu-id="cc5c2-119">How do I use advanced ledger entries to record yearend accrual entries?</span></span>
<span data-ttu-id="cc5c2-120">Opret en avanceret finanspost, vælg indstillingen **Tilbageførsel** indstilling, og angiv en tilbageførselsdato.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-120">Create an advanced ledger entry, select the **Reversing entry** option, and enter a reversing date.</span></span> <span data-ttu-id="cc5c2-121">Den tilbageførte avancerede finanspost oprettes, når den avancerede finanspost er bogført.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-121">The reversing advanced ledger entry is created when the advanced ledger entry is posted.</span></span> <span data-ttu-id="cc5c2-122">Den tilbageførte avancerede finanspost har et nyt posteringsnummer og kladdestatus.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-122">The reversing advanced ledger entry will have a new transaction number and a draft status.</span></span> <span data-ttu-id="cc5c2-123">Tilbageførselsdatoen bruges som regnskabsdatoen, og debet- eller kreditbeløbet på hver linje i den oprindelige post tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-123">The reversing date will be used as the accounting date and the debit or credit amount on each line of the original entry will be reversed.</span></span> <span data-ttu-id="cc5c2-124">Den samme bogføringsdefinition bruges.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-124">The same posting definition will be used.</span></span> <span data-ttu-id="cc5c2-125">Posteringstekst til headeren og linjerne indeholder ordene "Tilbagefører post fra", posteringsnummeret for den oprindelige avancerede finanspost og posteringsteksten for den oprindelige avancerede finanspost.</span><span class="sxs-lookup"><span data-stu-id="cc5c2-125">The transaction text for the header and lines will contain the words “Reversing entry from,” the transaction number of the original advanced ledger entry, and the transaction text of the original advanced ledger entry.</span></span>






