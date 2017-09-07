--- 
title: Konfigurere salgsprovisionsregler
description: Denne procedure viser, hvordan du kan konfigurere og aktivere beregning og sporing af salgsprovision.
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
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a>Konfigurere salgsprovisionsregler

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan konfigurere og aktivere beregning og sporing af salgsprovision. Proceduren viser, hvordan du kan oprette både debitor- og vareprovisionsgrupper, og hvordan du derefter sammenkæder en valgt kunde og et produkt til de respektive grupper. Disse grupper bruges derefter i opsætningen af provisionsberegningen til at oprette en debitor-, vare- og sælgerkombination, der skal matches af en salgsordre for at berettige sælgerne til en provision. Oprettelse af debitor- og vareprovisionsgrupper er valgfri, da beregningen af provisionen også kan udføres for en individuel debitor og/eller vare. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="set-up-commission-groups-and-commission-rates"></a>Konfigurer provisionsgrupper og provisionssatser
1. Gå til Salg og marketing > Provisioner > Provisionskundegrupper.
2. Klik på Ny.
3. Skriv en værdi i feltet Gruppe.
4. Skriv en værdi i feltet Navn.
5. Klik på Gem.
6. Luk siden.
7. Gå til Salg og marketing > Provisioner > Varegrupper.
8. Klik på Ny.
9. Skriv en værdi i feltet Gruppe.
10. Skriv en værdi i feltet Navn.
11. Luk siden.
12. Gå til Salg og marketing > Provisioner > Salgsgrupper.
    * En provisionssalgsgruppe angiver medarbejderne i sælgerroller, der er berettiget til at modtage en provision, når en kunde, der er knyttet til den relevante salgsgruppe, køber visse varer.  
    * I USMF-demodatafirmaet, er der en salgsgruppe, der kaldes "Sælgere USA".  
13. Klik på Generelt i handlingsruden.
14. Klik på Sælger.
    * Siden Sælger viser en oversigt over virksomhedens sælgere, der er knyttet til en bestemt Kommissionen gruppe. Du kan tildele flere sælgere til den samme gruppe og definere deres respektive andel af den samlede provision gebyr som en procentværdi. Den samlede provision andel på tværs af alle medarbejdere må ikke overstige 100.  
15. Markér den valgte række på listen.
16. Klik på Rediger.
17. Indstil Provisionsandel til "50".
18. Klik på Ny.
19. Klik på rullelisten i feltet Navn for at åbne opslaget.
20. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien "Susan Burk".
21. Klik på Vælg.
22. Indstil Provisionsandel til "50".
23. Klik på Gem.
24. Gå til Salg og marketing > Provisioner > Provisionsberegning.
    * På siden Provisionsberegning kan du definere den provisionssats, medarbejderen skal modtage for en salgspostering, når den indeholder den forudindstillede kombination af kunde og produkt. Som en del af provisionssatsopsætningen, skal du angive provisionsberegningsgrundlaget, og om det skal medtage eller udelukke rabatter. Du kan også angive en gyldighedsperiode for, hvornår provisionssatsen er aktiv.  
25. Klik på Ny.
26. Vælg "Gruppe" i feltet Varekode:
27. Klik på rullelisten i feltet Varerelation for at åbne opslaget.
28. Find og vælg den gruppe, som du oprettede tidligere, på listen.
29. Klik op linket i den valgte række på listen.
30. Vælg Gruppe i feltet Kundekode.
31. Klik på rullelisten i feltet Debitorrelation for at åbne opslaget.
32. Vælg den gruppe, som du konfigurerede tidligere, på listen.
33. I feltet Sælgerrelation skal du klikke på rullelisten for at åbne opslaget.
34. Find og vælg den ønskede post på listen.
    * Bevar indstillingen "Før linjerabat".  
    * Bevar indstillingen "Omsætning" som grundlag for beregningen af provisionsværdien.    
35. Angiv et tal i feltet Provisionssats i procent.
36. Klik på Gem.

## <a name="setting-up-commission-posting"></a>Konfiguration af provisionskonteringer
1. Gå til Salg og marketing > Provisioner > Provisionskontering.
    * Provisionsgebyrer skal betales til medarbejderne og skal derfor sættes op til at sikre korrekt økonomisk bogføring på de relevante konti i finansbogholderiet. Dette gøres på siden Provisionskontering. Gennemse den opsætning, der er tilgængelig for det aktuelle firma. Normalt bogføres provisionsbeløbene på en dedikeret konto for udgifter og modposteres på en dedikeret kreditorkonto. Hvis du ikke har konfigureret regler for provisionskonteringer, kan systemet ikke fuldføre fakturering af en salgsordre, der har berettiget provisioner.  
2. Luk siden.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Tildel en provisionsgruppe til en kunde og et produkt
1. Gå til Salg og marketing > Kunder > Alle kunder.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Udvid sektionen Salgsordrestandarder.
6. Klik på rullelisten i feltet Provisionsgruppe for at åbne opslaget.
7. Vælg den gruppe, som du oprettede tidligere, på listen.
8. Klik på rullelisten i feltet Salgsgruppe for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik på Gem.
11. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
12. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Varenummer med værdien "T0020".
13. Klik op linket i den valgte række på listen.
14. Klik på Rediger.
15. Udvid afsnittet Sælg.
16. Klik på rullelisten i feltet Provisionsgruppe for at åbne opslaget.
17. Find og vælg den provisionsgruppe, som du oprettede tidligere, på listen.

