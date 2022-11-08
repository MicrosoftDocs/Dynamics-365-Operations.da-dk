---
title: Administrere fragter
description: Denne artikel beskriver, hvordan du kan arbejde med fragter. En fragt repræsenterer typisk et fartøj. Afhængigt af dine fremgangsmåder og procedurer kan den dog repræsentere en leverandør, en indkøbsordre eller et andet element, der kan give mening for din organisation.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4499eeb9cdd4efd9c4b630106c6e052378191f2a
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725463"
---
# <a name="manage-voyages"></a>Administrere fragter

[!include [banner](../../includes/banner.md)]

En fragt repræsenterer typisk et fartøj. Afhængigt af dine fremgangsmåder og procedurer kan den dog repræsentere en leverandør, en indkøbsordre eller et andet element, der kan give mening for din organisation.

Siden **Alle fragter** indeholder oplysninger om fragt, levering og efterkalkulation samt oplysninger om varer, indkøbsordrer og flytteordrer. Du kan åbne siden **Alle fragter** ved at gå til **Landingsomkostninger \> Fragter \> Alle fragter**. På denne side vises en liste over alle aktuelle fragter. Du kan oprette, slette og arbejde med fragter ved at bruge knapperne i handlingsruden. Vælg en fragt på listen for at få vist detaljerne.

> [!NOTE]
> Forsendelsescontainere og folioer er kædet sammen med en fragt. Indkøbslinjer er knyttet til en forsendelsescontainer. Derudover er de omkostninger, der angives her, fordelt på alle tilknyttede indkøbslinjer.
> Projektindkøbsordre understøttes ikke i Landingsomkostninger.

## <a name="action-pane"></a>Handlingsrude

Handlingsruden på siden **Fragter** indeholder knapper, der giver dig mulighed for at arbejde med en valgt fragt. Hver knap udfører en enkelt handling. Handlingsruden indeholder også faner, som hver isæt indeholder et sæt relaterede knapper. Hvis intet andet er angivet, er alle knapper og faner tilgængelige både i listevisningen på siden **Alle fragter** og i den detaljerede visning af en enkelt valgt fragt.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knapper, der vises direkte i handlingsruden

I følgende tabel beskrives de knapper, der er direkte tilgængelige i handlingsruden.

| Knap | Beskrivelse |
|---|---|
| Nye | Opret en fragt. <!-- KFM: Link to scenario --> |
| Delete | Slet den aktuelle fragt. Det er kun fragter, der har statussen *Bekræftet*, som kan slettes. Når en fragt forlader havnen og behandler varer undervejs, kan den ikke længere slettes. |
| Fragteditor | Åbn siden **Fragteditor**, hvor du kan tilføje eller fjerne indkøbslinjer for fragten, oprette nye containere og redigere detaljer for selve fragten. |
| Ruteomkostninger | Åbn siden **Fragtomkostninger**, hvor du kan se og føje fragtomkostninger til alle varerne i fragten. Når fragtomkostninger føjes til fragten manuelt, føjes de automatisk til siden **Omkostningsforespørgsel** og fordeles på alle varer i overensstemmelse med den metode, der er angivet på siden **Fragtomkostninger**. |

### <a name="buttons-on-the-voyage-tab"></a>Knapper under fanen Fragt

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Fragt**. Denne fane er kun tilgængelig, når du arbejder i listevisningen på siden **Alle fragter**.

| Knap | Beskrivelse |
|---|---|
| Forsendelsescontainer | Åbn en side, der viser alle de forsendelsesbeholdere, der er tilknyttet den valgte fragt. Der kan være én container eller mange containere. |
| Folio | Åbn en side, der viser alle de folioer, der er tilknyttet den valgte fragt. Der kan være én folio eller mange folioer. |

### <a name="buttons-on-the-manage-tab"></a>Knapper under fanen Administrer

I følgende tabel beskrives de handlinger, der er tilgængelige i handlingsruden under fanen **Administrer**.

| Knap | Beskrivelse |
|---|---|
| Dokumenter modtaget | Opdater fragten, så **Dokumenter, der er modtaget** er indstillet til *Ja*. Du kan bruge denne knap til at låse varen og/eller indkøbslinjen, så den ikke kan opdateres yderligere. |
| I transit | Opdater feltet **Fragtstatus** til den status for transit, der er oprettet på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)**. Der er ingen yderligere logik i denne proces. En fragt kan også opdateres automatisk til transitstatus på basis af indstillingerne i [Sporingskontrolcenteret](delivery-information-setup.md).
| Klar til efterkalkulation | Opdater feltet **Fragtstatus** til Klar til efterkalkulation-status, der er oprettet på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)**. Det er muligt at efterkalkulere en fragt, når alle fakturaerne er behandlet (både lagerfakturaer og fragtomkostningsfakturaer), og varerne er modtaget. Hvis de forkalkulerede omkostninger, der er tilknyttet en fragt, ikke er blevet efterkalkuleret, opstår der en fejl, når du forsøger at behandle efterkalkulering af en fragt. |
| Efterkalkuleret | Ryd op i eventuelle uregelmæssigheder i efterkalkulation, efter at der findes en faktura for alle indkøbsordrer og fragtomkostninger. Når du vælger denne knap, vises dialogboksen **Fragtopdatering - Efterkalkuleret**. Her kan du vælge at bogføre på den økonomiske standarddato eller angive en bogføringsdato og derefter køre handlingen. Du kan køre handlingen lige så mange gange, som du vil. Du kan også bruge dialogboksen **Fragtopdatering - Efterkalkuleret** til at oprette en tidsplan for kørsel af handlingen som en periodisk opgave (batchjob). Det anbefales, at handlingen køres regelmæssigt ved at konfigurere den som et batchjob. |
| Bogfør tilgangsliste | Bogfør en tilgangsliste for alle indkøbsordrelinjer i fragten.  |
| Bogfør produktkvittering | Bogfør en produktkvittering for alle indkøbsordrelinjer i fragten. Produktkvitteringsprocessen for de indkøbsordrelinjer, der er tilknyttet en fragt, bruges kun, hvis varerne **ikke** gennemgår behandling af varer undervejs. Hvis varerne skal gennemgå behandlingen af varer undervejs, modtager du en fejl, når du forsøger at bogføre produktkvitteringen for en indkøbsordrelinje.  |
| Bogfør faktura | Bogfør en faktura for alle indkøbsordrelinjer i fragten. Hvis varerne i fragtsen gennemgår behandlingen af varer undervejs, faktureres indkøbsordrelinjerne, før modtagelsesprocessen er udført. Når den oprindelige indkøbsordre faktureres, oprettes de varer undervejs, som er knyttet til de oprindelige indkøbsordrelinjer. Disse ordrer kan derefter modtages af lagerstedet.  |
| Forsendelsesflytteordre | Bogfør en fragt af flytteordre for alle flytteordrelinjer i fragten. Når denne knap er valgt, er det kun flytteordrer, der kan opdateres. |
| Modtag flytteordre | Bogfør en flytteordrekvittering for alle flytteordrelinjer i fragten. |
| Modtag varer i transit | Modtag alle ordrelinjer, der er i transit, i fragten. Denne knap er en af de tre muligheder, der er tilgængelige for modtagelse af varer i transit i en fragt. (De to øvrige indstillinger er Knappen **Opret modtagelseskladde**, som beskrives senere i denne tabel, og mobilappen Lokationsstyring). Denne indstilling er den simpleste, og den bruges til at behandle varerne i transit ud fra lagerstedet for varer i transit og til det endelige destinationslagersted. Hvis du vil have mere kontrol over processen, skal du bruge modtagelseskladden eller en mobilenhed til at behandle varemodtagelsen. |
| Søg efter automatiske omkostninger | Find alle relevante fragtomkostninger. Hvis disse omkostninger allerede er fundet eller opdateret, får du følgende meddelelse: "Der findes ikke-fakturerede omkostningslinjer. Vil du overskrive dem?" Eventuelle omkostninger, som ikke er tilknyttet fragten på oprettelsestidspunktet, findes. Fragtomkostninger, der er knyttet til en fragt og er faktureret, bliver ikke overskrevet. |
| Opret modtagelseskladde | <p>Åbn dialogboksen **Opret modtagelseskladde**, hvor du kan oprette en modtagelseskladde, der angiver en lokation. Dialogboksen indeholder følgende indstillinger:</p><ul><li>**Opret fra varer i transit**, eller **Opret fra flytteordre** –Navnet på denne indstilling ændres, afhængigt af om du bruger varer i transit. Angiv den til *Ja*, hvis du vil åbne en modtagelseskladdeside, hvor du kan behandle en standardmodtagelseskladde for de varer i transit, der er tilknyttet fragten. Hvis varen allerede er modtaget på det endelige destinationslagersted, føjes den ikke til modtagelseskladdelinjerne.</li><li>**Initialiser antal** – Angiv denne indstilling til *Ja* for at initialisere det antal, der vil blive modtaget, baseret på antallet af varer, der er angivet på fragtlinjen. Hvis fragtlinjen er delvist modtaget, vil dette antal være restantallet. Det anbefales, at du angiver denne indstilling til *Ja*.</li><li>**Opret fra ordrelinjer** – Angiv denne indstilling til *Ja* for at tage værdien fra ordrelinjerne.</li></ul><p>Denne knap er en af de tre muligheder, der er tilgængelige for modtagelse af varer i en fragt. (De øvrige indstillinger er knappen **Modtag varer i transit**, som er beskrevet tidligere i denne tabel, og mobilappen Lokationsstyring).</p> |
| Periodiser omkostninger | Du kan periodisere omkostninger, når en omkostningstype har en finanskonto angivet til debet. Denne knap bruges typisk, når lageret er i transit, eller når der er modtaget og faktureret varer. |
| Aggreger omkostninger | Flyt omkostninger fra forsendelsescontainerniveauet til fragtniveauet. Du kan bruge denne knap i et scenario med delte tjenester/forsendelse, hvor flere enheder deler en forsendelsescontainer eller en kartonplads. Fragten har f.eks. en forsendelsescontainer på 40 meter og en forsendelsescontainer på 20 meter, og fordeling sker efter volumen. I dette tilfælde kan de varer/enheder, der deler eller bruger plads i forsendelsescontaineren på 20 meter, blive ændret. For at fordele omkostningerne ligeligt kan det være en fordel for nogle organisationer at overføre omkostningerne til fragten og fordele dem på basis af fordelingsmetoden på fragtniveau. |
| Skift rejseskabelon | Åbn en dialogboks, hvor du kan ændre rejseskabelonen. Når du har ændret skabelonen, slettes fragtomkostningerne. Du skal derfor muligvis vælge **Find automatiske omkostninger** (se beskrivelsen tidligere i denne tabel) eller manuelt tilføje omkostninger igen. |

### <a name="buttons-on-the-general-tab"></a>Knapper under fanen Generelt

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden under fanen **Generelt**.

| Knap | Beskrivelse |
|---|---|
| Tilgangsliste | Åbn en liste over produktkvitteringer for alle indkøbsordrelinjer i fragten.  Hvis der ikke er behandlet nogen produktkvitteringslister, er denne knap ikke tilgængelig. |
| Produktkvittering | Åbn produktkvitteringsposten for de indkøbsordrelinjer, der er tilknyttet fragten, hvis den pågældende post bruges. Hvis der ikke er bogført nogen produktkvitteringer, er denne knap ikke tilgængelig. Produktkvitteringsprocessen bruges ikke, hvis du bruger behandling af varer undervejs. |
| Varemodtagelse | Åbn varemodtagelseskladden, hvis den bruges. |
| Sporing | Åbn siden **Indgående sporing**, hvor du kan opdatere den forventede modtagelsesdato for varer i en forsendelsescontainer og en fragt og efterfølgende opdatere de forventede leveringsdatoer for indkøbsordrelinjer. |
| Omkostningsforespørgsel | <p>Åbn siden **Omkostningsforespørgsel**, som viser alle omkostningerne for en fragt.</p><p>Vælg **Vis** i handlingsruden for at justere visningen. Du kan få vist alle niveauer plus koden for varen og omkostningstypen.</p><p>Det er kun koder for omkostningstyper, som er direkte relateret til lagertransaktioner, der vises på siden **Omkostningsforespørgsel**. Hvis du fjerner omkostningstypekoder, kan du justere siden ved at gruppere omkostninger. Denne egenskab kan være nyttig, hvis du bruger størrelser og farver.</p><p>På siden **Omkostningsforespørgsel** vises kun omkostningstypekoder, hvor feltet **Debet** er angivet til *Vare*.</p> |
| Ordrer i varer i transit | Åbn siden **Ordrer for varer undervejs**, som kun viser posterne for varer undervejs for den valgte fragt. |

## <a name="lines-view"></a>Linjevisning

Hvis du vil åbne **Linjer**-visningen, skal du åbne en fragt og derefter vælge fanen **Linjer** i øverste højre hjørne af fragtoverskriften.

### <a name="information-on-the-voyage-header-fasttab"></a>Oplysninger i oversigtspanelet Fragtoverskrift

Oversigtspanelet **Fragtoverskrift** i visningen **Linjer** for en fragt indeholder grundlæggende oplysninger, der beskriver fragten. Mange af de felter, der vises i dette oversigtspanel, vises også i **Overskrift**-visningen, som det beskrives senere i denne artikel.

### <a name="information-on-the-voyage-lines-fasttab"></a>Oplysninger i oversigtspanelet Fragtlinjer

Oversigtspanelet **Fragtlinjer** i visningen **Linjer** for en fragt er relateret til de fragtdetaljer og efterkalkulationsoplysninger, der gælder på fragtniveau. Her kan du gennemse forsendelsescontainere, folioer og varer, der er tilknyttet fragten. Prisen og antallet af varerne i fragten vises også. Du kan se en hvilken som helst forsendelsescontainer eller folio på listen ved at vælge det relevante link.

### <a name="information-on-the-line-details-fasttab"></a>Oplysninger i oversigtspanelet Linjedetaljer

I oversigtspanelet **Linjdetaljer** i visningen **Linjer** af en fragt findes detaljer om den linje, der aktuelt er valgt i oversigtspanelet **Fragtlinjer**. Bemærk, at dette oversigtspanel indeholder oplysninger om den position, som hver linje indtager i containeren, og dens indberettede antal.

## <a name="header-view"></a>Overskriftsvisning

Hvis du vil åbne **Overskrift**-visningen, skal du åbne en fragt og derefter vælge fanen **Overskrift** i øverste højre hjørne af fragtoverskriften.

### <a name="settings-on-the-general-fasttab"></a>Indstillinger i oversigtspanelet Generelt

Følgende tabel beskriver de felter, der er tilgængelige i oversigtspanelet **Generelt** i visningen **Overskrift** af en fragt.

| Felt | Beskrivelse |
|---|---|
| Fragt | Angiv fragt- eller flynummeret. |
| Reservationsreference | Hvis afsenderen eller forsendelsescenteret angiver et referencenummer, der identificerer fragten (dvs. afsenderens eller forsendelsescenterets interne reference), skal du angive det her. |
| Fartøj | Angiv eller vælg fartøjet. Hvis fartøjet ikke er vist som en værdi, kan du angive fartøjets id'et som fritekst. I så fald opdateres hovedtabellen ikke, så fartøjets id kan vælges i dette felt senere. |
| Eksternt fragt-id | Angiv det offentligt tilgængelige id for fragten (f.eks. flynummeret). |
| Masterluftfragtbrev/fragtseddel | Angiv masterluftfragtbrevet eller fragtseddelnummeret. Du kan angive denne værdi, når du leverer med fly. |
| Speditørluftfragtbrev/fragtseddel | Angiv fragtbrev eller fragtseddel for forsendelsescontaineren. |
| Udlejning | Markér dette afkrydsningsfelt for at angive, at containeren er en lejecontainer, der skal returneres. |
| Beskrivelse | Angiv en beskrivelse af fragten, der gør det lettere at genkende den. |
| Fragtstatus | Status for fragten. Værdierne omfatter *Oprettet*, *I transit*, *Dokumenter, der er modtaget* og *Efterkalkuleret*. Dette felt beregnes ikke ud fra logik. Det opdateres kun via bogføringshandlingen. Værdien *Efterkalkuleret* angiver, at der er modtaget en faktura for lageret og alle fragtomkostninger. Medmindre der modtages en faktura, kan fragtstatussen ikke være *Efterkalkuleret*. |
| Status for indkøbsordre | Den højeste status, der er nået blandt alle de indkøbsordrer, der er tilknyttet fragten. |
| Dokumenter modtaget | En værdi, der angiver, om dit firma har modtaget alle de dokumenter, der er tilknyttet fragten. Hvis du vil ændre værdien, skal du vælge **Dokumenter, der er modtaget** i gruppen **Fragtopdatering** under fanen **Administrer** i handlingsruden. |
| Fragtfirma | Vælg fragtfirmaet for denne fragt. Dette felt kan bruges til at bestemme automatiske omkostninger. |
| Navn | Navnet på det firma, der er valgt i feltet **Fragtfirma**. |
| Mål | Dette felt giver mulighed for at angive et mål i en automatisk omkostning. Mål bruges ofte af organisationer, der ikke kender varernes individuelle volumen eller vægt, men som kræver en mere præcis fordeling, end beløb eller antal tillader. Speditøren leverer vægten eller kubikmålet, og du kan placere den på enten vareniveau eller indkøbsordreniveau. Den kan opdateres automatisk, hvis parameteren er valgt, eller angives manuelt. |
| Måleenhed | Den måleenhed, der gælder for antallet i feltet **Mål**. |
| Antal paller | Angiv antallet af paller på fragtlinjen. Dette felt opdateres automatisk, hvis indstillingen **Automatisk opdatering af antal kartoner** er angivet til *Ja* under fanen **Generelt** på siden **Parametre for landingsomkostninger**. |

### <a name="settings-on-the-delivery-fasttab"></a>Indstillinger i oversigtspanelet Levering

Følgende tabel beskriver de felter, der er tilgængelige i oversigtspanelet **Levering** i visningen **Overskrift** af en fragt.

| Felt | Beskrivelse |
|---|---|
| Dato og klokkeslæt for oprettelse | Dato og klokkeslæt for fragtpostens oprettelse. |
| Dato for ab fabrik | I dette felt vælges den tidligste dato for ab fabrik blandt de indkøbsordrer, der er knyttet til fragten. Datoen for ab fabrik er tilgængelig i indkøbsordrehovedet og opdateres ved hjælp af sporingskontrolfunktionen. |
| Afsendelsesdato | Den estimerede dato, hvor flyet eller fartøjet forlader oprindelsesstedet. |
| Afrejsedato | Afrejsedatoen er normalt den dato, hvor flyet eller fartøjet rent faktisk forlader den oversøiske havn. Afrejsedatoen og afsendelsesdatoen behøver ikke at være ens. Feltet **Afrejsedato** er udelukkende til orientering. Det bruges ikke til at beregne den forventede leveringsdato. Funktionen til sporingskontrol bruges til at estimere den forventede leveringsdato, og dette felt kan konfigureres, så det automatisk udfyldes med funktionen til sporingskontrol. |
| Dato for indgang på lager | Dette felt vælger den tidligste dato, hvor varerne fra de indkøbsordrer, som er tilknyttet fragten, vil være tilgængelige for salg. |
| Forventet leveringsdato | Den forventede leveringsdato er normalt den dato, hvor varerne skal ankomme til lagerstedet. Dette felt er udelukkende til orientering. Det bruges ikke til varedisponering. Den forventede leveringsdato på indkøbsordrelinjen bruges til varedisponering af varer til en fragt og opdateres ved hjælp af funktionen til sporingskontrol. Dette felt kan konfigureres, så det udfyldes af sporingskontrollen. |
| Faktisk leveringsdato | Den tidligste leveringsdato, der er baseret på de varer, der er tilknyttet fragten. |
| ETA på forsendelseshavn | Angiv den dato, hvor du forventer, at fragten ankommer til forsendelseshavnen, på baggrund af de oplysninger, som fragtfirmaet har afgivet. |
| Originaldokumenter modtaget. | Angiv den dato, hvor originaldokumenterne blev modtaget. |
| Mægler adviseret | Angiv den dato, hvor mægleren blev adviseret. |
| Oprindelig fragtseddel sendt | Angiv den dato, hvor den oprindelige fragtseddel blev sendt. |
| Frigivne varer | Angiv den dato, hvor varerne blev frigivet fra tolden. |
| Kundeaftale | Angiv kundeaftaledatoen, som er den dato, hvor du forventer, at kunden bliver ejer af varerne. |
| Leveret på lagersted | Angiv den dato, hvor varerne blev leveret til lagerstedet. |
| Bekræftelsesdato | Angiv bekræftelsesdatoen. |
| Leveringsinstruktioner | Angiv den dato, hvor leveringsinstruktionerne blev modtaget. |
| Leveringsmåde | Dette felt indeholder oplysninger om den metode, der bruges til levering af fragten og omkostningsvalg af automatiske omkostninger, der er knyttet til den pågældende leveringsmetode. |
| Fra havn | Den afsendelseshavn, som fragten afgår fra. |
| Til havn | Den havn, hvor fragten ankommer. Forsendelsescontainere kan have forskellige havne, da skibet kan stoppe ved flere havne. Ved at bekræfte "til"-havnen på forsendelsescontainerniveau giver du nøjagtige havneoplysninger for hver forsendelsescontainer på en fragt. Den automatiske omkostning, der er tilknyttet fragten, bestemmes på baggrund af kombinationen af containertypen for forsendelsen, "Til"-havnen og "fra"-havnen. |
| Lokal speditør | Dette felt er udelukkende til orientering. Den lokale speditør skal kunne vælges i leverandørtabellen. |
| Dato for lokal transport | Den dato, som den lokale transport er bestilt til. Feltet kan være en hjælp ved planlægning på lagerstedet. |
| Klokkeslæt for lokal transport | Det tidsinterval, som den lokale transport er bestilt til. Feltet kan være en hjælp ved planlægning på lagerstedet. |
| Ruteskabelon | Den rejseskabelon, der er angivet for fragten. Rejseskabelonen bruges til at angive "til"-havnen og "fra"-havnen for forsendelsescontaineren og fragten. Disse værdier er til gengæld en hjælp til at identificere de automatiske omkostninger, der er tilknyttet fragten. |

### <a name="settings-on-the-other-fasttab"></a>Indstillinger i oversigtspanelet Andet

Følgende tabel beskriver de felter, der er tilgængelige i oversigtspanelet **Andet** i visningen **Overskrift** af en fragt.

| Felt | Beskrivelse |
|---|---|
| Kommentarer | Angiv eventuelle yderligere oplysninger vedrørende fragten. |
| Værdiansættelsesdato | Vælg den tidligste dato for ab fabrik til de indkøbsordrer, der er knyttet til fragten. |
| Ventende fragt | Du kan bruge dette til at angive, om forsendelsen eller fragten er afgået. Den er udelukkende til orientering.  |
| Omdøbe forsendelsescontainere | Antallet af containere, der endnu ikke er modtaget, for fragt, der har mere end én container. |

## <a name="voyage-update-periodic-tasks"></a>Periodiske opgaver for fragtopdatering

Modulet **Landingsomkostninger** omfatter flere fragtrelaterede periodiske opgaver, der kan masseopdatere flere aspekter af fragt. Hvis du vil køre eller planlægge disse periodiske opgaver, skal du gå til **Landingsomkostninger \> Periodiske opgaver \> Fragtopdateringer** og derefter vælge en af følgende opgavetyper:

- **Dokumenter, der er modtaget** – Med denne opgave kan du angive **Dokumenter, der er modtaget** til *Ja* for flere fragter ad gangen. Brug **Filter**-indstillingerne til at definere det sæt fragter, du vil opdatere.
- **I transit** – Med denne opgave kan du angive feltet **Fragtstatus** til den transitstatus, der er angivet på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)** for flere fragter på én gang. Brug **Filter**-indstillingerne til at definere det sæt fragter, du vil opdatere.
- **Klar til efterkalkulation** – Med denne opgave kan du angive feltet **Fragtstatus** til klar til efterkalkulation, der er angivet på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)** for flere fragter på én gang. Du vil normalt konfigurere denne opgave til at køre regelmæssigt.
- **Efterkalkuleret** – Denne opgave giver dig mulighed for at angive feltet **Fragtstatus** til den efterkalkulerede status, der er angivet på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)** for flere fragter samtidig, forudsat at de er blevet efterkalkuleret, men ikke er opdateret på fragten endnu. Du vil normalt konfigurere denne opgave til at køre regelmæssigt.
