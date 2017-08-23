--- 
title: Konfigurere adgangsrettigheder for en controller for omkostningsobjekt
description: Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: 9c5f79b7d9d62b29f21f2ddd1f6507ff82b381cc
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigurere adgangsrettigheder for en controller for omkostningsobjekt

[!include[task guide banner](../../includes/task-guide-banner.md)]

Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller. Denne registrering bruger USP2-demodatafirmaet.


## <a name="assign-the-cost-object-controller-role"></a>Tildele rollen Controller til omkostningsobjekt
1. Gå til Systemadministration > Brugere > Brugere.
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på værdien 'alicia' i feltet Brugernavn.
3. Klik op linket i den valgte række på listen.
4. Klik på Tildel roller.
5. Find og vælg den ønskede post på listen.
6. Klik på OK.

## <a name="enable-access-list-security"></a>Aktivere sikkerhed for adgangsliste
1. Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.
2. Find og vælg den ønskede post på listen.
    * Vælg organisation.  
3. Klik på Rediger.
4. Vælg Ja i feltet Adgangslistehierarki.
5. Klik på Vis hierarki.

## <a name="assign-access-rights-to-user"></a>Tildele adgangsrettigheder til bruger
1. Klik på Ny.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Bruger-id.
    * Vælg administrator.  
4. Vælg 'Organisation\Administrerende direktør\Administrerende direktør\FIM'.
5. Klik på Ny.
6. Markér den valgte række på listen.
7. Indtast eller vælg en værdi i feltet Bruger-id.
    * Vælg Alicia.  
8. Klik på Gem.

## <a name="enable-access-rights-in-cost-accounting"></a>Aktivere adgangsrettigheder i omkostningsregnskab
1. Gå til Omkostningsregnskab > Opsætning > Parametre.
2. Klik på fanen Generelt.
3. Vælg Ja i feltet Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt.
4. Klik på Gem.
5. Luk siden.
6. Gå til Omkostningsregnskab > Opsætning > Konfiguration af arbejdsområde for omkostningsstyring.
7. Klik på Rediger.
8. Vælg Ja i feltet Publiceret.
    * Hvis du vælger Ja, kan en bruger, der er tildelt en af følgende fire roller, se rapporterne i arbejdsområdet Omkostningsstyring: regnskabschef, bogholder, bogholderimedarbejder og omkostningsobjektcontroller. Hvis du vælger Nej, er det kun en bruger, der er tildelt en af følgende roller, der kan se rapporterne: regnskabschef, bogholder og bogholderimedarbejder.    
9. Klik på Gem.


