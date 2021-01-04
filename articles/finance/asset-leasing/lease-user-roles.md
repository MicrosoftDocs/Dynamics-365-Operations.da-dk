---
title: Tildele leasingbrugerroller
description: I dette emne beskrives de sikkerhedsroller, der bruges til aktivleasing. Det forklarer også, hvordan du kan tildele brugere til disse roller.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441768"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="06020-104">Tildele leasingbrugerroller</span><span class="sxs-lookup"><span data-stu-id="06020-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06020-105">I dette emne beskrives de sikkerhedsroller, der bruges til aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="06020-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="06020-106">Det forklarer også, hvordan du kan tildele brugere til disse roller.</span><span class="sxs-lookup"><span data-stu-id="06020-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="06020-107">Tre brugerroller skelner adgang til aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="06020-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="06020-108">En rolle er velegnet til vedligeholdelse af leasingaftaler, en er velegnet til visning af leasingaftaler, en er relevant for udførelsen af en leasingassistentsopgaver.</span><span class="sxs-lookup"><span data-stu-id="06020-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="06020-109">Hver rolle har specifikke rettigheder til alle leasingsider, og de enkelte giver brugerne mulighed for at få vist, oprette, redigere eller slette rettigheder i henhold til deres arbejdsopgaver.</span><span class="sxs-lookup"><span data-stu-id="06020-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="06020-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="06020-110">Role</span></span>           | <span data-ttu-id="06020-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="06020-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="06020-112">Vedligehold leasingaftale</span><span class="sxs-lookup"><span data-stu-id="06020-112">Maintain Lease</span></span> | <span data-ttu-id="06020-113">Brugere i denne rolle kan tilføje, redigere, slette og få vist leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="06020-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="06020-114">Denne rolle er udviklet til daglige brugere, hvis opgaver omfatter oprettelse og bogføring af månedlige kladdeposter og tilføjelse af nye leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="06020-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="06020-115">Denne rolle giver adgang til alle aktivleasingfunktioner.</span><span class="sxs-lookup"><span data-stu-id="06020-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="06020-116">Vis leasingaftale</span><span class="sxs-lookup"><span data-stu-id="06020-116">View Lease</span></span>     | <span data-ttu-id="06020-117">Brugere i denne rolle kan kun få vist leasingposter, tidsplaner og køre rapporter.</span><span class="sxs-lookup"><span data-stu-id="06020-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="06020-118">De kan ikke oprette nye leasingaftaler, redigere eksisterende leasingaftaler eller oprette kladdeposteringer ud fra leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="06020-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="06020-119">Rollen er beregnet til brugere, der blot skal have vist leasingaftaler, leasingplaner og de transaktioner, der finder sted i forhold til disse leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="06020-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="06020-120">Leasingassistent</span><span class="sxs-lookup"><span data-stu-id="06020-120">Lease Clerk</span></span>    | <span data-ttu-id="06020-121">Brugere i denne rolle kan kun oprette nye leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="06020-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="06020-122">De kan hverken redigere eller slette eksisterende leasingaftaler, få vist leasing planer eller bogføre leasingkladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="06020-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="06020-123">Denne rolle er beregnet til brugere, der arbejder i en dataindtastningskapacitet.</span><span class="sxs-lookup"><span data-stu-id="06020-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="06020-124">Udfør følgende trin for at tildele brugere til de roller, der bruges i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="06020-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="06020-125">Gå til **Systemadministration \> Sikkerhed \> Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="06020-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="06020-126">Vælg rollen **Vedligehold leasingaftale**, **Leasingassistent** eller **Vis leasingaftale**, og vælg derefter **Tildel/Udeluk manuelt**.</span><span class="sxs-lookup"><span data-stu-id="06020-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="06020-127">Vælg den bruger, der skal tildeles til rollen, og vælg derefter **Tildel til rolle**.</span><span class="sxs-lookup"><span data-stu-id="06020-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
