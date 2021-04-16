---
title: Samlet nummerserie for job-id'er
description: Denne funktion indeholder en enkelt samlet nummerserie, der genererer job-id'er til modulerne Produktionsstyring, Produktionsudførelse og Tid og fremmøde.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824935"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="fe020-103">Samlet nummerserie for job-id'er</span><span class="sxs-lookup"><span data-stu-id="fe020-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe020-104">Denne funktion indeholder en enkelt samlet nummerserie, der genererer job-id'er til modulerne Produktionsstyring, Produktionsudførelse og Tid og fremmøde.</span><span class="sxs-lookup"><span data-stu-id="fe020-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="fe020-105">Tidligere kunne du vælge en anden nummerserie til hver af disse moduler, hvilket kunne resultere i konflikter mellem job-id'er, hvis to eller flere af disse nummerserier brugte et identisk format.</span><span class="sxs-lookup"><span data-stu-id="fe020-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="fe020-106">En sådan konflikt kan bevirke, at data bliver beskadiget.</span><span class="sxs-lookup"><span data-stu-id="fe020-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="fe020-107">Aktivere denne funktion i dit system</span><span class="sxs-lookup"><span data-stu-id="fe020-107">Turn on this feature for your system</span></span>

<span data-ttu-id="fe020-108">Hvis systemet ikke allerede indeholder den funktion, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Samlet nummerserie for job-id'er*.</span><span class="sxs-lookup"><span data-stu-id="fe020-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="fe020-109">Konfigurere samlet nummerserie for job-id'er</span><span class="sxs-lookup"><span data-stu-id="fe020-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="fe020-110">Når denne funktion er aktiveret, bliver de eksisterende indstillinger for nummerserier til **Job-id**, der findes på parametersiderne for Produktionsstyring, Produktionsudførelse og Tid og fremmøde frarådet, og der vil blive tilføjet et nyt **Samlet job-id**-felt.</span><span class="sxs-lookup"><span data-stu-id="fe020-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="fe020-111">Værdien af **Samlet job-id** deles af alle tre moduler, hvilket sikrer, at alle moduler refererer til samme nummerserie.</span><span class="sxs-lookup"><span data-stu-id="fe020-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="fe020-112">Job-id'er vil derfor være entydige på tværs af alle tre moduler, og der vil aldrig forekomme en konflikt.</span><span class="sxs-lookup"><span data-stu-id="fe020-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="fe020-113">Sådan konfigurerer du en samlet nummerserie for job-id'er:</span><span class="sxs-lookup"><span data-stu-id="fe020-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="fe020-114">Aktivér funktionen som beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="fe020-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="fe020-115">Identificer enten den nummerserie, du vil bruge til dine samlede job-id'er, eller opret en ny.</span><span class="sxs-lookup"><span data-stu-id="fe020-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="fe020-116">Du kan finde flere oplysninger under [Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fe020-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="fe020-117">Gå til siden **Parametre for produktionsstyring**, **Parametre for produktionsudførelse** eller **Parametre for tid og fremmøde**.</span><span class="sxs-lookup"><span data-stu-id="fe020-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="fe020-118">Det betyder ikke noget, hvilken af dem du vælger, for når du foretager denne indstilling på en af disse sider, opdateres alle de andre sider automatisk.</span><span class="sxs-lookup"><span data-stu-id="fe020-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="fe020-119">Åbn fanen **Nummerserier** på den valgte parameterside.</span><span class="sxs-lookup"><span data-stu-id="fe020-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="fe020-120">Tildel den **Nummerseriekode**, som du tidligere har identificeret, til rækken **Samlede job-id'er** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="fe020-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
