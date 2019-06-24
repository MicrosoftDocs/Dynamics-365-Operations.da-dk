---
title: EUR-00015 Registrering af kreditors moms-id
description: Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9788a35e768a4a289742e9cd864b3ca185a0407
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566869"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a>EUR-00015 Registrering af kreditors moms-id

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto. Denne proces er ens for juridiske enheder og kunder. 

Før du kan udføre denne procedure, skal du konfigurere moms-id'er. Denne procedure gælder for alle europæiske lande. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland. Denne fremgangsmåde er beregnet til en datastyringsadministrator, en debitorchef eller en kreditorchef. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

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

