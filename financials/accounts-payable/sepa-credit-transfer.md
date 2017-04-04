---
title: "Oversigt over SEPA-pengeoverførsel"
description: "Denne artikel indeholder generelle oplysninger om ISO 20022 pengeoverførsler, som omfatter pengeoverførsler (enkelt Eurobetalingsområde) og andre elektroniske betalinger til kreditorer. En SEPA-overførslen er en bestemt type betaling i euro fra en virksomhed eller til individuelle til et andet selskab eller individuel. Emnet beskriver, hvordan du oprette og sende en betalingsfil til overførsel af kredit."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Oversigt over SEPA-pengeoverførsel

Denne artikel indeholder generelle oplysninger om ISO 20022 pengeoverførsler, som omfatter pengeoverførsler (enkelt Eurobetalingsområde) og andre elektroniske betalinger til kreditorer. En SEPA-overførslen er en bestemt type betaling i euro fra en virksomhed eller til individuelle til et andet selskab eller individuel. Emnet beskriver, hvordan du oprette og sende en betalingsfil til overførsel af kredit.

## <a name="what-is-a-credit-transfer-message"></a>Hvad er en meddelelse til overførsel af kredit?
Kredit overførsel meddelelse er en anmodning, der sender en starter part (virksomheden) til at flytte midler fra sin egen konto til en kreditor. Der er mange lande-/ regionsspecifikke og bank-specifikke implementeringer af pengeoverførsel meddelelser. Nogle af dem der anvendes inden for ét land, og nogle bliver standarder. En veletableret global standard er ISO 20022 og dens indledning meddelelser, f.eks. pengeoverførsel. I følgende illustration vises forbindelserne og dækning for valgte kredit overføre meddelelser. 
![Kreditering af overførslen](./media/credit-transfer.jpg) kredit overføre meddelelser\[/billedtekst\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hvad er ISO 20022 og SEPA-betalinger?
Det Fælles eurobetalingsområde (SEPA) er nedsat af Europa-Kommissionen og bestemmer, at alle elektroniske betalinger behandles som indenlandske, uanset det land/område, hvor personen, virksomheden eller organisationen og banken er placeret. Der er ingen forskel mellem nationale betalinger og grænseoverskridende betalinger. SEPA omfatter 28 medlemsstaterne af den Europæiske Union (EU), og også Island, Liechtenstein, Norge, Schweiz, Monaco og San Marino. SEPA er med til at danne et enkelt marked for betalingstransaktioner inden for Det Europæiske Økonomiske Samarbejdsområde (EEA). I sidste ende forventes SEPA at reducere antallet af betalingsformater, som banker, virksomheder og enkeltpersoner skal arbejde med. Europa-Kommissionen har fastlagt det juridiske grundlag for SEPA-betalinger via PSD (Payment Services Directive). EPC (European Payments Council) understøtter SEPA gennem følgende aktiviteter:

-   Det angiver standarder for elektroniske betalinger til SEPA ved hjælp af ISO 20022 Universal finansielle industri skema XML-meddelelsesformatet.
-   Det fastlægger regler og retningslinjer om håndtering af betalinger i euro.

EPC, som består af europæiske banker, udvikler de forretningsmæssige og tekniske rammer for SEPA-betalingsmidler. Der anvendes tre typer SEPA-betalinger:

-   Pengeoverførsler
-   Direkte debiteringer
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hvad er en SEPA-pengeoverførsel?
En SEPA-pengeoverførsel er en betaling fra en virksomhed eller et individ til et andet selskab eller et andet individ. Betalinger skal være i euro og skal indeholde IBAN (International Bank Account Number) og BIC (Bank Identifier Code) for begge parter. (BI er også kendt som Society for Worldwide interbankrente Financial Telecommunication \[SWIFT\] kode.) Transaktionsomkostninger skal desuden være delt mellem begge parter. Pengeoverførsler, der foregår mellem parterne, skal bruge XML-filer, der er i overensstemmelse med ISO 20022 betalingsbehandlingsstandarder og XML-format, som angivet af EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvordan implementeres en pengeoverførsel?
Kredit overførsel betalingsformater for europæiske lande er implementeret ved hjælp af elektronisk indberetning (ER) og metoder for betaling funktionalitet i Dynamics 365 for operationer. Et par kredit overførsel formater, der bruges i andre områder stadig bruge ældre betaling rammerne. Blandt mange andre formater er der tolv ISO 20022 kredit overførsel filformater, der er tilgængelige. Disse formater til eksport er i overensstemmelse med SEPA ISO 20022 XML-standarden. De bruges til at generere ikke euro betalingsoverførsler for lande/områder, hvor de bruges og euro betalinger som angivet i version 8.2 af SEPA kredit overføre ordning regelsættet, der udgives af EPC. Før du kan implementere pengeoverførsler, skal du kontakte din bank for at få software, der kræves for at sende elektroniske filer. Du skal bruge softwaren til at overføre XML-filer, der indeholder betalingsordrer til banken.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hvilke formater til overførsel af kredit understøttes i øjeblikket i Dynamics 365 for operationer?
Du bør altid gå til den delte aktivbiblioteket på Microsoft Dynamics levetidsservices (LCS) og få vist den seneste liste over tilgængelige filer, som har et anlæg type **TYSK konfiguration**. Næste afsnit, "Hvad skal jeg har konfigureret?", indeholder et link til det emne, der forklarer, hvordan du opretter en LCS-lageret for at se tilgængelige konfigurationer og importere markerede konfigurationer.

## <a name="what-do-i-have-to-set-up"></a>Hvad skal jeg bruge for at komme i gang?
-   Før du kan oprette pengeoverførsel filer, skal mindst én konfiguration til overførsel af aktive kredit importeres til ER-konfigurationer. Yderligere oplysninger finder du [hente elektronisk indberetning konfigurationer fra levetidsservices](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Når du konfigurerer konti skal betales betalingsmåder, vælge den **generiske elektronisk indberetning** afkrydsningsfeltet, og vælg formatet passende kredit overførsel (for eksempel **ISO 20022 pengeoverførsel (AT)**) som en eksport format-konfiguration.
-   Du skal også angive den juridiske enhed og bankkonto oplysninger i Dynamics 365 for operationer.
-   Bankkontonumre, IBANs og undertiden SWIFT koder (BICs) eller andre id'er, der er nødvendige for at oprette gyldige pengeoverførsel betalinger. Derfor, du skal angive dem til kreditorbankkonto og bankkontoen for den organisation, der anmoder om overførslen.
-   Yderligere oplysninger kan være påkrævet tal for moms (moms) for de parter, der er omhandlet i meddelelsen kredit overførsel. Disse oplysninger konfigureres for kreditorer og for den juridiske enhed, når der er anmodet om.
-   Nogle konti skal betales betalingsmåder, hovedsagelig ISO 20022-baserede betalingsmåder, kræver muligvis yderligere opsætning for **betaling formater kodesæt**, som **Service type** = **SLEV**. Disse koder bruges som ekstra kodning for betalingstransaktioner under behandling af debitorbetalinger. Standardværdier af koderne for betalingen, ligesom **kategori formål**, **gratis bæreren**, **lokale instrument** og **serviceniveau** kan indstilles på to steder. Det første sted er **konti kreditorbetaling kladdehovedet** og andet er **konti skal betales metoder til betalinger**. Ved oprettelse af betaling kladde linjer betaling kodeværdier på kladdehovedet til betaling er overført til en kladdelinje, hvis det ikke angives, bruges værdierne fra betalingsmåder.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvilke parametre er tilgængelige til at generere betalinger til overførsel af kredit?
Liste over bestemte parametre, afhænger af formatet kredit overførsel. I følgende tabel vises de parametre, der er tilgængelige, når du opretter en ISO 20022 betaling-overførselsfil for Tyskland i en kreditorbetalingskladde. Ved hjælp af de indstillinger, der er tilgængelige på den **køre i baggrunden,** under fanen kan du køre Betalingsgenerering i batch-tilstand.

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
<li><strong>Strd</strong> – Vælg denne indstilling for at bruge strukturerede format, når en betalingslinje udlignes med en faktura. Denne indstilling er ikke tilgængelig for lande-/ regionsspecifikke eksportformater for Frankrig, Tyskland eller Nederlandene.</li>
<li><strong>Ustrd</strong> – Vælg denne indstilling for at bruge det ustrukturerede format, når betalingen udlignes med flere fakturaer. Fakturanumre for de udlignede fakturaer er sammenføjet og bruges som remitteringsoplysningerne. I overensstemmelse med ISO 20022 retningslinjer, remittering ustrukturerede oplysninger er begrænset til 140 tegn.</li>
</ul></td>
</tr>
<tr class="even">
<td>Antal fakturaer</td>
<td>Angiv antallet af fakturaer, den <strong>betalingsadvisering</strong> rapport udskrives fra.</td>
</tr>
<tr class="odd">
<td>Løbenummer</td>
<td>Du kan angive et sekvensnummer for at finde filen. Sekvensnummeret vises på den <strong>deltager note</strong> rapport.</td>
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
International Bank Account (Iran) og bankens identifikationsnummer (BI) bruges til at identificere en konto i mange lande verden over. Disse omfatter 34 SEPA-lande/områder. Angiv BI i den **SWIFT-koden** felt og IBAN-NUMMER i den **IBAN** felt. For både kreditors bankkonto og kundens bankkonto disse felter er placeret på den **yderligere identifikation** oversigtspanelet på den **bankkonto** tab af den **bankkonti** side. Anvendelse af BIC-kode til SEPA-betalinger gennemtvinges ikke længere.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvordan kan jeg sende en betalingsfil til banken?
Når du genererer betalinger, da betalingsfilen er oprettet, og du bliver bedt om at gemme den på en tilgængelig placering fra din webbrowser. Næste trin er at sende XML-filen til din bank. Denne proces varierer fra bank til bank. Følg vejledningen fra din bank til at sende filer til banken til behandling.


