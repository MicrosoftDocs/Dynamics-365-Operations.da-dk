---
title: Angive parametre for kildeskat i Kreditor og Debitor
description: Dette emne beskriver, hvordan du angiver parametre i Kreditor og Debitor, som understøtter fradrag af kildeskat (TDS – Tax Deducted at Source).
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023118"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="26b88-103">Angive parametre for kildeskat i Kreditor og Debitor</span><span class="sxs-lookup"><span data-stu-id="26b88-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26b88-104">Dette emne beskriver, hvordan du angiver parametre i Kreditor og Debitor, som understøtter fradrag af kildeskat (TDS – Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="26b88-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="26b88-105">Gå til **Skat \> Opsætning \> Parametre \> Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="26b88-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="26b88-106">Vælg **Opdater ordrelinjer** under fanen **Opdateringer** for at åbne dialogboksen **Opdater ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="26b88-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="26b88-107">I feltet **Opdatering af kildeskattegruppe** i sektionen **Kildeskattegruppe** skal du angive den metode, du vil bruge til at opdatere kildeskattegruppen på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="26b88-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="26b88-108">Denne indstilling bruges, når kildeskattegruppen opdateres i et ordrehoved.</span><span class="sxs-lookup"><span data-stu-id="26b88-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="26b88-109">Der findes følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="26b88-109">The following options are available:</span></span>

    - <span data-ttu-id="26b88-110">**Aldrig** – Kildeskattegruppen opdateres ikke på ordrelinjerne, når den opdateres i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="26b88-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="26b88-111">**Altid** – Kildeskattegruppen opdateres automatisk på ordrelinjerne, når den opdateres i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="26b88-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="26b88-112">**Spørg** – Brugerne modtager en meddelelse, hvor de bliver spurgt, om de vil opdatere kildeskattegruppen på ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="26b88-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="26b88-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="26b88-113">Select **OK**.</span></span>

    <span data-ttu-id="26b88-114">[![Dialogboksen Opdater ordrelinjer](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="26b88-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="26b88-115">Gå til **Skat \> Opsætning \> Parametre \> Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="26b88-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="26b88-116">Under fanen **Generelt** skal du i oversigtspanelet **Opdeling baseret på leveringsoplysninger** skal du angive indstillingen **Produktkvittering** til **Ja** for at bogføre og opdele en produktkvittering, der har forskellige leveringsadresser og skattekontonumre (TAN – Tax Account Number).</span><span class="sxs-lookup"><span data-stu-id="26b88-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="26b88-117">Hvis denne indstilling er angivet til **Nej**, kan du ikke bogføre et indkøbs følgeseddel, som har forskellige leveringsadresser og skattekontonumre.</span><span class="sxs-lookup"><span data-stu-id="26b88-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="26b88-118">Angiv indstillingen **Faktura** til **Ja** for at bogføre og opdele en indkøbsfaktura, der har forskellige leveringsadresser og skattekontonumre.</span><span class="sxs-lookup"><span data-stu-id="26b88-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="26b88-119">[![Oversigtspanelet Opdeling baseret på leveringsoplysninger](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="26b88-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="26b88-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26b88-120">Close the page.</span></span>
