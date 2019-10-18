---
title: Administrere udstyr, der er udlånt til arbejdere
description: Udlånsemner er poster, der hjælper ledere med at holde styr på de fysiske emner, som virksomheden udlåner til sine arbejdere.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 73ffe05d8c869418f7601025e8ce19e1b05c952f
ms.sourcegitcommit: 0dd8d0510214f92936a9dd214b404c5c8103587b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2419240"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="1abf0-103">Administrere udstyr, der er udlånt til arbejdere</span><span class="sxs-lookup"><span data-stu-id="1abf0-103">Manage items that are lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1abf0-104">Udlånsemner er poster, der hjælper ledere med at holde styr på de fysiske emner, som virksomheden udlåner til sine arbejdere.</span><span class="sxs-lookup"><span data-stu-id="1abf0-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="1abf0-105">Følgende punkter viser eksempler på emner, som en virksomhed kan udlåne til arbejdere:</span><span class="sxs-lookup"><span data-stu-id="1abf0-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="1abf0-106">Mobiltelefoner</span><span class="sxs-lookup"><span data-stu-id="1abf0-106">Mobile telephones</span></span>
-   <span data-ttu-id="1abf0-107">Biler</span><span class="sxs-lookup"><span data-stu-id="1abf0-107">Automobiles</span></span>
-   <span data-ttu-id="1abf0-108">Computerudstyr</span><span class="sxs-lookup"><span data-stu-id="1abf0-108">Computer equipment</span></span>

<span data-ttu-id="1abf0-109">Alle fysiske emner skal have et tilknyttet udlånsemne.</span><span class="sxs-lookup"><span data-stu-id="1abf0-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="1abf0-110">Alle udlånsemneposter skal beskrive, hvad der udlånes, hvem der er ansvarlig for udlånet, og det antal dage, emnet kan udlånes til en arbejder.</span><span class="sxs-lookup"><span data-stu-id="1abf0-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="1abf0-111">Du kan oprette flere udlånsemner f.eks. for emner som nøgler, adgangskort og uniformer, på samme tid.</span><span class="sxs-lookup"><span data-stu-id="1abf0-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="1abf0-112">Når et emne udlånes, skal du angive den dato, emnet blev udlånt, samt den planlagte tilbageleveringsdato.</span><span class="sxs-lookup"><span data-stu-id="1abf0-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="1abf0-113">Når emnet tilbageleveres, skal du angive den faktiske tilbageleveringsdato.</span><span class="sxs-lookup"><span data-stu-id="1abf0-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="1abf0-114">Medarbejderne kan få vist poster for de varer, der er lånt ud til dem, ved hjælp af medarbejderens selvbetjeningsarbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="1abf0-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="1abf0-115">De kan også redigere eksisterende poster eller angive nye udlånsemner, hvis de har modtaget flere fysiske elementer.</span><span class="sxs-lookup"><span data-stu-id="1abf0-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="1abf0-116">Arbejdsprocessen kan konfigureres til at rute ændringer til nye eller eksisterende udlånsemner gennem en godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="1abf0-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="1abf0-117">Ledere kan få vist udlånte emner for deres direkte rapporter.</span><span class="sxs-lookup"><span data-stu-id="1abf0-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="1abf0-118">De kan også få tilladelse til at tilføje nye udlån på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="1abf0-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="1abf0-119">Konto for beskadigede eller mistede udlånsemner</span><span class="sxs-lookup"><span data-stu-id="1abf0-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="1abf0-120">Hvis et emne bliver beskadiget eller mistes, skal du angive en fiktiv tilbageleveringspost.</span><span class="sxs-lookup"><span data-stu-id="1abf0-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="1abf0-121">Derefter skal du enten slette emnet eller beholde det i oversigten og ændre beskrivelsen for at angive, at emnet ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="1abf0-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="1abf0-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1abf0-122">Additional resources</span></span>
--------

[<span data-ttu-id="1abf0-123">Personale</span><span class="sxs-lookup"><span data-stu-id="1abf0-123">Human resources</span></span>](index.yml)



