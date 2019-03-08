---
title: Synkronisere projektliste fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "312502"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synkronisere projektliste fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Skabelon i dataintegration**
- Projekter (Finance and Operations til Field Service)

**Opgave i dataintegrationsprojekt**
- Projekter

Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:
- Konti (Sales til Finance and Operations) 

## <a name="entity-set"></a>Enhedssæt
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekter                |

## <a name="entity-flow"></a>Enhedsflow
Projekter oprettes i Finance and Operations. Projekter med **Projekttype** indstillet til **Tid og materialer** og **Projektstadie** indstillet til **Under behandling** bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti. Listen **Eksternt projekt** bruges til at parre arbejdsordrer i Field Service med Finance and Operations-projekter.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Enheden **Eksternt projekt** får alle projekterne fra Finance and Operations. Feltet **Eksternt projekt** er føjet til enheden **Arbejdsordre**. Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Finance and Operations. Når **Systemstatus** ændrer **Åben - i gang (690,970,000)** til en højere status, låses feltet **Eksternt projekt**, og du kan ikke længere tilføje, fjerne eller ændre værdien.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning
### <a name="finance-and-operations"></a>Finance and Operations
Gør det muligt at spore ændringer for Dataenhed-projekter.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekter (Finance and Operations til Field Service): Projekter

[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)
