---
title: Indgående lagerhandling i POS
description: I dette emne beskrives egenskaberne for den indgående lagerhandling af POS (Point Of Sale).
author: hhaines
manager: annbe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0f519ac3b5dd854d0c31b67382f46d0ab116ec7e
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071850"
---
# <a name="inbound-inventory-operation-in-pos"></a>Indgående lagerhandling i POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I Microsoft Dynamics 365 Commerce version 10.0.10 og nyere skal indgående og udgående handlinger på POS-stedet erstatte pluk- og modtagelseshandlingen.

> [!NOTE]
> I version 10.0.10 og nyere vil alle nye funktioner i POS-programmet, der er relateret til modtagelse af lagerbeholdninger i forhold til indkøbsordrer og flytteordrer, blive føjet til POS-handlingen **Indgående handling**. Hvis du i øjeblikket bruger pluk- og modtagelseshandlinger i POS, anbefales det, at du udvikler en strategi for flytning fra den pågældende handling til de nye indgående og udgående handlinger. Selvom pluk- og modtagelseshandlingen ikke fjernes fra produktet, vil der ikke være flere investeringer i den fra et funktionelt eller ydeevneperspektiv efter version 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Krav: Konfigurer en asynkron dokumentstruktur

Den indgående handling indeholder forbedringer af ydeevnen for at sikre, at brugere, der har mange kvitteringsposteringer på tværs af mange butikker eller firmaer og store lagerdokumenter, kan behandle disse dokumenter til Commerce Headquarters uden at få timeout eller fejl. Disse forbedringer kræver brug af en asynkron dokumentstruktur.

Når der bruges en asynkron dokumentstruktur, kan du knytte indgående dokumentændringer fra POS til Commerce Headquarters og derefter gå videre til andre opgaver, mens behandlingen til Commerce Headquarters udføres i baggrunden. Du kan kontrollere status for et dokument via dokumentlistesiden **Indgående handling** i POS for at sikre, at bogføringen er udført. I POS-programmet kan du også bruge listen over aktive dokumenter i indgående handling til at få vist dokumenter, der ikke kunne bogføres i Commerce Headquarters. Hvis et dokument mislykkes, kan POS-brugerne foretage rettelser og derefter prøve at behandle det i Commerce Headquarters igen.

> [!IMPORTANT]
> Den asynkrone dokumentstruktur skal konfigureres, før en virksomhed forsøger at bruge den indgående handling i POS.

Hvis du vil konfigurere en asynkron dokumentstruktur, skal du gennemføre følgende procedurer.

### <a name="create-and-configure-a-number-sequence"></a>Opret og konfigurer en nummerserie

1. Gå til **Organisationsadministration \> Nummerserier \> Nummerserier**.
2. På siden **Nummerserier** skal du oprette en nummerserie.
3. Angiv brugerdefinerede værdier i felterne **Nummerseriekode** og **Navn**.
4. Vælg **Tilføj** i oversigtspanelet **Referencer**.
5. Vælg **Commerce-parametre** i feltet **Område**.
4. Vælg **Retail-dokumenthandlings-id** i feltet **Reference**.
5. Indstil valget **Uafbrudt** til **Nej** i afsnittet **Opsætning** på oversigtspanelet **Generelt** for at sikre, at der ikke er problemer med ydeevnen.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Oprette og planlægge to batchjob for dokumentbehandlingen og overvågningen af opgaver

De batchjob, du opretter, bruges til at behandle dokumenter, der ikke fejler eller får timeout. De bruges også, når antallet af aktive lagerdokumenter, der behandles fra kasseapparatet, overskrider en systemkonfigureret værdi.

1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**.
2. Opret to batchjob på siden **Batchjob**:

    - Konfigurer det ene job til at køre klassen **RetailDocumentOperationMonitorBatch**.
    - Konfigurer det andet job til at køre klassen **RetailDocumentOperationProcessingBatch**.

2. Planlæg de nye batchjob, så de kører gentagne gange. Du kan f.eks. indstille planen, så jobbene køres hvert 5. minut.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Krav: Føj indgående handling til POS-skærmlayoutet

Før din organisation kan bruge funktionerne i indgående handling, skal den konfigurere POS-handlingen **Indgående handling** på et eller flere af dine [POS-skærmlayout](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Før du implementerer den nye handling i et produktionsmiljø, skal du sikre dig, at du tester den og lærer brugerne i at bruge den.

## <a name="overview"></a>Oversigt

Med den indgående handling kan POS-brugere udføre følgende opgaver:

- Modtage lagre i lagerbeholdning fra bekræftede indkøbsordredokumenter eller leverede dokumenter til flytteordren.
- Få vist oplysninger om historiske lagerkvitteringer for en periode på syv dage, efter at dokumentet er modtaget fuldt ud.
- Oprette anmodninger om ny indgående overflytningsordre.

Når den indgående handling startes fra POS-programmet, vises en listesidevisning. Denne visning viser åbne indkøbsordre- og flytteordredokumenter, hvor der er angivet lagerlinjer, der er planlagt til modtagelse af den aktuelle butik. Hvis brugerne vil finde og vælge et bestemt dokument, kan de rulle i listen eller bruge søgefunktionen.

Den indgående lagerdokumentliste indeholder tre faner:

- **Aktiv** – På denne fane vises dokumenter, der er helt eller delvist åbne, og som indeholder linjer eller antal på linjer, der stadig skal modtages.
- **Kladde** – På denne fane vises nye indgående anmodninger om overflytningsordrer, som butikken har oprettet. Dokumenterne er dog kun gemt lokalt. De er endnu ikke blevet sendt til Commerce Headquarters til behandling.
- **Fuldført** – På denne fane vises en liste over indkøbsordre- eller flytteordredokumenter, som butikken har modtaget helt i løbet af de seneste syv dage. Denne fane er udelukkende til orientering. Alle oplysninger om dokumenterne er skrivebeskyttede data til butikken.

Når du får vist dokumenter på en af fanerne, kan feltet **Status** hjælpe dig med at forstå det trin, som dokumentet er i.

- **Kladde** – Flytteordredokumentet er kun gemt lokalt i butikkens kanaldatabase. Der er endnu ikke blevet sendt oplysninger om flytteordreanmodningen til Commerce Headquarters.
- **Anmodet** – indkøbsordren eller flytteordren er blevet oprettet i Commerce Headquarters og er helt åben. Der er endnu ikke behandlet nogen kvitteringer i forhold til dokumentet. For dokumenter af typen af indkøbsordredokument kan modtagelsen påbegyndes når som helst, mens status **Anmodet**.
- **Delvist leveret** – Flytteordredokumentet har en eller flere linjer eller et delvist linjeantal, der er bogført som leveret af det udgående lagersted. Disse afsendte linjer kan modtages via den indgående handling.
- **Fuldt leveret** – Flytteordren har alle linjerne og det fulde linjeantal, der er bogført som leveret af det udgående lagersted. Hele dokumentet kan modtages via den indgående handling.
- **Delvist modtaget** – Nogle af linjerne eller linjemængderne i dokumentet for indkøbsordren eller flytteordren er modtaget af butikken, men nogle linjer forbliver åbne.
- **Fuldt modtaget** – Alle linjer og antal på indkøbsordre- eller flytteordredokumentet er blevet fuldt modtaget. Dokumenterne er kun tilgængelige under fanen **Fuldført**, og de er skrivebeskyttede til butikkens brugere.
- **I gang** – Denne status bruges til at informere enhedsbrugere om, at en anden bruger arbejder aktivt på dokumentet.
- **Midlertidigt afbrudt** – Denne status vises, efter at **Afbryd modtagelse** er valgt for midlertidigt at stoppe modtagelsesprocessen.
- **Behandling i HQ** – Dokumentet blev sendt til Commerce Headquarters fra POS-programmet, men det er endnu ikke bogført i Commerce Headquarters. Dokumentet går gennem den asynkrone dokumentbogføringsproces. Når dokumentet er bogført i Commerce Headquarters, skal statussen opdateres til **Fuldt modtaget** eller **Delvist modtaget**.
- **Behandlingen mislykkedes** – Dokumentet blev bogført til Commerce Headquarters og afvist. I ruden **Detaljer** vises årsagen til, at posteringsfejlen opstod. Dokumentet skal redigeres for at løse dataproblemer, og derefter skal det sendes til Commerce Headquarters igen til behandling.

Når du vælger en dokumentlinje på listen, vises ruden **Detaljer**. I denne rude vises yderligere oplysninger om dokumentet, f.eks. afsendelses- og datooplysninger. En statuslinje viser, hvor mange varer der mangler at blive behandlet. Hvis dokumentet ikke blev behandlet til Commerce Headquarters, viser ruden **Detaljer** også fejlmeddelelser vedrørende fejlen.

I dokumentlistens sidevisning kan du vælge **Ordredetaljer** på applinjen for at få vist dokumentoplysningerne. Du kan også aktivere modtagelsesbehandling for berettigede dokumentlinjer.

I dokumentlistens sidevisning kan du også oprette en ny anmodning om en indgående overførselsordre for en butik. Dokumenterne forbliver i statussen **Kladde**, og de kan justeres eller slettes, før de sendes til Commerce Headquarters til behandling. Når de er sendt til Commerce Headquarters, kan flytteordrelinjerne ikke længere ændres fra POS-programmet.

## <a name="receiving-process"></a>Modtagelsesproces

Når du har valgt et dokument i en indkøbsordre eller en flytteordre på fanen **Aktiv**, kan du vælge **Ordredetaljer** for at påbegynde modtagelsesprocessen.

Visningen **Modtager nu** vises som standard. Denne visning er optimeret til stregkodescanning. Den kan bruges til at oprette en liste over elementer, der er blevet scannet, så disse varer kan modtages. Hvis du vil påbegynde modtagelsesprocessen, kan du begynde at scanne varestregkoder.

Efterhånden som varestregkoder scannes i visningen **Modtager nu**, validerer programmet varerne i forhold til det valgte indkøbs- eller overførselsordredokument for at sikre, at hvert scannet element matcher en gyldig vare i dokumentet. I visningen **Modtager nu** antages det, at hver enkelt scanning af en stregkode skal repræsentere modtagelsen af et antal på én enhed, medmindre et antal er integreret i stregkoden. Du kan gentagne gange scanne stregkoder i denne visning for at oprette en liste over alle varer og antal til modtagelsen.

### <a name="example-scenario"></a>Eksempelscenario

En bruger modtager en indkøbsordre, der indeholder 10 enheder af stregkode 5657900266. Brugeren kan scanne denne stregkode 10 gange for at opdatere feltet **Modtager nu** med én enhed pr. scanning. Når brugeren har gennemført scanningerne, viser feltet **Modtager nu** for varens linje, at der er modtaget et antal på 10.

Alternativt kan brugeren i et scenarie, hvor antallet af varer er stort, foretrække at angive antallet manuelt i stedet for at scanne stregkoden for hver vare, der modtages. I det tilfælde kan brugeren scanne stregkoden én gang for at føje varen til listen **Modtager nu**. Brugeren kan derefter vælge den tilknyttede linje i visningen **Modtager nu** og derefter opdatere feltet **Modtagelsesantal** for varen i ruden **Detaljer**, der vises i højre side af siden.

Selvom visningen **Modtager nu** er optimeret til stregkodescanning, kan brugere også vælge **Modtag produkt** på applinjen og derefter angive vare-id'et eller stregkodedataene i en dialogboks. Når den angivne vare er valideret, bliver brugeren bedt om at angive modtagelsesantallet.

Visningen **Modtager nu** giver brugerne en fokuseret mulighed for at få vist, hvilke produkter de modtager. Du kan også bruge visningen **Komplet ordreliste**. Denne visning viser hele listen over dokumentlinjer for det valgte indkøbs- eller overførselsordredokument. Brugere kan manuelt vælge linje på listen og derefter opdatere feltet **Modtagelsesantal** i ruden **Detaljer** for den valgte linje. I visningen **Fuld ordreliste** kan brugerne scanne stregkoder, eller de kan bruge funktionen **Modtag produkt** til at angive vare-id'et eller stregkoden og dataene om det modtagne antal uden først at skulle vælge den tilsvarende varelinje på listen.

### <a name="over-receiving-validations"></a>Valideringer af overmodtagelser

Valideringer sker under modtagelsesprocessen for dokumentlinjerne. De indeholder valideringer for overlevering. Hvis en bruger forsøger at modtage mere lager, end der blev bestilt på en indkøbsordre, men overlevering ikke er konfigureret, eller det modtagne beløb overskrider den tolerance for overlevering, der er konfigureret for indkøbsordrelinjen, modtager brugeren en fejl og det er ikke tilladt at modtage for stort et antal.

Overmodtagelse er ikke tilladt for flytteordredokumenter. Brugere vil altid modtage fejl, hvis de forsøger at modtage mere end, der er leveret til flytteforslagslinjen.

### <a name="receiving-location-controlled-items"></a>Modtage placeringsstyrede varer

Hvis de varer, der modtages, er placeringsstyret, kan brugere vælge det sted, hvor varerne skal modtages, under modtagelsesprocessen. Det anbefales, at du konfigurerer en standardmodtagelsesplacering til dit butikslager stedet for at gøre denne proces mere effektiv. Selvom der er konfigureret en standardplacering, kan brugerne tilsidesætte modtagelsesplaceringen på de valgte linjer, når de har brug for det.

Handlingen respekterer konfigurationen af **Blank tilgang tilladt** på lagringsdimensionen **Sted** og kræver ikke, at der angives en placeringsdimension, hvis der er konfigureret en blank tilgang. Hvis blanke tilgangsplaceringer ikke er tilladt for en vare, viser POS-programmet en fejl og kræver, at der angives en placering, før modtagelsen kan bogføres.

### <a name="receive-all"></a>Modtag alle

Du kan vælge **Modtag alle** på applinjen efter behov for hurtigt at opdatere antallet i **Modtager nu** for alle dokumentlinjer til den maksimumværdi, der kan modtages for disse linjer.

### <a name="cancel-receiving"></a>Annuller modtagelse

Du bør kun bruge funktionen **Annuller modtagelse** på applinjen, hvis du vil have en sikkerhedskopi af dokumentet og ikke vil gemme ændringer. Du har f.eks. valgt et forkert dokument, og du vil ikke gemme nogen af de forrige modtagelsesdata.

### <a name="pause-receiving"></a>Afbryd modtagelse midlertidigt

Hvis du modtager lagerbeholdning, kan du bruge funktionen **Afbryd modtagelse**, hvis du vil tage en pause fra modtagelsesprocessen. Du kan f.eks. vælge at udføre en anden handling fra kasseapparatet, f.eks. ringe op til et kundesalg eller forsinke bogføringen af kvitteringen.

Når du vælger **Afbryd modtagelse**, ændres dokumentets status til **Midlertidigt afbrudt**. Derfor skal brugerne vide, hvilke data som er angivet for dokumentet, men dokumentet er ikke blevet bekræftet endnu. Når du er klar til at genoptage modtagelsesprocessen, skal du vælge det midlertidigt afbrudte dokument og derefter vælge **Ordredetaljer**. Alle antal i **Modtages nu**, der tidligere er gemt, bevares og kan vises fra visningen **Komplet ordreliste**.

### <a name="finish-receiving"></a>Afslut modtagelse

Når du er færdig med at angive alle mængder for **Modtager nu** for produkter, skal du vælge **Afslut modtagelse** på applinjen for at behandle kvitteringen.

Når brugere fuldfører en købsordrekvittering, bliver de bedt om at angive en værdi i feltet **Kvitteringsnummer**, hvis denne funktion er konfigureret. Denne værdi svarer typisk til id'et for kreditorfølgesedlen. Data for **Kvitteringsnummeret** gemmes i produktkvitteringskladden i Commerce Headquarters. Der hentes ikke kvitteringsnumre for overførslens ordrekvitteringer.

Når der bruges asynkron dokumentbehandling, sendes kvitteringen via en asynkron dokumentstruktur. Den tid, det tager, før det dokument, der skal bogføres, afhænger af dokumentets størrelse (antallet af linjer) og den generelle behandlingstrafik, der sker på serveren. Processen sker typisk i løbet af sekunder. Hvis dokumentbogføringen mislykkes, får brugeren vist dokumentlisten over **Indgående handlinger**, hvor dokumentstatus opdateres til **Behandling mislykkedes**. Brugeren kan derefter vælge det mislykkede dokument i kasseapparatet for at få vist fejlmeddelelserne og årsagen til fejlen i ruden **Detaljer**. Et mislykket dokument forbliver ikke-bogført og kræver, at brugeren vender tilbage til dokumentlinjerne ved at vælge **Ordredetaljer** i POS. Brugeren skal derefter opdatere dokumentet med rettelser på baggrund af fejlene. Når et dokument er rettet, kan brugeren forsøge at behandle det igen ved at vælge **Udfør opfyldelse** på applinjen.

## <a name="create-an-inbound-transfer-order"></a>Opret en indgående flytteordre

Fra POS kan brugere oprette nye dokumenter fra flytteordren. Hvis du vil starte processen, skal du vælge **Ny** på applinjen, mens du befinder dig i hoveddokumentlisten med **Indgående handlinger**. Du bliver derefter bedt om at vælge et **Overfør fra**-lagersted eller en butik, der skal levere lageret til din butiks placering. Værdierne er begrænset til den indstilling, der er defineret i konfigurationen af butikkens opfyldelsesgruppe. I en indgående overførselsanmodning vil din aktuelle butik altid være **Overførsel til**-lagersted for flytteordren. Denne værdi kan ikke ændres.

Du kan angive værdier i felterne **Afsendelsesdato**, **Modtagelsesdato** og **Leveringsmåde**, som du har brug for. Du kan også tilføje en note, der skal gemmes sammen med overflytningsordreoverskriften, som en vedhæftet fil i dokumentet i Commerce Headquarters.

Når oplysningerne i overskriften er oprettet, kan du føje produkter til flytteordren. Vælg **Tilføj produkt**for at starte processen med at tilføje varer og ønsket antal. I ruden **Detaljer** kan du også føje en linjespecifik bemærkning til kladdelinjerne. Disse noter gemmes som en linjevedhæftning.

Når linjerne er angivet på den indgående flytteordre, skal du vælge **Gem** for at gemme dokumentændringerne lokalt, eller **Send anmodning** for at indsende ordreoplysningerne til Commerce Headquarters til yderligere behandling. Hvis du vælger **Gem**, gemmes kladde dokumentet i kanaldatabasen, og det udgående lagersted kan ikke køre dokumentet, før det er blevet behandlet via **Indsend anmodning**. Du bør kun vælge **Gem**, hvis du ikke er klar til at bekræfte anmodningen til i Commerce Headquarters til behandling.

Hvis et dokument gemmes lokalt, findes det på fanen **Kladder** på dokumentlisten **Indgående handling**. Mens et dokument har statussen **Kladde**, kan du redigere det ved at vælge **Rediger**. Du kan opdatere, tilføje eller slette linjer efter behov. Du kan også slette hele dokumentet, mens det er i statussen **Kladde**, ved at vælge **Slet** på fanen **Kladder**.

Når kladdedokumentet er sendt til Commerce Headquarters, vises det under fanen **Aktiv** og har status som **Anmodet**. På dette tidspunkt kan brugere i det indgående lager eller lagersted ikke længere redigere det anmodede dokument for den indgående flytteordre. Det er kun brugere på det udgående lagersted, der kan redigere dokumentet ved at vælge **Udgående handling** i POS-programmet. Redigeringslåsen sikrer, at der ikke opstår konflikter, fordi en indgående anmoder ændrer overflytningsordren, samtidig med at den udgående afsender aktivt plukker og afsender ordren. Hvis der kræves ændringer fra det indgående lager eller lagersted, efter at flytteordren er sendt, skal den udgående afsender kontaktes og bedes om at angive ændringerne.

Når dokumentet har statussen **Anmodet**, vises det under fanen **Aktiv**. Det kan imidlertid endnu ikke modtages af det indgående lager eller lagersted. Når det udgående lagersted har afsendt nogle eller alle flytteordrer, kan det indgående lager eller lagersted bogføre kvitteringer i kasseapparatet. Når den udgående side behandler flytteordredokumenterne, opdateres deres status fra **Anmodet** til **Leveret** eller **Delvist leveret**. Når dokumenterne er i statussen **Leveret** eller **Delvist leveret**, kan det indgående lager eller lagersted bogføre kvitteringer i forhold til dem ved hjælp af den indgående handling for modtagelsesprocessen.

## <a name="related-topics"></a>Relaterede emner

[Udgående lagerhandling i POS](pos-outbound-inventory-operation.md)
