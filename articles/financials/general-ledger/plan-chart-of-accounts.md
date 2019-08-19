---
title: Planlægge din kontoplan
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26f7ca1fa539fb0cf69a7759e92c5e735bd41211
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846769"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="18526-103">Planlægge din kontoplan</span><span class="sxs-lookup"><span data-stu-id="18526-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18526-104">Dette emne indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.</span><span class="sxs-lookup"><span data-stu-id="18526-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="18526-105">Du kan oprette en kontoplan, når du vil registrere og vedligeholde økonomiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="18526-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="18526-106">En kontoplan er en samling konti, der definerer en økonomisk ramme.</span><span class="sxs-lookup"><span data-stu-id="18526-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="18526-107">For at spore transaktionerne på disse konti yderligere, kan du tilføje segmenter.</span><span class="sxs-lookup"><span data-stu-id="18526-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="18526-108">Disse segmenter kaldes økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="18526-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="18526-109">En udgiftskonto kan f.eks. indeholde økonomiske dimensioner med navnene Afdeling, Bærer og Formål.</span><span class="sxs-lookup"><span data-stu-id="18526-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="18526-110">Brugerdefinerede regler bestemmer, hvordan økonomiske dimensioner knyttes til hovedkontiene og andre økonomiske dimensioner, samt hvordan disse transaktioner angives.</span><span class="sxs-lookup"><span data-stu-id="18526-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="18526-111">Disse brugerdefinerede regler er kendt som kontostrukturer og avancerede regler.</span><span class="sxs-lookup"><span data-stu-id="18526-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="18526-112">Kontoplanen er en struktureret oversigt over en juridisk enheds finanskonti.</span><span class="sxs-lookup"><span data-stu-id="18526-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="18526-113">Oversigten bruges til at udarbejde økonomiske rapporter til myndigheder og til ejerne.</span><span class="sxs-lookup"><span data-stu-id="18526-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="18526-114">Kontiene grupperes først efter kontotype og samles derefter yderligere i større kategorier.</span><span class="sxs-lookup"><span data-stu-id="18526-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="18526-115">På det mest generelle niveau er kontiene grupperet som indtægter og udgifter (driftskonti) og aktiver og passiver (statuskonti).</span><span class="sxs-lookup"><span data-stu-id="18526-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="18526-116">En kontoplan kan deles og bruges af alle de juridiske enheder i en organisation.</span><span class="sxs-lookup"><span data-stu-id="18526-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="18526-117">Kontoplanen, der bruges af en juridisk enhed, defineres på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="18526-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="18526-118">Her er nogle af de faktorer, du bør overveje, når du planlægger strukturen af kontoplanen for din organisation:</span><span class="sxs-lookup"><span data-stu-id="18526-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="18526-119">De rapporteringskrav, der gælder i det land eller område, hvor organisationen er hjemmehørende</span><span class="sxs-lookup"><span data-stu-id="18526-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="18526-120">Hvilke rapporteringskrav der gælder for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="18526-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="18526-121">Detaljeringsgraden, som kræves, både for eksterne organisationer og for din organisation</span><span class="sxs-lookup"><span data-stu-id="18526-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="18526-122">Du kan oprette kontoplanen på siden **Kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="18526-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="18526-123">Du kan oprette hovedkonti fra siden **Kontoplan** eller **Hovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="18526-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="18526-124">Dine hovedkonti bør ikke omfatte specialtegn, der bruges som afgrænsningstegn i kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="18526-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="18526-125">Ellers kan funktionerne være ustabile, eller du er nødt til at bruge opslag eller dialogboksen, når du angiver kombinationer af konti og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="18526-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="18526-126">Du kan finde flere oplysninger i [Oprette en hovedkonto](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="18526-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="18526-127">I Microsoft Dynamics for Finance and Operations version 8.0 (april 2018) kan du redigere afgrænsningstegnet for kontoplanen fra siden **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="18526-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="18526-128">Det er en god ide at knytte hovedkontiene til hovedkontokategorier, så du kan drage fordel af økonomiske standardrapporter uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="18526-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="18526-129">Derfor kan du hurtigere og nemmere designe og vedligeholde rapporter.</span><span class="sxs-lookup"><span data-stu-id="18526-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="18526-130">Du kan oprette kontostrukturer på siden **Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="18526-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="18526-131">Kontostrukturer definerer gyldige kombinationer.</span><span class="sxs-lookup"><span data-stu-id="18526-131">Account structures define valid combinations.</span></span> <span data-ttu-id="18526-132">Disse kombinationer udgør sammen med hovedkontiene en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="18526-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="18526-133">Du kan finde flere oplysninger under [Oprette kontostrukturer](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="18526-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="18526-134">**Tilsidesættelser af juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="18526-134">**Legal entity overrides**</span></span>

<span data-ttu-id="18526-135">Ikke alle hovedkonti er gyldige for alle juridiske enheder, og nogle hovedkonti er muligvis kun relevante for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="18526-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="18526-136">I dette scenarie kan du bruge sektionen **Tilsidesættelser af juridisk enhed** for at identificere, hvilke firmaer hovedkontoen tilsidesættes for, ejeren, og den periode, hvor dimensionen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="18526-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="18526-137">Tilsidesættelser på det delte niveau må ikke være mere restriktive end tilsidesættelser på niveauet for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="18526-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="18526-138">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="18526-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="18526-139">Økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="18526-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="18526-140">Oprette og tildele avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="18526-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
