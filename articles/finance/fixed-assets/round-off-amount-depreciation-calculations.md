---
title: Afrund beløb til afskrivningsberegninger
description: I denne artikel beskrives det Afrund afskrivning-felt, der findes på sider med opsætning af en bog.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf7cf68c98b14fb6c206c99673168153b32a449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830417"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="a3ddc-103">Afrund beløb til afskrivningsberegninger</span><span class="sxs-lookup"><span data-stu-id="a3ddc-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3ddc-104">I denne artikel beskrives det Afrund afskrivning-felt, der findes på sider med opsætning af en bog.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="a3ddc-105">Afrunding af afskrivningsbeløb angives for hver bog.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="a3ddc-106">Afrunding af afskrivningsbeløb bruges i anlægsaktivets afskrivningsprofil, der viser den fremtidige afskrivning og værdi af anlægsaktivet samt i afskrivningsforslagene.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="a3ddc-107">Angiv laveste afskrivningsbeløb, der er tilladt i denne bog.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="a3ddc-108">Afskrivningsbeløbet i den sidste afskrivningsperiode afrundes ikke, uanset den afrunding der er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="a3ddc-109">I slutningen af den sidste afskrivningsperiode skal værdien af anlægsaktivet være 0 (nul) eller scrapværdien, hvis der anvendes scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="a3ddc-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a3ddc-110">Example</span></span>

<span data-ttu-id="a3ddc-111">Afskrivning uden afrunding er beregnet til 2.444,44.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="a3ddc-112">Som følgende tabel viser afhænger det foreslåede beløb af, hvordan afrundingen konfigureres.</span><span class="sxs-lookup"><span data-stu-id="a3ddc-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="a3ddc-113">Afrundingsmetode</span><span class="sxs-lookup"><span data-stu-id="a3ddc-113">Rounding method</span></span> | <span data-ttu-id="a3ddc-114">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="a3ddc-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="a3ddc-115">Afrunding 0,1</span><span class="sxs-lookup"><span data-stu-id="a3ddc-115">Rounding 0.1</span></span>    | <span data-ttu-id="a3ddc-116">2.444,40</span><span class="sxs-lookup"><span data-stu-id="a3ddc-116">2,444.40</span></span>            |
| <span data-ttu-id="a3ddc-117">Afrunding 1,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-117">Rounding 1.00</span></span>   | <span data-ttu-id="a3ddc-118">2.444,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-118">2,444.00</span></span>            |
| <span data-ttu-id="a3ddc-119">Afrunding 10,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-119">Rounding 10.00</span></span>  | <span data-ttu-id="a3ddc-120">2.440,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-120">2,440.00</span></span>            |
| <span data-ttu-id="a3ddc-121">Afrunding 100,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-121">Rounding 100.00</span></span> | <span data-ttu-id="a3ddc-122">2.400,00</span><span class="sxs-lookup"><span data-stu-id="a3ddc-122">2,400.00</span></span>            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]