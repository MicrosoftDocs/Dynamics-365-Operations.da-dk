---
title: Konfigurere og bruge betal ved betaling for kreditorbetalinger
description: I dette emne forklares det, hvordan du opretter vilkår for betal ved betaling, så du kan frigive delvise kreditorbetalinger baseret på debitorbetalinger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284107"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Konfigurere og bruge betal ved betaling for kreditorbetalinger

[!include [banner](../includes/banner.md)]

Når du godkender en leverandør til at arbejde som underleverandør, kan du vælge at tilbageholde betaling til leverandøren eller underleverandøren, indtil kunden betaler dig for projektet. Hvis du vil understøtte dette scenarie, kan du oprette betingelserne for betal ved betaling, når du opretter indkøbsordren til leverandøren.

Når en kunde betaler et beløb på en projektfaktura, kan du f.eks. frigive noget af eller hele kreditorfakturabeløbet. Du skal bare oprette betingelser for betal ved betaling, der angiver, at en kreditor betales, når du har modtaget en bestemt procentdel af den relaterede betaling fra kunden. Hvis du modtager en delvis betaling fra en kunde, kan du manuelt frigive nogle af de tilknyttede kreditorfakturaer til betaling.

I følgende eksempel vises processen, når du bruger betingelser for betal ved betaling.

## <a name="example"></a>Eksempel

Din organisation indvilliger i at levere 100 computere til en kunde, hvor der er installeret software, til en pris af 150 amerikanske dollar (USD) pr. computer. Derefter hyrer du en leverandør til at levere de computere, hvor softwaren er installeret, til dig. Ifølge aftalen skal kunden godkende kvaliteten af computerne, før kunden betaler din organisation. Din organisations politik er at tilbageholde betaling til leverandører, indtil kunden har betalt dig. Derfor konfigurerer du projektet, så det har en procentvis betal ved betaling på 100 %.

Leverandøren sender dig 100 computere, der har software installeret, sammen med en faktura på 10.000 USD. Da betal ved betaling-betingelser er oprettet for projektet, betaler du ikke leverandøren ved modtagelsen af computerne. Du sender i stedet computerne til kunden sammen med en faktura på 15.000. Kunden undersøger computerne og godkender hele beløbet på projektfakturaen.

Når du modtager den fulde betaling fra kunden, betaler du leverandøren det fulde beløb på kreditorfakturaen, 10.000.

## <a name="set-up-pwp-terms-for-a-project"></a>Oprette betingelser for betal ved betaling for et projekt

Når du konfigurerer betingelser for betal ved betaling for et projekt, skal du som en procentdel angive det minimumbeløb, som en kunde skal betale dig for projektet, før du betaler leverandøren. Grænsebeløbet beregnes automatisk på debitorfakturaerne for projektet. Hvis du vil konfigurere grænseprocenten i betingelser for betal ved betaling, skal du gøre følgende.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. Find og åbn det projekt, som du vil konfigurere betingelser for betal ved betaling for.
3. I oversigtpanelet **Kreditoraftaler** skal du vælge **Tilføj linje**.
3. Vælg én af følgende indstillinger i feltet **Kontokode**:

    - **Tabel** – Betingelserne for betal ved betaling gælder for en enkelt kreditor.
    - **Gruppe** – Betingelserne for betal ved betaling gælder for alle kreditorer i en kreditorgruppe.
    - **Alle** – Betingelserne for betal ved betaling gælder for alle kreditorer.

4. Hvis du har valgt **Tabel** eller **Gruppe** i det forrige trin, skal du i feltet **Kreditor/kreditorgruppe** vælge den kreditor eller kreditorgruppe, som betingelserne for betal ved betaling gælder for. Hvis du har valgt **Alle** i det foregående trin, kan feltet **Kreditor/kreditorgruppe** ikke redigeres.
5. Hvis projektet også har kreditortilbageholdelsesbetingelser konfigureret, skal du i feltet **Tilbageholdelsesbetingelser for kreditor** vælge Regel-id for tilbageholdelsesbetingelserne.
6. Angiv grænseprocenten for projektet i feltet **Grænseværdi for Betal ved betaling i procent**. Den procentsats, du angiver for projektet, er det mindste beløb, som kunden skal betale dig, før du betaler leverandøren.

## <a name="create-a-po-that-has-pwp-terms"></a>Oprette en indkøbsordre, der har betal ved betaling-betingelser

Når du bogfører en faktura fra en kreditor, og kreditoren er underlagt betingelser for betal ved betaling, står disse betingelser på indkøbsordrelinjerne. Hvis du vil oprette en indkøbsordre, der indeholder betingelser for betal ved betaling, skal du følge disse trin.

1. Gå til **Indkøb og forsyning** \> **Indkøbsordrer** \> **Alle indkøbsordrer**.
2. Gå til handlingsruden, og vælg **Ny**. Angiv de nødvendige oplysninger i dialogboksen **Opret indkøbsordre**, og vælg **OK**.

    Du kan også åbne en eksisterende indkøbsordre på listesiden **Alle indkøbsordrer**.

4. Gennemse oplysningerne på indkøbsordrelinjen for kreditoren i oversigtspanelet **Indkøbsordrelinjer** på siden **Indkøbsordre**. Indstillingen **Betal ved betaling** markeres automatisk, og værdien i feltet **Grænseværdi for Betal ved betaling i procent** kopieres automatisk til fra feltet **Grænseværdi for Betal ved betaling i procent** på siden **Projektet**.
6. Hvis du ikke vil anvende betal ved betaling-betingelser for leverandøren på en indkøbsordrelinje, skal du fjerne markeringen af indstillingen **Betal ved betaling**. I dette tilfælde vil feltet **Grænseværdi for Betal ved betaling i procent** for indkøbsordrelinjen blive nulstillet til 0 (nul).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Opdatere en kundebetaling og betale leverandøren

Når en leverandør færdiggør sit arbejde på et projekt og sender dig en faktura, skal du gennemgå projektets status og debitorfakturaerne for at se, om betingelserne for betal ved betaling er opfyldt for projektet. Hvis betal ved betaling-betingelserne for kreditoren er opfyldt, kan du afgøre, hvilke linjer på kreditorfakturaen, der skal betales, baseret på debitorbetalingerne for projektet. Hvis du beslutter at betale kreditoren, selvom betingelserne for betal ved betaling ikke er opfyldt, kan du tilsidesætte betingelserne for betal ved betaling på siden **Kreditorfakturaer med betal ved betaling**.

1. Gå til **Projektstyring og regnskab** \> **Forespørgsler og rapporter** \> **Tilbageholdelsesforespørgsler** \> **Kreditorfakturaer med betal ved betaling**.
2. Angiv værdier i søgefeltet på siden **Kreditorfakturaer med betal ved betaling** for at finde den kreditorfaktura, du vil gennemgå, og vælg derefter **Søg**.
3. Vælg de linjer, du vil ændre, i oversigtspanelet **Kreditorfakturalinjer**.
4. Hvis betingelserne for **Betal ved betaling** er opfyldt for fakturalinjen, skal du vælge **Frigiv kreditorbetaling**. Markeringen i afkrydsningsfeltet **Betal ved betaling** fjernes, og værdien af feltet **Klar til betaling** ændres til **Ja**.
