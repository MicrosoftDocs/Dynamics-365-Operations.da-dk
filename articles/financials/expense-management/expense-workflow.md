---
title: Arbejdsgang for udgift
description: Dette emne forklarer, hvordan du kan bruge arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations til at konfigurere en revisionsproces for udgiftsrapporter i Udgiftsstyring.
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 21815fccc91961653189f844718712faf573d2d7
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="aad04-103">Arbejdsgang for udgift</span><span class="sxs-lookup"><span data-stu-id="aad04-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aad04-104">Du kan bruge arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations til at konfigurere en revisionsproces for udgiftsrapporter i Udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="aad04-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="aad04-105">Du kan angive en arbejdsgang, der bruger følgende kriterier til at bestemme, hvem der skal godkende udgiftsrapporter:</span><span class="sxs-lookup"><span data-stu-id="aad04-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="aad04-106">Medarbejderens rapporteringshierarki og foruddefinerede godkendelsesbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="aad04-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="aad04-107">Godkendelse med flere niveauer, der understøtter midlertidige godkendere og en endelig godkender</span><span class="sxs-lookup"><span data-stu-id="aad04-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="aad04-108">Økonomiske dimensioner og projektansvar</span><span class="sxs-lookup"><span data-stu-id="aad04-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="aad04-109">Tildeling til bestemte brugere eller brugergrupper</span><span class="sxs-lookup"><span data-stu-id="aad04-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="aad04-110">Der kan oprettes godkendelse af arbejdsgangen for udgiftsrapporter, rejserekvisitioner, kontante forskud og refusion af moms.</span><span class="sxs-lookup"><span data-stu-id="aad04-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="aad04-111">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="aad04-111">**Example**</span></span>

<span data-ttu-id="aad04-112">Nedenstående proces er et eksempel på udgiftsstyringsarbejdsgangen for en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="aad04-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="aad04-113">En medarbejder opretter og gemmer en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="aad04-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="aad04-114">Medarbejderen sender udgiftsrapporten til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="aad04-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="aad04-115">Godkenderen identificeres ud fra de regler, der blev defineret, da arbejdsprocessen blev konfigureret.</span><span class="sxs-lookup"><span data-stu-id="aad04-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="aad04-116">Godkenderen modtager en meddelelse om, at en udgiftsrapport er klar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="aad04-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="aad04-117">Godkenderen gennemser udgiftsrapporten og kontrollerer, at følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="aad04-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="aad04-118">Udgifterne overtræder ikke nogen udgiftspolitikker.</span><span class="sxs-lookup"><span data-stu-id="aad04-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="aad04-119">Hvis en udgift overtræder en politik, kontrollerer godkenderen, at udgiftsrapporten omfatter en gyldig forretningsberettigelse.</span><span class="sxs-lookup"><span data-stu-id="aad04-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="aad04-120">Der er knyttet elektroniske kvitteringer til udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="aad04-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="aad04-121">Godkenderen godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="aad04-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="aad04-122">Udgiftsrapporten tildeles kreditorkoordinatoren for bogføring.</span><span class="sxs-lookup"><span data-stu-id="aad04-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="aad04-123">Et af følgende trin opstår, afhængigt af om der er konfigureret automatisk bogføring:</span><span class="sxs-lookup"><span data-stu-id="aad04-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="aad04-124">Hvis der er konfigureret automatisk bogføring, behandles udgiftsrapporten til betaling, og udgiftsrapportens status opdateres.</span><span class="sxs-lookup"><span data-stu-id="aad04-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="aad04-125">Hvis der ikke er konfigureret automatisk bogføring, kontrollerer kreditorkoordinatoren, at alle originale kvitteringer er indsendt, og at kvitteringerne svarer til udgifterne i udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="aad04-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="aad04-126">Alle momskoder, der er angivet på udgiftsrapporten, skal også kontrolleres som korrekte.</span><span class="sxs-lookup"><span data-stu-id="aad04-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="aad04-127">Når opfyldelsen af disse krav er kontrolleret, kan du bogføre udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="aad04-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="aad04-128">Når udgiftsrapporten er bogført, godkendes betaling for udgiftsrapporten, og medarbejderen bliver refunderet.</span><span class="sxs-lookup"><span data-stu-id="aad04-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

