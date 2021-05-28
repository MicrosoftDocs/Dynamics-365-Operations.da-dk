---
title: Beregne skattefakturaer ved hjælp af formularerne Indkøbsordre og Salgsordre
description: Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) for forskellige typer fakturaer.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023108"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="85edc-103">Beregne skattefakturaer ved hjælp af formularerne Indkøbsordre og Salgsordre</span><span class="sxs-lookup"><span data-stu-id="85edc-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85edc-104">Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) for forskellige typer fakturaer ved hjælp af siderne **Indkøbsordre**, **Indkøbskladde**, **Rammeordre** og **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="85edc-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="85edc-105">Opret en indkøbsordre, indkøbskladde, købsrammeordre eller en salgsordre ved hjælp af den viste side.</span><span class="sxs-lookup"><span data-stu-id="85edc-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="85edc-106">Angiv de relevante oplysninger.</span><span class="sxs-lookup"><span data-stu-id="85edc-106">Enter the required details.</span></span>

2. <span data-ttu-id="85edc-107">Vælg fanen **Opsætning** for at få vist arten af kreditorens eller debitorens vurdering.</span><span class="sxs-lookup"><span data-stu-id="85edc-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="85edc-108">Disse oplysninger vises i feltet **Art af vurdering** under feltgruppen **Gruppe for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="85edc-109">I feltet **Skattegruppe** kan du få vist eller redigere den skattestandardgruppe, der er defineret for kreditoren eller debitoren.</span><span class="sxs-lookup"><span data-stu-id="85edc-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="85edc-110">Feltet **TCS-gruppe** er ikke tilgængeligt, når du vælger en kildeskattegruppe i feltet **Kildeskattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="85edc-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="85edc-111">Kildeskat beregnes kun, hvis afkrydsningsfeltet **Beregn A-skat** er markeret for kreditoren eller debitoren på siden **Alle kreditorer** eller **Alle debitorer**.</span><span class="sxs-lookup"><span data-stu-id="85edc-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="85edc-112">Opret varelinjer under fanen **Linjer**, og angiv de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="85edc-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="85edc-113">Vælg fanen **Opsætning** (linjeniveau) for at få vist eller ændre den kildeskattegruppe, der er defineret på overskriftsniveau.</span><span class="sxs-lookup"><span data-stu-id="85edc-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="85edc-114">Skattegruppen vises i feltet **Skattegruppe**, som findes under feltgruppen **Gruppe for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="85edc-115">Vælg fanen **Skatteoplysninger**, og vælg alternative adresser, der er oprettet for det firmanavn, der vises i dette felt.</span><span class="sxs-lookup"><span data-stu-id="85edc-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="85edc-116">Firmanavnet vises i feltet **Navn**, som findes under feltgruppen **Firmaoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="85edc-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="85edc-117">Det amerikanske skattenavn for det valgte firma vises i feltet **Skattekontonummer** (**TAN**) under feltgruppen **A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="85edc-118">Vælg **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="85edc-119">Få vist følgende felter i øverste rude på siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="85edc-120">**Samlet** **beløb** **af** **A-skat** – Det samlede skattebeløb beregnet for transaktionen for kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="85edc-121">**Værdi** – Den samlede procentdel, der bruges til beregning af kildeskat for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="85edc-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="85edc-122">Den samlede procentdel er baseret på den formel, der er defineret for de kildeskattekoder, som er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="85edc-123">**Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="85edc-124">**Kildeskat** – Hvis dette felt markeres, knyttes der en kildeskattegruppe til transaktionen.</span><span class="sxs-lookup"><span data-stu-id="85edc-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="85edc-125">Felterne under fanen **Oversigt**, **Generelt** og **Regulering** på siden **Midlertidige transaktioner for A-skat** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="85edc-126">Vælg **Tærskel** for at åbne siden **Tærskel**.</span><span class="sxs-lookup"><span data-stu-id="85edc-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="85edc-127">Få vist den grænseværdi, der er defineret for kildeskattekomponenten, som er tilknyttet en bestemt kildeskattekode på denne side.</span><span class="sxs-lookup"><span data-stu-id="85edc-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="85edc-128">Vælg **Formeldesigner** for at åbne siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="85edc-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="85edc-129">Få vist den formel, der er defineret for en bestemt kildeskattekode, på denne side.</span><span class="sxs-lookup"><span data-stu-id="85edc-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="85edc-130">Bogfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="85edc-130">Post the invoice.</span></span> <span data-ttu-id="85edc-131">Det skattebeløb, der er beregnet for indkøbsfakturaer, bogføres på kreditorkontoen, og det skattebeløb, der er beregnet på salgsfakturaer, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="85edc-132">Kreditorkonti eller debitorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="85edc-133">Vælg knappen **Forespørgsel** **> Faktura > Bogført A-skat** for at åbne siden **Transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="85edc-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="85edc-134">Du kan få vist den samlede procentdel, der er anvendt til at beregne skatteværdier for transaktionen, i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="85edc-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="85edc-135">Felterne under fanen **Oversigt**, **Generelt** og **Beløb** på siden **Transaktioner for A-skat** viser oplysningerne om den kildeskat, der er beregnet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="85edc-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="85edc-136">Få vist skatteberegningsoplysningerne for hver kildeskattekode, der er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="85edc-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
