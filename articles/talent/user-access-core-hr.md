---
title: Brugeren kan få adgang til Personale, men ikke Onboard eller Attract
description: I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 Talent - Personale, men ikke til Attract eller Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460669"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="49d29-103">Brugeren kan få adgang til Personale, men ikke Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="49d29-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49d29-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="49d29-104">**Environment details**</span></span>

- <span data-ttu-id="49d29-105">Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.</span><span class="sxs-lookup"><span data-stu-id="49d29-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="49d29-106">Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="49d29-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="49d29-107">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="49d29-107">**Issue**</span></span>

<span data-ttu-id="49d29-108">Bruger B kan få adgang til Personale, men ikke til appen Talent: Attract eller Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="49d29-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="49d29-109">Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="49d29-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="49d29-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="49d29-110">**Solution**</span></span>

<span data-ttu-id="49d29-111">Bruger B skal tildeles rettigheder til at få vist Microsoft Power Apps-miljøet, som bruger A oprettede under klargøringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="49d29-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="49d29-112">Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="49d29-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="49d29-113">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="49d29-113">**Long-term solution**</span></span>

<span data-ttu-id="49d29-114">Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Personale.</span><span class="sxs-lookup"><span data-stu-id="49d29-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
