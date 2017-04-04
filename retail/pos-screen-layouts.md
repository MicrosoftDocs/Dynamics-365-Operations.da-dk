---
title: "Konfigurere skærmlayout for POS"
description: "Dette emne indeholder oplysninger om skærmlayout for Microsoft Dynamics 365 for operationer – Retail punkt salg (POS) oplevelser."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurere skærmlayout for POS

Dette emne indeholder oplysninger om skærmlayout for Microsoft Dynamics 365 for operationer – Retail punkt salg (POS) oplevelser.

Microsoft Dynamics 365 for operationer – Retail punkt i brugergrænsefladen for salg (POS) kan konfigureres ved hjælp af en kombination af visuelle profiler og skærmlayout, der er tildelt til butikker, kasseapparater og/eller brugere.

## <a name="visual-profile"></a>Visuel profil
Visuelle profiler, der er tildelt til registre og bruges til at angive de visuelle elementer, der er registeret-specifikke og delt på tværs af brugere. Alle brugere, der logger på journalen har det samme tema, farver og billeder. **Profil nummer** -profil antallet er entydig identifier for den visuelle profil. **Beskrivelse** -beskrivelsen, kan du angive et beskrivende navn, der hjælper med at identificere den korrekte profil for din situation. **Tema** -brugere kan vælge mellem lys eller mørk program temaer. Disse indstillinger påvirker skrifttypefarven og baggrundsfarven farver i hele programmet. **Markeringsfarve farve** -fremhævelsesfarve bruges til at adskille eller fremhæve visse visuelle elementer som fliser, kommandoknapper eller hyperlinks i POS. Disse elementer er typisk gennemførlige. **Hovedet farve** -header-farve gør det muligt for brugeren at konfigurere farven i sidehovedet til at imødekomme mærkning af forhandleren. Denne funktion er kun tilgængelig i Dynamics 365 for operationer version 1611 opdager. **Logon baggrunde** -brugere kan angive et baggrundsbillede til logonskærmen. Filstørrelsen for baggrundsbilleder bør holdes så små som muligt, som lagring og indlæsning af store filer kan have indflydelse på programmets funktionsmåde og ydeevne. **Programmet baggrund** -The POS kan også bruge et billede som baggrund i hele programmet i stedet for fast tema-farver. Som det er tilfældet med logon baggrunde, kan det anbefales at holde filstørrelsen så minimal som muligt.

## <a name="screen-layouts"></a>Skærmlayout
Layout skærmkonfigurationen bestemmer de handlinger, indhold og placering af UI kontrol i skærmbilledet Velkommen til POS og transaktion skærmen. ** Velkomstskærmen **-i de fleste tilfælde velkomstsiden er den side, som brugere får vist, når de først logge på POS. Velkomstskærmen kan bestå af en mærkning billeder og knapmatricer, der giver adgang til POS-handlinger. Typisk er operationer, ikke der er specifikke for den aktuelle postering placeret her. **Transaktionen skærmen** -transaktionen skærmen er hovedskærmbilledet i POS til behandling af salg og ordrer. Skærmbilledet transaktion kan konfigureres ved hjælp af skærmen layoutdesigneren. **Standard-startskærmbilledet** -nogle detailhandlere foretrækker kassereren navigere direkte til skærmen transaktion efter logføring i. Indstillingen start skærmen, kan brugerne angive dette for hver skærmlayout.

### <a name="assignment"></a>Tilknytning

Skærmlayout kan tildeles på niveauet for butikken, register eller bruger. Tildelingen bruger tilsidesætter registret og gemme tildelingen og register tildeling tilsidesættelser butik tildelingen. I en simpel scenario, hvor alle brugere skal bruge det samme layout uanset register eller rolle, kan der oprettes skærmlayoutet kun i butikken. I tilfælde, hvor visse registre eller brugere kræver specialiseret layout, kan de tildeles korrekt.

### <a name="layout-sizes"></a>Layoutstørrelser

Denne funktion gælder kun for Dynamics 365 for operationer version 1611 opdager. Da i mange tilfælde er det skærmlayout, der kan bruges på tværs af flere skærmstørrelser og opløsninger, kan brugere konfigurere deres layout og indhold for hver. POS-programmet vælger automatisk den nærmeste layout størrelse til enheden på tidspunktet for start. Et skærmlayout kan også indeholde konfigurationer for både fuld og kompakte enheder. Denne konfiguration giver en bruger tildeles til et enkelt skærmlayout, der fungerer på tværs af forskellige størrelser og formfaktorer i lageret. **Fuld moderne POS -** -fulde layout bruges typisk bedst til større skærme som PC-skærme eller tablets. Brugerne kan vælge, hvilke elementer i Brugergrænsefladen til at medtage, bestemmer deres størrelse og placering, og konfigurere deres detaljerede egenskaber. Fuld layout understøtter konfigurationer med både stående og liggende. **Kompakt moderne POS -** -kompakt layout bruges typisk bedst til telefoner eller små tablets. Designmuligheder er begrænset til kompakte enheder. Brugerne kan konfigurere kolonnerne og felterne for kvittering og totaler ruderne.

### <a name="screen-layout-designer"></a>Designer for skærmlayout

Hver layout størrelse inden for et skærmlayout skal konfigureres ved hjælp af skærmen layoutdesigneren. Designeren kan brugerne angive og konfigurere brugergrænsefladeelementer på skærmbilledet transaktion. Layoutdesigneren skærmen bruger ClickOnce til at hente, installere og starte den nyeste version af programmet, hver gang brugeren åbner den. Sørg for at kontrollere krav til browser til at bruge ClickOnce-nogle browsere, såsom Chrome, der kræver serverudvidelser. **Numerisk tastatur** -det numeriske tastatur er det vigtigste brugerinput i skærmbilledet transaktion på POS. Det kan konfigureres til at vise hele skærmen, pad, som er ideel til berøringsskærme, eller kun det inputfelt, som kan bruges med et fysisk tastatur. Indstillinger for tastatur er tilgængelige i den fuldstændige layout. I Dynamics 365 for operationer version 1611 opdager har kompakt layout altid den fuld numerisk tastatur, der er tilgængelige fra skærmbilledet transaktion. **Totaler panelet** - panelet totaler kan konfigureres på én eller to kolonner til at vise felter som linje count, rabatbeløb, gebyrer, subtotal og skat. I Dynamics 365 for operationer version 1611 opdager understøtter kompakt layout kun en enkelt totaler kolonne. **Modtagelsen** -** ** panelet modtagelsen indeholder de salgslinjer, betalingslinjer og leveringsoplysninger for de produkter og tjenester, der er behandlet i POS. Brugerne kan angive kolonner, bredder og placering. Du kan også konfigurere yderligere oplysninger, som vises i rækken under linjen main i kompakt layout i Dynamics 365 for operationer version 1611 opdager. **Debitorkortet** - kort viser oplysninger om den kunde hører til den kunde, der i øjeblikket er knyttet til posteringen. Kundekortet kan konfigureres til at skjule eller få vist yderligere oplysninger. **Faneblad** - fanebladet kan placeres på skærmlayoutet og andre kontrolelementer, som det numeriske tastatur, debitorkortet eller knapmatricer kan placeres inde i fanen. Fanestyringsfunktionen er en beholder, der hjælper brugerne med plads til mere indhold på skærmen. Fanestyringsfunktionen er kun tilgængelig for hele layout. ** Billede **-billedkontrolelementet kan bruges til at vise et logo eller andet mærkning billede på skærmen for posteringen. Billedkontrolelementet er kun tilgængelig for hele layout. **Anbefalede produkter** - Hvis der er konfigureret for miljøet, anbefalede produkter kontrol viser produktforslag baseret på machine learning. Anbefalede produkter-kontrol er kun tilgængelig for fuld layout i Dynamics 365 for operationer version 1611 opdager. ** Brugerdefinerede kontrolelement **-det brugerdefinerede kontrolelement fungerer som en pladsholder i skærmlayout til giver brugerne mulighed at reservere plads til brugerdefineret indhold. Det brugerdefinerede kontrolelement er kun tilgængelig for hele layout.

<a name="see-also"></a>Se også
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


