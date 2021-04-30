---
title: Kan ikke oprette et miljø i Power Apps Administration
description: I denne artikel beskrives det, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft Power Apps Administration.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892221"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="c3381-103">Kan ikke oprette et miljø i Power Apps Administration</span><span class="sxs-lookup"><span data-stu-id="c3381-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c3381-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="c3381-104">**Issue**</span></span>

- <span data-ttu-id="c3381-105">Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft Power Apps Administration.</span><span class="sxs-lookup"><span data-stu-id="c3381-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="c3381-106">Brugeren har ikke en licens, der giver ret til at oprette miljøer.</span><span class="sxs-lookup"><span data-stu-id="c3381-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="c3381-107">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="c3381-107">**Solution**</span></span>

<span data-ttu-id="c3381-108">Sørg for, at lejeradministratoren har tildelt en gyldig Power Apps P2-licens til den bruger, der opretter miljøet.</span><span class="sxs-lookup"><span data-stu-id="c3381-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="c3381-109">Følgende Microsoft Dynamics-serviceplaner indeholder rettigheder til at oprette miljøer:</span><span class="sxs-lookup"><span data-stu-id="c3381-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="c3381-110">Overordnet produktlagerenhed (SKU)</span><span class="sxs-lookup"><span data-stu-id="c3381-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="c3381-111">Serviceplan for Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="c3381-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="c3381-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="c3381-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="c3381-113">Power Apps til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c3381-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="c3381-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c3381-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="c3381-115">Power Apps til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c3381-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="c3381-116">Bemærk, at forskellige Microsoft Office-SKU'er også giver rettigheden sammen med enkeltstående Power Apps Plan 2-SKU'er.</span><span class="sxs-lookup"><span data-stu-id="c3381-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="c3381-117">Det vigtigste er, at der findes en af disse SKU'er.</span><span class="sxs-lookup"><span data-stu-id="c3381-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="c3381-118">Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="c3381-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c3381-119">Opret miljøerne ved at følge vejledningen i [Klargøre Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="c3381-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]