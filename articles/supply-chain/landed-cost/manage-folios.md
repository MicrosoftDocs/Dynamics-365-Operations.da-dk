---
title: Administrere folioer
description: Dette emne beskriver, hvordan du kan arbejde med folioer. En folio består typisk af en leverandørs varer for én enhed eller ét firma pr. forsendelse. Varerne i en folio kan være i én container eller være fordelt på flere containere.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 99159d2197648b8f17a719b74c8cd6ea4bffe550
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833827"
---
# <a name="manage-folios"></a>Administrere folioer

[!include [banner](../../includes/banner.md)]

En folio bestemmes ofte af toldlovgivningen. Den kan bestå af en leverandørs varer for én enhed eller ét firma pr. forsendelse. Varerne i en folio kan være i én container eller være fordelt på flere containere.

Du kan åbne siden **Alle folioer** ved at gå til **Landingsomkostninger \> Folioer \> Alle folioer**. På denne side vises en liste over alle aktuelle folioer. Du kan oprette, slette og arbejde med folioer ved at bruge knapperne i handlingsruden. Vælg en folio på listen for at få vist detaljerne på siden **Folioer**.

## <a name="action-pane"></a>Handlingsrude

Handlingsruden på siderne **Alle folioer** og **Folioer** indeholder knapper, der giver dig mulighed for at arbejde med en valgt folio. Hver knap udfører en enkelt handling. Handlingsruden indeholder også faner, som hver isæt indeholder et sæt relaterede knapper. Medmindre andet er angivet, er alle de knapper og faner, der beskrives i følgende undersektioner, tilgængelige både i listevisningen (det vil sige på siden **Alle folioer**) og i den detaljerede visning (det vil sige på siden **Folioer**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knapper, der vises direkte i handlingsruden

I følgende tabel beskrives de knapper, der er direkte tilgængelige i handlingsruden.

| Knap | Beskrivelse |
|---|---|
| Nye | Opret en folio. |
| Delete | Slet den åbne eller valgte folio. |
| Ruteomkostninger | Åbn siden **Fragtomkostninger**, hvor du kan se og føje omkostninger på folioniveau til alle varerne i fragten. Når folioomkostninger føjes til fragten manuelt, føjes de automatisk til forespørgselssiden for omkostninger og fordeles på alle varer i overensstemmelse med den metode, der er angivet på siden **Fragtomkostninger**. |

### <a name="buttons-on-the-manage-tab"></a>Knapper under fanen Administrer

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Administrer**.

| Knap | Beskrivelse |
|---|---|
| Bogfør tilgangsliste | Bogfør en tilgangsliste for alle indkøbsordrelinjer i folioen. Hvis der bruges forsendelser for flere virksomheder, åbnes en ny dialogboks til bogføring af tilgangslisten for hvert firma. |
| Bogfør produktkvittering | Bogfør en produktkvittering for alle indkøbsordrelinjer i folioen. Hvis der bruges fragter for flere virksomheder, åbnes en ny produktkvittering til bogføring for hvert firma. |
| Bogfør faktura | Bogfør en faktura for alle indkøbsordrelinjer i folioen. Hvis der bruges fragter for flere virksomheder, åbnes en ny dialogboks til fakturabogføring for hvert firma. |
| Forsendelsesflytteordre | Bogfør en flytteordre for alle flytteordrelinjer, der er relateret til den aktuelle folio i den relaterede forsendelse. |
| Modtag flytteordre | Bogfør en flytteordrekvittering for alle flytteordrelinjer, der er relateret til den aktuelle folio i den relaterede forsendelse. |
| Modtag varer i transit | Modtag alle ordrelinjer, der er i transit, i folioen. |
| Dokumenter modtaget | Opdater indstillingen af **Dokumenter, der er modtaget** til *Ja*. Du kan bruge denne knap til at låse varen og/eller indkøbslinjen, så den ikke kan opdateres yderligere. |
| Søg efter automatiske omkostninger | Find relevante fragtomkostninger. Hvis disse omkostninger allerede er fundet eller opdateret, får du følgende meddelelse: "Der findes ikke-fakturerede omkostningslinjer. Vil du overskrive dem?" Bemærk, at fragtomkostninger, der er knyttet til folioen og er faktureret, ikke bliver overskrevet. |
| Opret modtagelseskladde | Generer en modtagelseskladde for organisationer ved hjælp af avancerede lagerstedsfunktioner. Du kan vælge **Initialiser antal** (anbefales), **Opret fra varer i transit** og/eller **Opret fra indkøbsordrer**. Den sidste indstilling afhænger af, om der bruges behandling af varer undervejs. |
| Periodiser omkostninger | Periodiser omkostninger, når en omkostningstype har en finanskonto angivet til debet. Denne knap bruges typisk, når lageret er i transit, eller når der er modtaget og faktureret varer. |

### <a name="buttons-on-the-general-tab"></a>Knapper under fanen Generelt

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Generelt**.

| Knap | Beskrivelse |
|---|---|
| Tilgangsliste | Bogfør en tilgangsliste for alle indkøbsordrelinjer i folioen. Hvis der bruges fragter for flere virksomheder, åbnes en dialogboks til bogføring af en ny tilgangsliste for hvert firma. |
| Produktkvittering | Se produktkvitteringsposten, hvis den bruges. |
| Varemodtagelse | Se varemodtagelseskladden, hvis den bruges. |
| Omkostningsforespørgsel | Åbn forespørgselssiden for omkostninger for at få vist alle omkostningerne for en fragt, herunder forsendelsescontaineren, folioen og indkøbsordren. Du kan justere den nøjagtige visning af siden ved hjælp af handlingen Vis. På forespørgselssiden med omkostninger kan du få vist et hvilket som helst område samt koden for varen og omkostningstypen. Hvis du fjerner disse varer, kan du justere siden ved at gruppere omkostninger. Denne egenskab kan være nyttig, hvis du bruger størrelser og farver. Du kan ændre de dimensioner, der vises på siden. På siden **Omkostninger** vises kun omkostningstypekoder, hvor posten **Dr** under fanen **Bogføring** er angivet til *Vare*. |

## <a name="header-view"></a>Overskriftsvisning

Hvis du vil åbne **Overskrift**-visningen, skal du åbne en folio og derefter vælge fanen **Overskrift** i øverste højre hjørne af foliooverskriften.

### <a name="settings-on-the-general-fasttab"></a>Indstillinger i oversigtspanelet Generelt

Følgende tabel beskriver de felter, der er tilgængelige i oversigtspanelet **Generelt** i visningen **Overskrift** af en folio.

| Felt | Beskrivelse |
|---|---|
| Folio | Navnet på folioen. Dette navn genereres automatisk, når folioen oprettes.|
| Fragt | Den fragt, som folioen er tilknyttet. |
| Toldmægler | Vælg toldmægleren for folioen. Toldmæglere defineres på leverandøren. De gør det muligt at oprette omkostninger automatisk. |
| Speditørluftfragtbrev/fragtseddel | Angiv det fragtbrev eller den fragtseddel, der gælder for folioen. |
| Firma | Den juridiske enhed (firma), der er tilknyttet folioen. |
| Kontrolnummer for last | Dette felt bruges af toldafdelinger i nogle lande eller områder. |
| Mål | Dette felt giver mulighed for at angive et mål i modulet **Landingsomkostninger**. Mål bruges ofte af organisationer, der ikke kender varernes individuelle volumen eller vægt, men som kræver en mere præcis fordeling, end beløb eller antal tillader. Speditøren leverer vægten eller kubikmålet, og du kan placere den på enten vareniveau eller indkøbsordreniveau. Den kan opdateres automatisk, hvis parameteren er valgt eller angivet manuelt. |
| Måleenhed | Den enhed, der gælder for det angivne mål. |
| Antal kartoner | Antallet af kartoner i folioen. Dette felt kan opdateres automatisk, afhængigt af den valgte parameter. |
| Kreditorkonto | Vælg den leverandør, der er tilknyttet folioen. Dette felt er udelukkende til orientering. Den påvirker ingen funktionalitet. |
| Navn | Navnet på den valgte leverandørkonto. |
| Kommentarer | Angiv eventuelle yderligere oplysninger vedrørende folioen. |
| Beskrivelse af varer | Vælg en varebeskrivelse, der kan hjælpe dig med at identificere folioen. Du kan finde flere oplysninger i [Beskrivelse af varer](shipping-information-setup.md#description-of-goods). |
| Værdiansættelsesdato | Dette felt er relateret til siden for afgiftsregistrering. I modulet **Landingsomkostninger** anvendes toldens valutakurs for den dato, du angiver her. Standardværdien er datoen på afgiftsindtastningssiden. |
| Told-id | Angiv told-id'et. Toldafdelingerne i lande eller områder leverer dette id. |
| Tarifkode | Angiv en tarifkode, der skal knyttes til folioen. Denne kode skal normalt angives (og defineres) af det land eller område, som du sender til. |

### <a name="settings-on-the-delivery-fasttab"></a>Indstillinger i oversigtspanelet Levering

Følgende tabel beskriver de indstillinger, der er tilgængelige i oversigtspanelet **Levering** i visningen **Overskrift** af en folio.

| Felt | Beskrivelse |
|---|---|
| Databasedato | Vælg en dato, der skal knyttes til folioen. Standardværdien er fragtens oprettelsesdato. |
| ETA på forsendelseshavn | Forventet modtagelsestidspunkt (ETA) på destinationshavnen ("til"-havnen). |
| Forventet leveringsdato | Normalt er det den dato, hvor varerne skal ankomme til lagerstedet. Dette felt bruges ikke, når den forventede leveringsdato er beregnet. (Den forventede leveringsdato for sporingskontrollen bruges i stedet). Hvis du vil angive dette felt, så værdien svarer til den forventede leveringsdato for sporingskontrollen, skal du bruge [sporingskontrolcenteret](delivery-information-setup.md#tracking-control-center). |
| Originaldokumenter modtaget. | Den dato, hvor originaldokumenterne blev modtaget. |
| Mægler adviseret | Den dato, hvor mægleren blev adviseret. |
| Oprindelig fragtseddel er afsendt | Den dato, hvor den oprindelige fragtseddel blev sendt. |
| Frigivne varer | Den dato, hvor varerne blev frigivet. |
| Kundeaftale | Datoen for kundeaftalen. |
| Leveret på lagersted | Den dato, hvor varerne blev leveret til lagerstedet. |
| Bekræftelsesdato | Dato for bekræftelse. |
| Leveringsinstruktioner | Den dato, hvor leveringsinstruktionerne blev modtaget. |
| Fra havn | Den havn, som fragten afgår fra. |
| Til havn | Den havn, hvor fragten ankommer. Forsendelsescontaineren har muligvis en anden havn, da skibet kan stoppe ved flere havne. |

### <a name="settings-on-the-export-fasttab"></a>Indstillinger i oversigtspanelet Eksport

Følgende tabel beskriver de indstillinger, der er tilgængelige i oversigtspanelet **Eksport** i visningen **Overskrift** af en folio.

| Felt | Beskrivelse |
|---|---|
| Eksportør | Eksportøren kan gemmes i folioen. I international handel kan du sende en indkøbsordre til ét firma, men modtage varerne fra et andet firma. Sporing og dokumentation kræves af toldmyndighederne. Navnet og adressen på eksportøren kan gemmes her. |
| Navn | Navnet på den valgte eksportør. |

## <a name="lines-view"></a>Linjevisning

Hvis du vil åbne **Linjer**-visningen, skal du åbne en folio og derefter vælge fanen **Linjer** i øverste højre hjørne af foliooverskriften.

### <a name="information-on-the-folio-fasttab"></a>Oplysninger i oversigtspanelet Folio

I oversigtspanelet **Folio** i visningen **Linjer** vises oplysninger om folioen. De fleste af disse oplysninger vises også i visningen **Overskrift** som beskrevet tidligere i dette emne.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Oplysninger om knapper i oversigtspanelet Linjer

I oversigtspanelet **Linjer** i visningen **Linjer** har detaljer om hver hele eller delvise indkøbsordrelinje, der er medtaget i den aktuelle folio.

I følgende tabel forklares de knapper, der er tilgængelige på i visningen **Linjer** i oversigtspanelet **Linjer**.

| Knap | Beskrivelse |
|---|---|
| Fjern | Fjern den valgte indkøbsordrelinje fra fragten. |
| Lager \> Transaktioner | Se lagertransaktioner for den valgte indkøbsordrelinje. Bemærk, at hvis du bruger varer undervejs, vises den oprindelige ordre og ordrerne for varer undervejs også. |
| Lager \> Vis dimensioner | Åbn en dialogboks, hvor du kan vælge de lagerdimensioner, der skal vises for de transaktioner, du får vist. |
| Opdatér | Opdater oplysninger, der er relateret til linjebeløbet, vægten eller volumen for den valgte indkøbsordrelinje. |

### <a name="information-on-the-lines-details-fasttab"></a>Oplysninger i oversigtspanelet Linjer

I oversigtspanelet **Linjer** i visningen **Linjer** findes detaljer om den indkøbsordrelinje, der aktuelt er valgt i oversigtspanelet **Linjer**.
