--- 
title: Oprette callcenter-ordrer
description: "Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: b2e986df1e089ef2a394d0e9d9236d39f2726c77
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="create-call-center-orders"></a>Oprette callcenter-ordrer

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden. Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter. Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.

1. Gå til Detail og handel > Kunder > Kundeservice.
2. Angiv søgekriterierne til at søge efter kunden i feltet Søgetekst.
    * Til denne eksempelprocedure skal du skrive "karen" og trykke på tab.  
3. Klik på Søg.
    * Da der kun er én kunde med navnet Karen i demodataene, vælges de automatisk.  
4. Klik på Ny salgsordre.
5. Udvis eller skjul sektionen Salgsordrehoved.
6. Vælg kildekoden til kataloget.
    * Hvis der ikke er nogen aktive kildekoder, kan du lukke feltet Kilde og springe dette trin over.  
7. Klik på Tilføj linje.
8. Indtast ordet til varesøgning i feltet Varenummer.
    * Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab. Så vises vinduet til varesøgning.  
9. Vælg det produkt, der skal føjes til salgsordren
10. Angiv salgsantallet.
11. Klik på Opret.
12. Klik på Fuldført for at hente kundebetalingen.
13. Klik på Tilføj.
    * Linket Tilføj findes under fanen Betalinger. Udvid fanen Betalinger, hvis den er skjult.  
14. Vælg betalingsmåden.
    * Til denne procedure skal du vælge kontantbetalingsmetoden.  
15. Luk siden.
16. Indtast beløbet.
    * Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb. Det giver dig mulighed for at fuldføre ordren som fuldt ud betalt.  
17. Klik på OK.
18. Klik på Send.


