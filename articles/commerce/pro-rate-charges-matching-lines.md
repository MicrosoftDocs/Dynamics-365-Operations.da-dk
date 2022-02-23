---
title: Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer
description: I dette emne beskrives yderligere funktioner til beregning og anvendelse af automatiske gebyrer på Commerce-kanalordrer ved hjælp af den avancerede automatiske gebyrfunktion.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410954"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer


[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner til gruppering af automatiske gebyrer på hovedniveau og til forholdsmæssig beregning af dem for handelssalgslinjer. Denne funktionalitet er tilgængelig for transaktioner, der oprettes på POS i Retail version 10.0.1, og salg, der oprettes i et callcenter i Retail version 10.0.2.

Denne funktionalitet er kun tilgængelig, hvis den [avancerede automatiske gebyrfunktion](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) er aktiveret ved hjælp af indstillingen på siden **Commerce-parametre**. Desuden kan den forbedrede beregningsmåde for automatiske gebyrer kun anvendes til salgsordrer, der oprettes gennem handelskanaler (POS, et callcenter og Dynamics e-handelsplatformen).

Denne nye funktion giver organisationer større fleksibilitet i den måde, som automatiske gebyrer på hovedniveau beregnes og anvendes i salgstransaktioner.

I versioner af appen, der er ældre end version 10.0.1, beregnes automatiske gebyrer på hovedniveau, som har en bestemt leveringsmåderelation, kun, når der er overensstemmelse med den leveringsmåde, som er defineret i salgsordrehovedet.

F.eks. defineres automatiske gebyrer på hovedniveau for levering **99** og leveringsmåden **11**. Der oprettes en salgsordre, og leveringsmåden **99** defineres i ordrehovedet. Men nogle af salgslinjerne er konfigureret, så de sendes ved hjælp af leveringsmåde **11**. I så fald tages kun gebyrer på hovedniveau, der er knyttet til leveringsmåde **99**, i betragtning og anvendes på salgsordren.

I Commerce har gebyrer på hovedniveau en ekstra funktion, som du kan bruge til at definere en [konfiguration af lagdelte gebyrer](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery), der er baseret på ordreværdien. Eksempelvis hvis ordreværdien er mellem $50,00 og $200,00, kan en organisation eventuelt opkræve et fragtgebyr på $5,00. Hvis ordreværdien er mellem $200,01 og $500,00, kan fragten dog være $4,00.

Nogle organisationer ønsker fordelene ved beregningen af lagdelte gebyrer, der følger med gebyrer på hovedniveau. Men i scenarier, der består af blandede leveringsmåder, skal de også sikre, at de gebyrer, der beregnes, passer til den leveringsmåde, der er defineret på hver salgslinje.

Du kan nu konfigurere automatiske gebyrer på hovedniveau, så alle leveringsmåder på ordren indgår i beregningen af gebyrer. Denne funktionalitet kræver en mere kompleks beregningslogik til beregning af gebyrer på hovedniveau. Logikken grupperer de varer, der leveres ved hjælp af samme leveringsmåde, og behandler denne gruppe som beregningsgruppen for varerne ved beregning af automatiske gebyrer på hovedniveau. For varer, der har samme leveringsmåde, beregnes automatiske gebyrer ud fra den samlede salgsværdi for varerne. På denne måde bestemmes det relevante automatiske gebyrniveau.

Når de relevante gebyrer på hovedniveau opnås for de salgslinjer, der sendes ved hjælp af samme leveringsmåde, fordeles de beregnede gebyrer helt ned til salgslinjeniveau. Da disse gebyrer er på linjeniveau og ikke holdes på hovedniveau, oprettes en mere specifik tilknytning mellem varen og den gebyrværdi, der beregnes for den. Denne funktionsmåde kan være nyttig ved delvise returneringer, hvor en organisation kun ønsker at tilbagebetale en del af gebyrer i stedet for hele gebyret, når kun nogle af varerne returneres.

## <a name="scenarios"></a>Scenarier

Følgende to eksempelscenarier skitserer, hvordan disse gebyrer beregnes, både når den nye funktionalitet bruges, og når den ikke bruges.

### <a name="scenario-1"></a>Scenario 1

Dette scenario beskriver funktionsmåden, når indstillingen **Beregn forholdsmæssigt på matchende salgslinjer** er angivet til **Nej** i opsætningen af automatiske gebyrer. (Funktionsmåden svarer til funktionsmåden for gebyrer på hovedniveau i appversioner, der er ældre end version 10.0.1).

I dette scenario har organisationen defineret gebyrer på hovedniveau for leveringsmåderelation **99** og leveringsmåderelation **11**. Ingen automatiske gebyrer er konfigureret for leveringsmåde **21**.

![Automatiske gebyrer for leveringsmåde 99, når forholdsmæssig beregning for linjematchning er slået fra](media/99_disabled.png)

![Automatiske gebyrer for leveringsmåde 11, når forholdsmæssig beregning for linjematchning er slået fra](media/11_disabled.png)

Der oprettes en salgsordre i callcenteret, og leveringsmåden indstilles til **99**. Denne ordre indeholder fem varer. To ordrelinjer er konfigureret til at bruge leveringsmåde **99**, to linjer er konfigureret til at bruge leveringsmåde **11**, og én linje er konfigureret til at bruge leveringsmåde **21**, som vist i følgende tabel.

| Post  | Linjeantal | Leveringstilstand | Pris pr. enhed |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

I dette scenario evalueres hele ordren i forhold til tabellen over automatiske gebyrer for leveringsmåde **99**. Hele summen af alle salgslinjer bruges til at bestemme et matchningstrin i konfigurationen af automatiske gebyrer, og dette gebyr anvendes på ordrehovedniveau. Den samlede ordrebeløb er $165,00 i dette eksempel, og fragtgebyret på $15,00 anvendes i ordrehovedet. Der refereres aldrig til eller anvendes automatiske gebyrer, der er konfigureret for leveringsmåde **11**.

I dette scenario, hvis en kunde returnerer nogle af varerne i ordren, og hvis [gebyrkoden konfigureres, så den kan refunderes](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), anvendes det samlede gebyr på hovedniveau systematisk på refusionen, selvom kun nogle af varerne returneres.

### <a name="scenario-2"></a>Scenario 2

I dette scenario defineres gebyrer på hovedniveau for leveringsmåderelation **99** og leveringsmåderelation **11**. Men indstillingen **Beregn forholdsmæssigt på matchende salgslinjer** er angivet til **Ja** for disse tabeller over automatiske gebyrer.

![Automatiske gebyrer for leveringsmåde 99, når forholdsmæssig beregning for linjematchning er slået til](media/99_enabled.png)

![Automatiske gebyrer for leveringsmåde 11, når forholdsmæssig beregning for linjematchning er slået til](media/11_enabled.png)

I dette scenario bruges den samme salgsordre, der indeholder fem linjer. Leveringsmåden i ordrehovedet er indstillet til **99**, men leveringsmåden for de enkelte varer på salgsordren er konfigureret som vist i følgende tabel.

| Post  | Linjeantal | Leveringstilstand | Pris pr. enhed |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Da konfigurationen af automatiske gebyrer er indstillet til at bliver beregnet forholdsmæssigt til matchende salgslinjer, udfører systemet følgende beregning.

1. Alle varer, der har samme leveringsmåde, grupperes sammen, og systemet beregner den samlede produktværdi for varerne i gruppen.

    **Leveringsmåde 11**

    - Vare 81331, antal 1 = $10
    - Vare 81333, antal 2 = $60 netto ($30 pr. enhed)
    - **Samlet værdi af produktet for leveringsmåde 11 = $70**

    **Leveringsmåde 99**

    - Vare 81332, antal 1 = $50
    - Vare 81334, antal 3 = $30 netto
    - **Samlet værdi af produktet for leveringsmåde 99 = $80**

    **Leveringsmåde 21**

    - Vare 81334, antal 3 = $15 netto
    - **Samlet værdi af produktet for leveringsmåde 21 = $15**

2. Systemet søger efter konfigurationen for automatiske gebyrer på hovedniveau, der svarer til debitor- og leveringsmådeindstillingerne for hver gruppe af varer. Hvis konfigurationen findes, søges der i den niveaudelte konfiguration efter det gebyr, som skal anvendes, baseret på den samlede produktværdi af varer i leveringsmådegruppen.

    **Leveringsmåde 11**

    - Samlet produktværdi = $70
    - **Gebyrværdi = $7**

    **Leveringsmåde 99**

    - Samlet produktværdi = $80
    - **Gebyrværdi = $15**

    **Leveringsmåde 21**

    - Samlet produktværdi = $15
    - **Gebyrværdi = $0** (ingen automatiske gebyrer er konfigureret for denne kombination af en kunde og en leveringsmåde).

    ![Gebyrer for leveringsmåde 11 falder inden for det markerede niveau](media/step2mode11.png)

    ![Gebyrer for leveringsmåde 99 falder inden for det markerede niveau](media/step2mode99.png)

3. Systemet beregner den gebyrværdi, der skal anvendes på hver linje baseret på forholdsmæssig beregningslogik, der vurderer den proportionale værdi for linjen i forhold til gruppens samlede produktværdi.

    **Leveringsmåde 11**

    - Gebyrværdi = $7
    - Gruppeproduktværdi = $70
    - Værdi for linje 1 = $10 (= 14,2857 % af gruppeværdien)
    - Værdi for linje 3 = $60 (= 85,7143 % af gruppeværdien)
    - **Linjegebyr for linje 1 = $1**
    - **Linjegebyr for linje 3 = $6**

    **Leveringsmåde 99**

    - Gebyrværdi = $15
    - Gruppeproduktværdi = $80
    - Værdi for linje 2 = $50 (= 62,5 % af gruppeværdien)
    - Værdi for linje 4 = $30 (= 37,5 % af gruppeværdien)
    - **Linjegebyr for linje 2 = $9,38**
    - **Linjegebyr for linje 4 = $5,62**

    **Leveringsmåde 21**

    - Gebyrværdi = $0
    - Gruppeproduktværdi = $15
    - Værdi for linje 5 = $15 (= 100 % af gruppeværdien)
    - **Linjegebyr for linje 5 = $0**

Derfor tildeles vare 81334 et fragtgebyr på $5,62 i dette eksempel. Du kan få vist disse gebyrer på siden **Vedligehold gebyrer** for salgslinjen. I følgende illustration vises, hvordan denne side ser ud for vare 81334.

![Forholdsmæssigt beregnede gebyrer på salgslinje for vare 81334](media/proratedlinecharge.png)

Når denne beregningsmetode bruges til en delvis returnering, og hvis gebyrkoden kan refunderes, er det kun en del af det gebyr, som er allokeret til den pågældende linje, der refunderes, når varen er returneret.

## <a name="additional-resources"></a>Yderligere ressourcer

[Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md)

[Aktivere og konfigurere automatiske gebyrer efter kanal](auto-charges-by-channel.md)
