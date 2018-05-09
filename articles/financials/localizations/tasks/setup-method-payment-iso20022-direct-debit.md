--- 
title: Konfigurere en betalingsmetode for ISO20022 Direct Debit
description: "Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d18a72b511d51cbeb69f5b417defe0974112a67d
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="48f62-103">Konfigurere en betalingsmetode for ISO20022 Direct Debit</span><span class="sxs-lookup"><span data-stu-id="48f62-103">Set up method of payment for ISO20022 direct debit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48f62-104">Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="48f62-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="48f62-105">Før du udfører denne opgave, skal du konfigurere eksportformatkonfigurationer og betalingskonti.</span><span class="sxs-lookup"><span data-stu-id="48f62-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="48f62-106">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="48f62-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="48f62-107">Det er den tredje procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="48f62-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="48f62-108">Gå til Debitor > Betalingsopsætning > Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="48f62-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="48f62-109">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="48f62-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="48f62-110">Filtrer f.eks. efter feltet Betalingsmåde med værdien "ELECTRONIC".</span><span class="sxs-lookup"><span data-stu-id="48f62-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="48f62-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="48f62-111">Click Edit.</span></span>
4. <span data-ttu-id="48f62-112">I feltet Betalingskonto skal du specificere værdierne "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="48f62-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="48f62-113">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="48f62-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="48f62-114">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="48f62-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="48f62-115">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="48f62-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="48f62-116">Vælg ISO20022 Direct debit (DE) på listen.</span><span class="sxs-lookup"><span data-stu-id="48f62-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="48f62-117">Hvis listen er tom, betyder det, at der ikke er nogen importeret og aktiv eksportformatkonfiguration for kundebetaling.</span><span class="sxs-lookup"><span data-stu-id="48f62-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="48f62-118">Vælg Ja i feltet Kræv bemyndigelse.</span><span class="sxs-lookup"><span data-stu-id="48f62-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="48f62-119">Vælg parameteren Kræv bemyndigelse for formater for debitorbetalinger, der kræver, at der medtages bemyndigelse i betalingsmeddelelsen, f.eks. SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="48f62-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="48f62-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48f62-120">Click Save.</span></span>


