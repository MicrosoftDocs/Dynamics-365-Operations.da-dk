---
title: Oversigt over eksterne detailenheder
description: "I dette emne forklares begreberne i forbindelse med eksterne detailenheder. Det beskriver de forskellige måder, at eksterne enheder kan forbindes til POS-enheden, og komponenterne, der er ansvarlige for administration af forbindelsen med POS-enheden."
author: rubencdelgado
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 52a16be4b07eafb493c7fd7ad52a6d9d1bb9ee89
ms.openlocfilehash: 77049ba4c9c39cd44f1919b672deaf700b91357d
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="retail-peripherals-overview"></a>Oversigt over eksterne detailenheder

[!include[banner](includes/banner.md)]


I dette emne forklares begreberne i forbindelse med eksterne detailenheder. Det beskriver de forskellige måder, at eksterne enheder kan forbindes til POS-enheden, og komponenterne, der er ansvarlige for administration af forbindelsen med POS-enheden.

## <a name="concepts"></a>Begreber

### <a name="pos-registers"></a>Kasseapparater

Navigation: Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**. POS-kasseapparat er en enhed, der bruges til at definere egenskaberne for en bestemt forekomst af POS-enheden. Disse egenskaber omfatter hardwareprofilen eller opsætningen af detailenheder, der skal bruges ved kasseapparatet, den butik, som kasseapparatet er tilknyttet, og den visuelle oplevelse for den bruger, der logger på kasseapparatet.

### <a name="devices"></a>Enheder

Navigation: Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Enheder**. En enhed repræsenterer en fysisk forekomst af en enhed, der er knyttet til et POS-kasseapparat. Når der oprettes en enhed, knyttes den til et POS-kasseapparat. Enheden registrerer oplysninger om, hvornår et POS-kasseapparat aktiveres, den klienttype, som benyttes, og den programpakke, der er blevet installeret på en bestemt enhed. Enheder kan knyttes til følgende programtyper: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android og Retail Modern POS – iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS er POS-programmet til Microsoft Windows. Det kan anvendes på Windows 10-operativsystemer (OSs).

### <a name="cloud-pos"></a>Cloud POS

Cloud POS er en browserbaseret version af Modern POS-programmet, der kan åbnes i en webbrowser.

### <a name="modern-pos-for-ios"></a>Modern POS til iOS

Modern POS til iOS er en iOS-baseret version af Modern POS-programmet, der kan implementeres på iOS-enheder.

### <a name="modern-pos-for-android"></a>Modern POS til Android

Modern POS til Android er en Android-baseret version af Modern POS-programmet, der kan implementeres på Android-enheder.

### <a name="pos-peripherals"></a>Eksterne POS-enheder

Eksterne POS-enheder er enheder, der udtrykkeligt understøttes til POS-funktioner. Disse eksterne enheder er typisk opdelt i bestemte klasser. Du kan finde yderligere oplysninger om disse klasser i afsnittet "Enhedsklasser" i dette emne.

### <a name="hardware-station"></a>Hardwarestation

Navigation: Klik på **Detail** &gt; **Kanaler** &gt; **Detailbutikker** &gt; **Alle detailbutikker**. Vælg en butik, og klik derefter i oversigtspanelet **Hardwarestationer**. Indstillingen **Hardwarestation** er en indstilling på kanalniveau, der bruges til at definere forekomster, hvor logikken for eksterne detailenheder skal implementeres. Denne indstilling på kanalniveau bruges til at bestemme karakteristika for hardwarestationen. Den bruges også til at angive de hardwarestationer, der er tilgængelige for en Modern POS-forekomst i en given butik. Hardwarestationen er indbygget i Modern POS-programmet til Windows. Hardwarestationen kan også installeres uafhængigt som et enkeltstående Microsoft Internet Information Services (IIS)-program. I så fald kan der opnås adgang via et netværk.

### <a name="hardware-profile"></a>Hardwareprofil

Navigation: Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardware-profiler**. Hardwareprofilen er en liste over enheder, der er konfigureret til et POS-kasseapparat eller en hardwarestation. Hardwareprofilen kan afbildes direkte til et POS-kasseapparat eller en hardwarestation.

## <a name="devices-classes"></a>Enhedsklasser
Eksterne POS-enheder er typisk opdelt i klasser. Dette afsnit beskriver og giver et overblik over de enheder, der understøttes af Modern POS.

### <a name="printer"></a>Printer

Printere omfatter traditionelle POS-bonprintere og helsidesprintere. Printeren understøttes via Object Linking and Embedding for Retail POS (OPOS) og Microsoft Windows driver-grænseflader. Der kan bruges op til to printere på samme tid. Denne funktion understøtter scenarier, hvor cash-and-carry-kundekvitteringer udskrives på bonprintere, hvorimod kundeordrer, der indeholder yderligere oplysninger, udskrives på en helsidesprinter. Bonprintere kan være tilsluttet direkte til en computer via USB, tilsluttet til et netværk via Ethernet eller tilsluttet via Bluetooth.

### <a name="scanner"></a>Scanner

Der kan bruges op til to stregkodescannere på samme tid. Denne funktion understøtter scenarier, hvor der kræves en scanner, som er mere mobil, til at scanne store eller tunge varer, hvorimod en fast integreret scanner bruges til de fleste varer af standardstørrelse for at give hurtigere ekspeditionstider. Scannere kan understøttes via grænseflader til OPOS, UWP (Universal Windows Platform) eller kreditkortlæsere. USB eller Bluetooth kan bruges til at tilslutte en scanner til en computer.

### <a name="msr"></a>Magnetstribelæser

Én USB-magnetstribelæser (MSR) kan konfigureres ved hjælp af OPOS-drivere. Hvis du vil bruge en enkeltstående MSR til betalingstransaktioner med elektronisk pengeoverførsel, skal MSR-enheden administreres af en betalingsconnector. Enkeltstående MSR'er kan bruges til registrering af kundefordelskort, medarbejderlogon og registrering af gavekort, uafhængigt af betalingsconnectoren.

### <a name="cash-drawer"></a>Pengeskuffe

To pengeskuffer kan understøttes pr. hardwareprofil. Denne funktion gør det muligt for to aktive skift pr. kasseapparat at være tilgængelige på samme tid. I tilfælde af et delt skift eller en pengeskuffe, der bruges af flere mobile POS-enheder på samme tid, tillades kun én pengeskuffe pr. hardwareprofil. Pengeskuffer kan være tilsluttet direkte til en computer via USB, tilsluttet til et netværk eller tilsluttet til en bonprinter via en RJ12-grænseflade. I nogle tilfælde kan pengeskuffer også tilsluttes via Bluetooth.

### <a name="line-display"></a>Linjevisning

Linjedisplay bruges til at vise produkter, transaktionssaldi og andre nyttige oplysninger til kunden under en transaktion. Der kan være tilsluttet ét linjedisplay til computeren via USB ved brug af OPOS-drivere.

### <a name="signature-capture"></a>Signaturhentning

Signaturhentningsenheder kan være tilsluttet direkte til en computer via USB ved brug af OPOS-drivere. Når signaturhentningen er konfigureret, bliver kunden bedt om at logge på enheden. Når signaturen er angivet, vises den til kassereren til accept.

### <a name="scale"></a>Vægt

Der kan være tilsluttet vægte til computeren via USP ved brug af OPOS-drivere. Når et produkt, der er markeret som et produkt med "Vejning" føjes til en transaktion, aflæser POS-enheden den målte vægt fra vægten, føjer produktet til transaktionen og bruger det antal, der leveres af vægten.

### <a name="pin-pad"></a>Pinkodetastatur

Tastaturer til PIN-koder understøttes via OPOS, men de skal administreres via en betalingsconnector.

### <a name="secondary-display"></a>Sekundær skærm

Når en sekundær skærm er konfigureret, bruges nummer 2 Windows-skærm til at vise grundlæggende oplysninger. Formålet med den sekundære skærm er at understøtte udvidelser fra uafhængige softwareproducenter, for i leveringstilstand kan den sekundære skærm ikke konfigureres, og den viser begrænset indhold.

### <a name="payment-device"></a>Betalingsenhed

Understøttelse af betalingsenheder er implementeret via betalingsconnectoren. Betalingsenheder kan udføre én eller flere af de funktioner, som andre enhedsklasser indeholder. For eksempel kan en betalingsenhed fungere som en MSR/kortlæser, linjevisning, signaturhentningsenhed eller PIN-tastatur. Understøttelse af betalingsenheder er implementeret uafhængigt af den understøttelse af selvstændige enheder, der leveres til andre enheder, der er inkluderet i hardwareprofilen.

## <a name="supported-interfaces"></a>Understøttede grænseflader
### <a name="opos"></a>OPOS

For at sikre, at det største udvalg af enheder kan bruges sammen med Microsoft Dynamics 365 for Retail, er OLE til POS-branchestandarden den primære platform for eksterne detailenheder, der understøttes i Microsoft Dynamics 365 for Retail. OLE til POS-standarden blev produceret af NRF (National Retail Federation), som fastlægger branchestandarden for kommunikationsprotokoller til eksterne detailenheder. OPOS er en alment vedtagen implementering af OLE til POS-standarden. Den blev udviklet i midten af 1990'erne og er blevet opdateret flere gange siden da. OPOS indeholder en enhedsdriverarkitektur, der sikrer nem integration af POS-hardware med Windows-baserede POS-systemer. OPOS-kontrolelementer styrer kommunikation mellem kompatibel hardware og POS-softwaren. Et OPOS-kontrolelement består af to dele:

-   **Kontrolobjekt** – Kontrolobjektet for en enhedsklasse (f.eks. linjevisninger) indeholder grænsefladen til programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) indeholder et standardiseret sæt af OPOS-kontrolobjekter, der er kendt som de fælles kontrolobjekter (CCO'er). CCO'erne bruges til at teste POS-komponenten af Microsoft Dynamics 365 for Retail. Derfor hjælper afprøvningen med til at garantere, at hvis Microsoft Dynamics 365 for Retail understøtter en enhedsklasse gennem OPOS, kan mange enhedstyper understøttes, forudsat at producenten leverer et serviceobjekt, der er bygget til OPOS. Du behøver ikke udtrykkeligt at teste hver enhedstype.
-   **Serviceobjekt** – Serviceobjektet kan bruges til kommunikation mellem kontrolobjektet (CCO) og enheden. Typisk leveres serviceobjektet til en enhed af enhedsproducenten. I nogle tilfælde kan det dog være nødvendigt at hente serviceobjektet fra producentens websted. Et nyere serviceobjekt kan f.eks. være tilgængeligt. Se dokumentationen til hardwaren for at finde adressen på producentens websted.

[![Kontrolobjekt og serviceobjekt](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Understøttelse af OPOS-implementeringen af OLE til POS hjælper med til at sikre, at hvis enhedsproducenterne og POS-udgiverne implementerer standarden korrekt, så kan POS-systemer og understøttede enheder arbejde sammen, selvom de ikke tidligere er testet sammen. **Bemærk:** OPOS-support garanterer ikke understøttelse af alle enheder, der har OPOS-drivere. Microsoft Dynamics 365 for Retail skal først understøtte den pågældende enhedstype eller -klasse gennem OPOS. Desuden er serviceobjekter muligvis ikke altid opdateret med den nyeste version af CCO'erne. Du skal også være opmærksom på, at kvaliteten af serviceobjekter generelt varierer.

### <a name="windows"></a>Windows

Udskrivning af kvitteringer i POS-enheden er optimeret til OPOS. OPOS har en tendens til at være meget hurtigere end udskrivning via Windows. Det er derfor en god ide at bruge OPOS, især i detailmiljøer, hvor der udskrives kvitteringer med 40 kolonner, og transaktionshastigheden skal være hurtig. Til de fleste enheder bruger du OPOS-kontrolelementer. Men nogle OPOS-bonprintere understøtter også Windows-drivere. Ved hjælp af en Windows-driver kan du få adgang til de nyeste skrifttyper og via netværk forbinde én printer til flere kasseapparater. Der er dog ulemper ved at bruge Windows-drivere. Her er nogle eksempler på disse ulemper:

-   Når der bruges Windows-drivere, gengives billeder, før udskrivningen sker. Derfor har udskrivningen en tendens til at være langsommere end på printere, der bruger OPOS-kontrolelementer.
-   Enheder, der er tilsluttet via printeren ("sammenkoblet") fungerer muligvis ikke korrekt, når der bruges Windows-drivere. F.eks. åbner pengeskuffen muligvis ikke, eller bilagsprinteren fungerer muligvis ikke som forventet.
-   OPOS understøtter også et mere omfattende sæt af variabler, der er specifikke for bonprintere i detailhandlen, f.eks. papirafskæring eller bilagsudskrivning.

Hvis OPOS-kontrolelementer er tilgængelige for den Windows-printer, du bruger, skulle printeren stadig fungere korrekt med Microsoft Dynamics 365 for Retail.

### <a name="universal-windows-platform"></a>Universel Windows-platform

UWP, for så vidt angår eksterne detailenheder, er relateret til understøttelse af Plug and Play-enheder i Windows. Når en Plug and Play-enhed tilsluttes til en Windows OS-version, som understøtter denne type enhed, kræves der ingen driver, for at enheden kan bruges som tilsigtet. Hvis Windows f.eks. registrerer en enhed med en Bluetooth-højttaler, ved operativsystemet, at enheden har klassetypen **Højttaler**. Derfor behandler det den pågældende enhed som en højttaler. Der kræves ikke yderligere opsætning. Hvad angår POS-enheder, kan mange USB-enheder tilsluttes, og Windows kan genkende dem som brugerstyrede inputenheder (HID'er). Operativsystemet er dog muligvis ikke i stand til at bestemme de funktioner, enheden indeholder, fordi enheden ikke angiver klassen eller typen af enhed. Enhedsklasser til stregkodescannere og MSR'er er blevet tilføjet i Windows 10. Hvis en enhed derfor erklærer sig selv over for Windows 10 som en enhed af en af disse klasser, vil Windows lytte efter hændelser fra enheden på passende tidspunkter. Modern POS understøtter UWP MSR'er og scannere. Når det er klar til input fra en af disse enheder, og en enhed, der hører til en af disse klasser, er tilsluttet, kan enheden bruges. Hvis en UWP-stregkodescanner f.eks. er tilsluttet en computer med Windows 10, og stregkodelogon er konfigureret til Modern POS, bliver stregkodescanneren aktiv på logonskærmen. Der kræves ikke yderligere opsætning. Flere klasser af POS-enheder til UWP føjes til Windows. Disse klasser omfatter klasser for pengeskuffer og bonprintere. Understøttelse af disse nye enhedsklasser i Modern POS afventer.

### <a name="keyboard-wedge"></a>Kreditkortlæser

Enheder til kreditkortlæsning sender data til computeren, som om dataene blev indtastet på et tastatur. Som standard vil feltet der er aktivt på POS-enheden, derfor modtage de data, der er scannet eller ført gennem kortlæseren. Denne funktionsmåde kan i nogle tilfælde medføre, at den forkerte type data scannes ind i det forkerte felt. En stregkode scannes f.eks. ind i et felt, der er beregnet til indtastning af kreditkortdata. I mange tilfælde er der logik i POS-enheden, der bestemmer, om de data, der er scannet eller ført gennem kortlæser, er en stregkode eller et kort, der er ført gennem kortlæseren. Derfor håndteres dataene korrekt. Men når enhederne er angivet som OPOS i stedet for som enheder til kreditkortlæsning, er der mere kontrol med, hvordan dataene fra disse enheder kan bruges, fordi der er større "kendskab" til den enhed, som dataene stammer fra. F.eks. genkendes data fra en stregkodescanner automatisk som en stregkode, og den tilknyttede post i databasen findes lettere og hurtigere, end hvis en søgning med generisk streng blev brugt, som det er tilfældet med enheder til kreditkortlæsning.

### <a name="native-printer"></a>Indbygget printer

Indbyggede (eller "Enheds", som typen er navngivet i hardwareprofilen) printere kan konfigureres til at bede brugeren om at vælge en printer, der er konfigureret til computeren. Når en printer af typen **Enhed** er konfigureret, bliver brugeren bedt om at vælge en printer på en liste, hvis Modern POS støder på en udskrivningskommando. Denne funktionsmåde adskiller sig fra funktionsmåden for Windows-drivere, da printertypen **Windows** i hardwareprofilen ikke viser en liste over printere. I stedet kræver det, at der angives en navngiven printer i feltet **Enhedsnavn**.

### <a name="windows"></a>Windows

Enhedstypen **Windows** bruges kun til printere. Når en Windows-printer er konfigureret i hardwareprofilen, skal det specifikke printernavn angives. Når Modern POS registrerer udskrivningshændelser, vil hændelsen blive overført til den angivne Windows-printer, hvis der er konfigureret en printer i Windows. Brugeren bliver ikke bedt om at vælge en printer.

### <a name="network"></a>Netværk

Netværksadresserbare pengeskuffer, bonprintere og betalingsterminaler kan bruges via et netværk, enten direkte via IPC-hardwarestationen (Interprocess Communications), der er indbygget i Modern POS til Windows-programmet eller via IIS-hardwarestationen til andre Modern POS-klienter.

## <a name="hardware-station-deployment-options"></a>Installationsindstillinger for hardwarestation
### <a name="ipc-built-in"></a>IPC (indbygget)

IPC-hardwarestationen er indbygget i Modern POS til Windows-programmet. Hvis du vil bruge IPC hardwarestationen, kan du tildele en hardwareprofil til et kasseapparat, som skal bruge Modern POS til Windows-programmet. Opret derefter en hardwarestation af typen **Dedikeret** til den butik, hvor registret skal bruges. Når du starter Modern POS, vil IPC-hardwarestationen være aktiv, og de eksterne POS-enheder, der er konfigureret, vil være klar til brug. Hvis du midlertidigt ikke har brug for den lokale hardware af en eller anden grund, kan du bruge handlingen **Administrer hardwarestationer** til at deaktivere hardwarestationens funktioner. Modern POS kan også bruge IPC-hardwarestationen til at kommunikere direkte med eksterne enheder på netværket.

### <a name="iis"></a>IIS

Du kan bruge IIS-versionen eller den enkeltstående version af hardwarestationen på to måder. Beskrivelsen "IIS" betyder, at POS-programmet har forbindelse til hardwarestationen via Microsoft Internet Information Services. POS-programmet opretter forbindelse til IIS-hardwarestationen via webtjenester, der kører på en computer, hvor enhederne er tilsluttet. Når du bruger IIS, kan de eksterne detailenheder, der er tilsluttet en hardwarestation, bruges af ethvert POS-kasseapparat, der er på samme netværk som IIS-hardwarestationen. Da kun Modern POS til Windows indeholder indbygget understøttelse af eksterne detailenheder, skal alle andre Modern POS-programmer bruge IIS-hardwarestationen til at kommunikere med eksterne POS-enheder, der er konfigureret i hardwareprofilen. Hver forekomst af IIS hardware station kræver derfor, at en computer, der kører webtjenesten, og et program, der kommunikerer med enhederne. IIS hardwarestationen er påkrævet til alle ikke-Windows Modern POS-programmer.

#### <a name="dedicated"></a>Dedikeret

Modern POS bruger hardwarestationer af typen **Dedikeret** til at registrere, at eksterne enheder har direkte forbindelse til den computer, hvor programmet anvendes. Men typen **Dedikeret** kan også bruges til IIS-hardwarestationer. I et traditionelt, fast POS-scenarie, der bruger Cloud POS som POS-programmet, bruges hardwarestationen af typen **Dedikeret** til IIS-hardwarestationer, som er installeret på samme computer, der kører Cloud POS. Set fra en ekstern detailenhed har den dedikerede IIS-hardwarestation bedre understøttelse af eksterne detailenheder til traditionelle faste POS-scenarier. Dedikerede hardwarestationer understøtter alle eksterne enheder, der understøttes i hardwareprofilen.

#### <a name="shared"></a>Delt

Fælles hardwarestationer er beregnet til at blive brugt af flere POS-enheder i løbet af dagen. Fælles hardwarestationer er optimeret til kun at understøtte pengeskuffer, bonprintere og betalingsterminaler. Du kan ikke direkte forbinde enkeltstående stregkodescannere, MSR'er, linjeskærme, vægte eller andre enheder. Ellers kan der opstå konflikter, når flere POS-enheder gør krav på disse enheder på samme tid. Sådan håndteres konflikter for understøttede enheder:

-   **Pengeskuffe** – Pengeskuffen åbnes via en hændelse, der sendes til enheden. Det eneste problem, der kan opstå, når en pengeskuffen kaldes, er, at pengeskuffen allerede er åben. Når der er tale om fælles hardwarestationer, skal pengeskuffen indstilles til **Delt** i hardwareprofilen. Denne indstilling forhindrer, at POS-enheden kontrollerer, om kassen allerede er åben, når der sendes Åbn-kommandoer.
-   **Bonprinter** – Hvis to kommandoer til bonudskrivning sendes til hardwarestationen på samme tid, kan en af kommandoerne gå tabt, afhængigt af enheden. Nogle enheder har intern hukommelse eller gruppering, der kan forhindre dette problem. Hvis en udskrivningskommando ikke lykkes, modtager kassereren en fejlmeddelelse og kan derefter gentage udskrivningskommandoen fra POS-enheden.
-   **Betalingsterminal** – Hvis en kasserer forsøger at modtage betaling for en transaktion på en betalingsterminal, der allerede bruges, giver en meddelelse kassereren besked om, at terminalen bruges, og kassereren bliver bedt om at prøve igen senere. Normalt kan kasserere se, at en terminal allerede er i brug, og venter, indtil den anden transaktion er fuldført, inden de forsøger at modtage betaling igen.

Validering er planlagt til en fremtidig version for at registrere, om ikke-understøttede enheder er konfigureret for en hardwareprofil, der er knyttet til en delt hardwarestation. Hvis der registreres ikke-understøttede enheder, vil brugeren modtage en meddelelse om, at enhederne ikke understøttes til fælles hardwarestationer. Hvis der er fælles hardwarestationer, er indstillingen **Vælg ved betaling** angivet til **Ja** på kasseapparatniveauet. POS-bruger bliver derefter bedt om at vælge en hardwarestation, når et betalingsmiddel vælges til en transaktion på POS-enheden. Hvis hardwarestationen kun vælges på betalingstidspunktet, føjes valget af hardwarestation direkte til POS-arbejdsgangen for mobile scenarier. Som en ekstra fordel bruges linjevisningen på betalingsterminalen ikke til delte scenarier. Hvis betalingsterminalen bruges som en linjevisning, forhindres andre brugere muligvis i at bruge den pågældende terminal, før transaktionen er fuldført. I mobile scenarier kan linjer føjes til en transaktion i en længere periode. Derfor er indstillingen **Vælg ved betaling** påkrævet for at sikre enhedens optimale tilgængelighed.

### <a name="network-peripherals"></a>Eksterne netværksenheder

Netværksangivelsen for enheder i hardwareprofilen, giver pengeskuffer, bonprintere og betalingsterminaler mulighed for at være forbundet via en netværksforbindelse.

#### <a name="modern-pos-for-windows"></a>Modern POS til Windows

Du kan angive IP-adresser til eksterne netværksenheder to steder. Hvis Windows-klienten til Modern POS bruger et enkelt sæt af eksterne netværksenheder, skal du angive IP-adresserne for disse enheder ved hjælp af indstillingen **IP-konfiguration** i handlingsruden for selve kasseapparatet. Hvis netværksenheder skal deles mellem POS-kasseapparater, kan en hardwareprofil, der har netværksenheder tilknyttet, afbildes direkte til en delt hardwarestation. For at tildele IP-adresser, skal du vælge den pågældende hardwarestation på siden **Detailbutikker** side og derefter bruge indstillingen **IP-konfiguration** i afsnittet **Hardwarestationer** til at angive de netværksenheder, der er knyttet til denne hardwarestation. For hardwarestationer, der kun har netværksenheder, behøver du ikke at installere selve hardwarestationen. I det tilfælde kræves hardwarestationen kun for begrebsmæssigt at gruppere netværksadresserbare enheder ud fra deres placering i detailbutikken.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloud POS, Modern POS til iOS og Modern POS til Android

Den logik, der styrer fysisk tilsluttede og netværksadresserbare eksterne enheder, findes i hardwarestationen. Til alle POS-klienter med undtagelse af Modern POS til Windows skal IIS-hardwarestationen være installeret og aktiv for at aktivere POS-enheden til at kommunikere med eksterne enheder, uanset om disse enheder er fysisk forbundet til en hardwarestation eller adresseres via netværket.

## <a name="setup-and-configuration"></a>Installation og konfiguration
### <a name="hardware-station-installation"></a>Installation af hardwarestation

Du kan finde flere oplysninger i [Konfiguration og installation af hardwarestation til detail](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Installation og konfiguration af Modern POS til Windows

Du kan finde flere oplysninger i [Konfiguration og installation af Retail Modern POS](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>Installation og konfiguration af OPOS-enhed

Du kan finde flere oplysninger om OPOS-komponenter i afsnittet "Understøttede grænseflader" i dette dokument. Typisk leveres OPOS-drivere af producenten af enheden. Når der installeres en OPOS-enhedsdriver, føjer den en nøgle til Windows-registreringsdatabasen på en af følgende placeringer:

-   **32-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Konfigurerede enheder er organiseret efter enhedsklassen OPOS inden for lokaliteten for registreringsdatabasen ServiceOPOS. Flere enhedsdrivere gemmes.

## <a name="supported-scenarios-by-hardware-station-type"></a>Understøttede scenarier efter hardwarestationstype
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Understøttelse af klienter – IPC-hardwarestation vs. IIS-hardwarestation

Følgende tabel viser de topologier og installationsscenarier, der understøttes.

| Klient      | IPC-hardwarestation | IIS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

### <a name="network-peripherals"></a>Eksterne netværksenheder

Netværksenheder understøttes direkte via den hardwarestation, der er indbygget i Modern POS til Windows-programmet. Til alle andre klienter skal du installere en IIS-hardwarestation.

| Klient      | IPC-hardwarestation | IIS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Understøttede enhedstyper efter hardwarestationstype
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS til Windows med en IPC-hardwarestation (indbygget)

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
<li>UWP (opsætning er ikke nødvendig).</li>
<li>Kreditkortlæser (opsætning er ikke nødvendig).</li>
</ul></td>
</tr>
<tr class="even">
<td>Vekseludsteder</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> Der kan kun konfigureres én skuffe, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kasseskuffe 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk <strong>Bemærk:</strong> Der kan kun konfigureres én skuffe, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (opsætning er ikke nødvendig).</li>
<li>Kreditkortlæser (opsætning er ikke nødvendig).</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (opsætning er ikke nødvendig).</li>
<li>Kreditkortlæser (opsætning er ikke nødvendig).</li>
</ul></td>
</tr>
<tr class="even">
<td>Vægt</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Pinkodetastatur</td>
<td>OPOS (Support ydes gennem tilpasning af betalingsconnectorer).</td>
</tr>
<tr class="even">
<td>Signaturhentning</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal</td>
<td><ul>
<li>Understøttelse af brugerdefineret enhed</li>
<li>Netværk (Du kan finde yderligere oplysninger i dokumentationen til betalingsconnectorer).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle Modern POS-klienter, der har en dedikeret IIS-hardwarestation

**Bemærk:** Når IIS-hardwarestationen er "dedikeret", er der en én til én-relation mellem POS-klienten og hardwarestationen.

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
<li>Windows-driver <strong>Bemærk:</strong> Til Windows-printere på et netværk skal brugeren af hardwarestationen have rettighed til at få adgang til printeren.</li>
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
<li>Netværk <strong>Bemærk:</strong> Der kan kun konfigureres én skuffe pr. hardwareprofil, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
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
<td>Vægt</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Pinkodetastatur</td>
<td>OPOS (Support ydes gennem tilpasning af betalingsconnectorer).</td>
</tr>
<tr class="odd">
<td>Sig. hente</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal</td>
<td><ul>
<li>Understøttelse af brugerdefineret enhed</li>
<li>Netværk (Du kan finde yderligere oplysninger i dokumentationen til betalingsconnectorer).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter, der har en delt IIS-hardwarestation

**Bemærk:** Når IIS-hardwarestationen er "delt", kan flere enheder bruge hardwarestationen på samme tid. I dette scenarie skal du kun bruge de enheder, der er angivet i følgende tabel. Hvis du forsøger at dele enheder, der ikke er angivet her, f.eks. stregkodescannere og MSR'er, opstår der fejl, når flere enheder forsøger at gøre krav på den samme eksterne enhed. I fremtiden forhindres en sådan konfiguration udtrykkeligt.

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
<li>Windows-driver <strong>Bemærk:</strong> Til Windows-printere på et netværk skal brugeren af hardwarestationen have rettighed til at få adgang til printeren.</li>
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
<li>Netværk <strong>Bemærk:</strong> Der kan kun konfigureres én skuffe pr. hardwareprofil, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
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
<td>Betalingsterminal</td>
<td><ul>
<li>Understøttelse af brugerdefineret enhed</li>
<li>Netværk (Du kan finde yderligere oplysninger i dokumentationen til betalingsconnectorer).</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfiguration til understøttede scenarier
Du kan finde flere oplysninger om, hvordan du oprette hardwareprofiler i [Definer og vedligehold kanalklienter, herunder registre og hardwarestationer](define-maintain-channel-clients-registers-hw-stations.md). **Bemærk:** I Microsoft Dynamics 365 for Retail version 1611 bruges hardwarestationsprofilen ikke længere. Attributter, som du tidligere har konfigureret i hardwarestationsprofilen, er nu en del af selve hardwarestationen.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS til Windows med en IPC-hardwarestation (indbygget)

Denne konfiguration er den mest typiske konfiguration for traditionelle, faste POS-kasseapparater. I dette scenarie er hardwareprofiloplysningerne knyttet direkte til selve kasseapparatet. EFT-terminalnummeret bør også angives i selve registeret. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor alle de nødvendige eksterne enheder er konfigureret.
2.  Tilknyt hardwareprofilen til POS-kasseapparatet.
3.  Opret en hardwarestation af typen **Dedikeret** til den detailbutik, hvor POS-kasseapparatet skal bruges. En beskrivelse er valgfri. **Bemærk:** Du behøver ikke at angive andre egenskaber for hardwarestationen. Alle andre nødvendige oplysninger, f.eks. hardwareprofilen, kommer fra selve kasseapparatet.
4.  Klik på **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
5.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
6.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Installer og aktivér Modern POS til Windows.
8.  Start Modern POS til Windows, og begynd at bruge de tilsluttede eksterne enheder.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle Modern POS-klienter, der har en dedikeret IIS-hardwarestation

Denne konfiguration kan bruges til alle Modern POS-klienter, der har en hardwarestation, der bruges udelukkende af ét POS-kasseapparat. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor alle de nødvendige eksterne enheder er konfigureret.
2.  Opret en hardwarestation af typen **Dedikeret** til den detailbutik, hvor POS-kasseapparatet skal bruges.
3.  På den dedikerede hardwarestation skal du angive følgende egenskaber:
    -   **Værtsnavn** – Navnet på den værtscomputer, hvor hardwarestationen skal køre. **Bemærk:** Cloud POS kan fortolke **localhost** for at bestemme den lokale computer, hvor Cloud POS kører. Men det certifikat, der kræves for at parre Cloud POS med hardwarestationen, skal dog også have "Localhost" som navnet på computeren. For at undgå problemer anbefaler vi, at du efter behov angiver en forekomst af hver dedikeret hardwarestation for butikken. For hver hardwarestation skal værtsnavnet være det specifikke computernavn, hvor hardwarestationen skal installeres.
    -   **Port** – Den port, der skal bruges af hardwarestationen til at kommunikere med Modern POS-klienten.
    -   **Hardwareprofil** – Hvis hardwareprofilen ikke er angivet på selve hardwarestationen, bruges den hardwareprofil, der er tildelt til kasseapparatet.
    -   **Elektronisk pengeoverførsel POS-nummer** – Det terminal-id til elektronisk pengeoverførsel, der skal bruges, når godkendelser af elektronisk pengeoverførsel sendes. Dette id leveres af kreditkortprocessoren.
    -   **Pakkenavn** – Den hardwarestationspakke, der skal bruges, når hardwarestationen installeres.

4.  Klik på **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
5.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
6.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Installer hardwarestationen. Du kan finde flere oplysninger om, hvordan du installerer hardwarestationen i [Konfiguration og installation af hardwarestation til detail](retail-hardware-station-configuration-installation.md).
8.  Installer og aktivér Modern POS. Du kan finde flere oplysninger om, hvordan du installerer Modern POS i [Konfiguration og installation af Retail Modern POS](retail-modern-pos-device-activation.md).
9.  Log på Modern POS, og vælg **Udfør handlinger uden om kasseskuffen.**.
10. Start handlingen **Administrer hardwarestationer**.
11. Klik på **Administrer**.
12. Angiv indstillingen for at slå hardwarestationen til på siden til administration af hardwarestation.
13. Vælg den hardwarestation, der skal bruges, og klik derefter på **Par**.
14. Når hardwarestationen er parret, skal du klikke på **Luk**.
15. Klik på den senest valgte hardwarestation på siden til valg af hardwarestation for at gøre den aktiv.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter, der har en delt IIS-hardwarestation

Denne konfiguration kan bruges til alle Modern POS-klienter, der deler hardwarestationer med andre enheder. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor de nødvendige eksterne enheder er konfigureret.
2.  Opret en hardwarestation af typen **Delt** til den detailbutik, hvor POS-kasseapparatet skal bruges.
3.  På den delte hardwarestation skal du angive følgende egenskaber:
    -   **Værtsnavn** – Navnet på den værtscomputer, hvor hardwarestationen skal køre.
    -   **Beskrivelse** – Tekst, der hjælper med til at identificere hardwarestationen, f.eks. **Returneringer** eller **Foran i butikken**.
    -   **Port** – Den port, der skal bruges af hardwarestationen til at kommunikere med Modern POS-klienten.
    -   **Hardwareprofil** – For delte hardwarestationer skal hver hardwarestation have en hardwareprofil. Hardwareprofiler kan deles mellem hardwarestationer, men de skal være knyttet til hver hardwarestation. Vi anbefaler desuden, at du bruger delte skift, når flere enheder bruger den samme delte hardwarestation. Hvis du vil konfigurere et delt skift, skal du klikke på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**. For hver delt hardwareprofil skal du vælge pengeskuffen og angive indstillingen **Skuffe til delt skift** til **Ja**.
    -   **Elektronisk pengeoverførsel POS-nummer** – Det terminal-id til elektronisk pengeoverførsel, der skal bruges, når godkendelser af elektronisk pengeoverførsel sendes. Dette id leveres af kreditkortprocessoren.
    -   **Pakkenavn** – Den hardwarestationspakke, der skal bruges, når hardwarestationen installeres.

4.  Gentag trinene 2 og 3 for hver yderligere hardwarestation, der skal bruges i butikken.
5.  Klik på **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.
6.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.
8.  Installer hardwarestationen på hver værtscomputer, du har oprettet i trin 2 og 3. Du kan finde flere oplysninger om, hvordan du installerer hardwarestationen i [Konfiguration og installation af hardwarestation til detail](retail-hardware-station-configuration-installation.md).
9.  Installer og aktivér Modern POS. Du kan finde flere oplysninger om, hvordan du installerer Modern POS i [Konfiguration og installation af Retail Modern POS](retail-modern-pos-device-activation.md).
10. Log på Modern POS, og vælg **Udfør handlinger uden om kasseskuffen.**.
11. Start handlingen **Administrer hardwarestationer**.

12. Klik på **Administrer**.
13. Angiv indstillingen for at slå hardwarestationen til på siden til administration af hardwarestation.
14. Vælg den hardwarestation, der skal bruges, og klik derefter på **Par**.
15. Gentag trin 14 for hver hardwarestation, som Modern POS bruger.
16. Når alle de påkrævede hardwarestationer er parret, skal du klikke på **Luk**.
17. Klik på den senest valgte hardwarestation på siden til valg af hardwarestation for at gøre den aktiv. **Bemærk:** Hvis enheder ofte bruger forskellige hardwarestationer, anbefaler vi, at du konfigurerer Modern POS til at bede kassereren om at vælge en hardwarestation, når de begynder betalingsprocessen. Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**. Vælg kasseapparatet, og angiv derefter indstillingen **Vælg ved betaling** til **Ja**. Brug distributionsplanen **1090** til at synkronisere ændringerne til kanaldatabasen.

## <a name="extensibility"></a>Udvidelsesmuligheder
Du kan finde oplysninger om scenarier med udvidelsesmuligheder for hardwarestationen i [Udvidelsesmuligheder for hardwarestation](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sikkerhed
I henhold til de aktuelle sikkerhedsstandarder, skal følgende indstillinger bruges i et produktionsmiljø: **Bemærk:** Installationsprogrammet for hardwarestationen foretager automatisk disse redigeringer i registreringsdatabasen som en del af installationen via selvbetjening.

-   SSL (Secure Sockets Layer) skal deaktiveres.
-   Kun TLS (Transport Layer Security) version 1.2 (eller den aktuelle højeste version) skal aktiveres og anvendes. **Bemærk:** Som standard er SSL og alle version af TLS, undtagen TLS 1.2, deaktiveret. Hvis du vil redigere eller aktivere disse værdier, skal du følge disse trin:
    1.  Tryk på Windows-logotasten + R for at åbne et **Kør**-vindue.
    2.  I feltet **Åbn** skal du skrive **Regedit** og derefter klikke på **OK**.
    3.  Hvis meddelelsesboksen **Kontrol af brugerkonti** vises, skal du klikke på **Ja**.
    4.  I vinduet **Registreringseditor** skal du gå til **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Følgende taster er indsat automatisk for kun at tillade TLS 1.2:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Ingen yderligere netværksporte må være åbne, medmindre de er påkrævede af kendte, angivne grunde.
-   Deling af ressourcer på tværs af oprindelse skal deaktiveres, og skal angive de tilladte oprindelser, der er godkendt.
-   Kun de nøglecentre, der er tillid til, skal bruges til at hente certifikater, der skal bruges på computere, der kører hardwarestationen.

**Bemærk:** Det er meget vigtigt, at du gennemgår sikkerhedsretningslinjer for IIS og PCI-kravene (Payment Card Industry).

## <a name="peripheral-simulator"></a>Ekstern simulator
Du kan finde oplysninger under [Simulator for eksterne detailenheder](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsoft-testede eksterne enheder
### <a name="ipc-built-in-hardware-station"></a>IPC-hardwarestation (indbygget)

De følgende eksterne enheder blev testet ved hjælp af den IPC-hardwarestation, der er indbygget i Modern POS til Windows.

#### <a name="printer"></a>Printer

| Producent | Model    | Interface | Bemærkninger                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket   |
| Star         | mPOP     | OPOS      | Tilsluttet via Bluetooth |
| HP           | F7M67AA  | OPOS      | Drevet via USB             |

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Producent  | Model         | Interface | Bemærkninger |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Tegn        | LS2208        | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>Pinkodetastatur

| Producent | Model  | Interface | Bemærkninger                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Kræver tilpasning af betalingsconnector |

#### <a name="payment-terminal"></a>Betalingsterminal

| Producent | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Brugerdefineret    | Kræver tilpasning af betalingsconnector                                |
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tilsluttet via Bluetooth |
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Linjevisning

| Producent  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| HP integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturhentning

| Producent | Model  | Interface | Bemærkninger |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vægt

| Producent | Model         | Interface | Bemærkninger |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetstribelæser

| Producent | Model       | Interface | Bemærkninger |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Dedikeret IIS-hardwarestation

De følgende enheder blev testet ved hjælp af en dedikeret (ikke delt) IIS-hardwarestation samt Modern POS til Windows og Cloud POS.

#### <a name="printer"></a>Printer

| Producent | Model    | Interface | Bemærkninger                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket     |
| Star         | TSP100   | OPOS      | Kræver TSP650II-drivere |
| HP           | F7M67AA  | OPOS      | Drevet via USB               |

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Producent  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Tegn        | LS2208  | OPOS      |          |
| HP Integrated | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>Pinkodetastatur

| Producent | Model  | Interface | Bemærkninger                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Kræver tilpasning af betalingsconnector |

#### <a name="payment-terminal"></a>Betalingsterminal

| Producent | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Brugerdefineret    | Kræver tilpasning af betalingsconnector                                |
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Linjevisning

| Producent  | Model   | Interface | Bemærkninger |
|---------------|---------|-----------|----------|
| HP integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturhentning

| Producent | Model  | Interface | Bemærkninger |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vægt

| Producent | Model         | Interface | Bemærkninger |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetstribelæser

| Producent | Model       | Interface | Bemærkninger |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Delt IIS-hardwarestation

De følgende eksterne enheder blev testet ved hjælp af en delt IIS-hardwarestation samt Modern POS til Windows og Cloud POS. **Bemærk:** Kun en printer, en betalingsterminal og en pengeskuffe understøttes.

#### <a name="printer"></a>Printer

| Producent | Model    | Interface | Bemærkninger                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket     |
| Star         | TSP100   | OPOS      | Kræver TSP650II-drivere |
| HP           | F7M67AA  | OPOS      | Drevet via USB               |

#### <a name="payment-terminal"></a>Betalingsterminal

| Producent | Model | Interface | Bemærkninger                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |
| VeriFone     | MX915 | Brugerdefineret    | Kræver tilpasning af betalingsconnector, forbundet via netværk og USB |

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Fejlfinding
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kan registrere hardwarestationen på valglisten, men det kan ikke fuldføre parringen

**Løsning:** Kontrollér følgende liste over mulige fejlpunkter:

-   Den computer, der kører Modern POS har tillid til det certifikat, der bruges på den computer, der kører hardwarestationen.
    -   For at kontrollere denne opsætning i en webbrowser, skal du gå til følgende URL-adresse: https://&lt;computernavn&gt;:&lt;portnummer&gt;/HardwareStation/ping.
    -   Denne URL-adresse bruger et ping til at kontrollere, at du kan få adgang til computeren, og browseren angiver, om der er tillid til certifikatet. (F.eks. vises i Internet Explorer et låseikon på adresselinjen. Når du klikker på dette ikon, kontrollerer Internet Explorer, om der i øjeblikket er tillid til certifikatet. Du kan installere certifikatet på den lokale computer ved at få vist detaljer om det certifikat, der er vist.)
-   På den computer, der kører hardwarestationen, er den port, der bruges af hardwarestationen åben i firewall'en.
-   Hardwarestationen har installeret forhandlerkontooplysninger korrekt ved hjælp af værktøjet Installér forhandleroplysninger, der køres i slutningen af installationsprogrammet til hardwarestationen.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS kan ikke registrere hardwarestationen på valglisten

**Løsning:** En af følgende faktorer kan forårsage dette problem:

-   Hardwarestationen er endnu ikke blevet konfigureret korrekt i hovedsædet. Brug trinnene tidligere i dette emne til at kontrollere, at hardwarestationsprofilen og hardwarestationen er angivet korrekt.
-   Job til opdatering af kanalkonfigurationen har ikke været kørt. I dette tilfælde skal du køre job 1070 til kanalkonfiguration.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS afspejle ikke nye indstillinger for kontantskuffe

**Løsning:** Luk den aktuelle batch. Ændringer til kontantskuffen opdateres ikke i Modern POS, før den aktuelle batch er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS rapporterer et problem med en eksterne detailenhed

**Løsning:** Her er nogle typiske årsager til problemet:

-   Kontrollér, at andre konfigurationsværktøjer til enhedsdrivere er lukket. Hvis disse værktøjer er åbne, kan de forhindre Modern POS eller hardwarestationen i at gøre krav på enheden.
-   Hvis den eksterne detailenhed deles med flere POS-enheder, skal du kontrollere, at den tilhører en af følgende kategorier:
    -   Pengeskuffe
    -   Printer til modtagelse
    -   Betalingsterminal

    Hvis den eksterne enhed ikke tilhører en af disse kategorier, er hardwarestationen ikke beregnet til at aktivere den eksterne enhed til at blive delt mellem flere POS-enheder.
-   Nogle gange kan enhedsdrivere forårsage, at de fælles kontrolobjekter (CCO'er) holder op med at fungere korrekt. Hvis en enhed er blevet installeret for nylig, men den ikke fungerer korrekt, eller du bemærker andre problemer, kan du ofte løse problemet ved at geninstallere CCO'erne. Du kan hente CCO'erne på <http://monroecs.com/oposccos_current.htm>.
-   Hvis du foretager hyppige ændringer af eksterne enheder under test eller fejlfinding, skal du muligvis nulstille IIS i stedet for at vente på, at cachen opdaterer sig selv. Følg disse trin for at nulstille IIS:
    1.  Fra menuen **Start** skal du skrive **CMD**.
    2.  I søgeresultaterne, skal du højreklikke på **Kommandoprompt**, og derefter klikke på **Kør som administrator**.
    3.  I vinduet **Kommandoprompt** skal du skrive **iisreset/Restart** og derefter trykke på Enter.
    4.  Når IIS er genstartet, skal du genstarte Modern POS.
-   Hvis du foretager hyppige ændringer af eksterne enheder, og hvis du også ofte starter og lukker POS-klienten, kan dllhost-processen fra en tidligere POS-session forstyrre den aktuelle session. I dette tilfælde kan en enhed ikke bruges, før du lukker DLL-værten (dynamic-link library), der styrer den forrige session. Følg disse trin for at lukke DLL-værten:
    1.  Fra menuen **Start** skal du skrive **Jobliste**.
    2.  I søgeresultaterne, skal du klikke på **Jobliste**.
    3.  I Jobliste under fanen **Detaljer** skal du klikke på kolonneoverskriften, der hedder **Navn** at sortere tabellen alfabetisk efter navn.
    4.  Rul ned, indtil du finder dllhost.exe.
    5.  Vælg hver DLL-vært, og klik derefter på **Afslut job**.
    6.  Når DLL-værterne er blevet lukket, genstarter du Modern POS.


<a name="see-also"></a>Se også
--------

[Simulator for eksterne detailenheder](dev-itpro/retail-peripheral-simulator.md)




