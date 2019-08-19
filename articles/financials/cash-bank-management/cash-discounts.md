---
title: Kasserabatter
description: Kasserabatter konfigureres og deles for kreditor og debitor.  Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842539"
---
# <a name="cash-discounts"></a><span data-ttu-id="3ca86-104">Kasserabatter</span><span class="sxs-lookup"><span data-stu-id="3ca86-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ca86-105">Kasserabatter konfigureres og deles for kreditor og debitor.</span><span class="sxs-lookup"><span data-stu-id="3ca86-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="3ca86-106">Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="3ca86-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="3ca86-107">Kasserabatter</span><span class="sxs-lookup"><span data-stu-id="3ca86-107">Cash discounts</span></span>

<span data-ttu-id="3ca86-108">Kasserabatter for både debitorer eller kreditorer kan oprettes på siden Kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="3ca86-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="3ca86-109">Du kan også bruge feltet Næste rabatkode til at definere en række kasserabatter, der følger efter hinanden, efterhånden som tidligere kasserabatdatoer udløber.</span><span class="sxs-lookup"><span data-stu-id="3ca86-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="3ca86-110">Du kan finde flere oplysninger i "Eksempel: En række kasserabatter" senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="3ca86-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="3ca86-111">Hvis fakturaen, kreditposteringen (enten en betaling eller en kreditnota) eller begge angives en anden valuta end regnskabsvalutaen for den juridiske enhed, beregnes kasserabatten ved hjælp af valutakursen baseret på datoen for betalingen eller kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="3ca86-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="3ca86-112">Hvis fakturaen eller kreditdokumentet er angivet for forskellige juridiske enheder, og hvis regnskabsvalutaen for de juridiske enheder er forskellig, tages valutakursen fra den juridiske enhed for fakturaen på datoen for kreditdokumentet.</span><span class="sxs-lookup"><span data-stu-id="3ca86-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="3ca86-113">Du kan finde flere oplysninger i "Eksempel: Valutakurser for kasserabatter" senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="3ca86-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="3ca86-114">Standardrækkefølge af hovedkonto for kasserabat</span><span class="sxs-lookup"><span data-stu-id="3ca86-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="3ca86-115">Hvis en faktura udlignes inden for det tidsrum, der medfører en kasserabat, bogføres kasserabatten automatisk på en hovedkonto for kasserabatter i overensstemmelse med følgende standardprioritet:</span><span class="sxs-lookup"><span data-stu-id="3ca86-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="3ca86-116">Den hovedkonto, der er angivet i feltet Alternativ kasserabatkonto på debitorsiden Udlign åbne posteringer eller kreditorsiden Udlign åbne posteringer.</span><span class="sxs-lookup"><span data-stu-id="3ca86-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="3ca86-117">Den hovedkonto, der er angivet i feltet Debitor, kasserabat eller feltet Kreditor kasserabat i den finanskonteringsgruppe, der er knyttet til fakturaens momskode.</span><span class="sxs-lookup"><span data-stu-id="3ca86-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="3ca86-118">Konfigurer finanskonteringsgrupper på siden Finanskonteringsgrupper, og tildel dem til momskoder på siden Momskoder.</span><span class="sxs-lookup"><span data-stu-id="3ca86-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="3ca86-119">Hovedkonteringsgruppen på siden Kasserabatter i feltet Hovedkonto til debitorrabatter eller feltet Hovedkonto til kreditorrabatter for kasserabatkoden, der er anført på den udlignede faktura.</span><span class="sxs-lookup"><span data-stu-id="3ca86-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="3ca86-120">Hovedkontoen til kasserabatter, som defineret på siden Konti til automatiske posteringer.</span><span class="sxs-lookup"><span data-stu-id="3ca86-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="3ca86-121"> Eksempel: En række kasserabatter</span><span class="sxs-lookup"><span data-stu-id="3ca86-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="3ca86-122">Opret tre kasserabatkoder på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3ca86-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="3ca86-123">Kode 5D10% – En kasserabat på 10 %, når beløbet betales inden for fem dage.</span><span class="sxs-lookup"><span data-stu-id="3ca86-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="3ca86-124">Kode 10D5% – En kasserabat på 5 %, når beløbet betales inden for 10 dage.</span><span class="sxs-lookup"><span data-stu-id="3ca86-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="3ca86-125">Kode 14D2% – En kasserabat på 2 %, når beløbet betales inden for 14 dage.</span><span class="sxs-lookup"><span data-stu-id="3ca86-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="3ca86-126">I feltet Næste rabatkode:</span><span class="sxs-lookup"><span data-stu-id="3ca86-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="3ca86-127">Vælg 10D5% for koden 5D10%.</span><span class="sxs-lookup"><span data-stu-id="3ca86-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="3ca86-128">Vælg 14D2% for koden 10D5%.</span><span class="sxs-lookup"><span data-stu-id="3ca86-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="3ca86-129">For koden 14D2% skal du lade feltet Næste rabatkode være tomt.</span><span class="sxs-lookup"><span data-stu-id="3ca86-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="3ca86-130">De tre kasserabatter følger efter hinanden, når betalingsdatoen overskrider den tidligere kasserabatdato på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="3ca86-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="3ca86-131">Der gives kun én kasserabat, når fakturaen betales, ud fra hvilken dato for kasserabat, der opfyldes i rækkefølgen af kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="3ca86-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="3ca86-132"> Eksempel: Valutakurser for kasserabatter</span><span class="sxs-lookup"><span data-stu-id="3ca86-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="3ca86-133">Din juridiske enheds regnskabsvaluta i EUR og de følgende valutakurser, der er angivet for USD:</span><span class="sxs-lookup"><span data-stu-id="3ca86-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="3ca86-134">1. februar = 110</span><span class="sxs-lookup"><span data-stu-id="3ca86-134">February 1 = 110</span></span>
-   <span data-ttu-id="3ca86-135">1. marts = 80</span><span class="sxs-lookup"><span data-stu-id="3ca86-135">March 1 = 80</span></span>

<span data-ttu-id="3ca86-136">En faktura på 1000 USD med kasserabatbetingelserne for 20D2% bogføres den 15. februar.</span><span class="sxs-lookup"><span data-stu-id="3ca86-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="3ca86-137">Beløbet i regnskabsvalutaen for fakturaen er 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="3ca86-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="3ca86-138">Der foretages en betaling på 980 USD for fakturaen den 1. marts.</span><span class="sxs-lookup"><span data-stu-id="3ca86-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="3ca86-139">Kasserabatbeløbet er 20 USD.</span><span class="sxs-lookup"><span data-stu-id="3ca86-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="3ca86-140">Regnskabsvalutabeløbet for betalingen er 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="3ca86-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="3ca86-141">Regnskabsvalutabeløbet for kasserabatten beregnes ved hjælp af valutakursen for 1. marts: 20 \* 80/100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="3ca86-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="3ca86-142">Hvis indstillingen Beregn kasserabatter for delvise betalinger er valgt på siden Debitorparametre eller siden Kreditorparametre, bruges den valutakurs, der er gældende på datoen for hver delvise betaling.</span><span class="sxs-lookup"><span data-stu-id="3ca86-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

