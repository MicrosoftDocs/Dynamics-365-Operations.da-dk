---
title: Afstemme fragt i transportstyring
description: I denne artikel beskrives fragtafstemningsprocessen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 08b513609306bd4604cc910560324d87105afbf9
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="5c1b9-103">Afstemme fragt i transportstyring</span><span class="sxs-lookup"><span data-stu-id="5c1b9-103">Reconcile freight in transportation management</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5c1b9-104">I denne artikel beskrives fragtafstemningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="5c1b9-105">Fragtafstemning kan udføres manuelt, eller det kan indstilles til at ske automatisk.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="5c1b9-106">Hvis du vil bruge automatisk fragtafstemning, skal du angive en revisionsmaster, hvor du kan definere de kriterier, der bestemmer, hvilken fragtbreve der afstemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="5c1b9-107">Fragtafstemningsprocessen</span><span class="sxs-lookup"><span data-stu-id="5c1b9-107">The freight reconciliation process</span></span>
<span data-ttu-id="5c1b9-108">Fragtsatser beregnes af det satsprogram, der er knyttet til den relevante fragtmand.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="5c1b9-109">Når en belastning er bekræftet, oprettes der et fragtbrev, og fragtsatserne overføres til det.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="5c1b9-110">Fragtsatserne fordeles som diverse tillæg til det relevante kildedokument (indkøbsordre, salgsordre, og/eller flytteordre), afhængigt af den konfiguration, der bruges til den almindelige fakturering.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="5c1b9-111">Fragtafstemningsprocessen (der er også kaldes sammenholdelsesprocessen) kan begynde, så snart fragtfakturaen ankommer fra fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="5c1b9-112">Fakturaen kan modtages elektronisk eller på papir.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="5c1b9-113">Hvis fakturaen modtages på papir, kan du generere en elektronisk faktura ved at bruge fragtbrevet som skabelon.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="5c1b9-114">[![Fragtafstemningsproces](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="5c1b9-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="5c1b9-115">Manuel afstemning</span><span class="sxs-lookup"><span data-stu-id="5c1b9-115">Manual reconciliation</span></span>
<span data-ttu-id="5c1b9-116">Hvis du afstemmer fragt manuelt, skal du sammenholde hver fakturalinje med fragtbrevlinjen eller -linjerne for den belastning, der skal faktureres.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="5c1b9-117">Du udfører afstemningen på siden **Sammenholdelse af fragtbrev og faktura**.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="5c1b9-118">Hvis beløbet på fakturalinjen ikke stemmer overens med beløbet i fragtbrevet, skal du vælge en afstemningsårsag for forskellen.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="5c1b9-119">Hvis der er flere grunde til afstemning, kan du opdele uafstemte beløb på tværs af dem.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="5c1b9-120">Årsagen til afstemningen bestemmer, hvordan de forskellige beløb bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="5c1b9-121">Når afstemningen af hele fakturabeløbet er behandlet, sendes den til godkendelse, og derefter bogføres kladden.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="5c1b9-122">I følgende illustration vises, hvordan du opretter en fragtfaktura og udfører fragtafstemning in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="5c1b9-123">[![Fragtafstemningsopgaver i Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="5c1b9-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="5c1b9-124">Automatisk afstemning</span><span class="sxs-lookup"><span data-stu-id="5c1b9-124">Automatic reconciliation</span></span>
<span data-ttu-id="5c1b9-125">Hvis du vil bruge automatisk afstemning, skal du angive tidsplanen for afstemningen, og de fakturaer og fragtmænd der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="5c1b9-126">Sammenholdelse af fakturalinjer og fragtbreve sker i overensstemmelse med opsætningen af revisionsmaster- og fragtbrevtypen.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="5c1b9-127">Når du har kørt den automatiske afstemning, skal du håndtere eventuelle fakturaer, som systemet ikke kan afstemme.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="5c1b9-128">Du skal derefter behandle disse fakturaer manuelt, før du kan bogføre alle fakturaer til betaling.</span><span class="sxs-lookup"><span data-stu-id="5c1b9-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




