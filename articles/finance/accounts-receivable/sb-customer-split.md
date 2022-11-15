---
title: Debitoropdeling på faktureringstidsplaner
description: I denne artikel beskrives, hvordan du opdeler en debitor, når der bruges abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746310"
---
# <a name="customer-split-on-billing-schedules"></a>Debitoropdeling på faktureringstidsplaner

På en faktureringsplan er *fakturakontoen* den debitor, der modtager salgsordrefakturaen, så de kan betale fakturaen. I nogle scenarier kan mere end én debitor betale en faktura. Du kan bruge funktionen **Debitoropdeling** til at tilføje flere debitorer, der kan faktureres for samme faktureringsplan. Du kan aktivere denne funktion ved at gå til **Fakturering af abonnement \> Tilbagevendende kontraktfakturering \> Opsætning \> Parametre for tilbagevendende kontraktfakturering** og angive indstillingen **Debitoropdeling** til **Ja**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Debitoropdeling på faktureringstidsplanens overskrift

Når der er oprettet en faktureringsplan, kan der føjes flere kunder til faktureringsplanoverskriften.

Hvis du vil tilføje en kunde, skal du følge disse trin.

1. Vælg **Debitoropdeling** under fanen **Faktureringsplan**. I felterne **Debitorkonto** og **Debitorkontonavn** øverst angives den debitor, der er tildelt som **Faktureringsplankunde**.

    > [!NOTE]
    > Den debitorkonto, du tilføjer, kan ikke være den samme som fakturakontoen.

2. Vælg **Tilføj linje** under fanen **Debitoropdelte linjer**.
3. Vælg en debitor, og angiv derefter procentdelen af hver faktura for den pågældende debitor.
4. Start- og slutdatoerne i faktureringsplanen bruges som standard som start- og slutdatoer. Angiv andre start- og slutdatoer, hvis den nye kunde kun skal betale den angivne procentdel for en del af faktureringsplanen. Hvis faktureringsplanen f.eks. har startdatoen 1. januar og slutdatoen 31. december, og den nye kunde faktureres 40 procent for de første ni måneder, skal du angive 1. januar som startdato og 30. september som slutdato og angive **40,00** som procent.

Du kan føje mere end én debitor til de debitoropdelte linjer. I dette tilfælde må den angivne samlede procentdel ikke overstige 100 procent. Angiv en debitorreference og en debitorrekvisition som oplysningsfelter, der vises på salgsordrelinjen under processen **Opret faktura**.

Linjedetaljerne viser kontaktoplysninger, leveringsadresse, faktureringsadresse og betalingsoplysninger for de tilføjede debitorer. Disse oplysninger vises også på salgsordren for kunderne.

Når du føjer debitoropdelte oplysninger til hovedet i faktureringsplanen, og der er ikke-fakturerede faktureringsplanlinjer i faktureringsplanen, modtager du følgende meddelelse, hvor du bliver bedt om at rulle ændringerne ned: "Vil du rulle ændringen fra hovedet ned til linjerne? Ændringer opdaterer kun de faktureringsplanlinjer, der ikke er faktureret." Vælg **Ja** for at opdatere oplysningerne om debitoropdeling i faktureringsplanlinjen. Ændringer opdateres ikke, hvis faktureringsplanlinjen allerede er faktureret.

Hvis der oprettes en faktureringsplan ved hjælp af indstillingen **Kopiér tidsplan**, angives der standardoplysninger på overskriftslinjer i debitoropdelingen. Den kan ikke være den samme som debitorkontoen.

Når processen **Opret faktura** er fuldført, oprettes der flere salgsordrer. (Der oprettes også flere salgsfakturaer, hvis der bruges automatisk bogføring). Disse salgsordrer og salgsfakturaer kan ses under fanen **Faktura** i oversigtspanelet **Linjedetaljer** på siden **Vis faktureringsdetaljer**. **Flere** vises på faktureringsdetaljelinjen for at angive, at der er oprettet flere salgsordrer og salgsfakturaer.

## <a name="customer-split-on-billing-schedule-lines"></a>Debitoropdeling på linjer i faktureringsplan

Debitoropdelingen kan føjes til individuelle faktureringsplanlinjer, hvis du kun vil opdele bestemte faktureringsplanlinjer. Markér afkrydsningsfeltet **Debitoropdeling** på linjen, og vælg derefter **Debitoropdeling** i menuen for faktureringsplanlinjen for at opdatere eller angive oplysningerne om debitoropdeling.

Revisionsoplysningerne opdateres, hvis faktureringsplanen allerede er faktureret, men procentsatsen derefter er ændret på faktureringsplanlinjen. Alle linjer, der faktureres efter ændringen, vil bruge den nye procent.

> [!NOTE]
> - Indstillingen Debitoropdeling kan ikke bruges til lagervarer.
> - Hvis afkrydsningsfeltet **Ikke-afregnet indtægt** er markeret, kan afkrydsningsfeltet **Debitoropdeling** ikke markeres.
> - Hvis du kun bruger indstillingen **Indtægtsopdelt**, har den overordnede linje indstillingen **Debitoropdeling**, men det har de underordnede linjeelementer ikke.
