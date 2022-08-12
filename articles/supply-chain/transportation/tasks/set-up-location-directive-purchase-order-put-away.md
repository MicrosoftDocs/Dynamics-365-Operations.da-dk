---
title: Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer
description: Denne artikel beskriver, hvordan du konfigurerer en enkel lokationsvejledning.
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25484efd7be026bfc3a209fb52822b87d6b76cc2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065488"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer en enkel lokationsvejledning. Det viste eksemplet opretter en lokalitetsvejledning, som skal bruges til at bestemme, hvor du kan placere elementer, der er blevet modtaget for en indkøbsordre. Du kan afspille denne opgaveguide med de nævnte data ved hjælp af demodatafirmaet USMF. Forudsætninger: Du skal oprette en dispositionskode. I denne procedure bruger vi en dispositionskode kaldet Relabel. Hvis du opretter en lokalitetsvejledning i dine egne data, skal du havet oprettet lokationsstyringsprocesser (WMS) for dit lagersted og dine elementer. Denne procedure er beregnet til lagerchefen.

1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Lokationsvejledninger**.
2. I feltet **Arbejdsordretype** skal du vælge **Indkøbsordrer**.

## <a name="create-a-location-directive-header"></a>Overskriften Oprette en lokalitetsvejledning
1. Vælg **Ny**.
2. Indtast et tal i feltet **Serienummer**. Dette er den rækkefølge, som lokalitetsvejledningen skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
3. Skriv en værdi i feltet **Navn**. Dette er det entydige id for denne vejledning.  
4. Vælg **Læg på lager** i feltet **Arbejdstype**. Vælg den type arbejde, der skal udføres. For vejledningen med arbejdsordretype Indkøbsordre er **Læg på lager** den eneste understøttede værdi.  
5. Skriv en værdi i feltet **Sted**.
6. Skriv en værdi i feltet **Lagersted**. Lad Vejledningskode stå tom.  Vejledningskode bruges til at tilknytte en arbejdsordrelinje af typen Læg på lager til en bestemt vejledning. For indkøbsordrer løses lokaliteten for den sidste arbejdsordrelinjer af typen Læg på lager, inden arbejdsskabelonen bestemmes. Det er derfor ikke muligt at tilknytte den sidste linje i en arbejdsskabelon til en bestemt vejledning.   
7. Indtast en værdi i feltet **Dispositionskode**. Dispositionskoden begrænser brugen af lokalitetsvejledningen, så lokalitetsvejledningen kun bruges, hvis lagerarbejderen angiver denne specifikke værdi under registrering af elementet ved hjælp af en mobilenhed.  
8. Vælg **Gem**.

## <a name="edit-the-query-for-directive"></a>Rediger forespørgslen for vejledningen
1. Vælg **Rediger forespørgsel**. Anvendelsen af denne vejledning er allerede begrænset til elementer, der er registreret på det lagersted, du har angivet, og med den dispositionskode, du har angivet. Du kan tilføje andre begrænsninger ved hjælp af forespørgslen.  
2. Vælg **OK**.

## <a name="add-directive-lines"></a>Tilføj vejledningslinjer
1. Vælg **Ny**. Dette er den rækkefølge, som lokalitetsvejledningslinjerne skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
2. Indtast et tal i feltet **Fra antal**. Dette er den laveste mængde, som denne vejledningslinje gælder for.  
3. Indtast et tal i feltet **Til antal**.
4. I feltet **Enhed** skal du angive en værdi. Den enhed, som Fra antal og Til antal udtrykkes i. Hvis du lader feltet stå tomt, bruges lagerenheden fra varen.  
5. Vælg en indstilling i feltet **Angiv lokalitet for antal**.
    - Ingen eller nummerpladeantal: Den mængde, der er registreret på hver nummerplade.  
    - Enhedsopdelt antal: Hele den mængde, der er blevet registreret.  
    - Resterende antal: Den mængde, der er endnu ikke er registreret fra indkøbsordrelinjen.  
    - Forventet mængde: Den samlede mængde, der er angivet på indkøbsordrelinjen.  
6. Markér eller fjern markeringen af afkrydsningsfeltet **Begræns efter enhed**. Hvis du vælger denne indstilling og angiver enheden på siden **Begræns efter enhed**, kan kun varer med denne måleenhed placeres på lokaliteten. Hvis måleenheden f.eks. er PL (paller), kan kun elementer på paller placeres på en bestemt lokalitet.  
7. Markér eller fjern markeringen af afkrydsningsfeltet **Tillad opdeling**. Dette muliggør, at vejledningen opdeler mængden på flere lokaliteter.  
8. Vælg **Gem**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Begræns vejledningslinjen til en bestemt enhed
1. Vælg **Begræns efter enhed**. Denne knap er kun tilgængelig, når du trykker på **Gem**, efter at du har markeret afkrydsningsfeltet **Begræns efter enhed**.  
2. I feltet **Enhed** skal du angive en værdi.
3. Luk siden.

## <a name="add-a-location-directive-action-line"></a>Tilføj en vejledningshandlingslinje for lokalitet
1. Vælg **Ny**. Dette er den rækkefølge, som handlingslinjerne for lokalitetsvejledningen skal behandles i for den valgte arbejdstype. Hvis det er nødvendigt, kan du også ændre rækkefølgen.  
2. Skriv en værdi i feltet **Navn**. Dette er det entydige id for denne vejledningshandling.  
3. Vælg en indstilling i feltet **Anvendelse af fast lokation**.
    - Faste og ikke-faste lokationer: Alle ikke-faste lokationer er gyldige lige som produktets egen faste lokation inden for det interval, der er angivet i forespørgslen.  
    - Kun fast lokation for produktet: Faste lokationer for produktet er gyldige, og alle produktvarianter deler samme sæt af faste lokationer.  
    - Kun fast lokation for produktvarianterne: Kun faste lokationer, der er angivet for hver produktvariant, er gyldige.  
4. Vælg en indstilling i feltet **Strategi**. Arbejdsordrer af typen indkøbsordre understøtter følgende strategier: 
    - Ingen: Varen placeres på den første lokalitet, der findes.  
    - Konsolidering: Varen placeres på en lokalitet, hvor lignende elementer allerede er tilgængelige.  
    - Tom lokation uden indgående arbejde: elementet placeres på den første tomme lokalitet, der findes. En lokalitet betragtes som tom, hvis den ikke har noget fysisk lager og intet forventet indgående arbejde.  
5. Vælg **Gem**.

## <a name="edit-the-query-for-directive-action-line"></a>Rediger forespørgslen for vejledningshandlingslinjen
1. Vælg **Rediger forespørgsel**.
2. Vælg **Tilføj**.
3. Angiv `location profile ID` i feltet **Felt**. I dette eksempel vil vi begrænse de mulige lokaliteter ved hjælp af et lokalitetsprofil-id.  
4. Skriv en værdi i feltet **Kriterier**.
5. Vælg **OK**. Du kan fortsætte med at tilføje vejledningslinjer og vejledningshandlinger, indtil du har dækket alle de mulige scenarier på lagerstedet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]