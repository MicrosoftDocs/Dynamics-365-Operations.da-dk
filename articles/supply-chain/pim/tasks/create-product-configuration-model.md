--- 
title: Oprette en ny model for produktkonfiguration
description: "Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: da8dd3bbc350c29ce1f7dc22ab3914dfee4b967c
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-configuration-model"></a>Oprette en ny model for produktkonfiguration

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-product-model"></a>Oprette en produktmodel
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. Klik på Ny.
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Beskrivelse.
6. Vælg en indstilling i feltet Strategi for problemløser.
    * Problemløserstrategien bestemmer, hvordan begrænsningerne i en begrænsningsbaseret model til produktkonfiguration behandles. Dette valg kan have indflydelse på produktkonfigurationsmodellens ydeevne.  
7. Skriv en værdi i feltet Navn.
    * Rodkomponenten repræsenterer produktkonfigurationsmodellen, men den kan også bruges i andre produktmodeller.  
8. Klik på OK.
9. I feltet Genbrug konfigurationer skal du vælge en indstilling.
    * Hvis genbrugskonfigurationsparameteren er indstillet til Ja, vil systemet søge efter identiske konfigurationer efter hver konfigurationssession, og genbruge, hvis der findes en nøjagtig match.  

## <a name="add-attributes"></a>Tilføj attributter
1. Udvid sektionen Attributter.
2. Klik på Tilføj.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Navn på problemløser.
    * Problemløserens navn bruges til løsning af begrænsningsproblemer af variantstyringen. Det må ikke indeholde mellemrum eller specialtegn, undtagen _ (understregning).  
6. Skriv en værdi i feltet Beskrivelse.
    * Beskrivelsesteksten vises til brugeren af konfigurationen og kan derfor fungere som hjælp til at vælge den rigtige attributværdi.  
7. Indtast eller vælg en værdi i feltet Attributtype.
    * Attributtypen bestemmer, hvilke værdier der er tilgængelige for attributten.  
8. Marker afkrydsningsfeltet Medtag i genbrug.
    * Denne indstilling er kun tilgængelig, når indstillingen Genbrug konfigurationer er valgt. Når attributten medtages i genbrugsafkrydsningsfeltet betyder det, at denne attribut medtages, når systemet søger efter et nøjagtigt match.  

## <a name="add-subcomponents"></a>Tilføj underkomponenter
1. Vis eller skjul sektionen Underkomponenter.
2. Klik på Tilføj.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Navn på problemløser.
6. Skriv en værdi i feltet Beskrivelse.
7. Indtast eller vælg en værdi i feltet Komponent.
    * Hver underkomponent skal referere til en komponent-definition. Dette design understøtter genanvendelige komponenter og sikrer, at når en komponent er defineret, kan den bruges i mange produktmodeller.  
8. Klik på Gem.
9. Klik på Linjedetaljer i stykliste.
    * Formularen Linjedetaljer i stykliste gør det muligt for brugeren at vælge de nødvendige egenskaber for underkomponenten. Hver egenskab kan gives en fast værdi eller knyttes til en attribut. Tilknytning til en attribut medfører, at linjeegenskaben for styklisten få andre værdier, afhængigt af den valgte konfiguration.  
10. Indtast eller vælg en værdi i feltet Varenummer.
    * Hver underkomponent repræsenterer konfigurerbare produktmaster med begrænsningsbaseret konfigurationsteknologi. Referencen sker via varenummeret.  
11. Marker afkrydsningsfeltet Indstil.
12. Vælg Ja i feltet Beregning.
    * Indstilling af beregning sikrer, at produktet skal medtages, når du kører en omkostningsberegning for produktet.  
13. Klik på fanen Opsætning.
14. Marker afkrydsningsfeltet Indstil.
15. Angiv et tal i feltet Antal.
    * Antalsfeltet, der bestemmer, hvor meget af dette produkt, der forbruges i det konfigurerede produkt.  
16. Marker afkrydsningsfeltet Indstil.
17. Angiv et nummer i feltet Pr. serie.
18. Klik på OK.


