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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406468"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="d7bf9-103">ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7bf9-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d7bf9-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d7bf9-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="d7bf9-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="d7bf9-107">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="d7bf9-108">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="d7bf9-109">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="d7bf9-109">Run report</span></span>
1. <span data-ttu-id="d7bf9-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d7bf9-111">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d7bf9-112">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="d7bf9-113">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-113">Click Run.</span></span>
<span data-ttu-id="d7bf9-114">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="d7bf9-115">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="d7bf9-116">Hvis du vil vælge alle dimensioner i det aktuelle firma, skal du angive følgende oplysninger: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="d7bf9-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="d7bf9-118">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d7bf9-119">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-119">Click Filter.</span></span>
8. <span data-ttu-id="d7bf9-120">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="d7bf9-121">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="d7bf9-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-122">Click OK.</span></span>
11. <span data-ttu-id="d7bf9-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-123">Click OK.</span></span>
<span data-ttu-id="d7bf9-124">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="d7bf9-125">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-125">Review the generated output.</span></span> <span data-ttu-id="d7bf9-126">For hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="d7bf9-127">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run4.png)
