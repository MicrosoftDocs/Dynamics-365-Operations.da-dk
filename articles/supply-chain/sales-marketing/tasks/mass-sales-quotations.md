--- 
title: Opret flere salgstilbud
description: "Denne procedure viser, hvordan til effektivt du kan oprette tilbud, der tilbyder en række produkter eller ydelser, der skal sendes til flere kunder."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fcb2c4d47f0c8e701be025e0554ed476693d732
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="mass-create-sales-quotations"></a>Opret flere salgstilbud

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan til effektivt du kan oprette tilbud, der tilbyder en række produkter eller ydelser, der skal sendes til flere kunder. Oprettelse af dette massetilbud er baseret på tilbudsskabeloner. Du kan køre procedure på dine egne data eller i demofirmaet USMF.


## <a name="create-a-quotation-template"></a>Oprette en tilbudsskabelon
1. Gå til Salg og marketing > Opsætning > Tilbud > Skabelongrupper.
2. Klik på Ny.
3. Skriv et id efter eget valg i feltet Gruppe-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Luk siden.
7. Gå til Salg og marketing > Salgstilbud > Alle tilbud.
8. Klik på Ny.
9. Vælg 'Debitor' i feltet Kontotype.
10. Indtast eller vælg en værdi i feltet Kundekonto.
11. Klik på OK.
    * For at et tilbud kan blive en skabelon, skal du udføre nogle trin i opsætningen af tilbudshovedet. Dette skal gøres, før du føjer linjer til tilbuddet.   
12. Klik på Indstillinger i handlingsruden.
13. Klik på Skift visning.
14. Klik på Overskriftsvisning.
15. Udvid sektionen Konfiguration.
16. Indtast eller vælg en værdi i feltet Gruppe-id.
17. Skriv en værdi i feltet Skabelonnavn.
18. Vælg Ja i feltet Aktiv.
    * Kun aktive skabeloner kan bruges, når du anvender en skabelon på et nyt salgstilbud.  
19. Klik på Indstillinger i handlingsruden.
20. Klik på Skift visning.
21. Klik på Linjevisning.
22. Indtast eller vælg en værdi i feltet Vare.
23. Skriv en værdi i feltet Vare.
24. Luk siden.
25. Angiv et tal i feltet Rabatprocentdel.
26. Klik på Tilføj linje.
27. Indtast eller vælg en værdi i feltet Vare.
28. Skriv en værdi i feltet Vare.
29. Luk siden.
30. Angiv en ny pris i feltet Enhedspris, eller rediger den aktuelle pris.
31. Klik på Tilføj linje.
32. Indtast eller vælg en værdi i feltet Vare.
33. Skriv en værdi i feltet Vare.
34. Luk siden.
35. Angiv et tal i feltet Antal.
36. Angiv et tal i feltet Rabat.
37. Klik på Gem.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Anvende skabelonen til at oprette et enkelt tilbud
1. Gå til Salg og marketing > Salgstilbud > Alle tilbud.
    * Bemærk, at det tilbud, du lige har oprettet, er markeret som skabelon.  
2. Klik på Ny.
3. Vælg 'Debitor' i feltet Kontotype.
4. Indtast eller vælg en værdi i feltet Kundekonto.
5. Udvid afsnittet Skabelon.
6. Indtast eller vælg en værdi i feltet Gruppe-id.
7. Indtast eller vælg en værdi i feltet Skabelonnavn.
8. Vælg 'Baseret på skabelonværdier' i feltet Beregningsmåde.
9. Klik på OK.
    * Det nye tilbud er nu oprettet baseret på dataene og vilkårene i skabelonen.  
10. Luk siden.
11. Luk siden.

## <a name="apply-the-template-to-mass-create-quotations"></a>Anvende skabelonen til at oprette flere tilbud
1. Gå til Salg og marketing > Salgstilbud > Opdatering af tilbud > Opret flere tilbud.
2. Vælg 'Debitor' i feltet Kontotype.
3. Indtast eller vælg en værdi i feltet Gruppe-id.
4. Indtast eller vælg en værdi i feltet Skabelonnavn.
5. Vælg 'Baseret på skabelonværdier' i feltet Beregningsmåde.
6. Udvid posterne for at inkludere sektion.
7. Klik på Filtrér.
8. Indstil filteret til at dække en række kunder, du vil medtage i af denne oprettelse af flere tilbud. Brug følgende format "Customer1..CustomerN".
    * For eksempel kan du angive filteret: US-001..US-004  
9. Klik på OK.
10. Klik på OK.
11. Gå til Salg og marketing > Salgstilbud > Alle tilbud.
    * Kontroller, at der er oprettet tilbud for alle de debitorer, der er angivet i masseopdateringsrutinen, på basis af den valgte skabelon.  


