---
title: Det er ikke muligt at oprette et miljø i PowerApps Administration
description: I dette emne beskrives, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft PowerApps Administration.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "857240"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="7a965-103">Kan ikke oprette et miljø i PowerApps Administration</span><span class="sxs-lookup"><span data-stu-id="7a965-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a965-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="7a965-104">**Issue**</span></span>

- <span data-ttu-id="7a965-105">Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft PowerApps Administration.</span><span class="sxs-lookup"><span data-stu-id="7a965-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="7a965-106">Der er ikke blevet tildelt en licens, der giver brugerne ret til at udføre miljøoprettelsestrinnet, direkte til den bruger, der udfører dette trin.</span><span class="sxs-lookup"><span data-stu-id="7a965-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="7a965-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="7a965-107">**Solution**</span></span>

<span data-ttu-id="7a965-108">Kontrollér, at lejeradministratoren har tildelt en gyldig licens til PowerApps P2 direkte til den bruger, der skal udføre miljøoprettelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="7a965-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="7a965-109">Her er de Microsoft Dynamics-serviceplaner, der indeholder denne rettighed.</span><span class="sxs-lookup"><span data-stu-id="7a965-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="7a965-110">Overordnet produktlagerenhed (SKU)</span><span class="sxs-lookup"><span data-stu-id="7a965-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="7a965-111">PowerApps P2 serviceplan</span><span class="sxs-lookup"><span data-stu-id="7a965-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7a965-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7a965-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7a965-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7a965-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="7a965-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7a965-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7a965-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7a965-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="7a965-116">Bemærk, at forskellige Microsoft Office SKU'er også giver rettigheden sammen med enkeltstående PowerApps Plan 2 SKU'er.</span><span class="sxs-lookup"><span data-stu-id="7a965-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="7a965-117">Det vigtigste er, at der findes en af disse SKU'er.</span><span class="sxs-lookup"><span data-stu-id="7a965-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7a965-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7a965-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7a965-119">Opret miljøerne ved at følge vejledningen i [Klargøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7a965-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
