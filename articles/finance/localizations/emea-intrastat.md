---
title: Intrastat-oversigt
description: Denne artikel indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9360f97506ac7bdf67bb2f1b296f01b6ed49b39f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894774"
---
# <a name="intrastat-overview"></a>Intrastat-oversigt

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU. Denne artikel indeholder også en oversigt over rapporteringsprocessen og beskriver de nødvendige indstillinger og forudsætninger.

Intrastat er det system, der bruges til indsamling af oplysninger og generering af statistik over varehandel blandt lande/områder i EU. Intrastat-rapportering er påkrævet, når et produkt krydser grænsen til et andet EU-land/område. I nogle lande/områder gælder Intrastat-rapportering også for tjenester. Obligatoriske og fakultative elementer kan indsamles i Intrastat-rapportering. Følgende elementer er obligatoriske: momsnr. på den part, der er ansvarlig for at levere oplysninger, referenceperioden, strømmen (modtagelse eller forsendelse), den ottecifrede varekode, partnerens medlemsstat (afsendelsesmedlemsstaten på modtagelser) og bestemmelsesmedlemsstaten for forsendelser, varernes værdi, mængden af varer (nettomasse og supplerende enheder) og transaktionens art. Lande/regioner kan også indsamle valgfrie elementer i forskellige situationer. Nogle valgfrie elementer er land/region, leveringsbetingelserne, transportmåden, en mere detaljeret varekode end CN8, oprindelsesområdet for forsendelser og destinationsområdet for modtagelser, den statistiske procedure, den statistiske værdi, en beskrivelse af varerne og havn/lufthavn for lastning/losning.

## <a name="overview-of-the-intrastat-reporting-process"></a>Oversigt over Intrastat-rapporteringsprocessen
I følgende afsnit beskrives den samlede strøm af oplysninger, der bruges til Intrastat-rapportering.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Angiv en transaktion, der krydser grænsen til et andet EU-land/område

En debitorfaktura, fritekstfaktura, indkøbsordrefaktura, projektfaktura, følgeseddel for kunden og leverandørens produktkvittering eller overflytningsordre overføres til Intrastat-kladden, hvis landetypen for destination (på udførsel) eller forsendelse (på indførsel) er **EU**. Denne funktion blev udvidet til Microsoft Dynamics 365 for Operations (1611) og gør det muligt at angive fragtadresser for en transaktion inden for Fællesskabet. Hvis en fragtadresse afviger fra en leverandørs virksomhedsadresse (eller kundes virksomhedsadresse for returordre), bruges Intrastat-rapporteringen med disse oplysninger. Når du opretter en salgsordre, fritekstfaktura, indkøbsordre, kreditorfaktura, projektfaktura eller overflytningsordre, har nogle felter, der er relateret til udenrigshandel, standardværdier i dokumentets sidehoved eller på linjen. Standardkoden for transaktionen er taget fra det tilsvarende felt på siden **Udenrigshandelsparametre**. Standarden for varekode, oprindelsesland/-område og oprindelsesstat tages fra varen. Du kan ændre standardværdierne, og du kan også udfylde andre udenlandske handelsrelaterede oplysninger: den statistiske procedure, transportmåde og havn.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Brug denne Intrastat-kladde til at generere oplysninger om handel mellem lande/områder i EU

Til statistiske formål kan du generere oplysninger om handel mellem EU-lande/områder hver måned. Du kan overføre posteringer fra en fritekstfaktura, debitorfaktura, debitors følgeseddel, kreditorfaktura, kreditor følgeseddel, projektfaktura eller overflytningsordre, på grundlag af kriterier for overførsel, der er angivet på siden **Udenrigshandelsparametre**. Du kan også angive transaktioner manuelt. Du kan manuelt opdatere overførte transaktioner i Intrastat-kladden, hvis opdateringer er påkrævet. Under bestemte betingelser, der er angivet på siden **Komprimering af Intrastat**, kan du komprimere transaktionerne i Intrastat-kladden. For nogle lande/områder kan du anvende en tærskel på små transaktioner. Du kan rapportere transaktioner, der ligger under tærsklen, under den angivne varekode. Du kan opdatere varekoden på de tilsvarende Intrastat-kladdelinjer, baseret på indstillingen **Minimumsgrænse** på siden **Udenrigshandelsparametre**. Du kan også komprimere de transaktioner, der er baseret på indstillingen **Komprimering af Intrastat**. Du kan validere fuldstændigheden af transaktioner i Intrastat-kladden, baseret på indstillingen **Kontroller opsætning** på siden **Udenrigshandelsparametre**. Dataene i de tilsvarende felter kan valideres for nøjagtighed: land/område, stat eller region, vægt, varekode, transaktionskode, supplerende enhed, havn, oprindelse, vilkår for levering, transportmåde og momsundtagelsesnummer. Transaktioner, der ikke er fuldført, markeres som ikke gyldig.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Brug denne Intrastat-kladde til at rapportere oplysninger om handel mellem lande/områder i EU

Til statistiske formål kan du rapportere oplysninger om handel mellem EU-lande/områder hver måned. Du kan udskrive Intrastat-rapporten, baseret på indstillingen **Rapportformattilknytning** på siden **Udenrigshandelsparametre**. Du kan generere en elektronisk fil, baseret på indstillingen **Filformattilknytning** på siden **Udenrigshandelsparametre**. Se Opgaveregistrering for Intrastat-rapportering for at få yderligere oplysninger om Intrastat-rapportering, herunder de nødvendige forudsætninger.

  - Generere en EU Intrastat-opgørelse
  - Overføre transaktioner til Intrastat
  - Angiv fragtadresse for en transaktion inden for EU.

## <a name="prerequisites"></a>Forudsætninger
Tabellen nedenfor viser kravene til Intrastat-rapportering.

|  Forudsætning  |  Beskrivelse  |
|-------------------------|-------------------------|
| Adresseopsætning | Angiv ISO-koderne for lande/områder. |
| Juridisk enhed | Angiv momsfritagelsesnumre til import og eksport, afdelingens lokalnummer til import/eksport og den Intrastat-kode, der er tilknyttet den juridiske enhed. |
| Produktkategorihierarki (salgshierarki, indkøbshierarki) | Tildel Intrastat-varekoder til kategorinoder på fanen **Varekoder** på siden **Kategorihierarki**. Når du tildeler en varekode til en overordnet kategorinode, er den pågældende kode gældende for alle underordnede kategorinoder. De valgte varekoder bliver tilgængelig i visningen **Valgte**, når du vælger en varekode i produktdetaljer og på linjer for salgsordre, indkøbsordre og overførselsordre. |
| Frigivne produktdetaljer | Opret følgende udenrigshandelsdata for frigivne produkter:<ul><li>**Varekode** – Vælg enten en liste over valgte varer, der er hentet fra tildelte produktkategorier, eller den komplette liste over Intrastat-varekoder.</li><li>**Statistiske gebyrer i procent**</li><li>**Oprindelsesland/-område** – Vælg det standardland/-område, hvor varerne blev helt fremstillet eller produceret.</li><li>**Område for oprindelse/destination** – Vælg standardområdet for destinationen for modtagelser og stat/provins for afsendelser.</li><li>**Nettovægt i kg**</li><li>**Udelad** - Aktivér denne parameter for ikke at overføre transaktioner med dette produkt til Intrastat</li></ul> |
| Debitorer | Angiv kundens leveringsadresse i EU-landet. |
| Kreditorer | Angiv leverandørens adresse i EU-landet. |
| Tillæg | Angiv den tillægskode, der skal medtages i fakturabeløbet, statistiske beløb eller begge. På siden **Gebyrkoder** på fanen **Udenrigshandel** skal du aktivere **Intrastat-fakturaværdi** for at inkludere tillægsbeløbet i fakturaværdien og aktivere **Værdi af Intrastat-statistik** for at inkludere tillægsbeløbet i den statistiske værdi.</br>Du kan få flere oplysninger ved at gennemse eksemplet [Transaktionskoder og diverse gebyrer](#transaction-codes-and-miscellaneous-charges). |
| Elektronisk rapportering | Angiv elektronisk rapportering af konfigurationer for at eksportere Intrastat-data i en elektronisk fil, der har det format, der er anmodet om af de relevante myndigheder, og se Intrastat-data i et brugervenligt, læsbart format (for eksempel i Microsoft Excel). |
| Lagersted | Tilknyt kreditorkonti til lagerstedskoder til udfyldning af SE-nummer ved overførsel af flytteordre.</br>Du kan få flere oplysninger ved at gennemse eksemplet [Flytteordre](#transfer-order).|

## <a name="setup"></a>Konfiguration
I følgende afsnit beskrives de indstillinger, der skal bruges til Intrastat-rapportering.

### <a name="set-up-all-required-intrastat-related-lists"></a>Konfigurer alle nødvendige Intrastat-relaterede lister

|   Liste   |   Flere oplysninger   |
|-------------------------|-------------------------|
| Varekoder | Opret et kategorihierarki af typen **Varekode**, og angiv alle varekoder i henhold til den kombinerede nomenklatur-liste. For hver enkelt vare kan du angive følgende oplysninger:<ul><li>Navnet på varen og varekoden.</li><li>Det brugervenlige navn og/eller det oversatte navn</li><li>Indstillinger for rapportering af yderligere (supplerende) enheder under fanen **Udenrigshandel**. Du kan vælge den ekstra enhed på enhedslisten. Du kan også angive, om vægten af varer skal rapporteres sammen med den valgte ekstra enhed.</li></ul>Du kan få flere oplysninger ved at gennemse eksemplet [Supplerende enheder](#additional-units).|
| Transaktionskategorier | Angiv arten af transaktionen i henhold til dit lands/områdes krav. For hver transaktionskode, du har angivet, skal du angive regler for beregning af fakturabeløb og statistiske beløb for overførselsordrer og salgs-/købsordrer.<ul><li>For overførselsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:<ul><li>**Tom** – beløbet vil være 0 (nul).</li><li>**Økonomisk kostbeløb** – beløbet er lig med omkostningerne.</li><li>**Samlede omkostninger** – beløbet er lig med den samlede kostpris for transaktionen.</li><li>**Manuel** – beløbet er lig med det beløb, der angives manuelt på overførselsforslagslinjen.</li></ul></li><li>For salgsordrer og indkøbsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:<ul><li>**Tom** – beløbet vil være 0 (nul).</li><li>**Fakturabeløb** – beløbet er lig med det beløb, der er faktureret for varen.</li><li>**Grundbeløb** – beløbet, der er lig med det beløb, der skal faktureres, før nogen rabat.</li></ul></ul>Du kan få flere oplysninger ved at gennemse eksemplet [Transaktionskoder og diverse gebyrer](#transaction-codes-and-miscellaneous-charges). |
| Transportmåder | Angiv transportmåden i henhold til dit lands/områdes krav. For hver leveringsmåde kan du konfigurere en standardtransportmåde på fanen **Udenrigshandel**. |
| Havne | Angiv havn/lufthavn for lastning/losning, hvis disse oplysninger er indsamlet af dit land/område. |
| Statistiske procedurer | Angiv den statistiske procedure, hvis disse oplysninger er indsamlet af dit land/område. |



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
<li>Standardværdien transaktionskoder for salgsordrer, indkøbsordrer, kreditnotaer og overførselsordrer. Den transaktionskode, der er oprettet for kreditnotaer, bruges også som kode for fysisk returnerede varer og bruges til afvigende fysiske returneringer kontra korrektionskreditnotaer. Returneringer af fysiske varer rapporteres i Intrastat-overførsel med en anden retning. Modtagelsesreturen rapporteres som ekspedition, og afsendelsen rapporteres som modtagelse.</li>
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

## <a name="example"></a>Eksempel

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a>Transaktionskoder og diverse gebyrer

Denne artikel omhandler et scenario, hvor et firma i Tyskland skal købe varer fra et firma i Italien. For at kunne foretage dette køb skal det tyske firma oprette nye transaktionskoder og konfigurere beregningsregler for fakturabeløbet og det statistiske beløb for disse transaktionskoder. Når firmaet opretter en faktura, skal det desuden angive diverse gebyrer og deres procentsatser. Disse værdier tages i betragtning, når den statistiske værdi beregnes.

I scenariet bruges den juridiske enhed **DEMF**.

#### <a name="preliminary-setup"></a>Foreløbig opsætning

1. Gå til **Organisationsadministration** > **Organisation** > **Juridiske enheder**, og vælg **DEMF**.
2. Angiv feltet **Land/område** til **DEU Tyskland** i oversigtspanelet **Adresser**.
3. Gå til **Kreditor** > **Kreditorer** > **Alle kreditorer**.
4. Vælg **DE-001** i gitteret.
5. Vælg **Rediger** i oversigtspanelet **Adresse**.
6. Vælg **ITA** i feltet **Land/område** i dialogboksen **Rediger adresse**.
7. Vælg **OK** for at lukke dialogboksen.

#### <a name="set-up-transaction-codes"></a>Konfigurer transaktionskoder

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transaktionskoder**.
2. Vælg **11** i gitteret. Vælg derefter **Slet** i handlingsruden.
3. Gå til handlingsruden, og vælg **Ny**.
4. Angiv **11** i feltet **Transaktion** **kode** i oversigtspanelet **Transaktionskoder**.
5. Angiv **Direkte køb/salg** i feltet **Navn**.
6. Vælg **Fakturabeløb** i feltet **Fakturabeløb** under **Salg og køb**.
7. Vælg **Fakturabeløb** i feltet **Statistisk beløb**.
8. Vælg **Gem** i handlingsruden.

#### <a name="set-up-miscellaneous-charges"></a>Konfigurere diverse gebyrer

1. Gå til **Kreditor** > **Konfiguration af gebyrer** > **Gebyrkode**.
2. Vælg **Fragt** i gitteret.
3. Vælg **Rediger** i handlingsruden.
4. Angiv indstillingerne for **Intrastat-fakturaværdi** og **Intrastat-statistikværdi** til **Ja** i oversigtspanelet **Udenrigshandel**.

#### <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
2. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
3. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.

#### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Kreditor** > **Indkøbsordrer** > **Alle indkøbsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret indkøbsordre**, og vælg **DE-001** i feltet **Kreditorkonto**.
4. Vælg **OK**.
5. På fanen **Hoved** i oversigtspanelet **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **11**.
6. Vælg **D0003** i feltet **Varenummer** i oversigtspanelet **Indkøbsordrelinjer** under fanen **Linjer**. Angiv derefter **10** i feltet **Antal**.
7. I oversigtspanelet **Linjedetaljer** skal du under fanen **Udenrigshandel** kontrollere, at feltet **Transaktionskode** er angivet automatisk i sektionen **Udenrigshandel**.
8. I menuen **Finans** i oversigtspanelet **Indkøbsordrelinjer** skal du i sektionen **Gebyrer** vælge **Vedligehold gebyrer**.
9. Vælg **FRAGT** i feltet **Gebyrkode**.
10. Angiv **30** i feltet **Gebyrværdi**.
11. Vælg **Gem** i handlingsruden. Luk derefter siden.
12. Vælg **Bekræft** i gruppen **Handlinger** under fanen **Indkøb** i handlingsruden.
13. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
14. Vælg **Standard fra** i handlingsruden. Vælg **Bestilt antal** i feltet **Standardmængde for linjer**. Vælg derefter **OK**.
15. Angiv **00100** i feltet **Nummer** i sektionen **Fakturaidentifikation** i oversigtspanelet **Kreditorfakturahoved**.
16. Vælg **11/24/2021** (24. november 2021) i feltet **Fakturadato** i sektionen **Fakturadatoer**.
17. Vælg **Bogfør** i handlingsruden for at bogføre kladden.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Overføre kreditorfakturaen til Intrastat-kladden

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Kreditorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden.

   ![Linje, der repræsenterer indkøbsordren med diverse gebyrer på siden Intrastat](media/intrastat_overview_1.png)

5. Gennemse fanen **Generelt** for indkøbsordren. Bemærk, at feltet **Fakturaværdi** viser summen af felterne **Fakturabeløb** og **Fakturagebyrbeløb**, og at feltet **Statistisk værdi** viser summen af felterne **Statistisk beløb** og **Statistisk gebyrbeløb**.

   ![Detaljer om indkøbsordre med diverse gebyrer under fanen Generelt på Intrastat-siden](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Overførselsordre

I dette eksempel skal et firma i Tyskland fragte to vareenheder fra et lagersted i Tyskland til et lagersted i Italien. Der skal også angives gebyrer med en sats på 20 procent for dette produkt til regnskabet i feltet **Statistisk værdi**. I eksemplet bruges den juridiske enhed **DEMF**.

#### <a name="preliminary-setup"></a>Foreløbig opsætning

1. Gå til **Organisationsadministration** > **Organisation** > **Juridiske enheder**, og vælg **DEMF**.
2. Angiv feltet **Land/område** til **DEU Tyskland** i oversigtspanelet **Adresser**.
3. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
4. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
5. Gå til **Kreditor** > **Kreditorer** > **Alle kreditorer**.
6. Vælg **DE-001** i gitteret.
7. Vælg **Rediger** i oversigtspanelet **Adresse**.
8. Vælg **ITA** i feltet **Land/område** i dialogboksen **Rediger adresse**.
9. Vælg **OK** for at lukke dialogboksen.

#### <a name="set-up-transaction-codes"></a>Konfigurer transaktionskoder

1. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Transaktionskoder**.
2. Vælg **11** i gitteret. Vælg derefter **Slet** i handlingsruden.
3. Gå til handlingsruden, og vælg **Ny**.
4. Angiv **11** i feltet **Transaktion** **kode** i oversigtspanelet **Transaktionskoder**.
5. Angiv **Direkte køb/salg** i feltet **Navn**.
6. Vælg **Totalomkostning** i feltet **Fakturabeløb** i sektionen **Flytteordre**.
7. Vælg **Totalomkostning** i feltet **Statistisk beløb**.
8. Vælg **Gem** i handlingsruden.
9. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
10. Vælg **11** i feltet **Flytteordre** i oversigtspanelet **Generelt** under fanen **Intrastat**.

#### <a name="set-up-charges-for-an-item"></a>Konfigurere gebyrer for en vare

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
2. Vælg **D0001** i gitteret.
3. Angiv **20** i feltet **Gebyrprocent** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.

#### <a name="change-the-site-address"></a>Ændre adressen for webstedet

1. Gå til **Lagerstedsstyring** > **Konfiguration** > **Lagersted** > **Steder**.
2. Vælg **1** i gitteret.
3. Vælg **Rediger** i oversigtspanelet **Adresser**.
4. Vælg **DEU** i feltet **Land/område** i dialogboksen **Rediger adresse**.
5. Vælg **OK**.
6. Vælg **2** i gitteret.
7. Vælg **Rediger** i oversigtspanelet **Adresser**.
8. Vælg **ITA** i feltet **Land/område** i dialogboksen **Rediger adresse**.
9. Vælg **OK**.
10. Gå til **Lokationsstyring** > **Konfiguration** > **Lagersted** > **Lagersteder**.
11. Vælg **21** i gitteret.
12. Vælg **DE-001** i feltet **Kreditorkonto** i sektionen **Reference** i oversigtspanelet **Generelt**.

#### <a name="create-a-transfer-order"></a>Oprette en flytteordre

1. Gå til **Lagerstyring** > **Udgående ordrer** > **Flytteordre**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Under fanen **Linjer** i oversigtspanelet **Flytteordrehoved** i sektionen **Oversigt** skal du i feltet **Fra lagersted** vælge **11**. Vælg **21** i feltet **Til lagersted**.
4. Vælg **Tilføj** i oversigtspanelet **Flytteordrelinjer** under fanen **Linjer**.
5. Vælg **D0001** i feltet **Varenummer**. Angiv derefter **2** i feltet **Overfør antal**.
6. I oversigtspanelet **Linjedetaljer** skal du under fanen **Udenrigshandel** kontrollere, at feltet **Transaktionskode** er angivet automatisk i sektionen **Udenrigshandel**.
7. Vælg **Forsendelsesflytteordre** i gruppen **Handlinger** under fanen **Send** i handlingsruden.
8. I dialogboksen **Forsendelse** under fanen **Oversigt** skal du i feltet **Opdater** vælge **Alle**.
9. Vælg **OK** for at sende ordren.
10. I handlingsruden skal du vælge **Modtag** i gruppen **Handlinger** under fanen **Modtag**.
11. I dialogboksen **Modtag** under fanen **Oversigt** skal du i feltet **Opdater** vælge **Alle**.
12. Vælg **OK** for at sende ordren.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Overføre flytteordren til Intrastat-kladden

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Flytteordre** til **Ja** og alle andre indstillinger til **Nej** i dialogboksen **Intrastat (overførsel)**.
4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden.

   ![Linje, der repræsenterer flytteordren på siden Intrastat](media/intrastat_overview_3.png)

5.  Gennemse fanen **Generelt** for flytteordren.

    Bemærk, at felterne i områderne **Fakturaværdi** og **Statistik værdi** angives automatisk. Værdierne af felterne **Fakturabeløb** og **Statistisk beløb** er baseret på indstillingerne på siden **Transaktionskoder**. Værdien **20** i feltet **Gebyrprocent** er den værdi, der er angivet på siden **Frigivet produkt**. Værdien i feltet **Statistiske gebyrbeløb** er et kvantitativt udtryk for gebyrer (fordi 107,24 er lig med 20 procent af 536,18). Værdien af feltet **Statistik værdi** er summen af værdier fra felterne **Statistisk beløb** og **Statistik gebyrbeløb**.

  ![Detaljer om flytteordre under fanen Generelt på Intrastat-siden](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Supplerende enheder

I dette eksempel skal et firma i Tyskland købe 10 vareenheder fra et firma i Italien. Ud over varekoder skal der angives supplerende enheder for de pågældende varer. Eksemplet viser, hvordan du opretter nye måleenheder, tildeler supplerende enheder til Intrastat-varekoden, bogfører posteringer, der har supplerende enheder, og gennemgår Intrastat-kladden, hvor feltet til de supplerende enheder er angivet.

#### <a name="preliminary-setup"></a>Foreløbig opsætning

1. Gå til **Organisationsadministration** > **Organisation** > **Juridiske enheder**, og vælg **DEMF**.
2. Angiv feltet **Land/område** til **DEU Tyskland** i oversigtspanelet **Adresser**.
3. Gå til **Moms** > **Opsætning** > **Udenrigshandel** > **Udenrigshandelsparametre**.
4. Vælg **11** i feltet **Transaktionskode** i oversigtspanelet **Generelt** under fanen **Intrastat**.
5. Sørg for, at **Intrastat** er valgt i feltet **Kategorihierarki** i oversigtspanelet **Varekodehierarki**.
6. Gå til **Kreditor** > **Kreditorer** > **Alle kreditorer**.
7. Vælg **DE-001** i gitteret.
8. Vælg **Rediger** i oversigtspanelet **Adresse**.
9. Vælg **ITA** i feltet **Land/område** i dialogboksen **Rediger adresse**.
10. Vælg **OK** for at lukke dialogboksen.

#### <a name="create-a-unit-of-measure"></a>Opret en måleenhed

1. Gå til **Organisationsadministration** > **Konfiguration** > **Enheder** > **Enheder**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv et navn til måleenheden i feltet **Enhed**. I dette eksempel skal du angive **GRM**.
4. Vælg den egenskab, som måleenheden skal måle, i feltet **Enhedsklasse** i sektionen **Klassifikation** i oversigtspanelet **Generelt**. I dette eksempel skal du vælge **Masse**.
5. Vælg det målesystem, som enheden tilhører, i feltet **Enhedssystem**. Vælg f.eks. **Metriske enheder**.

#### <a name="set-up-unit-conversions"></a>Konfigurere enhedsomregninger

1. Gå til **Organisationsadministration** > **Konfiguration** > **Enheder** > **Enhedsomregninger**.
2. Vælg **Ny** under fanen **Konverteringer mellem klasser**.
3. Vælg **F00007** i feltet **Produkt** i dialogboksen **Enhedsomregning**.
4. Vælg **hver** i feltet **Fra enhed**.
5. Vælg **GRM** i feltet **Til enhed**.
6. Kontrollér, at omregningsfaktoren er **1 = 1**.
7. Vælg **OK**.
8. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
9. Vælg **F00007** i gitteret.
10. Vælg **GRM** i feltet **Enhed** i sektionen **Lager** i oversigtspanelet **Styr lager**.
11. Vælg **Gem** i handlingsruden.

#### <a name="set-up-product-information"></a>Angive produktoplysninger

1. Gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter**.
2. Vælg **F00007** i gitteret.
3. Vælg **920 20 34** i feltet **Vare** i sektionen **Intrastat** i oversigtspanelet **Udenrigshandel**.
4. Vælg **Gem** i handlingsruden.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Tildele den ekstra enhed til en Intrastat-varekode

1. Gå til **Administration af produktoplysninger** > **Opsætning** > **Kategorier og attributter** > **Kategorihierarkier**.
2. Vælg **Intrastat** på listen.
3. Vælg **Speaker** i gitteret.
4. Vælg **GRM** i feltet **Supplerende enheder** i oversigtspanelet **Udenrigshandel**.
5. Vælg **Gem** i handlingsruden.

   Du kan finde flere oplysninger i [Administrere måleenheder](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Kreditor** > **Indkøbsordrer** > **Alle indkøbsordrer**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Gå til dialogboksen **Opret indkøbsordre**, og vælg **DE-001** i feltet **Kreditorkonto**.
4. Vælg **OK**.
5. På fanen **Hoved** i oversigtspanelet **Udenrigshandel** skal du kontrollere, at feltet **Transaktionskode** er angivet til **11**.
6. Vælg **F00007** i feltet **Varenummer** i oversigtspanelet **Indkøbsordrelinjer** under fanen **Linjer**. Angiv derefter **10** i feltet **Antal**.
7. I oversigtspanelet **Linjedetaljer** skal du under fanen **Udenrigshandel** kontrollere, at felterne **Transaktionskode** og **Vare** er angivet automatisk i sektionen **Udenrigshandel**.
8. Vælg **Bekræft** i gruppen **Handlinger** under fanen **Indkøb** i handlingsruden.
9. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
10. Vælg **Standard fra** i handlingsruden. Vælg **Bestilt antal** i feltet **Standardmængde for linjer**. Vælg derefter **OK**.
11. Angiv **VE-0010** i feltet **Nummer** i sektionen **Fakturaidentifikation** i oversigtspanelet **Kreditorfakturahoved**.
12. Vælg **10/5/2021** (5. oktober 2021) i feltet **Fakturadato** i sektionen **Fakturadatoer**.
13. Vælg **Bogfør** i handlingsruden for at bogføre kladden.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Overføre kreditorfakturaen til Intrastat-kladden

1. Gå til **Moms** > **Erklæringer** > **Udenrigshandel** > **Intrastat**.
2. Vælg **Overfør** i handlingsruden.
3. Angiv indstillingen **Kreditorfaktura** til **Ja** i dialogboksen **Intrastat (Overførsel)**.
4. Vælg **OK** for at overføre transaktionerne og gennemse Intrastat-kladden.

   ![Linje, der repræsenterer indkøbsordren på siden Intrastat](media/intrastat_overview_5.png)

5. Gennemse fanen **Generelt** for indkøbsordren. Bemærk, at felterne **Antal supplerende enheder** og **Supplerende enhed** i sektionen **Enhed** angives automatisk.

   ![Detaljer om indkøbsordre under fanen Generelt på Intrastat-siden](media/intrastat_overview_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
