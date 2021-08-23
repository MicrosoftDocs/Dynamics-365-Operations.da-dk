---
title: Beregning af kildeskat for betalinger og egenveksler
description: Dette emne indeholder referenceoplysninger om de forskellige betalingstransaktioner, som kildeskat (TDS – Tax Deducted at Source) beregnes på.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28afd04b1c341985f7ac15e05aba7a9039a59d869dd5bc60b4163d2ba1ae4ec0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750334"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>Beregning af kildeskat for betalinger og egenveksler

[!include [banner](../includes/banner.md)]

Dette emne indeholder referenceoplysninger om de forskellige betalingstransaktioner, som kildeskat (TDS – Tax Deducted at Source) beregnes på.

| Serienummer | Transaktionstype | Transaktionsbeløb | Sidenavn og sti | Kontotype og modkontotype |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Forudbetaling/betaling mod faktura (skyldig kildeskat) | Debet eller Kredit | <ul><li>Finans (**Finans \> Kladdeposteringer \> Finanskladder**)</li><li>Fakturakladde (**Kreditor \> Fakturaer \> Fakturakladde**)</li><li>Betalingskladde (**Kreditor \> Betalinger \> Kreditorbetalingskladde**)</li></ul> | Kreditor (Dr.), Bank (Kr.). |
| 2             | Forudbetaling/betaling mod faktura (Køb foretaget fra kunde – skyldig kildeskat) | Debet eller Kredit | <ul><li>Finans (**Finans \> Kladdeposteringer \> Finanskladder**)</li><li>Fakturakladde (**Kreditor \> Fakturaer \> Fakturakladde**)</li><li>Betalingskladde (**Kreditor \> Betalinger \> Kreditorbetalingskladde**)</li></ul> | Debitor (Dr.), Bank (Kr.). |
| 3             | Egenveksler | Debet | Kladde til udstedelse af egenveksel (**Kreditor \> Betalinger \> Egenveksler \> Kladde til udstedelse af egenveksel**) | Kreditor (Dr.), Finans (Kr.). |
| 4             | Diverse indtægter (tilgodehavende kildeskat) | Debet eller Kredit | Finans (**Finans \> Kladdeposteringer \> Finanskladder**) | Bank (Dr.), Finans (Kr.). |
| 5             | Øvrige udgifter (skyldig kildeskat) | Debet eller Kredit | Finans (**Finans \> Kladdeposteringer \> Finanskladder**) | Bank (Dr.), Finans (Kr.). |

Benyt denne fremgangsmåde for at beregne kildeskat på betalinger og egenveksler.

1. Opret kladdelinjer på kladdesiderne. Vælg kontotypen til modkontotypen.
2. Vælg **Funktioner \> Udligning** for at åbne siden **Åbenpost-redigering**. Vælg derefter den faktura, der skal udlignes. Hvis kildeskatten allerede er beregnet på fakturaniveau, viser feltet **Beløbsgrundlag** det beløb, som kildeskatten er beregnet ud fra. Feltet **Skattebeløb** viser det beløb for kildeskat, der er beregnet for transaktionen. Feltet **Beløb** viser nettobetalingsbeløbet (hvilket vil sige betalingsbeløbet, efter kildeskatten er fratrukket).

    > [!NOTE]
    > For betalinger, der er foretaget i forhold til en faktura, gælder følgende betingelser:
    >
    > - Hvis betalingsbeløbet og fakturabeløbet er det samme, beregnes der ikke kildeskat, hvis den allerede er beregnet på fakturaniveau.
    > - Hvis fakturabeløbet efter fratrækning af skattebeløbet er større end betalingsbeløbet, beregnes der ikke kildeskat.
    > - Hvis fakturabeløbet efter fratrækning af skattebeløbet er mindre end betalingsbeløbet, beregnes der kildeskat ud fra det beløb, der overstiger fakturabeløbet.

3. I feltet **Kildeskattegrupper** på siden **Kladdebilag** på fanen **Oversigt** kan du gennemse og ændre den standardgruppe for kildeskat, som er defineret for kreditoren eller debitoren. Den beregnede kilde på kladdelinjerne er baseret på den formel, der er defineret for kildeskattekoderne i kildeskattegruppen.

    > [!NOTE]
    > Kildeskat beregnes kun, hvis indstillingen **Beregn A-skat** er angivet til **Ja** for kreditoren på siden **Kreditorer**.

4. I feltet **Navn** i sektionen **Skatteoplysninger** på fanen **Firmaoplysninger** kan du vælge en virksomheds navn for alternative adresser, som er angivet for virksomheden.

    I feltet **Art af vurdering** i sekstionen **A-skat** vises arten af vurderingskategorien for kreditoren eller debitoren. Feltet **Skattekontonummer (TAN)** viser skattekontonummeret (TAN –  Tax Account Number) for den valgte virksomhed.

5. Vælg **knappen A-skat \> A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Den øverste del af denne side indeholder følgende felter:

    - **Samlet beløb for A-skat** – Den samlede kildeskat er beregnet for transaktionen for kildeskattegruppen.
    - **Værdi** – Den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen. Den samlede procentdel er baseret på den formel, der er defineret for kildeskattekoderne og er tilknyttet kildeskattegruppen.
    - **Reguleret beløb for A-skat i alt** – Det samlede regulerede skattebeløb for alle skattekoder i kildeskattegruppen.
    - **Kildeskat** – Et markeret afkrydsningsfelt angiver, at der er knyttet en kildeskattegruppe til transaktionen.

    Felterne under fanen **Oversigt**, **Generelt** og **Regulering** viser det beregnede skattebeløb og oplysninger om det regulerede skattebeløb for hver kildeskattekode, som er tilknyttet kildeskattegruppen.

6. Vælg **Tærskel** for at åbne siden **Tærskel**, hvor du kan gennemse den grænseværdi, der er defineret for den skattekomponent, som er tilknyttet en specifik kildeskattekode.
7. Vælg **Formeldesigner** for at åbne siden **Formeldesigner**, hvor du kan gennemse den formel, der er defineret for en specifik kildeskattekode.
8. Luk **Formeldesigner** og siderne for **Midlertidige transaktioner for A-skat** for at vende tilbage til siden **Kladdebilag**.
9. Valider og bogfør kladden. Det beregnede kildeskattebeløb bogføres på den kreditorkonto, der er defineret for hver kildeskattekode i kildeskattegruppen. Kreditorkonti for kildeskattekoder er defineret på siden **Koder for A-skat**.
10. Vælg **Bogført A-skat** for at åbne siden **Midlertidige transaktioner for A-skat**. Feltet **Værdi** viser den samlede procentdel, der er brugt til beregning af kildeskat for transaktionen.

    Felterne på fanerne **Oversigt**, **Generelt** og **Beløb** viser de skattebeløb, der blev beregnet for den kildeskattegruppe, som er knyttet til transaktionen.

11. Gennemse beregningsoplysningerne for kildeskat for hver kildeskattekode, der er tilknyttet kildeskattegruppen.

## <a name="generate-payments"></a>Opret betalinger

Benyt følgende fremgangsmåde for at oprette betalinger.

1. Udfør ét af følgende trin:

    - Gå til **Kreditor \> Betalinger \> Kreditorbetalingskladde**.
    - Gå til **Debitor \> Betalinger \> Debitorbetalingskladde**.
    - Gå til **Kreditor \> Betalinger \> Egenveksler \> Kladde til udstedelse af egenveksel**.
    - Gå til **Debitor \> Betalinger \> Veksel \> Kladde til udstedelse af veksel**.
    - Gå til **Debitor \> Betalinger \> Veksel \> Genudsted vekseljournal**.

2. Vælg **Linjer**.
3. Vælg **Funktioner \> Opret betalinger**.
