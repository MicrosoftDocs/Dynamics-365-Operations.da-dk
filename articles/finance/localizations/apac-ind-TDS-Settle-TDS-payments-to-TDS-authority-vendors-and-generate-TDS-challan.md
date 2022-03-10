---
title: Udligne skattebetalinger til skattemyndighedskreditorer og generere en skatteopgørelse
description: Dette emne forklarer, hvordan du kan udligne betalinger af kildeskat (TDS – Tax Deducted at Source) til skattemyndighedskreditorer.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 19f41020c6e1db8b08c7f69a58d33852c730931447803e2e1e970b1c293b6acd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779392"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>Udligne skattebetalinger til skattemyndighedskreditorer og generere en skatteopgørelse

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan udligne betalinger af kildeskat (TDS – Tax Deducted at Source) til skattemyndighedskreditorer.

1. Gå til **Kreditor \> Betalinger \> Kreditorbetalingskladde**.

    [![Siden Kreditorbetalingskladde.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Vælg **Ny** på siden **Kreditorbetalingskladde** for at oprette en kladdelinje.
3. I feltet **Konto** skal du vælge den skattemyndighedskreditor, som du vil udligne skattebetalingen for.
4. Vælg **Udligningstransaktioner** for at åbne siden **Udligningstransaktioner**, hvor du kan få vist de udlignede skattetransaktioner for skattemyndighedskreditoren.

    De udlignede skattetransaktioner for en udligningsperiode er vist på følgende måde:

    - Skattetransaktioner, hvor arten af vurderingskategorien er **Virksomhed**, vises som én posteringslinje.
    - Skattetransaktioner, hvor arten af vurderingskategorien er **HUF**, **Virksomhed**, **Enkeltperson**, **AOP**, **BOI**, **Lokal myndighed** eller **Andre** vises som én posteringslinje.
    - Feltet **Beløb** viser det samlede skattebeløb, der skal betales til skattemyndighedskreditoren.

5. Vælg **Transaktioner for A-skat** for at få vist de forskellige skattetransaktioner, der er inkluderet i udligningsposten. Du kan få vist opdelingen af hver skattetransaktion, der er inkluderet i udligningsprocessen for udligningsperioden på denne side.
6. Under fanen **Oversigt** skal du markere afkrydsningsfeltet **Markér** for de skattetransaktioner, der skal udlignes for skattemyndighedskreditoren.

    På siden **Oversigt** vises følgende oplysninger for hver åben skattetransaktion:

    - **Dato** – Skattetransaktionsdatoen.
    - **Bilag** – Bilagsnummeret.
    - **Kilde** – Det modul, som skattetransaktionen er bogført i.
    - **Kreditor/debitor** – Det kreditor- eller debitorkontonummer, som kildeskatten er trukket fra.
    - **Navn på fratrukket part** – Navnet på den kreditor eller debitor, som kildeskatten er trukket fra.
    - **Art af vurdering** – Arten af den vurderingskategori, som den fratrukne part tilhører.
    - **Beløb** – Det fakturabeløb, som kildeskat blev beregnet for.
    - **Skattebeløb** – Det skattebeløb, der er beregnet for transaktionen.

    > [!NOTE]
    > Ryd afkrydsningsfeltet **Markér** for eventuelle skattetransaktioner, der ikke skal udlignes for skattemyndighedskreditoren.

    Under fanen **Generelt** viser feltet **PAN** det permanente kontonummer for den fratrukne part. Feltet **Dato** viser datoen for skatteberegningen, og feltet **Værdi** viser den samlede procentdel, der blev brugt til skatteberegningen.

7. Vælg **Bilag** for at få vist bilagsposterne for TDS-transaktionen.
8. Luk siden.
10. Vælg **Komponenter for A-skat** for at åbne siden **Komponenter for A-skat**, hvor du kan få vist den kildeskat, der blev beregnet pr. kildeskattekomponent, for en bestemt kildeskattekode.

    Under fanen **Oversigt** viser feltet **Skattekomponent** den kildeskattekomponent, der blev brugt til transaktionen. Feltet **Beløb** viser det skattebeløb, der blev beregnet for kildeskattekomponenten, i basisvalutaen. Feltet **Akkumuleret beløb** viser det samlede skattebeløb, som blev beregnet for kildeskattekomponenten for alle udlignede transaktioner.

    Under fanen **Beløb** viser sektionen **Standardvaluta** det skattebeløb, der blev beregnet for kildeskattekomponenten, i standardvalutaen. Sektionen **Sekundær valuta** viser beløbet i den sekundære valuta.

11. Luk siden **Komponenter for A-skat**.
12. På siden **Åbenpost-redigering** i feltet **Beløb** skal du bemærke, at det samlede beløb, der skal udlignes til skattemyndighedskreditoren for udligningsperioden, bliver opdateret.
13. Hvis du vil udligne skattetransaktionerne for forskellige skatteudligningsperioder til skattemyndighedskreditoren, skal du markere afkrydsningsfeltet **Markér** for transaktionerne.
14. Luk siden **Åbenpost-redigering**.

    > [!NOTE]
    > Hvis der kun er markeret nogle få transaktioner til udligning på siden **Transaktioner for A-skat**, opdateres det samlede skattebeløb for de valgte transaktioner i feltet **Rettelse** på siden **Åbenpost-redigering**. Det rettede beløb opdateres på kladdelinjen på siden **Kladdebilag**, og siden **Åbenpost-redigering** bliver lukket.

    På siden **Kladdebilag** viser feltet **Debet** det samlede beløb, der skal betales til skattemyndighedskreditoren.

15. Angiv oplysninger om modkontoen.

    > [!NOTE]
    > Hvis skattetransaktionerne har forskellige skattekontonumre (TAN), oprettes der kladdelinjer for hvert skattekontonummer på siden **Kladdebilag**.

16. Under fanen **Betalingsgebyr** i feltet **Gebyr-id** skal du vælge et gebyr-id med gebyrtypen **Rente** eller **Andre** for at opkræve betalingsgebyret for forsinkede betalinger, der foretages til skattemyndighedskreditoren.

    Under fanen **Skatteoplysninger** i sektionen **Firmaoplysninger** viser feltet **Navn** virksomhedens navn. I sektionen **A-skat** viser feltet **Skattekontonummer (TAN)** det skattekontonummer, der er knyttet til posteringslinjen.

17. Valider og bogfør kladden.
18. Vælg **A-skat \> Oplysninger til opgørelse** for at angive transaktionsoplysninger til opgørelsen.

    Feltet **Bilag** viser bilagsnummeret på transaktionen.
    
19. Markér afkrydsningsfeltet **Kildeskat indbetalt gennem bogført post**, hvis skattebeløbet indbetales ved hjælp af en bogført post.
20. I feltet **Opgørelsesnummer** skal du angive det opgørelsesnummer, der skal bruges til at foretage betalingen til skattemyndighedskreditoren.
21. Angiv opgørelsesdatoen i feltet **Dato**.
22. I feltet **Banknavn** skal du vælge navnet på den bank, hvor det skyldige skattebeløb til skattemyndighedskreditoren skal indbetales. I dette felt kan du se alle de bankkonti, der er konfigureret for skattemyndighedskreditoren hos **Kreditor \> Alle kreditorer \> Opsætning \> Bankkonti**.
23. I feltet **BSR-kode** skal du angiv bankens BSR-kode (BSR – Basic Statistical Return).
24. Luk siden.

### <a name="example"></a>Eksempel

Perioden 04/01/2009 udlignes for skattekomponentgruppen **Leje** ved hjælp af den periodiske skatteudligningsproces. Det samlede skattebeløb på 141.625,00 bogføres på skattemyndighedskreditorens konto for skatteudligningsperioden. Du kan få vist dette beløb i feltet **Beløb** på siden **Åbenpost-redigering** for skattemyndighedskreditoren.

Hvis du vælger **Transaktioner for A-skat** for at få vist de forskellige skattetransaktioner, der blev udlignet for perioden, vises følgende oplysninger.

| Skattebeløb |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

For et specifikt skattebeløb kan du vælge **Komponenter for A-skat** for at få vist det skattebeløb, der blev beregnet pr. kildeskattekomponent for en bestemt kildeskattekode. I dette eksempel kan du vælge **Komponenter for A-skat** for skattebeløbet 16.995,00. Det skattebeløb, der er beregnet pr. komponent for transaktionen, vises.

| Skattekomponent | Beløb    | Akkumuleret beløb |
|---------------|-----------|--------------------|
| Kildeskat           | 1,5000.00 | 125,000.00         |
| Tillæg     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Hvis du kun har valgt skattebeløbene 16.995,00, 22.660.00, og 28.325,00 til udligning på siden **Transaktioner for A-skat**, vises det samlede beløb for udligning som **67.980,00** i feltet **Rettelse** på siden **Åbenpost-redigering**. Hvis denne transaktion er markeret til udligning, og siden **Åbenpost-redigering** er lukket, vises beløbet **67.980,00** beløb i feltet **Debet** på siden **Kladdebilag**.

Du kan nu bogføre kladden og generere skatteopgørelsen.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Regulering af forudbetalinger, der er foretaget til TDS-myndighedskreditorer

Hvis du vil regulere en forskudsbetaling, der er foretaget til skattemyndighedskreditoren i forhold til en faktisk betaling, skal du gå til **Kreditor \> Kreditorer \> Alle kreditorer \> Transkationsredigering**. Hvis den faktiske betaling, der er foretaget, overstiger forskudsbetalingen, genereres der to opgørelsesnumre for transaktionen. Det er dog kun det første opgørelsesnummer, der vises i skatteforespørgslen.
