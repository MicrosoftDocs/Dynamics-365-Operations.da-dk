---
title: Oprette en forbrugsrekvisition
description: Denne fremgangsmåde fører dig gennem processen med at oprette en rekvisition.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560637"
---
# <a name="create-a-requisition-for-consumption"></a>Oprette en forbrugsrekvisition

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fører dig gennem processen med at oprette en rekvisition. Den viser forskellige måder at søge efter produkter i indkøbskataloget, og hvordan du tilføjer et produkt, der ikke findes i kataloget. Inden du begynder denne procedure, skal du have en indkøbspolitik, der er konfigureret med Forbrug som standardtypen for rekvisitionen. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Proceduren kan kun udføres af en brugerprofil, der er angivet som arbejder.  Denne opgave vil normalt udføres af en medarbejder. Medarbejders sikkerhedsrolle tillader, at du kan udføre opgaverne, eller hvis du bruger USMF, kan du logge på som Alicia.


## <a name="create-a-new-requisition"></a>Opret en ny rekvisition
1. Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig.
2. Klik på Ny.
3. Angiv et navn for rekvisitionen i feltet Navn.
4. Angiv en dato i feltet Ønsket dato.
    * Som standard kopieres den ønskede dato og regnskabsdatoen til indkøbsrekvisitionslinjerne. De kan ændres på linjeniveau. Den ønskede dato er den leveringsdato, der er anmodet om.  
5. Angiv en dato i datofeltet Regnskab.
    * Regnskabsdatoen bruges til registrering af regnskabsposten i finans og til at kontrollere, om budgetmidlerne er tilgængelige.  
6. Klik på OK.
7. Klik på rullelisten i feltet Årsag for at åbne opslaget.
    * Den forretningsberettigelsesårsag, som du vælger, vises som standard for indkøbsrekvisitionslinjerne, men du kan ændre den på linjeniveau.    
8. Find og vælg den ønskede post på listen.
9. Vælg årsagen.
10. Angiv en mere beskrivende begrundelse for rekvisitionen i oplysningsfeltet

## <a name="add-a-line-to-the-requisition"></a>Føj en ny linje til rekvisitionen.
1. Klik på Tilføj linje.
    * Der er to måder at føje linjer til indkøbsrekvisitionen på. Hvis du allerede kender produktnummeret, eller du allerede ved, at du anmoder om et produkt, der ikke findes i produktkataloget, kan du tilføje linjen direkte med "Tilføj linje". Den anden måde er at bruge "Tilføj produkter", hvor du kan bruge søgning og filtrering til at finde varer i produktkataloget.    
2. Klik på den række, du netop har oprettet.
    * Anmoderen er den arbejder, der har anmodet om rekvisitionen.   
    * Den person, der forbereder rekvisitionen, er som standard den arbejder, der har anmodet om den. Der skal gives tilladelse til at forberede en rekvisitionslinje på vegne af en anden arbejder. Hvis du har sådanne tilladelser, vises de andre arbejdere i dette opslag.  
3. Indtast en værdi i feltet Varenummer.
    * De varer, du kan vælge, er begrænset af kategoriadgangspolitik og indkøbskataloget for den juridiske indkøbsenhed.   
4. Angiv et tal i feltet Antal.

## <a name="add-more-products-to-the-requisition"></a>Føj flere produkter til rekvisitionen
1. Klik på Tilføj produkter.
    * Dette er indstillingen, hvor du kan søge efter produkter i produktkataloget.    
2. Skriv den første del af navnet på den kategori, du søger efter, i feltet Find indkøb, og klik derefter på Enter.
    * Skriv f.eks. comput.  
3. Bruge InvokeDefaultButton-genvejen.
4. I den valgte kategori skal du bruge Filter til filtrering af listen over produkter.
5. Vælg det produktkort, der skal føjes til rekvisitionen.
6. Klik på Føj til linjer
7. Angiv et tal i feltet Antal.
8. Skriv den første del af navnet på den kategori, du søger efter, i feltet Find indkøb, og klik derefter på Enter.
    * Skriv f.eks. over (overstregningstuscher).  
9. Bruge InvokeDefaultButton-genvejen.
10. Klik på Tilføj ikke-angivet produkt til linjer for at tilføje et produkt, der ikke findes i indkøbskataloget.
11. Angiv en værdi i feltet Produktnavn.
12. Skriv en værdi i feltet Enhed.
13. Klik på OK.
14. Angiv en beskrivelse af produktet i feltet Varebeskrivelse.
15. Angiv et tal i feltet Antal.
16. Angiv et tal i feltet Enhedspris.
    * Hvis du kender prisen for en bestemt kreditor (som du vælger i feltet kreditorkonto), kan denne pris indtastes   
17. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
    * De kreditorer, der findes i dette felt, afhænger af de indkøbspolitikker og den status, som kreditoren har for den aktuelle indkøbskategori. Som et alternativ til valg af kreditor her kan du klikke på knappen Foreslå kreditor.    
18. Vælg den kreditor, du vil bruge, på listen.
19. Skriv en værdi i talfeltet Ekstern vare.
    * Dette er et referencenummer til det produkt, der er kendt af kreditoren. Dette kan eksempelvis være varenummeret for produktet i kreditorens eget katalog.  
20. Klik på OK.

## <a name="distribute-amounts"></a>Fordel beløb
1. Klik på Finans.
2. Klik på Fordel beløb.
    * Denne fremgangsmåde viser, hvordan du fordeler omkostningerne for den første linje mellem 2 konti. Dette kan også foretages senere, når rekvisitionen er til gennemsyn.  
3. Klik på Opdel for at oprette en ny fordelingslinje.
4. Vælg den første bærer, som skal være en del af omkostningen, i feltet Finanskonto.
5. Vælg den anden fordelingslinje.
6. Angiv den anden bærer i feltet Finanskonto.
7. Klik på Fordel ligeligt.
8. Luk siden.

## <a name="view-line-details"></a>Vis linjedetaljer
1. Slå udvidelsen af sektionen Linjedetaljer til/fra.

## <a name="submit-the-requisition"></a>Send rekvisitionen
1. Klik på Arbejdsgang for at åbne dialogboksen.
2. Klik på Send.
3. Luk siden.
4. Skriv en bemærkning til godkenderen af rekvisitionen i feltet Bemærkning.
5. Klik på Send.
6. Luk siden.
7. Opdater siden.

