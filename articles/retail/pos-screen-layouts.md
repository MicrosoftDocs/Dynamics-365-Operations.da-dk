---
title: "Konfigurer skærmlayouts til POS"
description: "Dette emne indeholder oplysninger om skærmlayouts til Microsoft Dynamics 365 for Retail POS-oplevelser."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad425ab0848ab04003b7378cb5c488650f01c441
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurere skærmlayout til POS

[!INCLUDE [banner](includes/banner.md)]

Dette emne indeholder oplysninger om skærmlayouts til Microsoft Dynamics 365 for Retail POS-oplevelser.

Brugergrænsefladen i Microsoft Dynamics 365 for Retail POS kan konfigureres ved hjælp af en kombination af visuelle profiler og skærmlayouts, der er tildelt til butikker, kasseapparater og/eller brugere.

## <a name="visual-profile"></a>Visuel profil
Visuelle profiler tildeles til kasseapparater og bruges til at angive de visuelle elementer, der er kasseapparatspecifikke og delt på tværs af brugere. Alle brugere, der logger på kasseapparatet, får vist det samme tema, farver og billeder. 

**Profilnummer** - Profilnummeret er den entydige identifikator for den visuelle profil. 

**Beskrivelse** - Beskrivelsen giver dig mulighed for at angive et beskrivende navn, der hjælper med til at identificere den korrekte profil for din situation.

**Tema** - Brugerne kan vælge mellem de lyse eller mørke programtemaer. Disse indstillinger påvirker skrifttypefarven og baggrundsfarverne i hele programmet.

**Markeringsfarve** – Markeringsfarven bruges overalt på POS-enheden til at adskille eller fremhæve visse visuelle elementer, f.eks.felter, kommandoknapper eller hyperlinks. Disse elementer kræver typisk handling.

**Overskriftsfarve** – Overskriftsfarven gør det muligt for brugeren at konfigurere farven i sidehovedet til at imødekomme detailhandlerens behov for branding. Denne funktion er kun tilgængelig i Dynamics 365 for Retail version 1611.

**Logonbaggrunde** – Brugere kan angive et baggrundsbillede til logonskærmen. Filstørrelsen for baggrundsbilleder bør være så lille som muligt, da lagring og indlæsning af store filer kan have indflydelse på programmets funktionsmåde og ydeevne.

**Programbaggrund** – POS-enheden kan også bruge et billede som baggrund i hele programmet i stedet for den dækkende temafarve. Som det er tilfældet med logonbaggrunde, anbefales det at holde filstørrelsen så minimal som muligt.

## <a name="screen-layouts"></a>Skærmlayout
Konfigurationen af skærmlayoutet bestemmer handlingerne, indholdet og placeringen af UI-kontrolelementer på velkomstskærmen og transaktionsskærmen på POS-enheden. 

**Velkomstskærmen** – I de fleste tilfælde er velkomstskærmen den side, som brugere får vist, når de logger på POS-enheden første gang. Velkomstskærmen kan bestå af et brandingbillede og knapmatricer, der giver adgang til POS-handlinger. Typisk er operationer, der ikke er specifikke for den aktuelle transaktion, placeret her. 

**Transaktionsskærm** – Transaktionsskærmen er hovedskærmbilledet på POS-enheden behandling af salgstransaktioner og ordrer. Transaktionsskærmen kan konfigureres ved hjælp af skærmlayoutdesigneren. 

**Standardstartskærmbillede** – Nogle detailhandlere foretrækker, at kassereren navigere direkte til transaktionsskærmen, når de logger på. Indstillingen Standardstartskærmbillede giver brugerne mulighed for at angive dette for hvert skærmlayout.

### <a name="assignment"></a>Tilknytning

Skærmlayouts kan tildeles på butiks-, kasseapparats- eller brugerniveau. Brugertildelingen tilsidesætter kasseapparat og butikstildelingen, og kasseapparattildelingen tilsidesætter butikstildelingen. I et enkelt scenarie, hvor alle brugere skal bruge det samme layout uanset kasseapparat eller rolle, kan skærmlayoutet kun angives i butikken. I tilfælde, hvor visse kasseapparater eller brugere kræver specialiserede layouts, kan disse tildeles på tilsvarende måde.

### <a name="layout-sizes"></a>Layoutstørrelser

Denne funktion gælder kun for Dynamics 365 for Retail version 1611. Da skærmlayouts i mange tilfælde kan bruges på tværs af flere skærmstørrelser og -opløsninger, kan brugere konfigurere deres layout og indhold til hver. POS-programmet vælger automatisk den nærmeste layoutstørrelse til enheden på starttidspunktet. Et skærmlayout kan også indeholde konfigurationer for både fuldstændige og kompakte enheder. Denne konfiguration giver en bruger mulighed for at blive knyttet til et enkelt skærmlayout, der fungerer på tværs af forskellige størrelser og formfaktorer i butikken. 

**Moderne POS – Fuld** – Fulde layouts er typisk bedst til større skærme som pc-skærme eller tablets. Brugerne kan vælge, hvilke elementer i brugergrænsefladen der skal medtages, bestemme deres størrelse og placering, og konfigurere deres detaljerede egenskaber. Fulde layouts understøtter både stående og liggende konfigurationer. 

**Moderne POS - Kompakt** – Kompakte layouts er typisk bedst til telefoner eller små tablets. Designmulighederne er begrænsede på kompakte enheder. Brugerne kan konfigurere kolonnerne og felterne til kvitteringen og ruder med totaler.

### <a name="screen-layout-designer"></a>Designer for skærmlayout

Hver layoutstørrelse inden for et skærmlayout skal konfigureres ved hjælp af skærmlayoutdesigneren. Designeren giver brugerne mulighed for at angive og konfigurere elementer i brugergrænsefladen på transaktionsskærmbilledet. Skærmlayoutdesigneren bruger ClickOnce til at hente, installere og starte den nyeste version af programmet, hver gang brugeren åbner den. Sørg for at kontrollere browserkravene ved brug af ClickOnce, til nogle browsere, f.eks. Chrome, kræves udvidelser. 

**Numerisk tastatur** – Det numeriske tastatur er det vigtigste brugerinput i transaktionsskærmbilledet på POS-enheden. Det kan konfigureres til at vise hele tastaturet på skærmen, hvilket er ideelt til touchskærme, eller kun inputfeltet, som kan bruges sammen med et fysisk tastatur. Indstillingerne for numerisk tastatur er kun tilgængelige i det fulde layout. I Dynamics 365 for Retail version 1611 har kompakte layouts altid det fulde numeriske tastatur tilgængeligt fra transaktionsskærmbilledet.

**Panelet Totaler** – Panelet totaler kan konfigureres med én eller to kolonner til at vise felter, f.eks. linjeantal, rabatbeløb, gebyrer, subtotal og moms. I Dynamics 365 for Retail version 1611 understøtter kompakte layouts kun en enkelt totalkolonne. 

**Kvittering** – Kvitteringspanelet indeholder salgslinjerne, betalingslinjerne og leveringsoplysningerne for de produkter og tjenester, der er behandlet i POS-enheden. Brugerne kan angive kolonner, bredder og placering. I kompakte layouts i Dynamics 365 for Retail version 1611 kan du også konfigurere yderligere oplysninger, der vises i rækken under hovedlinjen. 

**Kundekort** – Kundekortet viser oplysninger om den kunde, der i øjeblikket er knyttet til transaktionen. Kundekortet kan konfigureres til at skjule eller få vist yderligere oplysninger. 

**Fanekontrolelement** – Fanekontrolelementet kan placeres på skærmlayoutet og andre kontrolelementer, f.eks. det numeriske tastatur, kundekortet eller knapmatricer kan placeres inde i fanen. Fanekontrolelementet er en beholder, der hjælper brugerne med at få plads til mere indhold på skærmen. Fanekontrolelementet er kun tilgængeligt for fulde layouts. 

**Billede** – Billedkontrolelementet kan bruges til at vise butikslogoet eller et andet branding-billede på transaktionsskærmbilledet. Billedkontrolelementet er kun tilgængeligt for fulde layouts. 

**Anbefalede produkter** – Hvis det er konfigureret for miljøet, viser kontrolelementet for anbefalede produkter produktforslag baseret på maskinel indlæring. Kontrolelementet for anbefalede produkter er kun tilgængeligt for fulde layouts i Dynamics 365 for Retail version 1611. **Brugerdefineret kontrolelement** – Det brugerdefinerede kontrolelement fungerer som en pladsholder i skærmlayoutet, der giver brugerne mulighed at reservere plads til brugerdefineret indhold. Det brugerdefinerede kontrolelement er kun tilgængeligt for fulde layouts.

<a name="see-also"></a>Se også
--------

[Installer layoutdesigneren til Retail POS](install-pos-layout-designer.md)




