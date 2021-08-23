---
title: Fordelskundekort og belønningspoint
description: I dette emne beskrives integrationen af data om fordelskundekort og belønningspoint i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d20dca3e8f15d04b85bcdf102dda8794c68dc2d54acb65dbd0088da1e6c6cdc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765092"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kundefordelskundekort og -belønningspoint

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre. Dynamics 365 Commerce har f.eks. infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser. Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres med Dataverse, kan disse data bruges af Customer Engagement-apps. Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.

## <a name="templates"></a>Skabeloner

Finance and Operations-apps | Kundeengagementapps     | Betegnelse
|-----------------------------|-----------------------------------|-------------|
[Fordelskundekort](mapping-reference.md#149) | msdyn_loyaltycards | Denne skabelon synkroniserer oplysninger om fordelskundekort. |
[Loyalitetsniveauer](mapping-reference.md#226) | msdyn_loyaltylevels | Denne skabelon synkroniserer oplysninger om kunders belønningspoint. |
[Fordelskundebelønningspoint](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
