---
title: Konfigurere behandling af bølge
description: Denne vejledning beskriver, hvordan du konfigurerer de kriterier, der bestemmer, hviket arbejde der genereres for et lagersted, når en bølge behandles, og om bølger behandles manuelt eller automatisk.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399146d35388a0151abb23e57bc36ec0173be928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571880"
---
# <a name="configure-wave-processing"></a>Konfigurere behandling af bølge

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning beskriver, hvordan du konfigurerer de kriterier, der bestemmer, hviket arbejde der genereres for et lagersted, når en bølge behandles, og om bølger behandles manuelt eller automatisk. Du angiver kriterierne ved at konfigurere bølgeskabeloner og forespørgsler, der svarer til en bølge med frigivne linjer i salgsordrer, produktionsordrer eller kanbanordrer. Bølgebehandling bruges på lagersteder, der bruger funktionerne i modulet Lagerstedsstyring, og ikke dem, der bruger funktionerne i modulet Lagerstyring. Du kan bruge denne procedure i USMF-demodatafirmaet.

1. Gå til Lagerstedsstyring > Konfiguration > Bølger > Bølgeskabeloner.
2. Klik på Ny.
3. Skriv en værdi i feltet Bølgeskabelonnavn.
    * Når du opretter en bølgeskabelon, kan du angive den rækkefølge, hvori skabelonerne knyttes til frigivne linjer på salgsordrer, produktionsordrer eller kanbans. Når en linje er frigivet til lagerstedet eller produktionen, bruges den første bølgeskabelon, den opfylder kriterierne for. Vi anbefaler, at du placerer skabeloner med de mest specifikke kriterier øverst på listen. Jo bredere kriterier, desto mere sandsynligt er det, at en linje opfylder kriterierne, og et kan medføre, at linjer tildeles til den forkerte bølge.  
4. Skriv en værdi i feltet Beskrivelse af bølgeskabelon.
5. Indtast eller vælg en værdi i feltet Lokation.
    * Hvis du bruger USMF, kan du vælge lokation 2.  
6. Indtast eller vælg en værdi i feltet Lagersted.
    * Hvis du bruger USMF, kan du vælge lagersted 24.  
7. Angiv feltet Automatiser bølgeoprettelse til Ja.
    * Vælg denne indstilling for automatisk at oprette en bølge, når en salgsordre, produktionsordre eller kanban er frigivet til lagerstedet.  
8. Angiv indstillingen Udfør behandling af bølgen ved frigivelse til lagerstedet til Ja. 
    * Vælg denne indstilling for automatisk at behandle bølgen og oprette arbejde, når en linje er frigivet til lagerstedet.  
9. Angiv indstillingen Automatiser frigivelse af bølge til Ja. 
    * Vælg denne indstilling for at frigive bølgen automatisk. Plukkearbejdet oprettes og gøres tilgængeligt på mobilenheder.  
10. Angiv indstillingen Tildel til åbne bølger til Ja. 
    * Linjerne tildeles bølger ud fra forespørgselsfiltret til bølgeskabelonen.  
11. Angiv indstillingen Udfør automatisk behandling af bølge ved grænseværdi til Ja. 
    * Vælg denne indstilling for automatisk at behandle bølgen, når dens værdier når de grænser for vægt, levering, og linjer, der er angivet i feltgruppen Grænser for bølge. Denne indstilling kan kun benyttes, hvis der er valgt Forsendelse i feltet Bølgeskabelontype.  
12. Angiv indstillingen Automatiser frigivelse af genopfyldningsarbejde til Ja. 
    * Vælg denne indstilling for at oprette behovsbaseret genopfyldningsarbejde og frigive det automatisk. Du skal føje genbestillingsbølgemetoden til bølgeskabelonen og oprette en genbestillingsskabelon af typen Bølgebehov.  
13. Udvid sektionen Metoder.
    * Bølgeskabelonmetoder gør det muligt at styre den rækkefølge af aktiviteter, som hver bølge gennemgår når den er behandlet. Du kan for eksempel have en metode til bølgegenopfyldning. Når du tilføjer en metode, vises den automatisk på den korrekte placering i trinrækkefølgen. Hvis du har angivet indstillingen Automatiser frigivelse af genopfyldningsarbejde til Ja, skal du tilføje genopfyldningsmetoden her.  
    * Bølgeattributter, der fungerer som filtre til at begrænse, hvilken type varer der kan bruge bølgen. Du kan for eksempel angive en varegruppe.  
14. Klik på Gem.
15. Luk siden.
16. Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.
17. Udvid sektionen Bølgebehandling.
18. Indtast eller vælg en værdi i feltet Batchgruppe til behandling af bølge.
19. Angiv indstillingen Udfør behandling af bølger i batch til Ja.
20. I feltet Vent på lås (ms.) skal du angive et tal.
    * Angiv tid i millisekunder, som et fordelingstrin venter på en systemressource, der er låst af et andet fordelingstrin. Når denne tid overskrides, behandles bølgen ikke, og der vises en fejlmeddelelse.  
21. Klik på Gem.
22. Luk siden.
23. Gå til Produktionsstyring > Konfiguration > Produktionsstyringsparametre.
24. Vælg en indstilling i feltet Frigiv til lagersted.
    * Når det gælder salgsordrer og kanban-ordrer, skal der reserveres lager, før ordren frigives til lagerstedet. Ellers kan varerne eller fordelingslinjerne ikke behandles i en bølge. Til produktionsordrer kan du også have mulighed for at vælge Tillad delvis reservation. Dette er f.eks. nyttigt, hvis du har de materialer, du skal bruge til at starte en produktion og derefter kan vente med at fuldføre processen, indtil de ekstra materialer bliver tilgængelige. Hvis du vælger denne indstilling, skal du gentage frigivelsen til lagerprocessen manuelt, når de ekstra materialer bliver tilgængelige.  
25. Luk siden.

