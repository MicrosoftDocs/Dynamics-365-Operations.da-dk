---
title: Intrastat-oversigt
description: Dette emne indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU. Den indeholder en oversigt over rapporteringsprocessen og beskriver de nødvendige indstillinger og forudsætninger.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a70108696d6187126c23eca1779553210cd4a9d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407713"
---
# <a name="intrastat-overview"></a>Intrastat-oversigt

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU. Den indeholder en oversigt over rapporteringsprocessen og beskriver de nødvendige indstillinger og forudsætninger.

Intrastat er det system, der bruges til indsamling af oplysninger og generering af statistik over varehandel blandt lande/områder i EU. Intrastat-rapportering er påkrævet, når et produkt krydser grænsen til et andet EU-land/område. I nogle lande/områder gælder Intrastat-rapportering også for tjenester. Obligatoriske og fakultative elementer kan indsamles i Intrastat-rapportering. Følgende elementer er obligatoriske: momsnr. på den part, der er ansvarlig for at levere oplysninger, referenceperioden, strømmen (modtagelse eller forsendelse), den ottecifrede varekode, partnerens medlemsstat (afsendelsesmedlemsstaten på modtagelser) og bestemmelsesmedlemsstaten for forsendelser, varernes værdi, mængden af varer (nettomasse og supplerende enheder) og transaktionens art. Lande/regioner kan også indsamle valgfrie elementer i forskellige situationer. Nogle valgfrie elementer er land/region, leveringsbetingelserne, transportmåden, en mere detaljeret varekode end CN8, oprindelsesområdet for forsendelser og destinationsområdet for modtagelser, den statistiske procedure, den statistiske værdi, en beskrivelse af varerne og havn/lufthavn for lastning/losning.

## <a name="overview-of-the-intrastat-reporting-process"></a>Oversigt over Intrastat-rapporteringsprocessen
I følgende afsnit beskrives den samlede strøm af oplysninger, der bruges til Intrastat-rapportering.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Angiv en transaktion, der krydser grænsen til et andet EU-land/område

En debitorfaktura, fritekstfaktura, indkøbsordrefaktura, projektfaktura, følgeseddel for kunden og leverandørens produktkvittering eller overflytningsordre overføres til Intrastat-kladden, hvis landetypen for destination (på udførsel) eller forsendelse (på indførsel) er **EU**. Denne funktion blev udvidet til Microsoft Dynamics 365 for Operations (1611) og gør det muligt at angive fragtadresser for en transaktion inden for Fællesskabet. Hvis en fragtadresse afviger fra en leverandørs virksomhedsadresse (eller kundes virksomhedsadresse for returordre), bruges Intrastat-rapporteringen med disse oplysninger. Når du opretter en salgsordre, fritekstfaktura, indkøbsordre, kreditorfaktura, projektfaktura eller overflytningsordre, har nogle felter, der er relateret til udenrigshandel, standardværdier i dokumentets sidehoved eller på linjen. Standardkoden for transaktionen er taget fra det tilsvarende felt på siden **Udenrigshandelsparametre**. Standarden for varekode, oprindelsesland/-område og oprindelsesstat tages fra varen. Du kan ændre standardværdierne, og du kan også udfylde andre udenlandske handelsrelaterede oplysninger: den statistiske procedure, transportmåde og havn.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Brug denne Intrastat-kladde til at generere oplysninger om handel mellem lande/områder i EU.

Til statistiske formål kan du generere oplysninger om handel mellem EU-lande/områder hver måned. Du kan overføre posteringer fra en fritekstfaktura, debitorfaktura, debitors følgeseddel, kreditorfaktura, kreditor følgeseddel, projektfaktura eller overflytningsordre, på grundlag af kriterier for overførsel, der er angivet på siden **Udenrigshandelsparametre**. Du kan også angive transaktioner manuelt. Du kan manuelt opdatere overførte transaktioner i Intrastat-kladden, hvis opdateringer er påkrævet. Under bestemte betingelser, der er angivet på siden **Komprimering af Intrastat**, kan du komprimere transaktionerne i Intrastat-kladden. For nogle lande/områder kan du anvende en tærskel på små transaktioner. Du kan rapportere transaktioner, der ligger under tærsklen, under den angivne varekode. Du kan opdatere varekoden på de tilsvarende Intrastat-kladdelinjer, baseret på indstillingen **Minimumsgrænse** på siden **Udenrigshandelsparametre**. Du kan også komprimere de transaktioner, der er baseret på indstillingen **Komprimering af Intrastat**. Du kan validere fuldstændigheden af transaktioner i Intrastat-kladden, baseret på indstillingen **Kontroller opsætning** på siden **Udenrigshandelsparametre**. Dataene i de tilsvarende felter kan valideres for nøjagtighed: land/område, stat eller region, vægt, varekode, transaktionskode, supplerende enhed, havn, oprindelse, vilkår for levering, transportmåde og momsundtagelsesnummer. Transaktioner, der ikke er fuldført, markeres som ikke gyldig.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Brug denne Intrastat-kladde til at rapportere oplysninger om handel mellem lande/områder i EU.

Til statistiske formål kan du rapportere oplysninger om handel mellem EU-lande/områder hver måned. Du kan udskrive Intrastat-rapporten, baseret på indstillingen **Rapportformattilknytning** på siden **Udenrigshandelsparametre**. Du kan generere en elektronisk fil, baseret på indstillingen **Filformattilknytning** på siden **Udenrigshandelsparametre**. Se Opgaveregistrering for Intrastat-rapportering for at få yderligere oplysninger om Intrastat-rapportering, herunder de nødvendige forudsætninger.

-   Generere en EU Intrastat-opgørelse
-   Overføre transaktioner til Intrastat
-   Angiv fragtadresse for en transaktion inden for EU.

## <a name="prerequisites"></a>Forudsætninger
Tabellen nedenfor viser kravene til Intrastat-rapportering.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Adresseopsætning</td>
<td>Angiv ISO-koderne for lande/områder.</td>
</tr>
<tr class="even">
<td>Juridisk enhed</td>
<td>Angiv momsfritagelsesnumre til import og eksport, afdelingens lokalnummer til import/eksport og den Intrastat-kode, der er tilknyttet den juridiske enhed.</td>
</tr>
<tr class="odd">
<td>Produktkategorihierarki (salgshierarki, indkøbshierarki)</td>
<td>Tildel Intrastat-varekoder til kategorinoder på fanen <strong>Varekoder</strong> på siden <strong>Kategorihierarki</strong>. Når du tildeler en varekode til en overordnet kategorinode, er den pågældende kode gældende for alle underordnede kategorinoder. De valgte varekoder bliver tilgængelig i visningen <strong>Valgte</strong>, når du vælger en varekode i de frigivne produktdetaljer og på linjer for salgsordre, indkøbsordre og overførselsordre.</td>
</tr>
<tr class="even">
<td>Frigivne produktdetaljer</td>
<td>Opret følgende udenrigshandelsdata for frigivne produkter:
<ul>
<li><strong>Varekode</strong> – Vælg enten en liste over valgte varer, der er hentet fra tildelte produktkategorier, eller den komplette liste over Intrastat-varekoder.</li>
<li><strong>Statistiske gebyrer i procent</strong></li>
<li><strong>Oprindelsesland/-område</strong> – Vælg det standardland/-område, hvor varerne blev helt fremstillet eller produceret.</li>
<li><strong>Område for oprindelse/destination</strong> – Vælg standardområdet for destinationen for modtagelser og stat/provins for afsendelser.</li>
<li><strong>Nettovægt i kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Debitorer</td>
<td>Angiv kundens leveringsadresse i EU-landet.</td>
</tr>
<tr class="even">
<td>Kreditorer</td>
<td>Angiv leverandørens adresse i EU-landet.</td>
</tr>
<tr class="odd">
<td>Tillæg</td>
<td>Angiv den tillægskode, der skal medtages i fakturabeløbet, statistiske beløb eller begge. På siden <strong>Gebyrkoder</strong> på fanen <strong>Udenrigshandel</strong> skal du aktivere <strong>Intrastat-fakturaværdi</strong> for at inkludere tillægsbeløbet i fakturaværdien og aktivere <strong>Værdi af Intrastat-statistik</strong> for at inkludere tillægsbeløbet i den statistiske værdi.</td>
</tr>
<tr class="even">
<td>Elektronisk rapportering</td>
<td>Angiv elektronisk rapportering af konfigurationer for at eksportere Intrastat-data i en elektronisk fil, der har det format, der er anmodet om af de relevante myndigheder, og se Intrastat-data i et brugervenligt, læsbart format (for eksempel i Microsoft Excel).</td>
</tr>
<tr class="even">
<td>Lagersted</td>
<td>Tilknyt kreditorkonti til lagerstedskoder til udfyldning af SE-nummer ved overførsel af flytteordre.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Konfiguration
I følgende afsnit beskrives de indstillinger, der skal bruges til Intrastat-rapportering.

### <a name="set-up-all-required-intrastat-related-lists"></a>Konfigurer alle nødvendige Intrastat-relaterede lister

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Liste</th>
<th>Flere oplysninger</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varekoder</td>
<td>Opret et kategorihierarki af typen <strong>Varekode</strong>, og angiv alle varekoder i henhold til den kombinerede nomenklatur-liste. For hver enkelt vare kan du angive følgende oplysninger:
<ul>
<li>Navnet på varen og varekoden.</li>
<li>Det brugervenlige navn og/eller det oversatte navn</li>
<li>Indstillinger for rapportering af yderligere (supplerende) enheder under fanen <strong>Udenrigshandel</strong>. Du kan vælge den ekstra enhed på enhedslisten. Du kan også angive, om vægten af varer skal rapporteres sammen med den valgte ekstra enhed.</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaktionskategorier</td>
<td>Angiv arten af transaktionen i henhold til dit lands/områdes krav. For hver transaktionskode, du har angivet, skal du angive regler for beregning af fakturabeløb og statistiske beløb for overførselsordrer og salgs-/købsordrer.
<ul>
<li>For overførselsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:
<ul>
<li><strong>Tom</strong> – beløbet vil være 0 (nul).</li>
<li><strong>Økonomisk kostbeløb</strong> – beløbet er lig med omkostningerne.</li>
<li><strong>Samlede omkostninger</strong> – beløbet er lig med den samlede kostpris for transaktionen.</li>
<li><strong>Manuel</strong> – beløbet er lig med det beløb, der angives manuelt på overførselsforslagslinjen.</li>
</ul></li>
<li>For salgsordrer og indkøbsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:
<ul>
<li><strong>Tom</strong> – beløbet vil være 0 (nul).</li>
<li><strong>Fakturabeløb</strong> – beløbet er lig med det beløb, der er faktureret for varen.</li>
<li><strong>Grundbeløb</strong> – beløbet, der er lig med det beløb, der skal faktureres, før nogen rabat.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transportmåder</td>
<td>Angiv transportmåden i henhold til dit lands/områdes krav. For hver leveringsmåde kan du konfigurere en standardtransportmåde på fanen <strong>Udenrigshandel</strong>.</td>
</tr>
<tr class="even">
<td>Havne</td>
<td>Angiv havn/lufthavn for lastning/losning, hvis disse oplysninger er indsamlet af dit land/område.</td>
</tr>
<tr class="odd">
<td>Statistiske procedurer</td>
<td>Angiv den statistiske procedure, hvis disse oplysninger er indsamlet af dit land/område.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Angiv regler for komprimering af Intrastat-transaktioner

På siden **Komprimering af Intrastat** kan du vælge felterne, der skal bruges til komprimering. Alle transaktioner, der har den samme kombination af værdier for de valgte felter i Intrastat-kladden, komprimeres til en enkelt transaktion, når du kører funktionen Komprimer i Intrastat-kladden.

### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

Brug siden **Udenrigshandelsparametre** til at konfigurere parametre i tabellen nedenfor.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fane</th>
<th>Parametre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generel</td>
<td><ul>
<li><strong>Generelt</strong> – Angiv følgende oplysninger:
<ul>
<li>Standardværdien transaktionskoder for salgsordrer, indkøbsordrer, kreditnotaer og overførselsordrer. Den transaktionskode, der er oprettet for kreditnotaer, bruges også som kode for fysisk returnerede varer og bruges til afvigende fysiske returneringer kontra korrektionskreditnotaer.</li>
<li>Den medarbejder, der er ansvarlig for udarbejdelse, af Intrastat-rapporter.</li>
</ul></li>
<li><strong>Minimumsgrænse</strong> – Angiv indstillinger for opdatering af transaktioner, der ligger under tærsklen:
<ul>
<li>Tærskelbeløb og vægt</li>
<li>Varekode, der skal gælde for transaktioner, der er under tærsklen</li>
</ul></li>
<li><strong>Overfør</strong> – Angiv kriterierne for at overføre transaktioner til Intrastat-kladden. Du kan angive, at transaktioner kun overføres, når varerne opfylder en eller flere af følgende kriterier:
<ul>
<li>Varerne er ikke serviceartikler.</li>
<li>Varerne har en varekode.</li>
<li>Varerne har en vægt.</li>
<li>Varerne har supplerende enheder.</li>
</ul></li>
<li><strong>Kontrollér opsætning</strong> – Angiv regler for validering af fuldstændigheden af Intrastat-data. Du kan vælge, hvilke data der skal valideres.</li>
<li><strong>Regler for afrunding</strong> – Angiv følgende indstillinger for afrunding af beløb og vægt i Intrastat-rapportering:
<ul>
<li>Afrundingsreglen (præcision)</li>
<li>Afrundingsmetoden: op, ned eller normal</li>
<li>Antallet af decimaler for beløb og vægt</li>
<li>Instruktioner for afrunding af vægt, der er mindre end 1 kilogram (kg): op til 1 kg, normal eller ingen afrunding</li>
</ul></li>
<li><strong>Elektronisk rapportering</strong> – Angiv referencer til elektronisk rapportering af konfigurationer, så du kan generere en elektronisk fil og rapport.</li>
<li><strong>Varekodehierarki</strong> – Angiv kategorihierarkiet af typen <strong>Varekode</strong>, der repræsenterer Intrastat-varekoder CN8.</li>
  <li> <strong>Valutakurstype</strong> – Du kan også angive en valutakurs, der skal bruges til at rapportere Intrastat-salgs- og købstransaktioner i fremmed valuta. Dette bruges, hvis valutakursen er anderledes end den, der blev anvendt, da posten blev bogført.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Kontaktoplysninger for agent</td>
<td>Angiv agentens navn, adresse, momsundtagelsesnummer, telefonnummer og faxnummer.</td>
</tr>
<tr class="odd">
<td>Egenskaber for land/område</td>
<td>Angiv landet/området for den aktuelle juridiske enhed til <strong>Indland</strong>. Angiv land/område i EU-lande/områder, der deltager i EU-handel med den aktuelle juridiske enhed til <strong>EU</strong>. For hvert land/område kan du også identificere lande-/områdekoden for formål med udenrigshandel.</td>
</tr>
<tr class="even">
<td>Nummerserie</td>
<td>Angiv nummerserien for Intrastat-kladden.</td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]