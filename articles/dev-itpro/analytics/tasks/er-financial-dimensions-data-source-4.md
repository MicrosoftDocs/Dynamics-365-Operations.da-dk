--- 
title: "Køre en rapport, der bruger økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: c5aefc44adc24f9d216f9470e4307a3723690173
ms.contentlocale: da-dk
ms.lasthandoff: 11/02/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="f9781-103">Køre en rapport, der bruger økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="f9781-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9781-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="f9781-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f9781-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="f9781-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f9781-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)".</span><span class="sxs-lookup"><span data-stu-id="f9781-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="f9781-107">Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f9781-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="f9781-108">Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9781-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="f9781-109">Kør rapporter</span><span class="sxs-lookup"><span data-stu-id="f9781-109">Run report</span></span>
1. <span data-ttu-id="f9781-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f9781-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f9781-111">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="f9781-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f9781-112">Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="f9781-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="f9781-113">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="f9781-113">Click Run.</span></span>
5. <span data-ttu-id="f9781-114">I feltet Dimensionens navn skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="f9781-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="f9781-115">Hvis du vil vælge alle dimensioner i det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="f9781-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="f9781-116">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="f9781-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="f9781-117">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="f9781-117">Click Filter.</span></span>
8. <span data-ttu-id="f9781-118">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="f9781-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="f9781-119">Skriv "00057" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="f9781-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="f9781-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9781-120">Click OK.</span></span>
11. <span data-ttu-id="f9781-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9781-121">Click OK.</span></span>
    * <span data-ttu-id="f9781-122">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="f9781-122">Review the generated output.</span></span> <span data-ttu-id="f9781-123">Bemærk, at for hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f9781-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="f9781-124">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations, Enterprise edition-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f9781-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


