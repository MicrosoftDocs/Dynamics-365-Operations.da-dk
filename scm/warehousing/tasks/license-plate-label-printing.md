--- 
title: Aktivere udskrivning af nummerpladeetiket
description: Denne procedure aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4ca3cd02a43692cfa9510847b460a318855fd24
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="enable-license-plate-label-printing"></a>Aktivere udskrivning af nummerpladeetiket

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk. Du kan bruge denne procedure i USMF-demodatafirmaet. Hvis du vil køre den med dine egne data, skal du have en nummerserie defineret for id'er. Du skal konfigurere en etiketprinter, før du begynder denne opgave. Gå til Virksomhedsadministration > Opsætning > Netværksprintere. I handlingsruden skal du klikke på indstillinger og derefter klikke på knappen til Download-installationsprogram for dokumentets ruteplanlægningsagent. Kør installationsprogrammet, og sørg for, at du har en fungerende netværksprinter, der er aktiveret, før du fortsætter med proceduren.


## <a name="set-up-the-gs1-company-prefix"></a>Angiv GS1-virksomhedspræfikset
1. Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.
2. Indtast de 7 tal for dit GS1-virksomhedsnummer i feltet til GS1-firmapræfikset.
3. Klik på Gem.
4. Luk siden.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Konfigurer SSCC-id-sekvensen
1. Gå til Virksomhedsadministration > Nummerserier > Nummerserier.
2. Vælg en indstilling i feltet Område.
3. Vælg en indstilling i feltet Reference.
4. Skriv en værdi i feltet Firma.
5. Markér den valgte række på listen.
6. Klik op linket i den valgte række på listen.
7. Udvid sektionen Segmenter.
8. Klik på Rediger.
9. Markér den første række i tabellen Segmenter
10. Klik på Fjern.
11. Klik på Fjern.
12. Klik på Gem.
13. Luk siden.

## <a name="create-the-document-route-layout"></a>Opret dokumentrutelayoutet
1. Gå til Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrutelayout.
    * Aktivér SSCC-layoutet.  
2. Klik på Ny.
3. Indtast en værdi i feltet Layout-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Find og vælg den ønskede post på listen.
6. Klik på Indsæt i slutningen af teksten.
7. Klik på Gem.
8. Luk siden.

## <a name="set-up-the-document-routing"></a>Konfigurer dokumentruten
1. Gå til Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrute.
2. Vælg en indstilling i feltet Arbejdsordretype.
3. Klik på Ny.
4. Skriv en værdi i feltet Lagersted.
5. Skriv en værdi i feltet Navn.
6. Klik på Ny.
7. Indtast eller vælg en værdi i feltet Layout-id.
8. Vælg det printernavn, du vil bruge, i feltet Navn.
9. Klik på Gem.
10. Luk siden.

## <a name="create-mobile-device-menu"></a>Opret menu til mobilenhed
1. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.
2. Klik på Ny.
3. Skriv en værdi i feltet Menupunktnavn.
4. Skriv en værdi i feltet Titel.
5. Vælg en indstilling i feltet Tilstand.
6. Vælg Ja i feltet Brug eksisterende arbejde.
7. Vælg Ja i feltet Generér id.
8. Udvid sektionen Arbejdsklasser.
9. Klik på Ny.
10. Skriv en værdi i feltet Arbejdsklasse-id.
11. Klik på Gem.
12. Luk siden.
13. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menu i mobilenhed.
14. Find og vælg den ønskede post på listen.
15. Vælg i træet "Vælg det menupunkt, du oprettede før, i træet".
16. Klik på Rediger.
17. Klik på pilen for at føje menupunktet til menuen.
18. Klik på Gem.
19. Luk siden.

## <a name="update-a-work-template"></a>Opdater en arbejdsskabelon
1. Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.
2. Find og vælg den ønskede post på listen.
3. Klik på Rediger.
4. Klik på Ny.
5. Markér den valgte række på listen.
6. Vælg "Udskriv" i feltet Arbejdstype.
7. Indtast eller vælg en værdi i feltet Arbejdsklasse-id.
8. Klik op linket i den valgte række på listen.
9. Klik på Flyt op.
10. Klik på Gem.
11. Luk siden.


