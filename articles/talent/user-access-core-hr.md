---
title: Brugeren kan få adgang til Core HR, men ikke Onboard eller Attract
description: I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 Talent - Core HR, men ikke til Attract eller Onboard.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772913"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="faa07-103">Brugeren kan få adgang til Core HR, men ikke Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="faa07-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="faa07-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="faa07-104">**Environment details**</span></span>

- <span data-ttu-id="faa07-105">Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.</span><span class="sxs-lookup"><span data-stu-id="faa07-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="faa07-106">Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="faa07-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="faa07-107">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="faa07-107">**Issue**</span></span>

<span data-ttu-id="faa07-108">Bruger B kan få adgang til Core HR, men ikke til Talent: Attract or Talent: Onboard-app.</span><span class="sxs-lookup"><span data-stu-id="faa07-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="faa07-109">Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="faa07-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="faa07-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="faa07-110">**Solution**</span></span>

<span data-ttu-id="faa07-111">Bruger B skal tildeles rettigheder til at få vist Microsoft Power Apps-miljøet, som bruger A oprettede under klargøringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="faa07-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="faa07-112">Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="faa07-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="faa07-113">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="faa07-113">**Long-term solution**</span></span>

<span data-ttu-id="faa07-114">Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Core HR.</span><span class="sxs-lookup"><span data-stu-id="faa07-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
