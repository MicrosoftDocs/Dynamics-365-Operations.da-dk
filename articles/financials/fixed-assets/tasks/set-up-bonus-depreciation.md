--- 
title: Oprette straksafskrivning
description: "Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7af954eaae76a327313a80cb3014d837267ccf4d
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-bonus-depreciation"></a>Oprette straksafskrivning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.


## <a name="create-a-special-depreciation-allowance"></a>Opret en særlig afskrivning
1. Gå til Anlægsaktiver > Opsætning > Særlig afskrivning.
2. Klik på Ny.
3. Skriv en værdi i feltet Særlig afskrivning.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Procent.
    * Hvis der ikke er angivet en procentdel, skal du angive et beløb.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Knyt en særlig afskrivning til en bog for anlægsaktivgruppe
1. Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.
2. Vælg på listen den anlægsaktivgruppe, der er tilknyttet den særlige afskrivning.
3. Klik på Bøger.
4. Vælg på listen den bog, der er tilknyttet den særlige afskrivning.
5. Klik på Særlig afskrivning.
6. Klik på Ny.
7. Skriv eller vælg en værdi i feltet Særlig afskrivning.
    * Procentdel eller Beløb hentes som standard fra konfigurationen af særlig afskrivning.  
8. Angiv et tal i feltet Prioritet.


