---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "345277"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="817c3-103">ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)</span><span class="sxs-lookup"><span data-stu-id="817c3-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="817c3-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="817c3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="817c3-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="817c3-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="817c3-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="817c3-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="817c3-107">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="817c3-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="817c3-108">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="817c3-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="817c3-109">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="817c3-109">Run report</span></span>
1. <span data-ttu-id="817c3-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="817c3-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="817c3-111">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="817c3-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="817c3-112">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="817c3-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="817c3-113">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="817c3-113">Click Run.</span></span>
5. <span data-ttu-id="817c3-114">I feltet Dimensionens navn skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="817c3-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="817c3-115">Hvis du vil vælge alle dimensioner i det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="817c3-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="817c3-116">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="817c3-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="817c3-117">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="817c3-117">Click Filter.</span></span>
8. <span data-ttu-id="817c3-118">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="817c3-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="817c3-119">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="817c3-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="817c3-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="817c3-120">Click OK.</span></span>
11. <span data-ttu-id="817c3-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="817c3-121">Click OK.</span></span>
    * <span data-ttu-id="817c3-122">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="817c3-122">Review the generated output.</span></span> <span data-ttu-id="817c3-123">Bemærk, at for hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="817c3-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="817c3-124">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations Enterprise edition-forekomst.</span><span class="sxs-lookup"><span data-stu-id="817c3-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

