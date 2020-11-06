---
title: Konfigurere et menupunkt for mobilenheden til registrering af modtagne varer
description: Dette emne fokuserer på opsætningen af et menupunkt på mobilenheden.
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f636a1f3d598a069c3922160eedbe05b68bc91eb
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017431"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Konfigurere et menupunkt for mobilenheden til registrering af modtagne varer

[!include [banner](../../includes/banner.md)]

Dette emne fokuserer på opsætningen af et menupunkt på mobilenheden. Dette menupunkt bruges til registrering af modtagelsen af varer, der er bestilt via købsordrer. 

Du kan bruge denne guide i USMF-demodatafirmaet. Denne procedure er beregnet til lagerchefen.


## <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed
1. Gå i navigationsruden til **Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Menupunktnavn**. Dette er det entydige id for dette menupunkt i mobilenhed. Du kan for eksempel skrive `My PO registration`.  
4. Skriv en værdi i feltet **Titel**. Dette er den titel, der vises for brugeren på mobilenheden. Du kan for eksempel skrive `PO registration`.  
5. Vælg **Arbejde** i feltet **Tilstand**. Registrering af de disponible mængder, der er modtaget for en indkøbsordrelinje, opretter arbejde med at flytte varerne fra modtagelsesområdet til lageret. Arbejde oprettes ikke, før varerne er registreret. Derfor skal du lade indstillingen **Brug eksisterende arbejde** være sat til **Nej**.
6. Vælg **Indkøbsordrevare til modtagelse** i feltet **Arbejdsoprettelsesproces** i sektionen **Generelt**.
    - En indkøbsordrelinje skal være entydigt identificeret, før der kan registreres i en beholdning på lageret. Mobilenheden registrerer indkøbsordrenummeret og varenummeret i dette scenario, så systemet kan identificere indkøbsordrelinjen. Lægge på lager-arbejde bliver oprettet og kan afhentes af en anden arbejder. Den arbejdsoprettelsesmetode, du vælger, bestemmer, hvilke felter bliver tilgængelige i oversigtspanelet **Generelt**.  
    - Hvis du vælger indstillingen **Brug standarddata** , aktiveres knappen **Standarddata**. Her kan du markere felter for at vise de data, som en arbejder typisk skal bruge i det daglige arbejde, så disse værdier vises på mobilenheden.  
    - Parameteren **Gruppering af nummerplader** fungerer sammen med enhedens sekvensgruppe, der er tilknyttet den vare, der modtages. Du kan angive, om modtagelser, som er større end eller mere end én palle, skal grupperes i ét id-nummer eller opdeles i et separat id-nummer for hver enhed.  
    - Hvis du vælger indstillingen **Generér nummerplade** , oprettes et entydigt id-nummer, der er baseret på den valgte nummerserie.  
    - Du kan vælge den skabelon, der skal bruges, når der oprettes arbejde. Hvis du f.eks. registrerer en vare for en indkøbsordre, oprettes læg på lager-arbejdet baseret på arbejdsskabelonen. Hvis du ikke vælger en arbejdsskabelon her, tildeler systemet en skabelon baseret på de forespørgselskriterier, der er knyttet til skabelonerne.  
    - Hvis dispositionskoder vises på mobilenheden, kan arbejdere evaluere status eller kvaliteten af varerne og vælge den relevante kode. Reglerne for dispositionskoden bestemmer, om varerne vil være tilgængelige for andre lagerprocesser. Reglerne bestemmer også, hvilket lokalitetsdirektiv der bruges til det arbejde, der oprettes.   
    - Hvis du vælger indstillingen **Batchdispositionskoder** , kan arbejdere evaluere status eller kvaliteten af en batch og vælge den relevante dispositionskode. De regler, der angives for batchdispositionskoden, bestemmer, om batchen vil være tilgængelig for andre lagerprocesser.  
    - Hvis du vælger indstillingen **Udskriv etiketter** , udskrives en nummerplademærkat automatisk, når der modtages varer.  
7. Vælg **Gem**.
8. Luk siden.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Føje menupunktet til en mobilenhedsmenu
1. Gå i navigationsruden til **Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menu i mobilenhed**.
2. Brug **Quick Filter** til at filtrere på feltet **Navn** med værdien `inbound`.
3. Vælg **Rediger**.
4. I Tilgængelig-menuen og varetræet skal du vælge det menupunkt, som du oprettede før.
5. Vælg den pil, der peger mod højre.
6. Vælg **Gem**.
7. Luk siden.

