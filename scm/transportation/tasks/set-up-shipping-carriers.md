--- 
title: "Konfigurere fragtmænd"
description: "Denne procedure beskriver, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: eec121859b7135741ccf204fd507ef0790f1c8d4
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-shipping-carriers"></a>Konfigurere fragtmænd

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure beskriver, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats. Derefter kan en transportkoordinator tildele en fragtmand til en indgående eller udgående last.


## <a name="create-a-new-shipping-carrier"></a>Opret en ny fragtmand
1. Gå til Transportstyring > Opsætning > Fragtmænd > Fragtmænd.
2. Klik på Ny.
3. Skriv en værdi i feltet Fragtmand.
4. Skriv en værdi i feltet Navn.
5. Klik på rullelisten i feltet Tilstand for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Udfyld generelle oplysninger om fragtmanden
1. Slå udvidelsen af sektionen Oversigt til/fra.
2. Markér eller fjern markeringen i afkrydsningsfeltet Aktivér fragtmand.
3. Klik på rullelisten i feltet Kreditor for at åbne opslaget.
    * Vælg kreditorkontoen, som fragtmanden skal tildeles.  
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Vælg en indstilling i feltet Transporttilbud.
    * Vælg Manuelt for at bruge siden Transporttilbud, eller vælg EDI for opdatere tilbuddet ved hjælp af EDI (Electronic Data Interchange).  
7. Markér eller fjern markeringen i afkrydsningsfeltet Aktivér fragtmandssatser.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Opret de nødvendige tjenester for fragtmanden
1. Slå udvidelsen af sektionen afsnittet Tjenester til/fra.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Fragttjeneste.
5. Skriv en værdi i feltet Navn.
6. Klik på rullelisten i feltet Transportmetode for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Konfigurer adressen for fragtmanden (valgfrit)
1. Slå udvidelsen af sektionen Adresser til/fra.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn eller beskrivelse.
4. Klik på rullelisten i feltet Land/område for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Postnummer for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Skriv en værdi i feltet Gade.
10. Klik på OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Konfigurer vurderingsprofil for fragtmanden
1. Slå udvidelsen af sektionen Vurderingsprofiler til/fra.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Vurderingsprofil.
5. Skriv en værdi i feltet Navn.
6. Klik på rullelisten i feltet Sted for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
10. Find og vælg den ønskede post på listen.
11. Klik op linket i den valgte række på listen.
12. Klik på rullelisten i feltet Satsprogram for at åbne opslaget.
    * Vælg det Satsprogram, der er i overensstemmelse med den kontrakt, du har lavet med fragtmanden.  
13. Find og vælg den ønskede post på listen.
14. Klik op linket i den valgte række på listen.
15. Klik på rullelisten i feltet Satsmaster for at åbne opslaget.
16. Find og vælg den ønskede post på listen.
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Program til transittid for at åbne opslaget.
19. Klik op linket i den valgte række på listen.
20. Klik på Gem.


