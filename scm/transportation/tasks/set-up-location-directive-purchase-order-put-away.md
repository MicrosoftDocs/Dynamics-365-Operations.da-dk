--- 
title: "Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer"
description: "Denne fremgangsmåde viser, hvordan du opretter en simpel lokalitetsvejledning."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4c2456fffd9a010728154749b35c58db13f142bb
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en simpel lokalitetsvejledning. Det viste eksemplet opretter en lokalitetsvejledning, som skal bruges til at bestemme, hvor du kan placere elementer, der er blevet modtaget for en indkøbsordre. Du kan afspille denne opgaveguide med de nævnte data ved hjælp af demodatafirmaet USMF. Forudsætninger: Du skal oprette en dispositionskode. I denne procedure bruger vi en dispositionskode kaldet Relabel. Hvis du opretter en lokalitetsvejledning i dine egne data, skal du havet oprettet avanceret lagerstedsstyring for dit lagersted og dine elementer.  Denne procedure er beregnet til lagerchefen.

1. Gå til Lagerstedsstyring > Opsætning > Lokalitetsvejledninger.
2. I feltet Arbejdsordretype skal du vælge "Indkøbsordrer".

## <a name="create-a-location-directive-header"></a>Overskriften Oprette en lokalitetsvejledning
1. Klik på Ny.
2. Indtast et tal i feltet Sekvensnummer.
    * Dette er den rækkefølge, som lokalitetsvejledningen skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
3. Skriv en værdi i feltet Navn.
    * Dette er det entydige id for denne vejledning.  
4. Vælg 'Læg på lager' i feltet Arbejdstype.
    * Vælg den type arbejde, der skal udføres. For vejledningen med arbejdsordretype Indkøbsordre er Læg på lager den eneste understøttede værdi.  
5. Skriv en værdi i feltet Sted.
6. Skriv en værdi i feltet Lagersted.
    * Lad Vejledningskode stå tom.  Vejledningskode bruges til at tilknytte en arbejdsordrelinje af typen Læg på lager til en bestemt vejledning. For indkøbsordrer løses lokaliteten for den sidste arbejdsordrelinjer af typen Læg på lager, inden arbejdsskabelonen bestemmes. Det er derfor ikke muligt at tilknytte den sidste linje i en arbejdsskabelon til en bestemt vejledning.   
7. Indtast en værdi i feltet Dispositionskode.
    * Dispositionskoden begrænser brugen af lokalitetsvejledningen, så lokalitetsvejledningen kun bruges, hvis lagerarbejderen angiver denne specifikke værdi under registrering af elementet ved hjælp af en mobilenhed.  
8. Klik på Gem.

## <a name="edit-the-query-for-directive"></a>Rediger forespørgslen for vejledningen
1. Klik på Rediger forespørgsel.
    * Anvendelsen af denne vejledning er allerede begrænset til elementer, der er registreret på det lagersted, du har angivet, og med den dispositionskode, du har angivet. Du kan tilføje andre begrænsninger ved hjælp af forespørgslen.  
2. Klik på OK.

## <a name="add-directive-lines"></a>Tilføj vejledningslinjer
1. Klik på Ny.
    * Dette er den rækkefølge, som lokalitetsvejledningslinjerne skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
2. Indtast et tal i feltet Fra antal.
    * Dette er den laveste mængde, som denne vejledningslinje gælder for.  
3. Indtast et tal i feltet Til antal.
4. Skriv en værdi i feltet Enhed.
    * Den enhed, som Fra antal og Til antal udtrykkes i. Hvis du lader feltet stå tomt, bruges lagerenheden fra varen.  
5. Vælg en indstilling i feltet Angiv lokalitet for antal.
    * Ingen, eller nummerpladeantal: Den mængde, der er registreret på hver nummerplade. Enhedsopdelt antal: Hele den mængde, der er blevet registreret. Resterende antal: Den mængde, der er endnu ikke er registreret fra indkøbsordrelinjen. Forventet mængde: Den samlede mængde, der er angivet på indkøbsordrelinjen.  
6. Markér eller fjern markeringen af afkrydsningsfeltet Begræns efter enhed.
    * Hvis du vælger denne indstilling og angiver enheden på siden Begræns efter enhed, kan kun varer med denne måleenhed placeres på lokaliteten. Hvis måleenheden f.eks. er PL (paller), kan kun elementer på paller placeres på en bestemt lokalitet.  
7. Markér eller fjern markeringen af afkrydsningsfeltet Tillad opdeling.
    * Dette muliggør, at vejledningen opdeler mængden på flere lokaliteter.  
8. Klik på Gem.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Begræns vejledningslinjen til en bestemt enhed
1. Klik på Begræns efter enhed.
    * Denne knap er kun tilgængelig, når du trykker på Gem, efter at du har markeret afkrydsningsfeltet Begræns efter enhed.  
2. Skriv en værdi i feltet Enhed.
3. Luk siden.

## <a name="add-a-location-directive-action-line"></a>Tilføj en vejledningshandlingslinje for lokalitet
1. Klik på Ny.
    * Dette er den rækkefølge, som handlingslinjerne for lokalitetsvejledningen skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
2. Skriv en værdi i feltet Navn.
    * Dette er det entydige id for denne vejledningshandling.  
3. Vælg en indstilling i feltet Anvendelse af fast lokation.
    * Faste og ikke-faste lokationer: Alle ikke-faste lokationer er gyldige lige som produktets egen faste lokation inden for det interval, der er angivet i forespørgslen.  Kun fast lokation for produktet: Faste lokationer for produktet er gyldige, og alle produktvarianter deler samme sæt af faste lokationer. Kun fast lokation for produktvarianterne: Kun faste lokationer, der er angivet for hver produktvariant, er gyldige.  
4. Vælg en indstilling i feltet Strategi.
    * Arbejdsordrer af typen Indkøbsordre understøtter følgende strategier: Ingen: Varen placeres på den første lokalitet, der findes. Konsolidering: Varen placeres på en lokalitet, hvor lignende elementer allerede er tilgængelige. Tom lokation uden indgående arbejde: elementet placeres på den første tomme lokalitet, der findes. En lokalitet betragtes som tom, hvis den ikke har noget fysisk lager og intet forventet indgående arbejde.  
5. Klik på Gem.

## <a name="edit-the-query-for-directive-action-line"></a>Rediger forespørgslen for vejledningshandlingslinjen
1. Klik på Rediger forespørgsel.
2. Klik på Tilføj.
3. Skriv "id for lokationsprofil" i feltet Felt.
    * I dette eksempel vil vi begrænse de mulige lokaliteter ved hjælp af et lokalitetsprofil-id.  
4. Skriv en værdi i feltet Kriterier.
5. Klik på OK.
    * Du kan fortsætte med at tilføje vejledningslinjer og vejledningshandlinger, indtil du har dækket alle de mulige scenarier på lagerstedet.  


