--- 
title: "Oprette en indkøbsordre med en leveranceplan"
description: "Denne procedure viser, hvordan du opretter en leveranceplan til en indkøbsordre."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Oprette en indkøbsordre med en leveranceplan

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en leveranceplan til en indkøbsordre. En leveranceplan bruges, når der anmodes om et antal i en ordre eller en kladde, som skal leveres i flere leverancer. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Denne procedure vil normalt ske via en indkøbsagent.


## <a name="create-a-delivery-schedule"></a>Oprette en leveranceplan
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Skriv "US-101" i feltet Kreditorkonto.
4. Klik på OK.
5. Indtast M0001 i feltet Varenummer.
6. Skriv 10 i feltet Antal.
7. Klik på Indkøbsordrelinje.
8. Klik på Leveranceplan.
    * På siden Leveranceplan kan du angive antallet af leverancer, hvor det samlede antal på ordrelinjen leveres fra leverandøren.  
    * Som standard kopieres det samlede antal og andre leveringsoplysninger for den oprindelige købslinje til den første linje i leveranceplanen. I dette eksempel skal vi oprette en tidsplan for to forsendelser, hvor datoen for den anden forsendelse er forskudt en uge i forhold til den første forsendelse.  
9. I feltet Antal skal du ændre antallet til 4.
10. Klik på Ny.
11. Angiv 6 som det resterende antal i feltet Antal.
    * Vælg en dato i feltet for leveringsdato, der er en uge efter datoen på den første leveringslinje.  
    * Du kan holde styr på det samlede antal, der er allokeret til linjerne i leveranceplanen, ved at se felterne Total og Resterende. Når det resterende antal er nul, er det fulde antal fra den oprindelige linje blevet allokeret til tidsplanen.  
12. Udvid sektionen Gebyrkonvertering.
    * Disse indstillinger gør det muligt at styre, hvordan gebyrer skal fordeles på tværs af linjerne i leveranceplanen. Hvis du vælger Kopier bruttobeløb, kopieres samme gebyrbeløbet på den oprindelige ordrelinje til hver leveringslinje. Indstillingen Fordel på leveringslinjer opdeler det oprindelige linjegebyr i overensstemmelse med antallet på hver leverancelinje.  
13. Skjul sektionen Gebyrkonvertering.
14. Klik på OK.
    * Leveranceplanen anvendes nu op ordren.  
    * Den oprindelige ordrelinje, nu kaldet en kommerciel linje, er konverteret til en ordrelinje med flere leverancer. Den er markeret med et tydeligt ikon og fungerer som overskrift for leveringslinjerne.  
15. Vælg den anden ordrelinje, som er den første af de to leveringslinjer.
    * De to nye linjer, kaldet leverancelinjer, udgør én leveranceplan. Ordren behandles mod disse linjer og ikke mod den oprindelige linje. Hvis dokumenter som bekræftelser, produktkvitteringskladder eller fakturaer, udskrives, vises kun leverancelinjerne.  

## <a name="change-the-delivery-schedule"></a>Skift leveranceplanen
    * Du kan ændre antallet på leverancelinjerne. Hvis du gør dette, opdateres den kommercielle linje automatisk til det samlede antal i leverancelinjerne.  
1. Ret antallet i feltet Antal for den første leverancelinje fra 4 til 5.
2. Vælg den første ordrelinje (kommercielle linje).
    * Antallet på den kommercielle linje er blevet ændret til 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Behandl produktkvittering ved hjælp af leveranceplaner
    * Købsordren skal bekræftes, før produktkvitteringen kan behandles. I dette eksempel registreres modtagelsen direkte på indkøbsordren. Modtagelsen blev måske også registreret, da varerne blev modtaget på lageret.  
1. Klik på Køb i handlingsruden.
2. Klik på Bekræft.
3. Klik på Modtag i handlingsruden.
4. Klik på Produktkvittering.
5. Skriv en hvilken som helst værdi i feltet Produktkvittering.
    * Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.  
    * Vælg 'Bestilt antal' i feltet Antal. Denne indstilling betyder, at kvitteringen behandles for det antal, som ordrelinjerne blev oprettet med.  
    * Sørg for, at feltet Udskriv produktkvittering er angivet til Nej. Udskrivning er ikke nødvendigt i dette eksempel.  
6. Udvid sektionen Linjer.
    * Bemærk, hvordan produktkvitteringen oprettes for de to leverancelinjer og ikke den oprindelige ordrelinje. Hvis modtagelsen var blevet registreret på lagerstedet, ville det også blive registreret på linjerne i leveranceplanen.  
7. Skjul sektionen Linjer.
8. Klik på OK for at bogføre kvitteringen.


