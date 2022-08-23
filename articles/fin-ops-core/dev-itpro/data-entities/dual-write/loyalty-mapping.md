---
title: Kundefordelskundekort og -belønningspoint
description: Denne artikel beskriver integrationen af data om fordelskundekort og belønningspoint i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 399682b3042c32fbf6fa200213f1b4982ed97174
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289108"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kundefordelskundekort og -belønningspoint

[!include [banner](../../includes/banner.md)]



Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre. Dynamics 365 Commerce har f.eks. infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser. Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres med Dataverse, kan disse data bruges af Customer Engagement-apps. Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.

## <a name="templates"></a>Skabeloner

Finans og drift-apps | Kundeengagementapps     | Betegnelse
|-----------------------------|-----------------------------------|-------------|
[Fordelskundekort](mapping-reference.md#149) | msdyn_loyaltycards | Denne skabelon synkroniserer oplysninger om fordelskundekort. |
[Loyalitetsniveauer](mapping-reference.md#226) | msdyn_loyaltylevels | Denne skabelon synkroniserer oplysninger om kunders belønningspoint. |
[Fordelskundebelønningspoint](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
