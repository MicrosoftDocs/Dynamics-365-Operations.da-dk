---
title: Hvordan konfigurerer jeg afstemning af økonomiske dimensioner?
description: Denne artikel beskriver indstillingerne for opsætning og brug af funktionen Afstemning af økonomisk dimension.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: dd859629b0eb9f14fa4907699613382f3897d21d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878006"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Hvordan konfigurerer jeg afstemning af økonomiske dimensioner?

[!include [banner](../includes/banner.md)]

Denne artikel beskriver indstillingerne for opsætning og brug af funktionen Afstemning af økonomisk dimension.

## <a name="symptom"></a>Symptom

Der er to indstillinger til opsætning af økonomiske dimensioner for afstemning. Den første indstilling er at bruge feltet **Udligning af økonomisk dimension** på opsætningssiden **Finans** (**Finans \> Finansopsætning \> Finans**). Den anden mulighed er at anvende feltet **Kræv, at dimensionen er udlignet** på siden **Økonomiske dimensioner** (**Finans > Kontoplan \> Dimensioner \> Økonomiske dimensioner**). Denne artikel forklarer forskellen mellem disse to indstillinger.

## <a name="resolution"></a>Løsning

Organisationer bruger typisk reguleringsdimensioner til at generere en balance, der er i balance på det økonomiske dimensionsniveau. Hvis du aktiverer en af disse funktioner, bliver bogførte, uafbalancerede dimensioner ikke i balance. Du skal først angive reguleringsposter manuelt for at få balancen i balance, før du aktiverer en af disse funktioner.

Disse to indstillinger udelukker ikke gensidigt hinanden. Den indstilling, organisationen bruger, skal være baseret på dine forretningsbehov. Vi hører ofte om kunder, der definerer udligningsdimensionen i både finansopsætningen og opsætningen af den økonomiske dimension, og derefter fuldfører nogle eller alle de ekstra opsætninger, der kræves. Men de kan stadig ikke bogføre på grund af en ubalance på det økonomiske dimensionsniveau.

I følgende afsnit beskrives de to indstillinger, og det forklares, hvordan de konfigureres.

### <a name="ledger--balancing-financial-dimension"></a>Finans - økonomisk udligningsdimension

Udligningsdimensionen på opsætningssiden **Finans** bruges til at aktivere mellemkontering. Følg følgende trin for at aktivere funktionen.

1. Bestem, hvilken økonomisk dimension der skal være udligningsdimension.

    - Denne funktionalitet giver dig mulighed for kun at vælge én økonomisk dimension som udligningsdimension.
    - Du skal endnu ikke vælge dimensionen på opsætningssiden **Finans**.
    - Kontrollér, at balancen allerede er afbalanceret for den valgte økonomiske dimension.

2. Opdater kontostrukturen for den økonomiske udligningsdimension.

    - Den udlignede økonomiske dimension skal inkluderes i alle kontostrukturer, som er knyttet til Finans.
    - Der må ikke være tomme felter i kontostrukturen for den økonomiske dimension. Denne begrænsning sikrer, at alle regnskabsposter, der bogføres i Finans, indeholder en økonomisk dimensionsværdi. En tom dimensionsangivelse kan ikke benyttes, når der bruges afstemningsdimensioner.

3. Definer hovedkontiene for mellemkontering og kredit på siden **Konti til automatiske posteringer** (**Finans \> Opsætning af posteringer \> Konti til automatiske transaktioner**).
4. Vælg en økonomisk dimension til udligning i feltet **Udligning af økonomisk dimension** på opsætningssiden **Finans** (**Finans \> Finansopsætning \> Finans**).

Hvis den valgte økonomiske dimension ikke afbalanceres som posteringer angives og bogføres, tilføjer systemet automatisk de debet- og kreditposter, der kræves for at afbalancere regnskabsposten under bogføringen. Debet- og kreditfinanskontiene for den mellemkontering vises på det bogførte bilag i Finans. De vises dog ikke i de kladder eller kildedokumenter, som regnskabsposterne er bogført for.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Økonomiske dimensioner – Kræver, at dimensionen afbalanceres

Selvom udligningsdimensionen på siden **Økonomiske dimensioner** typisk bruges af firmaer i den offentlige sektor, er funktionen ikke knyttet til en konfigurationsnøgle for den offentlige sektor. Da der ikke er begrænsninger i systemet, kan du bruge denne funktion, selvom din organisation ikke er en offentlig enhed.

Denne funktionalitet bruges typisk i kundebasen i den offentlige sektor, fordi den kræver, at der bruges bogføringsdefinitioner til automatisk at afbalancere hver postering. Den bruger ikke de mellemregnings- og kreditkonti, der er defineret på siden **Konti til automatiske posteringer**, til automatisk at afbalancere regnskabsposterne. Hvis en regnskabspost ikke afbalanceres på dimensionsniveau, efter at bogføringsdefinitionerne er anvendt, bogføres posteringen ikke, selvom der er defineret debet- og kreditkonti for mellemregninger.

Vi hører ofte om kunder, der definerer udligningsdimensionen i både finansopsætningen og opsætningen af den økonomiske dimension. I dette tilfælde bruger systemet funktionerne til økonomiske dimensioner. Opsætningen af afstemning af dimensioner på økonomisk dimensionsniveau har forrang ved bogføring. Bogføringen mislykkes, hvis bogføringsdefinitionen ikke opretter en balanceret regnskabspost på det økonomiske dimensionsniveau.

Benyt følgende fremgangsmåde for at aktivere brugen af en reguleringsdimension på det økonomiske dimensionsniveau.

1. Bestem, hvilke økonomiske dimensioner der skal være udligningsdimensioner.

    - Du kan angive mere end én økonomisk dimension som en reguleringsdimension.
    - Du skal endnu ikke angive de økonomiske dimensioner, der kræves for at afbalancere en transaktion på siden **Økonomiske dimensioner**.

2. Definer bogføringsdefinitionerne for hver af de kladde- eller kildedokumenttyper, organisationen bruger. Bogføringsdefinitioner bruger finanskonti fra en ikke-bogført kladde eller et kildedokument som 'søgekriterier'. Bogføringsdefinitionen returnerer derefter de 'genererede poster', som bliver regnskabsposten. Hvis bogføringsdefinitionen er konfigureret korrekt, omfatter den genererede post søgekriterierne for finanskontiene samt yderligere konti, der af stemmer overens med regnskabsposten på dimensionsniveau. Yderligere oplysninger finder du i afsnittet [Posteringsdefinitioner](posting-definitions.md). 
   
   Bogføringsdefinitioner understøttes ikke på alle posteringstyper. Bogføringsdefinitioner kan f.eks. ikke defineres for posteringer, der er angivet via finanskladden eller anlægsaktivkladden. Hvis der ikke kan defineres en bogføringsdefinition for en kladde eller et kildedokument, skal posteringen afbalanceres manuelt med den økonomiske dimensionsværdi. Hvis der f.eks. foretages en finanskladdepost, og afdelingsdimensionen er udligningsdimensionen, skal du sikre dig, at den enkelte afdelings værdi er i balance.  Hvis dimensionsdimensionen ikke afbalanceres for hver enkelt afdelingsværdi, bogføres bilaget først, når ubalancen er rettet, ved manuelt at føje en mellemregning eller kredit til bilaget. 

    > [!IMPORTANT]
    > Hvis et for stort antal posteringer skal afbalanceres manuelt, bør du **ikke** bruge funktionen afstemningsdimension på siden **Økonomiske dimensioner**. Brug i stedet funktionen til afstemningsdimensioner på opsætningssiden **Finans**.

3. Når der er defineret bogføringsdefinitioner, kan de økonomiske dimensioner markeres som nødvendige til afstemning.

Når du angiver og bogfører posteringer, kaldes bogføringsdefinitionerne under bogføring for at bestemme regnskabsposterne. Hvis de økonomiske dimensioner afbalanceres, foretages valideringen, når regnskabsposterne er fastlagt. Hvis de økonomiske dimensioner ikke er afbalancerede, bogføres posteringen ikke, og du modtager en meddelelse om, at debiteringen ikke svarer til krediteringen for en bestemt dimension.
