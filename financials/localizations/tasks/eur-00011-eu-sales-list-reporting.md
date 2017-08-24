--- 
title: Konfigurere rapportering for EU-listesystemet
description: "Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1379c8c5bc6f0f80eaa0d9b3348f810631f7c737
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-eu-sales-list-reporting"></a>Konfigurere rapportering for EU-listesystemet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering. Du kan finde flere oplysninger om rapportering i EU-listesystemet, herunder de nødvendige forudsætninger, i Dynamics 365 for Finance and Operations Hjælp.

Denne opgave gælder for alle europæiske lande/områder. Guiden er oprettet ved hjælp af demodatafirmaet DEMF og bruger derfor Tyskland som et EU-land/områdeeksempel. Guiden bruger også Portugal som et EU-land/områdeeksempel.

Disse opgaver er beregnet til systemadministratorer.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Importer konfiguration for elektronisk rapportering for rapportering til EU-listesystemet
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Angiv som aktiv.
3. Klik på Lagre.
4. Klik på Åbn.
5. Klik på Indstillinger i handlingsruden.
6. Klik på Avanceret filtrering/sortering.
7. Klik på Tilføj.
8. Vælg "Konfigurationsnavn" i feltet Felt.
9. Skriv '"EU-listesystem (DE)" i feltet Kriterier.
10. Klik på OK.
11. Klik på Importer.
12. Klik på Ja.
13. Klik på Indstillinger i handlingsruden.
14. Klik på Avanceret filtrering/sortering.
15. Klik på Nulstil.
16. Klik på Tilføj.
17. Vælg "Konfigurationsnavn" i feltet Felt.
18. Skriv "EU-listesystemrapport efter rækker'" i feltet Kriterier.
19. Klik på OK.
20. Klik på Importer.
21. Klik på Ja.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Opsætning af momskoder for rapportering til EU-listesystemet
1. Gå til Moms > Indirekte skatter > Moms > Momskoder.
2. Brug Quick Filter til at filtrere på feltet Momskode med værdien ''VAT19".
3. Udvid sektionen Rapportopsætning.
    * Kontroller, at sektionen Udelukket er angivet til Nej.  
    * Du skal muligvis oplåse opgaveguiden for at ændre denne indstilling.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Opsætning af momsgrupper for rapportering til EU-listesystemet
1. Gå til Moms > Indirekte skatter > Moms > Momsgrupper.
2. Brug Quick Filter til at filtrere på feltet Momsgruppe med værdien ''AR-DOM".
3. Klik på Rediger.
4. Udvid sektionen Konfiguration.
5. Marker den første række på listen.
6. Marker afkrydsningsfeltet Momsfri.
7. Marker den anden række på listen.
8. Marker afkrydsningsfeltet Momsfri.
9. Marker den tredje række på listen.
10. Marker afkrydsningsfeltet Momsfri.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Opsætning af varemomsgrupper for rapportering til EU-listesystemet
1. Gå til Moms > Indirekte skatter > Moms > Momsgrupper.
2. Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''FULL".
    * Kontroller, at Rapporteringstype er indstillet til "Vare".  
    * Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.  
3. Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''RED".
    * Kontroller, at Rapporteringstype er indstillet til "Service".  
    * Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Konfigurere parametre for land/område for rapportering til EU-listesystemet
1. Gå til Skat > Opsætning > Moms > Land/områdeparametre.
2. Klik på Ny.
3. Skriv "PRT" i feltet Land/område.
4. Skriv 'PT' i feltet Moms.

## <a name="create-tax-exempt-numbers"></a>Oprette SE-numre
1. Gå til Skat > Opsætning > Moms > SE-numre.
2. Klik på Ny.
3. Skriv "PRT" i feltet Land/område.
4. Skriv "PT12345" i feltet SE-nummer.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>Konfigurere parametre for rapportering for EU-listesystemet
1. Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.
2. Klik på fanen EU-listesystem.
3. Vælg Ja i feltet Overfør køb.
4. Udvid sektionen Afrundingsregler.
5. Indstil Afrundingsregel til "0.1".
6. Vælg Ja i feltet Brug minimumværdi.
7. Skriv "2" i feltet Antal decimaler.
8. Udvid sektionen Elektronisk rapportering.
9. Vælg "EU-listesystem (DE)" i feltet Filformattilknytning.
10. Vælg "EU-listesystemrapport efter rækker" i feltet Filformattilknytning.
11. Klik på fanen Egenskaber for land/område.
    * Kontroller, at feltet Lande-/områdetype er angivet til "Indland" for landet/området DEU.  
    * Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.  
12. Klik på Ny.
13. Skriv "PRT" i feltet Land/område.
14. Skriv 'PT' i feltet Intrastat-kode.
15. Vælg "EU" i feltet Lande-/områdetype.
16. Klik på fanen Nummerserier.
    * Kontroller, at der er angivet en nummerseriekode for referencen "EU-listesystem".  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Oprette en kunde med henblik på demonstration af EU-rapportering til EU-listesystemet
1. Gå til Debitor > Kunder > Alle kunder.
2. Klik på Ny.
3. Skriv "PRT-001" i feltet Kundekonto.
4. Skriv 'En kunde fra Portugal' i feltet Navn.
5. Vælg "10" i feltet Kundegruppe.
6. Vælg "AR-DOM" i feltet Momsgruppe.
7. Vælg "PT12345" i feltet SE-nummer.
8. Skriv "PRT" i feltet Land/område.
9. Klik på Gem.


