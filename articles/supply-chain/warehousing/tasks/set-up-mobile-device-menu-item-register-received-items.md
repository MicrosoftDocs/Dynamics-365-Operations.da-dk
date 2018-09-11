--- 
title: Konfigurere et menupunkt for mobilenheden til registrering af modtagne varer
description: "Denne opgave fokuserer på opsætningen af et menupunkt på mobilenheden."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7b5d757361c1163bbd0300abd3da4e0a2dd6b0e0
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Konfigurere et menupunkt for mobilenheden til registrering af modtagne varer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave fokuserer på opsætningen af et menupunkt på mobilenheden. Dette menupunkt bruges til registrering af modtagelsen af varer, der er bestilt via købsordrer. 

Du kan bruge denne guide i USMF-demodatafirmaet. Denne procedure er beregnet til lagerchefen.


## <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed
1. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.
2. Klik på Ny.
3. Skriv en værdi i feltet Menupunktnavn.
    * Dette er det entydige id for dette menupunkt i mobilenhed. Du kan for eksempel skrive "Min IO-registrering".  
4. Skriv en værdi i feltet Titel.
    * Dette er den titel, der vises for brugeren på mobilenheden. Du kan for eksempel skrive "IO-registrering".  
5. Vælg "Arbejde" i feltet Tilstand.
    * Registrering af de disponible mængder, der er modtaget for en indkøbsordrelinje, opretter arbejde med at flytte varerne fra modtagelsesområdet til lageret. Arbejde oprettes ikke, før varerne er registreret.  Derfor skal du lade indstillingen Brug eksisterende arbejde være sat til Nej.  
6. Udvis eller skjul sektionen Generelt.
7. Vælg "Indkøbsordrevare til modtagelse" i feltet Arbejdsoprettelsesproces.
    * En indkøbsordrelinje skal være entydigt identificeret, før der kan registreres i en beholdning på lageret. Mobilenheden registrerer indkøbsordrenummeret og varenummeret i dette scenario, så systemet kan identificere indkøbsordrelinjen. Lægge på lager-arbejde bliver oprettet og kan afhentes af en anden arbejder.    Den arbejdsoprettelsesmetode, du vælger, bestemmer, hvilke felter bliver tilgængelige i oversigtspanelet Generelt.  
    * Hvis du vælger indstillingen Brug standarddata, aktiveres knappen Standarddata. Her kan du markere felter for at vise de data, som en arbejder typisk skal bruge i det daglige arbejde, så disse værdier vises på mobilenheden.  
    * Parameteren Gruppering af nummerplader fungerer sammen med enhedens sekvensgruppe, der er tilknyttet den vare, der modtages. Du kan angive, om modtagelser, som er større end eller mere end én palle, skal grupperes i ét id-nummer eller opdeles i et separat id-nummer for hver enhed.  
    * Hvis du vælger indstillingen Generér nummerplade, oprettes et entydigt id-nummer, der er baseret på den valgte nummerserie.   
    * Du kan vælge den skabelon, der skal bruges, når der oprettes arbejde. Hvis du f.eks. registrerer en vare for en indkøbsordre, oprettes læg på lager-arbejdet baseret på arbejdsskabelonen. Hvis du ikke vælger en arbejdsskabelon her, tildeler systemet en skabelon baseret på de forespørgselskriterier, der er knyttet til skabelonerne.  
    * Hvis dispositionskoder vises på mobilenheden, kan arbejdere evaluere status eller kvaliteten af varerne og vælge den relevante kode. Reglerne for dispositionskoden bestemmer, om varerne vil være tilgængelige for andre lagerprocesser. Reglerne bestemmer også, hvilket lokalitetsdirektiv der bruges til det arbejde, der oprettes.   
    * Hvis du vælger indstillingen Batchdispositionskoder, kan arbejdere evaluere status eller kvaliteten af en batch og vælge den relevante dispositionskode.  De regler, der angives for batchdispositionskoden, bestemmer, om batchen vil være tilgængelig for andre lagerprocesser.  
    * Hvis du vælger indstillingen Udskriv etiketter, udskrives en nummerplademærkat automatisk, når der modtages varer.  
8. Klik på Gem.
9. Luk siden.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Føje menupunktet til en mobilenhedsmenu
1. Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menu i mobilenhed.
2. Brug Quick Filter til at filtrere på feltet Navn med værdien "indgående".
3. Klik på Rediger.
4. Vælg 'I menuen og varetræet Tilgængelig skal du vælge det menupunkt, som du oprettede før.' i træet.
    * Vælg det menupunkt, du oprettede før.  
5. Klik på den pil, der peger mod højre.
6. Klik på Gem.
7. Luk siden.


