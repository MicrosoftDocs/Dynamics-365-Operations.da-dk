---
title: Retail ydre simulator
description: "Dette emne beskriver værktøjet ydre simulator, der følger med Microsoft Dynamics 365 for operationer – Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Retail ydre simulator

Dette emne beskriver værktøjet ydre simulator, der følger med Microsoft Dynamics 365 for operationer – Retail.

<a name="overview"></a>Overblik
--------

Microsoft Dynamics 365 for operationer – Retail ydre simulator er et værktøj, som hjælper dig med at oprette, teste og fejlfinding i forbindelse med ydre enheder, der bruges i retail-miljøer. Du kan bruge eksterne simulator, strømliner testforløb retail perifere og isolere problemer, der skyldes forkert installation eller funktionsfejl enhedsdrivere. Den ydre simulator omfatter ethvert program, der indeholder virtuelle versioner af enheder, Dynamics 365 for operationer – Retail understøtter. En sektion for hver virtuel enhed viser interaktionen mellem enheden og retail salgsstedet (POS). Du kan også bruge den til at give input, der gælder for forskellige scenarier i POS. Den ydre simulator understøtter interaktion mellem POS og følgende virtuelle enheder:

-   **Printer** – den ydre simulator kan vise kvitteringer, der er konfigureret for en POS-printer.
-   **Justere visningen** – du kan konfigurere en virtuel linjevisningen at vise aktivitet på en fysisk visning.
-   **Magnetstriben reader (MSR)** – du kan sende simulerede Magnetstriben hændelser til POS fra den ydre simulator.
-   **Skuffe til** – du kan simulere en fysisk pengeskuffen.
-   **Skuffe 2** – ved at oprette en anden kassen i den ydre simulator, kan du simulere situationer, der involverer en enkelt POS-kasseapparat med to aktive Skift.
-   **Scanner** – den virtuelle stregkodescanner, som understøtter eksterne simulator kan udstede stregkode scanning hændelser.
-   **Skala** – en virtuel skala, kan du simulere samspillet mellem vejede elementer og POS.
-   **Personligt id-nummer (PIN) pad** – du kan simulere PIN pad operationer. **Bemærk:** skal du implementere understøttelse af en fysisk PIN-tastatur via betalingsconnector.
-   **Registrering af signatur** – den ydre simulator indeholder en enhed til hentning af virtuelle signatur, som du kan konfigurere til at bede om signaturer, der er nødvendige for nogle bud, som debitorbetalinger konto.

Du kan også bruge det eksterne simulator til at simulere kile tastaturhændelser, der stammer fra en stregkodescanner og MSR. Den virtuelle ydre simulator understøtter specifikt Object Linking and Embedding for Retail POS (OPOS)-enheder.

## <a name="key-scenarios"></a>Vigtige situationer
### <a name="troubleshooting"></a>Fejlfinding

Du kan bruge eksterne simulator til fejlfinding i forbindelse med enhedsinstallation. Hvis du ikke har den ydre simulator eller en anden enhed af samme klasse, kan det være svært at finde ud af, hvor problemer stammer. Men når du har ydre simulator, kan du oprette virtuelle enheder og køre den samme kodestier og forretningslogik, der bruges til fysiske enheder. Fra et perspektiv af ydre simulator er den vigtigste forskel mellem virtuelle enheder og fysiske enheder serviceobjekt eller enhedsdriver. For fysiske enheder leveres serviceobjektet af enhedsproducenten. Derimod findes serviceobjekterne som en del af den ydre simulator for den ydre simulator. Når den ydre simulator fungerer korrekt, hvis en enhed ikke fungerer korrekt efter enhedsnavnet i hardwareprofilen er ændret til navnet på en faktisk enhed, kan du antage, at der er et problem med det serviceobjekt, der er leveret af producenten.

### <a name="training"></a>Kursus

Du kan bruge eksterne simulator til at tilføje et realistisk lag for at kassererens uddannelse, når en fysisk hardware opsætning er ikke tilgængelig. Når den ydre simulator indgår i uddannelse scenarier, kan kassereren mere effektivt interaktivt POS ved at levere input f.eks. produkt kode scanninger og gave kort swipes og ved at observere, hvilke tilgange der udskrives på en bestemt transaktion.

### <a name="testing"></a>Test

Du kan bruge den eksterne simulator til at teste produktstregkoder, modtagelse formater osv., uden at skulle implementere fysisk hardware i et virtuelt miljø. Da fysisk hardware ikke er obligatorisk, og du behøver ikke at installere en POS-klient på en fysisk computer eller en hardware-station, kan du hurtigt teste ændringer, der foretages i back-office.

## <a name="set-up-the-peripheral-simulator"></a>Konfigurer ydre simulator
### <a name="set-up-a-hardware-profile"></a>Oprette en hardwareprofil

1.  For at indstille den ydre simulator skal du gå til **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**.
2.  Hvis du vil oprette en ny profil, skal du klikke på **ny**.
3.  Angiv værdier i den **profil nummer** og **beskrivelse** felter.
4.  Brug følgende tabel til at konfigurere de virtuelle enheder, der skal testes. Her er en forklaring på kolonnerne i tabellen:
    -   **Enheden** – i denne kolonne vises navnet på det oversigtspanel, du udvider for at konfigurere enheden.
    -   **Enhedstypen** – denne kolonne indeholder den værdi, du vælger i feltet, der er mærket med navnet på enheden.
    -   **Enhedens navn** – i denne kolonne vises den nøjagtige værdi, du angiver for enhedens navn. **Vigtigt:** er nødvendige, de enhedsnavne, der er angivet her, fordi stationen hardware bruger disse specifikke navne til at adressere enhederne. Hvis du ikke bruger disse specifikke navne, kan ikke enheden bruges.

    | Enhed            | Enhedstype | Enhedens navn              |
    |-------------------|-------------|--------------------------|
    | Printer           | OPOS        | MockOPOSPrinter          |
    | Linjevisning      | OPOS        | MockOPOSLineDisplay      |
    | Magnetstribelæser               | OPOS        | MockOPOSMSR              |
    | Vekseludsteder            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Scanner           | OPOS        | MockOPOSScanner          |
    | Skaler             | OPOS        | MockOPOSScale            |
    | pinkodetastatur           | OPOS        | MockOPOSPinPad           |
    | Signaturhentning | OPOS        | MockOPOSSignatureCapture |

**Bemærk:** ikke nogen speciel Opsætning i hardwareprofilen, der kræves for at simulere tastaturhændelser kile fra stregkodescanner og MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Tildel hardwareprofilen til et kasseapparat

1.  Når du har oprettet hardwareprofilen, kan du gå til **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**registrerer**.
2.  I den **POS-kasseapparater** skal du klikke på linket i den **journalnummer** til det register, der skal bruge den ydre simulator.
3.  Klik på **Rediger**.
4.  I den **profiler** i sektionen på **hardwareprofil** skal du vælge den hardwareprofil, du oprettede til virtuelle enheder.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere ændringerne til databasen kanal

1.  Gå til **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplanen**.
2.  Vælg den **1090** distributionsplan.
3.  Klik på **kører nu** til at synkronisere ændringer i POS.

Når dataene er synkroniseret, er ny hardwareprofil og ændringer i registret tilgængelige i databasen kanal.

## <a name="install-the-peripheral-simulator"></a>Installere den ydre simulator
1.  Gå til **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**.
2.  Klik på **hente**, og klik derefter på **PeripheralSimulator**. **Bemærk:** skal du deaktivere pop op-blokeringer, før du kan hente den ydre simulator.
3.  Når overførslen er fuldført, kan du åbne den **henter** mappe, og dobbeltklik på **VirtualPeripherals.msi** til at starte installationsprogrammet.
4.  Installer den ydre simulator ved hjælp af standardindstillingerne.

Ud over de ydre simulator, skal du installere de fælles kontrol-objekter fra Monroe Consulting Services. Ellers er fungerer den ydre simulator ikke korrekt. For at hente de fælles kontrol-objekter, skal du gå til <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Ved hjælp af den ydre simulator
Klik for at starte den ydre simulator, **Start** på din computer, skal du skrive **Retail ydre simulator**, og vælg derefter app, når det vises i søgeresultaterne. Når du starter den ydre simulator, skal du klikke på navnet på en enhed til at se de understøttede enheder. Disse enheder vil blive vist som faner i venstre side af vinduet. For at få vist en bestemt enhed, skal du klikke på fanen for den pågældende enhed.

### <a name="line-display-capabilities"></a>Linje visningsmulighederne

Linjevisningen er den første enhed, der er angivet i den ydre simulator. Når virtuelle linjevisningen er konfigureret, vises linjeelementer, som de scannes i POS-transaktion. Foruden linjeelementer viser skærmen det totale, når et bud er markeret på POS. Det viser også den forfaldne saldo er angivet et bud, men en balance er stadig betales for posteringen. Når POS ikke bruges, kan en meddelelse vises for at angive, at skuffen er lukket. Du skal konfigurere meddelelsen på den **linje skærm** i hardwareprofilen i oversigtspanelet.

### <a name="cash-drawer-capabilities"></a>Kontant skuffe funktioner

Kassen er den anden enhed, der er angivet i den ydre simulator. Når hardwareprofilen er konfigureret til at bruge virtuelle pengeskuffer, POS åbner pengeskuffen for aktive skiftet som svar på kasseskuffe som betalingsmiddel erklæringer og så kassereren kan ændre eller deponere kontanter under standard cash-and-carry transaktioner. De virtuelle pengeskuffer har etiketterne **Main skuffe** og **sekundære skuffe**. Disse etiketter repræsenterer skuffe og skuffe 2 i hardwareprofilen, henholdsvis. Når en skuffe er lukket, vises et billede af en lukket kassen og knappen på lukkede kassen hedder **Åbn kasseskuffe**. Hvis du klikker på denne knap, erstattes billedet med et billede af en åben kassen til at angive, at kassen er nu åben. Knappen på åbne kasseskuffen hedder **Luk skuffen**. Flere handlinger ved POS kan forårsage pengeskuffen åbnes. De fleste handlinger kan ikke fortsætte, når kassen er åben. Undtagelserne er nogle procedurer i slutningen af dagen. Hvis POS-bruger modtager en fejlmeddelelse, der angiver, at en handling ikke kan udføres, mens kassen er åben, skal brugeren lukke virtuelle eller fysiske kassen for at fortsætte. Hvis en kassen er markeret som **delte** i hardwareprofilen, systemet ikke kontrollere, at kassen er lukket før en operation. Handlingen fortsætter som normalt, selvom kassen er åben. Problemet understøtter scenarier, hvor pengeskuffer deles sales associates, og hvor én knytte bruger en pengeskuffen, mens en anden kollega udfører ikke-relaterede opgaver på sin egen POS-enhed. Ændringer, der foretages til kassen er ikke klart, indtil det aktuelle skifte lukkes og åbnes et nyt Skift.

### <a name="msr-capabilities"></a>MSR-funktioner

Ydre simulator giver robust understøttelse af virtuelle MSR-handlinger ved at arbejde i enten OPOS eller tastatur kile tilstand. OPOS tilstand kræver, at MSR konfigureres i hardwareprofilen til at fungere som en OPOS-enhed. Kile tastaturtilstand sender blot data tastaturhændelser kile til Microsoft Windows. Ud over forskelle i opsætningen OPOS og tastatur kile-tilstande, der adskiller sig på følgende måder:

-   POS-klient kan OPOS MSR-enheder i bestemte scenarier som scenarier, der tillader Magnetstriben data til loyalitet eller gave kort post.
-   I kile tastaturtilstand sender ydre simulator tastatur kile data til det felt, der er aktiv, når data sendes. Denne funktionsmåde ligner, hvad der sker, hvis data, der er angivet ved hjælp af et tastatur. For at bruge MSR som en kile tastatur, skal brugeren skifte til Retail moderne POS (MPOS) for at sikre, at dataene er modtaget i det rette felt. Derfor kan du konfigurere en forsinkelse, så brugeren har tid til at sikre, at data vil blive sendt til det rette felt.

#### <a name="testing-gift-and-payment-card-swipes"></a>Test af gaver og betaling kort swipes

Virtuelle MSR, ydre simulator giver også kan du konfigurere specifikke MSR-data for at teste scenarier for gaver og betaling kort swipes. Du kan oprette et kort ved at klikke på plustegnet (**+**) knappen, og vælg typen kort. Angiv kortnummer, eller holde styr på data, der skal sendes til POS samt udløbsdato-måned og år for det kort, du definerer. Den værdi, du vælger i den **Type kort** er blot en etiket, der kan knyttes til et kort. Denne etiket gør det nemmere at identificere kort, når de er ført gennem kortlæser gennem ydre simulator. Du kan vælge kort, der er konfigureret i ydre simulator ved hjælp af venstre pil (**&lt;**) og den højre pil (**&gt;**) knapperne over billedet af kortet. Du kan redigere og slette kort ved hjælp af den **Rediger** og **slette** knapper ved siden af plus-tegnet (**+**) knappen.

### <a name="pin-pad"></a>Pinkodetastatur

Du kan konfigurere PIN pad simulator for at simulere en OPOS PIN-pad. Når en elektronisk overførsel (EFT) transaktion udføres på POS og kræver pinkoden, kalder hardware stationen PIN-enheden til at bede om pinkoden. Hvis du vil arbejde, kræver PIN-tastatur i den ydre simulator AUTORISATIONSKODE betaling connector understøttelse.

### <a name="printer"></a>Printer

Virtuelle ydre printeren viser blot tilgange, som de udskrives fra POS. Hvis en Udskriv-handling resulterer i flere leverancer, kan du rulle gennem tilgange.

#### <a name="configure-receipt-printing"></a>Konfigurere udskrivning af kvitteringer

1.  Gå til **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**hardwareprofiler**.
2.  Vælg den hardwareprofil, du oprettede til virtuelle enheder.
3.  På den **Printer** oversigtspanelet, skal du klikke på **Rediger**.
4.  I den **profil-ID'ET for kvittering** skal du vælge en kvitteringsprofil.
5.  Click **Save**.

### <a name="scale"></a>Skaler

Når et produkt skala er føjet til transaktionen POS, og en skala er konfigureret, henter POS vægt fra skala. For både den virtuelle og fysiske skala, skal produktet eller vægt angives, før produktet er føjet til transaktionen. Før du føjer produktet skala til transaktionen, gå til skala i ydre simulator, og brug plustegnet (**+**) og minustegnet (**–**) knapper til at justere den vægt, der skal rapportere omfanget. Du kan også angive den ønskede styrke direkte i den **aktuelle værdi** felt. Du kan justere enheder for vægt for skalaen ved hjælp af plus-tegnet (**+**), **Rediger**, og **slette** knapper. På denne måde kan enheder angives baseret på de produkter, der anvendes i, eller den landestandard, hvor skalaen anvendes.

#### <a name="configure-a-scale-product"></a>Konfigurere en skala-produkt

1.  Gå til **Retail og****commerce**&gt;**produkter og kategorier**&gt;**frigivne produkter efter kategori**.
2.  Åbne produktposten.
3.  Vælg produktet til veje.
4.  På den **Retail** Angiv i oversigtspanelet på **skala produkt** indstilling fra **Nej** til **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere ændringerne til databasen kanal

1.  Gå til **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplanen**.
2.  Vælg den **1040** distributionsplan.
3.  Klik på **kører nu** til at synkronisere ændringer i POS.

Når dataene er synkroniseret, når et produkt skala er føjet til transaktionen POS, kontrollerer POS skalering for vægt.

### <a name="signature-capture"></a>Signaturhentning

Hentningsenhed virtuelle signatur beder brugeren om at angive en signatur på virtuelle signatur capture pad, når det bud, der bruges, kræver en signatur. Brugeren kan acceptere signatur for at få den vist ved POS. Kassereren kan derefter acceptere signaturen. Underskriften gemmes sammen med buddet og synkroniseres til kontoret sammen med andre transaktionsdata.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Oprette et bud til at kræve en signatur

1.  Gå til **detail- og commerce**&gt;**kanaler**&gt;**Retail butikker**&gt;**alle retail butikkerne**.
2.  Vælg detailbutikken.
3.  Klik på **Rediger**.
4.  Klik på **opsætning af**, og derefter i den **angive** skal du klikke på **betalingsmetoder**.
5.  Klik på **Rediger**.
6.  Vælg den betalingsmetode, der kræver en signatur.
7.  I den **generelle** under afsnit **signatur Capture**, skal du angive den **signatur capture enhed** at **Ja**.
8.  I den **signatur fangst-minimumsbeløb** skal du angive det minimumbeløb, der skal udløse registrering af signatur.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere ændringerne til databasen kanal

1.  Gå til **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplanen**.
2.  Vælg den **1070** distributionsplan.
3.  Klik på **kører nu** til at synkronisere ændringer i POS.

Når dataene er synkroniseret, når der bruges et bud, der kræver en signatur, og beløbet, der overholder grænsen signatur, beder POS om en signatur på enheden til hentning af virtuelle signatur.

## <a name="additional-configuration"></a>Yderligere konfiguration
Du kan redigere den ydre simulator konfigurationsfil for at løse de scenarier, som du tester mere hensigtsmæssigt. Du kan finde konfigurationsfilen på C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurationsfilen definerer de enheder, der er tilgængelige til test på skalaen, korttyper, der er tilgængelige til test og typer af stregkoden. For eksempel ved at ændre tekstværdier i konfigurationsfilen, kan du føje en ny korttype eller enhed, der kan vælges på kørselstidspunktet. De nye værdier vises, når programmet genstartes.

## <a name="troubleshooting"></a>Fejlfinding
Aktiviteter for den ydre simulator logføres i den ydre simulator. Du kan finde logfilen på C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Ydre simulator også rapporterer problemer til Windows-hændelsesloggen, hvor du kan få adgang til **program and Services Logs**&gt;**Microsoft**&gt;**Dynamics AX**. Hvis ændringer, du har foretaget til hardwareprofilen eller andre områder ikke ses, når du bruger MPOS eller ydre simulator, kontrollere distributionen planlægger-job, som du brugte til at synkronisere data til databasen kanal. Hvis ændringerne blev synkroniseret, men stadig ikke er tydelige tegn på POS, genstarte POS-klienten. Konfigurerede pengeskuffer ændringer ikke gældende, indtil der oprettes et nyt Skift. Derfor, hvis du ændrer pengeskuffer, Sørg for, at du altid lukke eksisterende Skift for at teste den nye opsætning af kontant skuffe. Nogle gange, hvis en producent driver installeres efter de almindelige kontrol-objekter fra Monroe Consulting Services, kan driveren forårsage de fælles kontrol-objekter fungerer ikke korrekt. I så fald skal du geninstallere de almindelige kontrol-objekter.

<a name="see-also"></a>Se også
--------

[Retail peripherals overview](retail-peripherals-overview.md)


