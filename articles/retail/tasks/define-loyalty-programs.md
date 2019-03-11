---
title: Definere fordelskundeprogrammer
description: Denne procedure viser, hvordan du konfigurerer et fordelskundeprogram med to niveauer.
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
ms.openlocfilehash: 9e57bb9c9e3348f2a9853dfda1351a8a75261beb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "355305"
---
# <a name="define-loyalty-programs"></a>Definere fordelskundeprogrammer

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du konfigurerer et fordelskundeprogram med to niveauer. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Detail og handel > .. > Fordelskundeprogrammer.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Tilføj linje.
6. Angiv et tal i feltet Niveau.
7. Skriv et navn for fordelskundeniveauet i feltet Niveau.
8. Indtast en værdi i feltet Beskrivelse.
9. Klik på rullelisten i feltet Datointerval for at åbne opslaget.
    * Dette datointerval skal udvides ud i fremtiden. Hvis for eksempel det datointerval, der er valgt for gold-niveauet, er en periode på ét år, kan kunder, der er berettiget til gold-niveauet, modtage belønninger, der er tildelt til gold-niveauet for ét år. Hvis kunden igen kvalificerer sig til gold-niveauet, mens de er på niveauet, forlænges den dato, hvor niveauet udløber, med endnu et år fra den dato, hvor de kvalificerer sig igen.  
10. Klik op linket i den valgte række på listen.
11. Klik på Tilføj linje.
12. Angiv et tal i feltet Niveau.
13. Skriv et navn for fordelskundeniveauet i feltet Niveau.
14. Indtast en værdi i feltet Beskrivelse.
15. Klik på rullelisten i feltet Datointerval for at åbne opslaget.
16. Klik op linket i den valgte række på listen.
17. Klik på Gem.
18. Find og vælg den ønskede post på listen.
    * Niveauregler definerer det mindste antal belønningspoint, der skal være optjent i en periode for at være berettiget til niveauet.  
19. Slå udvidelsen af sektionen Niveauregler til/fra.
20. Klik på Ny.
    * Der kan være mere end én niveauregel pr. niveau. Du kan for eksempel have tre forskellige kriterier til at optjene et niveau ved at bruge $ 500 på én måned, ved at bruge $ 1000 over et år og ved at have 20 transaktioner i løbet af et år. Hvis du vil gøre dette, skal du oprette tre niveauregler.  
21. Klik på rullelisten i feltet Belønningspoint for at åbne opslaget.
    * Dette skal være et belønningspoint for fordelskunde, som ikke kan indløses.  
22. Klik op linket i den valgte række på listen.
23. Skriv et tal i feltet Min. udstedte point.
    * For det laveste niveau, og hvis alle kunderne kan blive kvalificeret blot ved at deltage i programmet, skal du angive "0".  
24. Klik på rullelisten i feltet Evalueringsdatointerval for at åbne opslaget.
    * Dette datointerval skal udvides bagud i tid. Kun de point, der optjenes i løbet af dette datointerval, tælles med for at nå mindsteværdien for udstedte point.  
25. Klik op linket i den valgte række på listen.
26. Klik på Gem.
27. Find og vælg den ønskede post på listen.
28. Klik på Ny.
29. Klik på rullelisten i feltet Belønningspoint for at åbne opslaget.
30. Klik op linket i den valgte række på listen.
31. Skriv et tal i feltet Min. udstedte point.
32. Klik på rullelisten i feltet Evalueringsdatointerval for at åbne opslaget.
    * Dette datointerval skal udvides bagud i tid.  
33. Klik op linket i den valgte række på listen.
34. Klik på Gem.
35. Klik på Prisgrupper.
    * Hvis du vil give rabatter til fordelskunder. skal du tildele en eller flere prisgrupper til fordelskundeprogrammet og tildele prisgrupperne til rabatter. Det er en best practice ikke at blande prisgrupper på tværs af forskellige typer rabatenheder.  Brug for eksempel ikke samme prisgruppe til en fordelskunderabat og en kanalrabat.  
36. Klik på rullelisten i feltet Prisgruppe for at åbne opslaget.
    * Linket Prisgrupper øverst på siden er til fordelskundeprogrammet. Linket Prisgrupper i oversigtspanelet Programniveauer er kun for et bestemt for et bestemt fordelskundeniveau.  
37. Klik op linket i den valgte række på listen.
38. Klik på Gem.
39. Luk siden.
40. Klik på Gem.

