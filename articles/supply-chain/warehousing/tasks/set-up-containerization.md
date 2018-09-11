--- 
title: Konfigurere containerlogik
description: Denne procedure beskriver, hvordan du automatiserer containeriseringen af laster i Lagerstedsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Konfigurere containerlogik

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure beskriver, hvordan du automatiserer containeriseringen af laster i Lagerstedsstyring. Automatiseret containerisering opretter containere og plukker arbejde for leverancer, når en bølge behandles og arbejdslinjer kan opdeles i mængder, der passer til containerne. Det gør det lettere for lagermedarbejdere at plukke varer direkte i den valgte container. Sammenlignet med den manuelle pakningsproces, udføres opgaver såsom oprettelse af containere, tildeleling af varer og lukning af containere automatisk af systemet. Denne procedure bruger USMF-demofirmaet og udføres af en lagerchef.


## <a name="set-up-a-wave-template"></a>Konfigurere en bølgeskabelon
1. Gå til Lagerstedsstyring > Konfiguration > Bølger > Bølgeskabeloner.
2. Klik på Ny.
3. Skriv en værdi i feltet Bølgeskabelonnavn.
4. Skriv en værdi i feltet Beskrivelse af bølgeskabelon.
5. Indtast eller vælg en værdi i feltet Lokation.
6. Indtast eller vælg en værdi i feltet Lagersted.
7. Udvid sektionen Metoder.
    * I vinduet Valgte metoder vises metoderne for den valgte bølgeskabelontype. Bølgeskabelonen skal indeholde containeriseringsmetoden.  
8. Find og vælg den ønskede post på listen.
9. Skriv en værdi i feltet Kode for bølgetrin.
    * Angiv en bølgetrinkode for den tilføjede metode, som kan være en hvilken som helst kode. Det er muligt at tilføje metoden mere end én gang og tildele forskellige bølgetrinkoder. Til dette formål skal du vælge Kan gentages for denne metode på siden Metoder til bølgeproces.  
10. Klik på Gem.
11. Luk siden.

## <a name="set-up-a-container-type"></a>Konfigurere en containertype
1. Gå til Lagerstedsstyring > Konfiguration > Containere > Containertyper.
    * Du kan definere dine containere på siden Containertyper. Du kan konfiguree containeres fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde, vægt og højde. I dette eksempel har vi tre forskellige størrelser af bokse.  
2. Klik på Ny.
3. Indtast en værdi i feltet Containertypekode.
4. Angiv et tal i feltet Taravægt.
5. Angiv et tal i feltet Maksimal vægt.
6. Angiv et tal i feltet Volumen.
7. Angiv et tal i feltet Længde.
8. Indtast et tal i feltet Bredde.
9. Indtast et tal i feltet Højde.
10. Skriv en værdi i feltet Beskrivelse.
11. Klik på Gem.
12. Klik på Ny.
13. Indtast en værdi i feltet Containertypekode.
14. Skriv en værdi i feltet Beskrivelse.
15. Angiv et tal i feltet Taravægt.
16. Angiv et tal i feltet Maksimal vægt.
17. Angiv et tal i feltet Volumen.
18. Angiv et tal i feltet Længde.
19. Indtast et tal i feltet Bredde.
20. Indtast et tal i feltet Højde.
21. Klik på Gem.
22. Klik på Ny.
23. Indtast en værdi i feltet Containertypekode.
24. Skriv en værdi i feltet Beskrivelse.
25. Angiv et tal i feltet Taravægt.
26. Angiv et tal i feltet Maksimal vægt.
27. Angiv et tal i feltet Volumen.
28. Angiv et tal i feltet Længde.
29. Indtast et tal i feltet Bredde.
30. Indtast et tal i feltet Højde.
31. Klik på Gem.
32. Luk siden.

## <a name="set-up-a-container-group"></a>Konfigurere en containergruppe
1. Gå til Lagerstedsstyring > Konfiguration > Containere > Containergrupper.
2. Klik på Ny.
    * Du kan konfigurere logiske grupper af containertyper. For hver gruppe kan du angive den rækkefølge, i hvilken du skal pakke containerne, og hvor meget containerne skal fyldes op i procent. Varens størrelsesdimensioner bruges til at bestemme, om den kan være i en container. Den container, der er tættest på varens størrelsesdimension, bruges. Hvis du har flere containertyper i en gruppe, anbefaler vi, at du arrangerer rækkefølgen efter størrelse, så den største container er først, nummer 1 i rækkefølgen, og den mindste container er sidst.    
3. Skriv en værdi i feltet Containergruppe-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Ny.
6. Markér den valgte række på listen.
7. Indtast eller vælg en værdi i feltet Containertype.
8. Klik på Ny.
9. Markér den valgte række på listen.
10. Indtast eller vælg en værdi i feltet Containertype.
11. Klik på Ny.
12. Markér den valgte række på listen.
13. Indtast eller vælg en værdi i feltet Containertype.
14. Klik på Gem.
15. Luk siden.

## <a name="set-up-a-container-build-template"></a>Konfigurere en containerbuildskabelon
1. Gå til Lagerstedsstyring > Konfiguration > Containere > Skabeloner til container-build.
2. Klik på Ny.
    * Skabelonen til container-build er baseret på, hvilke af containeriseringsprocesserne der udføres. Hver skabelon til container-build definerer en containeriseringsproces, der vil blive brugt af en bølgeskabelon. Indstillingen Rediger forespørgsel giver dig mulighed at definere de betingelser, som den valgte skabelon vil blive behandlet under. For eksempel kan du kun køre containerisering for bestemte kunder, produkter eller lagersteder, eller du kan tilføje de tilsvarende forespørgselsområder til skabelonen. Feltet Bølgetrinkode viser, hvordan en skabelon til container-build er knyttet til trinnene i en bølgeskabelon. Når der udføres en bølge, bestemmer den, hvilke skabeloner til container-build der bruges til at starte containeriseringen. Feltet Basisforespørgselstype bestemmer, hvad der skal pakkes, og hvad filterforespørgslen skal baseres på.  
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Containerskabelon-id.
5. Indtast eller vælg en værdi i feltet Containergruppe-id.
6. Skriv en værdi i feltet Kode for bølgetrin.
7. Markér afkrydsningsfeltet Tillad opdeling af plukninger.
8. Klik på Gem.
9. Klik på Begrænsninger i containerblanding.
    * Med pauser i blandingsregler kan du angive regler for fordelingslinjer for pakning i containere. Hvis du for eksempel tilføjer feltet Varenummer, når varer tildeles containere, oprettes der en ny container, når der er et nyt varenummer. Dette er vil forhindre, at arbejdere pakker fordelingslinjer for to forskellige kunder i samme container.  
10. Klik på Ny.
11. Vælg en indstilling i feltet Tabel.
12. Indtast eller vælg en værdi i feltet Valg af felt.
13. Klik på OK.


