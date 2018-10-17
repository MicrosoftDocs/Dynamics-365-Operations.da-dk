--- 
title: "Opret betalingsmåde til ISO20022 direkte debet"
description: "Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 953a3cffc356ab44163944318e7e7d542a113112
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="8e097-103">Opret betalingsmåde til ISO20022 direkte debet</span><span class="sxs-lookup"><span data-stu-id="8e097-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e097-104">Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="8e097-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="8e097-105">Før du udfører denne opgave, skal du konfigurere eksportformatkonfigurationer og betalingskonti.</span><span class="sxs-lookup"><span data-stu-id="8e097-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="8e097-106">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="8e097-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="8e097-107">Det er den tredje procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="8e097-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="8e097-108">Gå til Debitor > Betalingsopsætning > Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="8e097-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="8e097-109">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="8e097-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8e097-110">Filtrer f.eks. efter feltet Betalingsmåde med værdien "ELECTRONIC".</span><span class="sxs-lookup"><span data-stu-id="8e097-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="8e097-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="8e097-111">Click Edit.</span></span>
4. <span data-ttu-id="8e097-112">I feltet Betalingskonto skal du specificere værdierne "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="8e097-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="8e097-113">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="8e097-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="8e097-114">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="8e097-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="8e097-115">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8e097-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8e097-116">Vælg ISO20022 Direct debit (DE) på listen.</span><span class="sxs-lookup"><span data-stu-id="8e097-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="8e097-117">Hvis listen er tom, betyder det, at der ikke er nogen importeret og aktiv eksportformatkonfiguration for kundebetaling.</span><span class="sxs-lookup"><span data-stu-id="8e097-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="8e097-118">Vælg Ja i feltet Kræv bemyndigelse.</span><span class="sxs-lookup"><span data-stu-id="8e097-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="8e097-119">Vælg parameteren Kræv bemyndigelse for formater for debitorbetalinger, der kræver, at der medtages bemyndigelse i betalingsmeddelelsen, f.eks. SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="8e097-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="8e097-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8e097-120">Click Save.</span></span>


