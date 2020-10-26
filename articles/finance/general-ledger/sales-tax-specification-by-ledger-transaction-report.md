---
title: Momsspecifikation pr. finanstransaktionsrapport
description: Dette emne forklarer, hvordan du kan bruge rapporten Momsspecifikation pr. finanstransaktion til at se og udskrive oplysninger om finanstransaktioner, der er beregnet moms for.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976085"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="635c9-103">Momsspecifikation pr. finanstransaktionsrapport</span><span class="sxs-lookup"><span data-stu-id="635c9-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="635c9-104">Dette emne forklarer, hvordan du kan bruge rapporten **Momsspecifikation pr. finanstransaktion** til at se og udskrive oplysninger om finanstransaktioner, der er beregnet moms for.</span><span class="sxs-lookup"><span data-stu-id="635c9-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="635c9-105">Momskonti versus ikke-momskonti</span><span class="sxs-lookup"><span data-stu-id="635c9-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="635c9-106">Rapporten **Momsspecifikation efter finanstransaktion** viser momstransaktioner for både momskonti og ikke-momskonti.</span><span class="sxs-lookup"><span data-stu-id="635c9-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="635c9-107">Disse konti kategoriseres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="635c9-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="635c9-108">**Momskonto** – En konto betragtes som en momskonto, når der bogføres en momstransaktion, og hovedkontoen på **Moms**-kladdelinjen er en momskonto, f.eks. en konto for udgående moms eller en indgående momskonto.</span><span class="sxs-lookup"><span data-stu-id="635c9-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="635c9-109">**Ikke-momskonto** – En konto betragtes som en ikke-momskonto, når der bogføres en momstransaktion, og hovedkontoen på den oprindelige transaktion er en ikke-momskonto, f.eks. en indtægtskonto eller en udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="635c9-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="635c9-110">For momskonti viser kolonnerne **Original**, **Indgående moms** og **Udgående moms** i rapporten **0** (nul).</span><span class="sxs-lookup"><span data-stu-id="635c9-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="635c9-111">I forbindelse med ikke-momskonti viser disse kolonner beløb.</span><span class="sxs-lookup"><span data-stu-id="635c9-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="635c9-112">Filtrering af dataene i rapporten</span><span class="sxs-lookup"><span data-stu-id="635c9-112">Filtering the data on the report</span></span>

<span data-ttu-id="635c9-113">Når du opretter rapporten, er følgende standardfelter tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="635c9-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="635c9-114">Du kan bruge disse felter til at filtrere de data, der vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="635c9-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="635c9-115">Felt</span><span class="sxs-lookup"><span data-stu-id="635c9-115">Field</span></span>                      | <span data-ttu-id="635c9-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="635c9-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="635c9-117">Dato</span><span class="sxs-lookup"><span data-stu-id="635c9-117">Date</span></span>                       | <span data-ttu-id="635c9-118">Brug felterne i sektionerne **Fra** og **Til** til at definere et datointerval for momstransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="635c9-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="635c9-119">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="635c9-119">Main account</span></span>               | <span data-ttu-id="635c9-120">Brug felterne i sektionerne **Fra** og **Til** til at definere et interval af hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="635c9-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="635c9-121">Momskode</span><span class="sxs-lookup"><span data-stu-id="635c9-121">Sales tax code</span></span>             | <span data-ttu-id="635c9-122">Brug felterne i sektionerne **Fra** og **Til** til at definere et interval af momskoder.</span><span class="sxs-lookup"><span data-stu-id="635c9-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="635c9-123">Gruppering</span><span class="sxs-lookup"><span data-stu-id="635c9-123">Grouping</span></span>                   | <span data-ttu-id="635c9-124">Vælg, om rapporten skal grupperes efter finanskonto eller momskode.</span><span class="sxs-lookup"><span data-stu-id="635c9-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="635c9-125">Subtotal efter momskode</span><span class="sxs-lookup"><span data-stu-id="635c9-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="635c9-126">Angiv denne indstilling til **Ja** for at få vist subtotaler efter momskode.</span><span class="sxs-lookup"><span data-stu-id="635c9-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="635c9-127">Kun totaler</span><span class="sxs-lookup"><span data-stu-id="635c9-127">Totals only</span></span>                | <span data-ttu-id="635c9-128">Angiv denne indstilling til **Ja** for kun at få vist totaler.</span><span class="sxs-lookup"><span data-stu-id="635c9-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="635c9-129">Kun hovedkonti</span><span class="sxs-lookup"><span data-stu-id="635c9-129">Main accounts only</span></span>         | <span data-ttu-id="635c9-130">Angiv denne indstilling til **Ja** for kun at medtage hovedkonti i rapporten.</span><span class="sxs-lookup"><span data-stu-id="635c9-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="635c9-131">Visning af ikke-momskonti i rapporten</span><span class="sxs-lookup"><span data-stu-id="635c9-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="635c9-132">Hvis du kun vil have vist ikke-momskonti i rapporten, skal du konfigurere en filterbetingelse, f.eks. en stjerne (\*), som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="635c9-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Rapport, der viser ikke-momskonti](media/taxspecperledgertrans.png)
