---
title: Konfigurer arbejdsgange til udgifter
description: Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 384c38f3e154495c882434d1c85cef63396cd897
ms.openlocfilehash: 8294aaa344e3cb6b79fa4f33f368258ca19c8205
ms.contentlocale: da-dk
ms.lasthandoff: 08/15/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="9b1c7-103">Konfigurer arbejdsgange til udgifter</span><span class="sxs-lookup"><span data-stu-id="9b1c7-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b1c7-104"> Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="9b1c7-105">De dokumenter, der kan være defineret en arbejdsgang for, omfatter udgiftsrapporter, rejserekvisitioner og anmodninger om kontaktforskud.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="9b1c7-106">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-106">A workflow represents a business process.</span></span> <span data-ttu-id="9b1c7-107">Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9b1c7-108">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="9b1c7-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="9b1c7-109">**Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9b1c7-110">Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="9b1c7-111">Synliggørelse af processer – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9b1c7-112">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="9b1c7-113">Centraliseret arbejdsliste – Brugerne kan få vist en centraliseret arbejdsliste for at se opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="9b1c7-114">**De typer arbejdsgange, du kan oprette**</span><span class="sxs-lookup"><span data-stu-id="9b1c7-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="9b1c7-115">Tabellen nedenfor viser de typer arbejdsgange, du kan oprette i **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="9b1c7-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="9b1c7-117"><strong>Brug denne type til at</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="9b1c7-118"><strong>Udgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="9b1c7-119">Oprette godkendelsesarbejdsgange for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="9b1c7-120"><strong>Automatisk bogføring af udgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="9b1c7-121">Oprette arbejdsgange for automatisk bogføring for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="9b1c7-122"><strong>Udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="9b1c7-123">Oprette godkendelsesarbejdsgange for linjevarer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="9b1c7-124"><strong>Automatisk bogføring af udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="9b1c7-125">Oprette arbejdsgange for automatisk bogføring for linjevarer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="9b1c7-126"><strong>Rejserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="9b1c7-127">Oprette godkendelsesarbejdsgange for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="9b1c7-128"><strong>Anmodning om kontantforskud</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="9b1c7-129">Oprette arbejdsgange for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="9b1c7-130"><strong>Momsopkrævning</strong></span><span class="sxs-lookup"><span data-stu-id="9b1c7-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="9b1c7-131">Oprette godkendelsesarbejdsgange for momsopkrævning.</span><span class="sxs-lookup"><span data-stu-id="9b1c7-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


