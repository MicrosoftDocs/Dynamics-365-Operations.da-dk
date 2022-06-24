---
title: Bogføring af indkøbsordre
description: Denne artikel beskriver fanen Indkøbsordre på siden Lagerbogføringsprofiler.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 0793c58b07d2c0a133e1a5bc0607483f22206b95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849925"
---
# <a name="purchase-order-posting"></a>Bogføring af indkøbsordre

Fanen **Indkøbsordre** på siden **Lagerposteringsprofiler** bruges til at styre, hvordan indkøbsordrer bogføres i finansmodulet. To hovedaktiviteter bogføres i finansmodulet for en indkøbsordre: 

- Produktkvittering
- Faktura

Hvis en fysisk transaktion (produktkvittering) skal bogføres i finansmodulet for en indkøbsordre, skal følgende afkrydsningsfelter være markeret:

- Afkrydsningsfeltet **Bogfør produktkvittering i finans** på siden **Parametre til lager- og lokationsstyring**.
- Afkrydsningsfelterne **Bogfør fysisk lager** og **Periodiser passiver ved produktmodtagelse** på siden **Varemodelgrupper**.

På siden **Lagerposteringsprofil** skal der være angivet hovedkonti for følgende posteringstyper:

- Omkostning til købte materialer, der er modtaget
- Udgifter til indkøb, ikke-faktureret
- Indkøb, periodisering

Hvis en økonomisk transaktion (faktira) skal bogføres i finansmodulet på en indkøbsordre, skal følgende betingelser være opfyldt:

- På siden **Varemodelgrupper** skal afkrydsningsfeltet **Bogfør økonomisk lager** være markeret for den vare, der er valgt på indkøbsordrelinjen.
- På siden **Lagerposteringsprofil** skal der være angivet hovedkonti for følgende posteringstyper:
  - Omkostning til købte materialer, der er faktureret
  - Udgifter til indkøb for produkt
  - Udgifter til indkøb for udgift
  - Rabat (valgfrit)

## <a name="fixed-receipt-price-posting"></a>Bogføring af fast tilgangspris

Du kan bruge den faste tilgangspris som standardomkostning for et produkt som et alternativ til at vælge indstillingen **Standardomkostning** i feltet **Lagermodel** på **Varemodelgrupper**-siden for en vare. Den væsentligste forskel er, at når du bruger **Fast tilgangspris**, bliver den aktuelle kostpris brugt for varen, når tilgangen til lageret bogføres. Der findes ingen værdireguleringsproces for **Fast tilgangspris**. Når der bogføres en økonomisk opdatering, bruges den aktuelle kostpris på bogføringstidspunktet. Hvis der er forskel melem den kostpris, der bruges ved tilgangen, og fakturaen, bogføres afvigelsen på driftskontiene for den faste tilgangspris.

Hvis du vil bruge en fast tilgangspris for et produkt, skal du konfigurere følgende:

- Markér afkrydsningsfelterne **Bogfør fysisk lager** og **Fast tilgangspris** på siden **Varemodelgrupper**. 
- På siden **Parametre til lager- og lokationsstyring** skal afkrydsningsfeltet **Bogfør følgeseddel i finans** være markeret.
- På siden **Lagerposteringsprofil** skal du angive hovedkonti for følgende posteringstyper:
  - Vind ved fast tilgangspris
  - Tab ved fast tilgangspris
  - Modposteret fast tilgangspris

Du kan finde flere oplysninger under [Fast tilgangspris](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Indkøbsgebyrer og bogføring af lagerafvigelse

Hvis du planlægger at tage højde for indkøbsgebyrer og lagervariationer, skal du gøre følgende:

- Markér afkrydsningsfeltet **Bogfør på omkostningskontoen i finans** under fanen **Faktura** på siden **Kreditorparametre**.
- På siden **Varemodelgrupper** for den vare, der er valgt på indkøbsordrelinjen, skal du markere afkrydsningsfelterne **Bogfør fysisk lager**, **Bogfør økonomisk lager** og **Periodiser passiver ved produktmodtagelse**.
- Markér afkrydsningsfeltet **Generér gebyrer på produktkvittering** på siden **Indkøbs- og forsyningsparametre**.
- På siden **Parametre til lager- og lokationsstyring** skal afkrydsningsfeltet **Bogfør følgeseddel i finans** være markeret.

På siden **Lagerposteringsprofil** skal du angive hovedkonti for følgende posteringstyper:

- Udgifter til indkøb, ikke-faktureret
- Udgifter til indkøb for produkt
- Lagerafvigelse

> [!NOTE]
> Posteringstypen **Gebyr** bruges ikke, når parameteren **Bogfør på omkostningskontoen i finans** er valgt.

Du kan finde flere oplysninger under [Regnskabsprincippet for bogføring på omkostningskonto](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfiguration af posteringsprofil

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser:

- I kolonnen **Clearingkonto** angives, at bogføringstypen er en clearingkonto. Det beløb, der bogføres på denne konto, tilbageføres automatisk, når en senere transaktion bogføres. 
- I **P/F**-kolonnen angives **P** til fysisk bogføring og **F** til økonomisk bogføring. 
- Kolonnen **Følg** angiver, om hovedkontoen for en bestemt bogføringstype typisk er den samme som en anden bogføringstype. Værdien i kolonnen angiver den bogføringstype, der typisk anvendes.

> [!NOTE]
> Disse hovedkonti og hovedkontonavne er kun forslag. Vi anbefaler<!--note from editor: Via Writing Style Guide.--> at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.


| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Omkostning til købte materialer, der er modtaget | 140100</br>140101 | Materialelager</br>Materialer, der er afsendt, ikke faktureret | Aktiv | Debet | Ja | P | Omkostning til købte materialer, der er faktureret | Bruges, når produktkvitteringen bogføres for en indkøbsordre. Modkontoen er Udgifter til indkøb, ikke-faktureret. Beløbet på denne konto tilbageføres, når der bogføres en indkøbsordrefaktura. |
| Udgifter til indkøb, ikke-faktureret | 600180 | Materialetilgange | Udgift | Debet | Ja | P | |Bruges, når produktkvitteringen bogføres for en indkøbsordre. Der oprettes to bilag til tilgangen for at spore afvigelser i indkøbsprisen, når standardomkostningen bruges. Modkontoen på det første bilag er Indkøb, periodisering. Modkontoen på det andet bilag er summen af kontiene Omkostning til købte materialer, der er modtaget og Afvigelse i købspris. De beløb, der bogføres på denne konto, tilbageføres, når der bogføres en indkøbsordrefaktura. |
| Omkostning til købte materialer, der er faktureret | 140100 | Materialelager | Aktiv | Debet | Nej | F  |Omkostning til købte materialer, der er modtaget | Bruges, når fakturaen for en indkøbsordre bogføres. Modkontoen til denne konto er Udgifter til indkøb for produkt. Denne konto repræsenterer lageret i balancen. Den anvendte konto er typisk den samme konto, som bruges til Omkostninger ved leverede enheder og Omkostninger ved fakturerede enheder for salgsordren. |
| Udgifter til indkøb for produkt | 600180 | Materialetilgang | Udgift | Kredit | Nej | F  | |Bruges, når fakturaen for en indkøbsordre bogføres. Modkontoe til denne konto er Omkostning til købte materialer. Denne konto repræsenterer lageret i balancen. |
| Vind ved fast tilgangspris (Indkøb, vind ved fast tilgangspris*) | 510310 | Afvigelse i købspris | Udgift | Kredit | Nej | F | Tab ved fast tilgangspris | Bruges, når en indkøbsordrefaktura bogføres, og der er forskel mellem den fakturerede pris og standardomkostningen for varen. Denne konto bruges, når forskellen er større. Modkontoen til denne konto er Modposteret fast tilgangspris. |
| Tab ved fast tilgangspris (Indkøb, tab ved fast tilgangspris*) | 510310 | Afvigelse i købspris | Udgift | Debet | Nej | F | Vind ved fast tilgangspris | Bruges, når en indkøbsordrefaktura bogføres, og der er forskel mellem den fakturerede pris og standardomkostningen for varen. Denne konto bruges, når forskellen er lavere. Modkontoen til denne konto er Modposteret fast tilgangspris. |
| Modposteret fast tilgangspris (Indkøb, modposteret fast tilgangspris*) | 140900 | Lagerafvigelse | Aktiv | Begge | Nej | F  | |Bruges, når en indkøbsordrefaktura bogføres, og der er forskel mellem den fakturerede pris og standardomkostningen for varen. Denne konto er modkontoen til driftskontiene for den faste tilgangspris. |
| Gebyr | IT | IT | IT | IT | IT | IT | IT | Denne konto bruges ikke længere. Brug i stedet Lagerafvigelse. |
| Lagerafvigelse | 600170 | Lagerafvigelse | Udgift | Kredit | Nej | Begge | | Denne konto bruges, når: <ul><li>Der er forskel på enhedsprisen mellem produktkvittering og faktura.</li><li>Gebyrer bogføres på varen.</li><li>Indirekte omkostninger er blevet<!--note from editor: Edit okay?--> føjet til de købte varer. </li><li>Modkontoen til denne konto er Udgifter til indkøb, ikke-faktureret.</li></ul> |
| Indkøb, periodisering | 200140 | Periodiserede køb | Passiv | Kredit | Y | P | |Bruges, når en produktkvittering for en indkøbsordre bogføres, og indstillingen til periodisering af købsbeløb er aktiveret. |
| Periodiseret moms af tilgang | 250500 | Periodiseret moms | Passiv | Kredit | Y | Begge  | |Denne konto bruges, når du vælger indstillingen **Bogfør fysisk moms** i **Parametre til lager- og lokationsstyring**, og du har en indkøbsordre med moms. Beløbet bogføres, når du opdaterer indkøbsordren fysisk (produktkvittering), og tilbageføres, når du bogfører indkøbsordren økonomisk (faktura). |
| Kvittering for anlægsaktiv (Anlægsaktiv, debet*) | 180100 | Materielle anlægsaktiver | Aktiv | Debet | N | Begge | Begge | Denne konto bruges, når du vælger indstillingen på indkøbsordrelinjen for Anlægsaktiver. Indkøbsordreintegrationen er konfigureret til at anskaffe anlægsaktivet efter produktkvittering eller faktura. Du kan få flere oplysninger om integration af indkøbsordrer for anlægsaktiver ved at gå til [Anskaffe aktiver via indkøb](/fixed-assets/acquire-assets-procurement). |
| Udgifter til indkøb for udgift | 618900 | Diverse udgifter | Udgift | Debet | N | Begge | |Bruges, når du bogfører en produktkvittering eller faktura for en indkøbsordre, hvor varerne ikke er på lager, eller der bruges en indkøbskategori. |
| Forudbetaling | 132190 | Forudbetalte udgifter | Aktiv | Debet | N | Begge | | Bruges ved behandling af en forudbetalingsfaktura på en indkøbsordre. |


\*Værdier, der står i parentes, repræsenterer den værdi, der bruges i feltet **Bogføringstype** på siden **Poster på bilag**. Du kan se **Bogføringstype** på siden **Poster på bilag** under fanen **Generelt**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Bogføre anlægsaktiver med indkøbsordrer

Hvis du bruger modulet **Anlægsaktiver** og planlægger at købe anlægsaktiver via indkøbsordrer, skal du konfigurere bogførringstypen **Kvittering for anlægsaktiv** under fanen **Indkøbsordre** på siden **Lagerposteringsprofil**. Du kan få flere oplysninger ved at gå til [Integration af anlægsaktiver](/fixed-assets/fixed-asset-integration.md) og [Oprette og anskaffe aktiver fra Kreditor](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Bogføring af faktura til forudbetaling i indkøbsordrer

Hvis du planlægger at bruge funktionen **Faktura til forudbetaling** til indkøbsordrer, skal bogføringstypen **Forudbetaling** være valgt under fanen **Indkøbsordre** på siden **Lagerposteringsprofil**. Du kan få flere oplysninger under [Forudbetalingsfakturaer vs. forudbetalinger](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Bogføring af indkøbsrekvisition og indkøbsordrebekræftelse

Indkøbsrekvisitioner og indkøbsordrebekræftelser kan også konfigureres til at bogføre budgetreservationer og behæftelser i finansmodulet. Disse bogføringer styres af en bogføringsdefinition. Du kan finde flere oplysninger under [Om indkøbsordrebehæftelse](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Bogføring af indkøbskategori

Som et alternativ til at konfigurere lagerbogføring for alle varer, en gruppe varer eller en enkelt vare kan du oprette kategorier og styre finansbogføringen efter indkøbskategorier. Du kan finde flere oplysninger om, hvordan du konfigurerer kategorier og tildeler dem produkter, ved at gå til [Konfiguration af eksempel på posteringsprofil](#sample-posting-profile-configuration) tidligere i denne artikel.

Når du bruger kategorier sammen med indkøbsordrer eller kreditorfakturaer, skal kategorihierarkiet tildeles typen **Indkøbskategorihierarki** på siden **Tildelinger af kategorihierarkirolle**.

### <a name="vendor-invoices-with-procurement-categories"></a>Kreditorfakturaer med indkøbskategorier

Hvis din organisation bruger indkøbsordrer til nogle indkøb og ikke til andre, kan du behandle fakturaer, der ikke er indkøbsordrerelaterede, på mange forskellige måder. Det omfatter brug af kladder i **Kreditor** eller på siden **Ventende kreditorfakturaer**, der bruges til at generere fakturaer for indkøbsordrer. Når du opretter fakturaer for fakturaer, der ikke er indkøbsordrerelaterede, skal du oprette indkøbskategorier for hver udgiftstype. Du skal knytte kategorien til den korrekte udgiftskonto på siden **Lagerposteringsprofiler**.

Det nøjagtige antal kategorier varierer, afhængigt af antallet af udgiftskonti, du bruger til at bogføre fakturaerne. Du skal bruge mindst én indkøbskategori for hver af de hovedkonti, hvor du udgiftsfører fakturaer, som ikke er til indkøbsordrer. Mange kategorier kan bruges til en enkelt hovedkonto. Dette kan være nyttigt for anvendelighed, søgbarhed og rapportering af de typer udgifter, du bruger.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Fordele ved at bruge indkøbskategorier til kreditorfakturaer

Nogle fordele ved at bruge indkøbskategorier til kreditorfakturaer omfatter:

- Gennemført brugeroplevelse: Når du konfigurerer indkøbskategorier for alle udgifter, der ikke vedrører indkøbsordrer, kan brugerne oplæres i bare én faktureringsproces ved at bruge siden **Ventende kreditorfakturaer**.
- Forbedret rapporteringsoplevelse: Når du konfigurerer indkøbskategorier for alle varer og alle udgifter, der ikke er indkøbsordrerelaterede, analyserer rapporten om indkøbsforbrug udgifterne efter leverandør, kategori og andet.
- Ensartet arbejdsgang: Når du bruger **Ventende kreditorfakturaer** til at behandle alle fakturaer, kan du oprette en gennemført arbejdsproces og godkendelsesproces ved hjælp af en enkelt arbejdsproces.

## <a name="consignment-inventory-posting"></a>Bogføring af konsignationslager

Konsignationslager bruger samme finanskontering som andre købte varer. Den væsentligste forskel er, at der ikke registreres finanstransaktioner ved modtagelse af lageret. Hvis du vil overføre ejerskabet til organisationen, når der bogføres en kladde for **Ændring af beholdningsejerskab**, oprettes der et bilag til registrering af varens omkostning. Du kan finde flere oplysninger under [Konfigurere konsignation](/supply-chain/inventory/consignment.md).
