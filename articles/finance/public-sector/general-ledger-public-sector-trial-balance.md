---
title: Råbalance med detaljeret transaktionsrapport
description: I denne artikel beskrives standardrapporten til råbalancer. Her beskrives også de komponenter, der er knyttet til denne rapport, og hvordan du kan redigere rapporten, så den passer til virksomhedens behov.
author: TaylorVH
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.13
ms.search.industry: public sector
ms.openlocfilehash: 54bcfa1f3c55d485fa0f379584ad5057f6c6ccf8
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9572959"
---
# <a name="trial-balance-with-transactional-detail-report"></a>Råbalance med detaljeret transaktionsrapport

[!include [banner](../includes/banner.md)]

I denne artikel beskrives standardrapporten til råbalancer. Rapporten **Råbalance med transaktionsoplysninger** genererer en råbalance og indeholder de detaljerede transaktioner, der er bogført på hver finanskonto. Hvis du vælger at medtage bestemte ikke-bogførte transaktioner, kan du bruge rapporten til at oprette en foreløbig råbalance sammen med detaljerede transaktioner.

Elektronisk rapportering (ER) blev brugt til at oprette rapporten **Råbalance med transaktionsoplysninger**. Derfor kan en organisation enten bruge den version af rapporten, der er medtaget i det globale lager, eller oprette sin egen version af rapporten.

## <a name="er-setup"></a>ER-opsætning

Hvis du ikke har konfigureret det globale lager, skal du konfigurere det for den opdaterede version af rapporten **Råbalance med transaktionsoplysninger**. Du kan finde flere oplysninger i [Konfigurere det globale lager](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. Gå til **Elektronisk rapportering**.
2. Vælg **Lagre** for udbyderen **Microsoft**.
3. Vælg **Åbn**.
4. Rul ned, eller tilføj et filter for det konfigurationsnavn, der starter med **Prøveversion**.
5. Vælg **Råbalance med transaktionsoplysninger (Excel)**, og vælg derefter **Importér**. 

Du kan nu køre den opdaterede rapport, og resultaterne vil være tilgængelige i Microsoft Excel.

## <a name="feature-management"></a>Administration af funktioner

Rapporten **Råbalance med transaktionsoplysninger** aktiveres automatisk, når funktionen **Generér råbalance med transaktionsoplysninger** er aktiveret i **Funktionsstyring**. Hvis du vil medtage ikke-bogførte transaktioner i rapporten, skal du aktivere funktionen **Generér råbalance med ventende typetransaktioner**. Hvis du vil have vist oversigtsdata fra finanskontoposten, skal du aktivere funktionen **Beløbsdetaljer fra finanskontoposten vises på råbalancen med rapporten Råbalance med transaktionsoplysninger**.

## <a name="report-options"></a>Rapportindstillinger

Når du genererer rapporten, kan du medtage følgende detaljerede finanstransaktioner i den:

- Bogførte posteringer
- Ventende transaktioner
- Alle transaktioner

Når bogførte transaktioner medtages i rapporten, kan det medføre et stort sæt data.

Alle detaljerede finanstransaktioner i rapportens datointerval udskrives på rapporten. Derfor kan rapporten kun genereres for 31 dage eller derunder.

Hvis du medtager ventende transaktioner i rapporten, skal du vælge den type ikke-bogførte transaktionstyper, der skal medtages. Kun de ikke-bogførte transaktionstyper, der vises i rapportparametrene, kan medtages i den foreløbige rapport. Her er nogle af de ikke-bogførte transaktionstyper:

- Avancerede finansposter
- Fordelingskladder
- Budgetkladder
- Budgetposteringer
- Debitorbetalingskladder
- Kassekladder
- Fritekstfakturaer
- Projektfakturaer
- Indkøbsordrer
- Indkøbsrekvisitioner
- Kreditorfakturaer
- Kreditorfakturakladder
- Kreditorindgangsbogskladder

Ikke-bogførte interne transaktioner, der er angivet i finanskladden (kassekladde) eller kreditorfakturakladder, vises ikke i rapporten. De relevante "forfalden til" og "forfalden fra"-poster kan ikke genereres, før de bogføres. Hvis disse kontoposter ikke genereres, viser rapporten en uafstemt regnskabspost, da rapporten kun indeholder kontoposterne for den aktive juridiske enhed.

Indstillingen **Primært økonomisk dimensionssæt** definerer, hvordan transaktioner grupperes for kombinationer af hovedkonti og økonomiske dimensioner. Hvis du f.eks. vælger et dimensionssæt , der indeholder dimensionerne **Hovedkonto** og **Afdeling**, vil rapporten vise startsaldoen, detaljerede transaktioner og slutsaldoen for hver kombination af en hovedkontoværdi og en afdelingsværdi. Uanset hvilken økonomisk dimensionsopsætning der er valgt, vises hele finanskontoen i kontokolonnen **Finansdimension**.

Brug felterne **Fra dato** og **Til dato** til at definere et datointerval. Dette datointerval skal være 31 dage eller derunder. Denne begrænsning er på grund af det store antal transaktioner, der medtages i en detaljeret transaktionsrapport.

Vælg det posteringslag, du vil have vist de detaljerede transaktioner for, i feltet **Posteringslag**. Der kan kun vælges ét posteringslag.

Brug indstillingen **Medtag primobeløb for transaktion i detaljer** til at føje detaljerne for startsaldoen til rapporten.

Brug indstillingen **Ultimopostering** til at medtage ultimoposteringer i rapporten. Hvis finansparameteren **Opret ultimoposter under overførsel** er angivet til **Ja**, oprettes ultimoposteringerne, når der køres en årsafslutning. Ultimoposteringer bogføres på den sidste dag i regnskabsåret og vises kun, når den sidste dag i regnskabsåret er medtaget i datointervallet.

## <a name="report-details"></a>Rapportdetaljer

Rapporten  **Råbalance med transaktionsoplysninger**  indeholder følgende oplysninger i rækkerne:

- Startsaldo
- Debet- eller kreditbeløb
- Slutsaldo

For transaktionsdetaljer indeholder rapporten følgende oplysninger i kolonnerne:

- Dato
- Bilag
- Dokument
- Kontonummer
- Beskrivelse
- Finansdimensionskonto
- Finansdimensionsnavn
- Debet
- Kredit
- Saldo

## <a name="transaction-information-on-the-report"></a>Transaktionsoplysninger i rapporten

De oplysninger, der vises i kolonnerne **Dokument** og **Beskrivelse**, varierer, afhængigt af transaktionstypen. Følgende tabel indeholder nogle eksempler på oplysninger, der vises i disse kolonner.

| Transaktionstype | Dokument | Beskrivelse |
|------------------|----------|-------------|
| Finanskladde – kun finanskonti | Kladdebatchnummer | Finanskonto eller finansmodkonto |
| Finanskladde – Kreditor-/finanskonto | **Betalingsnummer**: XXX **Betalingsdato**: xx/xx/xxxx | Hovedkontonavn |
| Fritekstfaktura eller fritekstkreditnota | **Bogføringstype**: Debitorsaldo eller **Bogføringstype**: Kundeomsætning | Kladdenummer: XXXXXX Linjebeskrivelse |
| Kreditorfaktura | **Bogføringstype:** Kreditorsaldo eller **Betalingsnummer**: XXX **Betalingsdato**: xx/xx/xxxx | Leverandørnavn |
| Kreditorbetalingskladde eller debitorbetalingskladde | **Betalingsnummer**: XXX **Betalingsdato**: xx/xx/xxxx | Kreditornavn eller debitornavn |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
