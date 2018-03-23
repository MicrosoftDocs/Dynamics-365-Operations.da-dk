---
title: Definer udgiftspolitikker
description: "Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: b52fe81015a324bde07f387b42b834b79dc7c2da
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="expense-policies"></a><span data-ttu-id="11e70-103">Udgiftspolitikker</span><span class="sxs-lookup"><span data-stu-id="11e70-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11e70-104">Du kan definere politikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="11e70-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="11e70-105">At implementere udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="11e70-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="11e70-106">Du kan f.eks. angive en politik for hoteludgifter i New York City, som angiver, at udgiften pr. nat ikke må overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="11e70-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="11e70-107">Hvis en arbejder sender en udgiftsrapport eller en rejserekvisition, hvori værelsessatsen overskrider dette beløb, giver systemet arbejderen besked om,</span><span class="sxs-lookup"><span data-stu-id="11e70-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="11e70-108">at udgiftsbeløbet i henhold til politikken er overskredet.</span><span class="sxs-lookup"><span data-stu-id="11e70-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="11e70-109">Du kan konfigurere den meddelelse, som medarbejderen modtager, når du definerer</span><span class="sxs-lookup"><span data-stu-id="11e70-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="11e70-110">politikken.</span><span class="sxs-lookup"><span data-stu-id="11e70-110">define the policy.</span></span>      
        
<span data-ttu-id="11e70-111">Du kan definere tre typer politikker:</span><span class="sxs-lookup"><span data-stu-id="11e70-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="11e70-112">Advarsel – Gør det muligt for medarbejderen at sende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og</span><span class="sxs-lookup"><span data-stu-id="11e70-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
<span data-ttu-id="11e70-113">til senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="11e70-113">for later reporting.</span></span>        

- <span data-ttu-id="11e70-114">Fejl – kræver, at medarbejderen reviderer de udgifter, der i overensstemmelse med politikken, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="11e70-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="11e70-115">Justering – kræver, at medarbejderen eller en leder angiver en begrundelse for, hvorfor politikkens beløb er overskredet, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="11e70-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
 <span data-ttu-id="11e70-116">Du kan også angive et datointerval, hvor udgiftspolitikkerne er gældende.</span><span class="sxs-lookup"><span data-stu-id="11e70-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="11e70-117">For eksempel kan luftfartsselskabets billetpriser for flyvninger mellem Danmark</span><span class="sxs-lookup"><span data-stu-id="11e70-117">For example, airline fares for flights between Denmark</span></span>      
 <span data-ttu-id="11e70-118">og New York City være høje i højsæsonen.</span><span class="sxs-lookup"><span data-stu-id="11e70-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="11e70-119">Du kan definere en regel for udgifter til flyvning, der begrænser</span><span class="sxs-lookup"><span data-stu-id="11e70-119">You can define a flight expense rule that restricts the</span></span>      
 <span data-ttu-id="11e70-120">omkostningerne ved flyvninger til New York til DKK 5000, og du kan angive, at denne regel er gældende mellem 15. marts og</span><span class="sxs-lookup"><span data-stu-id="11e70-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
 <span data-ttu-id="11e70-121">15. september.</span><span class="sxs-lookup"><span data-stu-id="11e70-121">September 15.</span></span>

