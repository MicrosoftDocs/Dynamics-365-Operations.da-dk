---
title: "Oversigt over SEPA-pengeoverførsel"
description: "Denne artikel indeholder generelle oplysninger om ISO 20022-kreditoverførsler, som omfatter SEPA-kreditoverførsler (Single Euro Payments Area) og andre elektroniske betalinger til kreditorer. En SEPA-kreditoverførsel er en specifik type betaling i euro fra én virksomhed eller enkeltperson til en anden virksomhed eller enkeltperson. Denne artikel beskriver også, hvordan du kan oprette og sende en betalingsfil til kreditoverførsel."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1aa70dea3b0e7056afbdba96f4475c3e7e71f57c
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="sepa-credit-transfer-overview"></a>Oversigt over SEPA-pengeoverførsel

[!include [banner](../includes/banner.md)]

Denne artikel indeholder generelle oplysninger om ISO 20022-kreditoverførsler, som omfatter SEPA-kreditoverførsler (Single Euro Payments Area) og andre elektroniske betalinger til kreditorer. En SEPA-kreditoverførsel er en specifik type betaling i euro fra én virksomhed eller enkeltperson til en anden virksomhed eller enkeltperson. Denne artikel beskriver også, hvordan du kan oprette og sende en betalingsfil til kreditoverførsel.

## <a name="what-is-a-credit-transfer-message"></a>Hvad er en kreditoverførselsmeddelelse?
Kreditoverførselsmeddelelsen er en anmodning, som en initierende part (din virksomhed) sender for at flytte midler fra sin egen konto til en kreditor. Der er mange lande-/områdespecifikke og bankspecifikke implementeringer af kreditoverførselsmeddelelser. Nogle af dem der anvendes inden for ét land/område, og nogle er ved at blive standarder. Én veletableret global standard er ISO 20022 og dens initieringsmeddelelser, f.eks. som kreditoverførsel. I følgende illustration vises forbindelserne og dækningen for udvalgte kreditoverførselsmeddelelser. 
![Kreditoverførsel](./media/credit-transfer.jpg) Kreditoverførselsmeddelelser 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hvad er ISO 20022 og SEPA-betalinger?
Det Fælles eurobetalingsområde (SEPA) er nedsat af Europa-Kommissionen og bestemmer, at alle elektroniske betalinger behandles som indenlandske, uanset det land/område, hvor personen, virksomheden eller organisationen og banken er placeret. Der er ingen forskel imellem nationale betalinger og betalinger, der involverer udlandet. SEPA omfatter de 28 EU-medlemsstater samt Island, Liechtenstein, Norge, Schweiz, Monaco og San Marino. SEPA er med til at danne et enkelt marked for betalingstransaktioner inden for Det Europæiske Økonomiske Samarbejdsområde (EEA). I sidste ende forventes SEPA at reducere antallet af betalingsformater, som banker, virksomheder og enkeltpersoner skal arbejde med. Europa-Kommissionen har fastlagt det juridiske grundlag for SEPA-betalinger via PSD (Payment Services Directive). EPC (European Payments Council) understøtter SEPA gennem følgende aktiviteter:

-   Det angiver standarder for elektroniske betalinger til SEPA ved hjælp af ISO 20022 Universal finansielle industri skema XML-meddelelsesformatet.
-   Det fastlægger regler og retningslinjer om håndtering af betalinger i euro.

EPC, som består af europæiske banker, udvikler de forretningsmæssige og tekniske rammer for SEPA-betalingsmidler. Der anvendes tre typer SEPA-betalinger:

-   Pengeoverførsler
-   Direkte debiteringer
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hvad er en SEPA-pengeoverførsel?
En SEPA-pengeoverførsel er en betaling fra en virksomhed eller et individ til et andet selskab eller et andet individ. Betalinger skal være i euro og skal indeholde IBAN (International Bank Account Number) og BIC (Bank Identifier Code) for begge parter. (BIC er også kendt som \[SWIFT\]-kode (Society for Worldwide Interbank Financial Telecommunication)). Transaktionsomkostninger skal desuden deles mellem begge parter. Pengeoverførsler, der foregår mellem parterne, skal bruge XML-filer, der er i overensstemmelse med ISO 20022 betalingsbehandlingsstandarder og XML-format, som angivet af EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvordan implementeres en kreditoverførsel?
Betalingsformatet for kreditoverførsel i de europæiske lande implementeres ved hjælp af den elektroniske rapportering (ER) og betalingsmetoderne i Microsoft Dynamics 365 for Finance and Operations. Nogle få kreditoverførselsformater, der bruges i andre områder, bruger stadig den ældre betalingsstruktur. Blandt mange andre formater er der tolv ISO 20022-filformater til kreditoverførsel, der er tilgængelige. Disse eksportformater er i overensstemmelse med SEPA ISO 20022 XML-standarden. De bruges til at generere ikke-euro betalingsoverførsler til lande/områder, hvor de bruges, og til euro-betalinger som angivet i version 8.2 af den SEPA Credit Transfer Scheme Rulebook, der udgives af EPC. Før du kan implementere kreditoverførsler, skal du kontakte din bank for at få den software, der kræves for at overføre elektroniske filer. Du skal bruge softwaren til at overføre de XML-filer, der indeholder betalingsordrer til banken.

## <a name="what-credit-transfer-formats-are-currently-supported-in-finance-and-operations"></a>Hvilke formater til kreditoverførsel understøttes i øjeblikket i Finance and Operations?
Du bør altid gå til den delte aktivbiblioteket på Microsoft Dynamics Lifecycle services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**. Næste afsnit, "Hvad skal jeg bruge for at komme i gang?", indeholder et link til det emne, der forklarer, hvordan du opretter en LCS-lager for at se tilgængelige konfigurationer og importere markerede konfigurationer.

## <a name="what-do-i-have-to-set-up"></a>Hvad skal jeg bruge for at komme i gang?
-   Før du kan oprette kreditoverførselsfiler, skal mindst én aktiv konfiguration af kreditoverførsel importeres til dine ER-konfigurationer. Du kan finde vejledning i [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Når du konfigurerer betalingsmetoder for kreditor, skal du markere afkrydsningsfeltet **Generiske elektronisk rapportering** og vælge det relevante kreditoverførselsformat (f.eks. **ISO 20022-kreditoverførsel (AT)**) som en formatkonfiguration til eksport.
-   Du skal også angive den juridiske enhed og bankkontooplysninger i Finance and Operations.
-   Bankkontonumre, IBAN og undertiden SWIFT-koder (BIC) eller andre id'er, der er nødvendige for at oprette gyldige betalinger ved kreditoverførsel. Derfor, du skal angive dem for kreditorbankkontoen og bankkontoen for den organisation, der anmoder om overførslen.
-   Yderligere oplysninger kan være påkrævet, f.eks. momsnumre for de parter, der er refereret til kreditoverførselsmeddelelsen. Disse oplysninger skal konfigureres for kreditorer og for den juridiske enhed, når der anmodes om det.
-   Nogle betalingsmetoder for kreditorer, hovedsagelig ISO 20022-baserede betalingsmåder, kræver muligvis yderligere opsætning af **betalingsformatkodesæt**, f.eks. **Servicetype** = **SLEV**. Disse koder bruges som ekstra kodning af betalingstransaktioner under behandlingen af betalingen. Standardværdier af betalingskoder, f.eks. **Kategoriformål**, **Bærer af gebyrer**, **Lokalt betalingsmiddel** og **Serviceniveau** kan indstilles på to steder. Det første sted er **hovedet på kreditorbetalingskladden**, og det andet er **betalingsmåder for kreditorbetaling**. Ved oprettelse af betalingskladdelinjer overføres betalingskodeværdier, der er angivet på betalingskladdehovedet, til en kladdelinje, hvis de ikke er angivet, bruges værdierne fra betalingsmåder.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvilke parametre er tilgængelige til oprettelse af betalinger ved kreditoverførsel?
Listen over bestemte parametre afhænger af kreditoverførselsformatet. I nedenstående tabel vises de parametre, der er tilgængelige, når du genererer en betalingsfil til ISO 20022-kreditoverførsel til Tyskland i en kreditorbetalingskladde. Ved hjælp af de indstillinger, der er tilgængelige under fanen **Kør i baggrunden** kan du køre betalingsgenerering i batchtilstand.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Batchbooking</td>
<td>Markér dette afkrydsningsfelt for at medtage batch reservationskode i XML-filen.</td>
</tr>
<tr class="even">
<td>Afviklingsdato</td>
<td>Angiv den dato, hvor banken skal behandle betalinger.</td>
</tr>
<tr class="odd">
<td>Format</td>
<td>Vælg formater for remitteringsoplysninger, afhængigt af kravene i dit land eller din bank:
<ul>
<li><strong>Strd</strong> – Vælg denne indstilling for at bruge det strukturerede format, når en betalingslinje udlignes med en faktura. Denne indstilling er ikke tilgængelig for lande-/områdespecifikke eksportformater for Frankrig, Tyskland eller Nederlandene.</li>
<li><strong>Ustrd</strong> – Vælg denne indstilling for at bruge det ustrukturerede format, når betalingen udlignes med flere fakturaer. Fakturanumre for de udlignede fakturaer er sammenføjet og bruges som remitteringsoplysningerne. I overensstemmelse med retningslinjerne for ISO 20022 er ustrukturerede remitteringsoplysninger begrænset til 140 tegn.</li>
</ul></td>
</tr>
<tr class="even">
<td>Antal fakturaer</td>
<td>Angiv antallet af fakturaer, som rapporten <strong>Betalingsadvisering</strong> udskrives fra.</td>
</tr>
<tr class="odd">
<td>Løbenummer</td>
<td>Du kan angive et sekvensnummer for at finde filen. Sekvensnummeret vises på rapporten <strong>Følgeskrivelse</strong>.</td>
</tr>
<tr class="even">
<td>Udskriv følgeskrivelse</td>
<td>Markér dette afkrydsningsfelt for at udskrive rapporten <strong>Deltagernote</strong>.</td>
</tr>
<tr class="odd">
<td>Udskriv kontrolrapport</td>
<td>Markér dette afkrydsningsfelt for at udskrive en rapport, der indeholder betalingsoplysninger.</td>
</tr>
<tr class="even">
<td>Udskriv følgeskrivelse</td>
<td>Markér dette afkrydsningsfelt for at udskrive rapporten <strong>Betalingsadvisering</strong>.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Hvad er IBAN og BIC?
IBAN-numre og BIC-koder bruges til at identificere alle konti i mange lande/områder over hele verden. Disse omfatter de 34 SEPA-lande/områder. Angiv BIC i feltet **SWIFT-kode** og IBAN-nummeret i feltet **IBAN**. For både kreditors bankkonto og kundens bankkonto er disse felter placeret på oversigtspanelet **Yderligere identifikation** under fanen **Bankkonto** på siden **Bankkonti**. Brugen BIC-kode til SEPA-betalinger gennemtvinges ikke længere.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvordan kan jeg sende en betalingsfil til banken?
Når du genererer betalinger, bliver betalingsfilen genereret, og du bliver bedt om at gemme den på en tilgængelig placering fra din webbrowser. Næste trin er at sende XML-filen til din bank. Denne proces varierer fra bank til bank. Følg vejledningen fra din bank til at sende filer til banken til behandling.




