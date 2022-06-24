---
title: Hvorfor kan jeg ikke tilbageføre denne postering?
description: Denne artikel beskriver forskellige årsager til, at posteringer ikke kan tilbageføres. Den indeholder også en oversigt over løsninger på dette problem.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9a8b26584b1a9b82440583db693cd14daa580e22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876176"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Hvorfor kan jeg ikke tilbageføre denne postering?

[!include [banner](../includes/banner.md)]

Denne artikel beskriver forskellige årsager til, at posteringer ikke kan tilbageføres. Den indeholder også en oversigt over løsninger på dette problem.

## <a name="symptom"></a>Symptom

Organisationer kan komme ud for situationer, hvor de skal tilbageføre en postering, som de har bogført. I enkelte tilfælde vil systemet forhindre dem i at tilbageføre disse posteringer. Denne funktionsmåde kan give to spørgsmål:

- Hvorfor kan jeg ikke tilbageføre posteringen?
- Hvordan påvirker funktionen til massetilbageførsel denne funktionsmåde?

## <a name="resolution"></a>Løsning

Posteringer skal opfylde bestemte kriterier, før de kan tilbageføres. De resterende afsnit i denne artikel indeholder validering for hvert modul. Selvom der i denne artikel fokuseres på posteringer i Microsoft Dynamics 365 Finance, kan nogle af begreberne og valideringen anvendes i andre apps, f.eks. Dynamics 365 Supply Chain Management.

Det sted, hvor en postering tilbageføres, kan desuden påvirke, om den kan tilbageføres. En kreditorbetaling, der bogføres som en check, kan f.eks. kun tilbageføres fra sektionen **Checks** på posteringssiden for bankkontiene. Den kan ikke tilbageføres fra siden **Posteringer på bilag** i Finans.

Hvis **Massetilbageførsel for flere dokumenter** (også kaldet funktionen Massetilbageførsel) er aktiveret i arbejdsområdet **Funktionsstyring**, har det indflydelse på, hvor mange posteringer der kan tilbageføres, og hvor de kan tilbageføres. Denne funktion giver to fordele, når den er slået til:

- Ved visse posteringstyper kan der vælges og tilbageføres mere end én postering ad gangen fra den kladde, den blev bogført fra, eller fra siden **Posteringer på bilag**. De enkelte posteringer skal dog være tilbageførselsberettigede, før funktionen blev aktiveret. Før denne funktion blev indført, skulle posteringer tilbageføres én ad gangen.
- *Visse* posteringer for reskontro kan tilbageføres fra kladden (finanskladden) eller siden **Posteringer på bilag**. De behøver ikke at blive tilbageført fra reskontrosiden. En kreditorfakturakladde kunne f.eks. tidligere kun tilbageføres fra siden **Kreditorposteringer**. Den kan dog nu også tilbageføres fra Finans-siden fra kladden eller siden **Posteringer på bilag**. Hvert afsnit i denne artikel indeholder en forklaring på de typer transaktioner, denne fordel ikke gælder for.

Funktionen til massetilbageførsel giver **ikke** mulighed for at tilbageføre flere posteringstyper. Hvis en posteringstype ikke tidligere kunne tilbageføres, kan den stadig ikke tilbageføres, efter at funktionen er aktiveret. Kreditorfakturaer for indkøbsordrer kan f.eks. ikke tilbageføres, uanset om funktionen Massetilbageførsel er aktiveret.

Yderligere oplysninger om funktionen Massetilbageførsel finder du i [Tilbageføre kladdebogføring](reverse-journal-posting.md).

## <a name="general-ledger"></a>Finans

Reguleringer af finansmodulet angives kun ved hjælp af finanskonti. Derfor opdaterer de kun finans.

Hvis funktionen Massetilbageførsel er deaktiveret, kan de fleste justeringer i finans tilbageføres individuelt fra siden **Posteringer \<main account\>** for finans (**LedgerTransAccount**). (Den nøjagtige titel på siden varierer, afhængigt af den valgte hovedkonto). På siden vises de enkelte posteringer, der er bogført på hovedkontoen. Den åbnes typisk fra listesiden **Prøvesaldo** eller ved at vælge **Posteringer** på siden **Posteringer på bilag**.

Hvis funktionen Massetilbageførsel er aktiveret, kan et eller flere finansbilag nu tilbageføres fra siden **Posteringer på bilag** og fra den kladde, som posteringen blev bogført fra. Undtagelserne er værdiregulerings-, konsoliderings- og årsafslutningsposteringer af udenlandsk valuta i finansmodulet. Disse posteringer tilbageføres fra de sider, som årsafslutningen blev kørt fra.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsager til, at posteringer ikke kan tilbageføres

Posteringer kan ikke tilbageføres af følgende årsager:

- Finanskladde:

    - Regnskabsperioden er på hold eller lukket permanent:

        - Hvis tilbageførselsdatoen ligger i en regnskabsperiode, der ikke er åben, kan posteringen ikke tilbageføres.
        - Hvis posteringen understøtter indtastning af en tilbageførselsdato, kan posteringen stadig tilbageføres ved at ændre tilbageførselsdatoen til en åben periode.

    - Processen til årsafslutning er kørt:

        - Regnskabsdatoen for posteringen ligger i et regnskabsår, hvor der er kørt en årsafslutning. Selvom en periode i regnskabsåret stadig er åben, kan posteringen ikke tilbageføres, hvis der er kørt årsafslutningsproces for regnskabsåret. Regnskabsåret har en anden status end perioderne i det.
        - Årsafslutningen kan tilbageføres, og derefter kan posteringen tilbageføres. Denne metode er måske ikke en mulighed. Det kan være lettere at angive en tilbageførselspostering manuelt i en åben periode for enten det lukkede regnskabsår eller det næste regnskabsår, afhængigt af statussen for processen til regnskabsafslutning. Hvis en ny postering bogføres i en åben periode i regnskabsåret, som har været gennem årsafslutningsprocessen, skal årsafslutningen køres igen.

    - Tilbageførsel af postering er allerede i gang:

        - Hvis posteringen er ved at blive tilbageført, skal den pågældende proces fuldføres. Der kan ikke udføres en separat tilbageførsel. 
        - Når tilbageførslen er fuldført, kan en tilbageført postering tilbageføres igen (det betyder, at tilbageførslen kan tilbageføres).

    - Finansudligning:

        - Hvis en eller flere linjer i posteringen er finansudlignet ved hjælp af den periodiske opgave **Finansudligninger** (**Finans \> Periodiske opgaver \> Finansudligninger**), så posten findes i tabellen LedgerTransSettlement, kan posteringen ikke tilbageføres.
        - Finansudligningen kan tilbageføres, og derefter kan bilaget tilbageføres.

    - Intern handel:

        - Hvis posteringen er en intern postering, kan den ikke tilbageføres.
        - Posteringen er **ikke** en intern postering, men bogføres på en "forfalden til" eller "forfalden fra" hovedkonto, der blev defineret på siden **Opsætning af internt firma**.

    - Periodiseringer:

        - Hvis det periodiserede finansbilag tilbageføres, tilbageføres den periodiserede post og alle de tilsvarende periodiseringsunderposteringer.
        - De enkelte periodiseringsunderposteringer kan ikke tilbageføres.

- Indtægtsføringskladde:

    - Indtægtsføringsposteringer kan ikke tilbageføres.
    - Når omsætningen registreres via indtægtsføringskladden, bogføres bilaget kun på finanskonti. På sider som f.eks. **Posteringer på bilag** vises posteringerne derfor, som om de kun var finansposter.

- Kursregulering:

    - Kursreguleringsposteringer af udenlandsk valuta kan tilbageføres, men kun fra siden finanssiden **Kursregulering**, som værdireguleringen blev kørt fra.
    - Tilbageførslen kan kun fuldføres, hvis den er bogført i en åben regnskabsperiode.

- Konsolidering:

    - Konsolideringsposteringer kan tilbageføres, men kun fra siden **Konsolideringsposteringer**.
    - Tilbageførslen kan kun fuldføres, hvis den er bogført i en åben regnskabsperiode.

- Årsafslutning:

    - Årsafslutningsposteringer (både ultimo- og primoposter) kan tilbageføres på følgende måder:

        - Hvis forbedringsfunktionen til finansårsafslutning er deaktiveret, skal du vælge indstillingen **Fortryd forrige lukning** i dialogboksen **Årsafslutning**.
        - Hvis forbedringsfunktionen til finansårsafslutning er aktiveret, skal du vælge det firma og de poster for regnskabsåret, der blev oprettet til årsafslutningen på siden **Årsafslutning** og derefter vælge **Tilbagefør årsafslutning**.

    - Bemærk, at tilbageførsel af årsafslutningen faktisk sletter ultimo- og primoposteringerne. Et tilbageførselsbilag bogføres aldrig.

## <a name="accounts-payable"></a>Kreditor

Flere posteringstyper opdaterer kreditorreskontroen. Det kan f.eks. være kreditorfakturaer, kreditorfakturakladder og udgiftsrapporter.

Hvis funktionen Massetilbageførsel er deaktiveret, kan posteringer tilbageføres individuelt fra siden **Kreditorposteringer** for fakturaer eller siden **Bankkonto** til checkbetalinger.

Hvis funktionen Massetilbageførsel er aktiveret, kan et eller flere kreditorposteringer også tilbageføres fra siden **Posteringer på bilag** og fra den kladde, som posteringerne blev bogført fra. Kreditorbetalinger kan dog stadig kun tilbageføres fra bankkontoen. Derudover kan kreditorposteringer ikke tilbageføres fra siden **Posteringer for \<main account\>** til finans. De kan kun tilbageføres fra siden **Posteringer på bilag**.

Bemærk, at visse posteringer slet ikke kan tilbageføres. Eksempler på dette er kreditorfakturaer for indkøbsordrer og elektroniske kreditorbetalinger.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Årsager til, at bilag ikke kan tilbageføres

Bilag kan ikke tilbageføres af følgende årsager:

- Regnskabsperioden er på hold eller lukket:

    - Hvis tilbageførselsdatoen ligger i en regnskabsperiode, der ikke er åben, kan posteringen ikke tilbageføres.
    - Hvis posteringen understøtter indtastning af en tilbageførselsdato, kan posteringen stadig tilbageføres ved at ændre tilbageførselsdatoen til en åben periode.

- Finansprocessen til årsafslutning er kørt:

    - Regnskabsdatoen for posteringen ligger i et regnskabsår, der er lukket i Finans. Selvom en periode i regnskabsåret stadig er åben, kan posteringen ikke tilbageføres, hvis der er kørt årsafslutningsproces for regnskabsåret. Regnskabsåret har en anden status end perioderne i det.
    - Årsafslutningen kan tilbageføres, og derefter kan posteringen tilbageføres. Denne metode er måske ikke en mulighed. Det kan være lettere at angive en tilbageførselspostering manuelt i en åben periode for enten det lukkede regnskabsår eller det næste regnskabsår, afhængigt af statussen for processen til regnskabsafslutning. Hvis en ny postering bogføres i en åben periode i regnskabsåret, som har været gennem årsafslutningsprocessen, skal årsafslutningen køres igen.

- Kladdeposteringen for reskontro er ikke overført til finans:

    - Denne årsag gælder kun for kreditorfakturaer, der ikke er indkøbsordrer.
    - Brug siden **Kladdeposteringer for reskontro, der endnu ikke er overført**, til at overføre posten til finans. Kreditorfakturaen, der ikke er en indkøbsordre, kan derefter tilbageføres fra siden **Kreditorposteringer**.

- Udligning:

    - Posteringen (f.eks. en faktura eller betaling) udlignes eller markeres til udligning.

        - Du kan kontrollere, om en postering er udlignet eller markeret til udligning, ved at vælge **Vis udligninger** eller **Udligning \> Udligningshistorik** på siden **Kreditorposteringer**.
        - Du kan også tilbageføre en udligning fra siden **Kreditorposteringer** (**Udligning \> Fortryd udligning**), hvis en af posteringerne skal tilbageføres.

- Bilaget indeholder mere end én postering for for reskontroen, der er angivet med samme bilagsnummer (én bilagsudstedelse).
- Fakturaen er ikke godkendt:

    - Hvis afkrydsningsfeltet **Godkendelse** ikke er markeret på fakturaen, kan fakturaen ikke tilbageføres.

        - I dette tilfælde refererer godkendelse ikke til godkendelser i arbejdsprocessen, men til indstillingen **Godkendelse** på fakturaen. Denne indstilling bruges til at forhindre, at der betales en faktura. Den bruges typisk til kreditorfakturaer i indgangsbogen.

- Posteringen er i fakturapuljen:

    - En faktura i puljen kan ikke tilbageføres direkte fra siden **Kreditorposteringer**. Den skal i stedet tilbageføres via annulleringsprocessen på siden **Fakturagodkendelseskladde**.

- Transaktionen har en overordnet faktura, der er rettet (indisk lokalisering).
- Transaktionen har statussen **Faktura remitteret** for egenveksel.
- Posteringen bruges til en delvis momsafregning.
- Posteringen indeholder en kreditorkonto, men den tilbageføres fra en forkert side, f.eks. siden **Posteringer for \<main account\>**:

    - Som denne årsag antyder, kan visse posteringer for reskontro kun tilbageføres fra bestemte sider, selvom funktionen Massetilbageførsel er aktiveret.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Posteringstyper, der ikke kan tilbageføres

Følgende typer posteringer kan ikke tilbageføres:

- Kursregulering:

    - I modsætning til kursregulering af udenlandsk valuta i finansmodulet kan debitor- og kreditorkursregulering af udenlandsk valuta ikke tilbageføres. Kursreguleringen skal i stedet køres igen ved hjælp af fakturadatoen. I dette tilfælde bruger værdireguleringen valutakursen fra fakturaens dato og bringer reelt den ikke-realiserede gevinst eller tabet til 0 (nul). Resultatet minder derfor om resultatet af tilbageførsel af den tidligere værdiregulering. Bemærk dog, at samme beløb ikke vil blive tilbageført, hvis standardvalutakursen er ændret på fakturaen.

- Kreditorfaktura for indkøbsordre:

    - Der skal oprettes en kreditnota, for at du kan tilbageføre kreditorfakturaen. Du kan finde flere oplysninger om, hvordan du opretter en tilbageførselspostering, under [Oprette en købsreturordre](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Egenveksel
- Eksportforsendelse af bankremburs

## <a name="accounts-receivable"></a>Debitor

Flere posteringstyper opdaterer debitorreskontroer. Eksempler omfatter debitorfakturaer fra salgsordrer, debitorfakturaer, der er indtastet via finanskladden, fritekstfakturaer, debitorbetalinger og afskrivninger.

Hvis funktionen Massetilbageførsel er deaktiveret, kan posteringer tilbageføres individuelt fra siden **Debitorposteringer** for fakturaer eller siden **Bankkonti** til indbetalinger. Du kan finde oplysninger om, hvordan du tilbagefører en betaling, i sektionen [Kontant- og bankstyring](cant-reverse-transctns.md#cash-and-bank-management) senere i denne artikel.

Hvis funktionen Massetilbageførsel er aktiveret, kan et eller flere debitorposteringer også tilbageføres fra siden **Posteringer på bilag** og fra den kladde, som de blev bogført fra. Men indbetalinger kan stadig kun tilbageføres fra bankkontoen, og fritekstfakturaer kan kun tilbageføres fra den oprindelige side (hvis funktionen, der tillader rettelser, er aktiveret). Derudover kan debitorposteringer stadig ikke tilbageføres fra siden **Posteringer for \<main account\>** til finans. De kan dog tilbageføres fra siden **Posteringer på bilag**.

Bemærk, at visse posteringer ikke kan tilbageføres. Det kan f.eks. være debitorfakturaer og afskrivninger for salgsordrer.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsager til, at posteringer ikke kan tilbageføres

Posteringer kan ikke tilbageføres af følgende årsager:

- Regnskabsperioden er på hold eller lukket permanent:

    - Hvis tilbageførselsdatoen ligger i en regnskabsperiode, der ikke er åben, kan posteringen ikke tilbageføres.
    - Hvis posteringen understøtter indtastning af en tilbageførselsdato, kan posteringen stadig tilbageføres ved at ændre tilbageførselsdatoen til en åben periode.

- Finansprocessen til årsafslutning er kørt:

    - Regnskabsdatoen for posteringen ligger i et regnskabsår, hvor der er kørt en årsafslutning i finans. Selvom en periode i regnskabsåret stadig er åben, kan posteringen ikke tilbageføres, hvis der er kørt årsafslutningsproces for regnskabsåret. Regnskabsåret har en anden status end perioderne i det.
    - Årsafslutningen kan tilbageføres, og derefter kan posteringen tilbageføres. Denne metode er måske ikke en mulighed. Det kan være lettere at angive en tilbageførselspostering manuelt i en åben periode for enten det lukkede regnskabsår eller det næste regnskabsår, afhængigt af statussen for processen til regnskabsafslutning. Hvis en ny postering bogføres i en åben periode i regnskabsåret, som har været gennem årsafslutningsprocessen, skal årsafslutningen køres igen.

- Kladdeposteringen for reskontro er ikke overført til finans:

    - Denne årsag gælder kun for fritekstfakturaer.
    - Brug siden **Kladdeposteringer for reskontro, der endnu ikke er overført**, til at overføre posten til finans. Fritekstfakturaen kan derefter tilbageføres eller rettes, hvis funktionen til rettelse er aktiveret.

- Udligning:

    - Posteringen (f.eks. en faktura eller betaling) udlignes eller markeres til udligning.

        - Du kan kontrollere, om en postering er udlignet eller markeret til udligning, ved at vælge **Vis udligninger** eller **Udligning \> Udligningshistorik** på siden **Debitorposteringer**.
        - Du kan også tilbageføre en udligning fra siden **Debitorposteringer** (**Udligning \> Fortryd udligning**), hvis en af posteringerne skal tilbageføres.

- Posteringen indeholder mere end én postering for reskontroen, der er angivet med samme bilagsnummer (én bilagsudstedelse).
- Fakturaen er ikke godkendt:

    - Hvis afkrydsningsfeltet **Godkendelse** ikke er markeret på fakturaen, kan fakturaen ikke tilbageføres.

        - I dette tilfælde refererer godkendelse ikke til godkendelser i arbejdsprocessen, men til indstillingen **Godkendelse** på bilagslinjerne. Denne indstilling bruges til at forhindre, at der betales en faktura. Selvom denne indstilling typisk bruges i Kreditor, er den også tilgængelig for debitorfakturaer, der indtastes via kladder.

- Transaktionen har en overordnet faktura, der er rettet (indisk lokalisering).
- Posteringen indeholder en debitorkonto, men den tilbageføres fra en forkert side, f.eks. siden **Posteringer for \<main account\>**:

    - Som denne årsag antyder, kan visse posteringer for reskontro kun tilbageføres fra bestemte sider, selvom funktionen Massetilbageførsel er aktiveret.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Posteringstyper, der ikke kan tilbageføres

Følgende typer posteringer kan ikke tilbageføres:

- Kursregulering:

    - I modsætning til kursregulering af udenlandsk valuta i finansmodulet kan debitor- og kreditorkursregulering af udenlandsk valuta ikke tilbageføres. Kursreguleringen skal i stedet køres igen ved hjælp af fakturadatoen. I dette tilfælde bruger værdireguleringen valutakursen fra fakturaens dato og bringer reelt den ikke-realiserede gevinst eller tabet til 0 (nul). Resultatet minder derfor om resultatet af tilbageførsel af den tidligere værdiregulering. Bemærk dog, at samme beløb ikke vil blive tilbageført, hvis standardvalutakursen er ændret på fakturaen.

- En postering, der har reguleret A-skat
- Debitorfaktura for salgsordre:

    - Der skal oprettes en kreditnota eller returnering, for at du kan tilbageføre posteringen. Du kan finde oplysninger om, hvordan du opretter tilbageførselsposteringen, under [Salgsreturneringer](../../supply-chain/warehousing/sales-returns.md).

- Veksel
- Kasseapparatpostering
- Avanceret regulering
- Rentenota
- Rykker
- Bankemburs
- Eksportforsendelse
- Indtægtsføringskladde:

    - Når fører indtægter via indtægtsføringskladden, bogføres bilag på finanskonti. Derfor ser det ud, som om de kun er finansposter. Disse poster kan ikke tilbageføres, da indtægtstidsplanen ikke genåbnes for at bogføre indtægten igen.

## <a name="cash-and-bank-management"></a>Kontant- og bankstyring

Flere posteringstyper opdaterer bankreskontroen via finanskladden. Det kan f.eks. være kreditorbetalinger, debitorbetalinger og bankoverførsler.

Hvis funktionen Massetilbageførsel er deaktiveret, kan posteringer tilbageføres individuelt fra siden **Bankkonti** for checks og indbetalinger eller fra siden **Debitorposteringer** til debitorbetalinger.

Hvis funktionen Massetilbageførsel er aktiveret, kan et eller flere betalingsposteringer også tilbageføres fra siden **Posteringer på bilag** og fra den kladde, som posteringerne blev bogført fra. Indbetalinger kan dog stadig kun tilbageføres fra bankkontoen. Derudover kan bankposteringer stadig ikke tilbageføres fra finanssiden **Posteringer for \<main account\>**. De kan dog tilbageføres fra siden **Posteringer på bilag**.

Bemærk, at visse posteringer ikke kan tilbageføres. Det kan f.eks. være elektroniske kreditorbetalinger.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsager til, at posteringer ikke kan tilbageføres

Posteringer kan ikke tilbageføres af følgende årsager:

- Regnskabsperioden er på hold eller lukket permanent:

    - Hvis tilbageførselsdatoen ligger i en regnskabsperiode, der ikke er åben, kan posteringen ikke tilbageføres.
    - Hvis posteringen understøtter indtastning af en tilbageførselsdato, kan posteringen stadig tilbageføres ved at ændre tilbageførselsdatoen til en åben periode.

- Finansprocessen til årsafslutning er kørt:

    - Regnskabsdatoen for posteringen ligger i et regnskabsår, hvor der er kørt en årsafslutning i finans. Selvom en periode i regnskabsåret stadig er åben, kan posteringen ikke tilbageføres, hvis der er kørt årsafslutningsproces for regnskabsåret. Regnskabsåret har en anden status end perioderne i det.
    - Årsafslutningen kan tilbageføres, og derefter kan posteringen tilbageføres. Denne metode er måske ikke en mulighed. Det kan være lettere at angive en tilbageførselspostering manuelt i en åben periode for enten det lukkede regnskabsår eller det næste regnskabsår, afhængigt af statussen for processen til regnskabsafslutning. Hvis en ny postering bogføres i en åben periode i regnskabsåret, som har været gennem årsafslutningsprocessen, skal årsafslutningen køres igen.

- Udligning:

    - Posteringen (betaling) udlignes eller markeres til udligning.

        - Du kan kontrollere, om en postering er udlignet eller markeret til udligning, ved at vælge **Vis udligninger** eller **Udligning \> Udligningshistorik** på siden **Kreditorposteringer** eller **Debitorposteringer**.
        - Du kan også tilbageføre en udligning fra siden **Kreditorposteringer** eller **Debitorposteringer** (**Udligning \> Fortryd udligning**), hvis en af posteringerne skal tilbageføres.

- Posteringen indeholder mere end én postering for reskontroen, der er angivet med samme bilagsnummer (én bilagsudstedelse).
- Mellemposteringer:

    - Hvis posteringen er relateret til en mellembetaling, kan den ikke tilbageføres.
    - Hvis mellembetalingen skal tilbageføres, skal betalingen først cleares fra mellemkontoen til banken. Betalingen kan derefter tilbageføres, hvis den opfylder de andre valideringskriterier.

- Posteringen indeholder en bankkonto, men den tilbageføres fra siden **Posteringer for \<main account\>** eller fra en forkert reskontro, f.eks. Debitor eller Kreditor:

    - Som denne årsag antyder, kan visse posteringer for reskontro kun tilbageføres fra bestemte sider, selvom funktionen Massetilbageførsel er aktiveret.

- Bank – værdiregulering af udenlandsk valuta:

    - Værdiregulering af udenlandsk valuta i banken kan tilbageføres. Tilbageførsel kan dog forhindres, hvis du fuldfører tilbageførselstrinnene uden for kronologisk rækkefølge. Hvis du f.eks. har kørt værdireguleringen i marts og april, kan værdireguleringen for marts ikke tilbageføres, før værdireguleringen for april tilbageføres.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Posteringstyper, der ikke kan tilbageføres

Følgende typer posteringer kan ikke tilbageføres:

- Kreditorbetalinger, der blev foretaget som elektroniske pengeoverførsler
- Egenveksler
- Veksler

## <a name="fixed-assets"></a>Anlægsaktiver

Flere posteringstyper opdaterer anlægsaktivers reskontro. Eksempler på dette er anskaffelser og afskrivninger.

Hvis funktionen til massetilbageførsel er deaktiveret, kan posteringer tilbageføres individuelt fra siden **Kreditorposteringer**, fra siden **Anlægsaktivposter** eller fra leasing af anlægsaktiver, afhængigt af posteringstypen.

Hvis funktionen Massetilbageførsel er aktiveret, kan et eller flere anlægsaktivsposter også tilbageføres fra siden **Posteringer på bilag** i den kladde, som posteringerne blev bogført fra.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsager til, at posteringer ikke kan tilbageføres

Posteringer kan ikke tilbageføres af følgende årsager:

- Regnskabsperioden er på hold eller lukket permanent:

    - Hvis tilbageførselsdatoen ligger i en regnskabsperiode, der ikke er åben, kan posteringen ikke tilbageføres.
    - Hvis posteringen understøtter indtastning af en tilbageførselsdato, kan posteringen stadig tilbageføres ved at ændre tilbageførselsdatoen til en åben periode.

- Finansprocessen til årsafslutning er kørt:

    - Regnskabsdatoen for posteringen ligger i et regnskabsår, der er lukket i Finans. Selvom en periode i regnskabsåret stadig er åben, kan posteringen ikke tilbageføres, hvis der er kørt årsafslutningsproces for regnskabsåret. Regnskabsåret har en anden status end perioderne i det.
    - Årsafslutningen kan tilbageføres, og derefter kan posteringen tilbageføres. Denne metode er måske ikke en mulighed. Det kan være lettere at angive en tilbageførselspostering manuelt i en åben periode for enten det lukkede regnskabsår eller det næste regnskabsår, afhængigt af statussen for processen til regnskabsafslutning. Hvis en ny postering bogføres i en åben periode i regnskabsåret, som har været gennem årsafslutningsprocessen, skal årsafslutningen køres igen.

- Anskaffelser:

    - Hvis anskaffelsen er sket på en kreditorfaktura for indkøbsordre, skal tilbageførslen ske ved at angive en kreditorkreditnota. Du kan finde oplysninger om, hvordan indtaster tilbageførselsposteringen, under [Oprette en købsreturordre](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Anskaffelsen fandt sted i forbindelse med en projektpostering.
    - Anskaffelsen kan ikke tilbageføres, når afskrivningen er bogført for aktivet. Afskrivningen skal tilbageføres, før anskaffelsen kan tilbageføres.
    - Hvis status for værdimodellen eller afskrivningsmodellen for et anlægsaktiv ikke er åben, kan posteringen ikke tilbageføres.

- Kassation:

    - Kassationen sker via en fritekstfaktura:

        - Korrektionen af en fritekstfaktura blokeres, hvis den indeholder et anlægsaktiv. Men hvis aktivet kasseres via en kladde, kan fritekstfakturaen tilbageføres fra anlægsaktivposten.

    - Hvis status for værdimodellen eller afskrivningsmodellen for et anlægsaktiv ikke er åben, kan posteringen ikke tilbageføres.

- Afskrivning:

    - Afskrivningen **kan** tilbageføres, hvis den efterfølgende afskrivning også bogføres. Der vil dog blive vist en advarsel, da denne metode ikke er den bedste fremgangsmåde.
    - Hvis status for værdimodellen eller afskrivningsmodellen for et anlægsaktiv ikke er åben, kan posteringen ikke tilbageføres.

- Der findes posteringer (eller tilbageførte posteringer) for et bestemt aktiv og anlægsaktivkartotek for bilagets posteringsdato eller senere.
- Posteringen indeholder en aktivkonto, men den tilbageføres fra siden **Posteringer for \<main account\>** eller fra en forkert reskontro, f.eks. Debitor eller Kreditor:

    - Som denne årsag antyder, kan visse posteringer for reskontro kun tilbageføres fra bestemte sider, selvom funktionen Massetilbageførsel er aktiveret.
    - Hvis en anskaffelse finder sted i en kreditorfaktura, der ikke er for en indkøbsordre, eller en kreditorfakturakladde, kan den kun tilbageføres fra siden **Kreditorposteringer** i Kreditor.
    - Hvis et aktiv anskaffes fra Aktivleasing, kan det tilbageføres fra siden **Forpligtelsestransaktioner** i Aktivleasing.
