---
title: Tilmelde og fjerne frynsegoder fra arbejdere
description: Denne procedure viser, hvordan en enkelt medarbejder kan være tilmeldt et eller flere frynsegoder, og hvordan flere arbejdere kan være tilmeldt et frynsegode.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "857470"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="32dc0-103">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="32dc0-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32dc0-104">Denne procedure viser, hvordan en enkelt medarbejder kan være tilmeldt et eller flere frynsegoder, og hvordan flere arbejdere kan være tilmeldt et frynsegode.</span><span class="sxs-lookup"><span data-stu-id="32dc0-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="32dc0-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="32dc0-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="32dc0-106">Tilmelde en enkelt arbejder til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="32dc0-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="32dc0-107">Gå til Personale > Arbejdere > Medarbejdere</span><span class="sxs-lookup"><span data-stu-id="32dc0-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="32dc0-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="32dc0-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="32dc0-109">Klik på Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="32dc0-109">Click Benefits.</span></span>
4. <span data-ttu-id="32dc0-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="32dc0-110">Click New.</span></span>
5. <span data-ttu-id="32dc0-111">Indtast eller vælg en værdi i feltet Frynsegode.</span><span class="sxs-lookup"><span data-stu-id="32dc0-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="32dc0-112">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="32dc0-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="32dc0-113">Angiv en dato og et klokkeslæt i feltet Gyldigheds slutdato.</span><span class="sxs-lookup"><span data-stu-id="32dc0-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="32dc0-114">Udvid sektionen Beneficianter, hvis modtagerne skal føjes til frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="32dc0-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="32dc0-115">Du kan også tilføje afhængige fra denne side, hvis de er relevante for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="32dc0-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="32dc0-116">Du kan også redigere oplysningerne for en frynsegodetilmelding eller slette en tilmelding på denne side.</span><span class="sxs-lookup"><span data-stu-id="32dc0-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="32dc0-117">Når du har udført ændringerne tilmeldingen til frynsegodet, skal du lukke siden.</span><span class="sxs-lookup"><span data-stu-id="32dc0-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="32dc0-118">Tilmelde flere arbejdere til et frynsegode</span><span class="sxs-lookup"><span data-stu-id="32dc0-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="32dc0-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="32dc0-119">Close the page.</span></span>
2. <span data-ttu-id="32dc0-120">Gå til Personale > Arbejdere > Medarbejdere</span><span class="sxs-lookup"><span data-stu-id="32dc0-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="32dc0-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="32dc0-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="32dc0-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="32dc0-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="32dc0-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="32dc0-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="32dc0-124">Klik på Tilmeld i frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="32dc0-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="32dc0-125">Indtast eller vælg en værdi i feltet Frynsegode.</span><span class="sxs-lookup"><span data-stu-id="32dc0-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="32dc0-126">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="32dc0-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="32dc0-127">Angiv en dato og et klokkeslæt i feltet Gyldigheds slutdato.</span><span class="sxs-lookup"><span data-stu-id="32dc0-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="32dc0-128">Klik på Tilmeld.</span><span class="sxs-lookup"><span data-stu-id="32dc0-128">Click Enroll.</span></span>
11. <span data-ttu-id="32dc0-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="32dc0-129">Close the page.</span></span>
12. <span data-ttu-id="32dc0-130">Gå til Personale > Frynsegoder > Tilmelding > Resultater af tilmelding til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="32dc0-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="32dc0-131">Find den post med frynsegoderesultater, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="32dc0-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="32dc0-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="32dc0-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="32dc0-133">På denne side kan du få vist de medarbejdere, som er tilmeldt frynsegodet, samt alle medarbejdere, der ikke er tilmeldt.</span><span class="sxs-lookup"><span data-stu-id="32dc0-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

