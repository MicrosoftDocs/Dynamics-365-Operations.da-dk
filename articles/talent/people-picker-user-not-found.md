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
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832598"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>Brugeren blev ikke fundet i personvælgeren i Attract eller Onboard

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Udsted

Visse gyldige brugere i Microsoft Azure Active Directory (Azure AD) for lejeren vises ikke, når du søger efter navnet i personvælgeren i Dynamics 365 Talent: Attract eller Dynamics 365 Talent: Onboard.

## <a name="cause"></a>Årsag

Visse brugertyper understøttes ikke i øjeblikket i Attract og Onboard. Kontroller, at brugeren ikke en Azure AD Business to Business (B2B)-gæstebruger. "Brugertype"-oplysninger findes i Azure Active Directory bladet i Azure-portalen.

Du kan finde flere oplysninger om Azure B2B i [Hvad er gæstebrugeradgang til Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

For ikke-B2B-brugere kan der være bestemte brugere, som ikke har en fuldstændig "Brugertype"-egenskab i objektet **Bruger**. Dette kan kontrolleres og rettes ved hjælp af Azure AD Powershell-modulet. Yderligere oplysninger finder du i [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

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
