---
title: Definere fordelskundeplaner
description: Denne procedure hjælper med at definere en fordelskundeplan.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bec8653c05d7684202c0e63d049ddb517e12834
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141275"
---
# <a name="define-loyalty-schemes"></a>Definere fordelskundeplaner

[!include [banner](../includes/banner.md)]

Denne procedure hjælper med at definere en fordelskundeplan. Fordelskundeplaner er belønning for opnåelse og indløsning af regler for et loyalitetsprogram. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Retail og Commerce > Kunder > Fordel > Fordelskundeplaner.
2. Klik på Ny.
3. Indtast en værdi i feltet Skema-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Navn for at åbne opslaget.
    * Du kan have flere fordelskundeplaner for et fordelskundeprogram. Fordelskundeplaner kan være for alle kanaler eller en underordnet række kanaler.  
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på Gem.
9. Klik på Tilføj linje.
10. Vælg en indstilling i feltet Aktivitetstype.
    * Vælg Køb produkter efter beløb, hvis kunderne skal kunne optjene belønninger baseret på, hvor meget de bruger. Vælg Køb produkter efter antal, hvis kunderne skal kunne optjene belønninger baseret på, hvor mange produkter de køber.  Vælg Antal salgstransaktioner, hvis kunder skal kunne optjene belønning for hver salgstransaktion, uanset hvad eller hvor meget der købes.  
    * Vælg en kategori. Kategorien vil begrænse, hvilke produkter denne indtjeningsregel gælder for.  
    * Lad feltet være tomt, hvis indtjeningsreglen skal gælde for alle produkter.  
11. Indtast et tal i feltet Aktivitetsbeløb/-antal.
    *  Du bør altid bruge værdien "1,0" for aktivitetstypen Salgstransaktion. For aktivitetstyper for køb efter beløb eller køb efter antal vil enhver transaktion, der er mindre end den angivne værdi, ikke udløse indtægtsreglen. Hvis aktivitetstypen for eksempel er køb efter beløb, og du indtaster "10,00", vil en salgstransaktion på "9,00" ikke optjene belønning ifølge denne indtægtsregel.  
12. Skriv en værdi i feltet Aktivitetsvaluta.
13. Klik på rullelisten i feltet Belønningspoint-id for at åbne opslaget.
14. Klik op linket i den valgte række på listen.
15. Angiv et tal i feltet Belønningspoint.
    * Belønningspoint af typen Beløb registrerer indtjente beløb med decimaler. Hvis indtægtsreglen for eksempel angiver, at der optjenes 1 belønningspoint for hver 1 canadiske dollar, der er brugt, og kunden bruger 1,25 canadiske dollar, optjener kunden derefter 1,25 belønningspoint. Belønningspoint af typen Antal registrerer beløb i hele tal. I eksemplet, hvor indtægtsreglen for eksempel angiver, at der optjenes 1 belønningspoint for hver 1 canadiske dollar, der er brugt, og kunden bruger 1,25 canadiske dollar, optjener kunden 1,0 belønningspoint.  
16. Klik på Gem.
17. Klik på Tilføj linje.
    * Reglerne for indløsning bruges, når der anvendes betalingsmåde for fordelskunder.  
18. Klik på rullelisten i feltet Belønningspoint-id for at åbne opslaget.
    * Der vises kun belønningspoint, som kan indløses.  
19. Klik op linket i den valgte række på listen.
20. Angiv et tal i feltet Belønningspoint.
21. Vælg en indstilling i feltet Indløsningstype.
    * Når der vælges Betaling efter beløb, behandles feltet Beløb eller Antal som en valutaværdi. I dette tilfælde er beløbet for belønningspoint brugt pr. valutaenhed af betalingen et fast forhold. Når der vælges Betaling efter antal, behandles feltet Beløb eller Antal som en antalsværdi. I dette tilfælde er beløbet for belønningspoint anvendt pr. vareantal et fast forhold. Men beløbet i valuta kan variere, hvis prisen på varer, der er betalt med fordelskundebelønningspoint, varierer for det samme antal. Indløsningstype for kundefordelspointrabat er kun gyldig, når konfigurationsnøglen med specifikke funktioner for landet/området "Rusland" er aktiveret, og POS-funktionalitetsprofilerne har ISO-koden "RU".  
    * Vælg en kategori. Kategorien vil begrænse, hvilke produkter denne indløsningsregel gælder for.  
    * Lad feltet være tomt, hvis indløsningsreglen skal gælde for alle produkter.  
22. Indtast et tal i feltet Beløb eller antal.
23. Skriv en værdi i feltet Valuta.
24. Klik på Gem.
25. Klik på Tilføj linje.
    * Vælg en eller flere noder på listen Tilgængelige organisationsnoder og flytte dem til listen Valgte organisationsnoder ved at klikke på pilen mellem de to lister.  
26. Klik på OK.
27. Klik på Gem.
    * Hver gang du skifter kanal for et fordelskundeprogram, skal du køre fordelskundeplaner. På den måde får kanalerne opdaterede fordelskundeplaner.  

