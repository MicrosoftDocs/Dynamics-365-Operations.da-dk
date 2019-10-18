---
title: Brugeren kan få adgang til Core HR, men ikke Onboard eller Attract
description: I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 Talent - Core HR, men ikke til Attract eller Onboard.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009300"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Brugeren kan få adgang til Core HR, men ikke Onboard eller Attract

[!include [banner](includes/banner.md)]

**Miljøoplysninger**

- Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.
- Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 Talent: Core HR.

**Udsted**

Bruger B kan få adgang til Core HR, men ikke til Talent: Attract or Talent: Onboard-app. Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.

**Løsning**

Bruger B skal tildeles rettigheder til at få vist Microsoft PowerApps-miljøet, som bruger A oprettede under klargøringsprocessen.

Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langsigtet løsning**

Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Core HR.
