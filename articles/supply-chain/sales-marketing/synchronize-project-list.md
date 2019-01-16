---
title: Synkronisere projektliste fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synkronisere projektliste fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Navnet på skabelonen i dataintegration:**
- Projekter (Finance and Operations til Field Service)

**Navne på opgaverne i dataintegrationsprojektet:**
- Projekter

Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:
- Konti (Sales til Finance and Operations) 

## <a name="entity-set"></a>Enhedssæt
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekter                |

## <a name="entity-flow"></a>Enhedsflow
Projekter oprettes i Finance and Operations. Projekter med **Projekttype** Tid og materialer og **Projektstadie** Under behandling bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti. Listen **Eksternt projekt** bruges til at parre Field Service-serviceordrer med Finance and Operations-projekter.
CRM-løsningen til Field Service Eksternt projekt er en ny enhed, der får alle projekterne fra Operations.
Feltet Eksternt projekt er føjet til enheden Arbejdsordre. Dette er et find og køb-felt, som mærker arbejdsordren til et projekt. Salgsordren bliver derefter forbundet med et projekt i Operations. Når systemstatus skifter Åben - i gang (690,970,000) til en højere status, låses feltet Eksternt projekt, og du kan ikke tilføje, fjerne eller ændre værdien.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning
### <a name="in-finance-and-operations"></a>I Finance and Operations
Gøre det muligt at spore ændringer for Dataenhed-projekter

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekter (Finance and Operations til Field Service): Projekter

[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)

