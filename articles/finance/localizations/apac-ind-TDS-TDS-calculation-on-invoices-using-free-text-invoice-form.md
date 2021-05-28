---
title: Beregning af kildeskat på fakturaer fra siden Fritekstfaktura
description: Dette emne beskriver, hvordan du beregner kildeskat på fakturaer ved hjælp af siden Fritekstfaktura.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023124"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="e62e7-103">Beregning af kildeskat på fakturaer fra siden Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="e62e7-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e62e7-104">Dette emne beskriver, hvordan du beregner kildeskat på fakturaer ved hjælp af siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="e62e7-105">Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="e62e7-106">[![Siden Fritekstfaktura](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="e62e7-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="e62e7-107">Vælg **Ny** for at oprette en fritekstfaktura, og angive de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e62e7-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="e62e7-108">Vælg fanen **Faktura**. I feltet **Art af vurdering** i sektionen **Gruppe for A-skat** vises vurderingskatagorien for debitoren.</span><span class="sxs-lookup"><span data-stu-id="e62e7-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="e62e7-109">I feltet **Kildeskattegruppe** kan du gennemse eller ændre den standardgruppe for kildeskat, der er defineret for debitoren.</span><span class="sxs-lookup"><span data-stu-id="e62e7-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e62e7-110">Når du vælger en værdi i feltet **Kildeskattegruppe** bliver feltet **Kildeskattegruppe** utilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="e62e7-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="e62e7-111">Kildeskat beregnes kun, hvis indstillingen **Beregn A-skat** er angivet til **Ja** for debitoren på siden **Alle debitorer**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="e62e7-112">På fanen **Skatteoplysninger** i sektionen **Firmaoplysninger** i feltet **Navn** skal du vælge virksomhedens navn for en alternativ adresse, som er angivet for virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e62e7-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="e62e7-113">I sektionen **A-skat** viser feltet **Skattekontonummer (TAN)** skattekontonummeret (TAN – Tax Account Number) for den valgte virksomhed.</span><span class="sxs-lookup"><span data-stu-id="e62e7-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="e62e7-114">Opret fakturalinjer under fanen **Fakturalinjer**, og angiv de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e62e7-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="e62e7-115">I sektionen **Gruppe for A-skat** viser feltet **Skattekontonummer (TAN)** skattekontonummeret, og feltet **Kildeskattegruppe** viser gruppen for kildeskat.</span><span class="sxs-lookup"><span data-stu-id="e62e7-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="e62e7-116">Vælg **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="e62e7-117">Den øverste del af denne side indeholder følgende felter:</span><span class="sxs-lookup"><span data-stu-id="e62e7-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="e62e7-118">**Samlet beløb for A-skat** – Den samlede kildeskat er beregnet for transaktionen for kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="e62e7-119">**Værdi** – Den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="e62e7-120">Den samlede procentdel er baseret på den formel, der er defineret for kildeskattekoderne og er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="e62e7-121">**Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="e62e7-122">**Kildeskat** – Et markeret afkrydsningsfelt angiver, at der er knyttet en kildeskattegruppe til transaktionen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="e62e7-123">Felterne under fanen **Oversigt**, **Generelt** og **Regulering** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, som er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="e62e7-124">Vælg **Tærskel** for at åbne siden **Tærskel**, hvor du kan gennemse den grænseværdi, der er defineret for den skattekomponent, som er tilknyttet en specifik kildeskattekode.</span><span class="sxs-lookup"><span data-stu-id="e62e7-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="e62e7-125">Vælg **Formeldesigner** for at åbne siden **Formeldesigner**, hvor du kan gennemse den formel, der er defineret for en specifik kildeskattekode.</span><span class="sxs-lookup"><span data-stu-id="e62e7-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="e62e7-126">Bogfør fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-126">Post the free text invoice.</span></span> <span data-ttu-id="e62e7-127">Det skattebeløb, der er beregnet for fritekstfakturaen, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="e62e7-128">Kreditorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="e62e7-129">Vælg **Bogført A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e62e7-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="e62e7-130">Feltet **Værdi** viser den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="e62e7-131">Felterne under fanen **Oversigt**, **Generelt** og **Beløb** viser de skattebeløb, der blev beregnet på fakturalinjerne.</span><span class="sxs-lookup"><span data-stu-id="e62e7-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="e62e7-132">Gennemse beregningsoplysningerne for kildeskat for hver kildeskattekode, der er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="e62e7-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
