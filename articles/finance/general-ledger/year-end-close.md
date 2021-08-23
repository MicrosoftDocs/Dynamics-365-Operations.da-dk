---
title: Årsafslutning
description: Dette emne beskriver den krævede konfiguration og trinnene for at køre årsafslutningsprocessen i Finans.
author: kweekley
ms.date: 07/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5677ebeee6b8260280d4c9c7c8a7a0e18e7bd78f68a42d23967948a2e75120cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778260"
---
# <a name="year-end-close"></a>Årsafslutning

[!include [banner](../includes/banner.md)]

Dette emne beskriver den krævede konfiguration og trinnene for at køre årsafslutningsprocessen i Finans.

Ved slutningen af hvert regnskabsår skal du køre årsafslutningsprocessen for at overføre startsaldi til det nye år. De fleste organisationer kører årsafslutningsprocessen flere gange. Den første kørsel flytter saldi til det nye regnskabsår. Processen kan derefter køres igen, så mange gange det er nødvendigt, for at flytte saldiene fra reguleringsposter til det nye regnskabsår.

Under årsafslutningsprocessen oprettes der to typer af mulige transaktioner. Der genereres altid en åbningstransaktion, der bruges til at oprette startsaldi i det nye regnskabsår. Åbningstransaktionen viser saldiene for statusfinanskonti i det nye regnskabsår og saldi fra driftskonti i finanskontoen for overført overskud i det nye regnskabsår. Den afsluttende postering oprettes eventuelt for at få saldiene på driftskonti til at gå i nul i det regnskabsår, der afsluttes.

## <a name="prepare-to-run-the-year-end-close"></a>Forbered kørsel af årsafslutning

Før du kører årsafslutningsprocessen, skal du validere indstillingerne for følgende:

På siden **Hovedkonto**:

- Kontrollér, at feltet **Hovedkontotype** er indstillet korrekt for hver hovedkonto. Hovedkontotypen bruges til at bestemme, om saldoen på hovedkontoen skal fremføres som en primosaldo eller overføres til overført overskud i primoposteringen.
- Saldoen på hovedkontoen kan overføres til en ny hovedkonto i forbindelse med årsafslutningen. Angiv den nye hovedkonto i feltet **Primokonto**. Dette felt bruges typisk til balancehovedkonti, når hovedkontoen er deaktiveret, og en ny hovedkonto bruges til det nye regnskabsår.

På siden **Finansparametre** under **Årsafslutning**:

- Indstillingen **Slet eksisterende årsafslutningsposter ved afslutning af året** bruges til at angive, om den systemgenererede åbningspostering fra en tidligere årsafslutning skal slettes, når årsafslutningen køres igen. Hvis denne indstilling er angivet til **Ja**, slettes de tidligere primo- og valgfrie ultimoposteringer, og en ny primo- eller ultimopostering oprettes ud fra de aktuelle saldi. Hvis denne indstilling er angivet til **Nej**, bevares de tidligere primo- og valgfrie ultimoposteringer, og der oprettes en ekstra primo- eller ultimopostering for at flytte saldiene fra reguleringsposteringer, der er bogført efter den forrige årsafslutning.
- Indstillingen **Opret ultimoposteringer ved overførsel** bruges til at oprette ultimoposteringer i det regnskabsår, der bliver afsluttet, for at angive saldiene på driftskontiene til 0 (nul). Hvis denne indstilling er angivet til **Ja**, oprettes både primoposteringen og ultimoposteringen. Hvis denne indstilling er angivet til **Nej**, oprettes primoposteringen i det næste regnskabsår for at overføre saldiene. Saldi på driftskonti forbliver i slutningen af regnskabsåret.
- Indstillingen **Indstil status til permanent afsluttet for regnskabsåret** bruges til at angive regnskabsåret til en permanent lukket status. Brug denne indstilling med forsigtighed, da perioder med permanent afsluttet status, ikke kan åbnes igen. Derfor kan reguleringer ikke bogføres i regnskabsåret. Den bedste fremgangsmåde er at angive denne indstilling til **Nej**.
- Indstillingen **Bilagsnummer skal være udfyldt**, hvis indstillingen er fjernet. Der kræves nu et bilag, når årsafslutningsprocessen køres. På det tidspunkt skal bilagsnummeret angives manuelt.

På siden **Regnskabskalender**:

- Det næste regnskabsår skal være oprettet, før du kører årsafslutningen. Ellers kan primosaldi ikke oprettes for primoperioden.

På siden **Finanskalender**:

- Valgfrit: Hver regnskabsperiode for det regnskabsår, der skal afsluttes, kan indstilles til **På hold** for at forhindre, at der indtastes nye posteringer. Når reguleringsposter er identificeret, kan På hold-perioderne genåbnes, så du kan bogføre reguleringsposterne, selv om årsafslutningsprocessen allerede er blevet kørt.

På siden **Opsætning af skabelon for årsafslutning**:

- Når funktionen **Forbedringer af finansårsslutning** er aktiveret, adskilles processen til opsætning af skabelonen for årsslutningen fra processen for kørsel af årsslutningen. Skabelonen kan defineres på siden **Opsætning af skabelon for årsslutning** (**Finans \> Finansopsætning \> Opsætning af skabelon for årsafslutning**), eller den kan åbnes fra årsafslutningsprocessen.

## <a name="define-year-end-close-templates"></a>Angiv årsafslutningsskabeloner

Når systemet er konfigureret, kan du køre årsafslutningsprocessen. På siden **Opsætning af skabelon for årsafslutning** kan en skabelon defineres for den gruppe af juridiske enheder, som årsafslutningsprocessen skal køres for. Skabelonen kan genbruges ved hver årsafslutning, men den kan ændres, hvis din organisation ændres.

Angiv først feltet **Gruppenavn** for skabelonen, og vælge regnskabskalenderen. Gruppenavnet skal identificere gruppen af inkluderede juridiske enheder. Når du bestemmer grupperne af juridiske enheder, skal du huske, at juridiske enheder kun kan medtages i samme gruppe, hvis samme regnskabskalender er valgt for dem. Skabelonerne kan f.eks. oprettes baseret på geografi, og separate grupper kan oprettes for juridiske enheder i Nordamerika, Europa, Mellemøsten og Afrika (EMEA) og Asien og Stillehavsområdet (APAC).

Derefter kan de juridiske enheder føjes til skabelonen. Juridiske enheder kan tilføjes ved at vælge et organisationshierarki eller ved at vælge de juridiske enheder. Hvis et organisatorisk hierarki er valgt, tilføjes kun juridiske enheder i hierarkiet, der bruger den valgte regnskabskalender, til skabelonen. Hvis du bruger juridiske enheder til at føje til skabelonen, kan kun juridiske enheder med samme regnskabskalender tilføjes. Samme regnskabskalender er påkrævet, fordi årsafslutningen køres ved at vælge et regnskabsår, som kan variere fra en kalender til en kalender.

Når de juridiske enheder er tilføjet, kan du definere hovedkontiene for overført overskud for hver juridisk enhed.

Fanen **Økonomiske dimension** bruges til at definere, hvilke økonomiske dimensioner der skal bruges til primoposteringen. Bemærk, at opsætningen af denne fane kun gælder for den juridiske enhed, der er valgt i gitteret **Juridiske enheder**. Du skal gentage opsætningen for hver juridisk enhed i gitteret.

Indstillingen **Overfør balancedimensioner** bruges til at angive, om de økonomiske dimensioner for posteringer, der er bogført på statuskonti, skal opretholdes på primoposteringen. Den bedste fremgangsmåde er at angive denne indstilling til **Ja**. Indstillingen for saldodimensionerne påvirker ikke eksisterende saldi på finanskonti for overført overskud. Disse saldi bestemmes af de overskuds- og tabsdimensioner, der bliver defineret i næste afsnit. Regnskabsåret 2019 var f.eks. det første år, der blev afsluttet, og indstillingen **Afslut alle** blev brugt til at vælge dimensionerne **Afdeling** og **Bærer** til afslutning. I dette tilfælde er der oprettet en separat konto til overført overskud for hver kombination af en afdeling og en bærer. Når årsafslutningen køres for regnskabsåret 2020, forbliver det overførte overskud fra forrige år nøjagtigt som det blev bogført, selvom **Overfør balancedimensioner** angivet til **Nej**. Saldi, der er bogført til overført overskud fra tidligere årsafslutninger, ændres aldrig.

Afsnittet **Overfør overskuds- og tabsdimensioner** bruges til at angive, hvilke økonomiske dimensioner på posteringer, der er bogført på overskuds- og tabskonti og bliver overført til hovedkontoen for overført overskud. Først skal du identificere de økonomiske dimensioner, der er relevante for den valgte juridiske enhed. Disse økonomiske dimensioner inkluderer enhver økonomisk dimension, der er bogført mod i løbet af året, selv om den økonomiske dimension ikke er en del af en aktiv kontostruktur. Derefter skal du angive hver dimension som enten **Luk et enkelt** eller **Luk alle**. Standardindstillingen er **Afslut alle**. Denne indstilling bevarer de oprindelige økonomiske dimensionsværdier fra bogførte posteringer og bruger dem til at oprette primosaldi for resultatkontoen. Der oprettes separate primosaldi for resultatkonti for hver enkelt kombination af økonomiske dimensionsværdier. Hvis **Afslut en enkelt** er valgt, opsummeres alle posteringer, der er bogført med den pågældende økonomiske dimension, i en primosaldo for resultatkonti for den dimensionsværdi, der er angivet i det felt, som vises efter **Afslut en enkelt**. Alle posteringer for regnskabsåret er f.eks. bogført med kontostrukturen **Hovedkonto – Afdeling**. For den økonomiske dimension **Afdeling** i skabelonen er **Afslut en enkelt** valgt, og **100** er angivet som dimensionsværdien. Hvis den samlede indtægt for alle posteringer, der er bogført på afdelingerne 200, 300 og 400 er $100.000, oprettes der en primosaldo for **Overført overskud – 100**. Hvis du vælger **Afslut en enkelt**, men lader den økonomiske dimensionsværdi være tom, bogføres alle posteringer på overført overskud, og dimensionsværdien vil være tom.

## <a name="run-the-year-end-close-process"></a>Kør årsafslutningsprocessen

Når du har oprettet årsafslutningsskabelonerne, kan du starte årsslutningsprocessen på siden **Årsslutning** (**Finans \> Periodeafslutning \> Årsafslutning**). Før du kører årsafslutning, kan du tilføje nye årsafslutningsskabeloner eller redigere eksisterende skabeloner ved at vælge **Opsætning af skabelon for årsslutning** for at åbne opsætningssiden for skabelonerne.

Vælg skabelonen for årsafslutning, og vælg derefter **Kør årsafslutning** i handlingsruden. Vælg enten alle eller et undersæt af juridiske enheder fra den skabelon, som du kører årsafslutningen for. Hvis du kører årsafslutningen for første gang i et regnskabsår, vil du sandsynligvis vælge alle de juridiske enheder, så du kan oprette primosaldi for dem alle. Hvis du har kørt årsafslutningen igen, vil du måske køre den igen kun for de juridiske enheder, hvor der er bogført reguleringsposter.

Vælg derefter det regnskabsår, du vil køre årsafslutningsprocessen for. Hvis der findes mere end én ultimoperiode for sidste periode i regnskabsåret, bliver feltet **Periodenavn** tilgængeligt. Du kan derefter vælge den ultimoperiode, der skal bruges til at bogføre ultimoposteringen, hvis opsætningen er defineret til at oprette ultimoposteringen.

Angiv derefter et bilagsnummer. Det samme bilagsnummer bruges til alle de juridiske enheder, som du har valgt til årsafslutningsprocessen. Bilagsnummeret genereres ikke ved hjælp af en nummerserie.

Årsafslutningsprocessen køres som standard i batchtilstand. Når du har startet den, kan du derfor vende tilbage til andre aktiviteter.

Da kontostrukturer kan ændres i løbet af et regnskabsår, kan den relevante kontostruktur ikke altid identificeres. Derfor overholder årsafslutningsprocessen ikke kontostrukturer. Når der oprettes primoposteringer, føres saldi med økonomiske dimensioner frem som defineret i årsafslutningsskabelonen. Primosaldiposter kan omfatte økonomiske dimensioner, der ikke længere er i den aktuelle kontostruktur og segmentkombinationer, der ikke længere er gyldige i den aktuelle kontostruktur. Hvis din organisation ønsker at udelukke en økonomisk dimension i primosaldoen for overført overskud, skal den økonomiske dimension defineres som **Afslut en enkelt** og dimensionsværdien skal være tom.

Når processen er fuldført, oprettes der en post for hver kombination af en juridisk enhed og et regnskabsår. Du får kun vist poster for de juridiske enheder, som du har adgang til. Hver post indeholder den dato og det klokkeslæt for systemet, hvor processen blev kørt, og et direkte link til de bilag, der blev oprettet for årsafslutningen.

[![Poster, der oprettes i oversigtspanelet Historik for årsafslutning på siden Årsafslutning](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Hvis du kører årsafslutningen igen, vises der en eller flere poster for hver kombination af en juridisk enhed og et regnskabsår, afhængigt af indstillingen for **Slet eksisterende poster for årsafslutning, når året afsluttes igen** på siden **Finansparametre**:

- Hvis indstilingen er angivet til **Ja**, slettes bilaget for den forrige årsafslutning. Posten markeres som **Tilbageført** og stemples med den dato og det klokkeslæt, hvor tilbageførslen blev udført. Derudover fjernes linket til bilagsnummeret. Når årsafslutningen er fuldført, oprettes der en ny post for det nye bilag, der er oprettet.
- Hvis indstillingen er angivet til **Nej**, bevares posten for den tidligere årsafslutning sammen med linket til bilaget. Hver gang årsafslutningen køres igen, oprettes der en ny post sammen med et link til de nye bilag.

## <a name="reverse-the-year-end-close-process"></a>Tilbageføre årsafslutningsprocessen

På siden **Årsafslutning** kan du tilbageføre en årsafslutning. Vælg posten for kombinationen af en juridisk enhed og et regnskabsår, der skal tilbageføres, og vælg derefter **Tilbagefør årsafslutning**. Tilbageførselsprocessen sletter alle primo- og ultimobilag, der er oprettet for regnskabsåret. Posten markeres som **Tilbageført** og stemples med den dato og det klokkeslæt, hvor tilbageførslen blev udført. Derudover fjernes linket til bilagsnummeret. Tilbaførselsprocessen køres i batchtilstand ligesom årsafslutningsprocessen.

Afkrydsningsfeltet **Vis tilbageført**, som er tilgængeligt over gitteret, gør det muligt at skjule eller få vist posterne for tilbageførte årsafslutningsprocesser. Når du har kørt processen **Tilbagefør årsafslutning**, skal du måske markere afkrydsningsfeltet **Vis tilbageført** for at få vist posten. Du kan angive yderligere filtre for at få vist andre oplysninger.

[![Bruge afkrydsningsfeltet Vis tilbageførte til at få vist poster for tilbageførte årsafslutningsprocesser på siden Årsafslutning](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Du kan finde flere oplysninger i [Luk Finans ved periodeafslutning](close-general-ledger-at-period-end.md) og [Lukke regnskabsåret](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
