---
title: Administrere forsendelsescontainere
description: Dette emne beskriver, hvordan du kan arbejde med forsendelsescontainere. Forsendelsescontainere bruges til at gruppere varer, der fysisk er grupperet samlet. De bruges også, hvis omkostningerne kun skal deles på tværs af disse varer, normalt fordi de er fysisk samlet.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ac88f8e3b8cf305a5bd247e7ed6b14b23ad85499
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686763"
---
# <a name="manage-shipping-containers"></a>Administrere forsendelsescontainere

[!include [banner](../../includes/banner.md)]

Forsendelsescontainere bruges til at gruppere varer, der fysisk er grupperet samlet. De bruges også, hvis omkostningerne kun skal deles på tværs af disse varer, normalt fordi de er fysisk samlet.

Hvis du vil se og behandle varer via siden forsendelsescontainere, skal du gå til **Landingsomkostninger \> Forsendelsescontainere \> Alle Forsendelsescontainere**. På siden **Alle forsendelsescontainere** vises en liste over alle tilgængelige forsendelsescontainere. Du kan oprette, slette og arbejde med forsendelsescontainere ved at bruge knapperne i handlingsruden. Vælg en forsendelsescontainer på listen for at få vist dens oplysninger på siden **Forsendelsescontainere**.

Den øverste del af siden med oplysninger om forsendelsescontainere viser oplysninger om forsendelsescontainere og efterkalkulation. I sektionen **Linjer** vises de folier, varer og indkøbsordrer eller flytteordrer, der er knyttet til containeren.

## <a name="action-pane"></a>Handlingsrude

Handlingsruden på siderne **Alle forsendelsescontainere** og **Forsendelsescontainere** indeholder knapper, der giver dig mulighed for at arbejde med en valgt forsendelsescontainer. Hver knap udfører en enkelt handling. Handlingsruden indeholder også faner, som hver isæt indeholder et sæt relaterede knapper. Medmindre andet er angivet, er alle de knapper og faner, der beskrives i følgende undersektioner, tilgængelige både i listevisningen (det vil sige på siden **Alle forsendelsescontainere**) og i den detaljerede visning (det vil sige på siden **Forsendelsescontainere**).

### <a name="buttons-on-the-manage-tab"></a>Knapper under fanen Administrer

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Administrer**.

| Knap | Beskrivelser |
|---|---|
| Bogfør tilgangsliste | Bogfør en tilgangsliste, eller få vist produktkvitteringslisterne for alle indkøbsordrelinjer i forsendelsescontaineren. Hvis der bruges forsendelser for flere virksomheder, åbnes en ny dialogboks til bogføring af tilgangslisten for hvert firma. |
| Bogfør produktkvittering | Bogfør en produktkvittering for alle indkøbsordrelinjer i forsendelsescontaineren. |
| Bogfør faktura | Bogfør en faktura for alle indkøbsordrelinjer i forsendelsescontaineren. Hvis der bruges forsendelser for flere virksomheder, åbnes en ny dialogboks til fakturabogføring for hvert firma. |
| Forsendelsesflytteordre | Bogfør en forsendelse af flytteordre for alle flytteordrelinjer i forsendelsescontaineren. Det er kun de linjer i forsendelsescontaineren, der er af typen flytteordre, der vises i dialogboksen. |
| Modtag flytteordre | Bogfør en modtagelse af flytteordre for alle flytteordrelinjer i forsendelsescontaineren. Modtagelsesdialogboksen er den korteste vej til modtagelse af varer i en forsendelsescontainer eller fragt, og den er en af tre tilgængelige valgmuligheder. Du kan også modtage via modtagelseskladder eller behandling på mobilenheder. |
| Opret modtagelseskladde | Du kan generere en modtagelseskladde for organisationer ved hjælp af avancerede lagerstedsfunktioner. Du kan vælge _Initialiser antal_ (anbefales) og enten _Opret fra varer i transit_ eller _Opret fra indkøbsordrer_. De to sidste indstillinger afhænger af, om der bruges behandling af varer undervejs. |
| Omdøb | Åbn en dialogboks, hvor du kan omdøbe en valgt forsendelsescontainer. |
| Skift rejseskabelon | Skift rejseskabelonen. Når du har ændret rejseskabelonen, skal du måske vælge **Find automatiske omkostninger** eller manuelt tilføje omkostninger igen, fordi forsendelsesomkostningerne slettes. |
| Konvertér til leje | Konverter en valgt forsendelsescontainer til en lejeforsendelsescontainer. |

### <a name="buttons-on-the-general-tab"></a>Knapper under fanen Generelt

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Generelt**.

| Knap | Beskrivelser |
|---|---|
| Tilgangsliste | Bogfør en tilgangsliste for alle indkøbsordrelinjer i forsendelsescontaineren. Hvis der bruges fragter for flere virksomheder, åbnes en dialogboks til bogføring af en ny tilgangsliste for hvert firma. |
| Produktkvittering | Se produktkvitteringsposten, hvis den bruges. Produktkvitteringsprocessen bruges kun, hvis varerne ikke bruger funktionerne for varer undervejs. |
| Varemodtagelse | Få vist varemodtagelseskladden for forsendelsescontaineren, hvis den pågældende kladde bruges. |
| Etaper | Etaper bruges til at identificere forskellige dele af en rejse. Leveringstiderne kan knyttes til de enkelte etaper som en hjælp ved forsendelsessporing. Yderligere oplysninger finder du i [Opsætning af rejse i flere etaper](multi-leg-journey-setup.md). |
| Sporing | Se eller opdater forsendelsessporing. |
| Ordrer i varer i transit | Du kan åbne siden **Varer undervejs** direkte fra containeren. Denne side viser poster for varer undervejs for den valgte forsendelsescontainer. |

## <a name="header-view"></a>Overskriftsvisning

Hvis du vil åbne **Overskrift**-visningen, skal du åbne en forsendelsescontainer og derefter vælge fanen **Overskrift** i øverste højre hjørne af forsendelsescontaineroverskriften.

### <a name="settings-on-the-general-fasttab"></a>Indstillinger i oversigtspanelet Generelt

Følgende tabel beskriver de indstillinger, der er tilgængelige i oversigtspanelet **Generelt** i visningen **Overskrift** af en forsendelsescontainer.

| Felt | Beskrivelse |
|---|---|
| Forsendelsescontainer | Navnet på forsendelsescontaineren. |
| Fragt | Den fragt, som er tilknyttet forsendelsescontaineren. |
| Forsendelsescontainertype | Angiv forsendelsescontainertypen. Dette felt skal angives. Du kan bruge den til at bestemme fragtomkostningerne ved f.eks. at vælge den automatiske omkostning, der er knyttet til forsendelsescontainertypen. |
| Fartøj | Angiv eller vælg fartøjet. Hvis fartøjet ikke er vist som en værdi, kan du angive fartøjets id'et som fritekst. I så fald opdateres hovedtabellen ikke, så fartøjets id kan vælges i dette felt senere. Yderligere oplysninger finder du i [Fartøjer](shipping-information-setup.md#vessels). |
| Enhedstype | Enhedstyper bruges som en yderligere måde at gruppere og identificere forsendelsescontainere på. De vises og vælges på siden forsendelsescontainer. Du kan finde flere oplysninger under [Konfigurere enhedstyper](shipping-container-setup.md#unit-types). |
| Afkølingstype | Afkølingstyper bruges som en yderligere måde at gruppere og identificere forsendelsescontainere på, normalt afkølede containere. De vises og vælges på siden forsendelsescontainer. Du kan finde flere oplysninger under [Konfigurere afkølingstyper](shipping-container-setup.md#refrigeration-types). |
| Mål | Dette felt giver mulighed for at angive et mål i modulet **Landingsomkostninger**. Mål bruges ofte af organisationer, der ikke kender varernes individuelle volumen eller vægt, men som kræver en mere præcis fordeling, end beløb eller antal tillader. Speditøren leverer vægten i kilogram eller kubikmålet, og du kan placere den på vareniveau eller indkøbsordreniveau. Den kan opdateres automatisk, hvis parameteren er valgt, eller angives manuelt. |
| Måleenhed | Den måleenhed, der gælder for antallet i feltet **Mål**. |
| Faktisk vægt | Du kan registrere den faktiske vægt af kartonen eller containeren. Denne værdi kan bruges til kontrol i forhold til den maksimumvægt, der er tilladt i opsætningen af en forsendelsescontainer. |
| Antal kartoner | Antallet af kartoner opdateres automatisk, hvis parameteren er valgt. |
| Beskrivelse af varer | Du kan vælge en beskrivelse af varerne i forsendelsescontainer- eller foliohovedet. Den bruges til at identificere en fragt, forsendelsescontainer eller folio af varer. Du kan finde flere oplysninger i [Beskrivelse af varer](shipping-information-setup.md#description-of-goods). |
| Speditørluftfragtbrev/fragtseddel | Du kan angive fragtbrev eller fragtseddel for forsendelsescontaineren. |
| Kommentarer | Yderligere oplysninger vedrørende forsendelsescontaineren. |
| Kan returneres | En værdi, der angiver, om forsendelsescontaineren kan returneres efter fragten. |
| Fragtstatus | Status for den rejse, der er tilknyttet forsendelsescontaineren. |
| Status for indkøbsordre | Status for den indkøbsordre, der er tilknyttet forsendelsescontaineren. |

### <a name="settings-on-the-delivery-fasttab"></a>Indstillinger i oversigtspanelet Levering

Følgende tabel beskriver de indstillinger, der er tilgængelige i oversigtspanelet **Levering** i visningen **Overskrift** af en forsendelsescontainer.

| Felt | Beskrivelse |
|---|---|
| Dato og klokkeslæt for oprettelse | Dato og klokkeslæt for oprettelse af containeren. |
| Dato for ab fabrik | Denne dato leveres normalt til fabrikken/leverandøren for at angive, hvornår du forventer, at varerne forlader disse steder. Når du arbejder med en fabrik i Asien, er denne dato ofte påkrævet i stedet for den dato, du forventer varerne. (Modsat er det den dato, hvor du forventer, at varerne skal leveres, ved en lokal levering). Dette felt kan udfyldes fra indkøbsordrelinjerne på listen over forsendelsescontainere. Du kan også angive den manuelt her. |
| Afsendelsesdato | Denne dato kan udskrives på indkøbsordredokumentet. Det informerer normalt fabrikken/leverandøren om den dato, hvor varerne skal være leveret til havnen. Dette felt er udelukkende til orientering. Den bruges ikke til at beregne den forventede leveringsdato for varerne i forsendelsescontaineren. Dette felt kan angives, så det opdateres automatisk, når sporingskontrolsiden opdateres. |
| Dato for indgang på lager | Den tidligste dato, hvor varerne fra de indkøbsordrer, som er tilknyttet fragten, vil være tilgængelige for salg.|
| Forventet leveringsdato | Normalt er det den dato, hvor varerne skal ankomme til lagerstedet. Dette felt er udelukkende til orientering. Den bruges ikke til at beregne varedisponering på indkøbsordrelinjerne i forsendelsescontaineren. Den forventede leveringsdato på indkøbsordrelinjerne opdateres via sporingsstyring. Dette felt kan konfigureres, så det opdateres automatisk, når sporingskontrolsiden opdateres. |
| Afrejsedato | Normalt er det den dato, hvor flyet eller fartøjet rent faktisk forlader den oversøiske havn. |
| ETA på forsendelseshavn | Forventet modtagelsesdato på destinationshavnen ("til"-havnen). |
| Originaldokumenter modtaget. | Valgfrit: Opdater den dato, hvor originaldokumenterne blev modtaget. |
| Mægler adviseret | Valgfrit: Opdater den dato, hvor mægleren blev adviseret. |
| Oprindelig fragtseddel sendt | Valgfrit: Opdater den dato, hvor den oprindelige fragtseddel blev sendt. |
| Frigivne varer | Valgfrit: Opdater den dato, hvor varerne blev frigivet. |
| Kundeaftale | Valgfrit: Opdater datoen for kundeaftalen. |
| Leveret på lagersted | Valgfrit: Opdater den dato, hvor varerne blev leveret til lagerstedet. |
| Bekræftelsesdato | Valgfrit: Opdater bekræftelsesdatoen. |
| Leveringsinstruktioner | Valgfrit: Opdater datoen for leveringsinstruktionerne. |
| Fra havn | Den havn, som varerne vil blive afsendt fra. |
| Til havn | Den havn, som varerne vil blive afsendt til. |
| Lokal speditør | Dette felt er udelukkende til orientering. Den lokale speditør skal kunne vælges i leverandørtabellen. |
| Dato for lokal transport | Angiv den dato, som den lokale transport er bestilt til. Feltet kan være en hjælp ved planlægning på lagerstedet. |
| Klokkeslæt for lokal transport | Indtast tidsintervallet. Feltet kan være en hjælp ved planlægning på lagerstedet. |
| Rejseskabelon | Den rejseskabelon, der er angivet for fragten. Rejseskabelonen indeholder detaljer om "til"- og "fra"-havne samt de leveringstider, der er knyttet til sporingskontrollen for forsendelsescontaineren. |

### <a name="settings-on-the-other-fasttab"></a>Indstillinger i oversigtspanelet Andet

Følgende tabel beskriver de indstillinger, der er tilgængelige i oversigtspanelet **Andet** i visningen **Overskrift** af en forsendelsescontainer.

| Felt | Beskrivelse |
|---|---|
| Udlejning | En værdi, der angiver, om forsendelsescontaineren er en lejeforsendelsescontainer. Lejeomkostninger kan være tilknyttet lejecontainere. |
| Omregnet til leje | En værdi, der angiver, om forsendelsescontaineren er konverteret til en lejeforsendelsescontainer. Lejeomkostninger kan være tilknyttet lejecontainere. |
| Oprindelig fragtrute | Hvis forsendelsescontaineren blev flyttet til en ny fragt, er det den oprindelige fragt. |
| Brugt | Du kan bruge denne til at registrere, om der er brugt en lejeforsendelsescontainer. Den er udelukkende til orientering. |
| Forventet lastningsdato | Den dato, hvor forsendelsescontaineren forventes at blive lastet med varer. |
| Vores serienummer | Angiv det serienummer, som dit firma bruger internt til forsendelsescontaineren. |
| Fragtfirmas serienummer | Angiv det serienummer, som fragtfirmaet eller agenten har angivet for forsendelsescontaineren. |
| Anvendelsesdato for undersøgelsescertifikat | Den dato, hvor der blev anmodet om en undersøgelse af forsendelsescontaineren. |
| Modtagelsesdato for undersøgelsescertifikat | Den dato, hvor undersøgelsescertifikatet blev modtaget. |
| Udløbsdato for undersøgelsescertifikat | Den dato, hvor undersøgelsescertifikatet udløber. |
| Undersøgelsescertifikatnummer | Certifikatnummeret for det certifikat, der blev udstedt efter en undersøgelse. |

## <a name="lines-view"></a>Linjevisning

Hvis du vil åbne **Linjer**-visningen, skal du åbne en forsendelsescontainer og derefter vælge fanen **Linjer** i øverste højre hjørne af forsendelsescontaineroverskriften.

### <a name="information-on-the-shipping-container-fasttab"></a>Oplysninger i oversigtspanelet Forsendelsescontainer

I oversigtspanelet **Forsendelsescontainer** i visningen **Linjer** vises oplysninger om forsendelsescontaineren. De fleste af disse oplysninger vises også i visningen **Overskrift** som beskrevet tidligere i dette emne.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Oplysninger om knapper i oversigtspanelet Linjer

I oversigtspanelet **Linjer** i visningen **Linjer** har detaljer om hver hele eller delvise indkøbsordrelinje, der er medtaget i den aktuelle forsendelsescontainer.

I følgende tabel forklares de knapper, der er tilgængelige på i visningen **Linjer** i oversigtspanelet **Linjer**.

| Knap | Beskrivelse |
|---|---|
| Fjern | Fjern den valgte indkøbsordrelinje fra fragten. |
| Lager \> Transaktioner | Se lagertransaktioner for den valgte indkøbsordrelinje. Bemærk, at hvis du bruger varer undervejs, vises den oprindelige ordre og ordrerne for varer undervejs også. |
| Lager \> Vis dimensioner | Åbn en dialogboks, hvor du kan vælge de lagerdimensioner, der skal vises for de transaktioner, du får vist. |
| Opdatér | Opdater oplysninger, der er relateret til linjebeløbet, vægten eller volumen for den valgte indkøbsordrelinje. |

### <a name="information-on-the-lines-details-fasttab"></a>Oplysninger i oversigtspanelet Linjer

I oversigtspanelet **Linjer** i visningen **Linjer** findes detaljer om den indkøbsordrelinje, der aktuelt er valgt i oversigtspanelet **Linjer**.
