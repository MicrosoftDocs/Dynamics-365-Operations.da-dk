---
title: Konfigurere A-skattekoder for TDS-skattetypen
description: Dette emne forklarer, hvordan du opretter koder for afgifter fratrukket ved kilden (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023130"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="c6202-103">Konfigurere A-skattekoder for TDS-skattetypen</span><span class="sxs-lookup"><span data-stu-id="c6202-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6202-104">Dette emne forklarer, hvordan du opretter koder for afgifter fratrukket ved kilden (TDS).</span><span class="sxs-lookup"><span data-stu-id="c6202-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="c6202-105">Gå til **Moms \> Indirekte skatter \> A-skat \> Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="c6202-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="c6202-106">[![Siden Koder for indeholdt skat](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="c6202-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="c6202-107">Vælg **Ny** i handlingsruden for at oprette en kode for A-skat til TDS, og angiv de nødvendige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c6202-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="c6202-108">I feltet **Skattetype** i oversigtspanelet **Generelt** skal du vælge **TDS** for at kategorisere afgiftskoden som en TDS-afgiftskode.</span><span class="sxs-lookup"><span data-stu-id="c6202-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="c6202-109">Vælg TDS-afregningsperioden for TDS-afgiftskoden i feltet **Afregningsperiode**.</span><span class="sxs-lookup"><span data-stu-id="c6202-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="c6202-110">Vælg den finanskonto, som TDS-beløbet skal bogføres på, i feltet **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="c6202-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="c6202-111">I feltet **Debitorkonto** skal du vælge den debitorkonto, som det TDS-beløb, der trækkes fra i salgstransaktionerne, skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="c6202-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="c6202-112">Feltet **Grundlag** indstilles automatisk til **Procent af bruttobeløb**, og værdien kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="c6202-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6202-113">Du kan ikke indstille grundlaget til **Procentdel af nettobeløb** for afgiftskoder af TDS-afgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="c6202-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="c6202-114">Vælg TDS-afgiftskomponenten for TDS-afgiftskoden i feltet **A-skat-komponent**.</span><span class="sxs-lookup"><span data-stu-id="c6202-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="c6202-115">Vælg **Værdier** i handlingsruden for at åbne siden **Værdier for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="c6202-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="c6202-116">Angiv startdatoen for TDS-værdien i feltet **Fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="c6202-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="c6202-117">Angiv slutdatoen i feltet **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="c6202-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6202-118">Felterne **Minimumsgrænse**, **Øvre grænse** og **Udelad %** er ikke tilgængelige for afgiftskoder af TDS-afgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="c6202-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="c6202-119">Angiv procentdel af TDS for TDS-afgiftskoden i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="c6202-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="c6202-120">Luk siden **Værdier for A-skat** for at vende tilbage til siden **Koder for indeholdt skat**.</span><span class="sxs-lookup"><span data-stu-id="c6202-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6202-121">Knappen **Grænser** på siden **Koder for indeholdt skat** er ikke tilgængelig for afgiftskoder af TDS-afgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="c6202-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="c6202-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c6202-122">Close the page.</span></span>
