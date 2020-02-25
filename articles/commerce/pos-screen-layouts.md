---
title: Skærmlayout til POS
description: Dette emne indeholder oplysninger om skærmlayouts til Dynamics 365 Commerce POS-oplevelserne.
author: jblucher
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 5bf7b3d20ff0b42eb9eaedf584b2a508c1307707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022050"
---
# <a name="screen-layouts-for-the-point-of-sale-pos"></a>Skærmlayout til POS

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om skærmlayouts til Dynamics 365 Commerce POS-oplevelserne.

Brugergrænsefladen i POS kan konfigureres ved hjælp af en kombination af visuelle profiler og skærmlayouts, der er tildelt butikker, kasseapparater og/eller brugere.

I følgende illustration vises forholdet mellem de forskellige enheder, der udgør de konfigurerbare elementer i POS-brugergrænsefladen.

![Enheder i POS-skærmlayout](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuel profil

Visuelle profiler tildeles til kasseapparater, og de angiver de visuelle elementer, der er kasseapparatspecifikke og delt på tværs af brugere. Alle brugere, der logger på kasseapparatet, får vist det samme tema og de samme farver og billeder.

![POS-velkomstskærm med lystema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![POS-transaktionsskærm med mørkt tema](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profilnummer** - Profilnummeret er den entydige identifikator for den visuelle profil.
- **Beskrivelse** - Du kan angive et beskrivende navn, der hjælper med til at identificere den korrekte profil til din situation.
- **Tema** - Du kan vælge mellem de lyse eller mørke programtemaer. Temaet påvirker skrifttypen og baggrundsfarverne i hele programmet.
- **Markeringsfarve** – Markeringsfarven bruges overalt på POS-enheden til at adskille eller fremhæve specifikke visuelle elementer, f.eks.felter, kommandoknapper eller hyperlinks. Disse elementer kræver typisk handling.
- **Overskriftsfarve** – Du kan konfigurere farven på sidehovedet for at opfylde forhandlerens krav til branding. Denne funktion er kun tilgængelig i Retail version 1611.
- **Vis dato/klokkeslæt** – Når aktiveret, vises dags dato og det aktuelle klokkeslæt i POS-hovedet.
- **Logonbaggrunde** – Du kan angive et baggrundsbillede til logonskærmen. Filstørrelsen for baggrundsbilleder bør være så lille som muligt, da lagring og indlæsning af store filer kan påvirke programmets funktionsmåde og ydeevne.
- **Programbaggrund** – Du kan angive et baggrundsbillede, der bruges i hele programmet i stedet for den dækkende temafarve. Hvad angår logonbaggrunde, bør filstørrelsen holdes så lav som muligt.

## <a name="screen-layouts"></a>Skærmlayout

Konfigurationer af skærmlayoutet bestemmer handlingerne, indholdet og placeringen af UI-kontrolelementer på velkomstskærmen og **transaktionsskærmen** på POS-enheden.

![Visning af POS-skærmlayout](../commerce/media/POS-Screen-Layout-View.png)

- **Velkomstskærm** – I de fleste tilfælde er velkomstskærmen den side, som brugere får vist, når de logger på POS-enheden første gang. Velkomstskærmen kan bestå af et brandingbillede og knapmatricer, der giver adgang til POS-handlinger. Typisk er operationer, der ikke er specifikke for den aktuelle transaktion, placeret på denne skærm.

    ![POS-velkomstskærm](../commerce/media/POS-Welcome-Screen.png)

- **Transaktionsskærm** – **Transaktionsskærmen** er hovedskærmbilledet på POS-enheden til behandling af salgstransaktioner og ordrer. Indholdet og layoutet er konfigureret ved hjælp af skærmlayoutdesigneren.

    ![POS-transaktionsskærm](../commerce/media/POS-Transaction-Screen.png)

- **Standardstartskærmbillede** – Nogle detailhandlere foretrækker, at kasserere går direkte til skærmen **Transaktion**, når de logger på. Indstillingen **Standardstartskærmbillede** giver dig mulighed for at angive det standardskærmbillede, der vises efter logon for hvert skærmlayout.

### <a name="assignment"></a>Tilknytning

Skærmlayouts kan tildeles på butiks-, kasseapparats- eller brugerniveau. Brugertildelingen tilsidesætter kasseapparats- og butikstildelingerne, og kasseapparattildelingen tilsidesætter butikstildelingen. I et enkelt scenarie, hvor alle brugere skal bruge det samme layout uanset kasseapparat eller rolle, kan skærmlayoutet kun angives i butiksniveau. I tilfælde, hvor specifikke kasseapparater eller brugere kræver specialiserede layouts, kan disse layouts tildeles.

### <a name="layout-sizes"></a>Layoutstørrelser

De fleste aspekter af POS-brugergrænsefladen kan tilpasses, og layoutet tilpasses og justeres automatisk afhængigt af skærmens størrelse og retning. Dog skal POS-skærmbilledet **Transaktion** konfigureres til alle skærmopløsninger, der forventes.

Ved start vælger POS-programmet automatisk den nærmeste layoutstørrelse, der er konfigureret til enheden. Et skærmlayout kan også indeholde konfigurationer til både stående og liggende retning og til enheder i både i fuld størrelse og kompakte. Derfor kan brugere blive knyttet til et enkelt skærmlayout, der fungerer på tværs af forskellige størrelser og formfaktorer, der bruges i butikken.

![POS-layoutstørrelser](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Navn** – Du kan angive et beskrivende navn til identifikation af skærmens størrelse.
- **Layouttype** – POS-programmet kan vise brugergrænsefladen i forskellige tilstande for at give den bedste brugeroplevelse på en given enhed.

    - **Modern POS – Fuld** – Fulde layouts er typisk bedst til større skærme som pc-skærme og tablets. Du kan vælge de elementer på brugergrænsefladen, der skal medtages, angive størrelsen på og placeringen af disse elementer og konfigurere deres detaljerede egenskaber. Fulde layouts understøtter både stående og liggende konfigurationer.
    - **Modern POS - Kompakt** – Kompakte layouts er typisk bedst til telefoner og små tablets. Designmulighederne er begrænsede på kompakte enheder. Du kan konfigurere kolonnerne og felterne til kvitteringen og paneler med totaler.

- **Bredde/højde** – Disse værdier repræsenterer den effektive skærmstørrelse i pixel, der forventes i layoutet. Husk, at nogle operativsystemer bruger skalering til skærme i høj opløsning.

> [!TIP]
> Du kan se hvilken størrelse layout, der kræves til POS-skærmen, ved at kigge på opløsningen i programmet. Start POS, og gå til **Indstillinger \> Sessionsoplysninger**. POS viser det skærmlayout, som er indlæst i øjeblikket, layoutstørrelsen og opløsningen i appvinduet.

![POS-layoutstørrelser](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Knapmatricer

For hver layoutstørrelse i et skærmlayout kan du konfigurere og tildele knapmatricer for POS-velkomstskærmbilledet og skærmbilledet **Transaktion**. Knapmatricer til velkomstskærmbilledet placeres automatisk fra venstre mod højre, fra det laveste nummer (velkomstskærmbillede 1) til det højeste nummer.

I fulde POS-layouts er placeringen af knapmatricer angivet i skærmens layoutdesigner.

I kompakte POS-layouts placeres knapmatricerne automatisk fra top mod bund, fra det laveste nummer (transaktionsskærmbillede 1) til det højeste nummer. De kan benyttes via menuen **Handlinger**.

![Knapmatricer til kompakt layout](../commerce/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Billeder

Du kan angive billeder, der skal medtages i POS-brugergrænsefladen for de enkelte layoutstørrelser i et skærmlayout. Til fulde POS-layouts kan der angives et enkelt billede for velkomstskærmbilledet. Dette billede vises som det første element til venstre i brugergrænsefladen. På skærmbilledet **Transaktion** kan billeder bruges som fanebilleder eller et logo. Kompakte POS-layouts bruger ikke disse billeder.

### <a name="screen-layout-designer"></a>Designer for skærmlayout

Skærmlayoutdesigneren giver dig mulighed for at konfigurere forskellige aspekter af POS-skærmbilledet **Transaktion** billede for hver layoutstørrelse i både stående og liggende tilstand og til både fulde og kompakte layouts. Skærmlayoutdesigneren bruger ClickOnce-installationsteknologien til at hente, installere og starte den nyeste version af programmet, hver gang brugeren åbner det. Du skal kontrollere browserkravene til ClickOnce. Nogle browsere, f.eks. Google Chrome, kræver udvidelser.

> [!IMPORTANT]
> Du skal konfigurere et skærmlayout for hvert layout størrelse, der er defineret, og som bruges af POS.

### <a name="full-layout-designer"></a>Fuld layoutdesigner

Den fulde layoutdesigner giver brugerne adgang til trække kontrolelementer i brugergrænsefladen til POS-skærmbilledet **Transaktion** og konfigurere indstillingerne for disse kontrolelementer.

![Fuld layoutdesigner til POS (liggende tilstand)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Importere layout/eksportere layout** – Du kan eksportere og importere POS-skærmlayoutdesign som XML-filer, så du nemt kan genbruge og dele dem på tværs af miljøer. Det er vigtigt, at du importerer layoutdesign til de korrekte layoutstørrelser. Ellers placeres brugergrænsefladeelementerne muligvis ikke korrekt på skærmen.
- **Liggende/stående** – Hvis POS-enheden, giver brugerne mulighed for at skifte mellem stående og liggende retning, skal du definere et skærmlayout for hver tilstand. POS-enheden registrerer automatisk skærmrotation og viser det korrekte layout.
- **Layoutgitteret** – POS-layoutdesigneren bruger et gitter med 4 pixel. Brugergrænsefladen "fastgøres til" gitteret for at hjælpe dig med at justere indholdet korrekt.
- **Designerzoom** – du kan zoome designvisningen ind og ud for bedre at kunne se indholdet på POS-skærmen. Denne funktion er nyttig, når skærmopløsningen på POS-enheden afviger betydeligt fra opløsningen på den skærm, der bruges i designeren.
- **Vis/Skjul navigationslinjen** – Til fulde POS-layouts kan du vælge, om den venstre navigationslinje skal være synlig på skærmbilledet **Transaktion**. Denne funktion er nyttig til visninger med en lavere opløsning. Du kan angive synligheden ved at højreklikke på navigationslinjen i designeren og markere eller fjerne markeringen af afkrydsningsfeltet **Altid synlig**. Hvis navigationslinjen er skjult, har POS-brugere stadig adgang til den ved hjælp af menuen øverst til venstre.

    ![Vis/skjul navigationslinje](../commerce/media/Navigation-Bar.PNG)

- **POS-kontrolelementer** – POS-layoutdesigneren understøtter følgende kontrolelementer. Du kan konfigurere mange kontrolelementer ved at højreklikke og bruge genvejsmenuen.

    ![POS-brugergrænsefladekontrolelementer](../commerce/media/POS-UI-Controls.png)

    - **Numerisk tastatur** – Det numeriske tastatur er den vigtigste enhed til brugerinput i POS-skærmbilledet **Transaktion**. Du kan konfigurere kontrolelementet, så hele det numeriske tastatur vises. Denne indstilling er velegnet til enheder med berøringsskærm. Du kan også konfigurere den, så kun inputfeltet vises. I så fald bruges et fysisk tastatur til input. Indstillingerne for numerisk tastatur er kun tilgængelige i fulde layouts. For kompakte layouts vises det fulde numeriske tastatur altid på skærmbilledet **Transaktion**.
    - **Panelet Totaler** – Du kan konfigurere panelet totaler med enten én eller to kolonner til at vise værdier, f.eks. linjeantal, rabatbeløb, gebyrer, subtotal og moms. Kompakte layouts understøtter kun en enkelt kolonne.
    - **Kvitteringspanel** – Kvitteringspanelet indeholder salgslinjerne, betalingslinjerne og leveringsoplysningerne for de produkter og tjenester, der behandles i POS-enheden. Du kan angive kolonner, bredder og placering. I kompakte layouts kan du også konfigurere yderligere oplysninger, der vises i rækken under hovedlinjen.
    - **Kundekort** – Kundekortet viser oplysninger om den kunde, der er knyttet til den aktuelle transaktion. Du kan konfigurere kundekortet til at skjule eller få vist yderligere oplysninger.
    - **Fanekontrolelement** – Du kan tilføje fanekontrolelementet til et skærmlayout og derefter anbringe andre kontrolelementer, f.eks. det numeriske tastatur, kundekortet eller knapmatricer i det. Fanekontrolelementet er en beholder, der hjælper dig med at få plads til mere indhold på skærmen. Fanekontrolelementet er kun tilgængeligt for fulde layouts.
    - **Billede** – Du kan bruge billedkontrolelementet til at vise butikslogoet eller et andet brandingbillede på skærmbilledet **Transaktion**. Billedkontrolelementet er kun tilgængeligt for fulde layouts.
    - **Anbefalede produkter** – Hvis kontrolelementet anbefalede produkter er konfigureret for miljøet, viser det produktforslag baseret på maskinel indlæring.
    - **Brugerdefineret kontrolelement** – Det brugerdefinerede kontrolelement fungerer som en pladsholder i skærmlayoutet, og giver dig mulighed at reservere plads til brugerdefineret indhold. Det brugerdefinerede kontrolelement er kun tilgængeligt for fulde layouts.

### <a name="compact-layout-designer"></a>Designer til kompakt layout

Som designeren til fuld layout giver designeren til kompakt layout dig mulighed for at konfigurere POS-skærmlayoutet for telefoner og små tablets. Men i dette tilfælde er selve layoutet dog fast. Du kan konfigurere kontrolelementerne i layoutet ved at højreklikke og bruge genvejsmenuen. Du kan dog ikke bruge træk og slip-handlinger til yderligere indhold.

![Designer til kompakt layout](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Designer til knapmatrix

Designeren til knapmatrix giver dig mulighed for at konfigurere knapmatricer, der kan bruges på POS-velkomstskærmbilledet og skærmbilledet **Transaktion** til både fulde og kompakte layouts. Den samme knapmatrix kan bruges på tværs af layouts og layouttyper. Ligesom skærmlayoutdesigneren bruger designeren til knapmatrix ClickOnce-installationsteknologien til at hente, installere og starte den nyeste version af programmet, hver gang brugeren åbner det. Du skal kontrollere browserkravene til ClickOnce. Nogle browsere, f.eks. Google Chrome, kræver udvidelser.

![Designer til knapmatrix](../commerce/media/Button-Grid-Designer.png)

- **Knappen Ny** – Klik for at tilføje en ny knap til knapmatrixen. Nye knapper vises som standard i øverste venstre hjørne af gitteret. Men du kan arrangere knapper ved at trække dem i layoutet.

    > [!IMPORTANT]
    > Indholdet i knapmatricen kan overlappe hinanden. Når du arrangerer knapper, skal du sikre dig, at de ikke skjuler andre knapper.

- **Nyt design** – Klik for at konfigurere et layout til knapmatricen automatisk ved at angive antallet af knapper pr. række og kolonne.
- **Knapegenskaber** – Du kan konfigurere knapegenskaber ved at højreklikke på knappen og bruge genvejsmenuen.

    > [!IMPORTANT]
    > Nogle indstillinger af knapmatrix gælder kun for Enterprise POS, ikke for Modern POS eller Cloud POS.

    ![Knapegenskaber for knapmatrix](../commerce/media/Button-grid-button-properties.png)

    - **Handling** – På listen over relevante POS-handlinger skal du vælge den handling, der startes, når der klikkes på knappen i POS.

        Du kan se listen over understøttede POS-handlinger under [Online og offline POS-handlinger](pos-operations.md).

    - **Handlingsparametre** – Nogle POS-handlinger bruger flere parametre, når de aktiveres. For handlingen Tilføj produkt kan brugerne f.eks. angive det produkt, der skal tilføjes.
    - **Knaptekst** – Angiv den tekst, der vises på knappen i POS.
    - **Skjul tekst til knap** – Brug dette afkrydsningsfelt for at skjule eller vise teksten til knappen. Teksten til knappen er ofte skjult på små knapper, der kun viser et ikon.
    - **Værktøjstip** – Angiv yderligere hjælpetekst, der vises, når brugerne flytter musen over knappen.
    - **Størrelse på kolonner/størrelse på rækker** – Du kan angive højden og bredden på knappen.

        ![POS-knapstørrelser i rækker og kolonner](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Brugerdefineret skrifttype** – Når du markerer afkrydsningsfeltet **Aktivér brugerdefineret skrifttype til POS**, kan du angive en anden skrifttype end standardsystemskrifttypen for POS.
    - **Brugerdefineret tema** – Som standard bruger POS-knapper markeringsfarven fra den visuelle profil. Når du markerer afkrydsningsfeltet **Brug brugerdefineret tema**, kan du angive flere farver.

        > [!NOTE]
        > Modern POS og Cloud POS bruger kun værdierne **Baggrundsfarve** og **Skriftfarve**.

    - **Knapbillede** – Knapper kan indeholde billeder eller ikoner. Vælg mellem de tilgængelige billeder, der er angivet i **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> Billeder**.

![Eksempel knapmatrix i POS](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Installere layoutdesigneren til Retail POS](install-pos-layout-designer.md)
