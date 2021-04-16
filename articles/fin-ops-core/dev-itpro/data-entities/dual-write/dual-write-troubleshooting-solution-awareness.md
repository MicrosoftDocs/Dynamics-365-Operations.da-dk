---
title: Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748867"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="0ef9d-103">Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed</span><span class="sxs-lookup"><span data-stu-id="0ef9d-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0ef9d-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0ef9d-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ef9d-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0ef9d-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="0ef9d-108">Fejl på siden Dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="0ef9d-108">Error on the Dual-write page</span></span>

<span data-ttu-id="0ef9d-109">På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="0ef9d-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="0ef9d-110">*Enheden med navnet 'msdyn\_dualwriteentitymap' med namemapping='Logical' blev ikke fundet i MetadataCache*.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="0ef9d-111">Hvis du vil løse problemet, skal du sørge for, at Dobbeltskrivning-kerneløsningen er installeret i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="0ef9d-112">Dobbeltskrivning-kerneløsningen er en forudsætning for løsningsbevidsthed.</span><span class="sxs-lookup"><span data-stu-id="0ef9d-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]