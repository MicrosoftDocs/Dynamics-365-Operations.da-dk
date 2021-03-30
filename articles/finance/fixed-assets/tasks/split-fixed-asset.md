---
title: Opdele et anlægsaktiv
description: I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db601be192b57fbec220193d3c9fde1a4f50c085
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213502"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="f3a31-103">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="f3a31-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3a31-104">I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="f3a31-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="f3a31-105">Den bruger rollen Revisor og USMF demodata.</span><span class="sxs-lookup"><span data-stu-id="f3a31-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="f3a31-106">Opret et nyt anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="f3a31-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="f3a31-107">I navigationsruden skal du gå til **Moduler \> Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="f3a31-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-108">Select **New**.</span></span>
3. <span data-ttu-id="f3a31-109">Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="f3a31-110">Bemærk nummeret på anlægsaktivet til senere brug i opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f3a31-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="f3a31-111">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="f3a31-112">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="f3a31-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="f3a31-113">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="f3a31-113">Split a fixed asset</span></span>

<span data-ttu-id="f3a31-114">Inden et fuldt afskrevet aktiv opdeles, skal status for aktivbogen ændres manuelt fra **Lukket** til **Åben**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="f3a31-115">Dette trin er nødvendigt, fordi status for bogen skal være **Åben**, hvis du skal bogføre transaktioner for aktivet (f.eks. til kassationssalg).</span><span class="sxs-lookup"><span data-stu-id="f3a31-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="f3a31-116">Du skal også aktivere parameteren **Tillad flere posteringer inden for ét bilag** under fanen **Generelt** på siden **Fiannsparametre**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="f3a31-117">Når status for anlægskartoteket ændres, og flere posteringer inden for ét bilag er tilladt, skal du udføre følgende trin for at opdele aktivet.</span><span class="sxs-lookup"><span data-stu-id="f3a31-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="f3a31-118">På listen skal du finde og vælge linket for det anlægsaktiv, der skal opdeles.</span><span class="sxs-lookup"><span data-stu-id="f3a31-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="f3a31-119">Vælg **Bøger**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-119">Select **Books**.</span></span> <span data-ttu-id="f3a31-120">Vælg det kartotek, der skal opdeles til det nye aktiv.</span><span class="sxs-lookup"><span data-stu-id="f3a31-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="f3a31-121">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-121">Select **Functions**.</span></span>
4. <span data-ttu-id="f3a31-122">Vælg **Opdel anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="f3a31-123">Skriv eller vælg en værdi i feltet **Til anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="f3a31-124">Vælg rullelisteknappen i feltet **Til bog** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f3a31-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f3a31-125">Angiv en dato i feltet **Transaktionsdato**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="f3a31-126">Angiv et tal i feltet **Procent**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="f3a31-127">Indtast eller vælg en værdi i feltet **Kladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="f3a31-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="f3a31-129">Bogfør kladdeposteringen</span><span class="sxs-lookup"><span data-stu-id="f3a31-129">Post the journal transaction</span></span>

1. <span data-ttu-id="f3a31-130">I navigationsruden skal du gå til **Moduler \> Anlægsaktiver \> Kladdeposteringer \> Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="f3a31-131">Vælg på listen den kladde, der er oprettet med opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f3a31-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="f3a31-132">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-132">Select **Lines**.</span></span>

    - <span data-ttu-id="f3a31-133">Bekræft de oprettede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="f3a31-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="f3a31-134">Der oprettes en postering til anskaffelsesregulering for det oprindelige aktiv for at formindske værdien af den procentdel, der er angivet under opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f3a31-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="f3a31-135">Der oprettes en anskaffelsespostering for det nye aktiv for det samme beløb.</span><span class="sxs-lookup"><span data-stu-id="f3a31-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="f3a31-136">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f3a31-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]