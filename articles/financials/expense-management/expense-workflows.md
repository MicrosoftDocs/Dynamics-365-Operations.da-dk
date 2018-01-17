---
title: Konfigurer arbejdsgange til udgifter
description: Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter.
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="040da-103">Konfigurer arbejdsgange til udgifter</span><span class="sxs-lookup"><span data-stu-id="040da-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="040da-104"> Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="040da-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="040da-105">De dokumenter, der kan være defineret en arbejdsgang for, omfatter udgiftsrapporter, rejserekvisitioner og anmodninger om kontaktforskud.</span><span class="sxs-lookup"><span data-stu-id="040da-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="040da-106">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="040da-106">A workflow represents a business process.</span></span> <span data-ttu-id="040da-107">Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="040da-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="040da-108">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="040da-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="040da-109">**Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="040da-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="040da-110">Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="040da-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="040da-111">Synliggørelse af processer – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="040da-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="040da-112">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="040da-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="040da-113">Centraliseret arbejdsliste – Brugerne kan få vist en centraliseret arbejdsliste for at se opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="040da-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="040da-114">**De typer arbejdsgange, du kan oprette**</span><span class="sxs-lookup"><span data-stu-id="040da-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="040da-115">Tabellen nedenfor viser de typer arbejdsgange, du kan oprette i **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="040da-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="040da-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="040da-116">**Type**</span></span>                           | <span data-ttu-id="040da-117">**Brug denne type til at**</span><span class="sxs-lookup"><span data-stu-id="040da-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="040da-118">**Udgiftsrapport**</span><span class="sxs-lookup"><span data-stu-id="040da-118">**Expense report**</span></span>                 | <span data-ttu-id="040da-119">Oprette godkendelsesarbejdsgange for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="040da-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="040da-120">**Automatisk bogføring af udgiftsrapport**</span><span class="sxs-lookup"><span data-stu-id="040da-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="040da-121">Oprette arbejdsgange for automatisk bogføring for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="040da-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="040da-122">**Udgiftslinjeelement**</span><span class="sxs-lookup"><span data-stu-id="040da-122">**Expense line item**</span></span>              | <span data-ttu-id="040da-123">Oprette godkendelsesarbejdsgange for linjevarer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="040da-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="040da-124">**Automatisk bogføring af udgiftslinjeelement**</span><span class="sxs-lookup"><span data-stu-id="040da-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="040da-125">Oprette arbejdsgange for automatisk bogføring for linjevarer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="040da-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="040da-126">**Rejserekvisition**</span><span class="sxs-lookup"><span data-stu-id="040da-126">**Travel requisition**</span></span>             | <span data-ttu-id="040da-127">Oprette godkendelsesarbejdsgange for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="040da-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="040da-128">**Anmodning om kontantforskud**</span><span class="sxs-lookup"><span data-stu-id="040da-128">**Cash advance request**</span></span>           | <span data-ttu-id="040da-129">Oprette arbejdsgange for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="040da-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="040da-130">**Momsopkrævning**</span><span class="sxs-lookup"><span data-stu-id="040da-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="040da-131">Oprette godkendelsesarbejdsgange for momsopkrævning.</span><span class="sxs-lookup"><span data-stu-id="040da-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

