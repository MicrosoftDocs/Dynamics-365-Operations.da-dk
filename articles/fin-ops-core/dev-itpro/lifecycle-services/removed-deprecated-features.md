---
title: Fjernede eller udfasede funktioner i Lifecycle Services (LCS)
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive udfaset fra Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abf7a1a0a75ac3098efeeab3df65481999b69acc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687872"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="91a31-103">Fjernede eller udfasede funktioner i Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="91a31-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="91a31-104">I dette emne beskrives funktioner, der er blevet fjernet eller udfases for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="91a31-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="91a31-105">En *fjernet* funktion er ikke længere tilgængelige i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="91a31-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="91a31-106">En *udfaset* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="91a31-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="91a31-107">Denne liste er stillet tilrådighed, så du kan tage disse fjernelser og udfasninger med i din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="91a31-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="91a31-108">Meddelelser for oktober 2019</span><span class="sxs-lookup"><span data-stu-id="91a31-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="91a31-109">Rutediagrammer i forretningsmodeldesigneren</span><span class="sxs-lookup"><span data-stu-id="91a31-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="91a31-110"><strong>Årsagen til forældelsen/fjernelsen</strong></span><span class="sxs-lookup"><span data-stu-id="91a31-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="91a31-111">Vi fraråder komponenten rutediagram i forretningsmodeldesigneren (BPM), fordi det forældre design forårsagede lavt forbrug.</span><span class="sxs-lookup"><span data-stu-id="91a31-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91a31-112"><strong>Erstattet af en anden funktion?</strong></span><span class="sxs-lookup"><span data-stu-id="91a31-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="91a31-113">Nr.</span><span class="sxs-lookup"><span data-stu-id="91a31-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91a31-114"><strong>Påvirkede områder</strong></span><span class="sxs-lookup"><span data-stu-id="91a31-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="91a31-115">Forretningsmodeldesigner</span><span class="sxs-lookup"><span data-stu-id="91a31-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91a31-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="91a31-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="91a31-117">Udfaset: Komponenten rutediagram i BPM forventes fjernet i 2020.</span><span class="sxs-lookup"><span data-stu-id="91a31-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="91a31-118">Følgende funktion vil ikke være tilgængelig:</span><span class="sxs-lookup"><span data-stu-id="91a31-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="91a31-119">Alle rutediagrammer er skrivebeskyttede og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="91a31-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="91a31-120">De figuregenskaber, der er knyttet til rutediagramaktiviteter, vil også være tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="91a31-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="91a31-121">Disse rutediagrammer omfatter både standardrutediagrammer, der genereres automatisk, og tilpassede rutediagrammer, der er ændret på grundlag af disse standardrutediagrammer.</span><span class="sxs-lookup"><span data-stu-id="91a31-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="91a31-122">Procestrin er skrivebeskyttede og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="91a31-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="91a31-123">Funktionen legacy fit/Gab-analyse vil ikke være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="91a31-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="91a31-124">Derfor vil der ikke automatisk blive oprettet en gab-liste, og den kan heller ikke eksporteres.</span><span class="sxs-lookup"><span data-stu-id="91a31-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="91a31-125"><strong>Bemærk:</strong> Denne funktion er tidligere blevet udfaset og erstattet af Microsoft Azure DevOps-integrationer.</span><span class="sxs-lookup"><span data-stu-id="91a31-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="91a31-126">Versionsoversigten for rutediagrammet vil ikke være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="91a31-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
