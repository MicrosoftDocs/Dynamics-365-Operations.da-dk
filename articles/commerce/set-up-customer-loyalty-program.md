---
title: Oversigt over fordelskunde
description: Denne artikel beskriver fordelskundefunktionerne i Dynamics 365 Commerce og de tilsvarende konfigurationstrin, der kan hjælpe detailhandlere i gang med deres fordelskundeprogram.
author: josaw1
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.custom: 16201, "intro-internal"
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
ms.openlocfilehash: 17742bb5c0091804fc6f43bb2aabb7af73229890
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9784958"
---
# <a name="loyalty-overview"></a>Oversigt over fordelskundeprogrammer

[!include [banner](includes/banner.md)]

Med fordelskundeprogrammer kan forhandlere sikre kundeloyalitet ved at belønne kunderne for deres brug af detailhandlerens mærke. I Dynamics 365 Commerce kan du oprette enkle eller komplekse fordelskundeprogrammer, der gælder på tværs af juridiske enheder i enhver handelskanal. Denne artikel beskriver fordelskundefunktionerne i Commerce og de tilsvarende konfigurationstrin, der kan hjælpe detailhandlere i gang med deres fordelskundeprogrammer.

Du kan konfigurere fordelskundeprogrammet, så det inkluderer følgende indstillinger.

- Angiv flere typer bonusser, som du tilbyder i dine fordelskundeprogrammer, og spor deltagelse i dine fordelskundeprogrammer.
- Konfigurer fordelskundeprogrammer, der repræsenterer de forskellige bonusincitamenter, du tilbyder. Du kan medtage niveauer af fordelskundeprogrammer for at tilbyde større incitamenter og belønninger til kunder, der køber oftere eller bruge flere penge i dine butikker.
- Angiv optjeningsregler for at identificere de aktiviteter, en kunde skal udføre for at optjene belønninger. Du kan også definere indløsningsregler for at identificere, hvornår og hvordan en kunde kan indløse belønninger.
- Udsted fordelskundekort fra enhver kanal, der deltager i dine fordelskundeprogrammer, og knyt fordelskundekort til et eller flere fordelskundeprogrammer, som kunden kan deltage i. Du kan også sammenkæde en kundepost med et fordelskundekort, så kunden kan samle fordelskundepoint fra flere kort og indløse dem.
- Juster manuelt fordelskundekort, eller overfør fordelsbelønningssaldoen fra ét kort til et andet for at tilpasse den til og belønne en kunde.

Følgende video indeholder en oversigt og demo over loyalitetsfunktioner i Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5c2wW]

## <a name="setting-up-loyalty-programs"></a>Konfigurere loyalitetsprogrammer

Du skal oprette flere komponenter for at aktivere funktionen for fordelskunder i Commerce. I følgende diagram illustreres fordelskundekomponenter, og hvordan de er relateret til hinanden.

![Procesforløb for opsætning af kundefordel.](./media/loyaltyprocess.gif "Fordelskundekomponenter, og hvordan de er relateret til hinanden")

## <a name="loyalty-components"></a>Fordelskundekomponenter

I følgende tabel beskrives de enkelte komponenter, og hvor de er anvendt i opsætningen af fordelskunder.

| Komponent                                        | Betegnelse | Hvor den bruges |
|--------------------------------------------------|-------------|-----------------|
| Konfigurer rabatter (forudsætning)                  | Konfigurer de rabatter, du tilbyder dine fordelskunder. Eksempelvis kan du tilbyde en rabat på 5 % på alle beklædningsprodukter. | Rabatter skal føjes til prisgrupper, før de kan indgå i et fordelskundeprogram. Prisgrupper tildeles til fordelskundeprogrammer og fordelskundeniveauer. |
| Konfigurer prisgrupper (forudsætning)               | Prisgrupper bruges til at oprette og administrere priser og rabatter for produkter. Du kan oprette prisgrupper, der indeholder de rabatter, der gælder for din fordelskundeprogrammer. | Prisgrupper tildeles til fordelskundeprogrammer og niveauer af fordelskundeprogrammer. |
| Konfigurer kanaler (forudsætning)                   | Commerce-kanaler er de butikker, der deltager i fordelskundeprogrammer, f.eks. en fysisk butik, en onlinebutik eller et callcenter. Du skal oprette dine kanaler, før du kan tildele fordelskundeprogrammer til dem. | Du tildeler kanaler til et fordelskundeprogram, hvis kanalen deltager i fordelskundeprogrammet. |
| Konfigurer metoden for fordelskundebetaling (forudsætning) | Hvis du vil sikre, at fordelskundepointene kan indløses i en hvilken som helst kanal, f.eks. fysiske butikker, onlinebutikker eller callcentre, skal du konfigurere beholderintervallet for fordelskundekortet på siden **Kortnumre**. | Opret en betalingsmetode for fordelskunder, og tildel derefter betalingsmetode for fordelskunder til de kanaler, der deltager i fordelskundeprogrammet. |
| Konfigurer datointervaller                            | Med datointervaller kan du angive fleksible tidsintervaller, der gælder for niveauer for fordelskunder. Du kan bruge datointervallerne til at angive, hvor lang tid en kunde kan forblive på et niveau, eller hvor lang tid en kunde har til at udføre en aktivitet, der berettiger til et niveau. | Datointervaller gælder kun, hvis du bruger niveauer i dine fordelskundeprogrammer. Du kan vælge det datointerval, der gælder for programniveauer, og de datointervaller, der gælder for regler for programniveau. |
| Opret belønningspoint                             | Belønningspoint er de typer bonus, du tilbyder dine kunder. Belønningspoint kan enten indløses eller ikke indløses. Belønningspoint, der kan indløses, kan byttes til produkter. Ikke-indløselige belønningspoint bruges til sporing eller til at flytte en kunde til det næste niveau i et fordelskundeprogram. | Der henvises til belønningspoint i reglerne for niveauer, og de bruges til at kvalificere en kunde til et bestemt niveau. Der henvises også til belønningspoint i fordelskundeplaner i regler for optjening og indløsning. I regler for optjening kan du angive den belønning, som en kunde kan optjene for en bestemt aktivitet. I regler for indløsning kan du angive den belønning, som kunden kan indløse. |
| Konfigurere fordelskundeprogrammer                          | Fordelskundeprogrammer er den centrale fordelskundeenhed, du tilbyder. Alle fordelskundeprogrammer kan også have tildelt niveauer for fordelskunder. Rabatter og prisgrupper tildeles til fordelskundeprogrammer på programniveau eller på fordelskundeniveauet. | Du kan oprette fordelskundeplaner for dine fordelskundeprogrammer. Du tildeler dine fordelskundekort til dine fordelskundeprogrammer, og fordelskundekort kan tildeles til en kunde. Kanaler deltager i de fordelskundeprogrammer, der er tildelt til fordelskundeplaner. Kunder, der ejer et fordelskundekort, kan deltage i de fordelskundeprogrammer, der er knyttet til kortet. |
| Konfigurer niveauer for fordelskunder og regler for niveauer              | Niveauer for fordelskunder er valgfrie niveauer, som du definerer for dine fordelskundeprogrammer. Du kan oprette grundlæggende rabatter og belønninger for alle kunder, der deltager i fordelskundeprogrammet, og du kan angive yderligere rabatter og belønninger for kunder, der optjener de forskellige niveauer i programmet. For hvert niveau for fordelskunder, som du definerer, kan du konfigurere de regler, der kvalificerer en kunde til det pågældende niveau. Du kan også definere, hvor lang tid kunder kan forblive på dette niveau, når de har nået det. | Niveauer for fordelskunder og regler for niveauer defineres i fordelskundeprogrammerne. Hvis du ikke definerer eventuelle niveauer for fordelskunder, er alle kunder, der deltager i fordelskundeprogrammet, berettiget til de rabatter, som du tildeler i prisgruppen for fordelskundeprogrammet. Hvis du definerer niveauer for fordelskunder, kan du angive optjeningsregler og indløsningsregler for niveauer for fordelskunder i fordelskundeplanen. |
| Opsætning af fordelskundeplaner                           | Fordelskundeplaner angiver de optjenings- og indløsningsregler, der gælder for et bestemt fordelskundeprogram. Du tildeler kanaler til en fordelskundeplan for at identificere, hvilket fordelskundeprogram, hvilke optjeningsregler og hvilke indløsningsregler der gælder for en butik. | En fordelskundeplan tildeles et fordelskundeprogram og kanaler. Du kan tildele mange fordelskundeplaner til samme fordelskundeprogram, og du kan tildele mange fordelskundeplaner til mange kanaler. |
| Opsætning af fordelskundekort                             | Et fordelskundekort giver kortindehaveren ret til at deltage i de fordelskundeprogrammer, der er knyttet til kortet. Fordelskundekort kan udstedes anonymt, eller de kan tildeles til en bestemt kunde. Du kan få vist fordelskundeposteringer for et bestemt kort, og du kan få vist en oversigt over de fordelskundepoint, der er akkumuleret på kortet. Du kan udstede fordelskundekort fra enhver kanal. Du kan også manuelt justere et fordelskundekort for at opgradere kunden til et andet niveau, tilføje fordelskundepoint eller overføre fordelskundepointsaldoen fra ét kort til et andet. | Du tildeler fordelskundeprogrammer til et fordelskundekort. |

## <a name="loyalty-processes"></a>Fordelskundeprocesser

I følgende tabel beskrives de processer, der skal køres, for at sende konfigurationer af og data til fordelskundekort til dine butikker og hente fordelskundetransaktioner fra dine butikker.

| Procesnavn                         | Beskrivelse | Sidens navn |
|--------------------------------------|-------------|-----------|
| 1050 (oplysninger om fordelskunder)           | Kør denne proces for at sende fordelskundedata fra Commerce til butikkerne. Det er en god ide at planlægge denne proces til at køre ofte, så fordelskundedata overføres til alle butikker. | Distributionsplan |
| Udfør behandling af fordelskundeprogrammer              | Kør denne proces for at knytte fordelskundeplaner til de kanaler, der er tildelt fordelskundeplanen. Denne proces kan planlægges til at køre som en batchproces. Hvis du ændrer konfigurationsdataene for fordelskundeplaner, f.eks. fordelskundeprogrammer eller fordelskundebelønningspoint, skal du køre denne proces. | Udfør behandling af fordelskundeprogrammer |
| Bogfør optjente kundefordelspoint i batches | Kør denne proces for at opdatere fordelskundekort, så de medtager posteringer, der er behandlet offline. Denne proces gælder kun, hvis afkrydsningsfeltet **Bogfør optjente point i batches** er markeret på siden **Delte parametre for Commerce**, så der kan optjenes belønninger offline. | Bogfør optjente kundefordelspoint i batches |
| Opdater fordelskundeniveauer            | Kør denne proces for at vurdere kundens optjeningsaktivitet i forhold til niveaureglerne for et fordelskundeprogram og for at opdatere status for kundens niveau. Denne proces skal kun bruges, hvis du ændrer niveaureglerne i fordelskundeprogrammer, og de opdaterede regler skal anvendes med tilbagevirkende kraft for fordelskundekort, der allerede er udstedt. Denne proces kan køres som en batchproces eller for de enkelte kort. | Opdater fordelskundeniveauer |

## <a name="loyalty-capabilities"></a>Fordelskundefunktioner

- Ved hjælp af de prisgrupper, der er tilknyttet fordelskundeprogrammet og fordelskundeniveau, kan detailhandlere nemt oprette særlige priser og rabatter for fordelskundemedlemmer.

- Som en del af et fordelskundeprogram kan detailhandlere oprette optjenings- og indløsningsregler på forskellige niveauer for at adskille fra belønningerne for debitorer på andre niveauer. Detailhandlere kan også inkludere "tilhørsforhold" som en del af reglerne for optjening og indløsning, så bestemte kundegrupper kan være en del af eksisterende niveauer, men stadig blive belønnet forskelligt. Det fjerner behovet for at oprette flere niveauer.
    
    > [!NOTE]
    > Der er yderligere optjeningsregler i et fordelskundeprogram. F.eks. hvis du opretter en regel, der belønner et medlem på gold-niveau med 10 point for hver amerikanske dollar, og du også opretter en regel for en kunde med "veteran" tilknytning, der belønner med 5 point for hver amerikanske dollar, vil en veteran, der er også medlem på gold-niveau, få 15 point for 1 dollar, fordi kunden opfylder betingelserne for begge linjer. Men hvis veterankunden ikke er medlem på gold-niveau, får vedkommende 5 point for hver dollar. For at afspejle ændringerne i kanalerne skal du køre jobbene **Udfør behandling af fordelskundeprogrammer** og **1050** (med oplysninger om fordelskundekort).
    
    ![Tilknytningsbaseret optjening.](./media/Affiliation-based-earning.png "Tilknytningsbaseret optjening")

- Detailhandlere har ofte særpriser for en bestemt gruppe af kunder, som de ikke ønsker, at fordelskundeprogrammer skal gælde for. Det kan f.eks. dreje sig om grossister eller medarbejdere, der får særpriser og ingen fordelskundepoint. "Tilknytninger" bruges ofte til at give særpriser til sådanne kundegrupper. For at begrænse visse grupper af kunders mulighed for at opnå fordelskundepoint kan forhandleren angive en eller flere tilknytninger under sektionen **Udeladte tilknytninger** i fordelskundeprogrammet. Så når eksisterende kunder, der tilhører udeladte tilknytninger, er fordelskundemedlemmer, kan de ikke optjene kundefordelspoint for deres indkøb. For at afspejle ændringerne i kanalerne skal du køre jobbene **Udfør behandling af fordelskundeprogrammer** og **1050** (med oplysninger om fordelskundekort).

    ![Udeladte tilknytninger.](./media/Excluded-affiliations.png "Udeladte tilknytninger, som ikke kan optjene fordelskundepoint")
    
- Med POS kan detailhandler en bruge fleksibiliteten til enten de fysiske fordelskundekort eller til at generere et entydigt fordelskundekortnummer automatisk. Hvis du vil aktivere den automatiske generering af fordelskundekort i butikkerne, skal du slå **Generer nummer til fordelskundekort** til i funktionalitetsprofilen, der er knyttet til butikken. Ved onlinekanaler kan detailhandlere bruge IssueLoyaltyCard-API'en til at udstede fordelskundekort til kunder. Detailhandlere kan enten angive et fordelskundekortnummer til denne API, som skal bruges til at generere fordelskundekortet, eller systemet bruger nummerserien for fordelskundekort i Commerce. Men hvis nummerserien findes ikke, og forhandleren ikke angiver et fordelskundekortnummer under kald af API'en, opstår der en fejl.

    ![Generere fordelskundekort.](./media/Generate-loyalty-card.png "Automatisk generering af fordelskundekortnummer")

- Fordelskundepoint, der er optjent og indløst, kan nu gemmes for hver transaktion og salgsordre i forhold til salgslinjen, så det samme beløb, der kan refunderes eller tilbageføres ved hele eller delvise returneringer. Desuden kan callcenterbrugere, der kan se point på salgslinjeniveau, besvare spørgsmål fra kunder om, hvor mange point der er optjent eller indløst for hver linje. Før denne ændring blev optjente point altid genberegnet under returneringer, hvilket resulterede i et andet beløb end det oprindelige, hvis optjenings- eller indløsningsreglerne blev ændret, og desuden havde callcenterbrugerne ikke indsigt i pointopdelingen. Antal point kan ses under formularen **Korttransaktioner** for hvert fordelskundekort. For at aktivere denne funktion skal du aktivere konfigurationen **Bogfør fordelskundepoint pr. salgslinje** under **Delte parametre for Commerce** \> fanen **Generelt**.

    > [!NOTE]
    > Vi anbefaler at slå denne funktion til for i tilfælde af returneringer at sikre, at det rigtige antal point kan refunderes eller hentes fra kunden.

- Detailhandlere kan nu definere fordelingsperioden for hvert optjente point. Konfiguration af en fordelingsperiode kan definere varighed fra optjeningsdatoen, efter hvilken de optjente point bliver tilgængelige for kunderne. Ikke-optjente point kan ses i kolonnen **Ikke-optjente point** på siden **Fordelskundekort**. Når kunderne returnerer nogle varer, som fordelskundepointene er optjent for, vil systemet som standard fratrække de ikke-optjente point først og derefter trække en eventuel saldo fra de tilgængelige point. Men du kan kun konfigurere at fratrække de tilgængelige point i stedet for at trække dem fra ikke-optjente point.

Detailhandlere kan desuden definere grænsen for maksimalt antal kundefordelspoint pr. fordelskundekort. Dette felt kan bruges til at reducere effekten af svindel med fordelskundeprogrammet. Når brugeren har nået det maksimale antal belønningspoint, kan vedkommende ikke få flere point. Forhandleren kan vælge at blokere sådanne kort, indtil de er undersøgt for potentiel svindel. Hvis forhandleren opdager svindel, kan denne spærre kundens fordelskundekort og angive en kunde som spærret. Det kan gøres ved at indstille egenskaben **Spær for tilmelding til fordelskundeprogram for kunden** til **Ja** under **Alle kunder** i **Commerce**-oversigtspanelet. Der kan ikke udstedes et fordelskundekort til spærrede kunder i nogen af kanalerne.

   ![Fordelingspoint og maksimale bonuspoint.](./media/Vesting-and-maximum-reward-points.png "Definere fordelingspoint og maksimale belønningspoint")

- Tilknytninger bruges til at give særpriser og rabatter, men der kan være nogle tilknytninger, som detailhandlerne ikke ønsker, at kunderne skal se. F.eks. vil en tilknytning med titlen "Kunde med stort købspotentiale" muligvis ikke falde i god jord hos nogle kunder. Der er desuden nogle tilknytninger, der ikke skal administreres i butikken, f.eks. medarbejdere, fordi du sikkert ikke vil have, at kassereren skal bestemme, hvem der er medarbejder og dermed give medarbejderbaserede rabatter. Detailhandlere kan nu vælge, hvilke tilknytninger der skal være skjult i kanalerne. Tilknytninger, der er markeret som **Skjul i kanaler**, kan ikke vises, tilføjes eller fjernes i POS. Dog vil priser og rabatter, der gælder for tilknytningen, stadig blive anvendt på produkterne.

    ![Skjule tilhørsforhold.](./media/Hide-affiliations.png "Skjule tilknytninger i kanaler")
    
- Callcenterbrugere kan nu nemmere søge efter en kunde ved hjælp af kundens fordelskundekortoplysninger og navigere til kundens fordelskundekort og siden over transaktioner udført med fordelskundekortet fra siden **Kundeservice**.

    ![Kundeservice.](./media/Customer-service.png "Finde kundens fordelskundeoplysninger")
    
- Hvis en kunde mister et fordelskundekort, skal der oprettes et erstatningskort, og de eksisterende point skal overføres til det nye kort. Processen til udstedelse af erstatningskort er forenklet i denne version. Desuden kan kunder kan forære nogle eller alle deres fordelskundepoint til venner og familie. Ved overførsel af point oprettes der reguleringsposter for hvert fordelskundekort. Du kan få adgang til erstatningskortfunktioner og overførsel af saldo fra siden **Fordelskundekort**.

    ![Erstatte og overføre point.](./media/Replace-and-transfer-points.png "Erstatte fordelskundekort eller overføre saldo")
    
- Detailhandlere ønsker muligvis at udnytte effektiviteten ved en bestemt kanal til at tilmelde kunder til et fordelskundeprogram. Tilmeldingskilden til fordelskundekortene bliver nu gemt, så detailhandlere kan køre rapporter på disse data. Tilmeldingskilderne registreres automatisk for alle udstedte fordelskundekort fra MPOS/CPOS- eller e-handelskanaler. For de fordelskundekort, der er udstedt fra administrationsprogrammet, kan callcenterbrugeren vælge den ønskede kanal.
- I tidligere udgaver kunne detailhandlerne bruge MPOS/CPOS til at indløse fordelskundepoint for kunder i en butik. Men da kundefordelssaldoen i disse udgaver vises i fordelskundepoint, kan kassereren ikke se den valutabeløbsværdi, der kan anvendes på den aktuelle transaktion. Kassereren skal omregne pointene til valuta, før der kan betales med fordelskundepoint. I den aktuelle version, kan kassereren, når linjerne er føjet til transaktionen, se det beløb, som fordelskundepointene kan dække for den aktuelle transaktion, hvilket gør det lettere at anvende alle eller nogle af fordelskundepointene på transaktionen. Kassereren kan desuden se de point, der udløber inden for næste 30 dage, så han eller hun kan anbefale mersalg eller krydssalg for at motivere kunden til at bruge de point, der udløber, på den pågældende transaktion.

    ![Point, der er omfattet af fordelskundesaldoen.](./media/Points-covered-by-loyalty-balance.png "Vise saldo, der er omfattet af fordelskundepoint")

    ![Point, der udløber.](./media/Expiring-points.png "Se point, der udløber")

- Med version 8.1.3 har vi aktiveret indstillingen "Betal med fordelskundekort" i callcenterkanalen. For at aktivere denne indstilling skal du oprette en betalingsmiddeltype og knytte den til callcenteret. 

    > [!NOTE]
    > Da fordelskundebetalingerne er konfigureret som kortbetalinger, skal du vælge et kort fra siden **Opsætning af kort**. 

    ![Opsætning af fordelskundekort.](./media/LoyaltyCardSetup.png "Opsætning af fordelskundekort")

    Når dette er oprettet, kan kunder indløse deres fordelskundepoint i callcenteret. Derudover forbedrer vi brugeroplevelsen yderligere, så "Beløb, der er omfattet af fordelskundepoint" vises, og så callcenterets brugere ikke behøver at gå til en anden skærm for at få vist fordelssaldoen.

- Mange detailhandlere tildeler kun fordelskundepoint baseret på salgstransaktionerne, men mere kundefokuserede forhandlerne vil gerne kunne belønne kunderne, hver gang kunden indgår i en aktivitet med deres varemærke. De vil for eksempel kunne give kunderne belønninger for fuldførelse af en onlineundersøgelse, besøg i en butik, angivelse af "synes godt om" forhandlerne på Facebook eller tweet om forhandleren. Når forhandleren vil gøre det, skal han eller hun definere et antal af en "Anden aktivitetstype" og angive de tilsvarende optjeningsregler for disse aktiviteter. Der findes også en "PostNonTransactionalActivityLoyaltyPoints", der vises i Commerce Scale Unit-API, og som kan kaldes, når en aktivitet, der skal belønne kunden med fordelskundepoint, identificeres. Denne API forventer fordelskort-id, kanal-id og id for anden aktivitetstype , så den kunde, der skal belønnes, kan findes, og indtægtsreglen for aktiviteten kan identificeres. 

    Tildeling af point for ikke-transaktionsaktiviteter har generelt to overordnede trin:

    - En aktivitet er realiseret, og det bør blive belønnet.
    - Tildeling af de relevante point.

    Det første trin er eksternt i forhold til Commerce, f.eks. tweeting om mærket eller angivelse af "synes godt om" på Facebook. Når denne aktivitet er anerkendt, kan forhandlerne kalde ovennævnte Commerce Scale Unit-API og tildele fordelskundepoint i realtid. I sådanne tilfælde er der ikke behov for et gennemsynstrin, fordi der er udført en aktivitet, og der skal tildeles tilsvarende point. Der er dog situationer, hvor forhandleren bør gennemse posterne, før der tildeles point. For eksempel har forhandleren oprettet en workshop i butikken, som kunderne kan tilmelde sig på e-handelswebstedet eller i ethvert andet program til registrering af arrangementer. Det er dog kun de deltagende kunder, der skal optjene kundefordelspoint. I version 10.0 introducerede vi en dataenhed, **Andre aktivitetstypelinjer for detailfordelskunde**, til brug i sådanne tilfælde. Med denne dataenhed kan forhandlerne at bruge enten strukturen til dataimport/-eksport (DIXF) eller OData API'en til at registrere de aktiviteter, der skal belønne kunder med fordelskundepoint. Dataenheden gemmer aktiviteterne i kladden **Fordelskundelinjer til andre aktiviteter**, som kan bruges til gennemsyn og ændring. Når dataene er blevet gennemgået, kan it-brugeren manuelt bogføre aktivitetslinjerne eller køre et job med navnet **Behandle anden aktivitetstype for fordelskundelinjer**, som bogfører alle ikke-bogførte aktivitetslinjer og tildeler point til kunderne baseret på indtægtsreglerne. I eksemplet ovenfor vil hændelsesregistreringsprogrammet kalde OData API for at sende kundeoplysningerne til Commerce. It-brugeren kan dog kun bogføre aktivitetslinjerne for de kunder, der har deltaget i workshoppen, og slette aktivitetslinjerne for de øvrige kunder. 

    > [!NOTE]
    > I øjeblikket tvinger systemet brugerne til at konfigurere en nummerserie for "andre aktivitetstyper", men dette er ikke et nødvendigt trin i fremtidige versioner. Hvis du vil konfigurere en nummerserie, skal du gå til **Delte parametre for Commerce** \> **Nummerserier** og vælge en nummerserie for **Id for anden aktivitetstype for fordelskunde**.

- For at give god kundeservice og effektivt løse kundens spørgsmål er det vigtigt for kasserere skal have adgang til at fuldføre kundens profil. Med 10.0 udgivelsen kan kasserere se historikdetaljer for fordelskunder sammen med oplysninger om det tilknyttede fordelskundeprogram og niveauer på POS.
- Gratis eller nedsat levering er en af de faktorer, der motiverer kunderne stærkt til at købe online. For at gøre det muligt for detailforretninger at køre leveringskampagner med 10.0 udgivelsen har vi introduceret en ny type kampagne, "Leveringstærskelrabat", hvor forhandleren kan definere tærskelværdier, som, når de opfyldes, vil kvalificere kunderne til billig eller gratis forsendelse. For eksempel Brug 35 USD og få gratis 'Levering på to dage' eller gratis 'Levering på to dage' for alle fordelskunder. Denne funktion udnytter den nye egenskab Avancerede automatiske gebyrer. Se [dokumentationen om avancerede automatiske gebyrer](/dynamics365/unified-operations/retail/omni-auto-charges). Disse avancerede automatiske gebyrer skal aktiveres, for at leveringskampagner kan bruges. De kan aktiveres fra fanen **Kundeordrer** på siden **Commerce-parametre**, hvor du skal aktivere konfigurationen "Brug avancerede automatiske gebyrer". Fordi en forhandler kan oprette flere gebyrtyper, f.eks. håndtering eller installation, skal forhandleren desuden angive, hvilket gebyr der betragtes som forsendelsesgebyrer. Forsendelsesrabatterne anvendes kun på forsendelsesgebyrerne. For at angive gebyrer som forsendelsesgebyr skal du gå til formularen **Gebyrkoder**, der findes under **Retail og Commerce** \> **Retail og Commerce IT** \> **Konfiguration af kanal** \> **Gebyrer** og aktivere afkrydsningsfeltet "Forsendelsesgebyr" for de ønskede gebyrer. Nu kan du navigere til formularen **Leveringstærskelrabat** og konfigurere rabatten.

    Som ved produktrabatter bruger denne rabat alle de eksisterende standardrabatmuligheder, f.eks. giver forhandleren mulighed for at begrænse disse rabatter med kuponer, så kun kunder med kuponer, kan få disse rabatter. Desuden udnytter disse rabatter Prisgrupper-funktionen til at fastslå berettigelsen af disse rabatter. Forhandleren kan f.eks. vælge kun at køre disse kampagner i onlinekanalerne og/eller på tværs af kanaler til bestemte kundegrupper, f.eks. fordelskunder. Når ordrelinjerne med den angivne leveringstilstand overholder den definerede grænse, bliver leveringsrabatten anvendes og reducerer forsendelsesgebyret baseret på den angivne rabatopsætning. 

    > [!NOTE]
    > I modsætning til andre periodiske rabatter som antal, enkel, mix og match og tærskelrabatter, opretter leveringsrabatten ikke rabatlinjer, men redigerer snarere forsendelsesgebyret direkte og knytter navnet på rabatten til gebyrbeskrivelsen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
