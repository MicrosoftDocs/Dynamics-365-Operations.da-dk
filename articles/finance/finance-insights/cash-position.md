---
title: Likviditet (prøveversion)
description: Dette emne beskriver, hvordan funktionen likviditetsbudgettering forudsiger en organisations kontante stilling for bestemte tidspunkter. Den beskriver også de indstillinger, der er tilgængelige for visning af budgetter i forskellige perioder.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: ffe91d7ca273de36c2fae58a39d3a3d306496990
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208575"
---
# <a name="cash-position-preview"></a>Likviditet (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Likviditeten er den projektion af likviditeten, der er prognose for den nærmeste periode. Den er baseret på indregningen af indbetalinger fra debitorer, der skal betale udestående fakturaer og ordrer og også til de kontantbetalinger, der betales til kreditorer for indkøbsfakturaer og -ordrer.

Når systemet forudsiger debitorbetalinger, bruger det betalingsforudsigelserne fra funktionen til forudsigelse af debitorbetaling. Uden betalingsforudsigelser bruges den gennemsnitlige tid, der kræves for at konvertere en debitorfaktura til en betaling for hver debitor, til beregning af en betalingsdato. Ved åbne kundeordrer beregner systemet fakturadatoen ved hjælp af det gennemsnitlige antal dage til ordrelinjerne pr. kunde, der skal faktureres. Derefter bruger programmet fakturadatoen som et input til funktionen til betalingsforudsigelse. Funktionaliteten til forudsigelse af debitorbetaling beregner en betalingsdato for hver ordrelinje. 

<*Du skal bruge tekst fra Jarek eller Dave angående, hvordan betalingsforudsigelser konverteres til en dato*> Betalingsdatoen for udestående fakturaer er cirka [*estimeret*] fra betalingsforudsigelser ved at vælge en dato, der svarer til halvtredsindtyvende percentil for den kumulative fordelingsfunktion, der er opnået fra det forudsagte filsæts sandsynligheder.

En lignende fremgangsmåde bruges til at forudsige betalinger til kreditorer. For hver leverandør beregner systemet den gennemsnitlige tid, der kræves for at konvertere en kreditorfaktura til en betaling. Dette antal dage anvendes derefter til at beregne betalingsdatoen. I forbindelse med åbne kreditorordrer beregner systemet fakturadatoen ved at overveje det gennemsnitlige antal dage, der kræves for at konvertere ordrelinjer til en faktura for hver kreditor. Systemet beregner derefter betalingsdatoen ved at anvende den gennemsnitlige tid, der kræves for at konvertere en kreditorfaktura til en betaling for hver kreditor.

Den øverste del af fanen **Likviditet** indeholder et likviditetsdiagram. Dette diagram viser kontantindstrømning og -udstrømning samt deres indvirkning på den samlede likviditetssaldo. Oplysningerne i diagrammet over likviditetsbeholdningen kan vises i daglige, ugentlige, månedlige eller kvartalsvise perioder. Når du vælger **Dagligt**, kan du få vist budgetter for de næste 21 dage. Når du vælger **Ugentligt**, kan du få vist budgetter for de næste 20 uger. Når du vælger **Månedligt**, kan du få vist budgetter for de næste 12 måneder. Når du vælger **Kvartårligt**, kan du få vist budgetter for de næste 12 kvartaler. Du kan skjule diagrammet, hvis du har brug for mere plads på skærmen til at få vist indholdet under fanen **Likviditet**.

Den nederste del af fanen **Likviditet** indeholder oplysninger om stilling, pengestrøm, forventede betalinger og bankkonti.

- Oplysningerne i gitteret med **Stillingsoplysninger** vises i tre sektioner: En liste over likviditetskonti, en liste over dokumenter, der udgør pengestrømme, og en liste over dokumenter, der udgør udgående pengestrømme. I gitteret vises også saldi for likvide midler. For den første periode, du får vist, er saldoen for likviditetskontis startsaldo. For efterfølgende perioder beregnes saldiene for likviditetskontiene ud fra tilføjelse af kontantindstrømning og subtraktion af udgående pengestrømme fra tidligere perioder. Hvis du vil have vist detaljer om de posteringer, saldoen består af, skal du vælge lniket **Saldo**.
- Gitteret **Likviditet** viser indgående pengestrømme, aggregerede pengestrømme pr. periode og deres indvirkning på likviditetskonti. For den første periode, er saldoen for likviditetskontis startsaldo. For efterfølgende perioder beregnes saldiene for likviditetskontiene ud fra tilføjelse af kontantindstrømning og subtraktion af udgående pengestrømme fra tidligere perioder.
- Gitteret for den **forventede banksaldo** viser forventede kontantudstrømninger og deres indvirkning på likviditetskonti.
- **Bankkonto**-gitteret viser effekten af forventede kontantindstrømning og -udstrømering på banksaldoen.

Hvis du vil gemme og redigere likviditeten, skal du oprette et snapshot. Du kan finde flere oplysninger om, hvordan du arbejder med snapshots, under [Snapshots, oversigt](payment-snapshots.md).

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]