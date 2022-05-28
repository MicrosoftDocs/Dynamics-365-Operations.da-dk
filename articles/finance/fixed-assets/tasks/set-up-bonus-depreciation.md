---
title: Oprette straksafskrivning
description: Denne procedure viser, hvordan du opretter en særlig afskrivning og knytter den til et anlægskartotek.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bc768e6b470f8f49b23bf7ce0c8e5a080043281
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725871"
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
