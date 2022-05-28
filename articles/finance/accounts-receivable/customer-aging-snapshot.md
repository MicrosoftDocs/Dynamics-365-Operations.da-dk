---
title: Aldersfordelte øjebliksbilleder for debitor
description: Dette emne indeholder oplysninger om aldersfordelte øjebliksbilleder for debitorer. Et aldersfordelt øjebliksbillede beregner aldersfordelte saldi for en gruppe debitorer på et bestemt tidspunkt.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54db3e53cd31936ce80f0cdf1147535216d0d4b4
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722989"
---
# <a name="customer-aging-snapshots"></a>Aldersfordelte øjebliksbilleder for debitor

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om aldersfordelte øjebliksbilleder for debitorer. Et aldersfordelt øjebliksbillede beregner aldersfordelte saldi for en gruppe debitorer på et bestemt tidspunkt. Du kan oprette poster for aldersfordelte øjebliksbilleder enten for alle kunder eller for kunderne i kundepuljen.

Oplysninger fra aldersfordelte øjebliksbilleder vises på listesiden **Aldersfordelte saldi** og på siden **Rykkere**. Du skal oprette et aldersfordelt øjebliksbillede, før du kan bruge listesiden **Aldersfordelte saldi**. Listesiden viser kun kunder, der allerede er oprettet et aldersfordelt øjebliksbillede for.

Arbejdsområdet **Kundekredit og inkasso** viser også aldersfordelingen for kunder. Yderligere oplysninger finder du i [Styring af kredit og inkasso Power BI-indholdet](credit-collections-power-bi.md).

> [!NOTE]
> Hvis du vil reducere den tid, det tager at oprette et aldersfordelt øjebliksbillede, skal du aktivere funktionen **Forbedring af aldersfordelt ydeevne for debitorer** i arbejdsområdet **Funktionsstyring**. Du skal dog undlade at bruge kundepuljer, når denne funktion er aktiveret. Hvis der er valgt en kundepulje, fungerer funktionen ikke, men du kan stadig oprette et aldersfordelt øjebliksbillede.

Når du opretter et aldersfordelt øjebliksbillede for debitorer, skal du bruge følgende felter til at angive oplysninger om det:

- **Definition af forældelsesperiode** – Vælg definitionen på forældelsesperioden for det aldersfordelte øjebliksbillede. Du kan have ét aldersfordelt øjebliksbillede for hver definition af forældelsesperioder. Det aldersfordelte øjebliksbillede og definitionen af forældelsesperioden skal oprettes separat.
- **Pulje-id** – Det er valgfrit, om du vil udfylde feltet. Du kan bruge en pulje til at definere det sæt kunder, der skal behandles i det aldersfordelte øjebliksbillede. Hvis du vælger en kundepulje i dette felt, oprettes der kun et aldersfordelt øjebliksbillede for de debitorkonti, der indgår i kundepuljen. Den valgte kundepulje skal være af typen **Aldersfordelt øjebliksbillede**. Hvis du ikke udfylder dette felt, oprettes der et aldersfordelt øjebliksbillede for alle debitorkonti.

    > [!NOTE]
    > Hvis funktionen **Forbedring af aldersfordelt ydeevne for debitorer** er aktiveret, skal du ikke vælge en kundepulje.

- **Kriterier** – Aldersfordelt øjebliksbillede forældes baseret på den dato, du vælger:

    - **Posteringsdato** – Hver transaktion forældes baseret på transaktionsdatoen.
    - **Forfaldsdato** – Hver transaktion forældes baseret på forfaldsdatoen.
    - **Dokumentdato** – Hver transaktion forældes baseret på dokumentdatoen.

- **Aldersfordeling pr.** – Vælg den type dato, der skal bruges i feltet **Dags dato** for det aldersfordelte øjebliksbillede. Forældelsesperioder beregnes derefter på grundlag af denne dato. 

    - **Dags dato** – Brug systemdatoen. Vælg denne indstilling, hvis behandling er indstillet til at køre som et tilbagevendende batchjob. Hver gang batchen køres, bruges systemdatoen for kørslen.
    - **Valgt dato** – Brug en dato, du angiver. Hvis du vælger denne indstilling, skal du angive en aldersfordelingsdato.

    Den aktuelle forældelsesperiode er f.eks. 30 dage. Hvis du vælger **Dags dato** i dette felt, starter den aktuelle forældelsesperiode på dags dato og medtager derefter de foregående 29 dage. Hvis du vælger **Valgt dato** og angiver en dato, starter den aktuelle forældelsesperiode på den angivne dato og medtager derefter de foregående 29 dage.

- **Opdater rykkerstatus** – Vælg **Ja** i denne indstilling for at opdatere rykkerstatussen for transaktioner på siden **Rykkere** fra **Løfte om betaling** til **Brudt betalingsløfte**, hvis forældelsesdatoen ligger efter datoen i feltet **Dato for løfte om betaling**. Vælg **Nej** i denne indstilling for at lade rykkerstatus være uændret på siden **Rykkere**.
- **Medtag debitorer med nul-saldi**– Vælg **Ja** i denne indstilling, hvis du vil medtage alle debitorer uanset deres saldo. Hvis du medtager alle debitorer, anbefales det, at du aktiverer funktionen **Forbedring af aldersfordelt ydeevne for debitorer**, og at du ikke bruger kundepuljer. Vælg **Nej** i denne indstilling, hvis du kun vil medtage debitorer, der har en saldo. Denne indstilling er med til at øge ydeevnen, da kunder, der ikke har en saldo, springes over.
- **Firmaområde** – Under fanen **Firmaområde** skal du vælge de juridiske enheder (firmaer), der skal medtages i det aldersfordelte øjebliksbillede. Kun juridiske enheder, der er konfigureret til centraliserede betalinger, kan vælges. Posteringer fra de valgte juridiske enheder medtages derefter i forældelsesperioderne for debitorer, der har samme part-id i alle disse juridiske enheder. Valutabeløb konverteres til valutaen for den juridiske enhed, du er logget på, når du opretter det aldersfordelte øjebliksbillede.

Det anbefales, at du planlægger, at denne proces køres i en batch.

> [!NOTE]
> Hvis du vil forbedre batchydeevnen, når der oprettes aldersfordelte øjebliksbilleder, skal du angive et tal i feltet **Maksimalt antal batchopgaver** i oversigtspanelet **Rykkerstandard** under fanen **Rykkere** på siden **Debitorparametre**. I feltet **Aldersfordel kundesaldi** anbefales det, at du starter med standardværdien **100** og derefter justerer værdien for at optimere behandlingen til dit behov.

