---
title: Nyheder eller ændringer i Dynamics 365 Talent (7. januar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460693"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="59649-103">Nyheder eller ændringer i Dynamics 365 Talent (7. januar 2020)</span><span class="sxs-lookup"><span data-stu-id="59649-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="59649-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="59649-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="59649-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="59649-105">Changes in Attract</span></span>

<span data-ttu-id="59649-106">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="59649-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="59649-107">Ændringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="59649-107">Changes in Onboard</span></span>

<span data-ttu-id="59649-108">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="59649-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="59649-109">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="59649-109">Changes in Core HR</span></span>

<span data-ttu-id="59649-110">Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="59649-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="59649-111">Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="59649-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="59649-112">Kan ikke slette arbejdere, der ikke har ansættelsesposter - (386157)</span><span class="sxs-lookup"><span data-stu-id="59649-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="59649-113">Denne ændring tilføjer en sletteindstilling i formen **Arbejdere uden ansættelse**.</span><span class="sxs-lookup"><span data-stu-id="59649-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="59649-114">Arbejdere vises i denne form, når der ikke findes fremtidige, aktive eller historiske ansættelser for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="59649-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="59649-115">I denne version er sletning kun aktiveret for systemadministratorer.</span><span class="sxs-lookup"><span data-stu-id="59649-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="59649-116">I næste uges udgivelse vil sikkerheden dog blive opdateret, så alle brugere med rollen som personaleassistent kan fjerne medarbejdere uden ansættelser.</span><span class="sxs-lookup"><span data-stu-id="59649-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="59649-117">Du kan også foretage disse ændringer manuelt ved at følge nedenstående trin.</span><span class="sxs-lookup"><span data-stu-id="59649-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="59649-118">Gå til **Sikkerhedskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="59649-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="59649-119">Filtrer listen **Rettigheder** under fanen **Rettigheder** til **Vedligehold medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="59649-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="59649-120">Vælg **Vis menupunkter** i kolonnen **Referencer**.</span><span class="sxs-lookup"><span data-stu-id="59649-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="59649-121">Vælg **HcmWOrkersWithoutEmployment** i **Vis menupunkter**.</span><span class="sxs-lookup"><span data-stu-id="59649-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="59649-122">Angiv rettigheden **Slet** til Tildel.</span><span class="sxs-lookup"><span data-stu-id="59649-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="59649-123">Vælg fanen **Ikke-publicerede objekter**.</span><span class="sxs-lookup"><span data-stu-id="59649-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="59649-124">Vælg **Publicer alle**.</span><span class="sxs-lookup"><span data-stu-id="59649-124">Select **Publish all**.</span></span>
