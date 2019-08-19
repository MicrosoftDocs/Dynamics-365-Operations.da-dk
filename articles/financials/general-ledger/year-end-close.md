---
title: Årsafslutning
description: Dette emne beskriver den krævede konfiguration og trinnene for at køre årsafslutningsprocessen i Finans.
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3071365640eb6c012cb9af5461e885bb3f135143
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846167"
---
# <a name="year-end-close"></a>Årsafslutning

[!include [banner](../includes/banner.md)]

Dette emne beskriver den krævede konfiguration og trinnene for at køre årsafslutningsprocessen i Finans. 

Ved slutningen af hvert regnskabsår skal du køre årsafslutningsprocessen for at overføre startsaldi til det nye år. De fleste organisationer kører årsafslutningsprocessen flere gange. Første gang vil være for at få saldiene flyttet til det nye regnskabsår. Årsafslutningen kan derefter køres igen, så mange gange det er nødvendigt, for at flytte saldiene fra reguleringsposter til det nye regnskabsår. 

Under årsafslutningsprocessen oprettes der to typer af mulige transaktioner. Der genereres altid en åbningstransaktion, der bruges til at oprette startsaldi i det nye regnskabsår. Åbningstransaktionen viser saldiene for statusfinanskonti i det nye regnskabsår og saldi fra driftskonti i finanskontoen for overført overskud i det nye regnskabsår. Den afsluttende postering oprettes eventuelt for at få saldiene på driftskonti til at gå i nul i det regnskabsår, der afsluttes.

## <a name="prepare-to-run-the-year-end-close"></a>Forbered kørsel af årsafslutning
Før du kører årsafslutningsprocessen, skal du validere indstillingerne for følgende: 

På siden **Hovedkonto**:

-   Valider, om **Hovedkontotypen** er angivet korrekt for hver hovedkonto. Hovedkontotypen bruges til at bestemme, om saldoen på hovedkontoen skal fremføres som en startsaldo eller overføres til overført overskud i åbningstransaktionen.
-   Feltet **Primokonto** kan bruges til at overføre saldoen på hovedkontoen til en ny hovedkonto i forbindelse med årsafslutningen. Den nye hovedkonto angives i feltet **Primokonto**. Typisk bruges dette til balancehovedkonti, når hovedkontoen er deaktiveret, og en ny hovedkonto bruges til det nye regnskabsår.

På siden **Finansparametre** under **Årsafslutning**:

-   Indstillingen **Slet årsafslutningstransaktioner** bruges til at angive, om den systemgenererede åbningspostering fra en tidligere årsafslutning skal slettes, når årsafslutningen køres igen. Hvis denne indstilling er angivet til **Ja**, slettes den tidligere åbningspostering, og en ny åbningspostering oprettes ud fra de aktuelle saldi. Hvis denne indstilling er angivet til **Nej**, forbliver den tidligere åbningspostering, og der oprettes en yderligere åbningspostering for at flytte saldiene fra reguleringsposteringer, der er bogført efter den forrige årsafslutning.
-   Indstillingen **Opret ultimoposter ved overførsel** bruges til at oprette ultimoposteringer i det regnskabsår, der afsluttes, for at bringe saldiene på driftskontiene i nul. Hvis denne indstilling er angivet til **Ja**, oprettes både åbningsposteringen og ultimoposteringen. Hvis denne indstilling er angivet til **Nej**, oprettes kun åbningsposteringen i det næste regnskabsår for at overføre saldiene. Saldi på driftskonti forbliver i slutningen af regnskabsåret.
-   Indstillingen **Indstil status til permanent afsluttet for regnskabsåret** bruges til at angive regnskabsåret til en permanent lukket status. Brug denne indstilling med forsigtighed, da alle perioder med permanent lukket status ikke kan genåbnes, og det forhindrer justeringer fra at blive bogført i regnskabsåret. Det er bedste fremgangsmåde at angive den til **Nej**.
-   Indstillingen **Bilagsnummeret skal være udfyldt** bruges til at definere, om der kræves et bilagsnummer, når du kører årsafslutningsprocessen. Det er den bedste fremgangsmåde at kræve et bilagsnummer for nemt at identificere åbningsposteringen.

På siden **Regnskabskalender**:

-   Det næste regnskabsår skal eksistere, før du kører årsafslutning. Det næste regnskabsår kræves for at oprette startsaldiene i primoperioden.

På siden **Finanskalender**:

-   Valgfrit: Hver regnskabsperiode for det regnskabsår, der afsluttes, kan indstilles til **På hold** for at forhindre, at der indtastes nye posteringer. Når ændringsposterne identificeres, kan På hold-perioderne genåbnes, så du kan postere reguleringsposteringer, selv om årsafslutningsprocessen allerede er blevet kørt.

## <a name="define-year-end-close-templates"></a>Angiv årsafslutningsskabeloner
Når systemet er konfigureret, kan du køre årsafslutningsprocessen. På siden **Årsafslutning** kan en skabelon defineres for den gruppe af juridiske enheder, som årsafslutningsprocessen køres for. Skabelonen kan genbruges ved hver årsafslutning, men den kan ændres, hvis din organisation ændres. 

Først skal du definere **gruppenavnet** for skabelonen, og vælge regnskabskalenderen. Gruppenavnet skal identificere gruppen af inkluderede juridiske enheder.  Eksempelvis kan skabeloner oprettes baseret på geografi med separate grupper, der er oprettet for nordamerikanske juridiske enheder, EMEA juridiske enheder og juridiske enheder i APAC. 

Derefter kan de juridiske enheder føjes til skabelonen. Juridiske enheder kan tilføjes ved at vælge et organisationshierarki eller ved at vælge de juridiske enheder. Hvis et organisatorisk hierarki er valgt, tilføjes kun juridiske enheder i hierarkiet, der bruger den valgte regnskabskalender, til skabelonen. Hvis du bruger juridiske enheder til at føje til skabelonen, kan kun juridiske enheder med samme regnskabskalender tilføjes. Samme regnskabskalender er påkrævet, fordi årsafslutningen køres ved at vælge et regnskabsår, som kan variere fra en kalender til en kalender. 

Når de juridiske enheder er tilføjet, kan du definere hovedkontiene for overført overskud for hver juridisk enhed. Feltet **Dato for sidste årsafslutning** opdateres hver gang, årsafslutningen udføres for den juridiske enhed. 

Fanen **Økonomiske dimension** bruges til at definere, hvilke økonomiske dimensioner der skal bruges på åbningsposteringen. Bemærk, at de indstillinger, du definerer, er kun relevante for den juridiske enhed, der er valgt i gitteret **Juridiske enheder**. Du skal gentage opsætningen for hver juridisk enhed i gitteret. 

Indstillingen **Overfør balancedimensioner** bruges til at definere, om de økonomiske dimensioner for posteringer, der er bogført på statuskonti, skal opretholdes på åbningsposteringen. Det er bedste fremgangsmåde at angive denne indstilling til **Ja**. Indstillingen **Overfør driftsdimensioner** bruges til at definere, hvilke økonomiske dimensioner på posteringer, der bogføres på driftskonto, der bliver overført til hovedkontoen for overført overskud. Først skal du identificere de økonomiske dimensioner, der er relevante for den valgte juridiske enhed. Dette omfatter alle økonomiske dimensioner, der er bogført mod i løbet af året, selv om den økonomiske dimension ikke er en del af en aktiv kontostruktur. Derefter skal du angive hver dimension som enten **Luk et enkelt** eller **Luk alle**.  Standarden er **Luk alle**, som bevarer de oprindelige økonomiske dimensionsværdier fra bogførte posteringer og bruger dem til oprettelse af primosaldi for resultatkontoen. Der oprettes separate primosaldi for resultatkonti for hver enkelt kombination af økonomiske dimensionsværdier. Hvis **Luk et enkelt** er valgt, opsummeres alle posteringer, der er posteret med den pågældende økonomiske dimension, i en primosaldo for resultatkonti for den dimensionsværdi, der er angivet i feltet efter **Luk et enkelt**. Antag for eksempel, at alle posteringer for regnskabsåret er bogført med kontostrukturen for Hovedkonto - afdeling. På den økonomiske dimension Afdeling i skabelonen er **Luk et enkelt** valgt, og 100 er den angivne værdi. Hvis den samlede indtægt af alle transaktioner, der er bogført på afdelingerne 200, 300 og 400 er $100.000, oprettes der en primosaldo for overført overskud – 100. Hvis du vælger **Luk et enkelt** og lader den økonomiske dimensionsværdi være tom, bogføres alle transaktioner på overført overskud med den pågældende dimensionsværdi tom. 

Årsafslutningsprocessen overholder ikke kontostrukturer. Dette skyldes, at kontostrukturer kan ændres i løbet af et regnskabsår, og det er ikke altid muligt at identificere relevante kontostruktur på grund af disse ændringer.  Når der oprettes primoposteringer, fremføres saldi med økonomiske dimensioner som defineret i skabelonen til årsafslutning. Primosaldiposter kan omfatte økonomiske dimensioner, der ikke længere er i den aktuelle kontostruktur og segmentkombinationer, der ikke længere er gyldige i den aktuelle kontostruktur. Hvis din virksomhed ønsker at udelukke en økonomisk dimension for primosaldoen for overført overskud, skal den økonomiske dimension angives til **Luk et enkelt**, og dimensionsværdien skal være tom.

## <a name="run-the-year-end-close-process"></a>Kør årsafslutningsprocessen
Når årsafslutningsskabelonerne er oprettet, startes årsafslutningsprocessen ved at vælge **Kør regnskabsår** i handlingsruden. Vælg enten alle eller et undersæt af juridiske enheder fra den skabelon, som årsafslutningen skal køres for. Når du kører årsafslutningen for første gang i et regnskabsår, vil du sandsynligvis vælge alle de juridiske enheder for at oprette primosaldi for alle juridiske enheder. Hvis du kører årsafslutningen igen, kan du vælge at køre processen kun for de juridiske enheder, hvor reguleringsposteringer blev bogført. 

Vælg det regnskabsår, du vil køre årsafslutningen for. Hvis der findes mere end én ultimoperiode for den sidste periode i regnskabsåret, bliver feltet **Periodenavn** tilgængeligt, så du kan vælge, hvilken ultimoperiode ultimoposteringen skal bogføres i, hvis opsætningen er defineret til at oprette ultimoposteringen. 

Angiv et bilagsnummer, som muligvis ikke er påkrævet, afhængigt af opsætningen i finansparametrene. Det samme bilagsnummer bruges til alle de juridiske enheder, der er valgt til årsafslutningsprocessen. Bilagsnummeret genereres ikke ved brug af en nummerserie. Det er den bedste fremgangsmåde at angive et bilagsnummer, selvom det ikke er påkrævet. Angivelsen af et bilagsnummer gør det lettere at finde primoposteringen i det nye regnskabsår. Hvis der ikke angives et bilagsnummer, er bilagsnummeret tomt for den åbningsposteringen. 

Hvis du vil tilbageføre en tidligere årsafslutning for det valgte regnskabsår, skal du angive **Fortryd forrige afslutning** til **Ja**. Årsafslutningen tilbageføres, men processen kan køres igen når som helst. Hvis du tilbagefører en årsafslutning, er **Dato for sidste årsafslutning** ikke tilgængelig. 

Årsafslutningsprocessen køres som standard i batchtilstand. Det er den bedste fremgangsmåde at køre processen i batchtilstand, for at give brugeren mulighed for at vende tilbage til andre aktiviteter. Når årsafslutningsprocessen er fuldført, opdateres **Dato for sidste årsafslutning** med sessionsdatoen.

Du kan finde flere oplysninger i [Luk Finans ved periodeafslutning](close-general-ledger-at-period-end.md) og [Lukke regnskabsåret](tasks/close-fiscal-year.md).



