---
title: EUR-00015 Registrering af kreditors moms-id
description: Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 578f961fe1b5e3d06b624b78c278c8314df47f5e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822554"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a>EUR-00015 Registrering af kreditors moms-id

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto. Denne proces er ens for juridiske enheder og kunder. 

Før du kan udføre denne procedure, skal du konfigurere moms-id'er. Denne procedure gælder for alle europæiske lande/områder. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland. Denne fremgangsmåde er beregnet til en datastyringsadministrator, en debitorchef eller en kreditorchef. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Kreditor > Kreditorer > Alle kreditorer.
2. Find og vælg debitor DE-01001 på listen.
3. Klik på Registrerings-id'er.
4. Klik på Tilføj.
5. Vælg moms-id.
6. Skriv en værdi i feltet Registreringsnummer.
    * Angiv et moms-id i Tyskland for den valgte kreditor. Id'et skal svare til det angivne format for registreringstype.  
7. Klik på fanen Generelt.
8. Angiv en dato i feltet Gældende.
9. Klik på Gem.
10. Klik på Ny.
11. Skriv en værdi i feltet Navn eller beskrivelse.
    * Angiv for eksempel ITA.  
12. Indtast eller vælg en værdi i feltet Land/område.
    * Vælg for eksempel ITA.  
13. Vælg Ja i feltet Primært til land/område.
14. Klik på Gem.
15. Klik på fanen Oversigt.
16. Klik på Tilføj.
17. Indtast eller vælg en værdi i feltet Registreringstype.
    * Vælg f.eks. Moms-id.  
18. Skriv en værdi i feltet Registreringsnummer.
    * Du kan f.eks. angive et moms-id i Italien.  Id'et skal have samme format som registreringstypen.  
19. Klik på Gem.
20. Luk siden.
21. Find og vælg den ønskede post på listen.
    * Vælg f.eks. DE-01001.  
22. Klik op linket i den valgte række på listen.
23. Udvid sektionen Faktura og levering.
24. Klik på Rediger.
25. Indtast eller vælg en værdi i feltet SE-nummer.
26. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]