---
title: Funktion til opdeling af faktura
description: Dette emne beskriver, hvordan du opsætter og bruger funktionen til opdeling af fakturaer efter leveringsadresse og skattekontonummer (TAN – Tax Account Number).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023123"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="8a5b8-103">Funktion til opdeling af faktura</span><span class="sxs-lookup"><span data-stu-id="8a5b8-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a5b8-104">Dette emne beskriver, hvordan du opsætter og bruger funktionen til opdeling af fakturaer efter leveringsadresse og skattekontonummer (TAN – Tax Account Number).</span><span class="sxs-lookup"><span data-stu-id="8a5b8-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="8a5b8-105">På siden **Kreditorparametre** under fanen **Generelt** skal du markere afkrydsningsfeltet **Produktkvittering** eller **Faktura** for at bogføre og opdele en produktkvittering eller faktura, der har forskellige leveringsadresser og skattekontonumre på siden **Indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="8a5b8-106">Den bogførte faktura opdeles derefter efter leveringsadresse og skattekontonummer.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="8a5b8-107">På fanen **Samleopdatering** op oversigtspanelet **Deling basering på** i rækken **Leveringsoplysninger** skal du angive indstillingen **Bekræftelse**, **Plukliste**, **Følgeseddel** eller **Faktura** til **Ja** for at bogføre og opdele en bekræftelse, plukliste, følgeseddel eller faktura, når der er defineret forskellige leveringsadresser og skattekontonumre for forskellige fakturalinjer på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="8a5b8-108">Fakturaen opdeles først efter leveringsadresse og dernæst efter skattekontonummer.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="8a5b8-109">Hvis ingen indstillinger for **Leveringsoplysninger** er angivet til **Ja**, bogføres fakturaen som en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="8a5b8-110">Der foretages ingen opdeling af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="8a5b8-111">Hvis du vil opdele og bogføre en følgeseddel, hvor fakturalinjerne har forskellige leveringsadresser og skattekontonumre, skal du angive indstillingen **Følgeseddel** for **Leveringsoplysninger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="8a5b8-112">Hvis du vil opdele og bogføre en faktura, hvor fakturalinjerne har forskellige leveringsadresser og skattekontonumre, skal du angive indstillingen **Faktura** for **Leveringsoplysninger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="8a5b8-113">Hvis du vil bogføre en faktura, hvor fakturalinjerne har forskellige leveringsadresser men samme skattekontonummer, skal du angive indstillingen **Faktura** for **Leveringsoplysninger** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="8a5b8-114">Fakturaen opdeles efter leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="8a5b8-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8a5b8-115">Example</span></span>

<span data-ttu-id="8a5b8-116">I dette eksempel er indstillingen **Faktura** for **Leveringsoplysninger** angivet til **Ja** under fanen **Samleopdatering** på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="8a5b8-117">Der bogføres en indkøbsfaktura med følgende opsætning for leveringsadresser og skattekontonumre på linjerne:</span><span class="sxs-lookup"><span data-stu-id="8a5b8-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="8a5b8-118">**Varelinje 1:** Leveringsadresse 1, skattekontonummer-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="8a5b8-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="8a5b8-119">**Varelinje 2:** Leveringsadresse 1, skattekontonummer-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="8a5b8-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="8a5b8-120">**Varelinje 3:** Leveringsadresse 2, skattekontonummer-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="8a5b8-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="8a5b8-121">**Varelinje 4:** Leveringsadresse 3, skattekontonummer-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="8a5b8-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="8a5b8-122">I dette tilfælde opdeles den oprindelige faktura i to fakturaer og bogføres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="8a5b8-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="8a5b8-123">Faktura 1 bogføres for varelinje 1 og varelinje 2, fordi de to linjer har samme leveringsadresse og skattekontonummer.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="8a5b8-124">Faktura 2 bogføres for varelinje 3.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="8a5b8-125">Faktura 3 bogføres for varelinje 4.</span><span class="sxs-lookup"><span data-stu-id="8a5b8-125">Invoice 3 is posted for item line 4.</span></span>
