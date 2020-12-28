---
title: Brugeren kan få adgang til Personale, men ikke Onboard eller Attract
description: I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 Talent - Personale, men ikke til Attract eller Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460669"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Brugeren kan få adgang til Personale, men ikke Onboard eller Attract

[!include [banner](includes/banner.md)]

**Miljøoplysninger**

- Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.
- Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 Human Resources.

**Udsted**

Bruger B kan få adgang til Personale, men ikke til appen Talent: Attract eller Talent: Onboard. Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.

**Løsning**

Bruger B skal tildeles rettigheder til at få vist Microsoft Power Apps-miljøet, som bruger A oprettede under klargøringsprocessen.

Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langsigtet løsning**

Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Personale.
