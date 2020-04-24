---
title: Bekræftelse af batch og nummerplade
description: I dette emne beskrives, hvordan du kan konfigurere og anvende batch- og id-bekræftelse fra en mobilenhed.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020d33bfb7e23df7898414f5becf96d31307f2fa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201312"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="b817f-103">Bekræftelse af batch og nummerplade</span><span class="sxs-lookup"><span data-stu-id="b817f-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b817f-104">Med batchbekræftelse kan du bekræfte, at den korrekte batch plukkes fra mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="b817f-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="b817f-105">Ved det oprindelige pluk af arbejde for varer af typen batch over alene, hvor batch over angiver, at batch rangerer højere end sted i søgehierarkiet, skal du kontrollere, svarer det batch, der plukkes, svarer til batchen på arbejdslinjen.</span><span class="sxs-lookup"><span data-stu-id="b817f-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="b817f-106">Med id-bekræftelse kan du bekræfte, at det korrekte id plukkes fra mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="b817f-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="b817f-107">Ved pluk af arbejde fra et sted i et stadie, skal du kontrollere, at det id, der plukkes, svarer til det id, der er knyttet til arbejdet.</span><span class="sxs-lookup"><span data-stu-id="b817f-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="b817f-108">Hvis arbejdet startes ved at scanne et id, springes dette bekræftelsestrin over.</span><span class="sxs-lookup"><span data-stu-id="b817f-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="b817f-109">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="b817f-109">Where it applies</span></span>
<span data-ttu-id="b817f-110">Bekræftelsen anvendes i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="b817f-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="b817f-111">Batchbekræftelse gælder for de første pluk af arbejde for varer af typen batch over.</span><span class="sxs-lookup"><span data-stu-id="b817f-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="b817f-112">Bekræftelse af id gælder for pluk fra steder i stadier.</span><span class="sxs-lookup"><span data-stu-id="b817f-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="b817f-113">Konfigurere bekræftelse af batch og id</span><span class="sxs-lookup"><span data-stu-id="b817f-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="b817f-114">Du kan konfigurere batch- og id-bekræftelse fra mobilenhedens menupunkter.</span><span class="sxs-lookup"><span data-stu-id="b817f-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="b817f-115">Angiv opsætningen af arbejdsbekræftelsen fra menupunkterne på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="b817f-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="b817f-116">Vælg indstillingen for batch- eller id-bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="b817f-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="b817f-117">Begge indstillinger er tilgængelige for pluk af arbejdstypen, hvor automatisk bekræftelse ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b817f-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
