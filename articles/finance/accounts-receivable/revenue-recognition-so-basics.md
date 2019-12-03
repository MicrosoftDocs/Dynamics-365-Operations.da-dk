---
title: Indtægtsføring på salgsordrer
description: I dette emne beskrives de grundlæggende funktioner til registrering af indtægt på salgsordrer og fakturaer. Indtægtsføring er tilgængelig på salgsordren og på den tilsvarende faktura, der oprettes ud fra salgsordren.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e2eafc6785aaf9bc7421bc80c90fa4a7f98a2d4
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693014"
---
# <a name="revenue-recognition-on-sales-orders"></a>Indtægtsføring på salgsordrer

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring. I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.

I dette emne beskrives de grundlæggende funktioner til registrering af indtægt på salgsordrer og fakturaer. Indtægtsføring er tilgængelig på en salgsordre og på den tilsvarende faktura, der oprettes ud fra salgsordren. Salgsordren kan også oprettes via et Tid og materialer-projekt.

> [!NOTE]
> I illustrationerne i dette emne er kolonner skjulte eller føjet til gitre, så de bedre viser begreberne. Derfor kan siderne og dataene i illustrationerne være forskellige fra det, du kan se i produktet.

## <a name="enter-a-sales-order"></a>Angiv en salgsordre

Den følgende salgsordre angives og indeholder tre varer, der er konfigureret til indtægtsføring.

[![Angiv en salgsordre](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Der er to koncepter for indtægtsføring:

- **Angiv indtægtsprisen.** Indtægtsprisen beregnes på basis af opsætningen af de frigivne produkter. Indtægtsprisen vises aldrig for kunden, men bruges kun til bogføring af salgsordrefakturaen. Salgsordrelinjerne og de dokumenter, der udskrives som en del af salget, fortsætter med at vise enheds-/listeprisen.
- **Angiv, hvornår indtægtsføringen skal finde sted.** En indtægtstidsplan bruges til at bestemme, hvornår indtægten skal registreres.

    I dette eksempel tildeles den første vare, S0001, en **1O** (én forekomst)-indtægtstidsplan. Denne linje repræsenterer et milepæl-scenarie, hvor indtægten registreres, efter at installationen er fuldført fremover. Indtægten udskydes derfor, indtil installationen er fuldført.

    Den anden vare, S0008, er en servicevare, der er konfigureret som en PCS-vare (Support efter kontrakt). De vedvarende tekniske tjenester leveres til kunden i løbet af en periode på 12 måneder. Derfor tildeles som standard en indtægtstidsplan på **12M** til produktet. Da denne vare er en PCS-vare, skal der defineres start- og slutdato for kontrakten. Kontraktens start-og slutdato findes som standard i vinduet Vareoplysninger – fanen Opsætning. I indtægtsplanen er opsætningen af **12M** defineret, så kontraktbetingelserne automatisk udfyldes som vist i følgende illustration.

    [![Indtægtstidsplaner](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Den tredje vare, S0012, er hardware, og der tildeles ikke en indtægtsplan som standard. Indtægten for hardwaren registreres, så snart varen faktureres.

## <a name="confirm-the-sales-order"></a>Bekræft salgsordren

Hvis du vil have vist flere oplysninger om indtægtsprisen og indtægtstidsplanen, skal du bruge knapperne i gruppen **Indtægtsføring** på fanen **Administrer** i salgsordrens handlingsrude. Da salgsordren ikke er bekræftet på dette tidspunkt, er knapperne, der bruges til indtægtsføring, ikke tilgængelige. Disse knapper bliver tilgængelige eller utilgængelige, når salgsordren gennemgår de stadier, der fører til opfyldelse.

[![Salgsordreoverskrift](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

De første tre knapper giver oplysninger om indtægtsprisen for varerne i salgsordreopsætningen for indtægtsføring.

- **Fordeling af indtægtspris** – Denne knap bliver tilgængelig, når salgsordren er bekræftet, eller fakturaen er bogført. Både salgsordrebekræftelse og fakturabogføring beregner indtægten for at registrere den pris, der vil blive registreret eller udskudt på regnskabsposten. Afhængigt af konfigurationen kan den beregnede indtægtspris være forskellig fra den enhedspris, der vises for kunden.
- **Omfordel pris med nye ordrelinjger** – Denne knap bliver tilgængelig, når salgsordren er bekræftet, eller fakturaen er bogført. Omfordelingsprocessen bruges til at genberegne den indtægt, der skal registreres, når en ny linje føjes til den aktuelle salgsordre, når den er faktureret, eller til en ny salgsordre. I begge scenarier medfører tilføjelsen af en ny vare en ændring i kontrakten. Derfor skal indtægtsprisen genfordeles.
- **Opdater fordeling af indtægtspris** – Denne knap bliver tilgængelig, når salgsordren er bekræftet, men den bliver ikke tilgængelig, når salgsordren er faktureret. Opdateringen bruges til at køre fordelingen af indtægtspris uden at være nødt til at bekræfte salgsordren. Når salgsordren er faktureret, kan indtægtsprisen ikke genberegnes.

De sidste to knapper gjver oplysninger om indtægtsplanen for de varer på salgsordren, der har en indtægtstidsplan.

- **Tidsplan for registrering af forventet indtægt** – Denne knap bliver tilgængelig, når salgsordren er bekræftet, men den bliver ikke tilgængelig, når salgsordren er faktureret. Den åbner en side, der viser den forventede indtægtstidsplan. Den endelige tidsplan kan ændres, fordi den forventede tidsplan anvender den ønskede afsendelsesdato, mens den endelige tidsplan bruger den faktiske afsendelsesdato.
- **Tidsplan for indtægtsføring** – Denne knap bliver tilgængelig, når salgsordren faktureres. Den endelige tidsplan for indtægtsføring oprettes ikke, når en bekræftelse finder sted, eller der oprettes en følgeseddel. Den oprettes kun, når salgsordren faktureres.

I følgende eksempel forekom der en fordeling af indtægtspris, da salgsordren blev bekræftet. Bemærk, at selvom indtægtspriserne tildeles forskelligt, skal det samlede beløb i feltet **Indtægt, der skal registreres** stadig være lig med summen af de salgsordrelinjer, der faktureres til kunden. Summen af salgsordrelinjerne er 1499 USD eksklusive moms. Derfor skal summen af værdierne for **Indtægt, der skal registreres** også være 1499 USD.

[![Fordeling af indtægtspris](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Den forventede tidsplan for indtægtsføring oprettes også. I indtægtsplanen bruges værdien **Indtægt, der skal registreres** som det beløb, der skal udskydes. Vare S0001 udskyder 321,21 USD i stedet for 300 USD og vare S0008 udskyder 160,61 USD i stedet for 100 USD. Vare S0012 vises ikke i den forventede tidsplan, fordi indtægten ikke er udskudt. Når bogføringen foretages, bogfører vare S0012 1017,18 USD direkte på finanskontoen for indtægt.

[![Tidsplan for forventet indtægtsføring](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Opret følgeseddel

Derefter kan følgesedlen oprettes til salgsordren. Der registreres ingen indtægt, når følgesedlen bogføres. Hvis salgsordren ikke blev bekræftet, udløser bogføring af følgesedlen ikke beregning af indtægtspris. Den udløser heller ikke den forventede eller endelige tidsplan for indtægtsføring. Hvis varemodelgruppen er konfigureret til at udskyde indtægten på følgesedlen, fortsætter den med at bogføre vha. finanskontiene for den aktuelle bogføringsprofil og ikke de nye udskudte indtægtskonti, der bruges på fakturabogføringen.

## <a name="create-the-invoice"></a>Opret fakturaen

Det sidste trin er at fakturere salgsordren. Hvis du kigger på fakturaens bilag, vil du bemærke, at indtægten for vare S0001 og S0008 blev udskudt (321,21 + 160,61 = 481,82 USD), og restbeløbet for vare S0012 blev bogført i indtægt (1017,18 USD). Disse værdier føjes til 1.499 USD, hvilket svarer til summen af salgsordrelinjerne.

[![Posteringer på bilag](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Når fakturaen er oprettet, bliver knapperne for indtægtsføring **Fordeling af indtægtspris**, **Omfordel pris med nye ordrelinjger** og **Tidsplan for indtægtsføring** tilgænglige, men knapperne **Opdater fordeling af indtægtspris** og **Tidsplan for forventet indtægtsføring** bliver utilgængelige.

[![Tilgængelighed af knappen Tilgængelig indtægtsføring](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Knappen **Fordeling af indtægtspris** er stadig tilgængelig, så du kan se beregningen af indtægtsprisen. Hvis der ikke foretages ændringer på salgsordren, efter at den er bekræftet, ændres bogføringen af fakturaen i feltet **Indtægt, der skal registreres** ikke.

Den forventede tidsplan for indtægtsføring fjernes og erstattes af den endelige tidsplan for indtægtsføring. Oplysningerne om indtægtstidsplanen vedligeholdes for hver salgsordrelinje og bruges til at frigive den udskudte indtægt til faktisk indtægt, efterhånden som de kontraktmæssige forpligtelser opfyldes.

[![Tidsplan for endelig indtægtsføring](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)
