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
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory-brugere, der blev ikke fundet i personvælgeren

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Udsted

Visse gyldige brugere i Microsoft Azure Active Directory (Azure AD) for lejeren vises ikke, når du søger efter navnet i personvælgeren i programmerne Dynamics 365 for Talent Attract og Onboard.

## <a name="cause"></a>Årsag

Visse brugertyper understøttes ikke i øjeblikket i Attract- og Onboard-programmerne. Kontroller, at brugeren ikke en Azure AD Business to Business (B2B)-gæstebruger. "Brugertype"-oplysninger findes i Azure Active Directory bladet i Azure-portalen.

Du kan finde flere oplysninger om Azure B2B i [Hvad er gæstebrugeradgang til Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

For ikke-B2B-brugere kan der være bestemte brugere, som ikke har en fuldstændig "Brugertype"-egenskab i objektet **Bruger**. Dette kan kontrolleres og rettes ved hjælp af Azure AD Powershell-modulet. Yderligere oplysninger finder du i [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Løsning

Hvis du vil løse problemet ved hjælp af følgende trin, skal du have "Global Administrator"-rettigheder i Azure Active Directory-lejeren eller rettigheder til **User.ReadWrite.All**.

Sådan kontrollerer du "Brugertype" for den pågældende bruger:

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Kommandoen returnerer følgende oplysninger:
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Bemærk **UserType**-egenskaben for brugeren. Hvis **UserType** er tom, for eksempel ikke "Medlem" eller "Gæst", skal du opdatere **UserType** ved hjælp af følgende kommando.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
