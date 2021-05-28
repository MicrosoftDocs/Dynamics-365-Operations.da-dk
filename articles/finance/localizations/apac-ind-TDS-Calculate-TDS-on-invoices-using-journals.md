---
title: Beregne kildeskat for fakturaer ved hjælp af kladder
description: Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) i kladder.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023132"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="aa56a-103">Beregne kildeskat for fakturaer ved hjælp af kladder</span><span class="sxs-lookup"><span data-stu-id="aa56a-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa56a-104">Dette emne angiver trinnene til beregning af kildeskat (TDS – Tax Deducted at Source) i kladder.</span><span class="sxs-lookup"><span data-stu-id="aa56a-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="aa56a-105">Begynd med at åbne siden **Finanskladder** (**Finans > Kladdeposter > Finanskladder**).</span><span class="sxs-lookup"><span data-stu-id="aa56a-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="aa56a-106">[![Finanskladder](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="aa56a-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="aa56a-107">Opret kladdelinjer ved hjælp af de kladdeformularer, der er vist i tabellen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="aa56a-108">Vælg kontotypen og modkontotypen, og angiv transaktionsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="aa56a-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="aa56a-109">På siden **Fakturagodkendelseskladde** skal du vælge **Find bilag** og vælge de fakturaer, der skal beregnes kildeskat på.</span><span class="sxs-lookup"><span data-stu-id="aa56a-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="aa56a-110">Få vist de fakturaer, der er oprettet på siden **Fakturaregister** eller siden **Find bilag**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="aa56a-111">På siden **Kladdebilag** på fanen **Generelt** kan du få vist eller redigere den skattestandardgruppe, der er defineret for kreditoren eller debitoren, i feltet **Skattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="aa56a-112">Det skattebeløb, der er beregnet på kladdelinjerne, er baseret på den formel, der er defineret for de kildeskattekoder, der er angivet i feltet **Skattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="aa56a-113">Feltet **Gruppe for A-skat** og feltet **TCS-gruppe** bliver ikke tilgængeligt, når du vælger en kildeskattegruppe i feltet **Skattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="aa56a-114">Feltet **Gruppe for A-skat** er kun tilgængeligt på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="aa56a-115">Kildeskat beregnes kun, hvis afkrydsningsfeltet **Beregn A-skat** er markeret for kreditoren eller debitoren på siden **Alle kreditorer** eller **Alle debitorer**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="aa56a-116">Vælg fanen **Skatteoplysninger**. Hvis det er nødvendigt, kan du vælge de alternative adresser til en virksomhed, som er oprettet for virksomheden i dette felt.</span><span class="sxs-lookup"><span data-stu-id="aa56a-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="aa56a-117">Du kan få vist virksomhedens navn i feltet **Navn**, som findes under feltgruppen **Firmaoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="aa56a-118">Få vist arten af vurderingskategorien for kreditoren eller debitoren i feltet **Art af vurdering**, som findes i feltgruppen **A-skat**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="aa56a-119">I feltet **Skattekontonummer** (**TAN**) kan du få vist skattekontonummeret for det valgte virksomhedsnavn, der vises.</span><span class="sxs-lookup"><span data-stu-id="aa56a-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="aa56a-120">Vælg **A-skat** i menuen **A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="aa56a-121">Følgende felter vises i øverste rude på siden **Midlertidige transaktioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="aa56a-122">**Samlet beløb for A-skat** – Det samlede skattebeløb beregnet for transaktionen for kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="aa56a-123">**Værdi** – Den samlede procentdel, der bruges til beregning af kildeskat for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="aa56a-124">Den samlede procentdel er baseret på den formel, der er defineret for de kildeskattekoder, som er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="aa56a-125">**Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="aa56a-126">**Kildeskat** – Hvis dette felt markeres, knyttes der en kildeskattegruppe til transaktionen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="aa56a-127">Felterne under fanen **Oversigt**, **Generelt** og **Regulering** på siden **Midlertidige transaktioner for A-skat** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="aa56a-128">Vælg **Tærskel** for at åbne siden **Tærskel**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="aa56a-129">Få vist grænseværdien og den tærskel for fritagelse, der er defineret for den kildeskattekomponent, som er tilknyttet en bestemt kildeskattekode på denne side.</span><span class="sxs-lookup"><span data-stu-id="aa56a-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="aa56a-130">Vælg **Formeldesigner** for at åbne formularen **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="aa56a-131">Få vist den formel, der er defineret for en bestemt kildeskattekode, på denne side.</span><span class="sxs-lookup"><span data-stu-id="aa56a-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="aa56a-132">Luk **Formeldesigner** og siderne for **Midlertidige transaktioner for A-skat** for at vende tilbage til siden **Kladdebilag**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="aa56a-133">Angiv de øvrige krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="aa56a-133">Enter the other required details.</span></span> <span data-ttu-id="aa56a-134">Valider og bogfør kladden.</span><span class="sxs-lookup"><span data-stu-id="aa56a-134">Validate and post the journal.</span></span> <span data-ttu-id="aa56a-135">Det skattebeløb, der er beregnet for indkøbsfakturaer, bogføres på kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="aa56a-136">Det skattebeløb, der er beregnet for salgsfakturaer, bogføres på den debitorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="aa56a-137">Kreditorkonti eller debitorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="aa56a-138">Vælg **Bogført A-skat** for at åbne siden **Midlertidige** **transaktioner for** **A-skat**.</span><span class="sxs-lookup"><span data-stu-id="aa56a-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="aa56a-139">I feltet **Værdi** vises den samlede procentdel, der anvendes til at beregne kildeskat for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="aa56a-140">Felterne under fanen **Oversigt**, **Generelt** og **Beløb** på siden Midlertidige transaktioner for A-skat viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, der er tilknyttet kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa56a-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
