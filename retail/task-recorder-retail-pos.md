---
title: "Arbejdsrutineoptager og Hjælp til POS"
description: Dette emne beskriver, hvordan du bruger Arbejdsrutineoptager i Retail Modern POS og Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 007a7e8a34f3f5a2d0d18eb3955822a8fd8bdd0a
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="task-recorder-and-help-for-pos"></a>Arbejdsrutineoptager og Hjælp til POS

Dette emne beskriver, hvordan du bruger Arbejdsrutineoptager i Retail Modern POS og Cloud POS.

<a name="overview"></a>Overblik
--------

Arbejdsrutineoptager i Retail Modern POS eller Cloud POS er en ny løsning, der er bygget med fokus på høj tilgængelighed. Den indeholder en fleksibel API (brugergrænseflade til program) til udvidelse og problemfri integration for forbrugere af registreringer af forretningsprocesser. Derudover er integrationen af Arbejdsrutineoptager med værktøjet Forretningsprocesmodel (BPM) i Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) blevet overført. Brugerne kan derfor fortsætte med at producere omfattende forretningsprocesdiagrammer fra registreringer, så de kan analysere og designe deres programmer.

## <a name="architecture"></a>Arkitektur
Arbejdsrutineoptager kan registrere brugerhandlinger på klienten med stor nøjagtighed. Hvert kontrolelement er udstyret til at underrette Arbejdsrutineoptager om udførelsen af en brugerhandling. Kontrolelementet underretter Arbejdsrutineoptager om, at der opstod en hændelse, og overfører alle relevante oplysninger om den tilsvarende brugerhandling i realtid. Fra disse oplysninger kan Arbejdsrutineoptager hente typen af brugerhandling (f.eks. et klik på en knap, indtastning af en værdi eller navigation) og alle data, der er relateret til brugerhandlingen (f.eks. værdien og typen af inputdata, formularkontekst eller postkontekst). Arbejdsrutineoptager bevarer oplysningerne med tilstrækkelige detaljer til at sikre, at en afspilning af registreringen kan udføre de registrerede handlinger, nøjagtigt som brugeren har udført dem. (Afspilningsfunktionen er endnu ikke implementeret på Retail Modern POS eller Cloud POS).

## <a name="basic-configuration"></a>Basiskonfiguration
Følg disse trin for at aktivere opgaveregistrering i POS.

1.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**.
2.  Klik på kasseapparatet for at aktivere opgaveregistrering.
3.  Under fanen **Kasseapparat** på oversigtspanelet **Generelt** skal du angive indstillingen **Aktivér opgaveregistrering** til **Ja**.
4.  Klik på **Gem**.
5.  Gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
6.  Vælg jobbet **Kasseapparater (1090)**, og klik derefter på knappen **Kør nu**.

## <a name="create-a-recording"></a>Opret en registrering
Følg disse trin for at oprette en ny registrering ved hjælp af Arbejdsrutineoptager.

1.  Start Retail Modern POS eller Cloud POS, og log på.
2.  På siden **Indstillinger** i afsnittet **Arbejdsrutineoptager** skal du klikke på **Åbn Arbejdsrutineoptager**. Ruden **Arbejdsrutineoptager** vises. Du kan klikke på knappen **Luk** (**X**) i øverste højre hjørne for at lukke ruden **Arbejdsrutineoptager**, før du starter en ny registrering. Gentag trin 2 for at åbne ruden igen.
[![Ruden Arbejdsrutineoptager](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Angiv et navn og en beskrivelse for registreringen, og klik derefter på **Start**. Registreringssessionen starter, så snart du klikker på **Start**.

**Bemærk:** Hvis du klikker på knappen **Luk** (**X**) i øverste højre hjørne, mens registreringen er i gang, lukkes ruden **Arbejdsrutineoptager**, men registreringssessionen afsluttes ikke. Klik på **Hjælp** (spørgsmålstegn) øverst på skærmen for at åbne ruden Arbejdsrutineoptager igen. 

[![Spørgsmålstegn](./media/help.jpg)](./media/help.jpg)

4.  Når du klikker på **Start**, går Arbejdsrutineoptager i registreringstilstand. Ruden **Arbejdsrutineoptager** viser oplysninger og kontrolelementer, der vedrører registreringsprocessen.
5.  Udfør de handlinger, du vil udføre i Retail Modern POS- eller Cloud POS-brugergrænsefladen (UI).
6.  Klik på **Stop** for at stoppe registreringssessionen.

## <a name="download-options"></a>Downloadindstillinger
Når du har afsluttet registreringssessionen, vises flere indstillinger, så du kan hente din registrering. 
[![Downloadindstillinger](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Gem til denne pc

Du kan bruge registreringspakken til at afspille en opgaveguide, vedligeholde registreringen eller redigere anmærkningerne i registreringen. (Denne funktion er endnu ikke implementeret i Retail Modern POS eller Cloud POS).

### <a name="export-as-word-document"></a>Eksportér som Word-dokument

Du kan gemme registreringen som et Microsoft Word-dokument. Dokumentet indeholder de registrerede trin og de skærmbilleder, der blev hentet.

### <a name="save-as-developer-recording"></a>Gem som udviklerregistrering

Den rå registreringsfil er nyttig i udviklerscenarier, f.eks. oprettelse af testkode. (Denne funktion er ikke implementeret endnu).

## <a name="recording-controls"></a>Registreringskontrolelementer
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Registreringskontrolelementer](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Stop

Klik på **Stop** for at stoppe registreringssessionen. Bemærk, at du ikke kan genstarte en session, når du har afsluttet den. Du skal derfor sørge for, at registreringen er fuldført, før du afslutter den.

### <a name="pause"></a>Afbryd midlertidigt

Klik på **Afbryd midlertidigt** for at stoppe registreringssessionen midlertidigt og fortsætte med handlingen. Trin, du udfører, efter at du har klikket på **Afbryd midlertidigt**, registreres ikke.

### <a name="continue"></a>Fortsæt

Hvis du vil genoptage registreringssessionen, når du har afbrudt den midlertidigt, skal du klikke på **Fortsæt**.

### <a name="capture-screenshots"></a>Tag skærmbilleder

Arbejdsrutineoptager kan hente skærmbilleder af brugergrænsefladen i Retail Modern POS i takt med, at du registrerer en forretningsproces. Arbejdsrutineoptager bruger skærmbillederne, hvis du henter registreringen som et Word-dokument. Hvis du vil slå funktionen til hentning af skærmbilleder til, skal du angive indstillingen **Tag skærmbilleder** til **Ja**. 

#### <a name="note"></a>Bemærk!
> Funktionen til hentning af skærmbilleder understøttes ikke i Cloud POS.

### <a name="start-task-and-end-task"></a>Start opgave, og Afslut opgave

Du kan angive begyndelsen og slutningen af et sæt grupperede trin ved hjælp af knapperne **Start opgave** og **Afslut** **opgave**. Klik på **Start opgave** for at tilføje et "Start opgave"-trin, og udfør derefter de trin, der skal medtages i gruppen. Når du er færdig med at udføre trinnene for gruppen, skal du klikke på **Afslut opgave**. Opgaver hjælper dig med at organisere dine procedurer. Opgaver kan være indlejret i andre opgaver. På denne måde kan du bedre organisere meget lange og komplekse forretningsprocesser.

## <a name="adding-annotations"></a>Tilføj anmærkninger
En anmærkning er ekstra tekst, du føjer til et trin i en registrering. Du kan f.eks. bruge anmærkninger til at give brugeren mere kontekst eller flere instruktioner. Du kan tilføje anmærkninger før eller efter et trin. Du kan tilføje en anmærkning til ethvert trin ved at klikke på knappen **Rediger** (blyantssymbol) til højre for trinnet. 

[![Knappen Rediger til et trin](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekst og notater

Du kan bruge felterne **Tekster** og **Noter** til at tilføje tekst, der skal knyttes til et trin i en opgaveguide.
[![Felterne Tekster og Noter](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Tekst

Tekst, du har angivet i feltet **Tekst**, vises *over* teksten til trinnet i opgaveguiden. Denne placering er velegnet til tekst, du ønsker, at brugeren skal læse, før han eller hun fuldfører trinnet.

#### <a name="notes"></a>Notater

Tekst, du har angivet i feltet **Notater**, vises *under* teksten til trinnet i opgaveguiden. For at læse noteteksten skal brugeren udvide teksten til trinnet i pop op-vinduet. Denne placering er velegnet til valgfrit læsemateriale eller andre oplysninger, der kan være nyttige for brugeren, men som ikke er nødvendige for brugeren for at fuldføre handlingen.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Hjælp i Retail Modern POS og Cloud POS
For at få vist dine egne brugerdefinerede opgaveregistreringer i ruden Hjælp i Retail Modern POS og Cloud POS så de kan afspilles som opgaveguider eller vises som tekst, skal du gemme opgaveregistreringerne i dit eget BPM-bibliotek og derefter opdatere dine systemparametre til Hjælp til at pege på BPM-biblioteket. Vil du have mere hjælp, kan du se [Forbindelse til hjælpesystemet.](/dynamics365/unified-operations/dev-itpro/get-started/help-connect) Hjælpen til Retail Modern POS og Cloud POS søger i LCS i realtid. Den søger på tværs af alle BPM-biblioteker, der er valgt i Microsoft Dynamics 365 for Retail Hjælp-systemparametrene og viser de relevante resultater. For at få adgang til menuen **Hjælp** skal du klikke på knappen **Hjælp** (spørgsmålstegn) øverst på skærmen, og derefter skal du skrive navnet på din proces i søgefeltet og trykke på søgeknappen. 

[![Knappen Hjælp](./media/help.jpg)](./media/help.jpg) 

Når du klikker på en opgaveguide i søgeresultaterne, kan du enten få vist trinnene som et emne i Hjælp eller eksportere trinnene til et Word-dokument. 
#### <a name="note"></a>Bemærk!
> Hjælp i Retail Modern POS og Cloud POS viser ikke opgavevejledninger i henhold til, hvilken form du er, eller operation, du foretager. Du skal skrive procesnavnet i søgefeltet og derefter klikke på **Søg**.


