---
title: Oprette et rykkerforløb
description: Brug denne procedure til at oprette et rykkerforløb.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734152"
---
# <a name="create-a-collection-letter-sequence"></a>Oprette et rykkerforløb

[!include [banner](../../includes/banner.md)]

Brug denne procedure til at oprette et rykkerforløb. Denne opgave bruger demofirmaet USMF.

1. Gå til **Kredit og inkasso > Konfiguration > Konfigurer rykkerforløb**.
2. Klik på **Ny**.
3. Angiv et sekvens-id, der repræsenterer rækkefølgen, i feltet **Rykkerforløb**. Det vil blive brugt, når du opretter en posteringsprofil.
4. Indtast en værdi i feltet **Beskrivelse**. Betalingsbetingelserne er valgfrie. Hvis du indtaster en værdi her, vil rykkerens gebyrfaktura bruge disse betalingsbetingelser i stedet for betalingsbetingelserne, der er gemt sammen med kunden.  
5. I feltet **Rykkerkode** skal du vælge koden for den første rykker, du vil sende. Den første rykker oprettes på grundlag af fakturaens forfaldsdato, den værdi, som du har angivet som frist i feltet Dage på denne linje, og andre oplysninger, som du angiver på denne linje.  
6. Indtast en værdi i feltet **Beskrivelse**. 
7. Standardvalutaen for gebyret er valutaen i den juridiske enhed. Valutakoden kan være forskellig fra fakturaens valuta.   
8. Klik på **Tilføj** for at tilføje den næste rykker, der skal sendes i rækkefølgen. I mange tilfælde er den første rykker blot en advarsel. Hvis det er nødvendigt, kan du tilføje gebyrer.  
9. I feltet **Rykkerkode** skal du vælge den næste rykker, der skal sendes i rækkefølgen.
10. I feltet **Hovedkonto** skal du vælge den omsætningskonto, der skal bruges til gebyrer.
11. Angiv det gebyr, der opkræves, når denne rykker bogføres.
12. Klik på rullelisten i feltet **Varemomsgruppe** for at åbne opslaget. Vælg en varemomsgruppe, hvis der skal beregnes moms på gebyret.  
13. Klik op linket i den valgte række på listen.
14. Angiv den mindste forsinkede saldo, der kræves, før der sendes en rykker, i feltet **Mindste forsinkede saldo**.
15. Angiv antallet af respitdage, som du vil tillade, i feltet **Dage**. Dette er antallet af dage efter forfaldsdatoen, hvor der kan oprettes en rykker. Forfaldsdatoen, der bruges til beregningen, afhænger af placeringen af rykkeren i rykkersekvensen:
    - Respitperioden for rykker 1 er i forhold til forfaldsdatoen på fakturaen.
    - Respitperioden for rykkere 2 og højere er i forhold til den dato, hvor den forrige rykker bogføres eller udskrives, afhængigt af valget i feltet Opdater rykkerkode på siden Debitorparametre.  
16. Klik på **Tilføj** for at tilføje den sidste rykker i rækkefølgen. Du kan tilføje op til fem rykkerkoder for et rykkerforløb.  
17. I feltet **Rykkerkode** skal du vælge den næste rykker, der skal sendes i rækkefølgen.
18. Indtast en værdi i feltet **Beskrivelse**.
19. Angive de ønskede værdier i feltet **Hovedkonto**.
20. Indtast et tal i feltet **Gebyr i valuta**.
21. Klik på rullelisten i feltet **Varemomsgruppe** for at åbne opslaget.
22. Klik op linket i den valgte række på listen.
23. Skriv et tal i feltet **Mindste forsinkede saldo**.
24. Angiv et tal i feltet **Dage**.
25. Markér afkrydsningsfeltet **Spær**, hvis du vil spærre kunden mod yderligere leveringer og fakturaer. For at fjerne spærringen af kontoen skal du vælge **Nej** i feltet **Fakturering og levering er sat på hold** på siden **Debitorer**.  
26. Udvid oversigtspanelet **Note**.
27. Angiv den tekst, der skal vises i rykkeren for den valgte rykkerkode. Du kan oversætte denne tekst til flere sprog ved hjælp af menuen **Oversættelser** over notefeltet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
