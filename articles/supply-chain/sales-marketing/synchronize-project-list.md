---
title: Synkronisere projektliste fra Supply Chain Management til Field Service
description: Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 71c0580953f01c2d29e99fa2928a0b4a3937d5c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899347"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Synkronisere projektliste fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere projekter fra Supply Chain Management til Field Service.

**Skabelon i dataintegration**
- Projekter (Supply Chain Management til Field Service)

**Opgave i dataintegrationsprojekt**
- Projekter

Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:
- Konti (Sales til Supply Chain Management) 

## <a name="entity-set"></a>Enhedssæt
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekter                |

## <a name="entity-flow"></a>Enhedsflow
Projekter oprettes i Supply Chain Management. Projekter med **Projekttype** indstillet til **Tid og materialer** og **Projektstadie** indstillet til **Under behandling** bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti. Listen **Eksternt projekt** bruges til at parre arbejdsordrer i Field Service med projekter i Supply Chain Management.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Enheden **Eksternt projekt** får alle projekterne fra Supply Chain Management. Feltet **Eksternt projekt** er føjet til enheden **Arbejdsordre**. Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Supply Chain Management. Når **Systemstatus** ændrer **Åben - i gang (690,970,000)** til en højere status, låses feltet **Eksternt projekt**, og du kan ikke længere tilføje, fjerne eller ændre værdien.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning
### <a name="supply-chain-management"></a>Supply Chain Management
Gør det muligt at spore ændringer for Dataenhed-projekter.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projekter (Supply Chain Management til Field Service): Projekter

[![Skabelontilknytning i dataintegration.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]