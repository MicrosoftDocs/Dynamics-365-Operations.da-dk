---
title: "Brugeren kan få adgang til Core HR, men ikke Onboard- eller Attract-appen"
description: "I dette emne beskrives, hvordan du kan løse problemet, når en bruger kan få adgang til Microsoft Dynamics 365 for Talent Core HR, men ikke til Attract- eller Onboard-appen."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Brugeren kan få adgang til Core HR, men ikke Onboard- eller Attract-appen

[!include [banner](includes/banner.md)]

**Miljøoplysninger**

- Microsoft Dynamics Lifecycle Services (LCS)-installationen blev udført af bruger A.
- Bruger A tilføjede bruger B som bruger af Microsoft Dynamics 365 for Talent Core HR.

**Afgang**

Bruger B kan få adgang til Core HR, men ikke til Talent: Attract or Talent: Onboard-app. Når brugeren forsøger at gå til **Oplevelsesapps**, kommer han eller hun i stedet til et prøvemiljø.

**Løsning**

Bruger B skal tildeles rettigheder til at få vist Microsoft PowerApps-miljøet, som bruger A oprettede under klargøringsprocessen.

Du kan finde oplysninger i afsnittet "Giver adgang til miljøet" i [Klargøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Langsigtet løsning**

Microsoft overvejer at tildele de relevante rettigheder til Onboard og Attract automatisk, når en bruger føjes til Core HR.

