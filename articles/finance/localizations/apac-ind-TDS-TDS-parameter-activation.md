---
title: Angive parametre for kildeskat
description: Dette emne beskriver, hvordan du angiver parametre for at aktivere funktionen til kildeskat (TDS – Tax Deducted at Source) for angivne transaktioner. Det er et nødvendigt trin for at kunne bruge funktionen til kildeskat.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023116"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="26b40-104">Angive parametre for kildeskat</span><span class="sxs-lookup"><span data-stu-id="26b40-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26b40-105">Dette emne beskriver, hvordan du angiver parametre for at aktivere funktionen til kildeskat (TDS – Tax Deducted at Source) for angivne transaktioner.</span><span class="sxs-lookup"><span data-stu-id="26b40-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="26b40-106">Det er et nødvendigt trin for at kunne bruge funktionen til kildeskat.</span><span class="sxs-lookup"><span data-stu-id="26b40-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="26b40-107">Gå til **Finans \> Opsætning Finans \> Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="26b40-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="26b40-108">Under fanen **Direkte skatter** i sektionen **Kildeskat** skal du angive indstillingen **Aktivér kildeskat** til **Ja** for at aktivere funktionen til kildeskat samt de sider og felter, der hører under den.</span><span class="sxs-lookup"><span data-stu-id="26b40-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="26b40-109">Angiv indstillingen **Faktura** til **Ja** for at aktivere de felter, der bruges til at beregne og fratrække kildeskat på fakturaniveau.</span><span class="sxs-lookup"><span data-stu-id="26b40-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="26b40-110">Angiv indstillingen **Betaling** til **Ja** for at aktivere de felter, der bruges til at beregne og fratrække kildeskat på betalingsniveau.</span><span class="sxs-lookup"><span data-stu-id="26b40-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="26b40-111">[![Fanen Direkte skatter](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="26b40-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="26b40-112">Under fanen **Nummerserier** skal du finde den serie, hvor feltet **Reference** er angivet til **Betaling af A-skat**.</span><span class="sxs-lookup"><span data-stu-id="26b40-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="26b40-113">I feltet **Nummerseriekode** for serien skal du vælge nummerseriekoden.</span><span class="sxs-lookup"><span data-stu-id="26b40-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="26b40-114">Nummerseriekoden bruges til at generere bilagsnumre til den periodiske skatteudligningsproces.</span><span class="sxs-lookup"><span data-stu-id="26b40-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26b40-115">Du kan køre den periodiske skatteudligningsproces ved at gå til **Skat \> Angivelser \> A-skat \> Betaling af A-skat**.</span><span class="sxs-lookup"><span data-stu-id="26b40-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="26b40-116">[![Fanen Nummerserier](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="26b40-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="26b40-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26b40-117">Close the page.</span></span>
