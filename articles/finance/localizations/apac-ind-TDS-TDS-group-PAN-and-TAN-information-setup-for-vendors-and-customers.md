---
title: Konfigurere kildeskattegruppe, permanent kontonummer og skattekontonummer for kreditorer og kunder
description: Dette emne beskriver, hvordan du angiver oplysninger om kildeskattegruppen (TDS – Tax Deducted at Source), det permanente kontonummer (PAN – Permanent Account Number) og skattekontonummeret (TAN – Tax Account Number) for kreditorer og kunder.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023119"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="221e5-103">Konfiguration af kildeskattegruppe, permanent kontonummer og skattekontonummer for kreditorer og kunder</span><span class="sxs-lookup"><span data-stu-id="221e5-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="221e5-104">Dette emne beskriver, hvordan du angiver oplysninger om kildeskattegruppen (TDS – Tax Deducted at Source), det permanente kontonummer (PAN – Permanent Account Number) og skattekontonummeret (TAN – Tax Account Number) for kreditorer og kunder.</span><span class="sxs-lookup"><span data-stu-id="221e5-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="221e5-105">Gå til **Kreditor \> Kreditorer \> Alle kreditorer** eller **Debitor \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="221e5-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="221e5-106">[![Siden Alle kreditorer](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="221e5-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="221e5-107">Vælg **Ny** i handlingsruden for at oprette en kreditor eller debitor, og angiv de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="221e5-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="221e5-108">Du kan også vælge en eksisterende kreditor eller debitor.</span><span class="sxs-lookup"><span data-stu-id="221e5-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="221e5-109">I sektionen **A-skat** i oversigtspanelet **Faktura og levering** skal du angive indstillingen **Beregn A-skat** til **Ja** for at beregne A-skat, kildeskat (TDS - Tax Deducted at Source) eller skat, der opkræves ved kilden (TCS – Tax Collected at Source) for kreditoren eller debitoren.</span><span class="sxs-lookup"><span data-stu-id="221e5-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="221e5-110">Kildeskat for en indkøbsfaktura beregnes på basis af den standardgruppe for kildeskat, der er defineret for kreditoren eller debitoren.</span><span class="sxs-lookup"><span data-stu-id="221e5-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="221e5-111">I feltet **Kildeskattegruppe** skal du vælge kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="221e5-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="221e5-112">Når du vælger et kildeskattegruppe i feltet **Kildeskattegruppe**, bliver felterne **Gruppe for A-skat** og **Gruppe for skatteopkrævning ved kilde** utilgængelige.</span><span class="sxs-lookup"><span data-stu-id="221e5-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="221e5-113">Vælg statussen for det permanente kontonummer (PAN) for kreditoren eller debitoren i feltet **Status** i sektionen **PAN-oplysninger** i oversigtspanelet **Skatteoplysninger**:</span><span class="sxs-lookup"><span data-stu-id="221e5-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="221e5-114">**Ikke tilgængelig** – Kreditoren eller debitoren har ikke et PAN.</span><span class="sxs-lookup"><span data-stu-id="221e5-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="221e5-115">**Modtaget** – Kreditoren eller debitoren har et PAN.</span><span class="sxs-lookup"><span data-stu-id="221e5-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="221e5-116">**Ansøgt** – Kreditoren eller debitoren har ansøgt om et PAN.</span><span class="sxs-lookup"><span data-stu-id="221e5-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="221e5-117">**Ugyldig** – Kreditoren eller debitoren har et PAN, men det er ikke gyldigt.</span><span class="sxs-lookup"><span data-stu-id="221e5-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="221e5-118">Hvis du har valgt **Modtaget** i feltet **Status** for at angive, at kreditoren eller debitoren har et PAN, skal du angive dette PAN i feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="221e5-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="221e5-119">Det permanente kontonummer (PAN) skal indeholde fem alfabetiske tegn, derefter fire numeriske tegn og derefter ét alfabetisk tegn.</span><span class="sxs-lookup"><span data-stu-id="221e5-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="221e5-120">Her er et eksempel: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="221e5-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="221e5-121">Hvis du har valgt **Ansøgt** i feltet **Status** for at angive, at kreditoren eller debitoren har ansøgt om et PAN, skal du angive referencenummeret i feltet **Referencenummer**.</span><span class="sxs-lookup"><span data-stu-id="221e5-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="221e5-122">I feltet **Art af vurdering** skal du vælge den vurderingskategori, som kreditoren eller debitoren tilhører:</span><span class="sxs-lookup"><span data-stu-id="221e5-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="221e5-123">Firma</span><span class="sxs-lookup"><span data-stu-id="221e5-123">Company</span></span>
    - <span data-ttu-id="221e5-124">HUF</span><span class="sxs-lookup"><span data-stu-id="221e5-124">HUF</span></span>
    - <span data-ttu-id="221e5-125">Autoriser</span><span class="sxs-lookup"><span data-stu-id="221e5-125">Firm</span></span>
    - <span data-ttu-id="221e5-126">Individuelt</span><span class="sxs-lookup"><span data-stu-id="221e5-126">Individual</span></span>
    - <span data-ttu-id="221e5-127">AOP</span><span class="sxs-lookup"><span data-stu-id="221e5-127">AOP</span></span>
    - <span data-ttu-id="221e5-128">BOI</span><span class="sxs-lookup"><span data-stu-id="221e5-128">BOI</span></span>
    - <span data-ttu-id="221e5-129">Lokal myndighed</span><span class="sxs-lookup"><span data-stu-id="221e5-129">Local authority</span></span>
    - <span data-ttu-id="221e5-130">Andre</span><span class="sxs-lookup"><span data-stu-id="221e5-130">Others</span></span>

    <span data-ttu-id="221e5-131">[![Oversigtspanelet Skatteoplysninger](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="221e5-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="221e5-132">I handlingsruden i gruppen **Registrering** under fanen **Kreditor** skal du vælge **Registrerings-id'er** for at åbne siden **Admistrer adresser**.</span><span class="sxs-lookup"><span data-stu-id="221e5-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="221e5-133">Vælg **Tilføj** eller **Rediger** på siden **Administrer adresser** i oversigtspanelet **Skatteoplysninger** for at åbne siden **Administrer skatteoplysninger**, hvor du kan opbevare skatteregistreringen.</span><span class="sxs-lookup"><span data-stu-id="221e5-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="221e5-134">I feltet **Skattekontonummer (TAN)** på siden **Administrer skatteoplysninger** i oversigtspanelet **A-skat** skal du skrive skattekontonummeret (TAN – Tax Account Number).</span><span class="sxs-lookup"><span data-stu-id="221e5-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="221e5-135">Skattekontonummeret skal indeholde fire alfabetiske tegn, derefter fem numeriske tegn og derefter ét alfabetisk tegn.</span><span class="sxs-lookup"><span data-stu-id="221e5-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="221e5-136">Her er et eksempel: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="221e5-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="221e5-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="221e5-137">Close the page.</span></span>
