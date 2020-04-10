---
title: Fordelskundekort og belønningspoint
description: I dette emne beskrives integrationen af data om fordelskundekort og belønningspoint mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172963"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Fordelskundekort og belønningspoint

[!include [banner](../../includes/banner.md)]



Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre. I Microsoft Dynamics 365-programpakken har Dynamics 365 Commerce infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser. Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres til Common Data Service, kan disse data bruges af modelbaserede apps i Dynamics 365. Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.

## <a name="templates"></a>Skabeloner

| Finance and Operations-apps | Modelstyrede apps i Dynamics 365 | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
| Fordelskundekort                | msdyn\_loyaltycards               | Denne skabelon synkroniserer oplysninger om fordelskundekort. |
| Fordelskundebelønningspoint       | msdyn\_loyaltyrewardpoints        | Denne skabelon synkroniserer oplysninger om kunders belønningspoint. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
