---
title: Angive adgangsrettigheder for controllere til omkostningsobjekt
description: Dette emne indeholder oplysninger om adgangsrettigheder for controllere til omkostningsobjekter.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 290b16eeb99ac7ddb9b552b289215c99a0451660
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "355535"
---
# <a name="access-rights-of-a-cost-object-controller"></a>Adgangsrettigheder for en controller til et omkostningsobjekt

[!include [banner](../includes/banner.md)]

Arbejdsområdet **Omkostningsstyring** er et centralt punkt, hvor ledere kan få vist performance for deres omkostningsobjekter. I dette arbejdsområde kan ledere bruge omkostningsregnskabsdata, selvom de ikke er bogholdere. Ledere skal af sikkerhedsmæssige årsager kun have adgang til at se de omkostningsregnskabsdata, der er relateret til de specifikke omkostningsobjekter, som de er ansvarlige for.

Der er fire entydige roller i omkostningsregnskab.

| Rollenavn               | Licens      |
|-------------------------|--------------|
| Vedligehold regnskabschef for omkostning | Aktivitet     |
| Lagerbogholder         | Operations   |
| Lagerregnskabsassistent   | Operations   |
| Controller til omkostningsobjekt  | Teammedlemmer |

Dette emne forklarer, hvordan du tildeler rollen **Controller til omkostningsobjekt** til en leder.

Når rollen **Controller til omkostningsobjekt** tildeles til en leder, kan lederen udføre følgende opgaver:

- Få adgang til **Omkostningsstyring**-arbejdsområdet (i klienten).

    - Få detaljeadgang og adgang til at se de sider, der understøtter detaljeadgangsoplevelsen.

- Få adgang til **Omkostningsstyring**-arbejdsområdet (i mobilprogrammet).

> [!NOTE]
> Rollen **Controller til omkostningsobjekt** styrer ikke, hvilke omkostningsobjekter brugeren har adgang til og kan få vist data for. Sikkerheden på rækkeniveau leveres via dimensionshierarkier og adgangslistehierarkiet.

## <a name="grant-access-rights"></a>Tildele adgangsrettigheder
Følgende eksempel viser, hvordan et dimensionshierarki kan se ud.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension    | Navn på dimensionshierarkitype      | Adgangslistehierarki |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Bærere | Klassifikationshierarki for dimension | **Ja**               |

Du kan bruge oversigtspanelet **Brugere** i hierarkidesigneren til at indsætte et eller flere bruger-id'er på hver node.

|                                   | Brugere            | Intervaller for dimensionsmedlemmer   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Noder**                         | **Bruger-id**      | **Fra dimensionsmedlem** | **Til dimensionsmedlem** |
| Organisation                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administration                 | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Emballage | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Bogholdere skal tildeles til det øverste niveau i hierarkiet, så de kan se alle poster i omkostningsregnskabet.

Før adgangslistehierarkiet og de tilhørende sikkerhedsindstillinger kan anvendes, skal indstillingen **Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt** være indstillet til **Ja** under fanen **Generelt** på siden **Parametre for omkostningsregnskab** (**Omkostningsregnskab** > **Opsætning** > **Parametre**).

Indstillingerne for adgangslistehierarkiet bruges til at styre, hvilke data der vises i følgende områder:

- Arbejdsområdet **Omkostningsstyring** (i klienten):

    - Data på de sider, der bruges til detaljeadgang

- Arbejdsområdet **Omkostningsstyring** (i mobilprogrammet):

    - Saldi i kort

- Microsoft Power BI:

    - Data, der vises i Power BI-visualiseringer
    - Power BI-datavisualiseringer, der er integreret i Microsoft Dynamics 365 for Finance and Operations-klienten

> [!IMPORTANT]
> - Før adgangslistehierarkiet kan påvirke dataene i Power BI, skal adgangslistehierarki og sikkerhed på rækkeniveau i Power BI kombineres. Du kan finde flere oplysninger i [Konfigurere sikkerhed for indholdspakke til omkostningsregnskab](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - I dette emne beskrives de forudsætninger, der skal være opfyldt, før du kan bruge arbejdsområdet **Omkostningsstyring**.

Yderligere ressourcer

- [Arbejdsområde for omkostningsstyring](cost-control-workspace.md)
- [Dimensionshierarki](dimension-hierarchy.md)
- [Konfigurere sikkerhed for indholdspakke til omkostningsregnskab](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
