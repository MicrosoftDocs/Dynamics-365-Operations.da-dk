---
title: Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172615"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="3e81c-103">Foretage fejlfinding af problemer i forbindelse med løsningsbevidsthed</span><span class="sxs-lookup"><span data-stu-id="3e81c-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3e81c-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e81c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3e81c-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer relateret til løsningsbevidsthed.</span><span class="sxs-lookup"><span data-stu-id="3e81c-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e81c-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="3e81c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3e81c-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="3e81c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="3e81c-108">Fejl på siden Dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="3e81c-108">Error on the Dual-write page</span></span>

<span data-ttu-id="3e81c-109">På siden **Dobbeltskrivning** kan du få vist en fejlmeddelelse, der ligner følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="3e81c-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="3e81c-110">*Enheden med navnet 'msdyn\_dualwriteentitymap' med namemapping='Logical' blev ikke fundet i MetadataCache*.</span><span class="sxs-lookup"><span data-stu-id="3e81c-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="3e81c-111">Hvis du vil løse problemet, skal du sørge for, at Dobbeltskrivning-kerneløsningen er installeret i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e81c-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="3e81c-112">Dobbeltskrivning-kerneløsningen er en forudsætning for løsningsbevidsthed.</span><span class="sxs-lookup"><span data-stu-id="3e81c-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
