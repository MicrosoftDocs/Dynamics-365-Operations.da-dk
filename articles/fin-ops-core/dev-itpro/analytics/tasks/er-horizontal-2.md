---
title: 'ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 2: Kørselsformat)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til generering af rapporter som OPENXML-regneark (Excel-filer). (Del 2)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c13179f424d570b23615fe81ca5ddfb7afed582d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093470"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="a9301-104">ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 2: Kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="a9301-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9301-105">Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret.</span><span class="sxs-lookup"><span data-stu-id="a9301-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="a9301-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="a9301-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a9301-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Brug ER vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter (del 1: Designformat)".</span><span class="sxs-lookup"><span data-stu-id="a9301-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="a9301-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="a9301-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="a9301-109">Find oprettet format</span><span class="sxs-lookup"><span data-stu-id="a9301-109">Find created format</span></span>
1. <span data-ttu-id="a9301-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="a9301-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a9301-111">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="a9301-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a9301-112">Vælg 'Eksempelmodel til økonomiske dimensioner\Eksempel på rapport med vandret områder, der kan udvides' i træet.</span><span class="sxs-lookup"><span data-stu-id="a9301-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="a9301-113">Udfør format for at oprette Excel-output</span><span class="sxs-lookup"><span data-stu-id="a9301-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="a9301-114">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="a9301-114">Click Run.</span></span>
2. <span data-ttu-id="a9301-115">Skriv 'BusinessUnit;CostCenter;Department' i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="a9301-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="a9301-116">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="a9301-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="a9301-117">Hvis du vil vælge alle dimensioner for det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="a9301-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="a9301-118">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="a9301-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="a9301-119">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="a9301-119">Click Filter.</span></span>
5. <span data-ttu-id="a9301-120">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="a9301-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="a9301-121">Skriv '00057..00058' i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="a9301-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="a9301-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="a9301-122">00057..00058</span></span>  
7. <span data-ttu-id="a9301-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a9301-123">Click OK.</span></span>
8. <span data-ttu-id="a9301-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a9301-124">Click OK.</span></span>
    * <span data-ttu-id="a9301-125">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="a9301-125">Review the generated output.</span></span> <span data-ttu-id="a9301-126">Bemærk, at den netop oprettede Excel-fil indeholder det samme antal kolonner, der er valgt for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a9301-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="a9301-127">Rapporthovedet i disse kolonner repræsenterer navnene på økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a9301-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="a9301-128">Transaktionslinjerne i disse kolonner repræsenterer økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a9301-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="a9301-129">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.</span><span class="sxs-lookup"><span data-stu-id="a9301-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

