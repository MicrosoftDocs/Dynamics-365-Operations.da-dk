--- 
title: "Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter"
description: "Denne procedure viser, hvordan du indtaster svar på en tilbudsanmodning, angiver score og sammenligner bud og derefter tildeler buddet til en af kreditorerne."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7c76eab2cca4e15c13dd9f79432b9c6d81071a2
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du indtaster svar på en tilbudsanmodning, angiver score og sammenligner bud og derefter tildeler buddet til en af kreditorerne. Du kan bruge denne procedure i USMF-demodatafirmaet. Før du starter, skal du have en tilbudsanmodning med to linjer, der er blevet sendt til mindst to kreditorer. Du kan køre proceduren "Oprette en tilbudsanmodning" som en forudsætning for at oprette den. Du skal have oprettet en scorekriterier, før du kan køre denne procedure.


## <a name="enter-a-reply-from-a-vendor"></a>Angive et svar fra en kreditor
1. Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.
2. Vælg en tilbudsanmodning, der har statussen Afsendt, og klik på linket for tiilbudsanmodningens sagsnummer.
    * Tilbudsanmodningen bør være sendt til mindst 2 kreditorer.  
3. Klik på Overskrift for at gå til listen over kreditorer.
4. Vælg den kreditor, du vil angive et svar til på tilbudsanmodningen.
5. Klik på Indtast svar.
6. Klik på Svar i handlingsruden.
7. Klik på Kopiér data til svar.
    * Denne handling kopierer markerede data, f.eks. antallet fra tilbudsanmodningssagen til svaret på tilbudsanmodningen. Alternativt kan du springe over denne handling og udfylde alle svarfelter manuelt, når du redigerer svaret.  
8. Klik på Rediger.
9. Angiv et tal i feltet Enhedspris.
10. Vælg den anden tilbudslinje.
11. Angiv et tal i feltet Enhedspris.

## <a name="score-the-bid"></a>Give score til det andet bud
1. Klik på Overskrift for at gå til scoren for buddet.
2. Udvid sektionen Budscore.
3. Skriv et tal i feltet Resultat for en af scorekriterierne.
    * Hvis du placerer markøren over et af scorekriterierne, viser et værktøjstip intervallet for scoren. Du kan tilføje et tal mellem 1 og 5 til et af kriterierne i denne demo.  
4. Vælg et andet scorekriterium.
5. Angiv et tal i feltet Resultat.
6. Udvid sektionen Spørgeskemaer.
    * Hvis tilbudsanmodningssagen har et spørgeskema, der blev sendt til kreditorerne, kan du angive deres svar i afsnittet for spørgeskemaet.  
7. Luk siden.

## <a name="enter-a-reply-for-another-vendor"></a>Angive et svar til en anden kreditor
1. Vælg den næste kreditor ved at fjerne den kreditor, du lige har angivet svar til, og derefter vælge rækken for den næste kreditor.
2. Find og vælg den ønskede post på listen.
3. Klik på Indtast svar.
4. Klik på Kopiér data til svar.
5. Klik på Rediger.
6. Angiv et tal i feltet Enhedspris.
7. Vælg den anden tilbudslinje.
8. Angiv et tal i feltet Enhedspris.

## <a name="score-the-second-bid"></a>Give score til det andet bud
1. Klik på Overskrift for at gå til scoren for buddet.
2. Angiv et tal i feltet Resultat.
3. Find og vælg den ønskede post på listen.
4. Angiv et tal i feltet Resultat.

## <a name="compare-the-replies"></a>Sammenligne svarene
1. Klik på Generelt i handlingsruden.
2. Klik på Sammenlign svar.
3. Angiv et tal i feltet Rang.
    * Denne side viser bud med overskriften og linjerne samt den samlede score på overskriftsniveauet. Du kan sammenligne linjerne ved at sortere i gitteret, så sammenlignelige linjer er placeret ved siden af hinanden. Oplysningerne inkluderer også: Antal: Antallet er anført af kreditoren. Dette er muligvis ikke det samme som det antal, der er angivet i tilbudsanmodningen.   Nettobeløb: Den pris, som en kreditor har tilbudt efter fradrag af eventuelle rabatter, for varerne på linjen.   Afvigelse: Det antal dage, hvormed leveringsdatoen i tilbudshovedet eller -linjen afviger fra den ønskede leveringsdato i tilbudsanmodningshovedet eller -linjen.   Du kan angive en rangering for hvert bud.  
4. Vælg overskriftslinjen for det andet bud, du vil rangere.
5. Angiv et tal i feltet Rang.
6. Klik på Gem.

## <a name="reject-a-bid"></a>Afvise et bud
1. Vælg overskriftslinjen for det bud, du vil afvise.
    * Du kan kun acceptere, afvise eller returnere et bud eller linjer i et bud ad gangen.  
2. Marker afkrydsningsfeltet Marker.
    * Hvis du markerer afkrydsningsfeltet Marker i overskriften på et bud, markeres alle linjer. Du kan også vælge at markere et undersæt af linjer i buddet for at afvise eller acceptere dem. Det er muligt at acceptere én kreditors bud for nogle af linjerne i en tilbudsanmodning og derefter tildele andre linjer i en tilbudsanmodning til en anden kreditor, men du skal gøre dette i trin 2, et bud ad gangen. Hvis der findes alternative linjer, kan du kun acceptere den oprindelige budlinje eller dens alternativ, men ikke begge.  
3. Klik på Afvis.
4. Klik på Parametre for at åbne dialogboksen.
5. Indtast eller vælg en værdi i feltet Årsag.
    * Årsagen til afvisningen gemmes i svaret.  
6. Klik på OK.
7. Klik på OK.
8. Luk siden.
9. Luk siden.
10. Opdater siden.

## <a name="accept-a-bid"></a>Acceptere et bud
1. Vælg det bud, du vil acceptere, og klik derefter på linket i feltet Tilbudsanmodning.
2. Klik på Svar i handlingsruden.
3. Klik på Acceptér.
    * Hvis du har markeret bestemte linjer og ikke andre, vil accepten kun omfatte de markerede linjer. Hvis du vil acceptere alle linjer i et bud, behøver du ikke at markere linjerne.  
4. Klik på Parametre for at åbne dialogboksen.
    * Dette gør det muligt at registrere en årsag for accepten af buddet. Årsagen gemmes i buddet.  
5. Indtast eller vælg en værdi i feltet Årsag til godkendelse.
6. Klik på OK.
7. Klik på OK.
    * Når du klikker på OK, genereres en indkøbsordre ud fra de linjer, der er inkluderet i accepten af tilbudsanmodningen. Hvis der er andre bud, der ikke er blevet behandlet (accepteret, afvist eller returneret), bliver du bedt om at afvise de resterende bud.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Få vist den indkøbsordre, der bliver genereret
1. Klik på Generelt i handlingsruden.
2. Klik på indkøbsordre.
    * Her kan du se den indkøbsordre, der blev genereret, da du accepterede buddet.  
3. Luk siden.
4. Luk siden.
5. Luk siden.
6. Luk siden.


