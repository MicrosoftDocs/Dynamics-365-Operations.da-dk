---
title: Konfigurere A-skat-myndigheder for TDS-skattetypen
description: Dette emne forklarer, hvordan du opretter TDS-skattemyndigheder for afgifter trukket ved kilden.
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023110"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="005ac-103">Konfigurere A-skat-myndigheder for TDS-skattetypen</span><span class="sxs-lookup"><span data-stu-id="005ac-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="005ac-104">Dette emne forklarer, hvordan du opretter TDS-skattemyndigheder for afgifter trukket ved kilden.</span><span class="sxs-lookup"><span data-stu-id="005ac-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="005ac-105">Gå til **Moms \> Indirekte skatter \> A-skattemyndigheder**.</span><span class="sxs-lookup"><span data-stu-id="005ac-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="005ac-106">[![Siden A-skattemyndigheder](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="005ac-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="005ac-107">Vælg **TDS** i feltet **Skattetype** for at konfigurere skattemyndigheder for TDS-skattetypen.</span><span class="sxs-lookup"><span data-stu-id="005ac-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="005ac-108">Vælg **Ny** i handlingsruden for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="005ac-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="005ac-109">Angiv et navn for TDS-myndigheden i feltet **A-skattemyndighed**.</span><span class="sxs-lookup"><span data-stu-id="005ac-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="005ac-110">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="005ac-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="005ac-111">Vælg kreditorkontoen for TDS-skattemyndigheden i feltet **Kreditorkonto** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="005ac-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="005ac-112">Du skal definere navnet på den bank, hvor penge, som skyldes til TDS-myndighedskreditoren, skal indbetales.</span><span class="sxs-lookup"><span data-stu-id="005ac-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="005ac-113">Bankens navn defineres på siden **Bankkonti** (**Kreditor \> Alle kreditorer \> Kreditor \> Konfigurerer \> Bankkonti**).</span><span class="sxs-lookup"><span data-stu-id="005ac-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="005ac-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="005ac-114">Close the page.</span></span>
