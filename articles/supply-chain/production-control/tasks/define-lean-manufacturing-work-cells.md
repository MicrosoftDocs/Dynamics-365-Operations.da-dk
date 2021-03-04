---
title: Definere arbejdsceller for lean manufacturing
description: En arbejdscelle er en bestemt form for ressourcegruppe, der kan bruges i procesaktiviteter for lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4f460fb42be5cbeda55a82e536e2a83cd2f6b608
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424331"
---
# <a name="define-lean-manufacturing-work-cells"></a>Definere arbejdsceller for lean manufacturing

[!include [banner](../../includes/banner.md)]

En arbejdscelle er en bestemt form for ressourcegruppe, der kan bruges i procesaktiviteter for lean manufacturing. Arbejdsceller har indlagrings- og udlagringssteder og en kapacitetsdefinition, der er baseret på en produktionsflowmodel. Du kan få mere at vide om de grundlæggende begreber i arbejdsceller og kapacitetsberegninger i lean manufacturing i hvidbøgerne om Lean manufacturing. Det demodatafirma, der bruges til at oprette denne procedure, er USMF


## <a name="create-a-work-cell"></a>Opret en arbejdscelle. 
1. Gå til Virksomhedsadministration > Ressourcer > Ressourcegrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Ressourcegruppe.
    * Arbejdscelle-id'et er normalt en systematisk kode, som skal være entydig for den juridiske enhed.  
4. Skriv en værdi i feltet Beskrivelse.
    * Beskrivelsen indeholder navnet eller titlen på arbejdscellen.  
5. Klik på rullelisten i feltet Sted for at åbne opslaget.
    * En arbejdscelle er placeret på ét bestemt sted. Både indlagrings- og udlagrings-lagersted og lokalitet skal være placeret på dette sted.  
6. Klik op linket i den valgte række på listen.
7. Klik på rullelisten i feltet Produktionsenhed for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
    * Vælg en produktionsenhed, som denne arbejdscelle tilhører.  
9. Markér afkrydsningsfeltet Arbejdscelle.
    * Hvis du vil bruge en ressourcegruppe som en lean arbejdscelle, skal afkrydsningsfeltet Arbejdscelle være markeret.  Bemærk, at denne egenskab ikke kan ændres, når ressourcegruppen er oprettet.  
10. Klik på rullelisten i feltet Indlagringssted for at åbne opslaget.
11. Klik op linket i den valgte række på listen.
    * Ved kontrol af regnskab og materiale tildeles materialet typisk midlertidigt i produktionen til et specifikt virtuelt lager. Hvis du ønsker at genopfylde lokaliteterne ved hjælp af lagerarbejde, skal de være en del af modtageråvarelageret.  
12. Klik på rullelisten i feltet Indlagringslokation for at åbne opslaget.
13. Klik op linket i den valgte række på listen.
    * Bemærk, at indlagringslokaliteten for en procesaktivitet kan overskrives generelt eller for et bestemt produkt eller produktvariant ved at definere plukaktiviteter, der tilfører til procesaktiviteten. Indlagringslokaliteterne for en arbejdscelle må ikke være id-kontrollerede.  
14. Klik på rullelisten i feltet Udlagringssteder for at åbne opslaget.
15. Find og vælg den ønskede post på listen.
    * I flere aktivitetsproduktionsflow eller produktionslinjer er det ofte indlagringslagerstedet for den næste arbejdscelle eller salg-s eller transitlagersted, hvor et produkt normalt overføres til efter fremstillingen. Husk, ved modellering af manufacturingprocesser er transport er normalt affald ligesom rapportering af transport.  
16. Klik op linket i den valgte række på listen.
17. Klik på rullelisten i feltet Udlagringslokation for at åbne opslaget.
    * I et produktionsflow med flere procesaktiviteter er dette ofte indlagringsplaceringen af den næste arbejdscelle.  
18. Find og vælg den ønskede post på listen.
19. Klik op linket i den valgte række på listen.
20. Udvid eller skjul sektionen Handling.
    * En procestidskategori skal angives for at aktivere omkostningsberegning og behandling af lean kanban-job.  
21. Klik på rullelisten i feltet Procestidsart for at åbne opslaget.
22. Find og vælg den ønskede post på listen.
    * Omkostningskategorien for procestiden bruges i standardomkostningsberegningen og på efterkalkulerede varetræk.  
23. Klik op linket i den valgte række på listen.
24. Udvid eller skjul sektionen Kalendere.
25. Klik på Tilføj.
26. Klik på rullelisten i feltet Kalender for at åbne opslaget.
27. Find og vælg den ønskede post på listen.
    * Arbejdsceller på et bestemt sted bruger normalt den samme arbejdstidskalender. Hvis arbejdsceller kan have individuelle arbejdstider, skal du muligvis oprette en specifik arbejdstidskalender for arbejdscellen. Bemærk, at kalenderen bør have en normal arbejdstid, der defineres, når den anvendes til lean arbejdscelle, fordi definitionen af kapacitet normalt er relateret til den normale arbejdstid for en arbejdsdag.  
28. Klik op linket i den valgte række på listen.
29. Udvid eller skjul afsnittet Arbejdscelles kapacitet.
30. Klik på Tilføj.
31. Klik på rullelisten i feltet Produktionsflowmodel for at åbne opslaget.
32. Find og vælg den ønskede post på listen.
    * Denne procedurer kræver produktionsflowmodeltypen Gennemløb, som viser definitionen af gennemløbskapaciteten.  
33. Klik op linket i den valgte række på listen.
34. Vælg en indstilling i feltet Kapacitetsperiode.
    * Indstillingerne omfatter: Standardarbejdsdag – Kapaciteten udtrykkes ved længden af den almindelige arbejdsdag i arbejdstidskalenderen for arbejdscellen. Den faktiske arbejdstid bestemmes ud fra kalenderen, og effektive disponible kapacitet beregnes ud fra der for hver dag.   Uge – Giver en ugentlig kapacitet. Der foretages ingen regulering efter den faktiske arbejdstid.   Måned – Giver en månedlig kapacitet. Der foretages ingen regulering efter den faktiske kapacitet.   Normalt bruges standardarbejdsdagen til daglig perioder, og den ugentlige kapacitet bruges til ugentlige kapacitetsperioder.  
35. Indtast et tal i feltet Gennemsnitligt antal gennemløb.
    * Bemærk, at en lean handling aldrig konfigureres til den størst mulige kapacitet i et ideelt miljø. I stedet skal kapaciteten altid defineres for operationer, der kører under normale omstændigheder.  
36. Klik på rullelisten i feltet Enhed for at åbne opslaget.
37. Klik op linket i den valgte række på listen.
38. ResolveChanges enheden.

## <a name="add-a-financial-dimension"></a>Tilføj en økonomisk dimension
1. Udvid eller skjul sektionen Økonomiske dimensioner.
    * Bemærk, at økonomiske dimensioner, der er defineret i produktionsflowet, tilsidesætter den økonomiske dimension i en given arbejdscelle.    De økonomiske dimensioner, der kan vælges, afhænger af konfigurationen af de økonomiske dimensioner for dit system. Denne fremgangsmåde svarer til de demodata, der er angivet i USMF-firmaet. Når du bruger andre data, kan fremgangsmåden muligvis ikke anvendes.  
2. Klik på rullelisten i feltet CostCenter for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
    * De dimensioner, der skal være markeret i lean arbejdsceller, afhænger af gennemførelsen af økonomiske dimensioner i regnskabsmodellen for en bestemt juridisk enhed.  
4. Klik op linket i den valgte række på listen.
5. Klik på rullelisten i feltet Varegruppe for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.

## <a name="save"></a>Gem
1. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]