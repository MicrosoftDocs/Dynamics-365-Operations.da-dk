---
title: Administrere udstyr, der er udlånt til arbejdere
description: Udlånsemner er poster, der hjælper ledere med at holde styr på de fysiske emner, som virksomheden udlåner til sine arbejdere.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5915df388da7ce8b90cdcb0e859268c00003110c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417793"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="e0f7f-103">Administrere udstyr, der er udlånt til arbejdere</span><span class="sxs-lookup"><span data-stu-id="e0f7f-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="e0f7f-104">Udlånsemner er poster, der hjælper ledere med at holde styr på de fysiske emner, som virksomheden udlåner til sine arbejdere.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="e0f7f-105">Følgende punkter viser eksempler på emner, som en virksomhed kan udlåne til arbejdere:</span><span class="sxs-lookup"><span data-stu-id="e0f7f-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="e0f7f-106">Mobiltelefoner</span><span class="sxs-lookup"><span data-stu-id="e0f7f-106">Mobile telephones</span></span>
-   <span data-ttu-id="e0f7f-107">Biler</span><span class="sxs-lookup"><span data-stu-id="e0f7f-107">Automobiles</span></span>
-   <span data-ttu-id="e0f7f-108">Computerudstyr</span><span class="sxs-lookup"><span data-stu-id="e0f7f-108">Computer equipment</span></span>

<span data-ttu-id="e0f7f-109">Alle fysiske emner skal have et tilknyttet udlånsemne.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="e0f7f-110">Alle udlånsemneposter skal beskrive, hvad der udlånes, hvem der er ansvarlig for udlånet, og det antal dage, emnet kan udlånes til en arbejder.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="e0f7f-111">Du kan oprette flere udlånsemner f.eks. for emner som nøgler, adgangskort og uniformer, på samme tid.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="e0f7f-112">Når et emne udlånes, skal du angive den dato, emnet blev udlånt, samt den planlagte tilbageleveringsdato.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="e0f7f-113">Når emnet tilbageleveres, skal du angive den faktiske tilbageleveringsdato.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="e0f7f-114">Medarbejderne kan få vist poster for de varer, der er lånt ud til dem, ved hjælp af medarbejderens selvbetjeningsarbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="e0f7f-115">De kan også redigere eksisterende poster eller angive nye udlånsemner, hvis de har modtaget flere fysiske elementer.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="e0f7f-116">Arbejdsprocessen kan konfigureres til at rute ændringer til nye eller eksisterende udlånsemner gennem en godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="e0f7f-117">Ledere kan få vist udlånte emner for deres direkte rapporter.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="e0f7f-118">De kan også få tilladelse til at tilføje nye udlån på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="e0f7f-119">Konto for beskadigede eller mistede udlånsemner</span><span class="sxs-lookup"><span data-stu-id="e0f7f-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="e0f7f-120">Hvis et emne bliver beskadiget eller mistes, skal du angive en fiktiv tilbageleveringspost.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="e0f7f-121">Derefter skal du enten slette emnet eller beholde det i oversigten og ændre beskrivelsen for at angive, at emnet ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e0f7f-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e0f7f-122">Additional resources</span></span>
--------

[<span data-ttu-id="e0f7f-123">Personale</span><span class="sxs-lookup"><span data-stu-id="e0f7f-123">Human resources</span></span>](index.md)



