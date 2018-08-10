---
title: "Økonomiske dimensioner"
description: "I dette emne beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Økonomiske dimensioner

[!include [banner](../includes/banner.md)]

I dette emne beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet.

Du kan bruge siden **Økonomiske dimensioner** til at oprette økonomiske dimensioner, som du kan bruge som kontosegmenter i kontoplaner. Der er to typer økonomiske dimensioner: brugerdefinerede dimensioner og enhedsunderstøttede dimensioner. Brugerdefinerede dimensioner deles på tværs af juridiske enheder, og værdierne angives og vedligeholdes af brugerne. For enhedsunderstøttede dimensioner defineres værdierne andre steder i systemet, f.eks. som enheden Debitorer eller Butikker. Nogle enhedsunderstøttede dimensioner deles på tværs af juridiske enheder, mens andre enhedsunderstøttede dimensioner er firmaspecifikke. 

Når du har oprettet de økonomiske dimensioner, skal du bruge siden **Økonomiske dimensionsværdier** til at tildele hver økonomisk dimension yderligere egenskaber. 

Du kan bruge økonomiske dimensioner til at repræsentere juridiske enheder. Du behøver ikke at oprette de juridiske enheder i Microsoft Dynamics 365 for Finance and Operations. Økonomiske dimensioner kan dog ikke til opfylde juridiske enheders handlings- eller forretningsmæssige behov. Funktionen for regnskab mellem enheder i Finance and Operations er kun udviklet i forbindelse med de regnskabsposter, der oprettes ved hver transaktion. 

Før du kan konfigurere økonomiske dimensioner som juridiske enheder, skal du evaluere forretningsprocesserne på følgende områder for at afgøre, om denne installation vil fungere for organisationen:

- Lagerbeholdning
- Salg og køb mellem økonomiske dimensioner og juridiske enheder
- Beregning og rapportering af salgsmoms
- Driftsrapportering

Her er nogle begrænsninger:

- Du kan kun bruge salgsmomsfunktioner til juridiske enheder, ikke til økonomiske dimensioner.
- Nogle rapporter medtager ikke økonomiske dimensioner. Hvis du vil rapportere pr. økonomisk dimension, kan det derfor være nødvendigt at redigere rapporterne.

## <a name="custom-dimensions"></a>Brugerdefinerede dimensioner

For at oprette en brugerdefineret økonomisk dimension skal du vælge **&lt; Brugerdefineret dimension &gt;** i feltet **Brug værdier fra**. Du kan også angive en kontomaske for at begrænse mængden og typen af oplysninger, som du kan du angive for dimensionsværdier. Du kan skrive tegn, der forbliver ens for hver dimensionsværdi, f.eks. bogstaver eller en bindestreg (-). Du kan også angive nummertegn (\#) og &-tegn (&) som pladsholdere for bogstaver og tal, som ændres, hver gang der oprettes en dimensionsværdi. Brug et nummertegn (\#) som pladsholder for et tal, og tegnet (&) som pladsholder for et bogstav. Feltet til formatmasken er kun tilgængeligt, hvis du har valgt **&lt; Brugerdefineret dimension &gt;** i feltet **Brug værdier fra**.

**Eksempel**

Hvis du vil begrænse dimensionsværdien til bogstaverne "CC", en bindestreg og tre tal, skal du angive **CC-\#\#\#** som formatmaske.

## <a name="entity-backed-dimensions"></a>Enhedsunderstøttede dimensioner

For at oprette en enhedsunderstøttet økonomisk dimension skal du i feltet **Brug værdier fra** vælge en systemdefineret enhed, den økonomiske dimension skal baseres på. Der oprettes derefter økonomiske dimensionsværdier ud fra denne enhed. Hvis du f.eks. vil oprette dimensionsværdier for projekter, skal du vælge **Projekter**. Der oprettes derefter en dimensionsværdi for hvert projektnavn. Siden **Økonomiske dimensionsværdier** viser værdierne for enheden. Hvis disse værdier er firmaspecifikke, viser siden også firmaet.

## <a name="activating-dimensions"></a>Aktivering af dimensioner

Når du aktiverer en økonomisk dimension, opdateres tabellen, så den omfatter navnet på den økonomiske dimension. Slettede dimensioner fjernes. Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension. Men en økonomisk dimension ikke forbruges overalt, før den aktiveres. Du kan f.eks. ikke føje en økonomiske dimension til kontostruktur, før den økonomiske dimension er blevet aktiveret. Når du klikker på **Aktivér**, opdateres alle dimensioner og viser statusændringer. 

## <a name="translations"></a>Oversættelser

På siden **Oversættelse af tekst** kan du skrive tekst til den valgte økonomiske dimension på forskellige sprog. På siden **Oversættelse af hovedkonto** kan du skrive tekst til den hovedkontoen på forskellige sprog. 

## <a name="legal-entity-overrides"></a>Tilsidesættelser af juridisk enhed

Ikke alle dimensioner gælder for alle juridiske enheder. Desuden kan nogle dimensioner være relevante for kun en bestemt periode. I disse tilfælde kan du bruge sektionen **Tilsidesættelser af juridisk enhed** til at angive de firmaer, dimensionen bør suspenderes for, ejeren, og den periode, hvor dimensionen er aktiv.

## <a name="deleting-financial-dimensions"></a>Slette økonomiske dimensioner

Af hensyn til vedligeholdelsen af dataenes referenceintegritet kan økonomiske dimensioner sjældent slettes. Hvis du forsøger at slette en økonomisk dimension, evalueres følgende kriterier:

- Er den økonomiske dimension blevet anvendt på bogførte eller ikke-bogførte posteringer eller nogen form for kombination af dimensionsværdier?
- Bruges den økonomiske dimension i en aktiv kontostruktur, en avanceret regelstruktur eller et sæt økonomiske dimensioner?
- Er den økonomiske dimension en del af et standardintegrationsformat for økonomiske dimensioner?
- Er den økonomiske dimension konfigureret som en standarddimension?

Hvis et af kriterierne er opfyldt, kan du ikke slette den økonomiske dimension.


Du kan finde flere oplysninger under følgende emner:
- [Definere økonomiske dimensioner](tasks/define-financial-dimensions.md)
- [Vedligeholde standardskabeloner for økonomiske dimensioner](tasks/maintain-financial-dimension-default-templates.md)

