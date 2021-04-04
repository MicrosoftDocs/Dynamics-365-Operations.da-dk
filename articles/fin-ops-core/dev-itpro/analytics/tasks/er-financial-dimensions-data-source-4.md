---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565208"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="c63d2-104">ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)</span><span class="sxs-lookup"><span data-stu-id="c63d2-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c63d2-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="c63d2-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c63d2-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="c63d2-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c63d2-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="c63d2-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="c63d2-108">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="c63d2-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="c63d2-109">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c63d2-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="c63d2-110">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="c63d2-110">Run report</span></span>
1. <span data-ttu-id="c63d2-111">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="c63d2-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c63d2-112">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="c63d2-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c63d2-113">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="c63d2-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="c63d2-114">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="c63d2-114">Click Run.</span></span>
<span data-ttu-id="c63d2-115">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="c63d2-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="c63d2-116">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="c63d2-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="c63d2-117">Hvis du vil vælge alle dimensioner i det aktuelle firma, skal du angive følgende oplysninger: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="c63d2-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="c63d2-119">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="c63d2-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c63d2-120">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="c63d2-120">Click Filter.</span></span>
8. <span data-ttu-id="c63d2-121">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="c63d2-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="c63d2-122">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="c63d2-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="c63d2-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c63d2-123">Click OK.</span></span>
11. <span data-ttu-id="c63d2-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c63d2-124">Click OK.</span></span>
<span data-ttu-id="c63d2-125">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="c63d2-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="c63d2-126">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="c63d2-126">Review the generated output.</span></span> <span data-ttu-id="c63d2-127">For hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="c63d2-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="c63d2-128">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.</span><span class="sxs-lookup"><span data-stu-id="c63d2-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]