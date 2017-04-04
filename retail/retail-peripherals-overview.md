---
title: Oversigt over Retail eksterne enheder
description: "Dette emne beskriver de begreber, der er relateret til retail enheder. Den beskriver de forskellige måder, at eksterne enheder kan forbindes til salgsstedet (POS) og komponenterne, der er ansvarlig for forbindelsen med POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Oversigt over Retail eksterne enheder

Dette emne beskriver de begreber, der er relateret til retail enheder. Den beskriver de forskellige måder, at eksterne enheder kan forbindes til salgsstedet (POS) og komponenterne, der er ansvarlig for forbindelsen med POS.

<a name="concepts"></a>Begreber
--------

### <a name="pos-registers"></a>Kasseapparater

Navigation: Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**registrerer**. Formålet med salg (POS) register er en enhed, der bruges til at definere egenskaberne for en bestemt forekomst af POS. Disse kendetegn omfatter hardwareprofil eller opsætningen af retail-enheder, der skal bruges på kasseapparatet, butikken, der er tilknyttet registeret og den visuelle oplevelse for den bruger, der logger på dette register.

### <a name="devices"></a>Enheder

Navigation: Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**enheder**. En enhed repræsenterer en fysisk forekomst af en enhed, der er knyttet til et POS-kasseapparat. Når der oprettes en enhed, der er knyttet til en POS register. Enheden registrerer oplysninger om, hvornår et POS-kasseapparat aktiveres, den klienttype, som benyttes, og den programpakke, der er blevet installeret på en bestemt enhed. Enheder kan knyttes til følgende programtyper: moderne detail-POS, Retail POS sky, moderne detail-POS – Windows Phone, moderne detail-POS – Android og moderne detail-POS – iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Moderne POS er POS-program til Microsoft Windows. Det kan anvendes på operativsystemerne Windows 10 (OSs).

### <a name="cloud-pos"></a>Cloud POS

Sky POS er en browser-baseret version af moderne POS-programmet, der kan åbnes i en webbrowser.

### <a name="modern-pos-for-ios"></a>Moderne POS til iOS

Moderne POS for iOS er en iOS-baseret version af moderne POS-programmet, der kan implementeres på iOS-enheder.

### <a name="modern-pos-for-android"></a>Moderne POS til Android

Moderne POS for Android er en Android-baseret version af moderne POS-programmet, der kan implementeres på Android-enheder.

### <a name="pos-peripherals"></a>POS-tilbehør

POS-enheder er enheder, der udtrykkeligt understøttes for POS-funktioner. Disse enheder er typisk opdelt i bestemte klasser. Yderligere oplysninger om disse klasser, i afsnittet "Enhedsklasser" i dette emne.

### <a name="hardware-station"></a>Hardwarestation

Navigation: Klik på **detail- og commerce**&gt;**kanaler**&gt;**Retail butikker**&gt;**alle retail butikkerne**. Vælg en butik, og klik derefter i oversigtspanelet **Hardwarestationer**. Den **Hardware station** er en kanal niveau indstilling, der bruges til at definere forekomster, hvor den ydre retail-logik skal implementeres. Denne indstilling på niveauet for kanal bruges til at bestemme karakteristika for hardware-station. Den bruges også til listen over hardware-stationer, der er tilgængelige for en moderne POS forekomst i et givet lager. Hardware-station er indbygget i moderne POS-programmet til Windows. Hardware-station kan også installeres uafhængigt som et enkeltstående program i Microsoft Internet Information Services (IIS). I så fald kan opnås via et netværk.

### <a name="hardware-profile"></a>Hardwareprofil

Navigation: Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**. Hardwareprofilen er en liste over enheder, der er konfigureret til et POS-kasseapparat eller en hardware-station. Hardwareprofilen, der kan knyttes direkte til et POS-kasseapparat eller en hardware-station.

## <a name="devices-classes"></a>Enheder-klasser
POS-enheder er typisk opdelt i klasser. Dette afsnit beskriver og giver et overblik over de enheder, der understøtter moderne POS.

### <a name="printer"></a>Printer

-Printere byder på traditionelle POS modtagelsen printere og helsides printere. Printeren understøttes via Object Linking and Embedding for Retail POS (OPOS) og Microsoft Windows driver-grænseflader. Op til to printere kan bruges på samme tid. Denne funktion understøtter scenarier, hvor cash-and-carry kundekvitteringer udskrives på modtagelsen printere, hvorimod kundeordrer, der udfører yderligere oplysninger, der skal udskrives på en helsides printer. Modtagelsen printere kan direkte tilsluttet en computer via USB, forbindelse til et netværk via Ethernet eller forbindelse via Bluetooth.

### <a name="scanner"></a>Scanner

Op til to stregkode kan scannere bruges på samme tid. Denne funktion understøtter scenarier, hvor en scanner, som er mere mobile for at scanne store eller tunge varer, hvorimod en fast integreret scanner bruges til de fleste kopimaskiner til standardformater-elementer til hurtigere udlevering gange. Scannere kan understøttes via OPOS, Universal Windows Platform (UWP) eller tastatur kile grænseflader. USB- eller Bluetooth kan bruges til at tilslutte en scanner til en computer.

### <a name="msr"></a>Magnetstribelæser

Én USB-Magnetstriben læser (MSR) kan konfigureres ved hjælp af OPOS-drivere. Hvis du vil bruge en enkeltstående MSR til elektronisk overførsel (EFT) betalingstransaktioner, skal MSR administreres af en forbindelse til betaling. Enkeltstående MSRs kan bruges til loyalitet over for debitorposten, medarbejder-logon og gave kort post, uafhængigt af betalingsconnector.

### <a name="cash-drawer"></a>Kassen

To pengeskuffer kan støttes pr. hardwareprofil. Denne funktion gør det muligt for to aktive Skift pr. kasseapparat skal være tilgængelige på samme tid. I tilfælde af en delt Skift, eller en pengeskuffen, der bruges af flere mobile POS-enheder på samme tid, tillades kun ét pengeskuffen pr. hardwareprofil. Kontant skuffer kan direkte tilsluttet en computer via USB, forbindelse til et netværk eller tilsluttet en kvittering printer via en RJ12-grænseflade. I nogle tilfælde kan pengeskuffer også forbindes via Bluetooth.

### <a name="line-display"></a>Linjevisning

Linjen viser bruges til at vise produkter, transaktion saldi og andre nyttige oplysninger til kunden under en transaktion. En visning kan være tilsluttet til computeren via USB med OPOS-drivere.

### <a name="signature-capture"></a>Signaturhentning

Hentningsenheder signatur kan være tilsluttet direkte til en computer via USB med OPOS-drivere. Når registrering af signatur er konfigureret, bliver kunden bedt om at logge på enheden. Når signaturen er angivet, vises til kassereren om accept.

### <a name="scale"></a>Skaler

Skalaer kan tilsluttes computeren via USP ved hjælp af OPOS-drivere. Når et produkt, der er markeret som et produkt af "Weighed" føjes til en transaktion, POS læser vægten fra vægt, føjer produktet til transaktionen og bruger det antal, der leveres af skalaen.

### <a name="pin-pad"></a>Pinkodetastatur

Personligt id-nummer (PIN) pads understøttes via OPOS, men de skal administreres via et stik til betaling.

### <a name="secondary-display"></a>Sekundær skærm

Når en sekundær skærm er konfigureret, bruges nummer 2 Windows display til at vise grundlæggende oplysninger. Formålet med den sekundære skærm er at understøtte uafhængige softwareproducenter udvidelse, fordi ud af boksen sekundær skærm ikke kan konfigureres og viser begrænset indhold.

### <a name="payment-device"></a>Betalingsenhed

Understøttelse af enheder for betalingen er implementeret via betalingsconnector. Betaling-enheder kan udføre en eller flere af de funktioner, der giver andre enhedsklasser. For eksempel kan en betalingsenhed fungerer som en MSR/kortlæser, linjevisningen, signatur hentningsenhed eller PIN-tastatur. Understøttelse af betaling enheder gennemføres uafhængigt af den selvstændige enhed support, der leveres til andre enheder, der er inkluderet i hardwareprofilen.

## <a name="supported-interfaces"></a>Understøttede grænseflader
### <a name="opos"></a>OPOS

For at sikre, at det største udvalg af enheder kan bruges sammen med Microsoft Dynamics 365 for operationer - Detail, OLE for POS branchestandard er den primære retail ydre enhed platform, der understøttes i Microsoft Dynamics 365 for operationer – Retail. OLE for POS-standarden blev produceret af det nationale Retail Federation (NRF), som fastlægger branchestandarden kommunikationsprotokoller til retail ydre enheder. OPOS er et alment vedtagne implementering af OLE for POS-standarden. Det blev udviklet i midten 1990s og er blevet opdateret flere gange siden da. OPOS indeholder en device driverarkitektur, der sikrer nem integration af POS-hardware med Windows-baserede POS-systemer. OPOS styrer handle kommunikation mellem kompatibel hardware og software på POS. En OPOS-styring består af to dele:

-   **Objektet** – control-objekt af en enhedsklasse (f.eks. linje viser) indeholder grænsefladen til programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) indeholder et sæt standarder for kontrol OPOS-objekter, der er kendt som de almindelige kontrol-objekter (CCOs). CCOs, der bruges til at teste komponenten af Microsoft Dynamics 365 for operationer – Retail POS. Derfor afprøvning hjælper med at sikre, at, hvis Microsoft Dynamics 365 for operationer – Retail understøtter en enhedsklasse gennem OPOS, mange enhedstyper kan støttes, forudsat at producenten giver et serviceobjekt, der er bygget til OPOS. Du behøver ikke at udtrykkeligt teste hver enhedstype.
-   **Serviceobjekt** – serviceobjektet kan bruges til kommunikation mellem objektet (CCO) og enheden. Serviceobjekt til en enhed leveres typisk af producenten af enheden. Dog i nogle tilfælde kan være det nødvendigt at hente serviceobjektet fra producentens websted. Et nyere serviceobjekt kan eksempelvis være tilgængelige. Adressen på producentens websted finder du dokumentationen til hardwaren.

[![Styre objekterne og service](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) støtte til gennemførelse af OLE OPOS for POS hjælper med at sikre, at hvis enhedsproducenter og POS udgivere implementerer standarden korrekt, POS-systemer og understøttede enheder kan arbejde sammen, selvom de ikke var tidligere testede sammen. **Bemærk:** OPOS support garanterer ikke understøttelse af alle enheder, der har OPOS-drivere. Microsoft Dynamics 365 for operationer – Retail understøtte først pågældende enhedstype eller gennem OPOS-klassen. Desuden kan serviceobjekter ikke altid være opdateret med den nyeste version af CCOs. Du skal også være opmærksom på, at generelt kvaliteten af serviceobjekter varierer.

### <a name="windows"></a>Windows

Udskrivning af kvitteringer i POS er optimeret til OPOS. OPOS tendens til at være meget hurtigere end udskrivning via Windows. Det er derfor en god ide at bruge OPOS, især i retail-miljøer, hvor udskrives kvitteringer for 40 kolonner og postering klokkeslæt skal være hurtig. For de fleste enheder bruger du OPOS-kontrolelementer. Men nogle OPOS modtagelsen printere understøtter også Windows-drivere. Ved hjælp af en Windows-driver, du kan få adgang til de seneste skrifttyper og en netværksprinter til flere kasseapparater. Der er dog ulemper ved at bruge Windows-drivere. Her er nogle eksempler på disse ulemper:

-   Når der bruges Windows-drivere, gengives billeder før udskrivning indtræffer. Derfor tendens udskrivning til at være langsommere end på printere, der bruger OPOS-objekter.
-   Enheder, der er sluttet til printeren ("typehjulsforbundet") fungerer muligvis ikke korrekt når der bruges Windows-drivere. For eksempel kan ikke åbne kassen, eller slip printeren til word muligvis ikke som forventet.
-   OPOS understøtter også et mere omfattende sæt af variabler, der er specifikke for detail modtagelsen printere, som papir opskæring eller følgesedlen udskrives.

Hvis der er tilgængelige for den Windows-printer, du bruger OPOS-kontrolelementer, fungere printeren stadig korrekt med Microsoft Dynamics 365 for operationer – Retail.

### <a name="universal-windows-platform"></a>Universal Windows-platformen

UWP, for så vidt angår retail enheder er relateret til understøttelse af Plug and Play-enheder i Windows. Når en Plug and Play-enheden er tilsluttet en Windows OS-version, der understøtter typen enhed, kræves ingen driver til enheden til at blive brugt som tilsigtet. For eksempel, hvis Windows registrerer en enhed med Bluetooth-højttaler, OS ved, at enheden har den **taler** klasse type. Derfor, og den behandler enheden som en højttaler. Der kræves ingen yderligere installation. Mange USB-enheder kan tilsluttes for POS-enheder, og Windows kan genkende dem som Brugerstyrede inputenheder (HIDs). Det kan dog ikke kunne se de funktioner, der giver enheden, fordi enheden ikke angiver en klasse eller typer enheder. Enhedsklasser til stregkodescannere og MSRs er blevet tilføjet i Windows-10. Derfor, hvis en enhed erklærer sig selv Windows 10 som en enhed af en af disse klasser, Windows vil lytte efter hændelser fra enheden på passende tidspunkter. Moderne POS understøtter UWP MSRs og scannere. Derfor, når den er klar til input fra en af disse enheder og er tilsluttet en enhed, der hører til en af disse klasser, kan enheden bruges. For eksempel, hvis en UWP bar kode scanner er tilsluttet en computer med Windows 10 og stregkode-logon er konfigureret til moderne POS, træder stregkodescanneren i kraft på skærmen Log på. Der kræves ingen yderligere installation. Flere klasser i tjenesten UWP enheder punkt føjes til Windows. Disse klasser indeholder klasser for kontant skuffer og modtagelsen printere. Understøttelse af disse nye enhedsklasser i moderne POS afventer.

### <a name="keyboard-wedge"></a>Tastaturet kile

Tastaturet kile enheder sender data til computeren, som om, at data er indtastet på et tastatur. Som standard modtager det felt, der er aktive på POS derfor de data, der er scannet eller ført gennem kortlæser. Denne funktionsmåde kan i nogle tilfælde medføre en forkert type data der skal scannes i det forkerte felt. For eksempel kan en stregkode scannes i et felt, der er beregnet til indføring af kreditkortdata. I mange tilfælde er der logik ved POS, der bestemmer, om de data, der er scannet eller ført gennem kortlæser er en stregkode eller Kortbrug. Derfor håndteres data, der korrekt. Når enhederne er angivet som OPOS i stedet for tastaturet kile enheder, er der mere kontrol over, hvordan dataene fra enhederne, der kan forbruges, fordi flere er "kendte" om den enhed, som dataene stammer fra. For eksempel data fra en stregkodescanner genkendes automatisk som en stregkode, og den tilknyttede post i databasen findes, lettere og hurtigere, end hvis en søgning med generiske streng blev brugt som er tilfældet med tastaturet kile enheder.

### <a name="native-printer"></a>Indbygget printer

Oprindelig (eller "Enhed", som er navngivet i hardwareprofilen) printere kan konfigureres til at bede brugeren om at vælge en printer, der er konfigureret på computeren. Når en printer i den **enhed** type er konfigureret, hvis moderne POS støder på en kommando, der udskrives, brugeren bliver bedt om at vælge en printer på en liste. Denne funktionsmåde adskiller sig fra funktionsmåden for Windows-drivere, da den **Windows** printertype hardwareprofilen ikke vise en liste over printere. I stedet, det kræver, at der gives en navngiven printer i den **enhedsnavn** felt.

### <a name="windows"></a>Windows

Den **Windows** enhedstype bruges til kun printere. Når en Windows-printer er konfigureret på hardwareprofilen, skal der gives specifikke printernavnet. Når moderne POS støder udskrive hændelser, hvis der er konfigureret en printer i Windows, vil begivenheden blive overført til den angivne Windows-printer. Brugeren ikke bedt om at vælge en printer.

### <a name="network"></a>Netværk

Netværk-adresserbare pengeskuffer, modtagelsen printere og terminaler betaling kan bruges via et netværk, enten direkte via Interproces kommunikation (IPC) hardware-station, der er indbygget i moderne POS for Windows-program eller via IIS hardware station til andre moderne POS-klienter.

## <a name="hardware-station-deployment-options"></a>Indstillinger for installation af hardware station
### <a name="ipc-built-in"></a>IPC (indbygget)

Interproces-kommunikation (IPC) hardware station er indbygget i moderne POS for Windows-program. Hvis du vil bruge IPC hardware station, kan du tildele en hardwareprofil til et register, som skal bruge moderne POS for Windows-program. Opret derefter en hardware-station af den **dedikeret** type for den butik, hvor registret skal bruges. Når du starter moderne POS, IPC hardware station vil være aktiv, og POS-enheder, der er konfigureret, vil være klar til brug. Hvis du midlertidigt ikke har brug for lokal hardware eller anden grund, kan du bruge den **administrere hardware stationer** operation for at deaktivere computerens hardwarefunktioner station. Moderne POS kan også bruge IPC hardware station for at kommunikere direkte med enheder på netværket.

### <a name="iis"></a>IIS

Du kan bruge IIS eller enkeltstående version af hardware-station på to måder. Descriptor "IIS" indebærer, at POS-programmet har forbindelse til hardware stationen via Microsoft Internet Information Services. POS-programmet opretter forbindelse til IIS hardware stationen via webtjenester, der kører på en computer, hvor enhederne er tilsluttet. Når du bruger IIS, retail-enheder, der er tilsluttet en hardware-station kan bruges ved POS-kasseapparat, der er på samme netværk som IIS hardware station. Da kun moderne POS til Windows indeholder indbygget understøttelse af eksterne enheder retail, skal alle andre moderne POS-programmer bruge IIS hardware station til at kommunikere med POS-enheder, der er konfigureret i hardwareprofilen. Hver forekomst af IIS hardware station kræver derfor, at en computer, der kører webtjenesten og et program, der kommunikerer med enhederne. IIS hardware station er påkrævet for alle ikke - Windows moderne POS-programmer.

#### <a name="dedicated"></a>Dedikeret

Moderne POS bruger hardware stationerne i det **dedikeret** type til at registrere, at eksterne enheder har direkte forbindelse til den computer, hvor programmet anvendes. Men den **dedikeret** type kan også bruges til IIS hardware stationer. I et traditionelt, fast POS-scenario, der bruger Cloud POS som POS-programmet, den **dedikeret** hardware Stationstype bruges til IIS hardware stationer, der er installeret på samme computer, der kører sky POS. Fra en retail tilbehør perspektiv er dedikeret IIS hardware station bedre retail ydre understøttelse af traditionelt, fast POS-scenarier. Dedikeret hardware-stationer understøtter alle eksterne enheder, der understøttes i hardwareprofilen.

#### <a name="shared"></a>Delt

Fælles hardware stationer er beregnet til at blive brugt af flere POS-enheder i løbet af dagen. Fælles hardware stationer er optimeret til support kun kontant skuffer, modtagelsen printere og terminaler til betaling. Du kan oprette direkte forbindelse enkeltstående stregkodescannere, MSRs, linje viser, skalaer eller andre enheder. Ellers kan konflikter opstå, når flere POS-enheder, der forsøger at indløse disse enheder på samme tid. Her er, hvordan konflikter håndteres for understøttede enheder:

-   **Kassen** – pengeskuffen åbnes via en hændelse, der sendes til enheden. Det eneste problem, der kan opstå, når en pengeskuffen kaldes opstår, hvis pengeskuffen allerede er åben. For fælles hardware stationer kassen skal indstilles til **delte** i hardwareprofilen. Denne indstilling forhindrer, at POS kontrollerer, om kassen allerede er åben, når der udsendes Åbn-kommandoer.
-   **Bonprinteren** – Hvis to modtagelse, udskrivning kommandoer sendes til hardware-station på samme tid, en af kommandoerne, der kan gå tabt, afhængigt af enheden. Nogle enheder har interne hukommelse eller gruppering, der kan forhindre dette problem. Hvis en kommando, der udskrives ikke lykkes, kassereren modtager en fejlmeddelelse og kan derefter prøve kommandoen Udskriv fra POS.
-   **Betaling terminal** – Hvis en kasserer forsøg til at afgive bud på en transaktion på en terminal betaling, der allerede bruges, en meddelelse underretter kassereren, at terminalen bruges og beder kassereren om at prøve igen senere. Normalt kan kasserere se, at en terminal er allerede i brug og venter, indtil anden transaktionen er fuldført, inden de forsøger at afgive bud igen.

Validering er planlagt til en fremtidig version til at registrere, om ikke-understøttede enheder er konfigureret for en hardwareprofil, der er knyttet til en delt hardware station. Hvis der registreres ikke-understøttede enheder, vil brugeren modtage en meddelelse om, at enhederne, der ikke understøttes for fælles hardware-stationer. For fælles hardware stationer på **Vælg ved licitation** indstilling er angivet til **Ja** på niveauet register. POS-bruger derefter bedt om at vælge en station hardware, når et bud er valgt for en transaktion på POS. Når hardware-station vælges kun på tidspunktet for bud, føjes hardware station valg direkte til POS-arbejdsgang for mobile scenarier. Som en ekstra fordel er ikke linjevisningen for betalingen terminal bruges til delte scenarier. Hvis betalingen terminal bruges som en visning, kan andre brugere forhindres i ved hjælp af denne terminal, før transaktionen er fuldført. I mobile scenarier kan linjer føjes til en transaktion i en længere periode. Derfor de **Vælg ved licitation** indstilling, der er nødvendige for at sikre optimal enhed tilgængelighed.

### <a name="network-peripherals"></a>Netværk-enheder

Netværk-betegnelse for enheder i hardwareprofilen kan pengeskuffer, modtagelsen printere og terminaler betaling skal være forbundet via en netværksforbindelse.

#### <a name="modern-pos-for-windows"></a>Moderne POS til Windows

Du kan angive IP-adresser til netværk tilbehør to steder. Hvis Windows med moderne POS-klienten ved hjælp af et enkelt sæt af eksterne netværk, skal du angive IP-adresserne for disse enheder ved hjælp af den **IP-konfiguration** indstilling i handlingsruden for kasseapparatet sig selv. I tilfælde af netværksenheder, der skal deles mellem POS-kasseapparater, der kan knyttes en hardwareprofil med netværksenheder, der er tildelt direkte til en delt hardware station. For at tildele IP-adresser, kan du vælge denne hardware station på den **Retail butikker** side, og brug derefter de **IP-konfiguration** indstilling i den **Hardware stationer** sektion til at angive de netværksenheder, der er tildelt denne hardware station. For hardware-stationer, der har kun netværksenheder, behøver du ikke at installere hardware-stationen selv. I så fald kræves hardware-station kun at gruppere begrebsmæssigt netværk adresserbare enheder ud fra deres placering i detailbutikken.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Sky POS, moderne POS for iOS og moderne POS til Android

Den logik, der styrer fysisk tilsluttet og netværks-adresserbare enheder findes i hardware-stationen. Derfor til alle POS-klienter med undtagelse af moderne POS til Windows skal hardware-station en IIS være installeret og aktiv for at aktivere POS til at kommunikere med eksterne enheder, uanset om disse enheder er fysisk tilsluttet en hardware-station eller behandles via netværket.

## <a name="setup-and-configuration"></a>Installation og konfiguration
### <a name="hardware-station-installation"></a>Hardwareinstallation station

Oplysninger finder du under [Retail station hardwarekonfiguration og installation af](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderne POS til Windows installation og konfiguration

Oplysninger finder du under [moderne detail-POS-konfiguration og installation](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS enhedsinstallation og konfiguration

Du kan finde flere oplysninger om OPOS-komponenter, afsnittet "Understøttede grænseflader" i dette dokument. Typisk OPOS-drivere, der leveres af producenten af enheden. Når der installeres en enhedsdriver OPOS, føjer en nøgle til Windows-registreringsdatabasen på en af følgende placeringer:

-   **32-bit system:** HKEY\_lokale\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bit system:** HKEY\_lokale\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Konfigurerede enheder er organiseret efter enhedsklasse OPOS inden for placering i registreringsdatabasen ServiceOPOS. Flere enhedsdrivere, gemmes.

## <a name="supported-scenarios-by-hardware-station-type"></a>Understøttede scenarier efter hardwaretype station
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Understøttelse af klienter – IPC hardware station vs. IIS hardware station

Følgende tabel viser de topologier og installationsscenarier, der understøttes.

| Klient      | IPC hardware station | IIS hardware station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

### <a name="network-peripherals"></a>Netværk-enheder

Netværk-enheder understøttes direkte via hardware-station, der er indbygget i moderne POS for Windows-program. Du skal installere en IIS hardware station til alle klienter.

| Klient      | IPC hardware station | IIS hardware station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Understøttede enhedstyper efter hardwaretype station
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS til Windows med et IPC (indbyggede) hardware station

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Understøttet enhedsklasse</th>
<th>Understøttede grænseflader</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhed</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhed</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Dobbeltvisning</td>
<td>Windows-driver</td>
</tr>
<tr class="odd">
<td>Magnetstribelæser</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ingen installation er nødvendig).</li>
<li>Tastaturet kile (ingen installation er nødvendig).</li>
</ul></td>
</tr>
<tr class="even">
<td>Vekseludsteder</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> kun én skuffe kan konfigureres, hvis <strong>Brug deles Skift</strong> er konfigureret på kassen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kasseskuffe 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> kun én skuffe kan konfigureres, hvis <strong>Brug deles Skift</strong> er konfigureret på kassen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ingen installation er nødvendig).</li>
<li>Tastaturet kile (ingen installation er nødvendig).</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ingen installation er nødvendig).</li>
<li>Tastaturet kile (ingen installation er nødvendig).</li>
</ul></td>
</tr>
<tr class="even">
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Pinkodetastatur</td>
<td>OPOS (Support ydes gennem tilpasning af betalingsconnector).</td>
</tr>
<tr class="even">
<td>Signaturhentning</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Understøttelse af brugerdefinerede enheder</li>
<li>Netværk (se dokumentationen til connector For at få flere oplysninger).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-klienter, der har en dedikeret hardware station til IIS

**Bemærk:** når IIS hardware station er "dedicated", der er en én til én-relation mellem POS-klient- og hardware-station.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Understøttet enhedsklasse</th>
<th>Understøttede grænseflader</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver <strong>Bemærk:</strong> til Windows-printere på et netværk, brugeren af hardware-station skal have tilladelse til at få adgang til printeren.</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Magnetstribelæser</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Vekseludsteder</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> kun én skuffe pr. hardwareprofil kan konfigureres, hvis <strong>Brug deles Skift</strong> er konfigureret på kassen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kasseskuffe 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Scanner 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Pinkodetastatur</td>
<td>OPOS (Support ydes gennem tilpasning af betalingsconnector).</td>
</tr>
<tr class="odd">
<td>Sig. hente</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal </td>
<td><ul>
<li>Understøttelse af brugerdefinerede enheder</li>
<li>Netværk (se dokumentationen til connector For at få flere oplysninger).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-klienter, der har en fælles IIS hardware station

**Bemærk:** når IIS hardware station er "delt", flere enheder kan bruge hardware-station på samme tid. I dette scenarie skal du bruge kun de enheder, der er angivet i følgende tabel. Hvis du forsøger at dele enheder, der ikke er angivet her, som stregkodescannere og MSRs, sker fejl, når flere enheder, der forsøger at gøre krav på den samme eksterne enhed. I fremtiden, forhindres sådan konfiguration udtrykkeligt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Understøttet enhedsklasse</th>
<th>Understøttede grænseflader</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver <strong>Bemærk:</strong> til Windows-printere på et netværk, brugeren af hardware-station skal have tilladelse til at få adgang til printeren.</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vekseludsteder</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> kun én skuffe pr. hardwareprofil kan konfigureres, hvis <strong>Brug deles Skift</strong> er konfigureret på kassen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kasseskuffe 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Understøttelse af brugerdefinerede enheder</li>
<li>Netværk (se dokumentationen til connector For at få flere oplysninger).</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfiguration for understøttede scenarier
Finde flere oplysninger om, hvordan du oprette hardwareprofiler [Definer og vedligehold kanal klienter, inklusive registre og hardware stationer](define-maintain-channel-clients-registers-hw-stations.md). **Bemærk:** For Microsoft Dynamics 365 for operationer version 1611 opdager station hardwareprofil bruges ikke længere. Attributter, som du tidligere har konfigureret i hardwareprofilen station er nu en del af selve stationen hardware.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS til Windows med et IPC (indbyggede) hardware station

Denne konfiguration er den mest typiske konfiguration for traditionelle, fast POS-kasseapparater. I dette scenarie er profiloplysninger hardware knyttet direkte til kasseapparatet sig selv. AUTORISATIONSKODE terminalnummer, bør også angives i selve register. Hvis du vil konfigurere denne konfiguration, skal du følge disse trin.

1.  Opret en hardwareprofil, hvor alle de nødvendige enheder er konfigureret.
2.  Du kan knytte hardwareprofilen til POS-kasseapparat.
3.  Oprette en hardware-station af den **dedikeret** type til den forhandler, hvor der skal bruges på POS-kasseapparat. En beskrivelse er valgfrit. **Bemærk:** du behøver ikke at angive andre egenskaber for hardware-station. Alle andre nødvendige oplysninger som hardwareprofilen, kommer fra kasseapparatet sig selv.
4.  Klik på **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplan**.
5.  Vælg den **1090** distributionsplan at synkronisere den nye hardwareprofil til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
6.  Vælg den **1040** distributionsplan at synkronisere den nye hardware-station til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
7.  Installer og aktiver moderne POS til Windows.
8.  Start moderne POS til Windows, og begynde at bruge de tilsluttede eksterne enheder.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-klienter, der har en dedikeret hardware station til IIS

Denne konfiguration kan bruges til alle moderne POS-klienter, der har en hardware-station, der bruges udelukkende af en POS registrere. Hvis du vil konfigurere denne konfiguration, skal du følge disse trin.

1.  Opret en hardwareprofil, hvor alle de nødvendige enheder er konfigureret.
2.  Oprette en hardware-station af den **dedikeret** type til den forhandler, hvor der skal bruges på POS-kasseapparat.
3.  På stationen dedikeret hardware, skal du angive følgende egenskaber:
    -   **Værtsnavn** – navnet på værtscomputeren, hvor hardware-station skal køres. **Bemærk:** sky POS kan løse **localhost** til at bestemme den lokale computer, hvor kører sky POS. Det certifikat, der kræves for at parre hardware-station sky POS skal dog også have "Localhost" som navnet på computeren. For at undgå problemer, anbefaler vi, at du viser en forekomst af hver dedikeret hardware station til butikken, efter behov. For hver hardware-station skal værtsnavnet specifikt computernavn, hvor hardware-station skal implementeres.
    -   **Port** – porten, der skal bruges til hardware-station til at kommunikere med moderne POS-klienten.
    -   **Hardwareprofil** – Hvis der ikke er hardwareprofilen, forudsat på stationen hardware selv, der skal bruges den hardwareprofil, der tildeles til kasseapparatet.
    -   **Autorisationskode – POS-nummer** – den AUTORISATIONSKODE terminal-ID'ET skal bruges, når der sendes elektronisk PENGEOVERFØRSEL bevillinger. Dette ID er leveret af kreditkortprocessoren.
    -   **Pakkenavn** – pakken hardware station skal bruges, når stationen hardware er installeret.

4.  Klik på **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplan**.
5.  Vælg den **1090** distributionsplan at synkronisere den nye hardwareprofil til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
6.  Vælg den **1040** distributionsplan at synkronisere den nye hardware-station til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
7.  Installer hardware-station. Finde flere oplysninger om, hvordan du installerer hardware-station [Retail station hardwarekonfiguration og installation af](retail-hardware-station-configuration-installation.md).
8.  Installer og aktiver moderne POS. Finde flere oplysninger om, hvordan du installerer moderne POS [moderne detail-POS-konfiguration og installation](retail-modern-pos-device-activation.md).
9.  Log på moderne POS, og vælg **udfører handlinger uden for pengeskuffe**.
10. Start den **administrere hardware stationer** handling.
11. Klik på **styre**.
12. Angive indstillingen for at slå hardware-station på siden hardware station management.
13. Vælg stationen hardware til at bruge, og klik derefter på **par**.
14. Når hardware-station er parret, skal du klikke på **Luk**.
15. Klik på stationen for at aktivere den sidst valgte hardware på siden hardware station valg.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-klienter, der har en fælles IIS hardware station

Denne konfiguration kan bruges til alle moderne POS-klienter, der deler hardware stationer med andre enheder. Hvis du vil konfigurere denne konfiguration, skal du følge disse trin.

1.  Opret en hardwareprofil, hvor de nødvendige enheder er konfigureret.
2.  Oprette en hardware-station af den **delte** type til den forhandler, hvor der skal bruges på POS-kasseapparat.
3.  På stationen delte hardware, skal du angive følgende egenskaber:
    -   **Værtsnavn** – navnet på værtscomputeren, hvor hardware-station skal køres.
    -   **Beskrivelse** – tekst, der hjælper med at identificere hardware-station, som **returnerer** eller **foran på store**.
    -   **Port** – porten, der skal bruges til hardware-station til at kommunikere med moderne POS-klienten.
    -   **Hardwareprofil** – For fælles hardware stationer hver hardware station skal have en hardwareprofil. Hardwareprofiler kan deles mellem hardware stationer, men de skal være knyttet til hver station hardware. Vi anbefaler desuden, at du bruger delte skiftehold, når flere enheder, der bruger den samme delte hardware-station. Hvis du vil konfigurere en delt Skift, skal du klikke på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**. Marker kassen for hver delt hardwareprofil og angive den **delt Skift skuffe** at **Ja**.
    -   **Autorisationskode – POS-nummer** – den AUTORISATIONSKODE terminal-ID'ET skal bruges, når der sendes elektronisk PENGEOVERFØRSEL bevillinger. Dette ID er leveret af kreditkortprocessoren.
    -   **Pakkenavn** – pakken hardware station skal bruges, når stationen hardware er installeret.

4.  Gentag trin 2 og 3 for hver ekstra hardware-station, der kræves i butikken.
5.  Klik på **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplan**.
6.  Vælg den **1090** distributionsplan at synkronisere den nye hardwareprofil til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
7.  Vælg den **1040** distributionsplan at synkronisere den nye hardware-station til butikken. Klik på **kører nu** til at synkronisere ændringer i POS.
8.  Installer hardware-station på hver computer, du har oprettet i trin 2 og 3. Finde flere oplysninger om, hvordan du installerer hardware-station [Retail station hardwarekonfiguration og installation af](retail-hardware-station-configuration-installation.md).
9.  Installer og aktiver moderne POS. Finde flere oplysninger om, hvordan du installerer moderne POS [moderne detail-POS-konfiguration og installation](retail-modern-pos-device-activation.md).
10. Log på moderne POS, og vælg **udfører handlinger uden for pengeskuffe**.
11. Start den **administrere hardware stationer** handling.

12. Klik på **styre**.
13. Angive indstillingen for at slå hardware-station på siden hardware station management.
14. Vælg stationen hardware til at bruge, og klik derefter på **par**.
15. Gentag trin 14 for hver station til hardware, der skal bruge moderne POS.
16. Når alle de påkrævede hardwareenheder stationer er parret, skal du klikke på **Luk**.
17. Klik på stationen for at aktivere den sidst valgte hardware på siden hardware station valg. **Bemærk:** Hvis enheder ofte bruger forskellige hardware-stationer, anbefaler vi, at du konfigurerer moderne POS for at spørge kassereren kan vælge en hardware-station, når de begynder processen betalingsmiddel. Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**registrerer**. Vælg registret, og angiv derefter den **Vælg ved bud** at **Ja**. Brug af **1090** distributionsplan synkronisere ændringerne til databasen kanal.

## <a name="extensibility"></a>Udvidelsesmuligheder
Finde oplysninger om udvidelsesmuligheder scenarier for hardware-station, [Hardware Station udvidelsesmuligheder](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sikkerhed
I henhold til aktuelle sikkerhedsstandarder, der skal bruges følgende indstillinger i et produktionsmiljø: **Bemærk:** gør hardware station installationsprogrammet automatisk disse redigeringer i registreringsdatabasen som en del af installationen via selvbetjening.

-   Secure Sockets Layer (SSL), der skal deaktiveres.
-   Kun Transport Layer Security (TLS) version 1.2 (eller den aktuelle højeste version) skal aktiveres og anvendes. **Bemærk:** som standard SSL og alle version af TLS undtagen TLS 1.2 er deaktiveret. Hvis du vil redigere eller aktivere disse værdier, skal du følge disse trin:
    1.  Tryk på Windows-tasten + R for at åbne en **køre** vindue.
    2.  I den **åbne**, skal du skrive **Regedit**, og klik derefter på **OK**.
    3.  Hvis en **User Account Control** meddelelsesboks vises, skal du klikke på **Ja**.
    4.  I den **Registreringseditor** vinduet Naviger til **HKEY\_lokale\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Følgende taster er indsat automatisk for at tillade TLS 1.2 kun:
        -   TLS 1.2Server: aktiveret = 1
        -   TLS-1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: aktiveret = 1
        -   TLS-1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: aktiveret = 0
        -   TLS 1.1Client: aktiveret = 0
        -   TLS 1.0Server: aktiveret = 0
        -   TLS 1.0Client: aktiveret = 0
        -   SSL-3.0Server: aktiveret = 0
        -   SSL-3.0Client: aktiveret = 0
        -   SSL-2.0Server: aktiveret = 0
        -   SSL-2.0Client: aktiveret = 0
-   Ikke flere netværksporte skal være åbent, medmindre det er påkrævet af kendte, angivne grunde.
-   Deling af ressourcer på tværs af oprindelse skal deaktiveres, og skal angive de tilladte oprindelse, der er godkendt.
-   Kun pålidelige certifikatudstedere, der skal bruges til at hente certifikater, der skal bruges på computere, der kører hardware-station.

**Bemærk:** det er meget vigtigt, at du gennemgår sikkerhedsretningslinjer for IIS og betaling kort industri (PCI) krav.

## <a name="peripheral-simulator"></a>Ekstern simulator
Oplysninger finder du under [Retail ydre simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested ydre enheder
### <a name="ipc-built-in-hardware-station"></a>IPC (indbyggede) hardware station

De følgende enheder blev testet ved hjælp af IPC hardware-station, der er indbygget i moderne POS til Windows.

#### <a name="printer"></a>Printer

| Fabrikanten | Model    | Interface | Bemærkninger                |
|--------------|----------|-----------|-------------------------|
| EPSON        | TM-T88IV | OPOS      |                         |
| EPSON        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket   |
| Star         | mPOP     | OPOS      | Forbindelse via Bluetooth |
| HP           | F7M67AA  | OPOS      | Strømdrevet USB             |

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Fabrikanten  | Model         | Interface | Bemærkninger |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Tegn        | LS2208        | OPOS      |          |
| Integreret HP | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>Pinkodetastatur

| Fabrikanten | Model  | Interface | Bemærkninger                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Kræver tilpasning af betalings-stik |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikanten | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Brugerdefineret    | Kræver tilpasning af betalings-stik                                |
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |

#### <a name="cash-drawer"></a>Kassen

| Fabrikanten | Model     | Interface | Bemærkninger                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Forbindelse via Bluetooth |
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket   |
| Star         | SMD2 1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Linjevisning

| Fabrikanten  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| Integreret HP | G6U79AA | OPOS      |          |
| EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturhentning

| Fabrikanten | Model  | Interface | Bemærkninger |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skaler

| Fabrikanten | Model         | Interface | Bemærkninger |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetstribelæser

| Fabrikanten | Model       | Interface | Bemærkninger |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Dedikeret IIS hardware station

De følgende enheder blev testet ved hjælp af en dedikeret (ikke delt) IIS hardware station samt moderne POS til Windows og sky POS.

#### <a name="printer"></a>Printer

| Fabrikanten | Model    | Interface | Bemærkninger                  |
|--------------|----------|-----------|---------------------------|
| EPSON        | TM-T88IV | OPOS      |                           |
| EPSON        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket     |
| Star         | TSP100   | OPOS      | Kræver TSP650II drivere |
| HP           | F7M67AA  | OPOS      | Strømdrevet USB               |

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Fabrikanten  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Tegn        | LS2208  | OPOS      |          |
| Integreret HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>Pinkodetastatur

| Fabrikanten | Model  | Interface | Bemærkninger                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Kræver tilpasning af betalings-stik |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikanten | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Brugerdefineret    | Kræver tilpasning af betalings-stik                                |
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |

#### <a name="cash-drawer"></a>Kassen

| Fabrikanten | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Linjevisning

| Fabrikanten  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| Integreret HP | G6U79AA | OPOS      |          |
| EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturhentning

| Fabrikanten | Model  | Interface | Bemærkninger |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skaler

| Fabrikanten | Model         | Interface | Bemærkninger |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetstribelæser

| Fabrikanten | Model       | Interface | Bemærkninger |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Delte IIS hardware station

De følgende enheder blev testet ved hjælp af en delt IIS hardware station samt moderne POS til Windows og sky POS. **Bemærk:** understøttes kun en printer, betaling terminal og pengeskuffen.

#### <a name="printer"></a>Printer

| Fabrikanten | Model    | Interface | Bemærkninger                  |
|--------------|----------|-----------|---------------------------|
| EPSON        | TM-T88IV | OPOS      |                           |
| EPSON        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket     |
| Star         | TSP100   | OPOS      | Kræver TSP650II drivere |
| HP           | F7M67AA  | OPOS      | Strømdrevet USB               |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Fabrikanten | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector; forbindelse via Netværks- og USB- |

#### <a name="cash-drawer"></a>Kassen

| Fabrikanten | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Fejlfinding
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderne POS kan registrere hardware-station på listen til valg, men det kan ikke fuldføre parringen

**Løsning:** Kontrollér følgende liste over mulige fejlpunkter:

-   Den computer, der kører moderne POS har tillid til det certifikat, der bruges på den computer, der kører hardware-station.
    -   For at kontrollere denne opsætning i en webbrowser, gå til følgende Webadresse: https://&lt;computernavnet&gt;:&lt;portnummer&gt;/HardwareStation/ping.
    -   Denne URL-adresse bruger en ping til at kontrollere, at du kan få adgang til computeren, og browseren angiver, om certifikatet, der er tillid til. (For eksempel, i Internet Explorer vises et låseikon på adresselinjen. Når du klikker på dette ikon, kontrollerer Internet Explorer, om certifikatet, der er tillid til i øjeblikket. Du kan installere certifikatet på den lokale computer ved at få vist detaljer om det certifikat, der er vist.)
-   På den computer, der kører hardware-station, er den port, der bruges af hardware-station åbnes i firewall'en.
-   Hardware-station er korrekt installeret forhandlerkontooplysninger ved hjælp af værktøjet installation købmand oplysninger, der køres i slutningen af hardware station installer.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderne POS registrere ikke hardware-station på listen til valg

**Løsning:** en af følgende faktorer kan forårsage dette problem:

-   Hardware-stationen endnu ikke er konfigureret korrekt i headquarters. Følg trin tidligere i dette emne for at kontrollere, at station hardwareprofil og hardware-station er angivet korrekt.
-   Job, der ikke har været kørt for at opdatere kanalkonfigurationen af. I dette tilfælde kørsel 1070 for channel-konfiguration.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderne POS afspejle ikke nye kontant skuffe indstillinger

**Løsning:** lukker den aktuelle batch. Ændringer til kassen er ikke opdateret til moderne POS, før den aktuelle batch er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderne POS rapporterer et problem med en ydre Detail

**Løsning:** her er nogle typiske årsager til problemet:

-   Sørg for, at andre device driver konfigurationsværktøjer er lukket. Hvis disse værktøjer er åbne, kan de forhindre, at moderne POS eller hardware-station påberåbelse af enheden.
-   Hvis den eksterne enhed retail deles med flere POS-enheder, skal du kontrollere, at den tilhører en af følgende kategorier:
    -   Kassen
    -   Printer til modtagelse
    -   Betalingsterminal 

    Hvis den eksterne enhed ikke tilhører en af disse kategorier, er ikke hardware-station udviklet til at aktivere den eksterne enhed skal fordeles på flere POS-enheder.
-   Nogle gange kan enhedsdrivere forårsage de fælles kontrol-objekter (CCOs) for at fungere korrekt. Hvis en enhed er for nylig blevet installeret, men det ikke fungerer korrekt, eller du bemærker andre problemer, kan du ofte løse problemet ved at geninstallere CCOs. Du kan hente CCOs <http://monroecs.com/oposccos_current.htm>.
-   Hvis du ændrer hyppige ydre under test eller fejlfinding, skal du muligvis nulstille IIS i stedet for venter i cachen til at opdatere sig selv. Hvis du vil nulstille IIS, skal du følge disse trin:
    1.  Fra den **Start** i menuen, skal du skrive **CMD**.
    2.  I søgeresultaterne, skal du højreklikke på **kommandoprompt**, og klik derefter på **Kør som administrator**.
    3.  I den **kommandoprompt** vindue, skal du skrive **iisreset/Restart**, og tryk derefter på Enter.
    4.  Når IIS er genstartet, skal du genstarte moderne POS.
-   Mens du foretager hyppige ændringer til ydre enheder, hvis du også ofte starter og lukker POS-klienten, kan dllhost processen fra en tidligere POS-session forstyrre den aktuelle session. I dette tilfælde kan en enhed ikke bruges indtil du lukker værten dynamic-link library (DLL), der styrer den seneste session. For at lukke DLL-værten, skal du følge disse trin:
    1.  Fra den **Start** i menuen, skal du skrive **Jobliste**.
    2.  I søgeresultaterne, skal du klikke på **Jobliste**.
    3.  I Jobliste, på den **oplysninger om**, og klik på den kolonneoverskrift, der hedder **navn** at sortere tabellen alfabetisk efter navn.
    4.  Rul ned, indtil du finder dllhost.exe.
    5.  Vælg hver DLL-vært, og klik derefter på **Afslut job**.
    6.  Når værterne DLL-filen er blevet lukket, kan du genstarte moderne POS.


<a name="see-also"></a>Se også
--------

[Retail ydre simulator](retail-peripheral-simulator.md)


