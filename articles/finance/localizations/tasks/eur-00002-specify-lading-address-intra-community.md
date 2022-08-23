---
title: EUR-00002 Angive en fragtadresse for en transaktion inden for fællesskabet
description: Denne fremgangsmåde viser, hvordan du angiver en læsningsadresse for en transaktion handel i EU.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid
- VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
ms.openlocfilehash: 2094d24f256647ee3193f7e069e33bf4d99c1b70
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280595"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 Angive en fragtadresse for en transaktion inden for fællesskabet

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du angiver en læsningsadresse for en transaktion handel i EU. Eksempelvis bestiller en virksomhed i Tyskland varer fra en leverandør med en tysk firmaadresse. Denne leverandør har et lagersted i Italien og leverer varerne derfra. Denne levering skal rapporteres i Intrastat. Samme funktionsmåde gælder for returvarer fra kunder.
Denne procedure gælder for alle europæiske lande/områder. Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland. Før du kan fuldføre denne procedure, skal du konfigurere Intrastat-rapportering. Denne procedure er kun beregnet til bogholdere. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi
    * Vælg f.eks. DE-001. Denne kreditor har en tysk firmaadresse.  
4. Klik på OK.
5. Markér den valgte række på listen.
6. Indtast eller vælg værdien D0001 i feltet Varenummer.
7. Klik på Gem.
8. Klik på Modtag i handlingsruden.
9. Klik på Transportdetaljer.
10. Angiv en dato og et klokkeslæt i feltet Dato og klokkeslæt for læsning.
11. Klik på Tilføj adresse,
12. Klik på Ny, og opret en ny adresse med formålet Læsning.
13. Skriv Italien i feltet Navn eller beskrivelse.
14. Vælg værdien Læsning.
    * Bemærk, at adressens formål for være Læsning.  
15. Indtast eller vælg værdien ITA i feltet Land/område.
16. Klik på Gem.
17. Luk siden.
18. Klik på Gem.
    * Kontroller, at læsningsadressen er korrekt.  
19. Luk siden.
20. Klik på Køb i handlingsruden.
21. Klik på Bekræft.
22. Klik på Faktura i handlingsruden.
23. Klik på Faktura.
24. Skriv en værdi i feltet Nummer.
25. Indtast en dato i feltet Fakturadato.
26. Klik på Modtag fra: Antal produktkvitteringer for at åbne dialogboksen Fjern.
27. Vælg 'Bestilt antal' i feltet Standardmængde for linjer.
28. Klik på OK.
29. Klik på Transportdetaljer.
    * Kontroller, at varerne er afsendt fra Italien. Hvis det er nødvendigt, kan du redigere læsningsoplysningerne.  
30. Luk siden.
31. Klik på Bogfør.
32. Luk siden.
33. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.
34. Klik på Overførsel.
35. Vælg Ja i feltet Kreditorfaktura.
36. Klik på OK.
37. Klik på fanen Generelt.
    * Find en nyoprettet linje, og kontroller, at afsenderen har leveret varerne fra Italien.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
