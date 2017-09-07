--- 
title: "Definere cyklusoptælling"
description: "Cyklusoptælling er en lagerproces, du kan bruge til at overvåge disponible varer i lagerbeholdningen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f0d598bbd13406b27a23dcf349f6c81e758a9e61
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="define-cycle-counting"></a>Definere cyklusoptælling 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Cyklusoptælling er en lagerproces, du kan bruge til at overvåge disponible varer i lagerbeholdningen. Denne opgave viser, hvordan du: opsætter standardoptælling af arbejdsprioritet, aktiverer et mobilenhedsmenupunkt til at behandle både plukning og optælling, aktiverer en udløser for optællingsgrænse, når en placering bliver tom, og aktiverer en cyklusoptællingsplan for et bestemt element i et bestemt lagersted. Disse opgaver udføres typisk af en lagerstedschef. Du kan gennemgå denne procedure i USMF-demodatafirmaet eller i dine egne data.


## <a name="set-the-priority-of-counting-work"></a>Angive prioriteten for optælling af arbejde
1. Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.
2. Klik på fanen Cyklusoptælling.
3. Skriv et tal i feltet Prioritet for standardcyklusoptællingsarbejde.
    * Dette trin ændrer prioriteten af cyklusoptællingsarbejdet sammenlignet med andre typer af arbejde på lageret. Du kan øge prioriteten af cyklusoptællingsarbejde ved at angive et lavere tal end for andre typer arbejde.  
4. Klik på Gem.
5. Luk siden.

## <a name="enable-the-mobile-device"></a>Aktivere mobilenheden
1. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.
2. Klik på Ny.
3. Skriv en værdi i feltet Menupunktnavn.
4. Skriv en værdi i feltet Titel.
5. Vælg "Arbejde" i feltet Tilstand.
6. Angiv indstillingen Brug eksisterende arbejde til Ja.
    * Når du vælger Ja for denne indstilling, søger systemet efter eksisterende arbejde, når mobilenhedsmenupunktet bruges.  
7. Vælg "Systembaseret" i feltet Ledet af.
    * Når Systembaseret er markeret, føres lagermedarbejderen til det åbne arbejde, der er defineret i arbejdsklasser. (Vi vil oprette disse arbejdsklasser som det næste).  
8. Udvid eller skjul sektionen Arbejdsklasser.
    * Nu skal vi oprette to arbejdsklasser, der skal bruges sammen med dette menupunkt på mobilenheden. Når dette menupunkt bruges, forespørges der på disse arbejdsklasser, og det arbejdet, der har den højeste prioritet, vises for brugeren.  
9. Klik på Ny.
10. Vælg en værdi i feltet Arbejdsklasse-id.
11. Klik på Ny.
12. Vælg en værdi i feltet Arbejdsklasse-id.
13. Klik på Gem.
14. Luk siden.
15. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menu i mobilenhed.
16. Find og vælg den ønskede post på listen.
17. Vælg 'det menupunkt, du lige har oprettet' i træet.
18. Klik på Rediger.
19. Klik på pilen for at tilføje menupunktet til menuen.
20. Klik på Gem.

## <a name="create-a-counting-threshold"></a>Oprette en optællingsgrænse
1. Gå til Lagerstedsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsgrænser.
2. Klik på Ny.
3. Skriv en værdi i feltet Id for cyklusoptællingsgrænse.
4. Angiv indstillingen Udfør behandling af cyklusoptælling med det samme til Ja.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Gem.
7. Klik på Vælg lokaliteter.
8. Markér den valgte række på listen.
9. Vælg en værdi i feltet Kriterier.
10. Klik på OK.
11. Luk siden.

## <a name="create-a-cycle-count-plan"></a>Oprette en cyklusoptællingsplan
1. Gå til Lagerstedsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsplaner.
2. Klik på Ny.
3. Skriv en værdi i feltet Id for cyklusoptællingsplan.
4. Indtast en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Maks. antal cyklusoptællinger.
6. Klik på Gem.
7. Klik på Vælg lokaliteter.
8. Markér den valgte række på listen.
9. Vælg en værdi i feltet Kriterier.
10. Klik på OK.
11. Skriv et tal i feltet Dage mellem cyklusoptællinger.
    * Hvis f.eks. antallet i feltet Dage mellem cyklusoptællinger, er indstillet til 5, oprettes der cyklusoptællingsarbejde, hver gang der er gået fem dage. Men cyklusoptællingsarbejdet imidlertid behandles på dag tre, oprettes det næste cyklusoptællingsarbejde, fem dage efter at den seneste cyklusoptælling blev behandling, nemlig på dag 8.  
12. Klik på Gem.
13. Klik på Ny.
14. Indtast et tal i feltet Sekvensnummer.
    * Sorteringen udføres fra det mindste tal til det største tal. Værdien skal være større end 0 (nul).  
15. Markér den valgte række på listen.
16. Skriv en værdi i feltet Beskrivelse.
17. Klik på Gem.
18. Klik på Definer produktforespørgsel.
19. Markér den valgte række på listen.
20. Indtast eller vælg en værdi i feltet Kriterier.
21. Klik på OK.
22. Luk siden.

