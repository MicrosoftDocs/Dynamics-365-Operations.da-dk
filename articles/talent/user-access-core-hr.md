---
title: Brugeren kan få adgang til Core HR, men ikke Onboard- eller Attract-appen
description: I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 for Talent Core HR, men ikke til Attract- eller Onboard-appen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "855650"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="14138-103">Brugeren kan få adgang til Core HR, men ikke Onboard- eller Attract-appen</span><span class="sxs-lookup"><span data-stu-id="14138-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14138-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="14138-104">**Environment details**</span></span>

- <span data-ttu-id="14138-105">Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.</span><span class="sxs-lookup"><span data-stu-id="14138-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="14138-106">Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="14138-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="14138-107">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="14138-107">**Issue**</span></span>

<span data-ttu-id="14138-108">Bruger B kan få adgang til Core HR, men ikke til Talent: Attract or Talent: Onboard-app.</span><span class="sxs-lookup"><span data-stu-id="14138-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="14138-109">Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="14138-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="14138-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="14138-110">**Solution**</span></span>

<span data-ttu-id="14138-111">Bruger B skal tildeles rettigheder til at få vist Microsoft PowerApps-miljøet, som bruger A oprettede under klargøringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="14138-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="14138-112">Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="14138-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="14138-113">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="14138-113">**Long-term solution**</span></span>

<span data-ttu-id="14138-114">Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Core HR.</span><span class="sxs-lookup"><span data-stu-id="14138-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
