---
title: "Økonomiske dimensioner"
description: "I denne artikel beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Økonomiske dimensioner

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet.

Du kan bruge siden Økonomiske dimensioner til at oprette økonomiske dimensioner, som du kan bruge som kontosegmenter i kontoplaner. Der er to typer økonomiske dimensioner, brugerdefinerede dimensioner og enhedsunderstøttede dimensioner. Brugerdefinerede dimensioner deles på tværs af juridiske enheder, og værdierne angives og administreres af brugeren. Enhedsunderstøttede dimensioner er dimensioner, hvis værdier er defineret andre steder i systemet, f.eks. debitorer eller butikker. Nogle enhedsunderstøttede dimensioner deles på tværs af juridiske enheder, og nogle enhedsunderstøttede dimensioner er firmaspecifikke. 

Når du har oprettet de økonomiske dimensioner, skal du bruge siden Økonomiske dimensionsværdier til at tildele hver økonomisk dimension yderligere egenskaber. 

Selvom du kan bruge økonomiske dimensioner til at repræsentere juridiske enheder uden at oprette de juridiske enheder i Microsoft Dynamics 365 for Operations, er økonomiske dimensioner ikke designet til at opfylde de driftsmæssige eller virksomhedsmæssige behov for de juridiske enheder. Funktionen for regnskab mellem enheder i Microsoft Dynamics 365 for Operations er kun udviklet i forbindelse med de regnskabsposter, der oprettes ved hver transaktion. 

Før du kan konfigurere økonomiske dimensioner som juridiske enheder, skal du evaluere forretningsprocesserne på følgende områder for at afgøre, om denne installation vil fungere for organisationen:

-   Lager
-   Salg og køb mellem økonomiske dimensioner og juridiske enheder
-   Beregning og rapportering af salgsmoms
-   Driftsrapportering

Nogle eksempler på begrænsningerne er følgende:

-   Du kan kun bruge salgsmomsfunktioner til juridiske enheder, ikke til økonomiske dimensioner.
-   Nogle rapporter indeholder ikke økonomiske dimensioner, så du kan ikke altid rapportere med den økonomiske dimension, medmindre disse rapporter er ændret.

**Brugerdefinerede dimensioner** 

For at oprette en brugerdefineret økonomisk dimension skal du i feltet Brug værdier fra vælge &lt; Brugerdefineret dimension &gt;. Du kan også angive en kontomaske for at begrænse mængden og typen af oplysninger, som du kan du angive for dimensionsværdier. Du kan skrive tegn, der forbliver ens for hver dimensionsværdi, f.eks. bogstaver eller en bindestreg. Du kan også angive nummertegn (\#) og &-tegn (&) som pladsholdere for bogstaver og tal, som ændres, hver gang der oprettes en dimensionsværdi. Brug et nummertegn (\#) som pladsholder for et tal, og tegnet (&) som pladsholder for et bogstav. 

**Eksempel** 

Hvis du vil begrænse dimensionsværdien til bogstaverne CC, en bindestreg og tre tal, skal du angive CC-\#\#\# som formatmaske. Dette felt er kun tilgængeligt, hvis du har valgt &lt; Brugerdefineret dimension &gt; i feltet Brug værdier fra. 

**Enhedsunderstøttede dimensioner** 

For at oprette en enhedsunderstøttet økonomisk dimension skal du i feltet Brug værdier fra vælge en systemdefineret enhed, den økonomiske dimension skal baseres på. Økonomiske dimensionsværdier oprettes ud fra dette valg. Hvis du f.eks. vil oprette dimensionsværdier for projekter, skal du vælge Projekter. Der oprettes en dimensionsværdi for hver projektnavn. Siden for dimensionsværdier viser værdierne for enheden, og hvis de er firmaspecifikke, firmaet for værdien. 

**Aktivering af dimensioner** 

Aktivering af den økonomiske dimension opdaterer tabellen med navnet på den økonomiske dimension og fjerner slettede dimensioner. Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension, men en økonomisk dimension kan ikke forbruges nogen steder, før den aktiveres. Du kan f.eks. ikke føje en økonomiske dimension til kontostruktur, før den økonomiske dimension er blevet aktiveret. Hvis du klikker på Aktiver opdateres alle dimensioner med statusændringer. 

**Oversættelser** 

Siden Oversættelse af tekst giver dig mulighed for at indtaste tekst til visning på forskellige sprog for den valgte økonomiske dimension. Siden Oversættelse af hovedkonto er, hvor du kan indtaste tekst til visning på forskellige sprog for hovedkontoen. 

**Tilsidesættelser af juridisk enhed** 

Ikke alle dimensioner er gyldige for alle juridiske enheder, og nogle er muligvis kun relevante for en bestemt tidsperiode. I dette scenarie kan sektionen Tilsidesættelser af juridisk enhed bruges til at identificere, hvilke firmaer dimensionen bør suspenderes for, hvem der er ejer, og hvor lang tid dimensionen er aktiv.






