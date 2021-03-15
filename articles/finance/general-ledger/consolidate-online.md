---
title: Økonomiske konsolideringer online
description: I dette emne beskrives økonomiske onlinekonsolideringer i Finans.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 91df786ed2298e21e7a3018b915c9bd5458efc32
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009237"
---
# <a name="online-financial-consolidations"></a>Økonomiske konsolideringer online

[!include [banner](../includes/banner.md)]

I dette emne beskrives økonomiske onlinekonsolideringer i Finans. Inden du læser dette emne, skal du læse emnet [Oversigt over økonomiske konsolideringer og valutaomregning](financial-consolidations-currency-translation.md).

Når du har fuldført opsætningen, kan du angive detaljerne om konsolideringen på siden **Konsolider [Online]**. Når du er færdig, kan du klikke på **OK** eller **Batch** for at behandle konsolideringen.

## <a name="criteria"></a>Afgrænsning
Under fanen **Kriterier** på siden **Konsolider [Online]** kan du definere kontiene, perioderne og typen af data, der konsolideres.

![Fanen kriterier](./media/criteria-consolidate-online.png "Fanen kriterier")

Her er en forklaring på de forskellige felter under denne fane:

- **Beskrivelse** – Angiv en præcis beskrivelse af den periode, som du konsoliderer.
- **Hovedkonto** – Brug felterne i denne sektion til at definere de hovedkonti, som vil blive behandlet.

    - **Fra** og **Til** – Angiv et interval af konti, der skal behandle. Hvis du ikke udfylder disse felter, flyttes alle konti fra alle firmaer til det konsoliderede regnskab. Derfor, hvis du konsoliderer fire firmaer, og hvert firma har en anden kontoplan, oprettes alle konti fra alle fire firmaer i det konsoliderede regnskab.
    - **Brug koncernkonto** – Hvis du angiver denne indstilling til **Ja**, bliver feltet **Vælg koncernkonto fra** tilgængeligt. I dette felt kan du vælge, om alle konti skal konsolideres til den konsoliderede konto, der er angivet på siden **Hovedkonti**, eller om du vil vælge kontoen i en af koncernkontogrupperne.
    - **Koncernkontogruppe** – Vælg den gruppe, der skal bruges til tilknytningen af hovedkontoen for konsolideringen.

- **Konsolideringsperiode** – Brug felterne i denne sektion til at definere konsolideringsperioden.

    - **Fra** og **Til** – Angiv et datointerval for konsolideringen. Hvis du ikke udfylder disse felter, bliver konsolideringen behandlet for alle perioder, der er defineret i finanskalenderen for firmaet. Det anbefales ikke at udfylde disse felter.
    - **Medtag faktiske beløb** – Angiv denne indstilling til **Ja** for at konsolidere dine faktiske data.
    - **Medtag budgetbeløb** – Angiv denne indstilling til **Ja** for at konsolidere data fra budgetregisteret.
    - **Gendan saldi under konsolidering** – Vi anbefaler, at du ikke vælger **Ja** i denne indstilling. Gendan i stedet saldi som et separat batchjob.

- **Budgetmodeller** – Hvis du har valgt at konsolidere budgetdata, skal du bruge felterne i denne sektion til at definere budgetmodellerne.

    - **Fra** og **Til** – Angiv det interval af konti, der skal bruges.
    - **Budgetkurstype** – Vælg den budgettype, der skal bruges til valutaomregning for budgetdata.

## <a name="financial-dimensions"></a>Økonomiske dimensioner
Under fanen **Økonomiske dimensioner** skal du definere de dimensioner, der skal medtages i det konsoliderede regnskab. Du kan vælge en dimension ved at indstille feltet **Specifikation** til **Dimension** og derefter definere rækkefølgen for dimensionen i det konsoliderede regnskab.

![Fanen økonomiske dimensioner](./media/financial-dimensions-cons.png "Fanen økonomiske dimensioner")

Uanset hvilken rækkefølge du definerer, er **Hovedkonto** altid det første segment.

## <a name="legal-entities"></a>Juridiske enheder
Under fanen **Juridiske enheder** skal du definere de firmaer, der skal medtages i det konsoliderede regnskab. Du kan også definere ejerskabsprocentdelen for disse firmaer. Hvis du angiver mindre end 100 procent ejerskab, bliver den angivne procentdel aggregeret til det konsoliderede regnskab. For enhver omregningsdifference bruges feltet **Kontotype til omregningsdifferencer** til at vælge hovedkontoen fra opsætningen på siden **Konti til automatisk posteringer**.

![Fanen juridiske enheder](./media/legal-entities-cons.png "Fanen juridiske enheder")

![Siden konti til automatisk posteringer](./media/accounts-for-automatic-cons.png "Siden konti til automatisk posteringer")

## <a name="elimination"></a>Eliminering
Under fanen **Eliminering** har du tre muligheder for at behandle elimineringer:

- Vælg elimineringsreglen, og vælg derefter **Kun forslag** i feltet **Forslagsmuligheder**. Denne indstilling vil behandle elimineringen under konsolideringsprocessen, men den kan ikke bogføre alt på én gang. Du kan bogføre kladden senere.
- Vælg elimineringsreglen, og vælg derefter **Kun bogføring** i feltet **Forslagsmuligheder**. Denne indstilling vil behandle elimineringen under konsolideringsprocessen og bogfører alt på én gang.
- Kør et elimineringsforslag separat fra konsolideringsprocessen ved hjælp af elimineringskladden.

![Fanen eliminering](./media/elimination-cons-onl.png "Fanen eliminering")

Du kan finde flere oplysninger om elimineringer i [Elimineringsregler](./elimination-rules.md).

## <a name="currency-translation"></a>Valutaomregning
Under fanen **Valutaomregning** kan du definere den juridiske enhed, kontoen og valutakurstypen og kursen. Der findes tre muligheder i feltet **Anvend valutakurs fra**:

- **Konsolideringsdato** – Datoen for konsolideringen bruges til at hente valutakursen. Denne kurs svarer til spotsatsen eller kursen ved månedens afslutning. Du kan se en forhåndsvisning af kursen, men du kan ikke redigere den.
- **Posteringsdato** – Datoen for hver postering, der skal bruges til at vælge en valutakurs. Denne indstilling bruges oftest til anlægsaktiver og kaldes ofte en historisk kurs. Du kan ikke se en forhåndsvisning af satsen, fordi der vil være mange satser for de forskellige transaktioner i kontointervallet.
- **Brugerdefineret sats** – Når du vælger denne indstilling, kan du angive den valutakurs, som du ønsker. Denne indstilling kan være praktisk ved gennemsnitlige valutakurser, eller hvis du konsoliderer mod en fast valutakurs.

![Fanen valutaomregning](./media/currency-translation-cons-online.png "Fanen valutaomregning")

## <a name="additional-resources"></a>Yderligere ressourcer

Du kan finde flere oplysninger om konsolidering og valutaomregning i det overordnede emne til dette emne, [Oversigt over økonomiske konsolideringer og valutaomregning](./financial-consolidations-currency-translation.md).

Oplysninger om scenarier, hvor du kan generere konsoliderede regnskaber, finder du i [Generere konsoliderede regnskaber](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]