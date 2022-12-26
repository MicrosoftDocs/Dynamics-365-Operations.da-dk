---
title: Forespørgsel om finansudligning
description: Denne artikel beskriver forespørgselsvinduet for finansudligninger
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853118"
---
# <a name="ledger-settlement-inquiry"></a>Forespørgsel om finansudligning

[!include [banner](../includes/banner.md)]

Denne artikel beskriver det **forespørgselsvindue for finansudligninger**, der kan bruges til at få vist udlignede, ikke-udlignede eller både udlignede og ikke-udlignede finansposteringer for en regnskabsperiode.

## <a name="view-ledger-settlement-transactions"></a>Vise transaktioner for finansudligning
1.  Gå til **Finans > Forespørgsler og rapporter > Forespørgsel om finansudligning**.
2.  Brug felterne **Fra dato** og **Til dato** eller **Datointerval** til at angive et datointerval. Hvad angår forsøgssaldoen, skal datointervallet ligger inden for et enkelt regnskabsår.
3.  Vælg en eller flere hovedkonti , du vil have vist finansposteringer for, i feltet **Hovedkonti**. På rullelisten vises kun de hovedkonti, der er konfigureret til finansudligning på siden **Økonomiparametre**.
4.  Brug feltet **Økonomisk dimensionsopsætning** til at vise de økonomiske dimensioner i gitteret. Da hovedkontoen er påkrævet, vises værdien i feltet **Hovedkonto** altid som den første kolonne, selvom du vælger et økonomisk dimensionssæt, der ikke omfatter hovedkontoen.
5.  Vælg i feltet **Status**:
-   **Alle** for at få vist både udlignede og ikke-udlignede posteringer
-   **Ikke udlignet** for kun at få vise ikke-udlignede posteringer 
-   **Udlignet** for kun at få vise udlignede posteringer
6.  Vælg **Vis transaktioner**. Finansposteringer vises i gitteret ud fra de kriterier, du har angivet. Du kan eksportere resultaterne af forespørgslen til Microsoft Excel til yderligere analyse. Vælg, og hold (eller højreklik) på gitret.

### <a name="column-details"></a>Kolonnedetaljer
Gitteret på siden **Forespørgsel om finansudligning** indeholder følgende kolonner:
-   **Hovedkonto** – Dette felt er påkrævet og vises altid.
-   **Økonomiske dimensioner** – Økonomiske dimensioner vises på baggrund af den valgte økonomiske dimensionssæt.
-   **Posteringsdato** – Posteringsdatoen for finanstransaktionen.
-   **Oprindelig posteringsdato** – Hvis årsafslutning er kørt, og finansudligning er konfigureret, så oplysningerne for en hovedkonto bevares, overføres de ikke-afviklede, detaljerede posteringer som en startsaldo. Den oprindelige bogføringsdato for finansposteringen vedligeholdes i feltet **Oprindelig posteringsdato**.
-   **Transaktionsalder** – Værdien er 0 (nul) for alle udlignede posteringer. I forbindelse med ikke-afregnede posteringer beregnes værdien som antallet af dage fra enten den oprindelige posteringsdato eller posteringsdatoen til den dato, hvor forespørgslerne køres.
En finanspostering har f.eks. posteringsdatoen 1. januar 2022 (1/1/2022) og en oprindelig posteringsdato d. 30. december 2021 (30/12/2021). Hvis der køres en forespørgsel den 2. januar 2022 (1/2/2022) for regnskabsåret 2022, er **værdien for transaktionsalder** 4. Denne værdi beregnes som antallet af dage mellem den oprindelige posteringsdato (30/12/2021) og 1/2/2022.

Hvis der ikke er nogen oprindelig posteringsdato, bruges posteringsdatoen i stedet.
-   **(Andre transaktionsoplysninger)** – Yderligere kolonner viser oplysninger som bilagsnummer, beskrivelse og debet- og kreditbeløb i alle tre valutaer (postering, regnskab og rapportering).
-   **Status** – Denne værdi er enten **Udlignet** eller **Ikke udlignet**.
-   **Udlignings-id** – Det id, som er tildelt udlignede transaktioner.

[![Forespørgselsside om finansudligning](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Totaler kan vises under gitteret.
1.  Vælg ellipsen (...) til højre for gitteret, og vælg derefter **Vis sidefod**.
2.  Vælg og hold (eller højreklikke) på hvert beløb i kolonnen, og vælg derefter **Gruppér efter denne kolonne**, for at vise totaler. Totalerne vises i sidefoden. Hvis forespørgslerne er filtreret, så den kun viser ikke-tilbagesatte posteringer, kan du bruge totalerne til at afstemme beløbene med forsøgssaldoen.







