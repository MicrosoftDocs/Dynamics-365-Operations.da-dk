---
title: Eksterne enheder
description: Denne artikel forklarer begreberne i forbindelse med eksterne Commerce-enheder.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459986"
---
# <a name="peripherals"></a>Eksterne enheder

[!include[banner](includes/banner.md)]

Denne artikel beskriver begreberne i forbindelse med eksterne butiksenheder. Det beskriver de forskellige måder, at eksterne enheder kan forbindes til POS-enheden, og komponenterne, der er ansvarlige for administration af forbindelsen med POS-enheden.

## <a name="concepts"></a>Begreber

### <a name="pos-registers"></a>Kasseapparater

Navigation: Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Kasseapparater**. POS-kasseapparat er en enhed, der bruges til at definere egenskaberne for en bestemt forekomst af POS-enheden. Disse egenskaber omfatter hardwareprofilen eller opsætningen af eksterne enheder, der skal bruges ved kasseapparatet, den butik, som kasseapparatet er tilknyttet, og den visuelle oplevelse for den bruger, der logger på kasseapparatet.

### <a name="devices"></a>Enheder

Navigation: Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Enheder**. En enhed repræsenterer en fysisk forekomst af en enhed, der er knyttet til et POS-kasseapparat. Når der oprettes en enhed, knyttes den til et POS-kasseapparat. Enheden registrerer oplysninger om, hvornår et POS-kasseapparat aktiveres, den klienttype, som benyttes, og den programpakke, der er blevet installeret på en bestemt enhed. 

Enheder kan knyttes til følgende programtyper: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Android og Retail Modern POS – iOS.

### <a name="modern-pos"></a>Moderne POS

Modern POS er POS-programmet til Microsoft Windows. Det kan anvendes på Windows 10- og Windows 11-operativsystemer.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS er en browserbaseret version af Modern POS-programmet, der kan åbnes i en webbrowser.

### <a name="modern-pos-for-ios"></a>Modern POS til iOS

Modern POS til iOS er en iOS-baseret version af Modern POS-programmet, der kan implementeres på iOS-enheder.

### <a name="modern-pos-for-android"></a>Modern POS til Android

Modern POS til Android er en Android-baseret version af Modern POS-programmet, der kan implementeres på Android-enheder.

### <a name="pos-peripherals"></a>Eksterne POS-enheder

Eksterne POS-enheder er enheder, der udtrykkeligt understøttes til POS-funktioner. Disse eksterne enheder er typisk opdelt i bestemte klasser. Du kan finde yderligere oplysninger om disse klasser i afsnittet "Enhedsklasser" i denne artikel.

### <a name="hardware-station"></a>Hardwarestation

Navigation: Gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker**. Vælg en butik, og vælg derefter oversigtspanelet **Hardwarestationer**. Indstillingen **Hardwarestation** er en indstilling på kanalniveau, der bruges til at definere forekomster, hvor logikken for eksterne enheder skal implementeres. Denne indstilling på kanalniveau bruges til at bestemme karakteristika for hardwarestationen. Den bruges også til at angive de hardwarestationer, der er tilgængelige for en Modern POS-forekomst i en given butik. Hardwarestationen er indbygget i Modern POS-programmer til Windows og Android. Hardwarestationen kan også installeres uafhængigt som et enkeltstående Microsoft Internet Information Services (IIS)-program. I så fald kan der skaffes adgang via et netværk.

### <a name="hardware-profile"></a>Hardwareprofil

Navigation: Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. Hardwareprofilen er en liste over enheder, der er konfigureret til et POS-kasseapparat eller en hardwarestation. Hardwareprofilen kan afbildes direkte til et POS-kasseapparat eller en hardwarestation.

## <a name="devices-classes"></a>Enhedsklasser
Eksterne POS-enheder er typisk opdelt i klasser. Dette afsnit beskriver og giver et overblik over de enheder, der understøttes af Modern POS.

### <a name="printer"></a>Printer

Printere omfatter traditionelle POS-bonprintere og helsidesprintere. Printere understøttes via objektsammenkædning og -integrering (Object Linking and Embedding – OLE) for Retail POS (OPOS) og Microsoft Windows-drivergrænseflader. Der kan bruges op til to printere på samme tid. Denne funktion understøtter scenarier, hvor cash-and-carry-kundekvitteringer udskrives på bonprintere, hvorimod kundeordrer, der indeholder yderligere oplysninger, udskrives på en helsidesprinter. Bonprintere kan være tilsluttet direkte til en computer via USB, tilsluttet til et netværk via Ethernet eller tilsluttet via Bluetooth.

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

### <a name="scale"></a>Målestok

Der kan være tilsluttet vægte til computeren via USB ved brug af OPOS-drivere. Når et produkt, der er markeret som et produkt med "Vejning" føjes til en transaktion, aflæser POS-enheden den målte vægt fra vægten, føjer produktet til transaktionen og bruger det antal, der leveres af vægten.

### <a name="pin-pad"></a>Pinkodetastatur

Tastaturer til PIN-koder understøttes via OPOS, men de skal administreres via en betalingsconnector.

### <a name="secondary-display"></a>Sekundær skærm

Når en sekundær skærm er konfigureret, bruges nummer 2 Windows-skærm til at vise grundlæggende oplysninger. Som standard kan den sekundære visning ikke konfigureres og viser begrænset indhold. Formålet med den sekundære visning er at understøtte en uafhængig softwareleverandørudvidelse. 

### <a name="payment-device"></a>Betalingsenhed

Understøttelse af betalingsenheder er implementeret via betalingsconnectoren. Betalingsenheder kan udføre én eller flere af de funktioner, som andre enhedsklasser indeholder. For eksempel kan en betalingsenhed fungere som en MSR/kortlæser, linjevisning, signaturhentningsenhed eller PIN-tastatur. Understøttelse af betalingsenheder er implementeret uafhængigt af den understøttelse af selvstændige enheder, der leveres til andre enheder, der er inkluderet i hardwareprofilen.

## <a name="supported-interfaces"></a>Understøttede grænseflader
### <a name="opos"></a>OPOS

OLE til POS-branchestandarden er den primære platform for eksterne enheder, der understøttes, for at sikre, at det største udvalg af enheder kan bruges sammen med Commerce. OLE til POS-standarden blev produceret af NRF (National Retail Federation), som fastlægger branchestandarden for kommunikationsprotokoller til eksterne enheder. OPOS er en alment vedtagen implementering af OLE til POS-standarden. Den blev udviklet i midten af 1990'erne og er blevet opdateret flere gange siden da. OPOS indeholder en enhedsdriverarkitektur, der sikrer nem integration af POS-hardware med Windows-baserede POS-systemer. OPOS-kontrolelementer styrer kommunikation mellem kompatibel hardware og POS-softwaren. Et OPOS-kontrolelement består af to dele:

-   **Kontrolobjekt** – Kontrolobjektet for en enhedsklasse (f.eks. linjevisninger) indeholder grænsefladen til programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) indeholder et standardiseret sæt af OPOS-kontrolobjekter, der er kendt som de fælles kontrolobjekter (CCO'er). CCO'er bruges til at teste POS-komponenten i Commerce. Derfor er afprøvningen med til at garantere, at hvis Commerce understøtter en enhedsklasse gennem OPOS, kan mange enhedstyper understøttes, forudsat at producenten leverer et serviceobjekt, der er bygget til OPOS. Du behøver ikke udtrykkeligt at teste hver enhedstype.
-   **Serviceobjekt** – Serviceobjektet kan bruges til kommunikation mellem kontrolobjektet (CCO) og enheden. Typisk leveres serviceobjektet til en enhed af enhedsproducenten. I nogle tilfælde kan det dog være nødvendigt at hente serviceobjektet fra producentens websted. Et nyere serviceobjekt kan f.eks. være tilgængeligt. Se dokumentationen til hardwaren for at finde adressen på producentens websted.

[![Kontrolobjekt og serviceobjekt.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Understøttelse af OPOS-implementeringen af OLE til POS hjælper med til at sikre, at hvis enhedsproducenterne og POS-udgiverne implementerer standarden korrekt, så kan POS-systemer og understøttede enheder arbejde sammen, selvom de ikke tidligere er testet sammen. 

> [!NOTE]
> OPOS-support garanterer ikke understøttelse af alle enheder, der har OPOS-drivere. Commerce skal først understøtte den pågældende enhedstype eller klasse via OPOS. Desuden er serviceobjekter muligvis ikke altid opdateret med den nyeste version af CCO'erne. Du skal også være opmærksom på, at kvaliteten af serviceobjekter generelt varierer.

### <a name="windows"></a>Windows

Udskrivning af kvitteringer i POS-enheden er optimeret til OPOS. OPOS har en tendens til at være meget hurtigere end udskrivning via Windows. Det er derfor en god ide at bruge OPOS, især i miljøer, hvor der udskrives kvitteringer med 40 kolonner, og transaktionshastigheden skal være hurtig. Til de fleste enheder bruger du OPOS-kontrolelementer. Men nogle OPOS-bonprintere understøtter også Windows-drivere. Ved hjælp af en Windows-driver kan du få adgang til de nyeste skrifttyper og via netværk forbinde én printer til flere kasseapparater. Der er dog ulemper ved at bruge Windows-drivere. Her er nogle eksempler på disse ulemper:

-   Når der bruges Windows-drivere, gengives billeder, før udskrivningen sker. Derfor har udskrivningen en tendens til at være langsommere end på printere, der bruger OPOS-kontrolelementer.
-   Enheder, der er tilsluttet via printeren ("sammenkoblet") fungerer muligvis ikke korrekt, når der bruges Windows-drivere. F.eks. åbner pengeskuffen muligvis ikke, eller kvitteringsprinteren fungerer muligvis ikke som forventet.
-   OPOS understøtter også et mere omfattende sæt af variabler, der er specifikke for bonprintere i handlen, f.eks. papirafskæring eller bilagsudskrivning.
-   Windows-printere understøttes ikke via IIS-hardwarestationen. 

Hvis OPOS-kontrolelementer er tilgængelige for den Windows-printer, du bruger, skulle printeren stadig fungere korrekt med Commerce.

### <a name="plug-and-play-devices"></a>Plug and play-enheder

Når en plug and play-enhed tilsluttes til en Windows OS-version, som understøtter denne type enhed, kræves der ingen driver, for at enheden kan bruges som tilsigtet. Hvis Windows f.eks. registrerer en enhed med en Bluetooth-højttaler, ved operativsystemet, at enheden har klassetypen "Højttaler" og behandler enheden som en højttaler. Der kræves ikke yderligere opsætning. 

Hvad angår ydre POS-enheder, kan mange USB-enheder tilsluttes og genkendes af Windows som brugerstyrede inputenheder (HID'er). Windows er dog muligvis ikke i stand til at bestemme de funktioner, enheden indeholder, fordi enheden ikke angiver klassen eller typen af enhed. Enhedsklasser til stregkodescannere og MSR'er er blevet tilføjet i Windows 10. Hvis en enhed derfor erklærer sig selv over for Windows 10 som en enhed af en af disse klasser, vil Windows lytte efter hændelser fra enheden på passende tidspunkter.

Modern POS understøtter UWP MSR'er og scannere. Når Modern POS er klar til input fra en af disse enheder, og en enhed, der hører til en af disse enhedsklasser, er tilsluttet, kan enheden bruges. Hvis en plug and play-stregkodescanner f.eks. er tilsluttet en computer med Windows 10, og stregkodelogon er konfigureret til Modern POS, bliver stregkodescanneren aktiv på logonsiden. Der kræves ikke yderligere opsætning.

Der føjes yderligere klasser af eksterne POS-enheder til Windows, f.eks. klasser for kasseskuffer og kvitteringsprintere. Understøttelse af disse nye enhedsklasser i Modern POS afventer.

> [!NOTE] 
> Visse USB-enheder kan blive upålidelige eller upålidelige, når de administreres af en Windows 10-strømstyringsfunktion, der kaldes [USB Selective Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend). Hvis en ekstern USB-enhed ikke længere kan reagere, kan det være nødvendigt at deaktivere den selektive suspenderingsfunktion for den pågældende enhed. Du kan finde flere oplysninger i [Aktivering af Selective Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Kreditkortlæser

Enheder til kreditkortlæsning sender data til computeren, som om dataene blev indtastet på et tastatur. Som standard vil feltet der er aktivt på POS-enheden, derfor modtage de data, der er scannet eller ført gennem kortlæseren. Denne funktionsmåde kan i nogle tilfælde medføre, at den forkerte type data scannes ind i det forkerte felt. En stregkode scannes f.eks. ind i et felt, der er beregnet til indtastning af kreditkortdata. I mange tilfælde er der logik i POS-enheden, der bestemmer, om de data, der er scannet eller ført gennem kortlæser, er en stregkode eller et kort, der er ført gennem kortlæseren. Derfor håndteres dataene korrekt. Men når enhederne er angivet som OPOS i stedet for som enheder til kreditkortlæsning, er der mere kontrol med, hvordan dataene fra disse enheder kan bruges, fordi der er større "kendskab" til den enhed, som dataene stammer fra. F.eks. genkendes data fra en stregkodescanner automatisk som en stregkode, og den tilknyttede post i databasen findes lettere og hurtigere, end hvis en søgning med generisk streng blev brugt, som det er tilfældet med enheder til kreditkortlæsning.

> [!NOTE]
> Når der bruges kreditkortlæsere i POS, skal de programmeres til at sende en vognretur, eller en **Enter**-hændelse efter det sidste scannede tegn. Hvis denne konfiguration ikke er udført, fungerer kreditkortlæsere ikke korrekt. Læs dokumentationen fra enhedsproducenten for at få oplysninger om, hvordan du tilføjer hændelsen med vognretur.  

### <a name="device-printers"></a>Enhedsprintere

Printere af typen "Enhed" kan konfigureres til at bede brugeren om at vælge en printer, der er konfigureret til computeren. Når en printer af typen "Enhed" er konfigureret, bliver brugeren bedt om at vælge en printer på en liste, hvis Modern POS støder på en udskrivningskommando. Denne funktionsmåde adskiller sig fra funktionsmåden for Windows-drivere, da printertypen Windows i hardwareprofilen ikke viser en liste over printere for brugeren. I stedet kræver det, at der angives en navngiven printer i feltet **Enhedsnavn**.

### <a name="network"></a>Netværk

Netværksadresserbare pengeskuffer, bonprintere og betalingsterminaler kan bruges via et netværk, enten direkte via IPC-hardwarestationen (Interprocess Communications), der er indbygget i Modern POS til Windows-programmet eller via IIS-hardwarestationen til andre Modern POS-klienter.

## <a name="hardware-station-deployment-options"></a>Installationsindstillinger for hardwarestation

### <a name="dedicated"></a>Dedikeret

Modern POS-klienter til Windows og Android omfatter **dedikerede** eller indbyggede hardwarestationer. Disse klienter kan kommunikere direkte med eksterne enheder ved hjælp af forretningslogik, der er indbygget i programmerne. Android-programmet understøtter kun netværksenheder. Du kan finde yderligere oplysninger om understøttelse af eksterne enheder til Android i artiklen [Konfigurere POS Hybrid-appen på Android og iOS](./dev-itpro/hybridapp.md).

Hvis du vil bruge den dedikerede hardwarestation, skal du følge disse trin.

1. Tildel en hardwareprofil til et kasseapparat, som skal bruge Modern POS til Windows- eller Android-programmet.
1. Opret en hardwarestation af typen "Dedikeret" til den butik, hvor kasseapparatet skal bruges. 
1. Åbn Modern POS i ikke-kassetilstand, og brug handlingen **Administrer hardwarestationer** til at slå funktioner for hardwarestation til. Den dedikerede hardwarestation vil som standard være aktiv. 
1. Log af Modern POS. Log derefter på igen, og åbn et skift. De eksterne enheder, der er konfigureret i hardwareprofilen, kan nu bruges. 

### <a name="shared"></a>Delt

Det kaldes også "IIS"-hardwarestationen. "IIS" antyder, at POS-programmet opretter forbindelse til hardwarestationen via Microsoft Internet Information Services. POS-programmet opretter forbindelse til IIS-hardwarestationen via webtjenester, der kører på en computer, hvor enhederne er tilsluttet. Når du bruger den delte hardwarestation, kan de eksterne enheder, der er tilsluttet en hardwarestation, bruges af ethvert POS-kasseapparat, der er på samme netværk som IIS-hardwarestationen. Da kun Modern POS til Windows og Android indeholder indbygget understøttelse af eksterne enheder, skal alle andre Modern POS-programmer bruge IIS-hardwarestationen til at kommunikere med eksterne POS-enheder, der er konfigureret i hardwareprofilen. Hver forekomst af IIS hardware station kræver derfor, at en computer, der kører webtjenesten, og et program, der kommunikerer med enhederne. 

Den delte hardwarestation kan bruges til at tillade, at flere POS-klienter deler eksterne enheder, eller at de kan bruges til at administrere et sæt eksterne enheder for et enkelt POS. 

Når en hardwarestation bruges til at understøtte deling af eksterne enheder mellem flere POS-klienter, skal du kun bruge kontantskuffer, kvitteringsprintere og betalingsterminaler. Du kan ikke direkte forbinde enkeltstående stregkodescannere, MSR'er, linjeskærme, vægte eller andre enheder. Ellers kan der opstå konflikter, når flere POS-enheder gør krav på disse enheder på samme tid. Sådan håndteres konflikter for understøttede enheder:

-   **Pengeskuffe** – Pengeskuffen åbnes via en hændelse, der sendes til enheden. Problemer kan opstå, når en pengeskuffe kaldes, mens skuffen allerede er åben. En pengeskuffe, der bruges i en konfiguration af delt hardwarestation, skal indstilles til **Delt** i hardwareprofilen. Denne indstilling forhindrer, at POS-enheden kontrollerer, om kassen allerede er åben, når der sendes Åbn-kommandoer.
-   **Bonprinter** – Hvis to kommandoer til bonudskrivning sendes til hardwarestationen på samme tid, kan en af kommandoerne gå tabt, afhængigt af enheden. Nogle enheder har intern hukommelse eller gruppering, der kan forhindre dette problem. Hvis en udskrivningskommando ikke lykkes, modtager kassereren en fejlmeddelelse og kan derefter gentage udskrivningskommandoen fra POS-enheden.
-   **Betalingsterminal** – Hvis en kasserer forsøger at modtage betaling for en transaktion på en betalingsterminal, der allerede bruges, giver en meddelelse kassereren besked om, at terminalen bruges, og kassereren bliver bedt om at prøve igen senere. Normalt kan kasserere se, at en terminal allerede er i brug, og venter, indtil den anden transaktion er fuldført, inden de forsøger at modtage betaling igen.

Validering er planlagt til en fremtidig version for at registrere, om ikke-understøttede enheder er konfigureret for en hardwareprofil, der er knyttet til en delt hardwarestation. Hvis der registreres ikke-understøttede enheder, vil brugeren modtage en meddelelse om, at enhederne ikke understøttes til fælles hardwarestationer. Hvis der er fælles hardwarestationer, er indstillingen **Vælg ved betaling** angivet til **Ja** på kasseapparatniveauet. POS-bruger bliver derefter bedt om at vælge en hardwarestation, når et betalingsmiddel vælges til en transaktion på POS-enheden. Hvis hardwarestationen kun vælges på betalingstidspunktet, føjes valget af hardwarestation direkte til POS-arbejdsgangen for mobile scenarier. Som en ekstra fordel bruges linjevisningen på betalingsterminalen ikke til delte scenarier. Hvis betalingsterminalen bruges som en linjevisning, forhindres andre brugere muligvis i at bruge den pågældende terminal, før transaktionen er fuldført. I mobile scenarier kan linjer føjes til en transaktion i en længere periode. Derfor er indstillingen **Vælg ved betaling** påkrævet for at sikre enhedens optimale tilgængelighed.

### <a name="network-peripherals"></a>Eksterne netværksenheder

Netværksangivelsen for enheder i hardwareprofilen, giver pengeskuffer, bonprintere og betalingsterminaler mulighed for at være forbundet via en netværksforbindelse.

#### <a name="modern-pos-for-windows"></a>Modern POS til Windows

Du kan angive IP-adresser til eksterne netværksenheder to steder. Hvis Windows-klienten til Modern POS bruger et enkelt sæt af eksterne netværksenheder, skal du angive IP-adresserne for disse enheder ved hjælp af indstillingen **IP-konfiguration** i handlingsruden for selve kasseapparatet. Hvis netværksenheder skal deles mellem POS-kasseapparater, kan en hardwareprofil, der har netværksenheder tilknyttet, afbildes direkte til en delt hardwarestation. For at tildele IP-adresser, skal du vælge den pågældende hardwarestation på siden **Butikker** og derefter bruge indstillingen **IP-konfiguration** i afsnittet **Hardwarestationer** til at angive de netværksenheder, der er knyttet til denne hardwarestation. For hardwarestationer, der kun har netværksenheder, behøver du ikke at installere selve hardwarestationen. I det tilfælde kræves hardwarestationen kun for begrebsmæssigt at gruppere netværksadresserbare enheder ud fra deres placering i butikken.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS og Modern POS til iOS

Den logik, der styrer fysisk tilsluttede og netværksadresserbare eksterne enheder, findes i hardwarestationen. Til alle POS-klienter med undtagelse af Modern POS til Windows og Android skal IIS-hardwarestationen være installeret og aktiv for at aktivere POS-enheden til at kommunikere med eksterne enheder, uanset om disse enheder er fysisk forbundet til en hardwarestation eller adresseres via netværket.

## <a name="setup-and-configuration"></a>Installation og konfiguration
### <a name="hardware-station-installation"></a>Installation af hardwarestation

Du kan finde oplysninger om, hvordan du en IIS-hardwarestation, i [Konfigurere og installere hardwarestation](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Installation og konfiguration af Modern POS til Windows

Du kan finde flere oplysninger i [Konfigurer, installer og aktiver Modern POS (MPOS)](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Installation og konfiguration af Modern POS til Android og iOS

Du kan få flere oplysninger i [Konfigurere POS Hybrid-appen på Android og iOS](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>Installation og konfiguration af OPOS-enhed

Du kan finde flere oplysninger om OPOS-komponenter i afsnittet "Understøttede grænseflader" i dette dokument. Typisk leveres OPOS-drivere af producenten af enheden. Når der installeres en OPOS-enhedsdriver, føjer den en nøgle til Windows-registreringsdatabasen på en af følgende placeringer:

-   **32-bit system:** HKEY\_LOCAL\_MACHINE\SOFTWARE\OLEforRetail\ServiceOPOS
-   **64-bit system:** HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\OLEforRetail\ServiceOPOS

Konfigurerede enheder er organiseret efter enhedsklassen OPOS inden for lokaliteten for registreringsdatabasen ServiceOPOS. Flere enhedsdrivere gemmes.

## <a name="supported-scenarios-by-hardware-station-type"></a>Understøttede scenarier efter hardwarestationstype
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Understøttelse af klienter – IPC-hardwarestation vs. IIS-hardwarestation

Følgende tabel viser de topologier og installationsscenarier, der understøttes.

| Klient      | IPC-hardwarestation | IIS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nej                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nej                   | Ja                  |

### <a name="network-peripherals"></a>Eksterne netværksenheder

Netværksenheder understøttes direkte via den hardwarestation, der er indbygget i Modern POS til Windows- og Android-programmer. Til alle andre klienter skal du installere en IIS-hardwarestation.

| Klient      | IPC-hardwarestation | IIS-hardwarestation |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Cloud POS   | Nej                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nej                   | Ja                  |

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
<td>Kasseskuffe</td>
<td><ul>
<li>OPOS</li>
<li>Netværk </br><strong>Bemærk!</strong> Der kan kun konfigureres én skuffe, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kasseskuffe 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk </br><strong>Bemærk!</strong> Der kan kun konfigureres én skuffe, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
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

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-klienter, der har en bindende "Delt" IIS-hardwarestation

> [!NOTE]
> Når IIS-hardwarestationen er "bindende", er der en én til én-relation mellem POS-klienten og hardwarestationen.

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
<li>Netværk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
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
<td>Kasseskuffe</td>
<td><ul>
<li>OPOS</li>
<li>Netværk </br><strong>Bemærk!</strong> Der kan kun konfigureres én skuffe pr. hardwareprofil, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
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

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Alle Modern POS-klienter, der deler en IIS-hardwarestation

> [!NOTE]
> Når IIS-hardwarestationen er "delt", kan flere enheder bruge hardwarestationen på samme tid. I dette scenarie skal du kun bruge de enheder, der er angivet i følgende tabel. Hvis du forsøger at dele enheder, der ikke er angivet her, f.eks. stregkodescannere og MSR'er, opstår der fejl, når flere enheder forsøger at gøre krav på den samme eksterne enhed. I fremtiden forhindres en sådan konfiguration udtrykkeligt.

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
<li>Netværk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Netværk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kasseskuffe</td>
<td><ul>
<li>OPOS</li>
<li>Netværk </br><strong>Bemærk!</strong> Der kan kun konfigureres én skuffe pr. hardwareprofil, hvis <strong>Brug af delt skift</strong> er konfigureret på skuffen.</li>
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
Du kan finde flere oplysninger om, hvordan du opretter hardwareprofiler i [Tilslutte ydre enheder til POS](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS til Windows med en IPC-hardwarestation (indbygget)

Denne konfiguration er den mest typiske konfiguration for traditionelle, faste POS-kasseapparater. I dette scenarie er hardwareprofiloplysningerne knyttet direkte til selve kasseapparatet. EFT-terminalnummeret bør også angives i selve registeret. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor alle de nødvendige eksterne enheder er konfigureret.
2.  Tilknyt hardwareprofilen til POS-kasseapparatet.
3.  Opret en hardwarestation af typen **Dedikeret** til den butik, hvor POS-kasseapparatet skal bruges. En beskrivelse er valgfri. 

    > [!NOTE]
    > Du behøver ikke at angive andre egenskaber for hardwarestationen. Alle andre nødvendige oplysninger, f.eks. hardwareprofilen, kommer fra selve kasseapparatet.

4.  Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
5.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
6.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Installer og aktivér Modern POS til Windows.
8.  Start Modern POS til Windows, og begynd at bruge de tilsluttede eksterne enheder.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS til Android med en IPC-hardwarestation (indbygget)

**Nyhed for 10.0.8** - Epson-netværksprintere og pengeskuffer, der er tilsluttet de pågældende printere via DK-porten, understøttes nu af Modern POS til Android-app. Du kan finde yderligere oplysninger i artiklen [Konfigurere POS Hybrid-appen på Android og iOS](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-klienter, der har en bindende, delt IIS-hardwarestation

Denne konfiguration kan bruges til alle Modern POS-klienter, der har en hardwarestation, der bruges udelukkende af ét POS-kasseapparat. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor alle de nødvendige eksterne enheder er konfigureret.
2.  Opret en hardwarestation af typen **Dedikeret** til den butik, hvor POS-kasseapparatet skal bruges.
3.  På den dedikerede hardwarestation skal du angive følgende egenskaber:
    -   **Værtsnavn** – Navnet på den værtscomputer, hvor hardwarestationen skal køre. 
    
        > [!NOTE]
        > Cloud POS kan fortolke **localhost** for at bestemme den lokale computer, hvor Cloud POS kører. Men det certifikat, der kræves for at parre Cloud POS med hardwarestationen, skal dog også have "Localhost" som navnet på computeren. For at undgå problemer anbefaler vi, at du efter behov angiver en forekomst af hver dedikeret hardwarestation for butikken. For hver hardwarestation skal værtsnavnet være det specifikke computernavn, hvor hardwarestationen skal installeres.
    
    -   **Port** – Den port, der skal bruges af hardwarestationen til at kommunikere med Modern POS-klienten.
    -   **Hardwareprofil** – Hvis hardwareprofilen ikke er angivet på selve hardwarestationen, bruges den hardwareprofil, der er tildelt til kasseapparatet.
    -   **Elektronisk pengeoverførsel POS-nummer** – Det terminal-id til elektronisk pengeoverførsel, der skal bruges, når godkendelser af elektronisk pengeoverførsel sendes. Dette id leveres af kreditkortprocessoren.
    -   **Pakkenavn** – Den hardwarestationspakke, der skal bruges, når hardwarestationen installeres.

4.  Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
5.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
6.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Installer hardwarestationen. Du kan finde flere oplysninger om, hvordan du installerer hardwarestationen i [Konfigurer og installer hardwarestation til Retail](retail-hardware-station-configuration-installation.md).
8.  Installer og aktivér Modern POS. Du kan finde flere oplysninger om, hvordan du installerer Modern POS, under [Konfigurere, installere og aktivere Modern POS (MPOS)](retail-modern-pos-device-activation.md).
9.  Log på Modern POS, og vælg **Udfør handlinger uden om kasseskuffen.**.
10. Start handlingen **Administrer hardwarestationer**.
11. Vælg **Administrer**.
12. Angiv indstillingen for at slå hardwarestationen til på siden til administration af hardwarestation.
13. Vælg den hardwarestation, der skal bruges, og vælg derefter **Par**.
14. Når hardwarestationen er parret, skal du vælge **Luk**.
15. På siden til valg af hardwarestation skal du vælge den senest valgte hardwarestation for at gøre den aktiv.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter, der har en delt IIS-hardwarestation

Denne konfiguration kan bruges til alle Modern POS-klienter, der deler hardwarestationer med andre enheder. Benyt denne fremgangsmåde for at udføre konfigurationen.

1.  Opret en hardwareprofil, hvor de nødvendige eksterne enheder er konfigureret.
2.  Opret en hardwarestation af typen **Delt** til den butik, hvor POS-kasseapparatet skal bruges.
3.  På den delte hardwarestation skal du angive følgende egenskaber:
    -   **Værtsnavn** – Navnet på den værtscomputer, hvor hardwarestationen skal køre.
    -   **Beskrivelse** – Tekst, der hjælper med til at identificere hardwarestationen, f.eks. **Returneringer** eller **Foran i butikken**.
    -   **Port** – Den port, der skal bruges af hardwarestationen til at kommunikere med Modern POS-klienten.
    -   **Hardwareprofil** – For delte hardwarestationer skal hver hardwarestation have en hardwareprofil. Hardwareprofiler kan deles mellem hardwarestationer, men de skal være knyttet til hver hardwarestation. Vi anbefaler desuden, at du bruger delte skift, når flere enheder bruger den samme delte hardwarestation. Hvis du vil konfigurere et delt skift, skal du gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. For hver delt hardwareprofil skal du vælge pengeskuffen og angive indstillingen **Skuffe til delt skift** til **Ja**.
    -   **Elektronisk pengeoverførsel POS-nummer** – Det terminal-id til elektronisk pengeoverførsel, der skal bruges, når godkendelser af elektronisk pengeoverførsel sendes. Dette id leveres af kreditkortprocessoren.
    -   **Pakkenavn** – Den hardwarestationspakke, der skal bruges, når hardwarestationen installeres.

4.  Gentag trinene 2 og 3 for hver yderligere hardwarestation, der skal bruges i butikken.
5.  Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
6.  Vælg distributionsplanen **1090** for at synkronisere den nye hardwareprofil til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
7.  Vælg distributionsplanen **1040** for at synkronisere den nye hardwarestation til butikken. Vælg **Kør nu** for at synkronisere ændringer til POS-enheden.
8.  Installer hardwarestationen på hver værtscomputer, du har oprettet i trin 2 og 3. Du kan finde flere oplysninger om, hvordan du installerer hardwarestationen i [Konfigurer og installer hardwarestation til Retail](retail-hardware-station-configuration-installation.md).
9.  Installer og aktivér Modern POS. Du kan finde flere oplysninger om, hvordan du installerer Modern POS, under [Konfigurere, installere og aktivere Modern POS (MPOS)](retail-modern-pos-device-activation.md).
10. Log på Modern POS, og vælg **Udfør handlinger uden om kasseskuffen.**.
11. Start handlingen **Administrer hardwarestationer**.

12. Vælg **Administrer**.
13. Angiv indstillingen for at slå hardwarestationen til på siden til administration af hardwarestation.
14. Vælg den hardwarestation, der skal bruges, og vælg derefter **Par**.
15. Gentag trin 14 for hver hardwarestation, som Modern POS bruger.
16. Når alle de påkrævede hardwarestationer er parret, skal du vælge **Luk**.
17. På siden til valg af hardwarestation skal du vælge den senest valgte hardwarestation for at gøre den aktiv. 

> [!NOTE]
> Hvis enheder ofte bruger forskellige hardwarestationer, anbefaler vi, at du konfigurerer Modern POS til at bede kassereren om at vælge en hardwarestation, når de begynder betalingsprocessen. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Kasseapparater**. Vælg kasseapparatet, og angiv derefter indstillingen **Vælg ved betaling** til **Ja**. Brug distributionsplanen **1090** til at synkronisere ændringerne til kanaldatabasen.

## <a name="extensibility"></a>Udvidelsesmuligheder
Oplysninger om udvidelsesmuligheder for hardwarestationen finder du i [Integrere POS med en ny hardwareenhed og generere installationsprogrammet til udvidelse](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Sikkerhed
Ifølge de aktuelle sikkerhedsstandarder skal der bruges følgende indstillinger i et produktionsmiljø: 

### <a name="hardware-station-installer"></a>Installationsprogram til hardwarestation
Som en del af installationen via selvbetjening udfører hardwarestation-installationsprogrammet automatisk disse redigeringer i registreringsdatabasen.

-   SSL (Secure Sockets Layer) skal deaktiveres.
-   Kun TLS (Transport Layer Security) version 1.2 (eller den aktuelle højeste version) skal aktiveres og anvendes. 

### <a name="ssl-and-tls"></a>SSL og TLS
Som standard er SSL og alle versioner af TLS, undtagen TLS 1.2, deaktiveret. Hvis du vil redigere eller aktivere disse værdier, skal du følge disse trin:
    1.  Tryk på Windows-logotasten + R for at åbne et **Kør**-vindue.
    2.  I feltet **Åbn** skal du skrive **Regedit** og derefter vælge **OK**.
    3.  Hvis meddelelsesboksen **Kontrol af brugerkonti** vises, skal du vælge **Ja**.
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

> [!NOTE]
> Det er meget vigtigt, at du gennemgår sikkerhedsretningslinjer for IIS og PCI-kravene (Payment Card Industry).

## <a name="peripheral-simulator"></a>Ekstern simulator
Du kan finde oplysninger under [Ekstern simulator til Commerce](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsoft-testede eksterne enheder
### <a name="ipc-built-in-hardware-station"></a>IPC-hardwarestation (indbygget)

De følgende eksterne enheder blev testet ved hjælp af den IPC-hardwarestation, der er indbygget i Modern POS til Windows.

#### <a name="printer"></a>Printer

| Producent | Model    | Interface | Bemærkninger                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Drevet via USB             |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket   |
| Star         | mPOP     | OPOS      | Tilsluttet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Star TSP 100-printeren understøttes ikke for den indbyggede hardwarestation. Den indbyggede hardwarestation bruger en 64-bit proces, som ikke er kompatibel med de eksisterende Star TP 100-drivere. 

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Producent  | Model         | Interface | Bemærkninger |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Betalingsterminaler og pinkodetastaturer

Dynamics 365 Commerce indeholder en indbygget løsning til integration med Adyen til betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruger enhedsagnostik [Adyen Payment Terminal Application Programming Interface (API)](https://www.adyen.com/blog/introducing-the-terminal-api) og kan bruge alle betalingsterminaler, som denne API understøtter. Du kan få en komplet liste over understøttede betalingsterminaler i [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruge andre betalingsudbydere sammen med Dynamics 365 Commerce ved at oprette en brugerdefineret connector. Alle betalingsterminaler, der understøttes af betalingsudbyderen, kan bruges sammen med Dynamics 365 Commerce. Dynamics 365 Commerce tillader ligeledes alle modeller til integration af betalingsenhed, der understøttes af betalingsudbyderen, f.eks. lokal IP, sky-API eller direkte forbindelse (f.eks. via USB) til POS. Du kan få flere oplysninger i [Oprette komplet integration af betaling for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tilsluttet via Bluetooth |
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Brugerdefineret    | Tilsluttet Epson-netværksprinter via DK-port |

#### <a name="line-display"></a>Linjevisning

| Producent | Model    | Interface | Bemærkninger |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T-serie | OPOS      |          |

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

| Producent | Model    | Interface | Bemærkninger                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Drevet via USB             |
| Star         | TSP650II | Brugerdefineret    | Forbundet via netværket   |
| Star         | mPOP     | OPOS      | Tilsluttet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Stregkodescanner

| Producent  | Model         | Interface | Bemærkninger |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Betalingsterminaler og pinkodetastaturer

Dynamics 365 Commerce indeholder en indbygget løsning til integration med Adyen til betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruger enhedsagnostik [Adyen Payment Terminal-API](https://www.adyen.com/blog/introducing-the-terminal-api) og kan bruge alle betalingsterminaler, som denne API understøtter. Du kan få en komplet liste over understøttede betalingsterminaler i [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruge andre betalingsudbydere sammen med Dynamics 365 Commerce ved at oprette en brugerdefineret connector. Alle betalingsterminaler, der understøttes af betalingsudbyderen, kan bruges sammen med Dynamics 365 Commerce. Dynamics 365 Commerce tillader ligeledes alle modeller til integration af betalingsenhed, der understøttes af betalingsudbyderen, f.eks. lokal IP, sky-API eller direkte forbindelse (f.eks. via USB) til POS. Du kan få flere oplysninger i [Oprette komplet integration af betaling for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Brugerdefineret    | Tilsluttet Epson-netværksprinter via DK-port |

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

De følgende eksterne enheder blev testet ved hjælp af en delt IIS-hardwarestation samt Modern POS til Windows og Cloud POS. 

> [!NOTE]
> Kun en printer, en betalingsterminal og en pengeskuffe understøttes.

#### <a name="printer"></a>Printer

| Producent | Model    | Interface | Bemærkninger                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Drevet via USB             |
| Star         | mPOP     | OPOS      | Tilsluttet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Betalingsterminal

Dynamics 365 Commerce indeholder en indbygget løsning til integration med Adyen til betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruger enhedsagnostik [Adyen Payment Terminal-API](https://www.adyen.com/blog/introducing-the-terminal-api) og kan bruge alle betalingsterminaler, som denne API understøtter. Du kan få en komplet liste over understøttede betalingsterminaler i [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruge andre betalingsudbydere sammen med Dynamics 365 Commerce ved at oprette en brugerdefineret connector. Alle betalingsterminaler, der understøttes af betalingsudbyderen, kan bruges sammen med Dynamics 365 Commerce. Dynamics 365 Commerce tillader ligeledes alle modeller til integration af betalingsenhed, der understøttes af betalingsudbyderen, f.eks. lokal IP, sky-API eller direkte forbindelse (f.eks. via USB) til POS. Du kan få flere oplysninger i [Oprette komplet integration af betaling for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Pengeskuffe

| Producent | Model     | Interface | Bemærkninger              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Brugerdefineret    | Forbundet via netværket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Brugerdefineret    | Tilsluttet Epson-netværksprinter via DK-port |


## <a name="troubleshooting"></a>Fejlfinding
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kan registrere hardwarestationen på valglisten, men det kan ikke fuldføre parringen

**Løsning:** Kontrollér følgende liste over mulige fejlpunkter:

-   Den computer, der kører Modern POS har tillid til det certifikat, der bruges på den computer, der kører hardwarestationen.
    -   For at kontrollere denne opsætning i en webbrowser, skal du gå til følgende URL-adresse: https://&lt;Computernavn&gt;:&lt;Portnummer&gt;/HardwareStation/ping.
    -   Denne URL-adresse bruger et ping til at kontrollere, at du kan få adgang til computeren, og browseren angiver, om der er tillid til certifikatet. (F.eks. vises i Internet Explorer et låsesymbol på adresselinjen. Når du vælger dette symbol, kontrollerer Internet Explorer, om der i øjeblikket er tillid til certifikatet. Du kan installere certifikatet på den lokale computer ved at få vist detaljer om det certifikat, der er vist.)
-   På den computer, der kører hardwarestationen, er den port, der bruges af hardwarestationen åben i firewall'en.
-   Hardwarestationen har installeret forhandlerkontooplysninger korrekt ved hjælp af værktøjet Installér forhandleroplysninger, der køres i slutningen af installationsprogrammet til hardwarestationen.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS kan ikke registrere hardwarestationen på valglisten

**Løsning:** En af følgende faktorer kan forårsage dette problem:

-   Hardwarestationen er endnu ikke blevet konfigureret korrekt i hovedkontoret. Du kan finde flere oplysninger i [Konfigurer og installer hardwarestation til Retail](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Job til opdatering af kanalkonfigurationen har ikke været kørt. I dette tilfælde skal du køre job 1070 til kanalkonfiguration.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS afspejle ikke nye indstillinger for kontantskuffe

**Løsning:** Luk den aktuelle batch. Ændringer til kontantskuffen opdateres ikke i Modern POS, før den aktuelle batch er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS rapporterer et problem med en ekstern enhed

**Løsning:** Her er nogle typiske årsager til problemet:

-   Kontrollér, at andre konfigurationsværktøjer til enhedsdrivere er lukket. Hvis disse værktøjer er åbne, kan de forhindre Modern POS eller hardwarestationen i at gøre krav på enheden.
-   Hvis den eksterne enhed deles med flere POS-enheder, skal du kontrollere, at den tilhører en af følgende kategorier:
    -   Pengeskuffe
    -   Printer til modtagelse
    -   Betalingsterminal

    Hvis den eksterne enhed ikke tilhører en af disse kategorier, er hardwarestationen ikke beregnet til at aktivere den eksterne enhed til at blive delt mellem flere POS-enheder.
-   Nogle gange kan enhedsdrivere forårsage, at de fælles kontrolobjekter (CCO'er) holder op med at fungere korrekt. Hvis en enhed er blevet installeret for nylig, men den ikke fungerer korrekt, eller du bemærker andre problemer, kan du ofte løse problemet ved at geninstallere CCO'erne. Du kan hente CCO'er på <http://monroecs.com/oposccos_current.htm>.
-   Hvis du foretager hyppige ændringer af eksterne enheder under test eller fejlfinding, skal du muligvis nulstille IIS i stedet for at vente på, at cachen opdaterer sig selv. Følg disse trin for at nulstille IIS:
    1.  Fra menuen **Start** skal du skrive **CMD**.
    2.  I søgeresultaterne, skal du højreklikke på **Kommandoprompt** og derefter vælge **Kør som administrator**.
    3.  I vinduet **Kommandoprompt** skal du skrive **iisreset/Restart** og derefter trykke på Enter.
    4.  Når IIS er genstartet, skal du genstarte Modern POS.
-   Hvis du foretager hyppige ændringer af eksterne enheder, og hvis du også ofte starter og lukker POS-klienten, kan dllhost-processen fra en tidligere POS-session forstyrre den aktuelle session. I dette tilfælde kan en enhed ikke bruges, før du lukker DLL-værten (dynamic-link library), der styrer den forrige session. Følg disse trin for at lukke DLL-værten:
    1.  Fra menuen **Start** skal du skrive **Jobliste**.
    2.  I søgeresultaterne skal du vælge **Jobliste**.
    3.  I Jobliste under fanen **Detaljer** skal du vælge kolonneoverskriften, der hedder **Navn**, for at sortere tabellen alfabetisk efter navn.
    4.  Rul ned, indtil du finder dllhost.exe.
    5.  Vælg hver DLL-vært, og vælge derefter **Afslut job**.
    6.  Når DLL-værterne er blevet lukket, genstarter du Modern POS.


## <a name="additional-resources"></a>Yderligere ressourcer

[Ekstern simulator for Commerce](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
