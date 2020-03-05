---
title: Kan ikke oprette et miljø i Power Apps Administration
description: I denne artikel beskrives det, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft Power Apps Administration.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008454"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7bdad-103">Kan ikke oprette et miljø i Power Apps Administration</span><span class="sxs-lookup"><span data-stu-id="7bdad-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="7bdad-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="7bdad-104">**Issue**</span></span>

- <span data-ttu-id="7bdad-105">Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft Power Apps Administration.</span><span class="sxs-lookup"><span data-stu-id="7bdad-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7bdad-106">Der er ikke blevet tildelt en licens, der giver brugerne ret til at udføre miljøoprettelsestrinnet, direkte til den bruger, der udfører dette trin.</span><span class="sxs-lookup"><span data-stu-id="7bdad-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="7bdad-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="7bdad-107">**Solution**</span></span>

<span data-ttu-id="7bdad-108">Kontrollér, at lejeradministratoren har tildelt en gyldig licens til Power Apps P2 direkte til den bruger, der skal udføre miljøoprettelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="7bdad-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="7bdad-109">Her er de Microsoft Dynamics-serviceplaner, der indeholder denne rettighed.</span><span class="sxs-lookup"><span data-stu-id="7bdad-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="7bdad-110">Overordnet produktlagerenhed (SKU)</span><span class="sxs-lookup"><span data-stu-id="7bdad-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="7bdad-111">Serviceplan for Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="7bdad-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7bdad-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7bdad-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7bdad-113">Power Apps til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7bdad-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7bdad-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7bdad-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7bdad-115">Power Apps til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7bdad-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7bdad-116">Bemærk, at forskellige Microsoft Office-SKU'er også giver rettigheden sammen med enkeltstående Power Apps Plan 2-SKU'er.</span><span class="sxs-lookup"><span data-stu-id="7bdad-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7bdad-117">Det vigtigste er, at der findes en af disse SKU'er.</span><span class="sxs-lookup"><span data-stu-id="7bdad-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7bdad-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7bdad-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7bdad-119">Opret miljøerne ved at følge vejledningen i [Klargøre Personale](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7bdad-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>