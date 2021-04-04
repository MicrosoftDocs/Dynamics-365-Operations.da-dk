---
title: Fjernede eller udfasede funktioner i Lifecycle Services (LCS)
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive udfaset fra Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559079"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="3fe72-103">Fjernede eller udfasede funktioner i Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3fe72-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3fe72-104">I dette emne beskrives funktioner, der er blevet fjernet eller udfases for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3fe72-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="3fe72-105">En *fjernet* funktion er ikke længere tilgængelige i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="3fe72-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="3fe72-106">En *udfaset* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="3fe72-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="3fe72-107">Denne liste er stillet tilrådighed, så du kan tage disse fjernelser og udfasninger med i din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="3fe72-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="3fe72-108">Meddelelser for oktober 2019</span><span class="sxs-lookup"><span data-stu-id="3fe72-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="3fe72-109">Rutediagrammer i forretningsmodeldesigneren</span><span class="sxs-lookup"><span data-stu-id="3fe72-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="3fe72-110"><strong>Årsagen til forældelsen/fjernelsen</strong></span><span class="sxs-lookup"><span data-stu-id="3fe72-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="3fe72-111">Vi fraråder komponenten rutediagram i forretningsmodeldesigneren (BPM), fordi det forældre design forårsagede lavt forbrug.</span><span class="sxs-lookup"><span data-stu-id="3fe72-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3fe72-112"><strong>Erstattet af en anden funktion?</strong></span><span class="sxs-lookup"><span data-stu-id="3fe72-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="3fe72-113">Nr.</span><span class="sxs-lookup"><span data-stu-id="3fe72-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3fe72-114"><strong>Påvirkede områder</strong></span><span class="sxs-lookup"><span data-stu-id="3fe72-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="3fe72-115">Forretningsmodeldesigner</span><span class="sxs-lookup"><span data-stu-id="3fe72-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3fe72-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="3fe72-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="3fe72-117">Udfaset: Komponenten rutediagram i BPM forventes fjernet i 2020.</span><span class="sxs-lookup"><span data-stu-id="3fe72-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="3fe72-118">Følgende funktion vil ikke være tilgængelig:</span><span class="sxs-lookup"><span data-stu-id="3fe72-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="3fe72-119">Alle rutediagrammer er skrivebeskyttede og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="3fe72-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="3fe72-120">De figuregenskaber, der er knyttet til rutediagramaktiviteter, vil også være tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="3fe72-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="3fe72-121">Disse rutediagrammer omfatter både standardrutediagrammer, der genereres automatisk, og tilpassede rutediagrammer, der er ændret på grundlag af disse standardrutediagrammer.</span><span class="sxs-lookup"><span data-stu-id="3fe72-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="3fe72-122">Procestrin er skrivebeskyttede og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="3fe72-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="3fe72-123">Funktionen legacy fit/Gab-analyse vil ikke være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="3fe72-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="3fe72-124">Derfor vil der ikke automatisk blive oprettet en gab-liste, og den kan heller ikke eksporteres.</span><span class="sxs-lookup"><span data-stu-id="3fe72-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="3fe72-125"><strong>Bemærk:</strong> Denne funktion er tidligere blevet udfaset og erstattet af Microsoft Azure DevOps-integrationer.</span><span class="sxs-lookup"><span data-stu-id="3fe72-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="3fe72-126">Versionsoversigten for rutediagrammet vil ikke være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="3fe72-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]