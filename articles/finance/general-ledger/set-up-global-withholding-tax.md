---
title: Konfigurere global A-skat
description: Dette emne indeholder en oversigt over trinene til opsætning af global A-skat for køb og salg.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060715"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="7edd7-103">Konfigurere global A-skat</span><span class="sxs-lookup"><span data-stu-id="7edd7-103">Set up global withholding tax</span></span>

<span data-ttu-id="7edd7-104">Dette emne indeholder en oversigt over trinene til opsætning af global A-skat for køb og salg.</span><span class="sxs-lookup"><span data-stu-id="7edd7-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="7edd7-105">Opsætte A-skattemyndigheder på siden **A-skattemyndigheder**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="7edd7-106">Konfigurere afregningsperioder for A-skat på siden **Afregningsperioder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="7edd7-107">Opret en A-finanskonteringsgruppe på siden **A-skat > finanskonteringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="7edd7-108">Kontoen for **A-skat** tildeles en hovedkonto med bogføringstypen **A-skat**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="7edd7-109">Kontoen for **A-skatteforskydning** tildeles også en hovedkonto med bogføringstypen **A-skatteforskydning**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="7edd7-110">Gå til **Finans > Kontoplan > Konti > Hovedkonti**, konfigurer **Bogføringstype** i underformularen **Bogføringsvalidering** for hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="7edd7-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="7edd7-111">Konfigurere A-skattekoder på siden **A-skattekoder**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="7edd7-112">Konfigurere A-skattegrupper på siden **A-skattegrupper**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="7edd7-113">Konfigurer A-skatteindtægtstyper på siden **A-skatteindtægtstyper** på siden **typer**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="7edd7-114">Konfigurere A-skattegrupper på siden **A-skattegrupper for varer** for en vare eller service.</span><span class="sxs-lookup"><span data-stu-id="7edd7-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="7edd7-115">Konfigurer **Minimumfakturabeløb** på siden **Økonomiparametre > A-skat**.</span><span class="sxs-lookup"><span data-stu-id="7edd7-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
