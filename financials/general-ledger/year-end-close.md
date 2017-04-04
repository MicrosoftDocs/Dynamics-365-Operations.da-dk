---
title: "Årsafslutning"
description: "Dette emne beskriver de nødvendige konfiguration og trin for at køre Finans Luk årsafslutningsprocessen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Årsafslutning

Dette emne beskriver de nødvendige konfiguration og trin for at køre Finans Luk årsafslutningsprocessen. 

I slutningen af et regnskabsår, skal du køre årsafslutningsprocessen for at overføre primosaldi til det nye år Luk. De fleste organisationer køre årsafslutningsprocessen for Luk flere gange. Første gang ville være at få de saldi, der er flyttet til det nye regnskabsår. Årets tæt kan derefter køre igen, så mange gange, der kræves, for at flytte saldi fra reguleringsposter i det nye regnskabsår. 

Luk processen ved årets afslutning, der er to typer af mulige transaktioner, der er oprettet. En åbning transaktion genereres altid og bruges til oprettelse af startsaldi i det nye regnskabsår. Den åbne postering viser balancen finanskontosaldi i det nye regnskabsår og saldi fra finanskontosaldi driftskonto i Finans resultatkontoen i det nye regnskabsår. Afsluttende posteringen oprettes eventuelt for at overføre saldiene på driftskonti ned til nul i det regnskabsår, der afsluttes.

## <a name="prepare-to-run-the-year-end-close"></a>Forbered kørsel af årets tæt
Før du kører årsafslutningsprocessen Luk, validere indstillingerne for følgende: 

På siden **Hovedkonto**:

-   Validering af den **Main kontotype** er angivet korrekt for hver hovedkonto. Kontotypen hoved bruges til at bestemme, om saldoen på hovedkontoen skal bringes frem som en startsaldo eller lukkede til resultatkontoen i den åbne postering.
-   Den **primokonto** felt kan bruges til at overføre saldoen på hovedkontoen til en ny hovedkonto under årets tæt. Den nye hovedkonto, der er angivet i den **primokonto** felt. Typisk bruges dette til balancekonti af vigtigste når hovedkontoen er uvirksom, og en ny hovedkonto bruges til det nye regnskabsår.

På den **økonomiparametrene** side **årsafslutning**:

-   Den **slette lukke år transaktioner** indstilling bruges til at angive, om den systemgenererede primoposter fra en tidligere årets tæt skal slettes, når årets tæt køres igen. Hvis denne indstilling er angivet til **Ja**, tidligere primoposter slettes, og en ny primoposter er oprettet ud fra de aktuelle saldi. Hvis denne indstilling er angivet til **ingen**, forbliver den tidligere primoposter og en flere primoposter er oprettet for at flytte saldi fremad fra regulering af posteringer, der er bogført efter den forrige årsafslutning.
-   Den **oprette ultimoposteringer ved overførsel** indstilling, der bruges til at oprette ultimoposteringer i det regnskabsår, der afsluttes for at overføre saldiene for kontiene drift til nul. Hvis denne indstilling er angivet til **Ja**, oprettes der både primoposter og afsluttende transaktion. Hvis denne indstilling er angivet til **ingen**, kun primoposter er oprettet i det næste regnskabsår for at overføre saldiene. Kontosaldi drift forbliver i slutningen af regnskabsåret.
-   Den **indstillet status for regnskabsåret til permanent lukket** indstilling bruges til at angive regnskabsåret til en permanent lukket status. Brug denne indstilling med forsigtighed, da alle perioder med permanent lukket status ikke kan genåbnes, forhindrer justeringer fra der bogføres i regnskabsåret. Det er den bedste fremgangsmåde indstilles til **ingen**.
-   Den **bilagsnummeret skal udfyldes** indstilling bruges til at definere, om der kræves et bilagsnummer, når du kører årsafslutningsprocessen Luk. Det er den bedste fremgangsmåde til at kræve et bilagsnummer for at nemt for at identificere den åbne postering.

På den **regnskabskalender** side:

-   Det næste regnskabsår skal eksistere, før du kører årets tæt. Det næste regnskabsår, der kræves for at oprette startsaldoen i den åbne periode.

På den **finanskalender** side:

-   Valgfrit: Hver regnskabsperiode for det regnskabsår, der afsluttes kan indstilles til **på hold** til at forhindre, at der indtastes nye posteringer. Når ændringsposterne identificeres, kan On hold perioder genåbnes du posterer ændringsposterne, selvom Luk årsafslutningsprocessen er blevet kørt.

## <a name="define-year-end-close-templates"></a>Angiv årsafslutning Luk skabeloner
Når systemet er konfigureret, kan du køre årsafslutningsprocessen Luk. På den **årsafslutning** side, en skabelon kan defineres for gruppen af juridiske enheder, årsafslutning proces køres. Skabelonen kan genbruges ved hver årsafslutningen tæt, men kan ændres, hvis din organisation ændres. 

Du skal først definere de **gruppenavn** skabelon, og vælg den regnskabskalender. Gruppenavnet skal identificere gruppen af juridiske enheder.  Eksempelvis kan skabeloner oprettes baseret på Geografi, med separate grupper, der er oprettet for nordamerikanske juridiske enheder, EMEA juridiske enheder og juridiske enheder i APAC. 

Derefter skal de juridiske enheder, der kan føjes til skabelonen. Juridiske enheder kan tilføjes ved at vælge et organisatorisk hierarki eller ved at vælge de juridiske enheder. Hvis et organisatorisk hierarki er markeret, tilføjes kun juridiske enheder i hierarkiet, der bruger den valgte regnskabskalender til skabelonen. Kun juridiske enheder med samme regnskabskalender kan tilføjes, hvis du føjer til skabelonen ved hjælp af juridiske enheder. Samme regnskabskalender er påkrævet, fordi køres årets tæt ved at vælge et regnskabsår, som kan variere fra en kalender til en kalender. 

Når der tilføjes de juridiske enheder, kan du definere resultatkontoen hovedkontiene for hver juridisk enhed. Den **dato for sidste år afslutning lukke** opdateres hver gang, årets slutning tæt udføres for den juridiske enhed. 

Den **økonomiske dimension** fane bruges til at definere, hvilke økonomiske dimensioner der skal bruges på den åbne postering. Bemærk, at de indstillinger, du definerer, er relevante for kun den valgte juridiske enhed i den **juridiske enheder** gitter. Opsætningen af gentages for hver juridisk enhed i gitteret. 

Den **Transfer balancen dimensioner** bruges til at definere, om de økonomiske dimensioner for posteringer, der er bogført til statuskonti bør opretholdes i den åbne postering. Det er den bedste fremgangsmåde til at angive denne indstilling til **Ja**. Den **Transfer drift dimensioner** bruges til at definere, hvilke økonomiske dimensioner på posteringer, der bogføres for at fortjeneste og tabskonto vil blive overført til de vigtigste resultatkontoen. Først skal du identificere de økonomiske dimensioner, der er relevante for den valgte juridiske enhed. Dette ville omfatte økonomiske dimensioner bogføres mod i år, selv om den økonomiske dimension ikke er en del af en kontostruktur. Derefter skal du angive hver dimension som enten **Luk enkelt** eller **lukke alle**.  Standarden er **lukke alle**, som bevarer den oprindelige økonomiske dimension værdier fra bogførte posteringer og bruger dem til oprettelse af åbningen saldi for resultatkontoen. Der oprettes separate resultatkontoen primosaldi for hver enkelt kombination af økonomiske dimensionsværdier. Hvis **Luk enkelt** er valgt, alle posteringer med den økonomiske dimension, der opsummeres i en startsaldo for den dimensionsværdi, der er angivet i feltet efter resultatkontoen **Luk enkelt**. Antag for eksempel, alle posteringer for regnskabsåret er bogført med kontostrukturen for hovedkonto - afdeling. På den økonomiske dimension Afdeling i skabelonen, **Luk enkelt** er valgt, og 100 er den angivne værdi. Hvis den samlede indtægt af alle transaktioner, der er bogført på afdelinger, 200, 300 og 400 $100,000, oprettes der en primosaldo for Retained overskud - 100. Hvis du vælger **Luk enkelt** og udfylder den økonomiske dimensionsværdi, alle transaktioner skal bogføres på resultatkontoen med dimensionsværdien er tom. 

Luk årsafslutningsprocessen overholder ikke kontostrukturer. Dette skyldes, at kontostrukturer kan ændre i løbet af et regnskabsår, og det er ikke altid muligt at identificere relevante kontostrukturen på grund af disse ændringer.  Når der oprettes primoposteringer vil saldi blive bragt frem med økonomiske dimensioner som defineret i skabelonen år end tæt. Begyndelsen saldi poster kan omfatte økonomiske dimensioner ikke længere i de aktuelle konto struktur og målgruppe kombinationer, der ikke længere er gyldige i den aktuelle konto-struktur. Hvis din virksomhed ønsker at udelukke en økonomisk dimension for tilbageholdte vinde startsaldo, angive den økonomiske dimension skal være **Luk enkelt** og tomt dimensionsværdien.

## <a name="run-the-year-end-close-process"></a>Køre årsafslutningsprocessen for Luk
Når årets Luk skabelonerne er oprettet, Luk årsafslutningsprocessen startes ved at vælge **køre regnskabsåret** i handlingsruden. Vælg alle eller en del af retlige enheder fra den skabelon, du vil køre årsafslutningens tæt. Når du kører årets lukker for første gang i et regnskabsår, du alle de juridiske enheder til at oprette primosaldi for alle juridiske enheder sandsynligvis. Hvis du kører årets tæt igen, kan du vælge at køre processen for kun de juridiske enheder, tilpasning af posterne blev bogført. 

Vælg det regnskabsår, du vil køre år Afslut Luk proces mod. Hvis der findes mere end én periode for den sidste periode i regnskabsåret, den **Periodenavnet** felt bliver tilgængeligt, så du kan vælge hvilke ultimoperiode til at bogføre transaktionen lukkes, hvis installationsprogrammet er defineret til at oprette den sidste postering. 

Angiv et bilag nummer, som eller er ikke påkrævet, afhængigt af opsætningen i almindelighed Økonomiparametre. Det samme bilagsnummer, der skal bruges til alle de juridiske enheder, der er valgt for år end lukkeprocessen. Bilagsnummeret er ikke genereret ved hjælp af en nummerserie. Det er den bedste fremgangsmåde til at angive et bilagsnummer, selvom det ikke er påkrævet. Indtaste et bilagsnummer, gør det lettere at åbne posten findes i det nye regnskabsår. Hvis der ikke angives et bilagsnummer, er bilaget tomt for den åbne postering. 

Hvis du vil tilbageføre en tidligere år end tæt for det valgte regnskabsår, skal du angive **fortryde tidligere tæt** til **Ja**. Årets lukning tilbageføres, men processen kan køre igen når som helst. Hvis du tilbagefører en årets Luk, den **dato for sidste år afslutning lukke** vil ikke være tilgængelige. 

Luk årsafslutningsprocessen standarder skal køres i batchtilstand. Det er den bedste fremgangsmåde til at køre processen i batch-tilstand, der tillader brugeren at vende tilbage til andre aktiviteter. Efter år end tæt processen er fuldført, den **dato for sidste år afslutning lukke** vil blive opdateret med sessionsdatoen.

Yderligere oplysninger finder du [lukke finansbogholderiet ved periodens afslutning](close-general-ledger-at-period-end.md).


