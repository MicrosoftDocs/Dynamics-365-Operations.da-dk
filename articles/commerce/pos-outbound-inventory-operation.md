---
title: Udgående lagerhandling i POS
description: I dette emne beskrives egenskaberne for den udgående lagerhandling af POS (Point Of Sale).
author: hhaines
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3cfe144f7bba2bbc4b25024b68155045271f6366
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795639"
---
# <a name="outbound-inventory-operation-in-pos"></a>Udgående lagerhandling i POS

[!include [banner](includes/banner.md)]


I Microsoft Dynamics 365 Commerce version 10.0.10 og nyere skal indgående og udgående handlinger på POS-stedet erstatte pluk- og modtagelseshandlingen.

> [!NOTE]
> I version 10.0.10 og nyere vil alle nye funktioner i POS-programmet, der er relateret til modtagelse af lagerbeholdninger i forhold til indkøbsordrer og flytteordrer, blive føjet til handlingen Indgående handling. Hvis du i øjeblikket bruger pluk- og modtagelseshandlinger i POS, anbefales det, at du udvikler en strategi for flytning fra den pågældende handling til de nye indgående og udgående handlinger. Selvom pluk- og modtagelseshandlingen ikke fjernes fra produktet, vil der ikke være flere investeringer i den fra et funktionelt eller ydeevneperspektiv efter version 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Krav: Konfigurer en asynkron dokumentstruktur

Den udgående handling indeholder forbedringer af ydeevnen for at sikre, at brugere, der har mange modtagelsesposteringer på tværs af mange butikker eller firmaer og store lagerdokumenter, kan behandle disse dokumenter til Commerce Headquarters (HQ) uden at få timeout eller fejl. Disse forbedringer kræver brug af en asynkron dokumentstruktur.

Når der bruges en asynkron dokumentstruktur, kan du knytte udgående dokumentændringer fra POS til Commerce Headquarters (HQ) og derefter gå videre til andre opgaver, mens behandlingen til Commerce Headquarters (HQ) udføres i baggrunden. Du kan kontrollere status for dokumentet via dokumentlistesiden **Udgående handling** i POS for at sikre, at bogføringen er udført. I POS-programmet kan du også bruge listen over aktive dokumenter i udgående handling til at få vist dokumenter, der ikke kunne bogføres i Commerce Headquarters (HQ). Hvis et dokument mislykkes, kan POS-brugerne foretage rettelser og derefter prøve at behandle det i Commerce Headquarters (HQ) igen.

> [!IMPORTANT]
> Den asynkrone dokumentstruktur skal konfigureres, før en virksomhed forsøger at bruge den udgående handling i POS.

Hvis du vil konfigurere en asynkron dokumentstruktur, skal du gennemføre følgende procedurer.

### <a name="create-and-configure-a-number-sequence"></a>Opret og konfigurer en nummerserie

1. Gå til **Organisationsadministration \> Nummerserier \> Nummerserier**.
2. På siden **Nummerserier** skal du oprette en nummerserie.
3. Angiv brugerdefinerede værdier i felterne **Nummerseriekode** og **Navn**.
4. Vælg **Tilføj** i oversigtspanelet **Referencer**.
5. Vælg **Commerce-parametre** i feltet **Område**.
6. Vælg **Retail-dokumenthandlings-id** i feltet **Reference**.
7. Indstil valget **Uafbrudt** til **Nej** i afsnittet **Opsætning** på oversigtspanelet **Generelt** for at sikre, at der ikke er problemer med ydeevnen.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Oprette og planlægge to batchjob for dokumentbehandlingen og overvågningen af opgaver

> [!NOTE]
> I Commerce version 10.0.13 og nyere behøver du ikke konfigurere batchjobbene i batchjobbet-frameworket. Batchprocesserne kan konfigureres fra  menuen **Retail og Commerce >Retail og Commerce IT**. Brug menuindstillingerne **Retail-dokumenbetjeningsovervågning** og **Retail-dokumentbetjeningsbehandling** for at konfigurere batchjobbene

De batchjob, du opretter, bruges til at behandle dokumenter, der ikke fejler eller får timeout. De bruges også, når antallet af aktive lagerdokumenter, der behandles fra kasseapparatet, overskrider en systemkonfigureret værdi.

1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**.
2. Opret to batchjob på siden **Batchjob**:

    - Konfigurer det ene job til at køre klassen **RetailDocumentOperationMonitorBatch**.
    - Konfigurer det andet job til at køre klassen **RetailDocumentOperationProcessingBatch**.

3. Planlæg de nye batchjob, så de kører gentagne gange. Du kan f.eks. indstille planen, så jobbene køres hvert 5. minut.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Krav: Føj udgående handling til POS-skærmlayoutet

Før din organisation kan bruge funktionerne i udgående handling, skal den konfigurere POS-handlingen **Udgående handling** på et eller flere af dine [POS-skærmlayout](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Før du implementerer den nye handling i et produktionsmiljø, skal du sikre dig, at du tester den og lærer brugerne i at bruge den.

## <a name="overview"></a>Oversigt

Med den udgående handling kan POS-brugere udføre følgende opgaver:

- Bogføre forsendelser for flytteordredokumenter i tilfælde, hvor brugerens butik er det angivne udgående lagersted.
- Få vist oplysninger om historiske flytteordreforsendelser, der er bogført af butikken.
- Oprette anmodninger om ny udgående overflytningsordre.

Når den udgående handling startes fra POS-programmet, vises en listesidevisning. Denne visning viser åbne flytteordredokumenter, der har lagerlinjer, om at brugerens nuværende butik er beregnet til at afsende og opfylde. Hvis brugerne vil finde og vælge et dokument, kan de rulle i listen eller bruge søgefunktionen.

Den udgående lagerdokumentliste indeholder tre faner.

- **Aktiv** – På denne fane vises flytteordrer, der har statussen **Anmodet** eller **Delvist leveret**. Ordrerne indeholder linjer eller antal på linjer, der skal leveres af brugerens aktuelle butik. På denne fane vises også ordrer, der har statussen **Behandles i HQ** (dvs., at de venter på bekræftelse af en vellykket bogføring fra Commerce Headquarters (HQ)), eller **Behandling mislykkedes** (dvs. at bogføring til Commerce Headquarters (HQ) ikke lykkedes, og brugeren skal rette data og prøve at sende ordrerne igen).
- **Kladde** – På denne fane vises nye udgående anmodninger om overflytningsordrer, som brugerens butik har oprettet. Dokumenterne er dog kun gemt lokalt. De er endnu ikke blevet sendt til Commerce Headquarters (HQ) til behandling.
- **Fuldført** – På denne fane vises en liste over flytteordredokumenter, som butikken har afsendt helt i løbet af de seneste syv dage. Denne fane er udelukkende til orientering. Alle oplysninger om dokumenterne er skrivebeskyttede data til butikken.

Når du får vist dokumenter på en af fanerne, kan feltet **Status** hjælpe dig med at forstå det trin, som dokumentet er i.

- **Kladde** – Flytteordredokumentet er kun gemt lokalt i butikkens kanaldatabase. Der er endnu ikke blevet sendt oplysninger om flytteordreanmodningen til Commerce Headquarters (HQ).
- **Anmodet** – indkøbsordren eller flytteordren er blevet oprettet i Commerce Headquarters (HQ) og er helt åben. Brugerens aktuelle butik har endnu forarbejdet nogen forsendelser i forhold til dokumentet.
- **Delvist leveret** – Flytteordredokumentet har en eller flere linjer eller et delvist linjeantal, der er bogført som leveret af det udgående lagersted. Disse afsendte linjer kan modtages via den indgående handling.
- **Fuldt leveret** – Flytteordren har alle linjerne og det fulde linjeantal, der er bogført som leveret af det udgående lagersted.
- **I gang** – Denne status bruges til at informere enhedsbrugere om, at en anden bruger arbejder aktivt på dokumentet.
- **Midlertidigt afbrudt** – Denne status vises, efter at **Afbryd modtagelse** er valgt for midlertidigt at stoppe modtagelsesprocessen.
- **Behandling i HQ** – Dokumentet blev sendt til Commerce Headquarters (HQ) fra POS-programmet, men det er endnu ikke bogført i Commerce Headquarters (HQ). Dokumentet går gennem den asynkrone dokumentbogføringsproces. Når dokumentet er bogført i Commerce Headquarters (HQ), skal statussen opdateres til **Fuldt modtaget** eller **Delvist modtaget**.
- **Behandlingen mislykkedes** – Dokumentet blev bogført til Commerce Headquarters (HQ) og afvist. I ruden **Detaljer** vises årsagen til, at posteringsfejlen opstod. Dokumentet skal redigeres for at løse dataproblemer, og derefter skal det sendes til Commerce Headquarters (HQ) igen til behandling.

Når du vælger en dokumentlinje på listen, vises ruden **Detaljer**. I denne rude vises yderligere oplysninger om dokumentet, f.eks. afsendelses- og datooplysninger. En statuslinje viser, hvor mange varer der mangler at blive behandlet. Hvis dokumentet ikke blev behandlet til Commerce Headquarters (HQ), viser ruden **Detaljer** også fejlmeddelelser vedrørende fejlen.

I dokumentlistens sidevisning kan du vælge **Ordredetaljer** på applinjen for at få vist dokumentoplysningerne. Du kan også aktivere modtagelsesbehandling for berettigede dokumentlinjer.

I dokumentlistens sidevisning kan du også oprette en ny udgående overførselsordre for en butik.

## <a name="transfer-order-shipping-process"></a>Proces for flytteordrens afsendelse

Når du har valgt et flytteordredokument på fanen **Aktiv**, kan du vælge **Ordredetaljer** for at påbegynde opfyldelsesprocessen. Visningen **Fuld ordreliste** vises. På denne side vises alle de dokumentlinjer, der indeholder varen. Der vises også oplysninger om det bestilte antal.

Hver scanning af en stregkode opdaterer antallet i feltet **Sender nu** med én enhed. Du kan også angive et afsendelsesantal ved at vælge **Afsend produkt** på applinjen, angive et vare-id og derefter angive antallet. Hvis varen er placeringsstyret, kan du bekræfte eller angive forsendelsesplaceringen for dokumentlinjen.

I visningen **Fuld ordreliste** kan du manuelt vælge en linje på listen og derefter opdatere antallet i **Afsender nu** for den valgte linje i ruden **Detaljer**.

### <a name="over-delivery-shipping-validations"></a>Leveringsvalideringer for overlevering

Valideringer sker under modtagelsesprocessen for dokumentlinjerne. De indeholder valideringer for overlevering. Hvis en bruger forsøger at modtage mere lager, end der blev bestilt på en indkøbsordre, men overlevering ikke er konfigureret, eller det modtagne antal overskrider den tolerance for overlevering, der er konfigureret for indkøbsordrelinjen, modtager brugeren en fejl og det er ikke tilladt at modtage for stort et antal.

### <a name="underdelivery-close-lines"></a>Lukkelinjer ved underlevering

I Commerce version 10.0.12 blev der tilføjet en funktionalitet, så POS-brugere kan lukke eller annullere det resterende antal under udgående ordreforsendelse, hvis det udgående lagersted bestemmer, at det fulde antal, der er anmodet om, ikke kan leveres. Antal kan også lukkes eller annulleres senere. Hvis du vil bruge denne funktion, skal firmaet være konfigureret til at tillade underlevering af flytteordrer. Derudover skal der defineres en underleveringsprocent til flytteordrelinjen.

Hvis du vil konfigurere firmaet, så der tillades underlevering af flytteordrer, skal du i Commerce Headquarters (HQ) gå til **Lagerstyring \> Opsætning \> Parametre til lager- og lagerstedsstyring**. På siden **Parametre til lager- og lokationsstyring** skal du under fanen **Flytteordrer** aktivere parameteren **Accepter underlevering**. Kør derefter distributionsplanlægningsjobbet **1070** for at synkronisere parameterændringerne til din butikskanal.

Underleveringsprocenter for en flytteordrelinje kan foruddefineres for produkter som del af produktkonfigurationen i Commerce Headquarters. Alternativt kan de angives eller overskrives på en bestemt flytteordrelinje via Commerce Headquarters (HQ).

Når en organisation har afsluttet konfigurationen af flytteordren med underlevering, vil brugerne af POS få vist en ny indstilling **Luk restantal** i ruden **Detaljer**, når de vælger en udgående flytteordrelinje via funktionen **Udgående handlinger**. Når brugeren fuldfører forsendelsen ved at bruge processen **Afslut opfyldelse**, kan de sende en anmodning til Commerce Headquarters (HQ) om at annullere det resterende ikke-afsendte antal. Hvis brugeren lukker restantallet, foretager Commerce en validering for at kontrollere, at det antal, der annulleres, er inden for den procentvise tolerance, der er defineret på flytteordrelinjen. Hvis underleveringstolerancen overskrides, vises en fejlmeddelelse, og brugeren kan ikke lukke restantallet, før det tidligere afsendte antal og "Send nu"-antal opfylder eller overholder tolerancen for underleveringen.

Når forsendelsen er blevet synkroniseret med Commerce Headquarters (HQ), opdateres de antal, der er defineret i feltet **Afsend nu** for flytteordrelinjen i POS, til en status som afsendt i Commerce Headquarters (HQ). Alle ikke-afsendte antal, der tidligere ville være anset for at være antal for "Resterende forsendelse" (dvs. antal, der skal leveres senere), i stedet anses for at være annullerede antal. Antallet for "Resterende forsendelse" for flytteordrelinje er angivet til **0** (nul), og linjen betragtes som fuldt afsendt.

### <a name="shipping-location-controlled-items"></a>Afsende placeringsstyrede varer

Hvis de varer, der afsendes, er placeringsstyret, kan brugerne vælge det sted, hvor de vil udstede lageret fra, under afsendelsesprocessen. Det anbefales, at du konfigurerer en standardudstedelsesplacering til dit butikslager stedet for at gøre denne proces mere effektiv. Selvom der er konfigureret en standardplacering, kan brugerne tilsidesætte udstedelsesplaceringen på de valgte linjer, når de har brug for det.

Handlingen respekterer konfigurationen af **Blank tilgang tilladt** på lagringsdimensionen **Sted** og kræver ikke, at der angives en placeringsdimension, hvis der er konfigureret en blank tilgang. Hvis blanke tilgangsplaceringer ikke er tilladt for en vare, viser POS-programmet en fejl og kræver, at der angives en placering, før modtagelsen kan bogføres.

### <a name="ship-all"></a>Send alle

Du kan vælge **Afsend alle** på applinjen efter behov for hurtigt at opdatere antallet i **Afsender nu** for alle dokumentlinjer til den maksimumværdi, der kan opfyldes for disse linjer.

### <a name="cancel-fulfillment"></a>Annuller opfyldelse

Brug kun funktionen **Annuller opfyldelse** på applinjen, hvis du vil have en sikkerhedskopi af dokumentet og ikke vil gemme ændringer. Du har f.eks. valgt et forkert dokument, og du vil ikke gemme nogen af de forrige afsendelsesdata.

### <a name="pause-fulfillment"></a>Afbryd opfyldelse midlertidigt

Hvis du opfylder en overførselsordre, kan du bruge funktionen **Afbryd opfyldelse**, hvis du vil tage en pause fra processen. Du kan f.eks. vælge at udføre en anden handling fra kasseapparatet, f.eks. ringe op til et kundesalg eller forsinke bogføringen af afsendelsen til Commerce Headquarters (HQ).

Når du vælger **Afbryd opfyldelse**, ændres dokumentets status til **Midlertidigt afbrudt**. Derfor skal brugen vide, hvilke data som er angivet i dokumentet, men dokumentet er ikke blevet bekræftet endnu. Når du er klar til at genoptage opfyldelsesprocessen, skal du vælge det midlertidigt afbrudte dokument og derefter vælge **Ordredetaljer**. Alle antal i **Afsender nu**, der tidligere er gemt, vil blive bevaret og kan vises fra visningen **Komplet ordreliste**.

### <a name="review"></a>Gennemse

Før den endelige forpligtelse af opfyldelsen til Commerce Headquarters (HQ) kan du bruge funktionen til **Gennemse** til at validere det udgående dokument. Denne funktion vil give dig besked om manglende eller forkerte data, der kan forårsage behandlingsfejl, og giver dig mulighed for at rette problemer, før opfyldelsesanmodningen sendes. Hvis du vil aktivere funktionen **Gennemse** på applinjen, skal du aktivere funktionen **Aktivér validering i indgående og udgående POS-lagerhandlinger** via arbejdsområdet Funktionsstyring i Commerce Headquarters (HQ).

Funktionen **Gennemse** validerer følgende problemer i et udgående dokument:
- **Overlevering** – antallet til levering er nu større end det bestilte antal. Problemets alvor bestemmes af konfigurationen af overlevering i Commerce Headquarters (HQ).
- **Underlevering** – antallet til levering er nu mindre end det bestilte antal. Problemets alvor bestemmes af konfigurationen af underlevering i Commerce Headquarters (HQ).
- **Serienummer** – serienummeret er ikke angivet eller ikke tilgængeligt for en serialiseret vare, der kræver, at der registreres et serienummer på lageret.
- **Lokationen er ikke angivet** – lokationen er ikke angivet for en lokationsstyret vare, hvor blank lokation ikke er tilladt.
- **Slettede linjer** – ordren indeholder linjer, der er slettet af Commerce Headquarters (HQ), og som ikke er kendt for POS-programmet.

Hvis du angiver parameteren **Aktivér automatisk validering** til **Ja** i **Commerce-parametre** > **Lager** > **Handlinger for butikslager**, udføres valideringen automatisk, når du vælger funktionen **Fuldfør opfyldelse**.

### <a name="finish-fulfillment"></a>Fuldfør opfyldelse

Når du er færdig med at angive alle mængder for **Afsender nu** for produkter, skal du vælge **Afslut opfyldelse** på applinjen for at behandle kvitteringen.

Når der bruges asynkron dokumentbehandling, sendes kvitteringen via en asynkron dokumentstruktur. Den tid, det tager, før det dokument, der skal bogføres, afhænger af dokumentets størrelse (antallet af linjer) og den generelle behandlingstrafik, der sker på serveren. Processen sker typisk i løbet af sekunder. Hvis dokumentbogføringen mislykkes, får brugeren vist dokumentlisten over **Udgående handling** på fanen **Aktiv**, hvor dokumentets status vil blive opdateret til **Behandling mislykkedes**. Brugeren kan derefter vælge det mislykkede dokument i kasseapparatet for at få vist fejlmeddelelserne og årsagen til fejlen i ruden **Detaljer**. Et mislykket dokument forbliver ikke-bogført og kræver, at brugeren vender tilbage til dokumentlinjerne ved at vælge **Ordredetaljer** i POS. Brugeren skal derefter opdatere dokumentet med rettelser på baggrund af fejlene. Når et dokument er rettet, kan brugeren forsøge at behandle det igen ved at vælge **Udfør opfyldelse** på applinjen.

## <a name="create-an-outbound-transfer-order"></a>Opret en udgående flytteordre

Fra POS kan brugere oprette nye dokumenter fra flytteordren. Hvis du vil starte processen, skal du vælge **Ny** på applinjen, mens du befinder dig i hoveddokumentlisten med **Udgående handlinger**. Du bliver derefter bedt om at vælge et **Overfør til**-lagersted eller en butik, som din nuværende butik vil sende lager til. Værdierne er begrænset til den indstilling, der er defineret i konfigurationen af butikkens opfyldelsesgruppe. I en udgående overførselsanmodning vil din aktuelle butik altid være **Overførsel fra**-lagersted for flytteordren. Denne værdi kan ikke ændres.

Du kan angive værdier i felterne **Afsendelsesdato**, **Modtagelsesdato** og **Leveringsmåde**, som du har brug for. Du kan også tilføje en note, der skal gemmes sammen med overflytningsordreoverskriften, som en vedhæftet fil i dokumentet i Commerce Headquarters (HQ).

Når oplysningerne i overskriften er oprettet, kan du føje produkter til flytteordren. Du starter processen med at tilføje varer og ønsket antal ved at scanne stregkoder eller vælge **Tilføj produkt**.

Når linjerne er angivet på den udgående flytteordre, skal du vælge **Gem** for at gemme dokumentændringerne lokalt, eller **Send anmodning** for at indsende ordreoplysningerne til Commerce Headquarters (HQ) til yderligere behandling. Hvis du vælger **Gem**, gemmes kladde dokumentet i kanaldatabasen, og det udgående lagersted kan ikke køre dokumentet, før det er blevet behandlet via **Indsend anmodning**. Vælg kun **Gem**, hvis du ikke er klar til at bekræfte anmodningen i Commerce Headquarters (HQ) til behandling.

Hvis et dokument gemmes lokalt, findes det på fanen **Kladder** på dokumentlisten **Indgående handling**. Mens et dokument har statussen **Kladde**, kan du redigere det ved at vælge **Rediger**. Du kan opdatere, tilføje eller slette linjer efter behov. Du kan også slette hele dokumentet, mens det er i statussen **Kladde**, ved at vælge **Slet** på fanen **Kladder**.

Når kladdedokumentet er sendt til Commerce Headquarters (HQ), vises det under fanen **Aktiv** og har status som **Anmodet**. På dette punkt er det kun brugere på det udgående lagersted, der kan redigere dokumentet ved at vælge **Udgående handling** i POS-programmet. Brugere på det indgående lagersted kan få vist flytteordren på fanen **Aktiv** på dokumentlisten **Indgående handling**, men de kan ikke redigere eller slette den. Redigeringslåsen sikrer, at der ikke opstår konflikter, fordi en indgående anmoder ændrer overflytningsordren, samtidig med at den udgående afsender aktivt plukker og afsender ordren. Hvis der kræves ændringer fra det indgående lager eller lagersted, efter at flytteordren er sendt, skal den udgående afsender kontaktes og bedes om at angive ændringerne.

Når dokumentet har status **Anmodet**, er det klar til opfyldelse af behandling af det udgående lagersted. Når afsendelsen behandles vha. den udgående handling, opdateres flytteordredokumentets status fra **Anmodet** til **Fuldt afsendt** eller **Delvist afsendt**. Når dokumenterne er i statussen **Fuldt afsendt** eller **Delvist afsendt**, kan det indgående lager eller lagersted bogføre kvitteringer i forhold til dem ved hjælp af den indgående handling for modtagelsesprocessen.

Fuldt afsendte flytteordrer flyttes til fanen **Fuldført** på dokumentlisten **Udgående handling**. Dér er de stadig synlige for brugere i det udgående lager eller lagersted i skrivebeskyttet tilstand i syv dage.

## <a name="related-topics"></a>Relaterede emner

[Indgående lagerhandling i POS](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]