---
title: Rapportering til EU-listesystemet
description: Denne artikel indeholder oplysninger om rapportering til EU-listesystemet.
author: EvgenyPopovMBS
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dfd3fafdfc011973b169516cd4e2d239751e96d
ms.sourcegitcommit: f5b156f2e5ca99ad05b3d6e4a5d118631fd3064e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2022
ms.locfileid: "9012494"
---
# <a name="eu-sales-list-reporting"></a>Rapportering til EU-listesystemet

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om rapportering til EU-listesystemet.

## <a name="eu-sales-list-reporting"></a>Rapportering til EU-listesystemet

En leverandør, der inden for fællesskabet leverer varer eller tjenesteydelser til virksomheder, der er etableret inden for den Europæiske Union (EU), skal indsende en erklæring om fællesskabsleveringer (EU-listesystemet eller ESL). Generelt skal ESL sendes til skattemyndigheder senest den sidste dag i måneden efter den kalenderperiode, der dækker ESL. Leverandøren skal angive sit momsidentifikationsnummer på ESL'en og skal også angive, efter debitor, følgende oplysninger:

-   EU-kundens momsidentifikationsnummer
-   Den samlede fælleskabsleveringen af varer og tjenesteydelser, der er foretaget til EU-debitoren i den pågældende periode. Leverandøren skal desuden adskille generelle leveringer af varer fra trekantshandelsleveringer. En trekantshandelstransaktion omfatter direkte levering af varer fra leverandørens leverandøren til debitoren, når begge parter er registreret i andre medlemsstater i EU.

Ved hjælp af ESL kan skattemyndighederne i hver EU-medlemsstat kontrollere, om der er betalt moms for hver transaktion inden for fællesskabet. Kombinationen af lister og momsopgørelserne giver EU-medlemsstater mulighed for at udveksle oplysninger om gennemstrømningen af varer i hele EU.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Oversigt over rapporteringsprocessen i forbindelse med EU-listesystemet
Du kan udføre følgende opgaver for rapportering i forbindelse med EU-listesystemet:

-   Indsaml oplysninger om handelstransaktioner inden for fællesskabet. En handelstransaktion inden for fælleskabet kan være en salgsfaktura, fritekstfaktura, projektfaktura eller kreditorfaktura. En transaktion er identificeret ud fra modpartens land/område. Handelstransaktioner inden for fællesskabet af forskellige typer indsamles i EU-listesystemet, hvor de er repræsenteret i den almindelige form. Hver post i ESL-tabellen repræsenterer en enkelt transaktion og består af modpartens moms-id og den samlede værdi af varer og tjenesteydelser, der blev leveret.
-   (Valgfrit) Se en forhåndsvisning af rapporten **EU-listesystemet**. Du kan gennemse og godkende rapporten **EU-listesystemet** for en given periode i form af en Microsoft Excel-projektmappe.
-   Generer rapporten **EU-listesystemet**. Rapporten **EU-listesystemet** genereres i form af en elektronisk fil med et bestemt format, der er specifik for hver EU-medlemsstat. Generelt indeholder en rapport for **EU-listesystemet** grundlæggende oplysninger om den rapporterende part og værdierne for levering af varer og tjenesteydelser. Oplysningerne er grupperet efter modpartens land/område og moms-id.
-   Luk EU-listesystemets rapporteringsperiode. Når rapporten **EU-listesystemet** er genereret og sendt til myndigheder, kan du markere posterne i ESL-tabellen som **Lukket**. Disse posteringer medtages ikke i flere rapporter.

## <a name="prerequisites"></a>Forudsætninger
Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategori</th>
<th>Forudsætning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Opsætning:</strong> Juridisk enhed</td>
<td>Den primære adresse for den juridiske skal enhed være i et EU-medlemsland. På siden <strong>Juridiske enheder</strong> (klik på <strong>Virksomhedsadministration</strong> &gt; <strong>Organisationer</strong> &gt; <strong>Juridiske enheder</strong>) skal du vælge din juridiske enhed. I oversigtspanelet <strong>Adresser</strong> skal du oprette en adresse, vælge et land/område og andre adressekomponenterne og markere adressen som <strong>Primær</strong>. I oversigtspanelet <strong>Momsregistrering</strong> skal du i feltet <strong>SE-nummer</strong> angive firmaets SE-nummer.</td>
</tr>
<tr class="even">
<td><strong>Opsætning:</strong> Identifikationsparametre for SE-nummer</td>
<td>Konfigurer identifikationsparametre for SE-nummer på siden <strong>Lande/områdeparametre</strong> (klik på <strong>Moms</strong> &gt; <strong>Opsætning</strong> &gt; <strong>Moms</strong> &gt; <strong>Lande/områdeparametre</strong>). For hvert land/område, hvor du har modparter, skal du oprette en post på siden og angive følgende oplysninger:
<ul>
<li><strong>Land/område</strong> – Vælg et land/område, der skal knyttes til en SE-nummeridentifikation.</li>
<li><strong>Moms</strong> – Angiv SE-nummeridentifikationen (dvs. momsregistreringsnummerets eller SE-nummerets præfiks) for det valgte land/område.</li>
<li><strong>Kontroller SE-nummer</strong> – Markér dette afkrydsningsfelt for at validere SE-nummeridentifikationen for det valgte land/område.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Konfiguration:</strong> Momsregistreringsnumre</td>
<td>Opret momsregistreringsoplysninger for dine modparter på siden <strong>Alle debitorer</strong> (gå til <strong>Salg og marketing</strong> &gt; <strong>Debitorer</strong> &gt; <strong>Alle debitorer</strong>, vælg en kundepost, og vælg derefter <strong>Debitorer</strong> &gt; <strong>Registrerings-id'er</strong>) eller siden <strong>Kreditorer</strong> (gå til <strong>Indkøb og forsyning</strong> &gt; <strong>Kreditorer</strong> &gt; <strong>Kreditorer</strong>, vælg en kreditorpost, og vælg derefter <strong>Kreditorer</strong> &gt; <strong>Registrerings-id'er</strong>). Opret en post i oversigtspanelet <strong>Registrerings-id</strong> under fanen <strong>Generelt</strong>, og angiv følgende oplysninger:
<ul>
<li><strong>Registreringstype</strong> – Vælg den registreringstype, der er tildelt registreringskategorien <strong>Moms-id</strong> for modpartens land/område.</li>
<li><strong>Registreringsnummer</strong> – Angiv modpartens momsregistreringsnummer.</li>
<li><strong>Gyldig fra</strong> – Vælg starten af brugsperioden for momsregistreringsnummeret.</li>
</ul>  
Du kan også oprette et momsregistreringsnummer for dine modparter på siden <strong>SE-numre</strong> (gå til <strong>Moms</strong> &gt; <strong>Konfiguration</strong> &gt; <strong>Moms</strong> &gt; <strong>SE-numre</strong>). Opret en post på siden for hvert SE-nummer, og angiv følgende oplysninger:
<ul>
<li><strong>Land/område </strong>– Vælg landet/området for momsregistrering af modparten.</li>
<li><strong>SE-nummer</strong> – Angiv modpartens SE-nummer.</li>
<li><strong>Firmanavn</strong> – (Valgfrit) Angiv navnet på modpartens navn.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Opsætning: </strong>Momsregistrering af modparter</td>
<td>Konfigurer momsregistreringsoplysninger for dine modparter enten på siden <strong>Alle debitorer</strong> (klik på <strong>Salg og marketing</strong> &gt; <strong>Debitorer</strong> &gt; <strong>Alle debitorer</strong>, vælg en kundepost, og klik derefter på <strong>Indstillinger</strong> &gt; <strong>Skift visning</strong> &gt; <strong>Detaljeret visning</strong>) eller på siden <strong>Kreditorer</strong> (klik på <strong>Indkøb og forsyning</strong> &gt; <strong>Kreditorer</strong> &gt; <strong>Kreditorer</strong>, vælg en kreditorpost, og klik derefter på <strong>Indstillinger</strong> &gt; <strong>Skift visning</strong> &gt; <strong>Detaljeret visning</strong>). I oversigtspanelet <strong>Faktura og levering</strong> i feltet <strong>SE-nummer</strong> skal du vælge momsregistreringsnummeret.</td>
</tr>
<tr class="odd">
<td><strong>Opsætning: </strong>Moms</td>
<td>Konfigurer momskoderne, der skal medtages i rapporten <strong>EU-listesystemet</strong> på siden <strong>Momskoder</strong> (klik på <strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momskoder</strong>). I oversigtspanelet <strong>Rapportopsætning</strong> skal du fjerne markeringen i afkrydsningsfeltet <strong>Udelukket </strong>for hver momskode, der skal medtages i rapporten. Konfigurer momsparametre for varer på siden <strong>Varemomsgrupper</strong> (klik på <strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Varemomsgrupper</strong>). Vælg en værdi i feltet <strong>Rapporteringstype</strong> for hver varemomsgruppe. Den værdi, du vælger, bestemmer den ESL-beløbskolonne, som linjebeløbet skal medtages i.
<ul>
<li><strong>Tom</strong> – Linjebeløbet medtages i kolonnen <strong>Værdi for ikke-tildelt</strong>.</li>
<li><strong>Vare</strong> – Linjebeløbet medtages i kolonnen <strong>Værdi for varer</strong> .</li>
<li><strong>Tjeneste</strong> – Linjebeløbet medtages i kolonnen <strong>Værdi for tjenester</strong> .</li>
<li><strong>Investering</strong> – Linjebeløbet medtages i kolonnen <strong>Værdi for investeringer</strong> . Denne kolonne er kun relevant for Belgien.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Opsætning:</strong> ESL-rapporteringskonfigurationer</td>
<td>Importer eller opret elektroniske rapporteringskonfigurationer for ESL. Se dokumentationen for Elektronisk rapportering for at finde oplysninger om, hvordan du kan oprette og vedligeholde elektroniske rapporteringskonfigurationer.</td>
</tr>
<tr class="odd">
<td><strong>Opsætning: </strong>Generelle parametre</td>
<td>Konfigurer ESL-rapporteringsparametre på siden <strong>Udenrigshandelsparametre</strong> (klik på <strong>Moms</strong> &gt; <strong>Opsætning</strong> &gt; <strong>Udenrigshandel</strong> &gt; <strong>Udenrigshandelsparametre</strong>). Angiv følgende parametre:
<ul>
<li>Fanen <strong>EU-listesystem</strong>:
<ul>
<li><strong>Indberet kasserabat</strong> – Markér dette afkrydsningsfelt, hvis der skal medtages kasserabat i værdien, når en transaktion er medtaget på ESL.</li>
<li><strong>Overfør køb</strong> – Markér dette afkrydsningsfelt for at medtage køb på ESL.</li>
<li><strong>Filformattilknytning</strong> – Vælg formatet for elektronisk indberetning til brug, når der oprettes en elektronisk fil for ESL.</li>
<li><strong>Rapportformattilknytning</strong> – Vælg formatet for elektronisk indberetning til brug, når der oprettes en forhåndsvist rapport for ESL.</li>
<li><strong>Afrundingsregel</strong> – Angiv et reelt tal, der skal bruges til afrunding. ESL-beløb afrundes til multipler af dette tal.</li>
<li><strong>Afrundingsmetode</strong> – Vælg den afrundingsmetode, der skal bruges, når ESL-beløb afrundes (<strong>Normal</strong>, <strong>Nedad</strong> eller <strong>Oprunding</strong>).</li>
<li><strong>Brug minimumværdi</strong> – Markér dette afkrydsningsfelt, hvis du vil have beløb, der er mindre end tallet for <strong>Afrundingsreglen</strong>, skal rundes oprundes til tallet for <strong>Afrundingsreglen</strong>.</li>
<li><strong>Antallet af decimaler,</strong> – Angiv antallet decimaler, der vises i ESL-beløb (både i elektroniske filer og i rapporten <strong>ESL-forhåndsvisning</strong> ).</li>
</ul></li>
<li>Fanen <strong>Lande/områdeparametre</strong>: Identificer EU-medlemsstater. Opret en post på siden for hver EU-medlemsstat, og angiv følgende oplysninger:
<ul>
<li><strong>Land/område</strong> – Vælg et land/område.</li>
<li><strong>Lande-/regionstype</strong> – Hvis værdien <strong>Land/område</strong> er det land/område, firmaet er registreret i, skal du vælge <strong>Indland</strong>. Hvis værdien <strong>Land/område</strong> er en anden EU-medlemsstat end det land/område, firmaet er registreret i, skal du vælge <strong>EU</strong>. Hvis værdien <strong>Land/område</strong> er ikke en EU-medlemsstat, skal du vælge <strong>Tredjeland/-region</strong>.</li>
</ul></li>
<li>Fanen <strong>Nummerserier</strong>: På linjen, hvor værdien <strong>Reference</strong> er <strong>EU-listesystemet</strong>, skal du vælge en nummerseriekode.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Relaterede transaktioner</strong></td>
<td><ul>
<li>Registrer et salg til en debitor i en anden EU-medlemsstat.</li>
<li>Registrer en fritekstfaktura for en debitor i en anden EU-medlemsstat.</li>
<li>Registrer en projektfaktura for en kunde i en anden EU-medlemsstat.</li>
<li>Registrer en faktura fra en kreditor i en anden EU-medlemsstat.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Arbejde med ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Indsamle oplysninger om handelstransaktioner inden for fællesskabet

Transaktioner af følgende typer kan anses for handel inden for Fællesskabet:

-   Salgsfakturaer
-   Fritekstfakturaer
-   Projektfakturaer
-   Kreditorfakturaer

En transaktion anses en transaktion inden for fællesskabet, hvis leveringsadressen for transaktionen er i en medlemsstat i EU. For disse lande/områder bør der være en post på fanen **Lande/områdeparametre** på siden **Udenrigshandelsparametre**, og værdien **Lande-/områdetype** skal indstilles til **EU**. Handel inden for fællesskabet er markeret i feltet **Listekode**. Du kan også bruge dette felt til at adskille generelle handler inden for fælleskabet fra trekantshandelstransaktioner. Du kan indsamle oplysninger om handel inden for fællesskabet på siden **EU-listesystemet** (klik på **Moms** &gt; **Erklæringer** &gt; **Udenrigshandel** &gt; **EU-listesystemet**) ved hjælp af funktionen **Overførsel**. Denne funktion giver mulighed for at medtage transaktioner, der har beløb af forskellige rapporteringstyper (dvs., varer eller tjenesteydelser) i henhold til de varemomsgrupper, der er angivet på transaktionslinjer. Du kan også anvende andre filtre til at definere de transaktioner, der skal medtages. Funktionen **Overførsel** opretter en post på siden **EU-listesystemet** for hver transaktion inden for fællesskabet, der er inkluderet, og angiver en modparts kontonummer, et land/område, et SE-nummer, et fakturanummer og dato og det samlede beløb af linjer pr. rapporteringstype. Den kopierer også værdien **Listekode** fra transaktionen. Du kan manuelt ændre listekoden for en transaktion på siden **EU-listesystemet**. Funktionen **Overførsel** opretter poster, hvor værdien **Rapporteringsstatus** er angivet til **Medtaget**. Du kan kontrollere de oplysninger, der er indsamlet på siden **EU-listesystemet** ved hjælp af funktionen **Valider**. Du kan få detaljerede oplysninger om fakturaen (for salgsretningen) ved at bruge funktionen **Totaler**.

### <a name="generating-the-eu-sales-list-report"></a>Generere EU-listesystemet-rapporten

Du kan generere en **EU-listesystemet**-rapport ved hjælp af funktionen **Rapportering** på siden **EU-listesystemet**. Funktionen giver dig mulighed for at vælge en rapporteringsperiode og anvende filtre for at definere ESL-poster, der skal medtages. Derudover kan du angive andre parametre, der er specifikke for hvert land/område. Du kan også vælge at oprette en rapportforhåndsvisning, en elektronisk fil eller begge dele. Funktionen **Rapportering** bruger rapport- og filformatindstillingerne, der er angivet på siden **Udenrigshandelsparametre**. Generelt består en **EU-listesystemet**-rapport af separate linjer, der viser det samlede beløb af forsyninger pr. modparts land/område, SE-nummer og rapporteringstype (trekantshandelstransaktioner medtages). Når du genererer en **EU-listesystemet**-rapport for en bestemt periode, kan du markere ESL-poster, der medtages i rapporten, ved at angive værdien for **Rapporteringsstatus** til **Rapporteret**. Du kan angive denne status ved at bruge funktionen **Marker som rapporteret** på siden **EU-listesystemet**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>Lukke EU-listesystemets rapporteringsperiode

Når du har fuldført rapporteringsprocessen for en bestemt periode (f.eks. når skattemyndighederne har accepteret **EU-listesystemet** -rapporten), kan du markere ESL-poster, der er medtaget i rapporten for perioden, ved at angive **Rapporteringsstatus**-værdien til **Lukket**. Du kan angive denne status ved at bruge funktionen **Marker som lukket** på siden **EU-listesystemet**. Hvis du tilbagefører lukningen af perioden, kan du markere ESL-poster ved at angive **Rapporteringsstatus**-værdien til **Medtaget**. Disse poster kan derefter medtages i en **EU-listesystemet**-rapport igen. Du kan angive denne status ved at bruge funktionen **Marker som** **medtages** på siden **EU-listesystemet**.

## <a name="list-of-country-specific-topics"></a>Liste over landespecifikke emner

| Land/område          | Link      |
|------------------|-----------|
| Østrig          | [EU-listesystem for Østrig](emea-aut-eu-sales-list.md)| 
| Belgien          |[EU-listesystem for Belgien](emea-bel-eu-sales-list.md)|
| Tjekkiet          |[EU-listesystem for Tjekkiet](emea-cze-eu-sales-list.md)|
| Danmark          |[EU-listesystem for Danmark](emea-dnk-eu-sales-list.md)|
| Estland          |[EU-listesystem for Estland](emea-est-eu-sales-list.md)|
| Finland          |[EU-listesystem for Finland](emea-fin-eu-sales-list.md)|
| Frankrig          |[EU-listesystem for Frankrig](emea-fra-eu-sales-list.md)|
| Tyskland          |[EU-listesystem for Tyskland](emea-deu-eu-sales-list.md)|
| Ungarn          |[EU-listesystem for Ungarn](emea-hun-eu-sales-list.md)|
| Letland          |[EU-listesystem for Letland](emea-lva-eu-sales-list.md)|
| Litauen          |[EU-listesystem for Litauen](emea-ltu-eu-sales-list.md)|
| Nederlandene          |[EU-listesystem for Nederlandene](emea-nl-eu-sales-list.md)|
| Polen          |[EU-listesystem for Polen](emea-pol-eu-sales-list.md)|
| Spanien          |[EU-listesystem for Spanien (rapport 349)](emea-esp-sales-list.md)|
| Sverige          |[EU-listesystem for Sverige](emea-swe-eu-sales-list.md)|
| Storbritannien (Nordirland)          |[EU-listesystem for Storbritannien (Nordirland)](emea-uk-eu-sales-list.md)|


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
