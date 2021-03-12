---
title: Oprette og tildele avancerede regelstrukturer
description: I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968588"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="54fee-103">Oprette og tildele avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="54fee-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54fee-104">I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="54fee-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="54fee-105">Denne guide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="54fee-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="54fee-106">Opret en avanceret regelstruktur</span><span class="sxs-lookup"><span data-stu-id="54fee-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="54fee-107">Gå til Finans **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Avancerede regelstrukturer**.</span><span class="sxs-lookup"><span data-stu-id="54fee-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="54fee-108">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="54fee-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="54fee-109">I feltet **Avanceret regelstruktur** skal du skrive et navn, som beskriver regelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="54fee-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="54fee-110">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54fee-110">Select **OK**.</span></span>
5. <span data-ttu-id="54fee-111">Vælg **Tilføj segment**.</span><span class="sxs-lookup"><span data-stu-id="54fee-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="54fee-112">Listen over segmenter, skal du vælge en økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="54fee-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="54fee-113">For eksempel **Butik**.</span><span class="sxs-lookup"><span data-stu-id="54fee-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="54fee-114">Vælg **Tilføj segment**.</span><span class="sxs-lookup"><span data-stu-id="54fee-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="54fee-115">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="54fee-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="54fee-116">Anvende en avanceret regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="54fee-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="54fee-117">Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="54fee-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="54fee-118">Søg på listen, og vælg den kontostruktur, som du vil anvende den avancerede regel for.</span><span class="sxs-lookup"><span data-stu-id="54fee-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="54fee-119">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="54fee-119">Select **Edit**.</span></span> <span data-ttu-id="54fee-120">Du kan også vælge **Avancerede regler**, hvorefter du bliver bedt om at sætte kontostrukturen i **Kladdetilstand**.</span><span class="sxs-lookup"><span data-stu-id="54fee-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="54fee-121">Vælg **Avancerede regler**.</span><span class="sxs-lookup"><span data-stu-id="54fee-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="54fee-122">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="54fee-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="54fee-123">Skriv en værdi i feltet **Avanceret regel**.</span><span class="sxs-lookup"><span data-stu-id="54fee-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="54fee-124">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="54fee-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="54fee-125">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="54fee-125">Select **Create**.</span></span>
9. <span data-ttu-id="54fee-126">Klik på **Tilføj nyt kriterie**.</span><span class="sxs-lookup"><span data-stu-id="54fee-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="54fee-127">Vælg hovedkontoen eller en økonomisk dimension i feltet **Hvor**.</span><span class="sxs-lookup"><span data-stu-id="54fee-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="54fee-128">Vælg en indstilling i feltet **Operatør**, f.eks. er **mellem** eller **inkluderer**.</span><span class="sxs-lookup"><span data-stu-id="54fee-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="54fee-129">Skriv en værdi i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="54fee-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="54fee-130">Skriv en værdi i feltet **værdi**.</span><span class="sxs-lookup"><span data-stu-id="54fee-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="54fee-131">Vælg **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="54fee-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="54fee-132">På listen, kan du finde den avancerede regelstruktur, som du vil bruge, når de kriterier, du har angivet, er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="54fee-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="54fee-133">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="54fee-133">Select **Add**.</span></span>
17. <span data-ttu-id="54fee-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="54fee-134">Close the page.</span></span>
18. <span data-ttu-id="54fee-135">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="54fee-135">Select **Activate**.</span></span>

