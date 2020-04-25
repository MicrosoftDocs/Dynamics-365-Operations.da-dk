---
title: Aktivere udskrivning af id-etiket
description: Dette emne viser, hvordan du aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 484a1465dd41429fe201de18aac55f118a483cab
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217005"
---
# <a name="enable-license-plate-label-printing"></a>Aktivere udskrivning af id-etiket

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk. Du kan bruge denne procedure i USMF-demodatafirmaet. Hvis du vil køre den med dine egne data, skal du have en nummerserie defineret for id'er. Du skal konfigurere en etiketprinter, før du begynder denne opgave. Gå til Virksomhedsadministration > Opsætning > Netværksprintere. I handlingsruden skal du klikke på indstillinger og derefter klikke på knappen til Download-installationsprogram for dokumentets ruteplanlægningsagent. Kør installationsprogrammet, og sørg for, at du har en fungerende netværksprinter, der er aktiveret, før du fortsætter med proceduren.


## <a name="set-up-the-gs1-company-prefix"></a>Angiv GS1-virksomhedspræfikset
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Parametre til lokationsstyring**.
2. Indtast de 7 tal for dit GS1-firmanummer i feltet **GS1-firmapræfiks**.
3. Vælg **Gem**.
4. Luk siden.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Konfigurer SSCC-id-nummersekvensen
1. Gå til **Navigationsrude > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.
2. Vælg en indstilling i feltet **Område**.
3. Vælg en indstilling i feltet **Reference**.
4. Skriv en værdi i feltet **Firma**.
5. Udvid sektionen **Segmenter**.
6. Vælg **Rediger**.
7. Markér den første række i tabellen **Segmenter**.
8. Vælg **Fjern**.
9. Vælg **Fjern**.
10. Vælg **Gem**.
11. Luk siden.

## <a name="create-the-document-route-layout"></a>Opret dokumentrutelayoutet
1. Gå til **Navigationsrude > Moduler > Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrutelayout**. Aktivér SSCC-layoutet.  
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Layout-id**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg **Indsæt i slutningen af tekst**.
6. Vælg **Gem**.
7. Luk siden.

## <a name="set-up-the-document-routing"></a>Konfigurer dokumentruten
1. Gå til **Navigationsrude > Moduler > Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrute**.
2. Vælg en indstilling i feltet **Arbejdsordretype**.
3. Vælg **Ny**.
4. Skriv en værdi i feltet **Lagersted**.
5. Skriv en værdi i feltet **Navn**.
6. Vælg **Ny**.
7. Indtast eller vælg en værdi i feltet **Layout-id**.
8. Angiv det printernavn, du vil bruge, i feltet **Navn**.
9. Vælg **Gem**.
10. Luk siden.

## <a name="create-mobile-device-menu"></a>Opret menu til mobilenhed
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Menupunktnavn**.
4. Skriv en værdi i feltet **Titel**.
5. Vælg en indstilling i feltet **Tilstand**.
6. Vælg **Ja** i feltet **Brug eksisterende arbejde**.
7. Vælg **Ja** i feltet **Generér id**.
8. Udvid sektionen **Arbejdsklasser**.
9. Vælg **Ny**.
10. Skriv en værdi i feltet **Arbejdsklasse-id**.
11. Vælg **Gem**.
12. Luk siden.
13. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menu i mobilenhed**.
14. Vælg det menupunkt, du tidligere har oprettet, i træet.
15. Vælg **Rediger**.
16. Vælg pilen for at tilføje menupunktet i menuen.
17. Vælg **Gem**.
18. Luk siden.

## <a name="update-a-work-template"></a>Opdater en arbejdsskabelon
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Arbejde > Arbejdsskabeloner**.
2. Vælg **Rediger**.
3. Vælg **Ny**.
4. Vælg **Udskriv** i feltet **Arbejdstype**.
5. Indtast eller vælg en værdi i feltet **Arbejdsklasse-id**.
6. Vælg **Flyt op**.
7. Vælg **Gem**.
8. Luk siden.

