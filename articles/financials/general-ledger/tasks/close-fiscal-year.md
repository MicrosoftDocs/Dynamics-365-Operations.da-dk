--- 
title: "Lukke regnskabsåret"
description: "Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f2f1f1206f3cb3534ef93923d4945bb63814514
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="close-the-fiscal-year"></a>Lukke regnskabsåret

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår.


## <a name="validate-year-end-close-parameters"></a>Valider årsafslutningens parametre
1. Gå til Finans > Opsætning Finans > Finansparametre.
2. Udvid sektionen Årsafslutning.
3. Vælg Ja eller Nej for indstillingen Slet årsafslutningsposter ved overførsel.
    * Denne indstilling er vigtig, hvis regnskabsåret er blevet lukket, og årsafslutningen køres igen. Hvis indstillingen er angivet til Ja, slettes bilaget for forrige årsafslutning, og der oprettes et nyt bilag for alle kontienes primosaldi. Hvis indstillingen er angivet til Nej, forbliver det tidligere bilag, og der oprettes kun et nyt bilag til regulering af poster, der blev bogført efter den sidste årsafslutning.  
4. Vælg Ja eller Nej for, om der skal oprettes årsafslutningsposter ved overførsel.
    * Hvis værdien angives til Ja, oprettes der to posteringer. Der oprettes et bilag i det regnskabsår, der afsluttes, for at bringe saldiene for P&L-finanskontiene til nul, og der oprettes et andet bilag i det næste regnskabsår for startsaldiene. Hvis værdien angives til Nej, oprettes der et enkelt bilag i det næste regnskabsår for startsaldiene.  
5. Vælg Ja eller Nej for, om du vil angive regnskabsårets status til permanent lukket.
    * Hvis værdien er angivet til Ja, angives regnskabsårets status til Permanent lukket.  Da et permanent lukket år ikke kan åbnes igen, er den bedste fremgangsmåde at angive denne indstilling til Nej.  
6. Vælg Ja eller Nej for, om et bilagsnummer skal udfyldes ved årsafslutningen.
    * Hvis værdien er angivet til Ja, skal der manuelt angives et bilagsnummer under processen for årsafslutning. Der bruges ikke en nummerserie til at oprette dette bilagsnummer. Det er bedste fremgangsmåde at angive den til Ja.  
7. Luk siden.
8. Gå til Finans > Luk periode > Årsafslutning
9. Klik på Ny for at oprette en årsafslutningsskabelon.
    * Der kan oprettes en skabelon for en gruppe af juridiske enheder, der skal køres årsafslutning for. Denne skabelon kan bruges igen år efter år.  
10. I feltet Gruppenavn skal du angive et navn til årsafslutningsskabelonen.
11. Vælg det regnskabsår, som skabelonen skal oprettes for.
    * Det er kun juridiske enheder, der bruger samme regnskabsår, der kan grupperes sammen i skabelonen for årsafslutning. Det skyldes, at årsafslutningen sker ved at vælge et regnskabsår, ikke en dato.  
12. Brug genvejen til lagring af en post.
13. Klik på Tilføj for at vælge de juridiske enheder for denne skabelon.
    * Juridiske enheder kan tilføjes ved enten at vælge de juridiske enheder eller ved at vælge et organisationshierarki.  Der kan kun tilføjes juridiske enheder, hvor det organisatoriske hierarki med den samme regnskabskalender er valgt.  
14. Vælg enten de juridiske enheder eller organisationshierarkiet.
15. Klik på OK.
16. Vælg, om de økonomiske dimensioner skal overføres til det næste regnskabsår.
    * Det er den bedste praksis at angive denne indstilling til Ja for statuskonti.  Derved bevares de økonomiske dimensioner for bogførte posteringer, når der oprettes primosaldi for statuskonti.  Til driftskonti kan du vælge at bevare de økonomiske dimensioner (Luk alle), når saldiene er flyttet til Overført resultat, eller du kan vælge at få de økonomiske dimensioner erstattet med en anden dimensionsværdi (Luk et enkelt. Hvis du vælger Luk et enkelt, kan du definere en bestemt dimensionsværdi for hver dimension eller vælge at lade det være tomt.  
17. Klik på Gem.
18. Start årsafslutningen ved at vælge Kør regnskabsafslutning i handlingsruden.
    * Årsafslutningen køres for den valgte skabelon.  
19. Vælg alle eller nogle af de juridiske enheder fra den skabelon, som årsafslutningen skal køres for.
    * Når årsafslutningen køres første gang, vælger de fleste virksomheder at køre årsafslutningen for alle juridiske enheder i skabelonen for at få primosaldiene. Hvis der foretages reguleringsposteringer herefter, kan du vælge at køre årsafslutningen kun for de juridiske enheder, der har justeringer.  
20. Klik på OK.
21. Vælg regnskabskalender, som årsafslutningen skal køres for.
22. Skriv en værdi i feltet Bilag.
    * Det er en god praksis at medtage regnskabsåret i bilagsnummeret for at gøre det nemmere at finde på det årsafslutningsbilag, der oprettes.  
23. Årsafslutningen køres som standarder i batch.
    * Det er den bedste praksis for langvarige processer, der skal køres i batchtilstand. Det er typisk en af disse processer, hvilket er grunden til, at standarden er at bruge batchtilstand.  
24. Klik på OK.


