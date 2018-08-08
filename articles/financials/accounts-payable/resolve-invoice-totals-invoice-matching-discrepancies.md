---
title: "Løse afvigelser under sammenholdelse af fakturatotaler"
description: "Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 67aa0b89eed1f82290659029dfcce92ca3710aea
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="1736e-103">Løse afvigelser under sammenholdelse af fakturatotaler</span><span class="sxs-lookup"><span data-stu-id="1736e-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1736e-104">En type validering af fakturasammenholdelse er matchning af fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="1736e-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="1736e-105">For at angive, at systemet skal udføre matchning af fakturatotaler skal du på siden **Kreditorparametre** på fanen **Fakturavalidering** angive indstillingen **Afstem fakturatotaler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1736e-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="1736e-106">Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse.</span><span class="sxs-lookup"><span data-stu-id="1736e-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="1736e-107">Seks totaler er sammenlignet på siden **Fakturatotalers tilsvarende oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="1736e-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="1736e-108">Hvis en af totalerne afviger fra de forventede tilsvarende indkøbsordretotal, markeres en matchningafvigelse.</span><span class="sxs-lookup"><span data-stu-id="1736e-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="1736e-109">For at gennemgå den faktura, der er matchningafvigelse for totaler, skal du i arbejdsområdet **Kreditorfakturapostering** klikke på flisen **Ventende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="1736e-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="1736e-110">Derefter skal du i handlingsruden på fanen **Gennemse** klikke på **Tilsvarende oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="1736e-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="1736e-111">Hvis der er konstateret matchningsafvigelser, vises der advarselsikoner ud for fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="1736e-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="1736e-112">Du kan få vist flere detaljer om totaler ved at få vist tilsvarende oplysninger for fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="1736e-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="1736e-113">Når du har identificeret afvigelse, kan det være nødvendigt at kontakte kreditoren, hvis du mener, at oplysningerne på fakturaen er forkerte.</span><span class="sxs-lookup"><span data-stu-id="1736e-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="1736e-114">Afhængigt af den indgåede aftale med kreditoren, kan du gøre en af følgende:</span><span class="sxs-lookup"><span data-stu-id="1736e-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="1736e-115">Accepter prisforskellen og bogfør fakturaen, der har matchningafvigelser.</span><span class="sxs-lookup"><span data-stu-id="1736e-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="1736e-116">Systemet kan konfigureres til at kræve godkendelse, inden den kan bogføre, hvis der er matchningafvigelser.</span><span class="sxs-lookup"><span data-stu-id="1736e-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="1736e-117">I så fald du skal godkende matchningafvigelsen og eventuelt indtaste en kommentar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="1736e-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="1736e-118">Du kan derefter vælge at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1736e-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="1736e-119">Revider fakturabeløbet med det forventede beløb, og bogfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1736e-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="1736e-120">Anmod om fuld kredit og en ny, rettet faktura fra kreditoren.</span><span class="sxs-lookup"><span data-stu-id="1736e-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="1736e-121">Yderligere oplysninger finder du i [Undersøge eller løse undtagelser](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="1736e-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



