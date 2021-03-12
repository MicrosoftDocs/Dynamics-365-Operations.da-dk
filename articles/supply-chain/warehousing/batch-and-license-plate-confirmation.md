---
title: Bekræftelse af batch og nummerplade
description: I dette emne beskrives, hvordan du kan konfigurere og anvende batch- og id-bekræftelse fra en mobilenhed.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97790b91d4de536b89b580c26ef1e37145f7d7c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977432"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="a1505-103">Bekræftelse af batch og nummerplade</span><span class="sxs-lookup"><span data-stu-id="a1505-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1505-104">Med batchbekræftelse kan du bekræfte, at den korrekte batch plukkes fra mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="a1505-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="a1505-105">Ved det oprindelige pluk af arbejde for varer af typen batch over alene, hvor batch over angiver, at batch rangerer højere end sted i søgehierarkiet, skal du kontrollere, svarer det batch, der plukkes, svarer til batchen på arbejdslinjen.</span><span class="sxs-lookup"><span data-stu-id="a1505-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="a1505-106">Med id-bekræftelse kan du bekræfte, at det korrekte id plukkes fra mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="a1505-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="a1505-107">Ved pluk af arbejde fra et sted i et stadie, skal du kontrollere, at det id, der plukkes, svarer til det id, der er knyttet til arbejdet.</span><span class="sxs-lookup"><span data-stu-id="a1505-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="a1505-108">Hvis arbejdet startes ved at scanne et id, springes dette bekræftelsestrin over.</span><span class="sxs-lookup"><span data-stu-id="a1505-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a1505-109">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="a1505-109">Where it applies</span></span>

<span data-ttu-id="a1505-110">Bekræftelsen anvendes i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="a1505-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="a1505-111">Batchbekræftelse gælder for de første pluk af arbejde for varer af typen batch over.</span><span class="sxs-lookup"><span data-stu-id="a1505-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="a1505-112">Bekræftelse af id gælder for pluk fra steder i stadier.</span><span class="sxs-lookup"><span data-stu-id="a1505-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1505-113">Genopfyldning understøttes ikke for bekræftelse af id.</span><span class="sxs-lookup"><span data-stu-id="a1505-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="a1505-114">Når der udføres genopfyldningsarbejde, oprettes der intet bekræftelsestrin for id.</span><span class="sxs-lookup"><span data-stu-id="a1505-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="a1505-115">Konfigurere bekræftelse af batch og id</span><span class="sxs-lookup"><span data-stu-id="a1505-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="a1505-116">Du kan konfigurere batch- og id-bekræftelse fra mobilenhedens menupunkter.</span><span class="sxs-lookup"><span data-stu-id="a1505-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="a1505-117">Angiv opsætningen af arbejdsbekræftelsen fra menupunkterne på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="a1505-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="a1505-118">Vælg indstillingen for batch- eller id-bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="a1505-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="a1505-119">Begge indstillinger er tilgængelige for pluk af arbejdstypen, hvor automatisk bekræftelse ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a1505-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
