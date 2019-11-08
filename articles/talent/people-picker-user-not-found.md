---
title: Brugeren blev ikke fundet i personvælgeren i Attract eller Onboard
description: I dette emne beskrives, hvad du skal gøre, når brugere i firmaets lejer ikke vises i personvælgeren i Dynamics 365 Talent - Attract eller Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
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
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551927"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="64636-103">Brugeren blev ikke fundet i personvælgeren i Attract eller Onboard</span><span class="sxs-lookup"><span data-stu-id="64636-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="64636-104">Udsted</span><span class="sxs-lookup"><span data-stu-id="64636-104">Issue</span></span>

<span data-ttu-id="64636-105">Visse gyldige brugere i Microsoft Azure Active Directory (Azure AD) for lejeren vises ikke, når du søger efter navnet i personvælgeren i Dynamics 365 Talent: Attract eller Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="64636-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="64636-106">Årsag</span><span class="sxs-lookup"><span data-stu-id="64636-106">Cause</span></span>

<span data-ttu-id="64636-107">Visse brugertyper understøttes ikke i øjeblikket i Attract og Onboard.</span><span class="sxs-lookup"><span data-stu-id="64636-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="64636-108">Kontroller, at brugeren ikke en Azure AD Business to Business (B2B)-gæstebruger.</span><span class="sxs-lookup"><span data-stu-id="64636-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="64636-109">"Brugertype"-oplysninger findes i Azure Active Directory bladet i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="64636-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="64636-110">Du kan finde flere oplysninger om Azure B2B i [Hvad er gæstebrugeradgang til Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="64636-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="64636-111">For ikke-B2B-brugere kan der være bestemte brugere, som ikke har en fuldstændig "Brugertype"-egenskab i objektet **Bruger**.</span><span class="sxs-lookup"><span data-stu-id="64636-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="64636-112">Dette kan kontrolleres og rettes ved hjælp af Azure AD Powershell-modulet.</span><span class="sxs-lookup"><span data-stu-id="64636-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="64636-113">Yderligere oplysninger finder du i [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="64636-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="64636-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="64636-114">Resolution</span></span>

<span data-ttu-id="64636-115">Hvis du vil løse problemet ved hjælp af følgende trin, skal du have "Global Administrator"-rettigheder i Azure Active Directory-lejeren eller rettigheder til **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="64636-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="64636-116">Sådan kontrollerer du "Brugertype" for den pågældende bruger:</span><span class="sxs-lookup"><span data-stu-id="64636-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="64636-117">Kommandoen returnerer følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="64636-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="64636-118">Bemærk **UserType**-egenskaben for brugeren.</span><span class="sxs-lookup"><span data-stu-id="64636-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="64636-119">Hvis **UserType** er tom, for eksempel ikke "Medlem" eller "Gæst", skal du opdatere **UserType** ved hjælp af følgende kommando.</span><span class="sxs-lookup"><span data-stu-id="64636-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
