---
title: "Nyheder eller ændringer i Dynamics 365 for Talent Core HR (15. november 2018)"
description: "Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Nyheder eller ændringer i Dynamics 365 for Talent Core HR (15. november 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2045**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="other-changesfixes"></a>Andre ændringer/rettelser

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Det er ikke muligt at ændres medarbejderens aktuelle stilling til en fremtidig åben stilling

Der er foretaget en ændring, som giver mulighed for overførsler af stillinger, når stillingen først er tilgængelig på et senere tidspunkt. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Stillingen vises ikke, når du opretter en ny medarbejder

Der er foretaget en ændring for at vise alle ledige stillinger, der er tilgængelige for tildeling ved ansættelse af nye medarbejdere i Talent. Dette omfatter historiske stillinger, eller hvis stillingerne er dateret i fremtiden. Stillinger vises nu korrekt ud fra startdatoen for ansættelsen. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Fratrædelsesdatoen vises på grundlag af brugerindstillinger

Er der foretaget en ændring af listen over tidligere medarbejdere, som tager højde for eventuelle tidszoneforskydninger for medarbejderens foretrukne tidszone, når du får vist fratrædelsesdatoen.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Workflowopgaver, der er tildelt til mig-links viser ikke de korrekte oplysninger

Med denne ændring viser navigation til detaljerne i de enkelte arbejdselementer på listen de korrekte oplysninger for det valgte element. Dette problem opstod kun med avancerede sikkerhedsindstillinger.


## <a name="known-issue"></a>Kendt problem

- **Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet. 
- **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket. Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret. (Dette problem vil blive løst i den næste platformsopdatering).

