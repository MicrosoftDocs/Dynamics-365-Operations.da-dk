---
title: Brugeren blev ikke fundet i personvælgeren i Attract eller Onboard
description: I dette emne beskrives, hvad du skal gøre, når brugere i firmaets lejer ikke vises i personvælgeren i programmerne Dynamics 365 for Talent Attract og Onboard.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303796"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="b64d7-103">Azure Active Directory-brugere, der blev ikke fundet i personvælgeren</span><span class="sxs-lookup"><span data-stu-id="b64d7-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="b64d7-104">Udsted</span><span class="sxs-lookup"><span data-stu-id="b64d7-104">Issue</span></span>

<span data-ttu-id="b64d7-105">Visse gyldige brugere i Microsoft Azure Active Directory (Azure AD) for lejeren vises ikke, når du søger efter navnet i personvælgeren i programmerne Dynamics 365 for Talent Attract og Onboard.</span><span class="sxs-lookup"><span data-stu-id="b64d7-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="b64d7-106">Årsag</span><span class="sxs-lookup"><span data-stu-id="b64d7-106">Cause</span></span>

<span data-ttu-id="b64d7-107">Visse brugertyper understøttes ikke i øjeblikket i Attract- og Onboard-programmerne.</span><span class="sxs-lookup"><span data-stu-id="b64d7-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="b64d7-108">Kontroller, at brugeren ikke en Azure AD Business to Business (B2B)-gæstebruger.</span><span class="sxs-lookup"><span data-stu-id="b64d7-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="b64d7-109">"Brugertype"-oplysninger findes i Azure Active Directory bladet i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="b64d7-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="b64d7-110">Du kan finde flere oplysninger om Azure B2B i [Hvad er gæstebrugeradgang til Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="b64d7-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="b64d7-111">For ikke-B2B-brugere kan der være bestemte brugere, som ikke har en fuldstændig "Brugertype"-egenskab i objektet **Bruger**.</span><span class="sxs-lookup"><span data-stu-id="b64d7-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="b64d7-112">Dette kan kontrolleres og rettes ved hjælp af Azure AD Powershell-modulet.</span><span class="sxs-lookup"><span data-stu-id="b64d7-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="b64d7-113">Yderligere oplysninger finder du i [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="b64d7-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="b64d7-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="b64d7-114">Resolution</span></span>

<span data-ttu-id="b64d7-115">Hvis du vil løse problemet ved hjælp af følgende trin, skal du have "Global Administrator"-rettigheder i Azure Active Directory-lejeren eller rettigheder til **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="b64d7-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="b64d7-116">Sådan kontrollerer du "Brugertype" for den pågældende bruger:</span><span class="sxs-lookup"><span data-stu-id="b64d7-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="b64d7-117">Kommandoen returnerer følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="b64d7-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="b64d7-118">Bemærk **UserType**-egenskaben for brugeren.</span><span class="sxs-lookup"><span data-stu-id="b64d7-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="b64d7-119">Hvis **UserType** er tom, for eksempel ikke "Medlem" eller "Gæst", skal du opdatere **UserType** ved hjælp af følgende kommando.</span><span class="sxs-lookup"><span data-stu-id="b64d7-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```