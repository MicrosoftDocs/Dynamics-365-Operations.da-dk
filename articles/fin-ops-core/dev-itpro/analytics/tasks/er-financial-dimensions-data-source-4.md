---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684733"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="55a7d-103">ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)</span><span class="sxs-lookup"><span data-stu-id="55a7d-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55a7d-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="55a7d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="55a7d-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="55a7d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="55a7d-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="55a7d-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="55a7d-107">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="55a7d-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="55a7d-108">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="55a7d-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="55a7d-109">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="55a7d-109">Run report</span></span>
1. <span data-ttu-id="55a7d-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="55a7d-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="55a7d-111">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="55a7d-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="55a7d-112">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="55a7d-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="55a7d-113">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="55a7d-113">Click Run.</span></span>
<span data-ttu-id="55a7d-114">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="55a7d-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="55a7d-115">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="55a7d-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="55a7d-116">Hvis du vil vælge alle dimensioner i det aktuelle firma, skal du angive følgende oplysninger: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="55a7d-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="55a7d-118">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="55a7d-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="55a7d-119">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="55a7d-119">Click Filter.</span></span>
8. <span data-ttu-id="55a7d-120">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="55a7d-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="55a7d-121">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="55a7d-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="55a7d-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a7d-122">Click OK.</span></span>
11. <span data-ttu-id="55a7d-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a7d-123">Click OK.</span></span>
<span data-ttu-id="55a7d-124">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="55a7d-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="55a7d-125">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="55a7d-125">Review the generated output.</span></span> <span data-ttu-id="55a7d-126">For hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="55a7d-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="55a7d-127">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.</span><span class="sxs-lookup"><span data-stu-id="55a7d-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run4.png)
