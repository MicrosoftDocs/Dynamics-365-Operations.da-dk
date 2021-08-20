---
title: Vedligehold rute for en produktmodel
description: Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 704a6b72c9eb8dc49ba9410ccd3689ba5ccfdd1f03e538b95ad174f6c1ee9796
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746130"
---
# <a name="maintain-route-for-a-product-model"></a>Vedligehold rute for en produktmodel

[!include [banner](../../includes/banner.md)]

Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration. Denne procedure bruger modellen Højttaler af topkvalitet i demofirmaet USMF til at føre dig gennem processen.

## <a name="add-a-route-operation"></a>Tilføj en ruteoperation

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Find og vælg den ønskede post på listen.
    * Vælg modellen Højttaler af topkvalitet til denne øvelse.  
1. Vælg linket i den valgte række på listen.
1. Udvid sektionen **Ruteoperationer**.
1. Vælg **Tilføj**.
1. Skriv en værdi i feltet **Navn**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg **Gem**.

## <a name="enter-route-operation-details"></a>Angiv oplysninger om ruteoperation

1. Vælg **Oplysninger om ruteoperation**.
1. Indtast eller vælg en værdi i feltet **Operation**.
1. I feltet **Oper.nr.** skal du angive et tal.
    * Operationsnumre bestemmer ruteforløbet.  
    * Hver egenskab for en ruteoperation kan få en statisk værdi eller kan knyttes til en attribut. Tilknytning til en attribut medfører, at værdien angives som en del af konfigurationen.  
1. Indtast eller vælg en værdi i feltet **Rutegruppe**.
    * Rutegruppen afgør den væsentlige funktionsmåde i forbindelse med efterkalkulation, forbrug og installation.  
1. Vælg fanen **Opsætning**.
1. Vælg fanen **Tider**.
1. Indtast et tal i feltet **Behandlingsantal**.
    * Bestem, hvor mange der vil blive behandlet under én handling.  
1. Indtast et tal i feltet **Timer/tid**.
    * Indtast tidsforholdet.  
1. Marker afkrydsningsfeltet **Indstil**.
1. Indtast et tal i feltet **Kørselstid**.
    * Bestemme behandlingstiden for den mængde, du har angivet.  
1. Vælg fanen **Ressourcebehov**.
1. Vælg **Tilføj**.
1. Markér den valgte række på listen.
1. Vælg en indstilling i feltet **Kravtype**.
    * Beslut, om du vil angive bestemte ressourcer eller egenskaber, som de skal have.  
1. Indtast eller vælg en værdi i feltet **Krav**.
1. Vælg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]