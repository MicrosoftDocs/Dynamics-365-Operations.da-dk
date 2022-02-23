---
title: Konfigurere adgangsrettigheder for en controller for omkostningsobjekt
description: Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88d6208e867bd322ddfc4e599856b1905fa8e19b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969372"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigurere adgangsrettigheder for en controller for omkostningsobjekt

[!include [banner](../../includes/banner.md)]

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

