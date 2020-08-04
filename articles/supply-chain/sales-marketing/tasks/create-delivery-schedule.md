---
title: Opret leveranceplan
description: Denne procedure viser, hvordan du opretter en leveranceplan til en salgsordre.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 487188531434e65908fbf5fe9dac89bfba8b6a47
ms.sourcegitcommit: 96ec8b7252296de0049bff406c743f8da9e0f0be
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/20/2020
ms.locfileid: "3606839"
---
# <a name="create-delivery-schedule"></a>Opret leveranceplan

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en leveranceplan til en salgsordre. En leveranceplan bruges, når der anmodes om et antal i en ordre eller et tilbud, som skal leveres i flere leverancer. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="create-delivery-schedule"></a>Opret leveranceplan
1. Gå til Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
4. Klik på OK.
5. Indtast eller vælg en værdi i feltet Varenummer.
6. Skriv et tal, der er større end 1, i feltet Antal.
7. Klik på Salgsordrelinje.
8. Klik på Leveranceplan.
    * Siden Leveranceplan er det sted, hvor du kan angive antallet af leverancer, hvor det samlede antal på ordrelinjen leveres til kunden.    
    * Som standard kopieres det samlede antal og andre leveringsoplysninger for den oprindelige salgslinje til den første linje i leveranceplanen. I dette eksempel skal vi oprette en tidsplan for to forsendelser, hvor datoen for den anden forsendelse er forskudt en uge i forhold til den første.  
9. Angiv et tal, der er en del af det samlede antal, i feltet Antal.
10. Klik på Ny.
11. Angiv det resterende antal i feltet Antal.
12. Angiv en dato, der ligger en uge før datoen for den første leverancelinje, i feltet Ønsket afsendelsesdato.
    * De to indstillinger på oversigtspanelet Gebyrkonvertering styrer, hvordan gebyrerne skal fordeles på linjerne i leveranceplanen, når de er blevet tildelt til den oprindelige ordrelinje. Hvis du vælger Kopier bruttobeløb, kopieres samme gebyrbeløb til hver linje. Indstillingen Fordel på leveringslinjer opdeler gebyrer ligeligt på leverancelinjerne.  
    * Det er kun faste gebyrer, der kan opdeles, mens variable gebyrer stadig skal kopieres til linjerne.  
13. Flyt markøren væk fra den anden leverancelinje for at opdatere siden.
    * Du kan holde styr på det samlede antal, der er allokeret til linjerne i leveranceplanen, ved at se felterne Total og Resterende. Når det resterende antal er nul, er det fulde antal fra den oprindelige linje blevet allokeret til tidsplanen.   
14. Klik på OK.
    * Leveranceplanen er nu kopieret til ordrelinjerne.   
    * Den oprindelige ordrelinje, kaldet en kommerciel linje, er konverteret til en ordrelinje med flere leverancer. Den er markeret med et tydeligt ikon og fungerer som overskrift for leveringslinjerne.  
    * De to nye linjer, kaldet leverancelinjer, udgør én leveranceplan. Ordren behandles mod disse linjer og ikke mod den oprindelige linje. Hvis dokumenter som bekræftelse af sedler, pluklister, følgesedler eller fakturaer udskrives, vises kun leverancelinjerne.   
    * Leverancelinjerne kan have forskellige leveringsdatoer, antal, leveringsmåder og lagringsdimensioner, som f.eks. sted og lagersted. Dog skal altid svarer til dem på linjen kommercielle produktdimensionerne, og kan ikke ændres.  
15. Skriv et tal, der er større end det aktuelle tal, i feltet Antal.
16. Vælg den kommercielle linje for at se effekten af genberegningen af antallet.
17. Klik på fanen Pluk og pak i handlingsruden.
18. Klik på Bogfør følgeseddel.
19. Udvid sektionen Parametre.
20. Vælg "Alle" i feltet Antal.
    * Bemærk, at følgesedlen oprettes for de to linjer i leveranceplanen og ikke den oprindelige ordrelinje.  
21. Vælg Ja i feltet Udskriv følgeseddel.
22. Klik på OK.
23. Klik på Ja.
24. Luk siden.
