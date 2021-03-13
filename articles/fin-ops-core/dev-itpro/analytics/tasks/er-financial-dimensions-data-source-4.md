---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 4)
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
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092269"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="0ccdb-104">ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)</span><span class="sxs-lookup"><span data-stu-id="0ccdb-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ccdb-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="0ccdb-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0ccdb-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="0ccdb-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="0ccdb-108">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="0ccdb-109">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="0ccdb-110">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="0ccdb-110">Run report</span></span>
1. <span data-ttu-id="0ccdb-111">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0ccdb-112">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0ccdb-113">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="0ccdb-114">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-114">Click Run.</span></span>
<span data-ttu-id="0ccdb-115">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="0ccdb-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="0ccdb-116">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="0ccdb-117">Hvis du vil vælge alle dimensioner i det aktuelle firma, skal du angive følgende oplysninger: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="0ccdb-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="0ccdb-119">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="0ccdb-120">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-120">Click Filter.</span></span>
8. <span data-ttu-id="0ccdb-121">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="0ccdb-122">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="0ccdb-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-123">Click OK.</span></span>
11. <span data-ttu-id="0ccdb-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-124">Click OK.</span></span>
<span data-ttu-id="0ccdb-125">![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="0ccdb-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="0ccdb-126">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-126">Review the generated output.</span></span> <span data-ttu-id="0ccdb-127">For hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="0ccdb-128">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.</span><span class="sxs-lookup"><span data-stu-id="0ccdb-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run4.png)
