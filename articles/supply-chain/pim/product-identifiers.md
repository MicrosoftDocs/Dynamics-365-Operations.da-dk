---
title: Produktidentifikatorer
description: Dette emne indeholder oplysninger om de forskellige typer produkt-id'er og forklarer, hvordan du kan føje produkt-id'er til produktdataene.
author: cvocph
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 58a32bd7f857e8173996cd4eb21f176bae508587
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "335410"
---
# <a name="product-identifiers"></a>Produktidentifikatorer 

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om de forskellige typer produkt-id'er og forklarer, hvordan du kan føje produkt-id'er til produktdataene.

Når du arbejder med produkter i produktionen eller på et lagersted i Microsoft Dynamics ERP eller Microsoft Dynamics CRM, skal du have en god strategi til at identificere disse produkter og produktvarianter.

## <a name="unique-product-numberproduct-id"></a>Entydigt produktnummer/produkt-id

I Microsoft Dynamics 365 for Finance and Operations er det primære id for et produkt produktnummeret (dvs. det entydige produkt-ID). Dette nummer kan genereres automatisk fra en nummerserie, eller det kan manuelt knyttes til et produkt. For produktvarianter kan numrene defineres via produktnomenklaturskabelonen.

I mange tilfælde er produktnummeret ikke oprindeligt oprettet i Finance and Operations. I stedet tilknyttes til et produkt i et system til administration af produktlivscyklus (PLM) eller et system til administration af produktoplysninger (PDM). I så fald skal du bruge dataenheder til at importere produkterne og produktvarianterne. Finance and Operations bruger derefter numrene i alle handlinger.

Når du implementerer Finance and Operations, skal du foretage specielle overvejelser med hensyn til din strategi for produktnumre. En godt nummereringssystem forbedrer logistikprocesser og hjælper med til at forhindre fejl. Et godt produkt-id må højst være på 15 tegn. Ideelt set har det mindre end 10 tegn og indeholder mere end fem klassificeringstegn. Du kan også bruge søgenavne til at aktivere hurtig søgning. Et søgenavn er et yderligere navn, der repræsenterer klassificeringer af et produkt.

Når du bruger Common Data Service (CDS), er produktnummeret i Finance and Operations også produktnummeret i CDS. Produktvarianter synkroniseres til CDS som specifikke produkter.

## <a name="item-number-and-product-dimensions"></a>Varenummer og produktdimensioner

Varenummeret er det produkt-id, der bruges af en bestemt juridisk enhed. Ideelt set bør varenummeret være identisk med produktnummeret. Hvis nomenklaturen afviger pr. juridisk enhed, bliver det vanskeligt at følge et produkt i hele forsyningskæden, og der introduceres krævende processer til fornyet mærkning og referencer. Af hensyn til kompatibilitet med ældre versioner (det vil sige med Microsoft Dynamics AX 2009 og tidligere) har vi bevaret denne model. Det anbefales dog, at id'er, der er specifikke for juridiske enheder, fjernes, når du har mulighed for det, og at du i stedet bruger entydige produktnummer som det primære id.

Desuden kan en produktvariant ikke identificeres entydigt af et varenummer. Det kræver altid kombinationen af et varenummer og alle de produktdimensioner, der er defineret på produktmasteren. Dette krav kan blive besværligt og kan sænke hastigheden i id-processerne. Derfor anbefales det, at du bruger det entydige produktnummer i stedet for varenummeret, så snart du kan.

Mange sider har stadig varenummeret og produktdimensioner som de primære id'er. Dog kan produktnumrene bruges til søgning. Under **Salg og marketing** &gt; **Konfiguration** &gt; **Søg** &gt; **Søgeparametre**, kan du kan ændre søgningsopslaget, så det bruger produktnumre i stedet for varenumre som den primære søgningsstrategi. Hvis du angiver indstillingen **Aktivér opslag for produktsøgning** til **Ja**, vil opslaget ikke kun vise produktmastere men også produktvarianter. Du kan finde flere oplysninger under [Søge efter produkter og produktvarianter under ordreindtastning](search-products-product-variants.md).

Derudover vil du være i stand til at søge og filtrere på produktnummeret, produktnavnet og beskrivelsen samt produktdimensions-id'er for produktvarianten. Når du vælger en variant, vælges det relaterede varenummer og alle produktdimensions-id'er. Derfor kan du lettere finde og vælge den korrekte variant. Denne indstilling anbefales kraftigt, hvis du bruger produktvarianter og de entydige produktnumre som de primære id'er for produkter. Den eneste undtagelse kan være modebranchen, hvor forretningsprocesserne ofte kræver, at du vælger masteren, før du kan vælge en variant. Du skal evaluere denne indstilling omhyggeligt, før du implementerer nummereringssystemet.

## <a name="product-name-and-description"></a>Produktnavn og -beskrivelse

Produktnavnet og beskrivelsen er de læsbare id'er for et produkt og kan vedligeholdes på mange sprog. Som standard viser Finance and Operations-klienten alle produktoplysninger på firmaets standardsprog, ikke på brugerens sprog. Dog bruges oversatte produktnavne og -beskrivelser i al kommunikation med kunder og leverandører. Oversættelserne er baseret på sprogkoden for debitor- og kreditorkontiene.

For produktvarianter kan produktnavne genereres via en produktnomenklaturskabelon. Da der ikke er noget krav om, at produktnavne skal være entydige, kan du finde flere produkter, der har samme navn.

## <a name="product-and-item-search-names"></a>Produkt- og varesøgenavne

Finance and Operations tilbyder et sekundært søgenavn for produkter og for varer (frigivne produkter). Dette søgenavn behøver ikke være entydigt, og det kan ændres, efter at et produkt eller en produktvariant er oprettet. Det anbefales, at du bruger søgenavnet til at søge efter produkter efter kategorier. Søgenavnene muliggør hurtig søgning, især i salgs- og købsprocesser.

Søgenavnet kan også indeholde et debitor- eller kreditor-produkt-id eller nogle andre eksterne produkt-id'er, hvis dette eksterne id er det primære søgekriterium for et produkt.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Eksterne produkt-id'er (debitor- og kreditor-id'er)

For frigivne produkter kan du vedligeholde de varenumre, varenavne og varebeskrivelser, som debitoren eller kreditoren bruger. Referencerne vises på eksterne dokumenter, f.eks. salgsordrer, indkøbsordrer, følgesedler og fakturaer. I den aktuelle version af Finance and Operations vises eksterne referencer ikke på siderne for grundlæggende operationer. Den eneste undtagelse er kreditorvarenummeret. Dette nummer vises i dialogboksen **Produktoplysninger**, hvis der er angivet en standardleverandør for det frigivne produkt.

Du kan vedligeholde eksterne produkt-id'er efter frigivet produkt, frigiven produktvariant, debitor eller debitorgruppe, eller kreditor eller kreditorgruppe.

På siden **Frigivne produkter** skal du følge en af følgende fremgangsmåder.

- For kunder skal du under fanen **Sælg** i gruppen **Relaterede oplysninger** vælge **Ekstern varebeskrivelse**.
- For leverandører skal du under fanen **Køb** i gruppen **Relaterede oplysninger** vælge **Ekstern varebeskrivelse**.

På siden **Eksterne varebeskrivelser** kan du knytte kundens eller leverandørens varenummer til et frigivet produkt. Denne tilknytning skal udføres for hver juridisk enhed. Der kan hentes følgende oplysninger. Desværre er etiketter en smule vildledende i den aktuelle version af Finance and Operations. Disse etiketter kan dog blive ændret i en fremtidig version.

| Felt | Tilhørende kundeoplysninger | Tilhørende leverandøroplysninger |
|-------|------------------------------------|----------------------------------|
| Eksternt varenummer | Debitorens varenummer | Leverandørens varenummer |
| Betegnelse | Det navn, som kunden knytter til varen | Det navn, som leverandøren knytter til varen |
| Ekstern varetekst | Debitorens varebeskrivelse | Leverandørens varebeskrivelse |

Hvis mange debitorer eller kreditorer bruge de samme varenumre (som det f.eks. er tilfældet i en indkøbssammenslutning eller en detailgruppe), kan du oprette grupper af debitorer/kreditorer for at forenkle vedligeholdelse af eksterne produktoplysninger.

- For debitorgrupper skal du gå til **Salg** &gt; **Konfiguration** &gt; **Varer** &gt; **Ekstern varebeskrivelse** for at oprette og vedligeholde grupperne og de relaterede varenumre. For at knytte kunder til en gruppe, skal du gå til **Debitor** &gt; **Debitorer** &gt; **Alle kunder** og derefter klikke på oversigtspanelet **Salgsordrestandarder** og angive en værdi i feltet **Vare - Kundegruppe**.
- For kreditorgrupper skal du gå til **Indkøb og forsyning** &gt; **Konfiguration** &gt; **Ekstern varebeskrivelsesgruppe** for at oprette og vedligeholde grupperne og de relaterede varenumre. For at knytte kreditorer til en gruppe, skal du gå til **Kreditor** &gt; **Kreditorer** &gt; **Alle kreditorer** og derefter under oversigtspanelet **Standardindstillinger for indkøbsordrer** angive en værdi i feltet **Vare - Leverandørgruppe**.
 
## <a name="bar-codes"></a>Stregkoder

Hvis du vil bruge en stregkodescanner til at identificere produkter, skal produkt-id'et opfylde kravene i stregkodestandard, der bruges. Derfor indeholder stregkoder ikke typisk det rå produktnummer, men et tal, der er oprettet specifikt til den valgte stregkodeteknologi. Du kan vedligeholde flere stregkoder efter stregkodetype. Du kan også knytte den samme stregkode til flere produkter og derefter vælge den faktiske aktive tilknytning, når du scanner en stregkode.

Før du definerer stregkoder, kan du definere en eller flere stregkodeopsætninger. Stregkodeopsætningerne kan hjælpe med til at validere, at stregkoder følger de retningslinjer, der kræves, og at de derfor i praksis kan udskrives og scannes. Du kan også vedligeholde særlige stregkoder til bestemte produktantal.

Det anbefales, at du bruger stregkodeopsætningen til at vedligeholde GTIN-koder (Global Trade Item Number) og EAN-koder (International Article Number).

For at vedligeholde stregkoder skal du på siden **Frigivne produkter** under fanen **Lagerstyring** i gruppen **Lagersted** vælge **Stregkoder**.

## <a name="gtin-codes"></a>GTIN-koder (Global Trade Identification Number-koder)

I e-handel er det afgørende, at alle parter taler et fælles sprog og refererer til produkter ved hjælp af et fælles sæt id'er . Derfor baserer nogle brancher sig på [GTIN](https://www.gs1.org/id-keys/gtin), som er et globalt varenummersystem, der styres af GS1.

I Finance and Operations anbefales det, at du vedligeholder GTIN-nummeret som en stregkode. Men du kan også vedligeholde det på siden **Vare – GTIN**. For at åben denne side skal du på siden **Frigivne produkter** under fanen **Lagerstyring** i gruppen **Lagersted** vælge **GTIN-koder**. Bemærk, at GTIN ikke vedligeholdes som et globalt nummer. I stedet vedligeholdes det efter juridisk enhed.

I Finance and Operations kan du definere emballagevarianter i lagerstedsoperationer ved at definere bestemte måleenheder. En vare kan f.eks. være opbevaret i stykker, bundter af seks, i bakker af 18 eller i fulde paller. Der defineres en specifik måleenhed for hver af disse emballagevarianter. Da GTIN-nummeret normalt er relateret til pakningsenheden af et produkt, giver siden **Vare – GTIN** dig mulighed for at vedligeholde flere GTIN-koder pr. produkt og måleenhed. Men du kan ikke bruge den samme GTIN-kode mere end én gang til forskellige varer eller produktvarianter i en juridisk enhed.

For at vedligeholde **GTIN-koder** skal du på siden **Frigivne produkter** under fanen **Lagerstyring** i gruppen **Lagersted** vælge **GTIN**.

## <a name="external-codes"></a>Eksterne koder

Eksterne koder kan defineres for mange objekter i Finance and Operations. Du kan f.eks. definere eksterne koder til at identificere produkter og frigivne produkter. Disse eksterne koder kan bruges til at tilknytte statistiske koder eller momskoder til frigivne produkter og frigivne produktvarianter. Eksterne koder defineres efter juridisk enhed og kodetype. De skal være entydige efter juridisk enhed, kodetype og tabelreference.

Desværre er der ingen standardfunktioner, hvor du kan søge efter produkter efter eksterne koder.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Dataenheder, der bruges til at importere og eksportere produkt-id'er

| Enhedsnavn | Import-id'er | Eksport-id'er | Bemærkninger |
|-------------|--------------------|--------------------|----------|
| Produkter V2 | Produktnummer, søgenavn for produkt, produktnavn, produktbeskrivelse | Produktnummer, søgenavn for produkt, produktnavn, produktbeskrivelse | Afhængigt af indstillingerne for enheden og nummerserien for produktnummeret, kan produktnummeret oprettes automatisk på tidspunktet for import. |
| Produktvarianter | Produktnummer, søgenavn for produkt, produktnavn, produktbeskrivelse | Produktnummer, søgenavn for produkt, produktnavn, produktbeskrivelse | Afhængigt af produktnomenklaturskabelonen kan produktnummeret oprettes automatisk på tidspunktet for import. Men du kan importere ethvert entydigt produktnummer, og dette produktnummer behøver ikke at følge strukturen i produktnomenklaturskabelonerne. |
| Produktoversættelser | Produktnavn, produktbeskrivelse | Produktnavn, produktbeskrivelse | Denne enhed overskriver alle sprog. Bemærk, at når navnet eller beskrivelsen af en juridisk enheds primære sprog overskrives, ændres navnet og beskrivelsen af selve produktet. |
| Frigivne produkter V2 | Varenummer, produktnummer, søgenavn for vare| Varenummer, produktnummer, søgenavn for vare, søgenavn for produkt, produktnavn | Denne enhed kan være en udfordring, når der bruges nummerserier under oprettelsen af nye frigivne produkter. Både nummerserien **Varenummer** og nummerserien **Produktnummer** har indflydelse. Men nummerserien **Varenummer** er pr. juridisk enhed, mens nummerserien **Produktnummer** er global. Derfor anbefales det ikke, at du bruger nummerserien **Varenummer**, når du angiver nye frigivne produkter. Men når enheden bruges til at frigive et eksisterende produkt, skal produktnummeret naturligvis gives til enheden. Du kan finde yderligere oplysninger i afsnittet "Produkt- og varenummerserier" i dette emne. |
| Frigivne produktvarianter | Varenummer, produktdimensioner, produktnummer | Produktnummer, søgenavn for produkt, produktnavn, produktbeskrivelse, produktdimensioner | Ligesom enheden **produktvarianter** kan denne enhed bruges til at oprette nye produkter, der enten følger produktnomenklaturskabelonen eller bruger deres egne produktnumre til varianten. |
| Ekstern varebeskrivelse for debitorer | Kundens varenummer, kundens varenavn, debitorbeskrivelse, debitorkonto | Kundens varenummer, kundens varenavn, debitorbeskrivelse, debitorkonto | En gruppe kunder (f.eks. en indkøbssammenslutning) kan samles i én gruppe ved hjælp af enheden **Kundegrupper til eksterne varebeskrivelser**. |
| Ekstern varebeskrivelse for kreditorer | Leverandørens varenummer, varenavn for leverandør, leverandørbeskrivelse, leverandørkonto | Leverandørens varenummer, varenavn for leverandør, leverandørbeskrivelse, leverandørkonto | En gruppe leverandører (f.eks. en salgssammenslutning eller en brancheorganisation) kan samles i én gruppe ved hjælp af enheden **Ekstern varebeskrivelse for kreditorgrupper**. |
| Varestregkode | Stregkode | Stregkode | Bemærk, at på tidspunktet for importen, skal du referere til en stregkodeopsætning, der er defineret i målsystemet. De importerede stregkodereferencer valideres mod den pågældende stregkodeopsætning og afvises, hvis stregkoderne ikke stemmer overens med de krav, der er defineret i den pågældende stregkodeopsætning. |
| Eksterne koder for frigivne produkter | Ekstern kode | Ekstern kode, eksterne kodeklasser, varenummer | Eksterne koder er efter juridisk enhed. Til import skal du referere til en defineret kodeklasse. Importér kodeklasserne ved hjælp af enheden **Eksterne kodeklasser for frigivne produkter**. |
| Eksterne koder for frigivne produktvarianter | Ekstern kode | Ekstern kode, eksterne kodeklasser, varenummer, produktdimensioner | Eksterne koder er efter juridisk enhed. Til import skal du referere til en defineret kodeklasse. Importér kodeklasserne ved hjælp af enheden **Eksterne kodeklasser for frigivne produkter**. Denne enhed refererer til produktvarianter af varenummer og produktdimensioner. |
| Eksterne koder for frigivne produktvarianter efter produktnummer-id | Ekstern kode | Ekstern kode, eksterne kodeklasser, produktnummer | Eksterne koder er efter juridisk enhed. Til import skal du referere til en defineret kodeklasse. Importér kodeklasserne ved hjælp af enheden **Eksterne kodeklasser for frigivne produkter**. Denne enhed refererer til produktvarianter efter variantens produktnummer. (Fra den næste store udgivelse) |
| GTIN (Global Trade Identification Number) | Ikke tilgængelig | Ikke tilgængelig | Der er i øjeblikket ingen specifikke enhed, der bruges til at importere og eksportere GTIN-koder. Det anbefales, at du bruger enheden **Varestregkode** i stedet. |
| Common Data Service-id-enhed for produktenhed | Ikke tilgængelig | Varenummer, varenavn for søgning, søgenavn for produkt, leverandørens varenummer, kundens varenummer, eksterne koder, GTIN-koder, stregkoder | Denne enhed konsoliderer alle id'er i én datamodel, så der kan bruges én grænseflade til at eksportere alle id'er og deres relaterede typer. Brug enheden **Id-kode for produktenhed** enhed til at eksportere id-koderne og beskrivelserne. Brug enheden **Id-område for produktenhed** til at eksportere yderligere områdeoplysninger til et id, f.eks. parten, den juridiske enhed, antal eller enhed. |

### <a name="product-and-item-number-sequences"></a>Produkt- og varenummerserier

I Finance and Operations kan du definere to forskellige nummerserier:

- Nummerserien **Produktnummer** for det produktnummer
- Nummerserien **Varenummer** for varenummeret pr. juridisk enhed

> [!NOTE]
> Du skal bruge varenummeret som et separat id, når du overfører forskellige juridiske enheder fra forskellige kilder, der har forskellige nummereringssystemer. Du bør altid prøve at bruge et produkt-id, der er entydig på tværs af alle juridiske enheder. Derfor skal du angive indstillingen **Manuel** til **Ja** for nummerserien **Varenummer**. På denne måde følger varenummeret produktnummeret ved oprettelse. Hvis Finance and Operations ikke er det førende system for nye produktnumre, skal du angive indstillingen **Manuel** til **Ja** for både nummerserierne **Varenummer** og **Produktnummer**.

Når du bruger enheden **Frigivet produkt V2** til at oprette produkter, er der flere indstillinger, som kan påvirke, hvordan nummerserierne bruges til at oprette produktnummeret og varenummeret:

- Indstillingerne for nummerserien **Produktnummer**
- Indstillingerne for nummerserien **Varenummer**
- Tilknytningen af varenummeret 
- Tilknytningen af produktnummeret

Tabellen nedenfor indeholder en oversigt over resultaterne af import og manuel oprettelse ved bestemte kombinationer af indstillingerne for nummerserie og felttilknytning.

| Nummerserie for produktnummer | Nummerserie for varenummer | Tilknytning af varenummeret | Tilknytning af produktnummeret | Resultatet af importen af enheden | Resultatet af manuel oprettelse | Konklusion |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Manuelt = Nej | Manuelt = Nej | Ingen tilknytning | Ingen tilknytning | Produktnumre bruger nummerserien **Produktnummer**. Varenumre bruger nummerserien **Varenummer**. | Produktnumre bruger nummerserien **Produktnummer**. Varenumre bruger nummerserien **Varenummer**. | Disse indstillinger kan bruges, hvis du skal bruge et andet nummer til produkter og varer. Det anbefales dog ikke at bruge forskellige numre til varer og produkter. |
| Manuelt = Nej | Manuelt = Ja | Generer automatisk | Ingen tilknytning | Både produktnumre og varenumre bruger nummerserien **Varenummer**. | Både produktnumre og varenumre bruger nummerserien **Produktnummer**. | Disse indstillinger anbefales ikke. Import og manuel oprettelse fungerer forskelligt. |
| Manuelt = Nej | Manuelt = Ja | Ingen tilknytning | Ingen tilknytning | Både produktnumre og varenumre bruger nummerserien **Produktnummer**. | Både produktnumre og varenumre bruger nummerserien **Produktnummer**. | Disse indstillinger anbefales, hvis produkterne skal have overensstemmende automatisk nummerering, uanset om import eller manuel oprettelse anvendes. |
| Manuelt = Ja | Ikke tilgængelig | Ikke tilgængelig | Generer automatisk | Du modtager følgende fejlmeddelelse: "Nummerserie kan ikke registreres". | I henhold til nummerserien **Varenummer** | Denne indstilling understøttes ikke til import. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Produktenheds-id (eksportér alle produkt-id'er)

Modellen for produktenheds-id enhed blev oprettet for at muliggøre, at version 1.0 af CDS kunne klargøres med alle id'er, der bruges til at referere til et produkt. For at forenkle denne opgave, samles alle id'er i en global id-tabel, så de kan eksporteres som én model. Bemærk, at denne version af CDS ikke bruger modellen for produkt-id'er. Derfor har enheden **Common Data Service-id-enhed for produktenhed** og denne proces begrænset praktisk brug, de vil sandsynligvis blive ændret på et senere tidspunkt.

Produkt-id-tabellen er en global tabel, der udfyldes fra alle referencetabeller i den primære juridiske enhed via et tilbagevendende batchjob. Du skal vælge en juridisk enhed og et produktkategorihierarki som definition af omfanget af den globale produktmaster. Oprettelse af tabellen med globale produkt-id er begrænset til produkter, der er frigivet til den valgte juridiske enhed, og produkter, der er medlemmer af produkthierarkiet, der er valgt til rollen for **Common Data Service** i produktkategorihierarkiet.

Denne processen forudsætter, at produktmasterdata primært vedligeholdes i én central juridisk enhed. (Denne juridiske enhed kan dog være en virtuel juridisk enhed, der kun bruges til at vedligeholde globale masterdata).

Følg disse trin for at konfigurere miljøet.

1. Vælg kategorihierarkiet for CDS. På siden **Tilknytninger af kategorihierarkiroller** skal du oprette en ny tilknytning, hvis der ikke er knyttet noget hierarki til rollen **Common Data Service**. Vælg rollen **Common Data Service**, og tilknyt derefter det kategorihierarki, der repræsenterer det produktsortiment, der skal synkroniseres til CDS.
2. Vælg den juridiske enhed for globale produktmasterdata. På siden **Parametre for administration af produktoplysninger** skal du vælge fanen **Produktattributter**, hvor produkt- og vare-id'erne vedligeholdes primært.
3. Definer de id-kodetyper og -koder, der skal eksporteres. Gå til **Administration af produktoplysninger** &gt; **Konfiguration** &gt; **Produkt-id-koder**. For at generere id-kodetyperne skal du vælge **Generér koder**. Der genereres en kodetypepost for hver type id, der findes i den valgte juridiske enhed.

    Bemærk, at for stregkoder genereres der en kodetype for hver stregkodeopsætning. For eksterne koder genereres der en kodetype for hver ekstern kodeklasse.

    Du kan nu vedligeholde listen over kodetyper. Du kan ændre koden, navnet og beskrivelsen. Du kan også slette kodetyper. Kodetyper, som du kan slette, bruges ikke til at udfylde de globale tabeller over enhed for produktenheds-id.

4. Når du er færdig med at definere typerne af produkt-id-kode, kan du oprette id'er i den globale tabel ved at starte jobbet **Generér koder** på siden **Id-koder for produktenhed**. Dette job bør køres i batchtilstand. Dette job skal være oprettet som et periodisk batchjob, så tabellen udfyldes i overensstemmelse med de nye poster.

Du kan nu bruge **Common Data Service-id-enhed for produktenhed**, **Id-koder for produktenhed**, og **Id-område for produktenhed** til alle målsystemer.

## <a name="related-topic"></a>Relateret emne

[Søge efter produkter og produktvarianter under ordreindtastning](search-products-product-variants.md)
