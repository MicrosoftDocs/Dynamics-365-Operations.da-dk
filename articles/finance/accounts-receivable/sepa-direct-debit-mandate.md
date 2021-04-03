---
title: Oprette bemyndigelse til SEPA Direct Debit
description: En direkte SEPA-debitering (fælles eurobetalingsområde (SEPA)) gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at debitoren er tildelt en signeret bemyndigelse til kreditor.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24803e7157edc87e73eb6c8af404311bdf8fc5c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245610"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="27c6d-103">Oprette bemyndigelse til SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="27c6d-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27c6d-104">En direkte SEPA-debitering (fælles eurobetalingsområde (SEPA)) gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at debitoren er tildelt en signeret bemyndigelse til kreditor.</span><span class="sxs-lookup"><span data-stu-id="27c6d-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="27c6d-105">Den bemyndigelse, som debitor underskriver, giver kreditoren tilladelse til at opkræve en betaling og beder kundens bank om at betale opkrævningen.</span><span class="sxs-lookup"><span data-stu-id="27c6d-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="27c6d-106">Dette emne er organiseret til at vise processen til oprettelse af SEPA-bemyndigelser til direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="27c6d-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27c6d-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="27c6d-107">Prerequisites</span></span>
<span data-ttu-id="27c6d-108">Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.</span><span class="sxs-lookup"><span data-stu-id="27c6d-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="27c6d-109">Kategori</span><span class="sxs-lookup"><span data-stu-id="27c6d-109">Category</span></span>       | <span data-ttu-id="27c6d-110">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="27c6d-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c6d-111">Land/område</span><span class="sxs-lookup"><span data-stu-id="27c6d-111">Country/region</span></span> | <span data-ttu-id="27c6d-112">Den primære adresse for den juridiske enhed skal være i de følgende lande: Østrig, Belgien, Tyskland, Spanien, Frankrig, Italien eller Nederlandene.</span><span class="sxs-lookup"><span data-stu-id="27c6d-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="27c6d-113">Opret en nummerserie til bemyndigelser til direkte debitering. Hver bemyndigelse til direkte debitering skal have et entydigt nummer.</span><span class="sxs-lookup"><span data-stu-id="27c6d-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="27c6d-114">Brug siden **Nummerserier** til at oprette en nummerserie for bemyndigelser til direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="27c6d-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="27c6d-115">Du skal bruge denne identifikator til at tildele nummerserien til systemet til bemyndigelser til direkte debitering på siden **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="27c6d-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="27c6d-116">Angiv debitorparametre for bemyndigelser til direkte debitering: Brug siden **Debitorparametre** til at konfigurere parametre for bemyndigelser til direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="27c6d-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="27c6d-117">For at angive parametrene under fanen **Direct Debit** skal du ændre standardparametrene efter behov.</span><span class="sxs-lookup"><span data-stu-id="27c6d-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="27c6d-118">Under fanen **Nummerserier** skal du derefter opdatere feltet **Id for bemyndigelse til Direct Debit** med den nummerserie, du har angivet tidligere.</span><span class="sxs-lookup"><span data-stu-id="27c6d-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="27c6d-119">Konfigurer en betalingsmåde for bemyndigelser til direkte debitering. Du skal angive en betalingsmåde for bemyndigelser til direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="27c6d-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="27c6d-120">Du kan bruge denne betalingsmåde til at forespørge om fakturaer, der skal genereres direkte debetbetalinger for.</span><span class="sxs-lookup"><span data-stu-id="27c6d-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="27c6d-121">Brug siden **Betalingsmetode** til at konfigurere betalingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="27c6d-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="27c6d-122">Hvis du vil konfigurere en betalingsmetode for bemyndigelse af direkte debitering, skal du følge følgende fremgangsmåde for en betalingsmetode:</span><span class="sxs-lookup"><span data-stu-id="27c6d-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="27c6d-123">I feltet **Betalingstype** skal du vælge **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="27c6d-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="27c6d-124">Valgfrit: Hvis du forventer, at hver af dine kunder skal have flere bemyndigelser, skal du i feltet **Periode** vælge **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="27c6d-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="27c6d-125">Der oprettes en separat betaling for hver faktura, og hver betaling bruger den bemyndigelse, der er angivet for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="27c6d-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="27c6d-126">Vælg indstillingen **Kræv bemyndigelse** for at oprette betalinger ved hjælp af bemyndigelser til direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="27c6d-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="27c6d-127">Indstillingen **Kræv bemyndigelse** er kun tilgængelig, hvis du vælger **Elektronisk betaling** i feltet **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="27c6d-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="27c6d-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="27c6d-128">Additional resources</span></span>

[<span data-ttu-id="27c6d-129">Oversigt over SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="27c6d-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="27c6d-130">Oprette en ny bemyndigelse til direkte debitering til en debitor</span><span class="sxs-lookup"><span data-stu-id="27c6d-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]