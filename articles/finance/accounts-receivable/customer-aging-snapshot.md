---
title: Aldersfordelte øjebliksbilleder for debitor
description: Denne artikel indeholder oplysninger om aldersfordelte øjebliksbilleder for debitorer. Et aldersfordelt øjebliksbillede beregner aldersfordelte saldi for en gruppe debitorer på et bestemt tidspunkt.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775230"
---
# <a name="customer-aging-snapshots"></a>Aldersfordelte øjebliksbilleder for debitor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om aldersfordelte øjebliksbilleder for debitorer. Et aldersfordelt øjebliksbillede beregner aldersfordelte saldi for en gruppe debitorer på et bestemt tidspunkt. Du kan oprette poster for aldersfordelte øjebliksbilleder enten for alle kunder eller for kunderne i kundepuljen.

Oplysninger fra aldersfordelte øjebliksbilleder vises på listesiden **Aldersfordelte saldi** og på siden **Rykkere**. Du skal oprette et aldersfordelt øjebliksbillede, før du kan bruge listesiden **Aldersfordelte saldi**. Listesiden viser kun kunder, der allerede er oprettet et aldersfordelt øjebliksbillede for.

Arbejdsområdet **Kundekredit og inkasso** viser også aldersfordelingen for kunder. Yderligere oplysninger finder du i [Styring af kredit og inkasso Power BI-indholdet](credit-collections-power-bi.md).

> [!NOTE]
> Hvis du vil reducere den tid, det tager at oprette et aldersfordelt øjebliksbillede, skal du aktivere følgende funktioner i arbejdsområdet **Funktionsstyring**: 
> - **Forbedret ydeevne af aldersfordelte debitorer** 
> - **Forbedret ydeevne af aldersfordeling af kunder med kundepuljer**  
>Når begge funktioner er aktiveret, kan **kundepuljer** bruges til oprettelse af det aldersfordelte øjebliksbillede. 

Når du opretter et aldersfordelt øjebliksbillede for debitorer, skal du bruge følgende felter til at angive oplysninger om det:

- **Definition af forældelsesperiode** – Vælg definitionen på forældelsesperioden for det aldersfordelte øjebliksbillede. Du kan have ét aldersfordelt øjebliksbillede for hver definition af forældelsesperioder. Det aldersfordelte øjebliksbillede og definitionen af forældelsesperioden skal oprettes separat.
- **Pulje-id** – Det er valgfrit, om du vil udfylde feltet. Du kan bruge en pulje til at definere det sæt kunder, der skal behandles i det aldersfordelte øjebliksbillede. Hvis du vælger en kundepulje i dette felt, oprettes der kun et aldersfordelt øjebliksbillede for de debitorkonti, der indgår i kundepuljen. Den valgte kundepulje skal være af typen **Aldersfordelt øjebliksbillede**. Hvis du ikke udfylder dette felt, oprettes der et aldersfordelt øjebliksbillede for alle debitorkonti.


- **Kriterier** – Aldersfordelt øjebliksbillede forældes baseret på den dato, du vælger:

    - **Posteringsdato** – Hver transaktion forældes baseret på transaktionsdatoen.
    - **Forfaldsdato** – Hver transaktion forældes baseret på forfaldsdatoen.
    - **Dokumentdato** – Hver transaktion forældes baseret på dokumentdatoen.

- **Aldersfordeling pr.** – Vælg den type dato, der skal bruges i feltet **Dags dato** for det aldersfordelte øjebliksbillede. Forældelsesperioder beregnes derefter på grundlag af denne dato. 

    - **Dags dato** – Brug systemdatoen. Vælg denne indstilling, hvis behandling er indstillet til at køre som et tilbagevendende batchjob. Hver gang batchen køres, bruges systemdatoen for kørslen.
    - **Valgt dato** – Brug en dato, du angiver. Hvis du vælger denne indstilling, skal du angive en aldersfordelingsdato.

   Den aktuelle forældelsesperiode er f.eks. 30 dage. Hvis du vælger **Dags dato** i dette felt, starter den aktuelle forældelsesperiode på dags dato og medtager derefter de foregående 29 dage. Hvis du vælger **Valgt dato** og angiver en dato, starter den aktuelle forældelsesperiode på den angivne dato og medtager derefter de foregående 29 dage.

- **Opdater rykkerstatus** – Vælg **Ja** i denne indstilling for at opdatere rykkerstatussen for transaktioner på siden **Rykkere** fra **Løfte om betaling** til **Brudt betalingsløfte**, hvis forældelsesdatoen ligger efter datoen i feltet **Dato for løfte om betaling**. Vælg **Nej** i denne indstilling for at lade rykkerstatus være uændret på siden **Rykkere**.
- **Medtag debitorer med nul-saldi**– Vælg **Ja** i denne indstilling, hvis du vil medtage alle debitorer uanset deres saldo. Hvis du medtager alle debitorer, anbefales det, at du aktiverer funktionerne **Forbedret ydeevne af aldersfordelte debitorer** og **Forbedret ydeevne af aldersfordeling af kunder med kundepuljer**. Vælg **Nej** i denne indstilling, hvis du kun vil medtage debitorer, der har en saldo. Denne indstilling er med til at øge ydeevnen, da kunder, der ikke har en saldo, springes over.
- **Undgå beregning af kreditmaksimum under forældelse** – Hvis denne indstilling er angivet til **Ja**, kan forældelsesprocessen ikke beregne beløbene **Subtotal på følgeseddel**, **Subtotal for åben ordre** og **Kredit** for hver kunde. Disse saldi vises på siden **Aldersfordelte saldi** i FactBox under **Kreditmaks**. Angiv denne indstilling til **Ja**, hvis du vil have en hurtigere performance under forældelsesprocessen. Angiv det til **Nej** for at genberegne saldi, når du kører forældelsesprocessen. 
- **Firmaområde** – Under fanen **Firmaområde** skal du vælge de juridiske enheder (firmaer), der skal medtages i det aldersfordelte øjebliksbillede. Kun juridiske enheder, der er konfigureret til centraliserede betalinger, kan vælges. Posteringer fra de valgte juridiske enheder medtages derefter i forældelsesperioderne for debitorer, der har samme part-id i alle disse juridiske enheder. Valutabeløb konverteres til valutaen for den juridiske enhed, du er logget på, når du opretter det aldersfordelte øjebliksbillede.

Det anbefales, at du planlægger, at denne proces køres i en batch.

> [!NOTE]
> Hvis du vil forbedre batchydeevnen, når der oprettes aldersfordelte øjebliksbilleder, skal du angive et tal i feltet **Maksimalt antal batchopgaver** i oversigtspanelet **Rykkerstandard** under fanen **Rykkere** på siden **Debitorparametre**. I feltet **Aldersfordel kundesaldi** anbefales det, at du starter med en værdi mellem **12** og **20** og derefter justerer værdien for at optimere behandlingen til dit behov. Det anbefales ikke at angive denne værdi, der er større end **30**, da det vil have indflydelse på ydeevnen. 

