---
title: Beregning af kildeskat for interne transaktioner
description: Dette emne beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023121"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="a759f-103">Beregning af kildeskat for interne transaktioner</span><span class="sxs-lookup"><span data-stu-id="a759f-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a759f-104">Dette emne beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.</span><span class="sxs-lookup"><span data-stu-id="a759f-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="a759f-105">Når der oprettes en intern indkøbsordre eller salgsordre, bruges den standardgruppe for kildeskat, som er defineret for debitoren eller kreditoren, til at beregne skattebeløbet.</span><span class="sxs-lookup"><span data-stu-id="a759f-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="a759f-106">Når fakturaen bogføres, bogføres skattebeløbet på de relevante konti for tilgodehavende eller skyldig skat.</span><span class="sxs-lookup"><span data-stu-id="a759f-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="a759f-107">Der oprettes automatisk en intern salgsordre eller indkøbsordre for den oprindelige indkøbsordre eller salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a759f-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="a759f-108">Standardskattegruppen vises på den interne ordre, så kildeskatten kan beregnes.</span><span class="sxs-lookup"><span data-stu-id="a759f-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="a759f-109">Du kan ændre kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="a759f-109">You can change the TDS group.</span></span> <span data-ttu-id="a759f-110">Fakturaen kan kun bogføres, hvis nettofakturabeløbet på den interne ordre, som er oprettet automatisk, svarer til nettofakturabeløbet på den oprindelige ordre.</span><span class="sxs-lookup"><span data-stu-id="a759f-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="a759f-111">(Nettobeløbet er fakturabeløbet, efter kildeskatten er fratrukket).</span><span class="sxs-lookup"><span data-stu-id="a759f-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="a759f-112">Der oprettes f.eks. en salgsfaktura på 50.000, og kildeskattegruppen **10 %** bliver tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="a759f-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="a759f-113">Det bogførte fakturabeløb er 45.000, og det bogførte skattebeløb for salgsfakturaen er 5.000.</span><span class="sxs-lookup"><span data-stu-id="a759f-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="a759f-114">Der oprettes automatisk en indkøbsordre for den interne salgsordre, og kildeskattegruppen **10 %** bliver tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="a759f-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="a759f-115">Hvis du ændrer TDS-gruppen til **15 %**, kan du ikke bogføre fakturaen, da nettofakturabeløbet for den interne salgsordre, der er oprettet automatisk, ikke svarer til nettofakturabeløbet på den oprindelige salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a759f-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="a759f-116">Der oprettes og bogføres automatisk en betalingskladde for en intern faktura.</span><span class="sxs-lookup"><span data-stu-id="a759f-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="a759f-117">Denne betalingskladde kan kun bogføres, hvis nettobetalingsbeløbet på den svarer til nettobetalingsbeløbet på den oprindelige betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="a759f-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
