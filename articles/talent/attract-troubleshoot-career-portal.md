---
title: Attract-brugere kan ikke anvende job fra karriereportal
description: Dette emne forklarer, hvordan du lokaliserer fejl, når Attract-brugere ikke kan ansøge om job fra karriereportalen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460652"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-brugere kan ikke anvende job fra karriereportal

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Udsted

Attract-brugere kan ikke anvende job fra karriereportalen. Når de forsøger at ansøge om et job, der er oprettet i Dynamics 365 Talent: Attract, indlæser browseren hele siden og fuldfører ikke handlingen.

## <a name="cause"></a>Årsag

Dette problem opstår, når talentrelationsteamet ikke har brugerrollen Talent.

## <a name="resolution"></a>Løsning

Tildel Talent-brugerrollen til talentrelationsteamet.

1. Log på [Power Platform Administration](https://admin.powerplatform.microsoft.com) med en af følgende administratorlegitimationsoplysninger:

   - Dynamics 365 Administration
   - Global administrator
   - Power Platform Administration

2. Vælg **Miljøer** i navigationsruden, og vælg derefter det miljø, som brugerrollen Talent skal tildeles til talentrelationsteamet i.

   ![Vælg miljø](./media/attract-troubleshoot-career-portal-select-environment.png)

3. I ruden **Miljøer** skal du vælge **URL-adressen til miljøet** og logge på miljøets administrationsportal (f.eks. https:<orgname>.crm.dynamics.com).

4. Vælg **Indstillinger**, vælg **System**, og vælg derefter **Sikkerhed**.

   ![Naviger til Sikkerhed](./media/attract-troubleshoot-career-portal-security.png)

5. Vælg **Teams**.

   ![Vælg Teams.](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Søg efter **Talentrelationsteam** i søgefeltet, og vælg derefter teamet i søgeresultaterne.

7. Vælg **Administrer roller** på båndet.

8. Vælg **Talent-bruger** på listen over tilgængelige roller i dialogboksen **Administrer teamroller**, og vælg derefter **OK** for at anvende rollen.

   ![Anvend rolle](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Test dine ændringer:

   1. Log på karriereportalen fra et nyt browservindue.
   2. Ansøg om jobbet fra karriereportalen. 