---
title: Detailopgørelser
description: I dette emne beskrives, hvordan opgørelser oprettes og bogføres.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: e9162bb9b56432dbeb4638e0598dcbf436ab0b1b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989495"
---
# <a name="retail-statements"></a>Detailopgørelser

[!include [banner](includes/banner.md)]

I Dynamics 365 Commerce bruges processen til bogføring af opgørelsen til at redegøre for de transaktioner, der opstår i Cloud POS eller MPOS (Modern POS). Opgørelsesbogføringsprocessen bruger distributionsplanen til at trække en række POS-transaktioner til Headquarters-klienten (HQ). De parametre, der er defineret på siden **Commerce-parametre** og **Butikker**, bruges til at vælge de transaktioner, der trækkes til hver enkelt opgørelse.

Følgende illustration viser til opgørelsesbogføringsprocessen. I denne proces overføres transaktioner, der er registreret i POS, til klienten ved hjælp af Commerce-planlægger. Når klienten modtager transaktionerne, kan du oprette, beregne og bogføre transaktionsopgørelsen for butikken.

[![Opgørelsesbogføringsproces](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Oprettelse og bogføring af opgørelser

Du kan oprette en opgørelse manuelt eller ved at bruge batchprocesser, som du opretter, så de køres regelmæssigt i løbet af dagen. I begge tilfælde bruges følgende trin til at oprette og bogføre opgørelser.

### <a name="create-the-statement"></a>Oprette opgørelsen

Dette trin identificerer den butik, som opgørelsen oprettes til manuelt. Hvis du konfigurerer en batchproces, kan du automatisk oprette opgørelser til alle butikker på basis af en plan, som du definerer.

### <a name="calculate-the-statement"></a>Beregne opgørelsen

I dette trin vælges transaktionslinjer på baggrund af kriterier, der er defineret for hver butik på siderne **Commerce-parametre** og **Butikker**. På disse sider kan du definere kriterierne og angive, hvordan transaktionerne skal beregnes. Du kan bruge siden **Transaktioner** til at få vist en liste over de transaktioner, der er medtaget i opgørelsen, før du beregner opgørelsen.

Ved beregningen af opgørelsen bruges kasseoptællinger fra kasseapparaterne som optalt beløb. Du kan også angive det optalte beløb manuelt. Opgørelsen viser differencen mellem salgsbeløbet for transaktionerne og det faktisk optalte beløb for alle betalingsmetoder. Opgørelsen vil kun blive bogført, hvis denne difference er mindre end den maksimale bogføringsdifference, der er defineret for butikken.

> [!NOTE]
> Opgørelsesberegningsprocessen bruger den globale nummerserie.

Når du beregner en opgørelse, omfatter beregningen følgende opgaver:

- For det valgte datointerval skal du markere de transaktioner, der ikke er medtaget i en tidligere opgørelsesberegning.
- Beregn de samlede beløb, der blev tilbudt i de valgte transaktioner. Resultaterne vises i opgørelseslinjerne afhængigt af opgørelsesmetoden:

    - Hvis opgørelsesmetoden er **Sum**, oprettes der en linje for hver betalingsmetode i de valgte transaktioner.
    - Hvis opgørelsesmetoden er **Human Resources**, oprettes der en linje for hver betalingsmetode i transaktioner, der er udført af den valgte medarbejder.
    - Hvis opgørelsesmetoden er **POS-klient**, oprettes der en linje for hver betalingsmetode i transaktioner, der blev udført i det valgte register.
    - Hvis opgørelsesmetoden er **Skift**, oprettes der en linje for hver betalingsmetode i transaktioner, der blev udført under et skift.

Hvis afkrydsningsfeltet **Opdel efter opgørelsesmetode** er markeret på siden **Butikker**, oprettes en separat opgørelse ud fra den værdi, der er valgt i feltet **Opgørelsesmetode**.

Hvis der er åbent i din butik til efter midnat, kan du bogføre opgørelsesbogføringen, så den er baseret på slutningen på forretningsdagen i stedet for udløbet af kalenderdagen.

På siden **Butikker** i oversigtspanelet **Opgørelse/ultimo** skal du i feltet **Afslutning på forretningsdag** angive det tidspunkt, hvor den sidste transaktion skal registreres for at blive medtaget i opgørelsen af forretningsdagen. Markér afkrydsningsfeltet **Bogfør som arbejdsdag** for at bogføre transaktioner inden for samme forretningsdag. Når opgørelsen bogføres, kan transaktioner, der er registreret inden for samme forretningsdag, medtages på den samme salgsordre, selvom nogle transaktioner forekommer før midnat og nogle transaktioner efter midnat.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Eksempel: Bogfør en opgørelse for en forretningsdag, der strækker sig over to kalenderdage

En butik er åben mellem 8:00 og 3:00, og feltet **Bogfør som arbejdsdag** er markeret i butikkens konfiguration. Den 31. maj bogfører butikken transaktioner mellem 8:00 og midnat. Butikken posterer også transaktioner mellem 12:01 og 3:00 den 1. juni.

Når butikken bogfører sin opgørelse ved afslutningen af forretningsdagen, indeholder den salgsordre, der oprettes, alle transaktioner, der er registreret i åbningstiden mellem kl. 08:00 og kl. 03:00, selvom transaktionerne fandt sted på datoer, d. 31. maj og d. 1. juni.

Hvis afkrydsningsfeltet **Bogfør som arbejdsdag** ikke er markeret for den samme butik, oprettes der separate salgsordrer, når butikken bogfører sin opgørelse ved afslutningen af forretningsdagen. Én salgsordre, der indeholder de transaktioner, der er registreret mellem åbningstiderne mellem kl. 08.00 og midnat d. 31, maj, og en anden salgsordre, der indeholder de transaktioner, der er registreret i forretningstiden mellem kl. 12:01 og kl. 03:00 d. 1. juni.

> [!NOTE]
> Før du kan oprette opgørelser, skal du lukke skiftene i opgørelsesperioden.

### <a name="post-the-statement"></a>Bogføre opgørelsen

Når du bogfører en opgørelse, oprettes der salgsordrer og fakturaer for salg i opgørelsen.

- Salg efter princippet "kontant og afhentet" er samlet på én salgsordre og faktureret til den standardkunde, der er knyttet til butikken.
- Salg, for hvilket der blev føjet en kunde til transaktionen i POS, genererer separate salgsordrer og fakturaer – én for hver entydig kunde.

Der oprettes automatisk betalingskladder for betalingerne i opgørelsen, og lageret opdateres for POS-butikken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]