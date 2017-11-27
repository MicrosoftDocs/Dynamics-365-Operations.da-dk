---
title: Definer udgiftspolitikker
description: "Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="b2731-103">Udgiftspolitikker</span><span class="sxs-lookup"><span data-stu-id="b2731-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b2731-104">Du kan definere politikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="b2731-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="b2731-105">At implementere udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="b2731-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="b2731-106">Du kan f.eks. angive en politik for hoteludgifter i New York City, som angiver, at udgiften pr. nat ikke må overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="b2731-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="b2731-107">Hvis en arbejder sender en udgiftsrapport eller en rejserekvisition, hvori værelsessatsen overskrider dette beløb, giver systemet arbejderen besked om, at politikbeløbet for udgiften er overskredet.</span><span class="sxs-lookup"><span data-stu-id="b2731-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="b2731-108">Du kan konfigurere den meddelelse, som medarbejderen modtager, når du definerer politikken.</span><span class="sxs-lookup"><span data-stu-id="b2731-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="b2731-109">Du kan definere tre typer politikker:</span><span class="sxs-lookup"><span data-stu-id="b2731-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="b2731-110">Advarsel – Gør det muligt for medarbejderen at sende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og</span><span class="sxs-lookup"><span data-stu-id="b2731-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="b2731-111">til senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="b2731-111">for later reporting.</span></span> 
 - <span data-ttu-id="b2731-112">Fejl – kræver, at medarbejderen reviderer de udgifter, der i overensstemmelse med politikken, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="b2731-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="b2731-113">Justering – kræver, at medarbejderen eller en leder angiver en begrundelse for, hvorfor politikkens beløb er overskredet, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="b2731-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="b2731-114">Du kan også angive et datointerval, hvor udgiftspolitikkerne er gældende.</span><span class="sxs-lookup"><span data-stu-id="b2731-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="b2731-115">For eksempel kan luftfartsselskabets billetpriser for flyvninger mellem Danmark og New York City være dyre i højsæsonen.</span><span class="sxs-lookup"><span data-stu-id="b2731-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="b2731-116">Du kan definere en regel for flyudgifter, der begrænser omkostningerne ved flyvninger til New York City til en grænse på DKK 5000, og du kan angive, at denne regel er gældende mellem 15. marts og 15. september.</span><span class="sxs-lookup"><span data-stu-id="b2731-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

