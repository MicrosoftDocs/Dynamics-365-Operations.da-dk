---
title: Oprette og tildele avancerede regelstrukturer
description: I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837051"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="9718c-103">Oprette og tildele avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="9718c-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9718c-104">I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="9718c-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="9718c-105">Denne guide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9718c-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="9718c-106">Opret en avanceret regelstruktur</span><span class="sxs-lookup"><span data-stu-id="9718c-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="9718c-107">Gå til Finans **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Avancerede regelstrukturer**.</span><span class="sxs-lookup"><span data-stu-id="9718c-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="9718c-108">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="9718c-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="9718c-109">I feltet **Avanceret regelstruktur** skal du skrive et navn, som beskriver regelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="9718c-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="9718c-110">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9718c-110">Select **OK**.</span></span>
5. <span data-ttu-id="9718c-111">Vælg **Tilføj segment**.</span><span class="sxs-lookup"><span data-stu-id="9718c-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="9718c-112">Listen over segmenter, skal du vælge en økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="9718c-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="9718c-113">For eksempel **Butik**.</span><span class="sxs-lookup"><span data-stu-id="9718c-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="9718c-114">Vælg **Tilføj segment**.</span><span class="sxs-lookup"><span data-stu-id="9718c-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="9718c-115">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="9718c-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="9718c-116">Anvende en avanceret regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="9718c-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="9718c-117">Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="9718c-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="9718c-118">Søg på listen, og vælg den kontostruktur, som du vil anvende den avancerede regel for.</span><span class="sxs-lookup"><span data-stu-id="9718c-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="9718c-119">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9718c-119">Select **Edit**.</span></span> <span data-ttu-id="9718c-120">Du kan også vælge **Avancerede regler**, hvorefter du bliver bedt om at sætte kontostrukturen i **Kladdetilstand**.</span><span class="sxs-lookup"><span data-stu-id="9718c-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="9718c-121">Vælg **Avancerede regler**.</span><span class="sxs-lookup"><span data-stu-id="9718c-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="9718c-122">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="9718c-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="9718c-123">Skriv en værdi i feltet **Avanceret regel**.</span><span class="sxs-lookup"><span data-stu-id="9718c-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="9718c-124">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9718c-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="9718c-125">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="9718c-125">Select **Create**.</span></span>
9. <span data-ttu-id="9718c-126">Klik på **Tilføj nyt kriterie**.</span><span class="sxs-lookup"><span data-stu-id="9718c-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="9718c-127">Vælg hovedkontoen eller en økonomisk dimension i feltet **Hvor**.</span><span class="sxs-lookup"><span data-stu-id="9718c-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="9718c-128">Vælg en indstilling i feltet **Operatør**, f.eks. er **mellem** eller **inkluderer**.</span><span class="sxs-lookup"><span data-stu-id="9718c-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="9718c-129">Skriv en værdi i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="9718c-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="9718c-130">Skriv en værdi i feltet **værdi**.</span><span class="sxs-lookup"><span data-stu-id="9718c-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="9718c-131">Vælg **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9718c-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="9718c-132">På listen, kan du finde den avancerede regelstruktur, som du vil bruge, når de kriterier, du har angivet, er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="9718c-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="9718c-133">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9718c-133">Select **Add**.</span></span>
17. <span data-ttu-id="9718c-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9718c-134">Close the page.</span></span>
18. <span data-ttu-id="9718c-135">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="9718c-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]