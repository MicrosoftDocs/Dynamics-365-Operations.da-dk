--- 
title: "Køre et format, der bruger områder, der kan udvides i vandret retning, for at tilføje kolonnerne i Excel-rapporter dynamisk"
description: "Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c4538bd9f8c71108e7ec8fd9da2c2b914d76f13
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="23f7e-103">Køre et format, der bruger områder, der kan udvides i vandret retning, for at tilføje kolonnerne i Excel-rapporter dynamisk</span><span class="sxs-lookup"><span data-stu-id="23f7e-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23f7e-104">Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret.</span><span class="sxs-lookup"><span data-stu-id="23f7e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="23f7e-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="23f7e-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="23f7e-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Brug ER vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter (del 1: Designformat)".</span><span class="sxs-lookup"><span data-stu-id="23f7e-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="23f7e-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="23f7e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="23f7e-108">Find oprettet format</span><span class="sxs-lookup"><span data-stu-id="23f7e-108">Find created format</span></span>
1. <span data-ttu-id="23f7e-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="23f7e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="23f7e-110">Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="23f7e-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="23f7e-111">Vælg 'Eksempelmodel til økonomiske dimensioner\Eksempel på rapport med vandret områder, der kan udvides' i træet.</span><span class="sxs-lookup"><span data-stu-id="23f7e-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="23f7e-112">Udfør format for at oprette Excel-output</span><span class="sxs-lookup"><span data-stu-id="23f7e-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="23f7e-113">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="23f7e-113">Click Run.</span></span>
2. <span data-ttu-id="23f7e-114">Skriv 'BusinessUnit;CostCenter;Department' i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="23f7e-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="23f7e-115">Indtast eller vælg en værdi i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="23f7e-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="23f7e-116">Hvis du vil vælge alle dimensioner for det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="23f7e-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="23f7e-117">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="23f7e-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="23f7e-118">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="23f7e-118">Click Filter.</span></span>
5. <span data-ttu-id="23f7e-119">Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="23f7e-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="23f7e-120">Skriv '00057..00058' i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="23f7e-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="23f7e-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="23f7e-121">00057..00058</span></span>  
7. <span data-ttu-id="23f7e-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23f7e-122">Click OK.</span></span>
8. <span data-ttu-id="23f7e-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23f7e-123">Click OK.</span></span>
    * <span data-ttu-id="23f7e-124">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="23f7e-124">Review the generated output.</span></span> <span data-ttu-id="23f7e-125">Bemærk, at den netop oprettede Excel-fil indeholder det samme antal kolonner, der er valgt for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="23f7e-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="23f7e-126">Rapporthovedet i disse kolonner repræsenterer navnene på økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="23f7e-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="23f7e-127">Transaktionslinjerne i disse kolonner repræsenterer økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="23f7e-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="23f7e-128">Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations-forekomst.</span><span class="sxs-lookup"><span data-stu-id="23f7e-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


