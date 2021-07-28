---
title: Arbejdere uden ansættelse
description: Arbejdere uden fremtidig, aktiv eller historisk ansættelse i organisationen vises i formularen Arbejdere uden ansættelse.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71cb119e533e64b14badf65f55e8c4d5aa4c4b2f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356578"
---
# <a name="workers-without-employment"></a>Arbejdere uden ansættelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbejdere uden fremtidig, aktiv eller historisk ansættelse i organisationen vises i formularen **Arbejdere uden ansættelse**. Arbejdere med denne status kan vises, når du importerer arbejdere uden en ansættelsespost, eller når du sletter en arbejders ansættelse via **Arbejder > Ansættelseshistorik**.

Formularen **Arbejdere uden ansættelse** er som standard tilgængelig for følgende roller:

- Personaleassistent
- Personalechef
- Rekrutteringsmedarbejder
- Chef for kompensation og frynsegoder
- Lønadministrator
- Lønchef
- Uddannelseschef

På listen **Arbejdere uden ansættelse** kan du slette de anførte personer. Denne rettighed gives som standard til rollen Personaleassistent. Du kan tildele denne rettighed til andre roller med følgende fremgangsmåde:

1. Vælg **Systemadministration**, og klik derefter under fanen **Sikkerhedskonfiguration**.

2. Filtrer listen **Rettigheder** under fanen **Rettigheder** til **Vedligehold medarbejdere**.

   [![Filtrere listen Rettigheder.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Vælg **Vis menupunkter** i kolonnen **Referencer**.

4. Vælg **HcmWorkersWithoutEmployment** i **Vis menupunkter**.

   [![Vælg formular.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Angiv rettigheden **Slet** til **Tildel**.

6. Vælg fanen **Ikke-publicerede objekter**.

7. Vælg **Publicer alle**.

   [![Publicer ændringer.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]