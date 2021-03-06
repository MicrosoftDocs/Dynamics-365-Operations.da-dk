---
title: Oprette straksafskrivning
description: Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad1b7f584d2b2a63dba5f8519ada9d89d6265e7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815614"
---
# <a name="set-up-bonus-depreciation"></a>Oprette straksafskrivning

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]