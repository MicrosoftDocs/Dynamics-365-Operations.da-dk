---
title: "Planlæg din kontoplan"
description: "Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="d163b-103">Planlæg din kontoplan</span><span class="sxs-lookup"><span data-stu-id="d163b-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d163b-104">Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.</span><span class="sxs-lookup"><span data-stu-id="d163b-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="d163b-105">Du kan oprette en kontoplan, når du vil registrere og vedligeholde økonomiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d163b-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="d163b-106">En kontoplan er en samling konti, der definerer en økonomisk ramme.</span><span class="sxs-lookup"><span data-stu-id="d163b-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="d163b-107">Hvis du derudover vil spore transaktionerne på disse konti, kan du tilføje segmenter, kaldet økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="d163b-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="d163b-108">En udgiftskonto kan f.eks. indeholde økonomiske dimensioner med navnene Afdeling, Bærer og Formål.</span><span class="sxs-lookup"><span data-stu-id="d163b-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="d163b-109">Brugerdefinerede regler, kaldet kontostrukturer og avancerede regler, bestemmer, hvordan disse økonomiske dimensioner er knyttet til hovedkontiene og andre økonomiske dimensioner, og også hvordan disse transaktioner er angivet.</span><span class="sxs-lookup"><span data-stu-id="d163b-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="d163b-110">Kontoplanen er en struktureret oversigt over en juridisk enheds finanskonti.</span><span class="sxs-lookup"><span data-stu-id="d163b-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="d163b-111">Oversigten bruges til at udarbejde økonomiske rapporter til myndigheder og til ejerne.</span><span class="sxs-lookup"><span data-stu-id="d163b-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="d163b-112">Kontiene er grupperet efter kontotype og derefter yderligere opsummeret i større kategorier.</span><span class="sxs-lookup"><span data-stu-id="d163b-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="d163b-113">På det mest generelle niveau er kontiene grupperet som indtægter og udgifter (driftskonti) og aktiver og passiver (statuskonti).</span><span class="sxs-lookup"><span data-stu-id="d163b-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="d163b-114">En kontoplan kan deles og bruges af alle de juridiske enheder i en organisation.</span><span class="sxs-lookup"><span data-stu-id="d163b-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="d163b-115">Kontoplanen, der bruges af en juridisk enhed, defineres på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="d163b-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="d163b-116">Her er nogle af de faktorer, du bør overveje, når du planlægger strukturen af kontoplanen for din organisation:</span><span class="sxs-lookup"><span data-stu-id="d163b-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="d163b-117">Hvilke rapporteringskrav der gælder i det land eller den region, hvor organisationen er hjemmehørende</span><span class="sxs-lookup"><span data-stu-id="d163b-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="d163b-118">Hvilke rapporteringskrav der gælder for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="d163b-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="d163b-119">Detaljeringsgraden, som kræves, både for eksterne organisationer og for din organisation</span><span class="sxs-lookup"><span data-stu-id="d163b-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="d163b-120">Opret kontoplanen på siden **Kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="d163b-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="d163b-121">Hovedkonti kan oprettes fra siden **Kontoplan** eller siden **Hovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="d163b-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="d163b-122">Dine hovedkonti bør ikke bruge specialtegn, der bruges som afgrænsningstegn i kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="d163b-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="d163b-123">Hvis du har et specialtegn, der er det samme som afgrænsningstegnet i din kontoplan, kan du opleve ustabilitet, eller der kan opstå behov for hele tiden at skulle bruge opslag eller pop op-vinduet, når du angiver kombinationer af konto og dimension.</span><span class="sxs-lookup"><span data-stu-id="d163b-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="d163b-124">Du kan finde flere oplysninger i [Oprette en hovedkonto](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d163b-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="d163b-125">Det er en god ide at knytte hovedkontiene til hovedkontokategorier, så du kan drage fordel af økonomiske standardrapporter uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="d163b-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="d163b-126">Derfor kan du hurtigere og nemmere designe og vedligeholde rapporter.</span><span class="sxs-lookup"><span data-stu-id="d163b-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="d163b-127">Brug siden **Konfigurer kontostrukturer** til at oprette kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="d163b-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="d163b-128">Kontostrukturer definerer gyldige kombinationer.</span><span class="sxs-lookup"><span data-stu-id="d163b-128">Account structures define valid combinations.</span></span> <span data-ttu-id="d163b-129">Kombinationerne udgør, sammen med hovedkontiene, en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d163b-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="d163b-130">Du kan finde flere oplysninger under [Oprette kontostrukturer](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="d163b-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="d163b-131">**Tilsidesættelser af juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="d163b-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="d163b-132">Ikke alle hovedkonti er gyldige for alle juridiske enheder, og nogle er muligvis kun relevante for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="d163b-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="d163b-133">I dette scenarie kan sektionen Tilsidesættelser af juridisk enhed bruges til at identificere, hvilke regnskaber hovedkontoen bør suspenderes for, hvem der er ejer, og hvor lang tid dimensionen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="d163b-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="d163b-134">Tilsidesættelser på det delte niveau må ikke være mere restriktive end tilsidesættelser på niveauet for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="d163b-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="d163b-135">Yderligere oplysninger finder du i følgende emner: [Økonomiske dimensioner](financial-dimensions.md)
[Opret og tildel avancerede regelstrukturer](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="d163b-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




