---
title: Bølgetrinskoder
description: Dette emne indeholder en oversigt over bølgetrinskoder, og hvordan de bruges.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992351"
---
# <a name="wave-step-codes"></a>Bølgetrinskoder

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Om bølgetrinskoder

Bølgetrinskoder er koder, som brugerne kan konfigurere og bruge til at knytte bestemte forekomster af bølgemetoder til en tilsvarende skabelon. Skabelonerne indeholder skabeloner til genopfyldning, containerisering, etiketudskrivning, lastopbygning og sortering.

Når der ikke bruges bølgetrinskoder, skal brugerne angive en fri tekst for at referere til en bestemt skabelon fra forekomsten af bølgemetoden. Der er fejlrisiko for fri tekst, fordi brugerne skal sørge for, at den bølgetrinstekst, som de føjer til en bestemt bølgetrinsmetode i i en bølgeskabelon, nøjagtigt svarer til bølgetrinsteksten i destinationsskabelonen.

Bølgetrinskoder for en specifik bølgetrinstype oprettes på en separat side. For hver forekomst af en bølgetrinsmetode i en bølgeskabelon, der kræver en bølgetrinskode, skal bølgetrinskoden være valgt på en rulleliste. Valg på en rulleliste erstatter indtastning af fritekst og hjælper med at reducere risikoen og virkningerne af menneskelige fejl. Opsætningskoder bruges til at sammenkæde en bølgetrinsmetode i en bølgeskabelon med en destinationsskabelon for metoden.

> [!NOTE]
> Det er valgfrit at bruge funktionen for bølgetrinskoder, og inddragelse sker pr. juridisk enhed. Hvis en bestemt juridisk enhed bruger funktionen, bliver alle eksisterende bølgetrinskoder i den juridiske enhed derfor opgraderet til den nye struktur.

## <a name="setup-demo"></a>Installationsdemo 

Til denne demo skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.

### <a name="enable-wave-step-codes"></a>Aktivér bølgetrinskoder

Udfør følgende trin for at aktivere funktionen for bølgetrinskoder.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
2. Under fanen **Generelt** på oversigtspanelet **Bølgebehandling** skal du vælge **Ja** i indstillingen **Aktivér bølgetrinskoder**.

Alle eksisterende fritekster til bølgetrin opgraderes til den nye struktur. Når denne opgradering er fuldført for en juridisk enhed, er indstillingen **Aktiver bølgetrinskoder** ikke længere tilgængelig på siden **Parametre til lokationsstyring**.

Valideringer udføres under opgraderingen, og hvis opgraderingen mislykkes, får du vist en fejlmeddelelse. En opgradering kan mislykkes på grund af følgende konflikter:

- Der findes identiske fritekster til bølgetrin.
- Tilpasninger findes.
- Et fritekst til bølgetrin, der er knyttet til en forekomst af bølgetrinsmetoden, stemmer ikke overens med den forventede skabelontype.

Når du har løst eventuelle konflikter, der er identificeret under valideringerne, kan du køre opgraderingsprocessen igen.

Når opgraderingen lykkes, bliver siden **Bølgetrinskoder** (**Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder**) tilgængelig. Denne side viser de bølgetrinskoder, der blev opgraderet, da funktionen bølgetrinskoder blev slået til.

### <a name="create-new-wave-step-codes"></a>Oprette nye bølgetrinskoder

Du kan bruge siden **Bølgetrinskoder** til at oprette og slette bølgetrinskoder.

Alle nye bølgetrinskoder og deres tilknyttede id skal være entydige på tværs af alle bølgetrinstyper, og de skal defineres for en bestemt bølgetrinstype.

### <a name="apply-wave-step-codes"></a>Anvende bølgetrinskoder

Når du har defineret de relevante bølgetrinskoder, kan de anvendes på bølgeprocesmetoderne.

Du kan anvende bølgetrinskoder ved at gå til den relevante destinationsskabelon. Her er de destinationsskabeloner, som bølgetrinskoderne peger på:

- **Genopfyldningsskabeloner:** Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner.
- **Lastopbygningsskabeloner** Lokationsstyring \> Konfiguration \> Last \> Lastopbygningsskabeloner
- **Sorteringsskabeloner:** Lokationsstyring \> Konfiguration \> Emballage \> Udgående sorteringsskabeloner
- **Containeriseringsskabeloner:** Lokationsstyring \> Konfiguration \> Containere \> Skabeloner til containerbygning
- **Labeludskrivningsskabeloner:** Lokationsstyring \> Konfiguration \> Dokumentrute \> Bølgelabelskabeloner

Skabelonerne på denne liste anvendes, når der refereres til dem fra en bølgeprocesmetode, der er valgt i en bølgeskabelon. Når bølgetrinskoden på en bølgeprocessmetode i en bølgeskabelon svarer til bølgetrinskoden i en af skabelontyperne, anvendes skabelonen.

### <a name="sample-scenario"></a>Eksempelscenario

Følgende procedure hjælper med at sikre, at den genopfyldningsskabelon, du har oprettet, anvendes på bølgeskabelonen.

1. Gå ti **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder**, og opret en bølgetrinskode til typen **Genopfyldning**.
2. Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner** , og opret en genopfyldningsskabelon.
3. Vælg den bølgetrinskode, du har oprettet til **Genopfyldning**-typen, i genopfyldningsskabelonen.
4. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**, og vælg den bølgeskabelon, du vil bruge.
5. Vælg **Genbestilling**-metoden i oversigtspanelet **Metoder** i skabelonen.
6. Vælg den bølgetrinskode, du har oprettet i genopfyldningsskabelonen, i feltet **Kode for bølgetrin**.
