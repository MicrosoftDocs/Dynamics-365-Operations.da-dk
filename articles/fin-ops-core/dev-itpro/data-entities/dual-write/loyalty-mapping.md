---
title: Fordelskundekort og belønningspoint
description: I dette emne beskrives integrationen af data om fordelskundekort og belønningspoint i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747981"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kundefordelskundekort og -belønningspoint

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre. Dynamics 365 Commerce har f.eks. infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser. Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres med Dataverse, kan disse data bruges af Customer Engagement-apps. Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.

## <a name="templates"></a>Skabeloner

| Finance and Operations-apps | Modelstyrede apps i Dynamics 365 | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
| Fordelskundekort                | msdyn\_loyaltycards               | Denne skabelon synkroniserer oplysninger om fordelskundekort. |
| Fordelskundebelønningspoint       | msdyn\_loyaltyrewardpoints        | Denne skabelon synkroniserer oplysninger om kunders belønningspoint. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]