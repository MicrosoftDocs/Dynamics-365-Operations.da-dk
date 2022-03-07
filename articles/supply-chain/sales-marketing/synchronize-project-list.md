---
title: Synkronisere projektliste fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 12708b35be87baf1ad13296b56507f3246f96394
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010866"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Synkronisere projektliste fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

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

[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)
