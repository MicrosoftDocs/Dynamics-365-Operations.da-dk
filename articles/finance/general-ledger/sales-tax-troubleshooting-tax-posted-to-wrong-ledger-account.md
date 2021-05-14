---
title: Momsen er bogført på den forkerte finanskonto i bilaget
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe, når moms bogføres på den forkerte finanskonto i bilaget.
author: qire
manager: beya
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0404d71f0492e188ed5da62387bb90a336e69c5a
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947615"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="f3ef3-103">Momsen er bogført på den forkerte finanskonto i bilaget</span><span class="sxs-lookup"><span data-stu-id="f3ef3-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3ef3-104">Under bogføringen kan momsen blive bogført på den forkerte finanskonto i bilaget.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="f3ef3-105">Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="f3ef3-106">I eksemplerne i dette emne bruges en salgsordre som virksomhedsdokument.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="f3ef3-107">Find momskoden for den forkerte bogførte momspostering</span><span class="sxs-lookup"><span data-stu-id="f3ef3-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="f3ef3-108">Vælg den postering, du vil arbejde med, på siden **Bilagsposteringer**, og vælg derefter **Bogført moms**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="f3ef3-109">[![Knappen Bogført moms på siden Bilagsposteringer](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="f3ef3-110">Gennemse værdien i feltet **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="f3ef3-111">I dette eksempel er værdien **Moms 19**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="f3ef3-112">[![Feltet Momskode på siden Bogført moms](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="f3ef3-113">Kontrollere finanskonteringsgruppen for momskoden</span><span class="sxs-lookup"><span data-stu-id="f3ef3-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="f3ef3-114">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="f3ef3-115">Find og vælg momskoden, og gennemse derefter værdien i feltet **Finanskonteringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="f3ef3-116">I dette eksempel er værdien **Moms**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="f3ef3-117">[![Feltet Finanskonteringsgruppe på siden Momskoder](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="f3ef3-118">Værdien i feltet **Finanskonteringsgruppe** er et link.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="f3ef3-119">Vælg linket for at få vist detaljerne om gruppens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="f3ef3-120">Du kan også vælge og holde (eller højreklikke) i feltet og derefter vælge **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="f3ef3-121">[![Kommandoen Vis detaljer](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="f3ef3-122">Kontrollér, at kontonummeret er korrekt i overensstemmelse med transaktionstypen i feltet **Skyldig moms**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="f3ef3-123">Hvis ikke, skal du vælge den rette konto til bogføringen.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="f3ef3-124">I dette eksempel skal momsen for salgsordren bogføres på kontoen for skyldig moms 222200.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="f3ef3-125">[![Feltet Skyldig moms på siden Finanskonteringsgrupper](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="f3ef3-126">Følgende tabel indeholder oplysninger om hvert felt på siden **Finanskonteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="f3ef3-127">Felt</span><span class="sxs-lookup"><span data-stu-id="f3ef3-127">Field</span></span>                  | <span data-ttu-id="f3ef3-128">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f3ef3-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="f3ef3-129">Moms, der skal betales</span><span class="sxs-lookup"><span data-stu-id="f3ef3-129">Sales tax payable</span></span>      | <span data-ttu-id="f3ef3-130">Hovedkontoen for udgående salgsmoms, der er skyldig til skattevæsenet.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="f3ef3-131">Moms, der skal modtages</span><span class="sxs-lookup"><span data-stu-id="f3ef3-131">Sales tax receivable</span></span>   | <span data-ttu-id="f3ef3-132">Hovedkontoen for indgående moms, der er modtaget fra skattevæsenet.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="f3ef3-133">Udgift for importmoms</span><span class="sxs-lookup"><span data-stu-id="f3ef3-133">Use tax expense</span></span>        | <span data-ttu-id="f3ef3-134">Den hovedkonto, der bruges til at bogføre fradragsberettiget brugsafgifter, som leverandører ikke indberetter til skattevæsenet som del af EU's modtagermoms for varer og tjenesteydelser (GST)/Harmonized Sales Tax (HST).</span><span class="sxs-lookup"><span data-stu-id="f3ef3-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="f3ef3-135">**Importmoms** skal være valgt for momskoden i den momsgruppe, der bruges i transaktionen.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="f3ef3-136">Dette felt er ikke tilgængeligt, hvis indstillingen **Anvend momsregler** er valgt på siden **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="f3ef3-137">Skyldig importmoms</span><span class="sxs-lookup"><span data-stu-id="f3ef3-137">Use tax payable</span></span>        | <span data-ttu-id="f3ef3-138">Den hovedkonto, der bruges til at bogføre indgående importmoms, som skal betales til skattevæsenet.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="f3ef3-139">Afregningskonto</span><span class="sxs-lookup"><span data-stu-id="f3ef3-139">Settlement account</span></span>     | <span data-ttu-id="f3ef3-140">Den hovedkonto, der bruges til at bogføre nettosaldoen for de finanskonti, der er angivet i felterne **Skyldig importmoms** og **Indgående moms**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="f3ef3-141">Kreditor kasserabat</span><span class="sxs-lookup"><span data-stu-id="f3ef3-141">Vendor cash discount</span></span>   | <span data-ttu-id="f3ef3-142">Den hovedkonto, der bruges til at bogføre en kasserabat for de momskoder, der er tilknyttet denne finanskonteringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="f3ef3-143">Debitor, kasserabat</span><span class="sxs-lookup"><span data-stu-id="f3ef3-143">Customer case discount</span></span> | <span data-ttu-id="f3ef3-144">Den hovedkonto, der bruges til at bogføre en kasserabat for de momskoder, der er tilknyttet denne finanskonteringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="f3ef3-145">Du kan finde flere oplysninger i [Opsætning af finanskonteringsgrupper til moms](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="f3ef3-146">Løse fejl i kode for at kontrollere finansdimensioner</span><span class="sxs-lookup"><span data-stu-id="f3ef3-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="f3ef3-147">I koden bestemmes bogføringskontoen af finansdimensionen.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="f3ef3-148">Finansdimensionen gemmer post-id'et for en konto i databasen.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="f3ef3-149">I forbindelse med en salgsordre skal du tilføje et pausepunkt ved metoderne **Moms::saveAndPost()** og **Moms::post()**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="f3ef3-150">Vær opmærksom på værdien af **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="f3ef3-151">[![Eksempel på en salgsordrekode med et pausepunkt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="f3ef3-152">For en indkøbsordre skal du tilføje et pausepunkt ved metoderne **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="f3ef3-153">Vær opmærksom på værdien af **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="f3ef3-154">[![Eksempel på en indkøbsordrekode med et pausepunkt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="f3ef3-155">Kør følgende SQL-forespørgsel for at finde frem til visningsværdien for kontoen i databasen baseret på det post-id, der er gemt af finansdimensionen.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="f3ef3-156">[![Visningsværdi for post-id'et](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="f3ef3-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="f3ef3-157">Undersøg kaldstakken for at finde den værdi for **_ledgerDimension**, der er tildelt.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="f3ef3-158">Normalt hentes værdien fra **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="f3ef3-159">I dette tilfælde skal du tilføje et pausepunkt ved **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** for at finde den tildelte værdi.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="f3ef3-160">Afgøre, om der findes tilpasninger</span><span class="sxs-lookup"><span data-stu-id="f3ef3-160">Determine whether customization exists</span></span>

<span data-ttu-id="f3ef3-161">Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="f3ef3-162">Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="f3ef3-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
