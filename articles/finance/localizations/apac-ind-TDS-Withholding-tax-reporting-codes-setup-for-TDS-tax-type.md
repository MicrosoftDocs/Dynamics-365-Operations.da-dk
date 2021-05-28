---
title: Konfigurere rapporteringskoder for A-skat for TDS-skattetypen
description: A-skatterapporteringskoder bruges til at generere Formular 26Q- og Formular 27Q-opgørelser til afgifter fratrukket ved kilden (TDS). Dette emne forklarer, hvordan du konfigurerer trin i rapporteringskoder for A-skat, så du kan konfigurere TDS-rapporteringskoder.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023128"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="37bd8-104">Konfigurere rapporteringskoder for A-skat for TDS-skattetypen</span><span class="sxs-lookup"><span data-stu-id="37bd8-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37bd8-105">A-skatterapporteringskoder bruges til at generere Formular 26Q- og Formular 27Q-opgørelser til afgifter fratrukket ved kilden (TDS).</span><span class="sxs-lookup"><span data-stu-id="37bd8-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="37bd8-106">Dette emne forklarer, hvordan du konfigurerer trin i rapporteringskoder for A-skat, så du kan konfigurere TDS-rapporteringskoder.</span><span class="sxs-lookup"><span data-stu-id="37bd8-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="37bd8-107">Gå til **Moms \> Opsætning \> A-skat \> A-skatterapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="37bd8-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="37bd8-108">[![Siden A-skatterapporteringskoder](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="37bd8-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="37bd8-109">Vælg **TDS** i feltet **Skattetype** for at definere A-skatterapporteringskode for TDS-skattetypen.</span><span class="sxs-lookup"><span data-stu-id="37bd8-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="37bd8-110">Vælg den TDS-komponent, du definerer rapporteringskoden for A-skat for, i feltet **A-skat-komponent**.</span><span class="sxs-lookup"><span data-stu-id="37bd8-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="37bd8-111">I feltet **A-skat-komponentgruppe** vises den TDS-komponentgruppe, der blev defineret for den TDS-komponent, som du definerer.</span><span class="sxs-lookup"><span data-stu-id="37bd8-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="37bd8-112">Feltet **Sektionskode** i oversigtspanelet **Generelt** viser den sektionskode, der er knyttet til TDS-komponentgruppen.</span><span class="sxs-lookup"><span data-stu-id="37bd8-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="37bd8-113">Vælg TDS-rapporteringskoden i feltet **Rapporteringskode** i oversigtspanelet **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="37bd8-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="37bd8-114">TDS</span><span class="sxs-lookup"><span data-stu-id="37bd8-114">TDS</span></span>
    - <span data-ttu-id="37bd8-115">TCS</span><span class="sxs-lookup"><span data-stu-id="37bd8-115">TCS</span></span>
    - <span data-ttu-id="37bd8-116">Tillæg</span><span class="sxs-lookup"><span data-stu-id="37bd8-116">Surcharge</span></span>
    - <span data-ttu-id="37bd8-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="37bd8-117">PE\_Cess</span></span>
    - <span data-ttu-id="37bd8-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="37bd8-118">SHE\_Cess</span></span>

5. <span data-ttu-id="37bd8-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="37bd8-119">Close the page.</span></span>
