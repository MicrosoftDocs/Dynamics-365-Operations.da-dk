---
title: Tilmelde og fjerne frynsegoder fra arbejdere
description: Denne procedure viser, hvordan en enkelt medarbejder kan være tilmeldt et eller flere frynsegoder, og hvordan flere arbejdere kan være tilmeldt et frynsegode.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 13e32c9bc77470d6b8e157e7a7805d3d72850478
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111894"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="567ed-103">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="567ed-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="567ed-104">Denne procedure viser, hvordan en enkelt medarbejder kan være tilmeldt et eller flere frynsegoder, og hvordan flere arbejdere kan være tilmeldt et frynsegode.</span><span class="sxs-lookup"><span data-stu-id="567ed-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="567ed-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="567ed-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="567ed-106">Tilmelde en enkelt arbejder til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="567ed-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="567ed-107">Gå til Human Resources > Arbejdere > Medarbejdere</span><span class="sxs-lookup"><span data-stu-id="567ed-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="567ed-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="567ed-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="567ed-109">Klik på Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="567ed-109">Click Benefits.</span></span>
4. <span data-ttu-id="567ed-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="567ed-110">Click New.</span></span>
5. <span data-ttu-id="567ed-111">Indtast eller vælg en værdi i feltet Frynsegode.</span><span class="sxs-lookup"><span data-stu-id="567ed-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="567ed-112">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="567ed-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="567ed-113">Angiv en dato og et klokkeslæt i feltet Gyldigheds slutdato.</span><span class="sxs-lookup"><span data-stu-id="567ed-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="567ed-114">Udvid sektionen Beneficianter, hvis modtagerne skal føjes til frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="567ed-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="567ed-115">Du kan også tilføje afhængige fra denne side, hvis de er relevante for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="567ed-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="567ed-116">Du kan også redigere oplysningerne for en frynsegodetilmelding eller slette en tilmelding på denne side.</span><span class="sxs-lookup"><span data-stu-id="567ed-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="567ed-117">Når du har udført ændringerne tilmeldingen til frynsegodet, skal du lukke siden.</span><span class="sxs-lookup"><span data-stu-id="567ed-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="567ed-118">Tilmelde flere arbejdere til et frynsegode</span><span class="sxs-lookup"><span data-stu-id="567ed-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="567ed-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="567ed-119">Close the page.</span></span>
2. <span data-ttu-id="567ed-120">Gå til Human Resources > Arbejdere > Medarbejdere</span><span class="sxs-lookup"><span data-stu-id="567ed-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="567ed-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="567ed-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="567ed-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="567ed-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="567ed-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="567ed-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="567ed-124">Klik på Tilmeld i frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="567ed-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="567ed-125">Indtast eller vælg en værdi i feltet Frynsegode.</span><span class="sxs-lookup"><span data-stu-id="567ed-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="567ed-126">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="567ed-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="567ed-127">Angiv en dato og et klokkeslæt i feltet Gyldigheds slutdato.</span><span class="sxs-lookup"><span data-stu-id="567ed-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="567ed-128">Klik på Tilmeld.</span><span class="sxs-lookup"><span data-stu-id="567ed-128">Click Enroll.</span></span>
11. <span data-ttu-id="567ed-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="567ed-129">Close the page.</span></span>
12. <span data-ttu-id="567ed-130">Gå til Human Resources > Frynsegoder > Tilmelding > Resultater af tilmelding til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="567ed-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="567ed-131">Find den post med frynsegoderesultater, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="567ed-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="567ed-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="567ed-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="567ed-133">På denne side kan du få vist de medarbejdere, som er tilmeldt frynsegodet, samt alle medarbejdere, der ikke er tilmeldt.</span><span class="sxs-lookup"><span data-stu-id="567ed-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

