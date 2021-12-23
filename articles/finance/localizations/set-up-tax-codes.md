---
title: Oprette momskoder
description: I dette emne beskrives, hvordan du konfigurerer momskoder i momsberegningstjenesten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883849"
---
# <a name="set-up-tax-codes"></a>Oprette momskoder

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer momskoder i momsberegningstjenesten. Det indeholder konfigurationen for et simpelt scenarie for at få momskoden til at fungere og oplysninger om visse avancerede momskodefunktioner til komplekse scenarier.

> [!IMPORTANT]
> Opsætningen af momskoder i momsberegningstjenesten er afhængig af en juridisk enhed. Du kan kun fuldføre denne opsætning i Regulatory Configuration Service (RCS) én gang. Momskoder synkroniseres automatisk med Microsoft Dynamics 365 Finance, når du aktiverer tjenesten Momsberegning for en valgt juridiske enhed i Finans.

## <a name="simple-setup"></a>Simpel opsætning

Benyt følgende fremgangsmåde for at bruge en momskode i et simpelt scenarie, for eksempel et scenario, hvor der kun er én momssats.

1. Log på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbejdsområder** \> **Globaliseringsfunktioner** \> **Momsberegning**.
3. Vælg den funktion og version, du vil konfigurere, og vælg **Rediger**.
4. Vælg **Konfigurationsversion** under fanen **Generelt**.
5. Under fanen **Momskoder** skal du vælge **Tilføj** og angive momskoden samt en beskrivelse.
6. Vælg **Beregningsgrundlag**. Et beregningsgrundlag er en gruppe af metoder, der er defineret i den version af momskonfiguration, du har valgt. Vælg **Efter nettobeløb** for dette simple scenarie.
7. Vælg **Gem**. Flere felter bliver tilgængelige baseret på det beregningsgrundlag, du har valgt.
8. Vælg **Tilføj** i oversigtspanelet **Satser** for at tilføje én momssats for denne momskode.
9. Vælg **Gem**.

## <a name="calculation-origin"></a>Oprindelse af beregning

Beregningsgrundlaget definerer, hvordan momsudgangsbeløbet og momsbeløbet beregnes. Det konfigureres af momskonfigurationen i arbejdsområdet **Elektronisk rapportering**. Du kan vælge mellem følgende værdier i feltet **Beregningsgrundlag**:

- Efter nettobeløb
- Efter bruttobeløb
- Efter antal
- Efter margen
- Moms på moms

### <a name="by-net-amount"></a>Efter nettobeløb

Hvis du vælger **Efter nettobeløb** i feltet **Beregningsgrundlag**, beregnes momsbeløbet som en procent af købs- eller salgsbeløbet, eksklusive andre momskoder.

Momssatsen er for eksempel 25 procent, fakturalinjen viser et antal på 10 varer til en pris af 1,00 pr. stk., og kunden får en linjerabat på 10 %. I dette tilfælde beregnes beløb på følgende måde:

- **Nettobeløb:** (10 × 1,00) - 10 % = 9,00 
- **Moms:** 9,00 × 25 % = 2,25 
- **Samlet fakturabeløb** = 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Efter bruttobeløb

Hvis du vælger **Efter bruttobeløb** i feltet **Beregningsgrundlag**, beregnes momsbeløbet som en procent af bruttosalgsbeløbet. Bruttobeløbet er nettobeløbet for linjen plus alle afgifter og gebyrer for linjen, bortset fra skatten, hvor feltet **Beregningsgrundlag** er angivet til **Efter bruttobeløb**.

Momsmyndighederne har for eksempel pålagt en vare specielle afgifter. Afgiftsbeløbene føjes til nettobeløbet, før der beregnes moms. Følgende momskoder anvendes:

- **Afgift 1** – Satsen er 10 %, og beregningsmetoden **Efter nettobeløb** anvendes.
- **Afgift 2** – Satsen er 20 %, og beregningsmetoden **Efter nettobeløb** anvendes.
- **Momssats** – Satsen er 25 %, og beregningsmetoden **Efter bruttobeløb** anvendes.

Hvis nettobeløbet er 10,00, er Afgift 1-beløbet 1,00 (10,00 × 10 %), og Afgift 2-beløbet er 2,00 (10,00 × 20 %). I dette tilfælde beregnes beløb på følgende måde: 

- **Bruttobeløb**: Nettobeløb + Afgift 1-beløb + Afgift 2-beløb = 10,00 + 1,00 + 2,00 = 13,00 
- **Momsbeløb:** 13,00 × 25 % = 3,25 
- **Afgifter og moms i alt**: 1,00 + 2,00 + 3,25 = 6,25 
- **Samlet fakturabeløb** = 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Efter antal

Hvis du vælger **Efter antal** i feltet **Beregningsgrundlag**, beregnes momsbeløbet som et fast beløb pr. enhed, multipliceret med det antal, der er angivet på dokumentlinjen. Beløbet pr. enhed angives i oversigtspanelet **Satser**.

Momskoden konfigureres for eksempel til 1,20 pr. enhed. Der sælges 25 enheder af en vare på en salgsfakturalinje. I dette tilfælde beregnes momsbeløbet som 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Efter margen

Hvis du vælger **Efter margen** i feltet **Beregningsgrundlag**, beregnes momsbeløbet som en procent af salgsmargenen. Salgsmargenen er salgsbeløbet minus kostbeløbet. Denne beregningsmetode gælder kun for salgstransaktioner.

Momssatsen er for eksempel 25 procent, fakturalinjen viser et antal på 10 varer til en pris af 10,00 pr. stk., og kostbeløbet pr. vare er 6. I dette tilfælde beregnes beløb på følgende måde:

- **Salgsmargen:** 10 × ( 10,00-6,00) = 40,00
- **Momsbeløb:** 40,00 × 25 % = 10,00
- **Samlet fakturabeløb** = 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Moms på moms

Hvis du vælger **Moms på moms** i feltet **Beregningsgrundlag**, beregnes momsen som en procentdel af alle de andre momsbeløb på samme dokumentlinje.

For eksempel anvendes følgende momskoder:

- **Afgift 1** – Satsen er 10 %, og beregningsmetoden **Efter nettobeløb** anvendes.
- **Afgift 2** – Satsen er 20 %, og beregningsmetoden **Efter nettobeløb** anvendes.
- **Moms på afgift** – Satsen er 25 %, og beregningsmetoden **Moms på moms** anvendes.

I dette tilfælde beregnes beløb på følgende måde:

- **Nettobeløb:** 10,00 
- **Afgift 1:** 10,00 × 10 % = 1,00 
- **Afgift 2:** 10,00 × 20 % = 2,00 
- **Moms på afgift:** 3,00 × 25 % = 0,75
- **Moms i alt:** 1,00 + 2,00 + 0,75 = 3,75 
- **Samlet fakturabeløb** = 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Avanceret funktonalitet

Dette afsnit indeholder en forklaring på nogle avancerede funktioner i opsætningen af momskoder til komplekse scenarier.

### <a name="tax-exemption"></a>Momsfritagelse

Hvis du angiver indstillingen **Er momsfri** til **Ja** i oversigtspanelet **Generelt**, tilsidesættes momsbeløbet altid til 0 (nul), uanset den faktiske momssats.

Du kan angive årsagen til fritagelsen i feltet **Fritagelseskode**. 

Du kan aktivere opslag efter masterdata i feltet **Fritagelseskode**. På den måde kan du vælge mellem de fritagelseskodeværdier, der er defineret i Finans. Du kan finde flere oplysninger om aktivering af masterdataopslag i [Aktivere masterdataopslag til konfiguration af momsberegning](tax-service-set-up-environment-master-data-lookup.md).

Momssatsen er for eksempel 25 %, og indstillingen **Er momsfri** er angivet til **Ja** i momskoden. Fakturalinjen viser et antal på 10 varer til en stykpris på 1,00, og kunden får en linjerabat på 10 %. I dette tilfælde beregnes beløb på følgende måde:

- **Nettobeløb:** (10 × 1,00) - 10 % = 9,00 
- **Moms:** 0,00 
- **Samlet fakturabeløb** = 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Importmoms

Hvis du angiver indstillingen **Er importmoms** til **Ja** i oversigtspanelet **Generelt**, bogføres momsbeløbet på kontoen **Skyldig importmoms** i stedet for på kontoen **Oversigt over kreditorer**.

Momssatsen er for eksempel 25 %, og indstillingen **Er importmoms** er angivet til **Ja** i momskoden. Fakturalinjen viser et antal på 10 varer til en stykpris på 1,00, og kunden får en linjerabat på 10 %. I dette tilfælde beregnes beløb på følgende måde:

- **Nettobeløb:** (10 × 1,00) - 10 % = 9,00 
- **Importmoms:** 9,00 × 25 % = 2,25
- **Samlet fakturabeløb** = 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Hvis både indstillingen **Er momsfri** og **Er importmoms** er angivet til **Ja** i en momskode, genkendes koden som momsfritaget for salgstransaktioner og importafgift for købstransaktioner.

### <a name="reverse-charges"></a>Tilbageføre gebyrer

Hvis du angiver indstillingen **Er modtagerpris** til **Ja** i oversigtspanelet **Generelt**, kan momssatsen konfigureres som negativ. Vi anbefaler, at du konfigurerer to momskoder til modtagermoms: en, der har en positiv momssats, og en, der har en negativ momssats. Begge momskoder skal have samme kursværdi, og indstillingen **Er modtagerafgift** skal angives til **Ja** for den momskode, der har en negativ momssats. Du kan finde flere oplysninger om løsningen med modtagermoms i Finance i [Modtagermomsmekanisme for momsskema](emea-reverse-charge.md).

Der fastsættes for eksempel to momskoder på én fakturalinje. En momssats er 25 %. Den anden momssats er -25 %, og indstillingen **Er modtagermoms** er angivet til **Ja** i den anden momskode. Fakturalinjen viser et antal på 10 varer, som hver koster 1,00. I dette tilfælde beregnes beløbene på følgende måde:

- **Nettobeløb:** (10 × 1,00) = 10,00 
- **Momskode 1:** 10,00 × 25 % = 2,50
- **Momskode 2:** 10 × -25 % = -2,50
- **Samlet fakturabeløb:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Udeladelse i beregninger af grundbeløb

Hvis du angiver indstillingen **Udelad i beregning af grundbeløb** til **Ja** i oversigtspanelet **Generelt**, udelades det beregnede momsbeløb for momskoden fra momsgrundlagsbeløbet for andre momskodeberegninger i det prisinklusive scenarie.

Du kan finde flere oplysninger under [Beregne moms på prisen, når Priser er aktiveret inklusive moms](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Satser

I oversigtspanelet **Sats** kan du definere forskellige momssatser for forskellige intervaller af momsgrundlagsbeløb. Til beregning af momsbeløbet bruger tjenesten Momsberegning altid den sats, der svarer til momsgrundlagsbeløbet.

Momssatser kan for eksempel være konfigureret som vist i følgende tabel.

| Minimumsbeløb | Maksimalt beløb | Momssats   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10 procent |
| 1.000          | 5.000          | 15 procent |
| 5.000          | 10,000         | 20 procent |
| 10,000         | 0              | 30 procent |

I dette tilfælde beregnes momsbeløbet på følgende måde:

- Hvis momsgrundlagsbeløbet er 300,00, momssatsen er 10 %, og momsbeløbet er 300,00 × 10 % = 30,00.
- Hvis momsgrundlagsbeløbet er 3.000,00, momssatsen er 15 %, og momsbeløbet er 3.000,00 × 15 % = 450,00.
- Hvis momsgrundlagsbeløbet er 6.000,00, momssatsen er 20 %, og momsbeløbet er 6.000,00 × 10 % = 1.200,00.
- Hvis momsgrundlagsbeløbet er 20.000,00, momssatsen er 30 %, og momsbeløbet er 20.000,00 × 30 % = 6.000,00.

> [!NOTE]
> Hvis momsgrundlagsbeløbet både kan svare til maksimumbeløbet på én linje og minimumbeløbet på den anden linje, bruger grundbeløbet den momssats, der svarer til minimumgrundlagsbeløbet. Hvis for eksempel momsgrundlagsbeløbet er 1000,00, momssatsen er 15 %, og momsbeløbet er 1.000,00 × 15 % = 150,00.

### <a name="limits"></a>Grænser

I oversigtspanelet **Grænser** kan du definere momsgrænser for at tilsidesætte det beregnede momsbeløb, hvis momsbeløbet ligger inden for intervallet for minimum/maksimum.

- Hvis det beregnede momsbeløb er større end eller lig med det maksimummomsbeløb, der er konfigureret i oversigtspanelet **Grænser**, er det endelige momsbeløb lig med det maksimale momsbeløb.
- Hvis det beregnede momsbeløb er mindre end det minimummomsbeløb, der er konfigureret i oversigtspanelet **Grænser**, er det endelige momsbeløb 0 (nul).

Momsgrænserne konfigureres for eksempel på følgende måde:

- **Minimummomsbeløb:** 100 
- **Maksimummomsbeløb:** 1.000

Hvis det beregnede momsbeløb er 2.000, er det endelige momsbeløb 1.000.

Hvis det beregnede momsbeløb er 500, er det endelige momsbeløb 500.

Hvis det beregnede momsbeløb er 80, er det endelige momsbeløb 0 (nul).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
