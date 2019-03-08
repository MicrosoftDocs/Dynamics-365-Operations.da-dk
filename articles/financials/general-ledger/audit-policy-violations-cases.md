---
title: Overtrædelser af overvågningspolitik og sager
description: I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler. Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3ed72f829ca4060fe0a4c03b6d4a47a98cdebd6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "352522"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="ab294-104">Overtrædelser af overvågningspolitik og sager</span><span class="sxs-lookup"><span data-stu-id="ab294-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab294-105">I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler.</span><span class="sxs-lookup"><span data-stu-id="ab294-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="ab294-106">Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="ab294-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="ab294-107">Sådan genereres revisionssager</span><span class="sxs-lookup"><span data-stu-id="ab294-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="ab294-108">Overvågningspolitikker bruges til at identificere udgiftsrapporter, indkøbsordrer og kreditorfakturaer, der ikke overholder de forretningsregler, som du definerer og konfigurerer som regler for overvågningspolitik.</span><span class="sxs-lookup"><span data-stu-id="ab294-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="ab294-109">Overvågningspolitikker køres i batchtilstand.</span><span class="sxs-lookup"><span data-stu-id="ab294-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="ab294-110">Når du kører en overvågningspolitik, køres alle de politikregler, der er del af den pågældende politik, på samme tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="ab294-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="ab294-111">Hver politikregel evaluerer et sæt dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ab294-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="ab294-112">Politikreglen vælger dokumenter, der ligger i datointervallet for dokumentvalg, og som svarer til de angivne kriterier.</span><span class="sxs-lookup"><span data-stu-id="ab294-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="ab294-113">En politikregel kan f.eks. vælge udgiftsrapporter, hvor der figurerer måltider, som overstiger 50,00.</span><span class="sxs-lookup"><span data-stu-id="ab294-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="ab294-114">En anden politikregel kan måske vælge kreditorfakturaer, der skal betales til en bestemt kreditor.</span><span class="sxs-lookup"><span data-stu-id="ab294-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="ab294-115">For hvert dokument, der er valgt i sættet, genereres der en overtrædelse.</span><span class="sxs-lookup"><span data-stu-id="ab294-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="ab294-116">Denne overtrædelse registrerer, at et bestemt dokument, f.eks. faktura 12345, ikke overholder politikreglen.</span><span class="sxs-lookup"><span data-stu-id="ab294-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="ab294-117">Flere poster for overtrædelse af overvågning grupperes sammen og knyttes til overvågningssager.</span><span class="sxs-lookup"><span data-stu-id="ab294-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="ab294-118">Sager til hver overvågningspolitik grupperes som standard efter overvågningspolitikregel.</span><span class="sxs-lookup"><span data-stu-id="ab294-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="ab294-119">Hvis du foretrækker det, kan du vælge andre kriterier for gruppering ved brug af siden **Kriterier for sagsgruppering**.</span><span class="sxs-lookup"><span data-stu-id="ab294-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="ab294-120">Du kan f.eks. gruppere udgiftshoveder efter projekt-id og kreditorfakturaer efter kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="ab294-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="ab294-121">I dette tilfælde bliver alle overtrædelser af udgiftshoveder, der har samme projekt-id, grupperet under samme sag, og alle kreditorfakturaer, der har samme kreditorkonto, bliver grupperet under samme sag.</span><span class="sxs-lookup"><span data-stu-id="ab294-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab294-122">Ved regler for overvågningspolitikker, der er baseret på forespørgselstypen **Dublet**, grupperes overtrædelser ikke efter politikregel eller efter de kriterier, der er angivet på siden **Kriterier for sagsgruppering**.</span><span class="sxs-lookup"><span data-stu-id="ab294-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="ab294-123">De grupperes i stedet efter de kriterier, der er indbygget i overvågningspolitikreglen.</span><span class="sxs-lookup"><span data-stu-id="ab294-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="ab294-124">Hvis en politikregel f.eks. evaluerer udgiftsrapporter for dubletudgifter med samme beløb, forhandler-id og dato, vil alle udgifter, der har samme værdier i disse felter, være én sag.</span><span class="sxs-lookup"><span data-stu-id="ab294-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="ab294-125">Eventuelle udgifter, der har andre værdier, vil udgøre en særskilt sag.</span><span class="sxs-lookup"><span data-stu-id="ab294-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="ab294-126">Når revisionssagerne er genereret, håndteres de med brug af typiske processer til sagsstyring.</span><span class="sxs-lookup"><span data-stu-id="ab294-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="ab294-127">Datointervaller for dokumentvalg</span><span class="sxs-lookup"><span data-stu-id="ab294-127">Document selection date ranges</span></span>
<span data-ttu-id="ab294-128">Når en overvågningspolitik er kørt, vælger hver politikregel dokumenter af den angivne type, som har en dato, der ligger i datointervallet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="ab294-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="ab294-129">Datointervallet for dokumentvalg angives på siden **Yderligere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="ab294-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="ab294-130">Mange dokumenter har mere end én tilknyttet dato.</span><span class="sxs-lookup"><span data-stu-id="ab294-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="ab294-131">Det datofelt, der bruges af overvågningspolitikreglen, er angivet på siden **Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="ab294-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="ab294-132">Her er nogle andre måder, en overvågningspolitik bruger datointervallet for dokumentvalg på:</span><span class="sxs-lookup"><span data-stu-id="ab294-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="ab294-133">Politikken bruger den version af hver politikregel, der var gældende på den sidste dag i datointervallet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="ab294-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="ab294-134">Du kan få vist gyldighedsdatoerne for hver politikregel på listesiden **Overvågningspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ab294-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="ab294-135">Politikken bruger de organisationsnoder, der er knyttet til politikken på den sidste dag i datointervallet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="ab294-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="ab294-136">Det er kun de organisationsnoder, der aktuelt er knyttet til politikken, der vises på listesiden **Overvågningspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ab294-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="ab294-137">I forbindelse med politikregler, der er baseret på forespørgselstypen **Listesøgning**, evaluerer politikken dokumenter til overvågede enheder, som er gyldige på den sidste dag i datointervallet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="ab294-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="ab294-138">Du kan finde flere oplysninger i [Overvåge politikregler](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="ab294-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



