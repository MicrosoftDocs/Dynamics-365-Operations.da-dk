---
title: Likviditet
description: Denne artikel beskriver, hvordan funktionen likviditetsbudgettering forudsiger en organisations kontante stilling for bestemte tidspunkter. Den beskriver også de indstillinger, der er tilgængelige for visning af budgetter i forskellige perioder.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870243"
---
# <a name="cash-position"></a>Likviditet

[!include [banner](../includes/banner.md)]

Likviditeten er den projektion af likviditeten, der er prognose for den nærmeste periode. Den er baseret på indregningen af indbetalinger fra debitorer, der skal betale udestående fakturaer og ordrer og også til de kontantbetalinger, der betales til kreditorer for indkøbsfakturaer og -ordrer.

Når systemet forudsiger debitorbetalinger, bruger det betalingsforudsigelserne fra funktionen til forudsigelse af debitorbetaling. Uden betalingsforudsigelser bruges den gennemsnitlige tid, der kræves for at konvertere en debitorfaktura til en betaling for hver debitor, til beregning af en betalingsdato. Ved åbne kundeordrer beregner systemet fakturadatoen ved hjælp af det gennemsnitlige antal dage til ordrelinjerne pr. kunde, der skal faktureres. Derefter bruger programmet fakturadatoen som et input til funktionen til betalingsforudsigelse. Funktionaliteten til forudsigelse af debitorbetaling beregner en betalingsdato for hver ordrelinje. 

Betalingsdatoen for udestående fakturaer er estimeret fra betalingsforudsigelser ved at vælge en dato, der svarer til halvtredsindtyvende percentil for den kumulative fordelingsfunktion, der er opnået fra det forudsagte filsæts sandsynligheder.

En lignende fremgangsmåde bruges til at forudsige betalinger til kreditorer. For hver leverandør beregner systemet den gennemsnitlige tid, der kræves for at konvertere en kreditorfaktura til en betaling. Dette antal dage anvendes derefter til at beregne betalingsdatoen. I forbindelse med åbne kreditorordrer beregner systemet fakturadatoen ved at overveje det gennemsnitlige antal dage, der kræves for at konvertere ordrelinjer til en faktura for hver kreditor. Systemet beregner derefter betalingsdatoen ved at anvende den gennemsnitlige tid, der kræves for at konvertere en kreditorfaktura til en betaling for hver kreditor.

Den øverste del af fanen **Likviditet** indeholder et likviditetsdiagram. Dette diagram viser kontantindstrømning og -udstrømning samt deres indvirkning på den samlede likviditetssaldo. Oplysningerne i diagrammet over likviditetsbeholdningen kan vises i daglige, ugentlige, månedlige eller kvartalsvise perioder. Når du vælger **Dagligt**, kan du få vist budgetter for de næste 21 dage. Når du vælger **Ugentligt**, kan du få vist budgetter for de næste 20 uger. Når du vælger **Månedligt**, kan du få vist budgetter for de næste 12 måneder. Når du vælger **Kvartårligt**, kan du få vist budgetter for de næste 12 kvartaler. Du kan skjule diagrammet, hvis du har brug for mere plads på skærmen til at få vist indholdet under fanen **Likviditet**.

Den nederste del af fanen **Likviditet** indeholder oplysninger om stilling, pengestrøm, forventede betalinger og bankkonti.

- Oplysningerne i gitteret med **Stillingsoplysninger** vises i tre sektioner: En liste over likviditetskonti, en liste over dokumenter, der udgør pengestrømme, og en liste over dokumenter, der udgør udgående pengestrømme. I gitteret vises også saldi for likvide midler. For den første periode, du får vist, er saldoen for likviditetskontis startsaldo. For efterfølgende perioder beregnes saldiene for likviditetskontiene ud fra tilføjelse af kontantindstrømning og subtraktion af udgående pengestrømme fra tidligere perioder. Hvis du vil have vist detaljer om de posteringer, saldoen består af, skal du vælge lniket **Saldo**.
- Gitteret **Likviditet** viser indgående pengestrømme, aggregerede pengestrømme pr. periode og deres indvirkning på likviditetskonti. For den første periode, er saldoen for likviditetskontis startsaldo. For efterfølgende perioder beregnes saldiene for likviditetskontiene ud fra tilføjelse af kontantindstrømning og subtraktion af udgående pengestrømme fra tidligere perioder.
- Gitteret for den **forventede banksaldo** viser forventede kontantudstrømninger og deres indvirkning på likviditetskonti.
- **Bankkonto**-gitteret viser effekten af forventede kontantindstrømning og -udstrømering på banksaldoen.

Hvis du vil gemme og redigere likviditeten, skal du oprette et snapshot. Du kan finde flere oplysninger om, hvordan du arbejder med snapshots, under [Snapshots, oversigt](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Oplysninger om muligheden for likviditet 

Funktionen til likviditet indeholder følgende funktioner. 

- Funktionen til likviditet viser pengestrømmen baseret på eksisterende dokumenter i systemet og indgående og udgående likviditetslinjer, der er importeret fra eksterne systemer.
- Gør det nemt at integrere pengestrømsdata fra eksterne systemer med Dynamics 365 Finance. Likviditet kan også bruge dataimport-eksportstrukturen. Denne struktur gør det nemt at integrere med Excel OData. Du kan også kombinere data fra flere kilder for at oprette en omfattende likviditetsløsning.
- Introducerer intelligent kasseposition. Der oprettes en likviditet på baggrund af kundens betalingsmåde for at forudsige, hvornår et firma kan forvente at betale kontanter i deres konti.
- For debitorordrer og -fakturaer bruges AI-forudsigelsesfunktionaliteten for debitorbetaling til at bestemme den historiske debitorbetalingsadfærd, når en ordre eller faktura betales.
- I forbindelse med kreditorordrer og -fakturaer bruger vi den gennemsnitlige tid mellem afsendelse og faktura og betaling af en faktura pr. kreditor til at bestemme, hvornår en kreditorordre eller -faktura vil blive betalt, hvilket gør udgående likviditet mere nøjagtig.

Det giver et mere præcist overblik over likviditet baseret på kassererens historiske betalingsadfærd. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
