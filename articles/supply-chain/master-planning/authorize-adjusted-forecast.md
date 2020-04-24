---
title: Godkende en justeret prognose
description: Det er ikke alle prognosedata, der skal godkendes med det samme. I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for. Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e511aa8181b5d554f3392bdc5f0c299dc031ee4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203934"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="a3663-105">Godkende en justeret prognose</span><span class="sxs-lookup"><span data-stu-id="a3663-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3663-106">Det er ikke alle prognosedata, der skal godkendes med det samme.</span><span class="sxs-lookup"><span data-stu-id="a3663-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="a3663-107">I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for.</span><span class="sxs-lookup"><span data-stu-id="a3663-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="a3663-108">Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller.</span><span class="sxs-lookup"><span data-stu-id="a3663-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="a3663-109">Det er ikke alle prognosedata, der skal godkendes med det samme.</span><span class="sxs-lookup"><span data-stu-id="a3663-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="a3663-110">Du kan angive start- og slutdatoerne for den periode, som prognosen er godkendt for.</span><span class="sxs-lookup"><span data-stu-id="a3663-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="a3663-111">Denne funktion gør det muligt at fryse bestemte filsæt.</span><span class="sxs-lookup"><span data-stu-id="a3663-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="a3663-112">De start- og slutdatoer, du angiver, skal svare til start- og slutdatoerne for det filsæt, som budgettet oprettes i.</span><span class="sxs-lookup"><span data-stu-id="a3663-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="a3663-113">Systemet opretholder denne begrænsning og justerer automatisk datoer, hvis regulering er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="a3663-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="a3663-114">Under fanen **Detaljer** på siden **Godkendelse** kan du få vist detaljer om den prognose, der blev oprettet for nylig.</span><span class="sxs-lookup"><span data-stu-id="a3663-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="a3663-115">Du kan vælge firmaerne og de prognosemodeller for at godkende den prognose, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="a3663-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="a3663-116">Dette gitter omfatter som standard alle de firmaer, som behovsprognosen er oprettet for.</span><span class="sxs-lookup"><span data-stu-id="a3663-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="a3663-117">For hver virksomhed bliver den prognosemodel, der svarer til den aktuelle prognoseplan, der er konfigureret i parametre for varedisponering, udfyldt på forhånd.</span><span class="sxs-lookup"><span data-stu-id="a3663-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="a3663-118">Du kan dog ændre denne prognosemodel til en prognosemodel, der hører til det pågældende firma.</span><span class="sxs-lookup"><span data-stu-id="a3663-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="a3663-119">Hvis der er genereret nogen behovsprognosedata for et valgt firma, modtager du en advarsel under import.</span><span class="sxs-lookup"><span data-stu-id="a3663-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="a3663-120">Det er meget vigtigt, at du forstår, hvordan afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget** fungerer.</span><span class="sxs-lookup"><span data-stu-id="a3663-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="a3663-121">Hvis du har foretaget manuelle justeringer i den statistiske budgetgrundlag, godkendes de justerede værdier til brug, også selvom dette afkrydsningsfelt er markeret.</span><span class="sxs-lookup"><span data-stu-id="a3663-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="a3663-122">Disse ændringerne kasseres dog efter godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="a3663-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="a3663-123">Næste gang der oprettes en prognose, er prognosen er derfor kun en statistisk prognose og har ingen manuelle tilsidesættelser, også selvom **Overfør manuelle justeringer til behovsprognosen** er markeret.</span><span class="sxs-lookup"><span data-stu-id="a3663-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="a3663-124">Derfor kan du overveje afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget**, der er en mekanisme, der gør det muligt at bevare eller slette alle manuelle ændringer.</span><span class="sxs-lookup"><span data-stu-id="a3663-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a3663-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a3663-125">Additional resources</span></span>
--------

[<span data-ttu-id="a3663-126">Foretage manuelle justeringer af prognosegrundlaget</span><span class="sxs-lookup"><span data-stu-id="a3663-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="a3663-127">Overvåge prognosenøjagtighed</span><span class="sxs-lookup"><span data-stu-id="a3663-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



