---
title: Oprette straksafskrivning
description: Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176945"
---
# <a name="set-up-bonus-depreciation"></a>Oprette straksafskrivning

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

