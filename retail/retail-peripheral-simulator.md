---
title: Simulator for eksterne detailenheder
description: "Dette emne beskriver simulatorværktøjet for eksterne enheder, der følger med Microsoft Dynamics 365 for Operations – Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 894aaaaa844447030dae73826d326f99366aa068
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="retail-peripheral-simulator"></a>Simulator for eksterne detailenheder

[!include[banner](includes/banner.md)]


Dette emne beskriver simulatorværktøjet for eksterne enheder, der følger med Microsoft Dynamics 365 for Operations – Retail.

<a name="overview"></a>Overblik
--------

Simulatoren for eksterne enheder til Microsoft Dynamics 365 for Operations – Retail er et værktøj, som hjælper dig med at oprette, teste og fejlfinde eksterne enheder, der bruges i detailmiljøer. Du kan bruge simulatoren for eksterne enheder til at strømline testen af eksterne detailenheder og til at isolere problemer, der skyldes forkert opsætning eller funktionsfejl i enhedsdrivere. Simulatoren for eksterne enheder indeholder et skrivebordsprogram med virtuelle versioner af enheder, som Dynamics 365 for Operations – Retail understøtter. Et afsnit for hver virtuel enhed viser interaktionen mellem enheden og POS-enheden. Du kan også bruge den til at give input, der gælder for forskellige POS-scenarier. Simulatoren for eksterne enheder understøtter interaktion mellem POS-enheden og følgende virtuelle enheder:

-   **Printer** – Simulatoren for eksterne enheder kan vise kvitteringer, der er konfigureret til en POS-printer.
-   **Linjevisning** – Du kan konfigurere en virtuel linjevisning til at vise aktivitet på en fysisk linjevisning.
-   **Magnetstribelæser (MSR)** – Du kan sende simulerede magnetstribehændelser til POS-enheden fra simulatoren for eksterne enheder.
-   **Kasseskuffe** – Du kan simulere en fysisk pengeskuffe.
-   **Kasseskuffe 2** – Ved at oprette en anden pengeskuffe i simulatoren for eksterne enheder, kan du simulere situationer, der omfatter et enkelt POS-kasseapparat med to aktive skift.
-   **Scanner** – Den virtuelle stregkodescanner, som simulatoren for eksterne enheder understøtter, kan udsende stregkodescanningshændelser.
-   **Vægt** – En virtuel skala giver dig mulighed for simulere samspillet mellem vejede varer og POS-enheden.
-   **Tastatur til PIN-kode** – Du kan simulere operationer på PIN-tastatur. **Bemærk:** Du skal implementere understøttelse af et fysisk PIN-tastatur via betalingsconnectoren.
-   **Signaturhentning** – Simulatoren for eksterne enheder indeholder en virtuel enhed til hentning af signatur, som du kan konfigurere til at bede om signaturer, der er nødvendige for nogle betalingsmidler, f.eks. kundekontobetalinger.

Du kan også bruge simulatoren for eksterne enheder til at simulere hændelser fra kreditkortlæsere, der stammer fra en stregkodescanner og MSR. Den virtuelle simulator for eksterne enheder understøtter objektsammenkædning og indlejring til Retail POS (OPOS)-enheder.

## <a name="key-scenarios"></a>Nøglescenarier
### <a name="troubleshooting"></a>Fejlfinding

Du kan bruge simulatoren for eksterne enheder til fejlfinding i forbindelse med enhedsinstallation. Hvis du ikke har simulatoren for eksterne enheder eller en anden enhed af samme klasse, kan det være svært at finde ud af, hvor problemer opstår. Men når du har simulatoren for eksterne enheder, kan du oprette virtuelle enheder og køre de samme kodestier og forretningslogik, der bruges til fysiske enheder. Set fra simulatoren for eksterne enheder er den vigtigste forskel mellem virtuelle enheder og fysiske enheder, serviceobjektet eller enhedsdriveren. For fysiske enheder leveres serviceobjektet af enhedsproducenten. For simulatoren for eksterne enheder leveres serviceobjekterne som en del af simulatoren for eksterne enheder. Når simulatoren for eksterne enheder fungerer korrekt, kan du, hvis en enhed ikke fungerer korrekt, efter at enhedsnavnet i hardwareprofilen er ændret til navnet på en faktisk enhed, antage, at der er et problem med det serviceobjekt, der er leveret af producenten.

### <a name="training"></a>Kursus

Du kan bruge simulatoren for eksterne enheder til at tilføje et realistisk lag til uddannelse af kasserere, når en fysisk hardwareopsætning er ikke tilgængelig. Når simulatoren for eksterne enheder indgår i uddannelsesscenarier, kan kassereren mere effektivt interagere med POS-enheden ved at levere input, f.eks. scanninger af produktkoder og læsninger af gavekort, og observere, hvilke kvitteringer der udskrives for en bestemt transaktion.

### <a name="testing"></a>Test

Du kan bruge simulatoren for eksterne enheder til at teste produktstregkoder, kvitteringsformater osv., uden at du skal implementere fysisk hardware i et virtuelt miljø. Da fysisk hardware ikke er påkrævet, og du ikke behøver at installere en POS-klient på en fysisk computer eller en hardwarestation, kan du hurtigt teste ændringer, der foretages i back-office.

## <a name="set-up-the-peripheral-simulator"></a>Opsætning af simulatoren for eksterne enheder
### <a name="set-up-a-hardware-profile"></a>Opsætning af en hardwareprofil

1.  For at opsætte simulatoren for eksterne enheder skal du gå til **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**.
2.  Klik på **Ny** for at oprette en ny profil.
3.  Angiv værdier i felterne **Profilnummer** og **Beskrivelse**.
4.  Brug følgende tabel til at konfigurere de virtuelle enheder, der skal testes. Her er en forklaring på kolonnerne i tabellen:
    -   **Enhed** – I denne kolonne vises navnet på det oversigtspanel, du udvider for at konfigurere enheden.
    -   **Enhedstype** – Denne kolonne indeholder den værdi, du vælger i feltet, der er mærket med navnet på enheden.
    -   **Enhedsnavn** – I denne kolonne vises den nøjagtige værdi, du angiver for enhedsnavnet. **Vigtigt:** De enhedsnavne, der er angivet her, er nødvendige, fordi hardwarestationen bruger disse specifikke navne til at adressere enhederne. Hvis du ikke bruger disse specifikke navne, kan ikke enheden bruges.

    | Enhed            | Enhedstype | Enhedens navn              |
    |-------------------|-------------|--------------------------|
    | Printer           | OPOS        | MockOPOSPrinter          |
    | Linjevisning      | OPOS        | MockOPOSLineDisplay      |
    | Magnetstribelæser               | OPOS        | MockOPOSMSR              |
    | Kasseskuffe            | OPOS        | MockOPOSDrawer1          |
    | Kasseskuffe2           | OPOS        | MockOPOSDrawers          |
    | Scanner           | OPOS        | MockOPOSScanner          |
    | Vægt             | OPOS        | MockOPOSScale            |
    | pinkodetastatur           | OPOS        | MockOPOSPinPad           |
    | Signaturhentning | OPOS        | MockOPOSSignatureCapture |

**Bemærk:** Der kræves ingen speciel opsætning i hardwareprofilen for at simulere hændelser fra kreditkortlæsere fra stregkodescanneren og MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Tildel hardwareprofilen til et kasseapparat

1.  Når du har oprettet hardwareprofilen, skal du gå til **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**.
2.  På listen **POS-kasseapparater** skal du klikke på linket i feltet **Kassenummer** for det kasseapparat, der skal bruge til det register, der skal bruge simulatoren for eksterne enheder.
3.  Klik på **Rediger**.
4.  I afsnittet **Profiler** i feltet **Hardwareprofil** skal du vælge den hardwareprofil, du oprettede til virtuelle enheder.
5.  Klik på **Gem**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkroniser ændringerne til kanaldatabasen

1.  Gå til **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan**.
2.  Vælg distributionsplanen **1090**.
3.  Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.

Når dataene er synkroniseret, er den nye hardwareprofil og ændringerne på kasseapparatet tilgængelige i kanaldatabasen.

## <a name="install-the-peripheral-simulator"></a>Installer simulatoren for eksterne enheder
1.  Gå til **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**.
2.  Klik på **Hent**, og klik derefter på **PeripheralSimulator**. **Bemærk:** Du skal deaktivere blokeringer af pop op-vinduer, før du kan hente simulatoren for eksterne enheder.
3.  Når hentningen er fuldført, skal du åbne mappen **Overførsler** og dobbeltklike på **VirtualPeripherals.msi** for at starte installationsprogrammet.
4.  Installer simulatoren for eksterne enheder ved hjælp af standardindstillingerne.

Ud over simulatoren for eksterne enheder skal du installere de fælles kontrolobjekter fra Monroe Consulting Services. Ellers er fungerer simulatoren for eksterne enheder ikke korrekt. For at hente de fælles kontrolobjekter, skal du gå til <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Brug af simulatoren for eksterne enheder
Klik på **Start** på din computer for at starte simulatoren for eksterne enheder, skriv **simulator for eksterne enheder til Retail**, og vælg derefter appen, når det vises i søgeresultaterne. Når du har startet simulatoren for eksterne enheder, skal du klikke et enhedsnavn for at se de understøttede enheder. Disse enheder vil blive vist som faner i venstre side af vinduet. For at få vist en bestemt enhed, skal du klikke på fanen for den pågældende enhed.

### <a name="line-display-capabilities"></a>Funktioner til linjevisning

Linjevisningen er den første enhed, der er angivet i simulatoren for eksterne enheder. Når den virtuelle linjevisning er konfigureret, vises linjeelementer, som de scannes i POS-transaktionen. Foruden linjeelementer viser skærmen den forfaldne total, når der vælges et betalingsmiddel på POS-enheden. Den viser også den forfaldne saldo, hvis et betalingsmiddel er angivet, men der er stadig er en forfalden saldo for transaktionen. Når POS-enheden ikke bruges, kan der vises en meddelelse for at angive, at pengeskuffen er lukket. Du skal konfigurere meddelelsen på oversigtspanelet **Linjevisning** i hardwareprofilen.

### <a name="cash-drawer-capabilities"></a>Pengeskuffefunktioner

Pengeskuffen er den anden enhed, der er angivet i simulatoren for eksterne enheder. Når hardwareprofilen er konfigureret til at bruge virtuelle pengeskuffer, åbner POS-enheden pengeskuffen for det aktive skift som svar på kasseskuffehandlinger, f.eks. kasseoptællinger, og så kassereren kan ændre eller deponere kontanter ved standard cash-and-carry-transaktioner. De virtuelle pengeskuffer har etiketterne **Hovedskuffe** og **Sekundær skuffe**. Disse etiketter repræsenterer henholdsvis Skuffe og Skuffe 2 i hardwareprofilen. Når en skuffe lukkes, vises et billede af en lukket pengeskuffe, og knappen på den lukkede pengeskuffe hedder **Åbn kasseskuffe**. Hvis du klikker på denne knap, erstattes billedet med et billede af en åben pengeskuffe for at angive, at kasseskuffen nu er åben. Knappen på den åbne pengeskuffen hedder **Luk kasseskuffen**. Flere handlinger ved POS-enheden kan forårsage, at pengeskuffen åbnes. De fleste handlinger kan ikke fortsætte, når pengeskuffen er åben. Undtagelserne er nogle procedurer ved slutningen af dagen. Hvis POS-brugeren modtager en fejlmeddelelse, der angiver, at en handling ikke kan udføres, mens pengeskuffen er åben, skal brugeren lukke denne virtuelle eller fysiske pengeskuffe for at fortsætte. Hvis en pengeskuffe er markeret som **Delt** i hardwareprofilen, kontrollerer systemet ikke, at kasseskuffen er lukket før en handling. Handlingen fortsætter som normalt, selvom pengeskuffen er åben. Denne funktion understøtter scenarier, hvor pengeskuffer deles mellem salgsmedarbejdere, og hvor én medarbejder bruger en pengeskuffen, mens en anden medarbejder udfører ikke-relaterede opgaver på sin egen POS-enhed. Ændringer, der er foretaget i pengeskuffen kan først opgøres, når det aktuelle skift lukkes, og et nyt skift åbnes.

### <a name="msr-capabilities"></a>MSR-egenskaber

Simulatoren for eksterne enheder giver robust understøttelse af virtuelle MSR-handlinger ved at arbejde i enten OPOS-tilstand eller tilstand for kreditkortlæser. OPOS-tilstand kræver, at MSR konfigureres i hardwareprofilen til at fungere som en OPOS-enhed. Tilstanden for kreditkortlæser sender blot datahændelser fra kreditkortlæseren Microsoft Windows. Ud over forskelle i opsætningen adskiller OPOS-tilstand og tilstanden for kreditkortlæser sig på følgende måder:

-   POS-klienten kan aktivere OPOS MSR-enheder til bestemte scenarier, f.eks. scenarier, der tillader magnetstribedata til indtastning af kundefordels- eller gavekort.
-   I tilstanden for kreditkortlæser sender simulatoren for eksterne enheder data fra kreditkortlæseren til det felt, der er aktivt, når data sendes. Denne funktionsmåde ligner det, der sker, hvis data indtastes ved hjælp af et tastatur. For at bruge MSR som en kreditkortlæser, skal brugeren skifte til Retail Modern POS (MPOS) for at sikre, at dataene modtages i det korrekte felt. Derfor kan du konfigurere en forsinkelse, så brugeren har tid til at sikre, at data sendes til det rette felt.

#### <a name="testing-gift-and-payment-card-swipes"></a>Test af læsning af gave- og betalingskort

Den virtuelle MSR, som simulatoren for eksterne enheder indeholder, giver dig også mulighed for at konfigurere specifikke MSR-data til testscenarier for læsning af gave- og betalingskort. Du kan oprette et kort ved at klikke på knappen med plustegnet (**+**) og vælge korttypen. Angiv derefter kortnummeret, eller spor data, der skal sendes til POS-enheden sammen med udløbsmåned og -år for det kort, du definerer. Den værdi, du vælger i feltet **Kortype**, er blot en etiket, der kan knyttes til et kort. Denne etiket gør det nemmere at identificere kort, når de er ført gennem simulatoren for eksterne enheder. Du kan vælge kort, der er konfigureret i simulatoren for eksterne enheder, ved hjælp af knapperne til venstre pil (**&lt;**) og højre pil (**&gt;**) over billedet af kortet. Du kan redigere og slette kort ved hjælp af knapperne **Rediger** og **Slet** ved siden af plus-tegnet (**+**).

### <a name="pin-pad"></a>Pinkodetastatur

Du kan konfigurere PIN-tastatursimulatoren til at simulere et OPOS PIN-tastatur. Når en transaktion med elektronisk overførsel (EFT) udføres på POS-enheden og kræver indtastning af pinkode, kalder hardwarestationen PIN-enheden for at bede om indtastning af pinkode. For at fungere kræver PIN-tastaturet i simulatoren for eksterne enheder understøttelse af EFT-betalingsconnector.

### <a name="printer"></a>Printer

Den virtuelle eksterne printer viser blot kvitteringer, som de udskrives fra POS-enheden. Hvis en udskrivningshandling resulterer i flere kvitteringer, kan du rulle gennem kvitteringerne.

#### <a name="configure-receipt-printing"></a>Konfigurer kvitteringsudskrivning

1.  Gå til **Detail og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofiler**.
2.  Vælg den hardwareprofil, du oprettede til virtuelle enheder.
3.  Klik på **Rediger** i oversigtspanelet **Printer**.
4.  Vælg en kvitteringsprofil i feltet **Kvitteringens profil-id**.
5.  Klik på **Gem**.

### <a name="scale"></a>Vægt

Når et produkt, der skal vejes, føjes til POS-transaktionen, og en vægt er konfigureret, henter POS-enheden vægten fra denne vægt. For både den virtuelle og fysiske vægt, skal produktet eller vægten angives, før produktet føjes til transaktionen. Før du føjer produktet, der skal vejes, til transaktionen, skal du gå til vægten i simulatoren for eksterne enheder og bruge knapperne med plustegnet (**+**) og minustegnet (**–**) til at justere den vægt, som vægten skal rapportere. Du kan også angive den ønskede vægt direkte i feltet **Aktuel værdi**. Du kan justere vægtenhederne for vægten ved hjælp af knapperne plustegn (**+**), **Rediger** og **Slet**. På denne måde kan enheder angives på basis af de produkter, der er vejet, eller den landestandard, hvor vægten anvendes.

#### <a name="configure-a-scale-product"></a>Konfigurer et produkt, der skal vejes

1.  Gå til **Detail og** **handel** &gt; **Produkter og kategorier** &gt; **Frigivne produkter efter kategori**.
2.  Åbn produktposten.
3.  Vælg produktet, der skal vejes.
4.  På oversigtspanelet **Detail** skal du ændre indstillingen **Produkt, der skal vejes** fra **Nej** til **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkroniser ændringerne til kanaldatabasen

1.  Gå til **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan**.
2.  Vælg distributionsplanen **1040**.
3.  Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.

Når dataene er synkroniseret, kontrollerer POS-enheden vægten for vægtangivelsen, når et produkt, der skal vejes, føjes til POS-transaktionen.

### <a name="signature-capture"></a>Signaturhentning

Enheden til hentning af virtuel signatur beder brugeren om at angive en signatur på tastaturet på enheden til hentning af virtuel signatur, når der bruges et betalingsmiddel, der kræver en signatur. Brugeren kan acceptere signaturen for at få den vist på POS-enheden. Kassereren kan derefter acceptere signaturen. Underskriften gemmes derefter sammen med betalingsmidlet og synkroniseres til back-office sammen med andre transaktionsdata.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Opret et betalingsmiddel, der kræver en signatur

1.  Gå til **Detail og handel** &gt; **Kanaler** &gt; **Detailbutikker** &gt; **Alle detailbutikker**.
2.  Vælg detailbutikken.
3.  Klik på **Rediger**.
4.  Klik på **Opsætning**, og i afsnittet **Opsætning** skal du derefter klikke på **Betalingsmetoder**.
5.  Klik på **Rediger**.
6.  Vælg den betalingsmetode, der kræver en signatur.
7.  I afsnittet **Generelt** under **Signaturhentning**, skal du angive indstillingen **Brug signaturhentningsenhed** til **Ja**.
8.  I feltet **Signaturhentning - minimum** skal du angive det minimumsbeløb, der skal udløse hentning af signatur.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkroniser ændringerne til kanaldatabasen

1.  Gå til **Detail og handel** &gt; **Detail-it** &gt; **Distributionsplan**.
2.  Vælg distributionsplanen **1070**.
3.  Klik på **Kør nu** for at synkronisere ændringer til POS-enheden.

Når dataene er synkroniseret, og der bruges et betalingsmiddel, som kræver en signatur, og beløbet overstiger grænseværdien, så vil POS-enheden bede om en signatur på enheden til hentning af virtuel signatur.

## <a name="additional-configuration"></a>Yderligere konfiguration
Du kan redigere konfigurationsfilen til simulatoren for eksterne enheder for at kunne løse de scenarier, du tester, mere hensigtsmæssigt. Du kan finde konfigurationsfilen på C:\\Programmer (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurationsfilen definerer de enheder, der er tilgængelige til test på vægten, de korttyper, der er tilgængelige til test, og stregkodetyper. Ved f.eks. at ændre tekstværdier i konfigurationsfilen, kan du tilføje en ny korttype eller måleenhed, der kan vælges på kørselstidspunktet. De nye værdier vises, når appen genstartes.

## <a name="troubleshooting"></a>Fejlfinding
Aktiviteter for simulatoren for eksterne enheder logføres i simulatoren for eksterne enheder. Du kan finde loggen på C:\\Programmer (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Simulatoren for eksterne enheder rapporterer også problemer til Windows-hændelsesloggen, som du kan få adgang til på **Logfiler for programmer og tjenester** &gt; **Microsoft** &gt; **DynamicsAX**. Hvis ændringer, du har foretaget i hardwareprofilen eller andre områder, ikke vises, når du bruger MPOS eller simulatoren for eksterne enheder, skal du kontrollere de distributionsplanlæggerjobs, du brugte til at synkronisere data til kanaldatabasen. Hvis ændringerne blev synkroniseret, men stadig ikke vises POS-enheden, skal du genstarte POS-klienten. Ændringer til konfigurerede pengeskuffer træder først i kraft, når der oprettes et nyt skift. Hvis du derfor foretager ændringer af pengeskuffer, skal du sørge for, at du altid lukker det eksisterende skift for at teste den nye opsætning af pengeskuffen. Hvis en producents driver er installeret efter de fælles kontrolobjekter fra Monroe Consulting Services, kan driveren nogle gange forårsage, at de fælles kontrolobjekter holder op med at fungere korrekt. I så fald skal du geninstallere de fælles kontrolobjekter.

<a name="see-also"></a>Se også
--------

[Oversigt over eksterne detailenheder](retail-peripherals-overview.md)




