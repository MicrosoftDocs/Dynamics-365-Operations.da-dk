---
title: Konfigurere farlige materialer
description: Dette emne forklarer, hvordan du kan konfigurere de data, der kræves for at klassificere varer som farlige materialer. Når du opretter en salgsordre, der indeholder en vare, der er klassificeret som farligt materiale, genererer systemet dokumentation til farligt materiale for den pågældende salgsordre, når den leveres.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: db0d78c7a6fa69aa4e0c4c82f92c33daabda073f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983335"
---
# <a name="set-up-hazardous-materials"></a>Konfigurere farlige materialer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Hvis du vil bruge funktionalitet til farlige materialer, skal du først konfigurere de data, der kræves for at klassificere varer som farligt materiale. Når du derefter opretter en salgsordre, der indeholder en vare, der er klassificeret som farligt materiale, genererer systemet dokumentation til farligt materiale for den pågældende salgsordre, når den leveres.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Aktivere funktionen til farligt materiale for systemet

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Administration af produktoplysninger*
- **Funktionsnavn:** *Produktoplysninger om farligt materiale og forsendelsesdokumentation*

## <a name="hazardous-material-regulations"></a>Bestemmelser om farligt materiale

Hvis du vil bruge processerne for farligt materiale, skal du først oprette en forordning. Forordninger definerer, hvordan den udskrevne forsendelsestekst oprettes for en vare. De definerer også de tilknyttede leveringsmåder.

Her er nogle almindelige forordninger:

- **ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej
- **CFR 49** – bestemmelser i USA om transport af farligt gods
- **IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)
- **IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods

Disse forordninger hjælper med at bestemme, hvilke oplysninger der skal vises, når du udskriver forsendelsesteksten for en vare. Du kan definere lige så mange forordninger, som du skal overholde.

> [!IMPORTANT]
> Funktionaliteten til konfiguration af oplysningskoder, der vedrører farligt materiale, får ikke dit firma til at overholde angivne standarder med forordninger. Det er kun et værktøj, der hjælper dig med at opbygge processer for dit firma.

En forordning er typisk tilgængelig for en bestemt transportmåde, f.eks. skibsfragt, vejtransport eller flyfragt. Du kan derfor knytte hver enkelt forordning til en leveringsmåde. Leveringsmåden bruges, når bestemte dokumenter udskrives i Lokationsstyring. I Lokationsstyring knyttes hver enkelt forsendelse til en fragtmand og en fragttjeneste, der er konfigureret i modulet **Transport**. Leveringsmåden er tilknyttet fragtmanden og fragttjenesten. Når du kører en rapport, bruges leveringsmåden til at finde den tekst til forsendelse, der er tilknyttet en frigivet vare.

Disse opsætningsdata er ikke specifikke for de enkelte juridiske enheder (firma). Derfor kan du have et fælles sæt oplysninger om farlige materialer, der deles mellem alle dine juridiske enheder.

For hver forordning kan du definere en materialeliste og bruge den som en skabelonliste, der er knyttet til frigivne varer. For hver forordning kan du også definere en udskriftsopsætning. Med en udskriftsopsætning kan du definere, hvordan forsendelsesteksten for en vare skal fremstilles. Udskriftsopsætningen bruges til at oprette forsendelsestekst til udskrivning for en frigivet vare.

Hvis du vil definere forordninger for farlige materialer, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Forordning for farligt materiale**. På siden **Forordning for farligt materiale** kan du oprette ethvert antal forordninger og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende underafsnit.

### <a name="hazardous-material-regulation-header"></a>Overskrift til forordning om farligt materiale

Hver forordning har en kode og en beskrivelse. I følgende tabel forklares de felter, der er tilgængelige i overskriften.

| Felt | Beskrivelse |
|---|---|
| Forordningskode | Angiv en kode, der identificerer farligt materialets forordningspost. |
| Beskrivelse | Angiv en beskrivelse af forordningen om farligt materiale. |

### <a name="print-setup-fasttab"></a>Oversigtspanelet Udskriftsopsætning

Hver forordning kan have ethvert antal udskriftsopsætninger. Du kan definere udskriftsopsætningerne i oversigtspanelet **Udskriftsopsætning**. I følgende tabel forklares de felter, der er tilgængelige for hver udskriftsopsætning.

| Felt | Beskrivelse |
|---|---|
| Rækkefølge | Definer den rækkefølge, som felterne i forsendelsesteksten skal omtales i. |
| Udskriftsfelt | Vælg det felt, der skal indgå i forsendelsesteksten. Ikke alle felter til farligt materiale kan udskrives. Det er kun de almindelige felter, der bruges til at definere forsendelsestekst i de forskellige forordninger, der vil være tilgængelige. Du skal definere det første udskriftsfelt som en feltseparator, der har en **Sekvens**-værdi på *0* (nul), så det kan bruges som separator mellem andre felter. Der kræves kun én reference til feltseparatoren.<p>Følgende værdier er tilgængelige:</p><ul></li><li>**Feltseparator** – Dette udskriftsfelt bruges som feltseparator for teksten. Der kræves kun én feltseparator i sekvensen. Normalt skal du angive **Sekvens**-værdien for dette udskriftsfelt til *0* (nul). Systemet vil søge efter en feltseparator og bruge den første, der findes på listen. Den tekstværdi, der bruges i strengen, kommer fra feltet **Udskriv efter**.</li><li>**Identifikation** – Dette udskriftsfelt indsætter [identifikationskoden og/eller beskrivelsen](#identification) i den trykte tekst.</li><li>**Klasse** – Dette udskriftsfelt indsætter [klassekoden og/eller beskrivelsen](#classes) i den trykte tekst.</li><li>**Division** – Dette udskriftsfelt indsætter [divisionskoden og/eller beskrivelsen](#divisions) i den trykte tekst.</li><li>**Emballagegruppe** – Dette udskriftsfelt indsætter [emballagegruppekoden og/eller beskrivelsen](#packing-group) i den trykte tekst.</li><li>**Tunnelkode og/eller -beskrivelse** – Dette udskriftsfelt indsætter [tunnelkode og/eller -beskrivelse](#tunnel) i den trykte tekst.</li><li>**Korrekt forsendelsesnavn** – Dette udskriftsfelt indsætter det [korrekte forsendelsesnavn](hazmat-items.md#hazmat-description) i den trykte tekst.</li><li>**Teknisk navn** – Dette udskriftsfelt indsætter [teknisk navn og/eller beskrivelse](#technical-name) i den trykte tekst.</li><li>**Transportkategori** – Dette udskriftsfelt indsætter [transportkategori og/eller -beskrivelse](#transport-category) i den trykte tekst.</li><li>**Opbevaring** – Dette udskriftsfelt indsætter [opbevaringskoden og/eller -beskrivelsen](#stowage) i den trykte tekst.</li><li>**Fasttekst** – Dette udskriftsfelt angiver den tekst, der er defineret i feltet **Fasttekst** for denne række.</li><li>**Etiketkode og/eller -beskrivelse** – Dette udskriftsfelt indsætter [etiketkode og/eller -beskrivelse](#label) i den trykte tekst.</li><li>**Flyemballage** – Dette udskriftsfelt indsætter [instruktionskoden og/eller -beskrivelsen til flyemballage](#packing-instruction) i den trykte tekst.</li><li>**Begrænset mængde** – Dette udskriftsfelt kontrollerer, om varen er markeret som [vare med begrænset mængde](hazmat-items.md#material-management) og angiver i så fald den tekst, der er defineret i feltet **Fasttekst** for denne række.</li><li>**Emballagebeskrivelse** – Dette udskriftsfelt indsætter [emballagebeskrivelsen](#packing-description) i den trykte tekst.</li></ul> |
| Udskriv før | Angiv den tekst, der skal udskrives før det indhold, der er defineret af indstillingen **Udskriftsfelt**. |
| Udskriv efter | Angiv den tekst, der skal udskrives efter det indhold, der er defineret af indstillingen **Udskriftsfelt**. |
| Udskriv med forrige | Markér dette afkrydsningsfelt for at forhindre, at feltseparatoren udskrives mellem det forrige felt og dette felt. Brug dette afkrydsningsfelt til udskriftsfelter, der enten er valgfrie eller er medtaget i et andet udskriftsfelt. |
| Fast tekst | Hvis du har angivet feltet **Udskriftsfelt** til **Fasttekst** eller **Begrænset mængde**, skal du angive den tekst, der skal udskrives. |
| Medtag i udskrift | Vælg, hvilken værdi eller hvilke værdier i det valgte udskriftsfelt der skal udskrives for denne række. Du kan udskrive koden, beskrivelsen eller både koden og beskrivelsen. |

### <a name="mode-of-delivery-fasttab"></a>Oversigtspanelet Leveringsmåde

Forordningen er en delt tabel, der ikke er specifik for de enkelte juridiske enheder. Leveringsmåder er dog specifikke for juridiske enheder. Når du konfigurerer en leveringsmåde, skal du derfor vælge relationen mellem forordningen, den juridiske enhed og leveringsmåden.

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Leveringsmåde**.

| Felt | Beskrivelse |
|---|---|
| Firma | Vælg en juridisk enhed, der skal knyttes til denne forordning. |
| Leveringsmåde | På basis af den juridiske enhed, du har valgt, skal du vælge den leveringsmåde, der skal knyttes til forordningen. |

### <a name="country-fasttab"></a>Oversigtspanelet Land/område

Til referenceformål kan du få vist de lande/områder eller regioner, som en regel er relevant for. Men når forsendelsesrapporter køres, er det kun leveringsmåden, der bruges til at bestemme forordningen. Når du gennemser en lagerforsendelse, er der ikke et direkte link til leveringsmåden. Forsendelsen kan være tilknyttet fragtmanden og fragttjenesten. Når du definerer en fragttjeneste, skal du knytte den til en leveringsmåde. Denne relation bruges i forsendelsesrapporter som f.eks. fragtseddel til at finde forsendelsens udskrivningstekst for en vare.

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Land/område**.

| Felt | Beskrivelse |
|---|---|
| Land/område | Vælg et land/område, der skal tilknyttes forordningen. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materialekoder

Materialekoder indeholder indstillinger, der vedrører en bestemt farlig komponent, som kan inkluderes i et frigivet produkt. Hver materialekode tilhører en specifik forordning om farligt materiale, og definitionen skal stemme overens med denne forordning. Når du anvender en materialekode på et frigivet produkt ved hjælp af feltet **Materialekode**, anvendes alle kodens indstillinger for farligt materiale automatisk på det pågældende produkt. Derfor er processen med at konfigurere frigivne produkter hurtigere og mere ligetil.

Udfør følgende trin for at administrere definitionerne af farlige materialer.

1. Gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Forordning for farligt materiale**.
2. Vælg den forordning, der skal konfigureres en definition af farligt materiale for.
3. I handlingsruden skal du under fanen **Konfiguration** vælge **Farlige materialer**.
4. Angiv en materialekode for definitionen af farligt materiale i feltet **Materialekode**. Du vælger denne værdi, når du anvender materialekoden på et frigivet produkt.

    Feltet **Forordningskode** er skrivebeskyttet og viser den forordning, som du valgte i trin 2.

5. Brug de resterende felter på denne side til at oprette og konfigurere hvert farligt materiale, der er relevant for den valgte forordning. De tilgængelige felter er et undersæt af de felter for farligt materiale, der er tilgængelige for individuelle frigivne produkter. Du kan finde flere oplysninger under [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Klassifikationsgrupper for farlige materialer

Hver klassifikationsgruppe for farligt materiale definerer en gruppe af feltværdier, der opretter en skabelon. Du kan bruge denne skabelon senere, når du konfigurerer oplysninger om farligt materiale for en frigivet vare.

Når du tildeler en frigivet vare en klassifikationsgruppekode for farligt materiale, vil de oplysninger, der er knyttet til den pågældende klassifikationsgruppe, blive kopieret til de relevante felter i varen. Derfor kan du forenkle konfigurationsprocesserne ved at oprette et sæt relaterede feltværdier, som du ofte bruger sammen.

Disse opsætningsdata er ikke specifikke for de enkelte juridiske enheder. Derfor kan du have et fælles sæt oplysninger om farlige materialer, der deles mellem alle dine juridiske enheder.

Hvis du vil konfigurere klassifikationsgrupper for farlige materialer, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Klassifikationsgruppe for farligt materiale**. På siden **Klassifikationsgruppe for farligt materiale** kan du oprette ethvert antal grupper og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende tabel.

| Felt | Beskrivelse |
|---|---|
| Gruppekode | Angiv en kode som identifikation af gruppen. |
| Beskrivelse | Angiv en beskrivelse af gruppen. |
| Klassekode | Knyt et farligt materiales [klassekode](#classes) til gruppen. |
| Afdelingskode | Knyt et farligt materiales [divisionskode](#divisions) til gruppen. |
| Pakkegruppekode | Knyt en [emballagegruppekode](#packing-group) til gruppen. |
| Kode for transportkategori | Knyt en [transportkategorikode](#transport-category) til gruppen. |
| Multiplikator | Angiv det farlige materiales multiplikator, der gælder for den valgte klasse og division af farligt materiale efter den gældende forordning. Denne multiplikator bruges som en del af den formel, der beregner de samlede *point for farligt materiale*, som er medtaget i en last eller forsendelse. Yderligere oplysninger om point for farlige materialer og denne multiplikator finder du i [oversigtspanelet Materialestyring](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Klasser af farlige materialer

En klasse af farligt materiale knyttes typisk til listen over de klasser, der findes i den forordning, som du skal være i overensstemmelse med. Den amerikanske forordning CFR 49 viser f.eks. "klasse 3" som brandfarlige og brændbare væsker. Du kan konfigurere de klasser, der er relevante for de materialer, du skal klassificere.

Hver klasse tildeles en materialeopsætning på den materialeliste, der er relateret til denne forordning. Du skal tildele hver af de frigivne varer en klasse efter behov for at beskrive et produkts skadelige karakter.

Disse opsætningsdata er ikke specifikke for de enkelte juridiske enheder. Derfor kan du have et fælles sæt oplysninger om farlige materialer, der deles mellem alle dine juridiske enheder.

Klasser af farligt materiale arbejder sammen med divisioner, grupper og kompatibilitetsgrupper på følgende måde:

- Når du knytter en klasse af farligt materiale til en frigivet vare, skal du også tilknytte en [division af farligt materiale](#divisions).
- Du kan bruge klasser af farlige materialer sammen med [klassifikationsgrupper for farlige materialer](#classification-groups) til at oprette en skabelon over koder til opsætning af varer.
- Du kan bruge [kompatibilitetsgrupper for farlige materialer](#compatibility-groups) til at fastslå, hvilke klasser og divisioner af farligt materiale der kan leveres sammen.

Hvis du vil konfigurere klasser af farlige materialer, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Klasse af farligt materiale**. På siden **Klasse af farligt materiale** kan du oprette ethvert antal klasser og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende tabel.

| Felt | Beskrivelse |
|---|---|
| Klassekode | Angiv en kode som identifikation af klassen. Du kan definere denne kode for varen. Den bruges derefter på opslagslister, når du knytter en klasse af farligt materiale til en frigivet vare. |
| Beskrivelse | Angiv en beskrivelse af klassen. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Divisioner af farligt materiale

En division af farligt materiale er et undersæt af en klasse af farligt materiale. Du skal knytte både en division og en klasse til hvert produkt, der indeholder farligt materiale.

For klasser, der ikke har divisioner, skal du oprette en division, hvor koden er *0*. I IATA-forordningen er der f.eks. ikke nogen underdivisioner i klasse 7 af radioaktive materialer. I dette tilfælde skal du oprette en *0*-division, som du kan knytte til et frigivet produkt, når du tildeler klassen.

Disse opsætningsdata er ikke specifikke for de enkelte juridiske enheder. Derfor kan du have et fælles sæt oplysninger om farlige materialer, der deles mellem alle dine juridiske enheder.

Divisioner af farligt materiale arbejder sammen med klasser, grupper og kompatibilitetsgrupper på følgende måder:

- Når du knytter en division af farligt materiale til en frigivet vare, skal du også tilknytte en [klasse af farligt materiale](#classes).
- Du kan bruge divisioner af farlige materialer sammen med [klassifikationsgrupper for farlige materialer](#classification-groups) til at oprette en skabelon over koder til opsætning af varer.
- Du kan bruge [kompatibilitetsgrupper for farlige materialer](#compatibility-groups) til at fastslå, hvilke klasser og divisioner af farligt materiale der kan leveres sammen.

Hvis du vil konfigurere divisioner for farlige materialer, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Division af farligt materiale**. På siden **Division af farligt materiale** kan du oprette ethvert antal divisioner og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende tabel.

| Felt | Beskrivelse |
|---|---|
| Division | Angiv en kode, der skal bruges som referencenummer for divisionen. |
| Beskrivelse | Angiv en beskrivelse af divisionen. |
| Klasse | Find og tildel den klasse, som divisionen tilhører. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Kompatibilitetsgrupper for farlige materialer

Kompatibilitetsgrupper for farlige materialer fastslår, hvilke klasser og divisioner af farligt materiale der kan leveres sammen. Når operatører opretter lagerlaster eller-forsendelser, kan de køre en kompatibilitetskontrol, der vil give en advarsel, hvis lasten eller forsendelsen indeholder varer, der ikke alle tilhører samme kompatibilitetsgruppe.

Disse opsætningsdata er ikke specifikke for de enkelte juridiske enheder. Derfor kan du have et fælles sæt oplysninger om farlige materialer, der deles mellem alle dine juridiske enheder.

Hvis du vil konfigurere kompatibilitetsgrupper for farlige materialer, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Kompatibilitetsgruppe for farligt materiale**. På siden **Kompatibilitetsgruppe for farligt materiale** kan du oprette ethvert antal kompatibilitetsgrupper og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende tabel.

### <a name="hazardous-material-compatibility-group-header"></a>Overskrift til kompatibilitetsgruppe for farlige materialer

Hver kompatibilitetsgruppe har en kode og en beskrivelse. I følgende tabel forklares de felter, der er tilgængelige i overskriften.

| Felt | Beskrivelse |
|---|---|
| Kompatibilitetsgruppe | Angiv en kode som identifikation af kompatibilitetsgruppen |
| Beskrivelse | Angiv en beskrivelse af kompatibilitetsgruppen. |

### <a name="compatibility-group-details"></a>Detaljer for kompatibilitetsgruppe

Hver kompatibilitetsgruppe fastslår en liste over klasser og divisioner af farligt materiale, der kan leveres sammen.

| Felt | Beskrivelse |
|---|---|
| Klasse | Vælg en klasse af farligt materiale, der er kompatibel med alle andre klasser i gruppen. |
| Division | Vælg en division af farligt materiale, der tilhører den valgte klasse. |

## <a name="hazardous-material-specification-values"></a>Værdier for specifikation af farligt materiale

Microsoft Dynamics 365 Supply Chain Management har flere typer specifikationer af skadelige materialer. For hver type skal du oprette et centraliseret sæt værdier for hvert relevant felt. Brugerne kan derefter vælge blandt disse værdier, når de konfigurerer definitioner af farlige materialer eller frigivne produkter. Supply Chain Management giver en samling sider, hvor du kan oprette værdierne. Hver side er dedikeret til én specifikationstype. Du kan finde en beskrivelse af de enkelte tilgængelige specifikationer og oplysninger om, hvordan du kan fastslå, hvilke værdier der er tilgængelige for den, i følgende underafsnit.

Et eksempel på en specifikation af farligt materiale er _opbevaringskoden_, som angiver, hvordan et bestemt materiale kan opbevares under transporten. Ved hjælp af oplysningerne i dette afsnit skal du oprette en central samling af opbevaringskoder. Denne samling vises derefter for brugerne på en rulleliste, når de indstiller opbevaringskoden for et frigivet produkt.

Disse specifikationsværdier for farlige materialer er ikke specifikke for de enkelte juridiske enheder. Derfor kan du have et sæt fælles værdier, der deles af alle dine juridiske enheder.

Du skal bruge [materialekoder](#hazmat-codes) til at etablere almindelige samlinger af indstillinger for hver specifikation, som gælder for en given forordning. Derefter kan du anvende den relevante kode på hvert enkelt frigivne produkt efter behov. Du kan finde oplysninger om, hvordan du anvender en kode for farligt materiale på et bestemt frigivet produkt, og hvordan du konfigurerer individuelle indstillinger for produktet for enhver specifikation, der beskrives her, under [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Nødberedskab for farligt materiale

Specifikationen *Nødberedskab for farligt materiale* angiver, hvad der skal gøres, hvis noget går galt, mens et produkt, der indeholder et bestemt farligt materiale, transporteres.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Nødberedskab for farligt materiale**. På siden **Nødberedskab for farligt materiale** kan du oprette et hvilket som helst antal værdier og konfigurere dem hver med en klassifikationskode og en kort beskrivelse.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Identifikation af farligt materiale

Specifikationen *Identifikation af farligt materiale* identificerer klassen eller arten af farligt materiale. Værdien er typisk en kode baseret på en FN-standard. Hver klasse er identificeret ved en kode og en beskrivelse, og den kan angive grænser for transportmetoder. Hvis du f.eks. vil identificere en brandfarlig vare eller et farligt materiale, skal du oprette en klasse af farligt materiale, der bruger koden *FL* og beskrivelsen *Brændbar*. Du angiver også, at klassen ikke må transporteres ad luftvejen.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Identifikation af farligt materiale**. På siden **Identifikation af farligt materiale** kan du oprette ethvert antal værdier og konfigurere dem ved hjælp af de felter, der er beskrevet i følgende tabel.

| Felt | Beskrivelse |
|---|---|
| Identifikation | Angiv en kode, der skal bruges som referencenummer, der identificerer denne klasse af farligt materiale. |
| Beskrivelse | Angiv en beskrivelse af denne klasse. |
| Begræns fra lufttransport | Markér dette afkrydsningsfelt for at angive, at denne klasse af farligt materiale ikke skal transporteres ad luftvejen. |
| Begræns fra søtransport | Markér dette afkrydsningsfelt for at angive, at denne klasse af farligt materiale ikke skal transporteres ad søvejen. |

### <a name="hazardous-material-label"></a><a name="label"></a>Etiket for farligt materiale

Specifikationen *Etiket for farligt materiale* identificerer den etiket på farligt gods, der skal anvendes på relevante frigivne produkter. Selve etiketterne beskriver, hvordan produktet skal håndteres. Du har f.eks. et produkt, der indeholder en giftig gasart. I dette tilfælde skal du konfigurere en etiketkode, der repræsenterer den giftige gasetiket. Du opretter også din forretningsproces, så den slår værdien op, når du leverer produkter.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Etiket for farligt materiale**. På siden **Etiket for farligt materiale** kan du oprette et hvilket som helst antal etiketter og konfigurere dem hver med en identifikationskode og en kort beskrivelse.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Pakningsbeskrivelser for farligt materiale

Specifikationen *Emballagebeskrivelser af farligt materiale* angiver, hvordan en farlig vare skal pakkes. Det kan f.eks. være nødvendigt at pakke den i en bestemt type ståltromle eller en anden type specialemballage.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Emballagebeskrivelser af farligt materiale**. På siden **Emballagebeskrivelser af farligt materiale** kan du oprette et hvilket som helst antal emballagebeskrivelser og konfigurere dem hver med en identifikationskode og en kort beskrivelse.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Pakkegruppe for farligt materiale

Specifikationen *Emballagegruppe af farligt materiale* identificerer emballagegruppen for en farlig vare. Du kan bruge emballagegruppen til at definere en kode og en beskrivelse, der angiver, hvordan varer med farligt materiale skal pakkes under transport eller forsendelse. Emballagegruppen tildeles varen via siden **Varen er farligt gods**.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Emballagegruppe af farligt materiale**. På siden **Emballagegruppe af farligt materiale** kan du oprette et hvilket som helst antal emballagegrupper og konfigurere dem hver med en identifikationskode og en kort beskrivelse.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Pakningsinstruktion for farligt materiale

Specifikationen *Emballageinstruktion til farligt materiale* angiver emballageinstruktioner, der skal følges, når en bestemt farlig vare forberedes til transport ad luftvejen.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Emballageinstruktion til farligt materiale**. På siden **Emballageinstruktion til farligt materiale** kan du oprette et hvilket som helst antal identifikatorer for emballageinstruktion og konfigurere dem hver med en identifikationskode og en kort beskrivelse.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Stuvning af farligt materiale

Specifikationen *Opbevaring af farligt materiale* angiver, hvordan et produkt skal opbevares på et skib, når det transporteres ad søvejen.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Opbevaring af farligt materiale**. På siden **Opbevaring af farligt materiale** kan du oprette et hvilket som helst antal opbevaringsidentifikatorer og konfigurere dem hver med en identifikationskode og en kort beskrivelse.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Transportkategori for farligt materiale

Specifikationen *Transportkategori af farligt materiale* bruges typisk til at gruppere ensartede farlige produkter i rapporter. Transportkategorier bruges f.eks. i rapporten **Forsendelsesoversigt**, som du kan udskrive fra lagerforsendelsesposten.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Transportkategori af farligt materiale**. På siden **Transportkategori af farligt materiale** kan du oprette et hvilket som helst antal transportkategorier og konfigurere dem hver med et vist navn og en kort beskrivelse.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Teknisk navn for farligt materiale

Specifikationen *Teknisk navn for farligt materiale* kan bruges til at angive et almindeligt anvendt eller internt firmanavn, der beskriver hvert materiale.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Teknisk navn for farligt materiale**. På siden **Teknisk navn for farligt materiale** kan du oprette et hvilket som helst antal tekniske navne og konfigurere dem hver med et vist navn og en kort beskrivelse.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Tunnel for farligt materiale

Specifikationen *Tunnel for farligt materiale* begrænser de typer af tunneler, som et farligt materiale kan transporteres gennem, ved at identificere de typer tunneler, der skal bruges. Tunnelkategorier fastlægges af gældende bestemmelser for transport af farligt materiale. Denne specifikation gælder normalt kun for vejtransport.

Hvis du vil konfigurere værdier for denne specifikation, skal du gå til **Administration af produktoplysninger: \> Konfiguration \> Forsendelsesdokumentation til farligt materiale \> Tunnel for farligt materiale**. På siden **Tunnel for farligt materiale** kan du oprette et hvilket som helst antal tunnelidentifikatorer og konfigurere dem hver med en identifikationskode og en kort beskrivelse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]