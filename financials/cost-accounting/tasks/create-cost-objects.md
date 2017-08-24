--- 
title: Oprette omkostningsobjekter
description: "Denne procedure viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske Dynamics 365 for Finance and Operations, Enterprise edition-dimension af typen Bærer til omkostningsregnskabet via en dataconnector."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 79cb18717c6b42ef0307f304d28902dd66f0f932
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-objects"></a>Oprette omkostningsobjekter 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske Dynamics 365 for Finance and Operations, Enterprise edition-dimension af typen Bærer til omkostningsregnskabet via en dataconnector. Demofirmaet USMF bruges til at oprette denne procedure. Denne fremgangsmåde er til en Omkostningsregnskab-funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-new-cost-objects"></a>Opret nye omkostningsobjekter
1. Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Gem.

## <a name="configure-the-data-connector"></a>Konfigurer dataconnectoren
1. Klik på Konfigurer leverandør af dimensionsmedlem.
    * Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.  
2. Vælg Bærer i feltet Dimensionens navn.
3. Klik på OK.

## <a name="import-cost-centers"></a>Importér bærere
1. Klik på Importér dimensionsmedlemmer.
2. Klik på OK.

## <a name="view-the-imported-cost-centers"></a>Få vist de importerede bærere
1. Klik på Vis dimensionsmedlemmer.


