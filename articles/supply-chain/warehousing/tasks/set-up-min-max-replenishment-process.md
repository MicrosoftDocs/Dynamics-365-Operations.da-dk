---
title: Konfigurere en min.-maks. genopfyldningsproces
description: Denne procedure viser, hvordan du opretter en ny genopfyldningsproces, som bruger strategien for minimal/maksimal genopfyldning.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5fc03e0cf0ceb27a5cc406860bf5bd877e95460c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "318298"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Konfigurere en min.-maks. genopfyldningsproces

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en ny genopfyldningsproces, som bruger strategien for minimal/maksimal genopfyldning. Når lagerbeholdningen falder under minimumniveauet, oprettes arbejde for genopfyldning af lokationen. Proceduren viser også, hvordan faste plukpladser kan tillade genopfyldning, selvom lageret falder under det minimale niveau, og hvordan du aktiverer genopfyldningsprocessen til at køre regelmæssigt ved hjælp af et batchjob. Disse opgaver udføres normalt af en lagerchef. Du kan køre denne procedure i USMF-demodatafirmaet ved hjælp af eksempelværdierne i noterne, eller du kan køre den for dine egne data. Hvis du bruger dine egne data, skal du sørge for, at du har et lagersted, der er aktiveret for lagerstedsstyringsprocesser.


## <a name="create-a-fixed-picking-location"></a>Oprette en fast plukplads
1. Gå til Lagerstedsstyring > Konfiguration > Lagersted > Faste lokationer.
    * Dette er en valgfri opgave for minimal/maksimal genopfyldning, men hvis du bruger en fast plukplads, kan lageret genopfyldes, selvom det falder under det minimale niveau, fordi systemet kan afgøre, hvilke varer der skal genbestilles, selvom der ikke er nogen tilbage.  
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Varenummer.
    * Hvis du bruger USMF, kan du vælge element A0001.  
4. Indtast eller vælg en værdi i feltet Lokation.
    * Hvis du bruger USMF, kan du vælge lokation 2.  
5. Indtast eller vælg en værdi i feltet Lagersted.
    * Hvis du bruger USMF, kan du vælge lagersted 24.  
6. Indtast eller vælg en værdi i feltet Lokation.
    * Hvis du bruger USMF, kan du vælge CP-003.  
7. Luk siden.

## <a name="create-a-replenishment-location-directive"></a>Oprette et lokationsdirektiv for genopfyldning
1. Gå til Lagerstedsstyring > Opsætning > Lokalitetsvejledninger.
    * Lokationsdirektiver bruges til at bestemme, hvor varerne skal plukkes i genopfyldningsprocessen.  
2. Vælg 'Genopfyldning' i feltet Arbejdsordretype.
3. Klik på Ny.
4. Skriv en værdi i feltet Navn.
5. Vælg "Pluk" i feltet Arbejdstype.
6. Indtast eller vælg en værdi i feltet Lokation.
    * Hvis du bruger USMF, kan du vælge lokation 2.  
7. Indtast eller vælg en værdi i feltet Lagersted.
    * Hvis du bruger USMF, kan du vælge lagersted 24.  
8. Klik på Gem.
9. Klik på Ny.
10. Markér den valgte række på listen.
11. Indtast et tal i feltet Til antal.
    * Du kan for eksempel indstille den til 9999.  
12. Markér afkrydsningsfeltet Tillad opdeling.
    * Hvis du vælger denne indstilling, tillader processen for oprettelse af arbejde, at arbejdslinjemængder deles på tværs af flere lokationer.  
13. Klik på Gem.
14. Klik på Ny.
15. Markér den valgte række på listen.
16. Skriv en værdi i feltet Navn.
17. Klik på Gem.
18. Klik på Rediger forespørgsel.
    * Du kan redigere denne forespørgsel for at tilføje begrænsninger for, hvor lageret kan vælges i genopfyldningsprocessen. For eksempel kan lageret muligvis kun bruges i bulkområdet på lagerstedet.  
19. Klik på OK.
20. Luk siden.

## <a name="create-a-replenishment-work-template"></a>Oprette en skabelon for genopfyldningsarbejde
1. Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.
    * Arbejdsskabelonen bruges til at vejlede systemet i, hvordan arbejdet for minimal/maksimal genopfyldning skal oprettes. Som minimum skal der være en arbejdsskabelonlinje til et pluk fra lager og et læg på lager. Arbejdsskabelonen vil sige, at den er ugyldig, indtil alle nødvendige oplysninger er udfyldt.  
2. Vælg 'Genopfyldning' i feltet Arbejdsordretype.
3. Klik på Ny.
4. Indtast en værdi i feltet Arbejdsskabelon.
5. Klik på Gem.
6. Klik på Ny.
7. Vælg "Pluk" i feltet Arbejdstype.
8. Indtast eller vælg en værdi i feltet Arbejdsklasse-id.
    * Det skal være en arbejdsklasse, der er relateret til genopfyldning. Hvis du bruger USMF, skal du vælge Genopfyld.  
9. Klik på Ny.
10. Markér den valgte række på listen.
11. Vælg 'Læg på lager' i feltet Arbejdstype.
12. Indtast eller vælg en værdi i feltet Arbejdsklasse-id.
13. Klik på Gem.
14. Luk siden.

## <a name="create-a-new-replenishment-template"></a>Oprette en ny genopfyldningsskabelon
1. Gå til Lagerstedsstyring > Konfiguration > Genopfyldning > Genopfyldningsskabeloner.
    * Genopfyldningsskabelonen bruges til at definere varer og mængder og den lokation der skal genopfyldes.  
2. Klik på Ny.
3. Skriv en værdi i feltet Genopfyld skabelon.
    * Giv skabelonen et navn for at angive, at den gælder for minimal/maksimal genopfyldning.  
4. Skriv en værdi i feltet Beskrivelse.
5. Markér afkrydsningsfeltet Tillad bølgebehov at bruge ikke-reserverede antal.
    * Hvis du vælger denne indstilling, kan bølgebaseret genopfyldning bruge det antal, der er relateret til minimal/maksimal genopfyldning. Det kan for eksempel være nyttigt, hvis arbejde med minimal/maksimal genopfyldning ikke behandles med det samme, så der ikke oprettes unødvendigt arbejde med genopfyldning efter behov.  
6. Klik på Ny.
7. Indtast et tal i feltet Sekvensnummer.
8. Skriv en værdi i feltet Beskrivelse.
9. Markér den valgte række på listen.
10. Indtast eller vælg en værdi i feltet Genopfyldningsenhed.
    * Vælg for eksempel 'styk'. Denne indstilling er obligatorisk. Så kan du angive en anden måleenhed for genopfyldningsarbejde sammenlignet med den enhed, der er angivet for de minimale og maksimale lagerniveauer i denne skabelon.  
11. Indtast eller vælg en værdi i feltet Arbejdsskabelon.
    * Vælg den arbejdsskabelon, du oprettede tidligere.  
12. Indtast et tal i feltet Minimumantal.
    * Vælg det minimumantal, der skal udløse genopfyldningen. Du kan for eksempel indstille den til 50. Det er muligt at lade indstillingen være nul, hvis du påfylder en fast lokation, og indstillingen Genopfyld tomme faste lokationer er angivet til Ja. Vi anbefaler også, at du vælger indstillingen Genopfyld kun faste lokationer for at forbedre ydeevnen.  
13. Indtast et tal i feltet Maksimumantal.
    * Indstil den for eksempel til 100.  
14. Indtast eller vælg en værdi i feltet Enhed.
    * Tildel enheden for de minimale og maksimale antal. Indstil den for eksempel til 'styk'.  
15. Markér afkrydsningsfeltet Genopfyld tomme faste lokationer.
    * Markér dette afkrydsningsfelt for at genopfylde faste lokationer, når de er tomme. Ellers genopfyldes kun de lokaliteter, hvor der er en mængde på lager.  
16. Markér afkrydsningsfeltet Genopfyld kun faste lokationer.
17. Klik på Vælg produkter.
    * Det er her, du skal definere, hvilke produkter der skal genopfyldes. Hvis indstillingen Faste plukpladser er valgt, skal du også definere lokationerne i denne forespørgsel. Både variantspecifikke forespørgsler og produktspecifikke forespørgsler er tilgængelige.  
18. Vælg rækken Varer.
19. Skriv en værdi i feltet Kriterier.
    * Vælg de elementer, der skal genopfyldes på de faste lokationer. Skriv for eksempel A* for at vælge alle varenumre, der begynder med A.  
20. Klik på Tilføj.
    * Tilføj objektet Lokation (medmindre det allerede findes) for at kunne begrænse genopfyldningsarbejdet til de faste plukpladser inden for et bestemt område på lagerstedet.  
21. Markér den valgte række på listen.
22. Indstil feltet Tabel til Lokationer.
23. Vælg 'Id for lokationsprofil' i feltet Felt.
24. Indtast eller vælg en værdi i feltet Kriterier.
25. Klik på OK.
26. Luk siden.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Indstille genopfyldningsprocessen til at køre som et batchjob
1. Gå til Lagerstedsstyring > Genopfyldning > Genopfyldninger.
    * På siden Genopfyldninger kan du konfigurere genopfyldning til at køre som et batchjob, eller kræve, at den startes manuelt.  
2. Klik på Filtrér.
3. Markér den valgte række på listen.
4. Indtast eller vælg en værdi i feltet Kriterier.
5. Klik på OK.
6. Udvid sektionen Kør i baggrunden.
7. Angiv indstillingen Batchbehandling til Ja.
8. Klik på Gentagelse.
9. Vælg indstillingen Slutdato mangler.
10. Indstil gentagelsesmønsteret.
    * Vælg for eksempel Dage.  
11. Klik på OK.
12. Klik på OK.

