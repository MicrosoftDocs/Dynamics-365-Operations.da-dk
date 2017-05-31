---
title: Definere og vedligeholde kanalklienter, kasseapparater og hardwarestationer
description: "Dette emne dækker, hvordan du forbinder enheder med din Retail POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 800e5c139b54541a179a336c8247eaa6017201d8
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definere og vedligeholde kanalklienter, kasseapparater og hardwarestationer

[!include[banner](includes/banner.md)]


Dette emne dækker, hvordan du forbinder enheder med din Retail POS.

**Bemærk:** Du kan finde særlige installationsinstruktioner i [Konfiguration og installation af Retail-hardwarestation](retail-hardware-station-configuration-installation.md) og [Selvbetjeningsdownload/-installation af Retail Modern POS og enhedsaktivering af Modern POS og Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Nøglekomponenter
Der bruges flere komponenter til at definere relationer mellem en butik, POS-kasseapparater eller kanaler i butikken og detailenheder, som de pågældende kasseapparater eller kanaler bruger til at behandle transaktioner. I dette afsnit beskrives hver komponent, og hvordan den skal bruges i en installation i en detailbutik.

### <a name="pos-registers"></a>Kasseapparater

Navigation: Klik på **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**. POS-kasseapparat er en enhed, der bruges til at definere egenskaberne for en bestemt forekomst af POS. Disse egenskaber omfatter hardwareprofilen eller opsætningen af detailenheder, der skal bruges ved kasseapparatet, den butik, som kasseapparatet er tilknyttet, og den visuelle oplevelse for den bruger, der logger på kassen.

### <a name="devices"></a>Enheder

Navigation: Klik på **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Enheder**. En enhed repræsenterer en fysisk forekomst af en enhed, der er knyttet til et POS-kasseapparat. Når der oprettes en enhed, knyttes den til et POS-kasseapparat. Enheden registrerer oplysninger om, hvornår et POS-kasseapparat aktiveres, den klienttype, som benyttes, og den programpakke, der er blevet installeret på en bestemt enhed. Enheder kan være af to typer: **Retail Modern POS** (MPOS) eller **Retail Cloud POS** (sky-POS).

#### <a name="mpos"></a>MPOS

MPOS er et POS-klientprogram, der installeres på Windows 8.1 eller et nyere pc-baseret operativsystem. Hvis programtypen **Retail Modern POS** er knyttet til en enhed, kan overførselspakken angives for en bestemt enhed. Overførselspakken kan tilpasses til at medtage forskellige versioner af installationspakken. Muligheden for at installere forskellige pakker giver fleksibilitet i tilfælde, hvor forskellige POS-kasseapparater kan kræve forskellige integrationer. MPOS installeres sammen med en indbygget hardwarestation.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS er en browserbaseret POS. Da det kan køre i browseren, kræver ikke Cloud POS ikke Windows 8.1 eller et nyere pc-baseret operativsystem. Hvis **Retail Cloud POS**-programtypen er knyttet til en bestemt enhed i administrationen (back-office), kan denne enhed bruges via webbrowseren, og der er ikke behov for at hente eller installere en pakke. Cloud POS kræver en hardware-station, der bruger hardware ud over kreditkortlæser-baseret stregkodescanning til tastaturet.

### <a name="hardware-profile"></a>Hardwareprofil

Navigation: Klik på **Handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardware-profiler**. En hardwareprofil identificerer den hardware, der er forbundet med et POS-kasseapparat eller en hardwarestation. Hardwareprofilen bruges også til at angive de parametre for betalingsprocessoren, der skal bruges under kommunikation med betalings-SDK'et (Software Development Kit). (Betaling-SDK'et installeres som en del af hardwarestationen).

### <a name="hardware-station"></a>Hardwarestation

Navigation: Klik på **Detail og handel** &gt; **Kanaler** &gt; **Detailbutikker** &gt; **Alle detailbutikker**. Vælg en butik, og klik derefter i oversigtspanelet **Hardwarestationer**. En hardwarestation er en forekomst af forretningslogik, der driver POS-enheder. En hardwarestation installeres automatisk sammen med MPOS. Hardwarestationen kan også installeres som en enkeltstående komponent og derefter åbnes af MPOS eller Cloud POS via en webtjeneste. Hardwarestationen skal defineres på kanalniveau.

### <a name="hardware-station-profile"></a>Hardwarestations profil

Navigation: Klik på **Handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwarestationens profiler**. Selvom selve hardwarestationen angives på kanalniveau, og angivelsen indeholder forekomstspecifikke oplysninger som f.eks. URL-adressen for hardwarestationen, indeholder hardwarestationsprofilen oplysninger, der kan være statiske eller delte på tværs af flere hardwarestationer. De statiske oplysninger omfatter den port, der skal bruges, hardwarestationspakken og hardwareprofilen. De statiske oplysninger omfatter også en beskrivelse af typen af hardwarestation, der skal installeres, som f.eks. **Til kassen**eller **Returneringer**, afhængigt af hvilken hardware der kræves for hver specifik hardwarestation.

## <a name="scenarios"></a>Scenarier
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS med forbundne eksterne enheder

[![Traditionelt, fast POS](./media/traditional-300x279.png)](./media/traditional.png) 

For at forbinde MPOS til POS-enheder i et traditionelt, fast POS-scenario skal du først navigere til selve kasseapparatet og tildele en hardwareprofil til det. Du kan finde POS-kasseapparater i **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**. Når du har tildelt hardwareprofilen, skal du synkronisere ændringer til kanaldatabasen ved hjælp af distributionsplanen "Kasseapparater". Du kan finde distributionsplanerne på **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan**. Opret derefter en "lokal" hardwarestation på kanalen. Klik på **Detail og handel** &gt; **Kanaler** &gt; **Detailbutikker** &gt; **Alle detailbutikker**, og vælg en butik. Derefter skal du i oversigtspanelet **Hardwarestationer** klikke på **Tilføj** for at tilføje en hardwarestation. Indtast en beskrivelse, angiv **localhost** som værtsnavn, og synkroniser derefter ændringerne til kanalen ved hjælp af distributionsplanen "Kanalkonfiguration". Du kan finde distributionsplanerne på **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan**. Brug til sidst i MPOS handlingen **Vælg hardwarestation** for at vælge hardwarestationen **localhost**. Indstil hardwarestationen til **Aktiv**. Den hardwareprofil, der bruges i dette scenario, skal komme fra selve POS-kasseapparatet. En hardwarestationprofil er ikke påkrævet i dette scenario. **Bemærk:** Nogle hardwareprofilændringer som f.eks. ændringer af pengeskuffer kræver, at et nyt skift åbnes, når ændringerne er blevet synkroniseret til kanalen. **Bemærk:** Cloud POS skal bruge den enkeltstående hardwarestation til at kommunikere med eksterne detailenheder.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS eller Cloud POS med en enkeltstående hardwarestation
[![Delte eksterne enheder](./media/shared-300x254.png)](./media/shared.png)

I dette scenario deles en enkeltstående hardwarestation af MPOS- og Cloud POS-klienter. Dette scenario kræver, at du opretter en hardwarestationprofil for at angive den overførselspakke, port og hardwareprofil, der bruger hardwarestationen. Du kan finde hardwarestationsprofilen på **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwarestations profiler**. Når du har oprettet hardwarestationsprofilen, skal du navigere til den specifikke detailkanal (**Detail og handel** &gt; **Kanaler** &gt; **Detailbutikker** &gt; **Alle detailbutikker**) og tilføje en ny hardwarestation. Knyt den nye hardwarestation til hardwarestationsprofilen, der tidligere blev oprettet. Derefter skal du angive en beskrivelse, så kassereren kan identificere hardwarestationen. I feltet **Værtsnavn** skal du angive URL-adressen på værtscomputeren i følgende format: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Erstat **&lt;MachineName:Port&gt;** med det faktiske computernavn på hardwarestationen og porten, der er angivet i hardwarestationsprofilen). For en enkeltstående hardwarestation skal du også angive terminal-id'et for den elektroniske pengeoverførsel (EFT). Denne værdi identificerer den elektronisk pengeoverførselsterminal, der er forbundet med hardwarestationen, når betalingsconnectoren kommunikerer med betalingsudbyderen. Naviger derefter fra den faktiske hardwarestationscomputer til kanalen, og vælg hardwarestationen. Klik derefter på **Hent**, og installer hardwarestationen. Brug derefter fra MPOS eller Cloud POS handlingen **Vælg hardwarestation** for at vælge den hardwarestation, der tidligere blev installeret. Vælg **Par** for at oprette en sikker forbindelse mellem POS'et og hardware-stationen. Dette trin skal udføres én gang for hver kombination af en POS og en hardwarestation. Når hardwarestationen er parret, skal du bruge den samme handling til at aktivere hardwarestationen, mens den bruges. I dette scenarie skal hardwareprofilen tildeles hardwarestationsprofilen i stedet for til selve kasseapparatet. Hvis en hardwarestation af en eller anden grund ikke har en direkte tilknyttet hardwareprofil, bruges den hardwareprofil, der er tildelt til kasseapparatet

## <a name="client-maintenance"></a>Vedligeholdelse af klient
### <a name="registers"></a>Kasseapparater

POS-kasseapparater styres primært via selve kasseapparaterne, men også via de profiler, der er tildelt til kasseapparaterne. Attributter, der er specifikke for et enkelt kasseapparat, administreres på kasseapparatniveau. Disse attributter omfatter den butik, hvor kasseapparatet bruges, kasseapparatnummer, beskrivelsen og terminal-id'et for den elektroniske pengeoverførsel, som er specifikt for det pågældende kasseapparat.

### <a name="pos-profiles"></a>POS-profiler

Du kan finde POS-profiler i **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler**. Det er nyttigt at administrere mange aspekter af et kasseapparat via profiler, fordi profilerne kan deles af mange kasseapparater. Profiler kan knyttes til enten et enkelt kasseapparat eller, hvis en profil er gældende for hele butikken, til detailbutikken. I følgende afsnit beskrives POS-profilerne, og hvordan de bruges.

#### <a name="offline-profile"></a>Offlineprofil

Offlineprofilen angives på butiksniveau. Den bruges til at angive overførselsindstillingerne for transaktioner, der udføres på et POS-kasseapparat, mens dette kasseapparat ikke er forbundet med kanaldatabasen.

#### <a name="functionality-profile"></a>Funktionalitetsprofil

Funktionalitetsprofilen angives på butiksniveau. Den bruges til at angive indstillinger for hele butikken om de funktioner, der kan udføres på POS'et. Følgende funktioner administreres gennem funktionalitetsprofilen. Disse funktioner arrangeres i oversigtspanelet.

-   Oversigtspanelet **Generelt**:
    -   International Organization for Standardization (ISO).
    -   Opret en kunde i offlinetilstand.
    -   Kvitteringsprofil med mail.
    -   Central godkendelse af medarbejderlogon.
-   Oversigtspanelet **Funktioner**:
    -   Administration af logon og udvidet logon.
    -   Finansielle og valutarelaterede aspekter af POS, som f.eks. muligheden for at indtaste priser, og om der kræves decimaler til mindre valutaenhed.
    -   Mulighed for tidsregistrering via POS'et.
    -   Hvordan produkter og betalinger vises på POS og på kvitteringer.
    -   Styring af kasseopgørelse.
    -   Parametre for opbevaring af kanaldatabasetransaktion.
    -   Hvordan der søges efter kunder, og hvordan de oprettet fra POS.
    -   Hvordan rabatter beregnes.
-   Oversigtspanelet **Beløb**:
    -   Største og mindste tilladte priser.
    -   Anvendelse og beregning af rabat.
-   Oversigtspanelet **Infokoder**:
    -   Alle aspekter af, hvordan infokoder administreres på POS'et. Du kan finde flere oplysninger i [Infokoder](info-codes-retail.md).
-   Oversigtspanelet **Kvitteringsnummerering**:
    -   Angiv kvitteringsnummereringsmasker, som kan omfatte segmenter for butiksnummer, terminalnummer, konstanter og om salg, returvarer, salgsordrer og tilbud udskrives i separate serier, eller om de alle følger den samme serie.

#### <a name="receipt-profiles"></a>Kvitteringsprofiler

Kvitteringsprofiler tildeles til printere i hardwareprofilen. De bruges til at angive de kvitteringstyper, der udskrives på en bestemt printer. Profilerne omfatter indstillinger for kvitteringsformater og indstillinger, der bestemmer, om kvitteringen altid skal udskrives, eller om kassereren bliver bedt om at beslutte, om den skal udskrives. Forskellige printere kan også bruge forskellige kvitteringsprofiler. For eksempel er printer 1 en standard termisk bonprinter, og den har derfor mindre kvitteringsformater. Men printer 2 er en kvitteringsprinter i fuld størrelse, der bruges til kun at udskrive kvitteringer for kundeordrer, hvilket kræver mere plads.

#### <a name="hardware-profiles"></a>Hardwareprofiler

Hardwareprofiler beskrives som en komponent til klientinstallation tidligere i denne artikel. Hardwareprofiler tildeles direkte til POS-kasseapparatet eller en hardwarestationprofil. De bruges til at angive de typer af enheder, som et bestemt POS-kasseapparat eller hardwarestation bruger. Hardwareprofiler bruges også til at angive indstillinger for elektronisk pengeoverførsel, der bruges til at kommunikere med betalings-SDK'et.

#### <a name="visual-profiles"></a>Visuelle profiler

Visuelle profiler tildeles på kasseapparatniveau. De bruges til at angive temaet for et bestemt kasseapparat. Profilerne omfatter indstillinger for den type program, der bruges (MPOS eller Cloud POS), markeringsfarve og tema, skrifttypeskemaet, logonbaggrund og POS-baggrund.

### <a name="custom-fields"></a>Brugerdefinerede felter

Du kan oprette brugerdefinerede felter for at tilføje felter, der ikke tilbydes som standard til POS'et. Du kan finde flere oplysninger om, hvordan du bruger brugerdefinerede felter, i [Blogindlæg om at arbejde med brugerdefinerede felter](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Sprogtekst

Du kan tilsidesætte standardstrenge på POS'et ved hjælp af sprogtekstindtastninger. For at tilsidesætte en streng i POS'et kan du tilføje en ny sprogtekstlinje. Angiv derefter et id, standardstrengen, der skal ændres, og den tekst, der skal vises på POS'et i stedet for standardstrengen.

### <a name="hardware-station-profiles"></a>Hardwarestations profiler

Hardwarestationprofiler er beskrevet tidligere i denne artikel. De bruges til at tildele ikke-forekomstspecifikke oplysninger til hardwarestationer.

### <a name="channel-reports-configuration"></a>Konfiguration af kanalrapporter

Du kan oprette de rapporter, der er tilgængelige på detailkanalen på siden **Konfiguration af detailkanalrapporter**. Du kan oprette nye rapporter ved at levere XML-definitionen af rapporten og tildele rapporten til en bestemt rettighedsgruppe på POS'et.

### <a name="devices"></a>Enheder

Enheder er beskrevet tidligere i denne artikel. De bruges til at administrere aktivering af et bestemt POS-kasseapparat. Enheder bruges også til at angive det program, der bruges til et bestemt kasseapparat og den installationspakke, der skal bruges til at installere MPOS-klienten. Her er enhedens aktiveringstilstande:

-   **Afventer** – Enheden er klar til at blive aktiveret.
-   **Aktiveret** – Enheden er aktiveret.
-   **Deaktiveret** – Enheden er blevet deaktiveret, enten af administrationen eller via POS.
-   **Deaktiveret** – Enheden er blevet deaktiveret.

Yderligere oplysninger i forbindelse med aktivering omfatter den medarbejder, der ændrede aktiveringsstatussen for enheden, et tidsstempel for aktiveringen og om konfigurationen af enheden er blevet valideret.

### <a name="client-data-synchronization"></a>Synkronisering af klientdata

Alle ændringer af POS-klienten med undtagelse af ændringer af enhedens aktiveringsstatus skal synkroniseres, for at kanaldatabasen kan træde i kraft. For at synkronisere ændringer med kanaldatabasen skal du gå til **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan** og køre den krævede distributionsplan. For klientændringer skal du køre distributionplanerne "Kasseapparater" og "Kanalkonfiguration".




