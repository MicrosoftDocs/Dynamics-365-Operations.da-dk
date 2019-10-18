---
title: Aktiver forsinket momsberegning på kladde
description: I dette emne forklares det, hvordan du kan bruge funktionen **Aktiver forsinket momsberegning på kladde** til at forbedre ydeevnen for momsberegningen, når antallet af kladdelinjer er stort.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176936"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="1ec37-103">Aktiver forsinket momsberegning på kladde</span><span class="sxs-lookup"><span data-stu-id="1ec37-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1ec37-104">I dette emne forklares det, hvordan du kan bruge funktionen **Aktiver forsinket momsberegning på kladde** til at forbedre ydeevnen for momsberegningen, når antallet af kladdelinjer er stort.</span><span class="sxs-lookup"><span data-stu-id="1ec37-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="1ec37-105">Den aktuelle beregningsmåde for moms i kladden udløses i realtid, når brugeren opdaterer momsrelaterede felter, f.eks. momsgruppe/varemomsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1ec37-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="1ec37-106">Hvis der opdateres på kladdelinjeniveau, beregnes momsbeløbet igen på alle kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="1ec37-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="1ec37-107">Det hjælper brugeren med at få vist beregnet momsbeløb i realtid, men det kan også give problemer med ydeevnen, hvis antallet af kladdelinjer er stort.</span><span class="sxs-lookup"><span data-stu-id="1ec37-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="1ec37-108">Denne funktion giver mulighed for at udsætte momsberegningen for at løse problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="1ec37-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="1ec37-109">Hvis denne funktion er slået til, vil momsbeløbet kun blive beregnet, når brugeren klikker på "Moms" eller bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="1ec37-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="1ec37-110">Brugeren kan slå parameteren til og fra på tre niveauer:</span><span class="sxs-lookup"><span data-stu-id="1ec37-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="1ec37-111">af juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="1ec37-111">By legal entity</span></span>
- <span data-ttu-id="1ec37-112">efter kladdenavn</span><span class="sxs-lookup"><span data-stu-id="1ec37-112">By journal name</span></span>
- <span data-ttu-id="1ec37-113">efter kladdehoved</span><span class="sxs-lookup"><span data-stu-id="1ec37-113">By journal header</span></span>

<span data-ttu-id="1ec37-114">Systemet vil tage parameterværdien i kladdehovedet som endelig.</span><span class="sxs-lookup"><span data-stu-id="1ec37-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="1ec37-115">Parameterværdien til kladdeoverskriften bruges som standard fra kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="1ec37-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="1ec37-116">Parameterværdien på kladdenavnet angives som standard fra finanskladdeparameteren, når kladdenavnet oprettes.</span><span class="sxs-lookup"><span data-stu-id="1ec37-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="1ec37-117">Felterne "Faktisk momsbeløb" og "Beregnet momsbeløb" i kladden vil blive skjult, hvis denne parameter er slået til.</span><span class="sxs-lookup"><span data-stu-id="1ec37-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="1ec37-118">Formålet er ikke at forvirre brugeren, fordi værdien af disse to felter altid vil vise 0, før brugeren udløser momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="1ec37-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="1ec37-119">Aktivér udsat beregning af moms efter juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="1ec37-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="1ec37-120">Gå til **Finans > Opsætning Finans > Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="1ec37-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="1ec37-121">Klik på fanen **Moms**</span><span class="sxs-lookup"><span data-stu-id="1ec37-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="1ec37-122">Under fanen **Generelt** kan du finde parameteren **Forsinket momsberegning**, slå den til/fra</span><span class="sxs-lookup"><span data-stu-id="1ec37-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="1ec37-123">Aktiver forsinket momsberegning efter kladdenavn</span><span class="sxs-lookup"><span data-stu-id="1ec37-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="1ec37-124">Gå til **Finans > Kladdeopsætning > Kladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="1ec37-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="1ec37-125">Under fanen **Generelt** kan du finde parameteren **Forsinket momsberegning**, slå den til/fra</span><span class="sxs-lookup"><span data-stu-id="1ec37-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="1ec37-126">Aktiver forsinket momsberegning efter kladde</span><span class="sxs-lookup"><span data-stu-id="1ec37-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="1ec37-127">Gå til **Finans > Kladdeposteringer > Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="1ec37-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="1ec37-128">Klik på **Ny**</span><span class="sxs-lookup"><span data-stu-id="1ec37-128">Click **New**</span></span>
3. <span data-ttu-id="1ec37-129">Vælg et kladdenavn</span><span class="sxs-lookup"><span data-stu-id="1ec37-129">Select a journal name</span></span>
4. <span data-ttu-id="1ec37-130">Klik på **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="1ec37-130">Click **Setup**</span></span>
5. <span data-ttu-id="1ec37-131">Find parameteren **Forsinket momsberegning**, slå den til/fra</span><span class="sxs-lookup"><span data-stu-id="1ec37-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
