--- 
title: Oprette og redigere salgstilbud
description: Denne procedure viser, hvordan du opretter og opdaterer et salgstilbud.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5dcf7d2b5e5d5397c51c51223abe95f9d4911b4f
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-edit-sales-quotations"></a>Oprette og redigere salgstilbud

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter og opdaterer et salgstilbud. Du kan køre procedure på dine egne data eller i demofirmaet USMF.


## <a name="create-a-sales-quotation"></a>Oprette et salgstilbud
1. Gå til Salg og marketing > Salgstilbud > Alle tilbud.
2. Klik på Ny.
3. Vælg Kundeemne i feltet Kontotype.
4. Indtast eller vælg en værdi i feltet Kundeemne.
5. Udvid sektionen Generelt.
    * Typen indstilles automatisk til Salgstilbud, fordi du har valgt at oprette et tilbud fra området Salg og marketing. Hvis du vil oprette et tilbud for et projekt, kan du åbne det i modulet Projektstyring og regnskab.   
6. Klik på OK.
    * Felter og handlinger på tilbudslinjerne er meget lig dem på salgsordrelinjerne.   Som salgsordrer, kan der oprettes tilbud for en bestemt vare, eller når varenummer ikke er kendt eller ikke findes på tidspunktet for oprettelse af tilbud, kan der oprettes tilbud for en salgskategori.  
7. Indtast eller vælg en værdi i feltet Vare.
8. Skriv en værdi i feltet Vare.
9. Luk siden.
10. Angiv et tal i feltet Antal.
    * Hvis der er gyldige samhandelsaftaler for varen, der er valgt på linjen, kopieres gældende priser og rabatter automatisk til tilbudslinjen. Kontroller, at feltet Enhedspris indeholder en værdi, og du kan også angive værdier for rabat, hvis du vil.  
11. Klik på Gem.
12. Klik på Salgstilbud i handlingsruden.
13. Klik på Totaler.
14. Klik på OK.
15. Klik på Salgstilbudslinje.
16. Klik på Priser.
    * På siden Kør prissimulering kan du eksperimentere med at justere forventet omsætning eller rentabilitet for dit tilbud baseret på den ønskede enhedspris, rabatbeløb, rabatprocent, samlet beløb, margen eller dækningsgrad.   Når du er tilfreds med måltallene, anvender du forslaget på tilbudslinjen; så opdateres dens prisrelaterede felter tilsvarende.  
    * Du kan oprette så mange prissimuleringer, som du ønsker. Når du klikker på Ny, kopieres prisbetingelserne fra den aktuelle tilbudslinje til siden. Du kan derefter ændre værdierne i ethvert af de prisrelaterede felter til målværdierne. En ændring i et af felterne udløser genberegning i alle andre felter. Produktets enhedsomkostning skal være kendt, for at systemet kan beregne salgsmargen og dækningsgrad. Brug fanen Simulerede priser for at se en detaljeret visning af de oprindelige priser, foreslåede ændringer og deres indvirkning på de samlede tilbudsbeløb.   Som hovedregel, når der anvendes en simulering, der angiver et nyt beløb på tilbudslinjen, genberegner og angiver systemet en ny værdi i feltet Enhedspris. Hvis simuleringen er baseret på en ny margen eller en ny dækningsgrad, opdateres kun feltet Nettobeløb, og Enhedspris er tomt. I begge tilfælde slettes eventuelle rabatter, der var på tilbudslinjen før simulering.  
17. Luk siden.
18. Klik på Tilbud i handlingsruden.
19. Klik på Send tilbud.
20. Vælg Ja i feltet Udskriv tilbud.
21. Klik på OK.
    * Rapporten kan tage et minut at generere. Luk ikke siden, før den er færdig.  
22. Luk siden.

## <a name="update-a-sales-quotation"></a>Opdatere et salgstilbud
1. Klik på Opfølgning i handlingsruden.
2. Klik på Konverter til kunde.
3. Skriv en værdi i feltet Kundekonto.
4. Klik på Kontroller.
    * Kontroller, at der vises en meddelelse om, at det kontonummer, du har skrevet, kan benyttes.  
5. Klik på OK.
    * Systemet er nu oprettet en ny debitorkonto for kundeemnet i tilbuddet.  
6. Luk siden.
7. Klik på Opfølgning i handlingsruden.
8. Klik på Bekræft.
9. Indtast eller vælg en værdi i feltet Årsag.
10. Klik på OK.
11. Klik på Generelt i handlingsruden.
12. Klik på Salgsordrer.
13. Luk siden.


