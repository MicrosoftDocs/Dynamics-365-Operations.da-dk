---
title: Definer udgiftspolitikker
description: Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender rejserekvisitioner og udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389709"
---
# <a name="define-expense-policies"></a><span data-ttu-id="7b566-103">Definer udgiftspolitikker</span><span class="sxs-lookup"><span data-stu-id="7b566-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b566-104">Du kan definere politikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="7b566-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="7b566-105">At implementere udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="7b566-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="7b566-106">Du kan f.eks. angive en politik for hoteludgifter i New York City, som angiver, at udgiften pr. nat ikke må overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="7b566-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="7b566-107">Hvis en arbejder sender en udgiftsrapport eller en rejserekvisition, hvori værelsessatsen overskrider dette beløb, giver systemet arbejderen besked om,</span><span class="sxs-lookup"><span data-stu-id="7b566-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="7b566-108">at udgiftsbeløbet i henhold til politikken er overskredet.</span><span class="sxs-lookup"><span data-stu-id="7b566-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="7b566-109">Du kan konfigurere den meddelelse, som medarbejderen modtager, når du definerer</span><span class="sxs-lookup"><span data-stu-id="7b566-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="7b566-110">politikken.</span><span class="sxs-lookup"><span data-stu-id="7b566-110">define the policy.</span></span>      
        
<span data-ttu-id="7b566-111">Du kan definere tre typer politikker:</span><span class="sxs-lookup"><span data-stu-id="7b566-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="7b566-112">Advarsel – Gør det muligt for medarbejderen at sende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og</span><span class="sxs-lookup"><span data-stu-id="7b566-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="7b566-113">til senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="7b566-113">for later reporting.</span></span>        

- <span data-ttu-id="7b566-114">Fejl – kræver, at medarbejderen reviderer de udgifter, der i overensstemmelse med politikken, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="7b566-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="7b566-115">Justering – kræver, at medarbejderen eller en leder angiver en begrundelse for, hvorfor politikkens beløb er overskredet, inden udgiftsrapporten eller rejserekvisitionen sendes.</span><span class="sxs-lookup"><span data-stu-id="7b566-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="7b566-116">Tip om politik</span><span class="sxs-lookup"><span data-stu-id="7b566-116">Policy tips</span></span>
<span data-ttu-id="7b566-117">Her er nogle få forslag, der kan hjælpe dig, når du opretter nye politikker for udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="7b566-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="7b566-118">Politikker er datostyrede og træder ikke i kraft, hvis politikken oprettes med en dato efter den dato, hvor udgiften opstod.</span><span class="sxs-lookup"><span data-stu-id="7b566-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="7b566-119">Hvis du f.eks. opretter en ny politik i dag for at gennemtvinge en maksimal måltidsudgift på $50, kontrolleres eventuelle eksisterende udgifter, der er angivet pr. i går, ikke med denne politik.</span><span class="sxs-lookup"><span data-stu-id="7b566-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="7b566-120">Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetypen.</span><span class="sxs-lookup"><span data-stu-id="7b566-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="7b566-121">Visse politikker, som f.eks. kræver en kvittering, giver muligvis ikke mening for specificerede linjer og bør kun anvendes på hovedlinjen eller en ikke-specificeret linje.</span><span class="sxs-lookup"><span data-stu-id="7b566-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="7b566-122">Politikker for udgiftsstyring evalueres som standard i forhold til kildeenheden.</span><span class="sxs-lookup"><span data-stu-id="7b566-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="7b566-123">I forbindelse med interne scenarier kan du angive den politik, der skal evalueres i forhold til destinationsenheden (låneenheden) i stedet.</span><span class="sxs-lookup"><span data-stu-id="7b566-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="7b566-124">Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen "Evaluere udgiftspolitik i forhold til juridisk enhed for udlån" i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="7b566-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="7b566-125">Hvornår politikker skal evalueres</span><span class="sxs-lookup"><span data-stu-id="7b566-125">When to evaluate policies</span></span>

<span data-ttu-id="7b566-126">I parametrene for udgiftsstyring er der mulighed for enten at evaluere politikker for udgiftsstyring, når en linje gemmes, eller når en udgiftsrapport sendes.</span><span class="sxs-lookup"><span data-stu-id="7b566-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="7b566-127">Hvis du vælger at evaluere, når en linje gemmes, sikrer det brugerne en tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang.</span><span class="sxs-lookup"><span data-stu-id="7b566-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="7b566-128">Ellers kan du forsinke evalueringen af en politik og spare tid, hvis du får foretaget valideringen ved afslutningen, under afsendelse til arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="7b566-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
