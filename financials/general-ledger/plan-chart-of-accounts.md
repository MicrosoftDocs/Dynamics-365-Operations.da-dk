---
title: "Planlæg din kontoplan"
description: "Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 424ea5ce12d51d384c86878b7d2199bcd52c40f8
ms.contentlocale: da-dk
ms.lasthandoff: 08/01/2017

---

# <a name="plan-your-chart-of-accounts"></a>Planlæg din kontoplan

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.

Du kan oprette en kontoplan, når du vil registrere og vedligeholde økonomiske oplysninger. En kontoplan er en samling konti, der definerer en økonomisk ramme. Hvis du derudover vil spore transaktionerne på disse konti, kan du tilføje segmenter, kaldet økonomiske dimensioner. En udgiftskonto kan f.eks. indeholde økonomiske dimensioner med navnene Afdeling, Bærer og Formål. Brugerdefinerede regler, kaldet kontostrukturer og avancerede regler, bestemmer, hvordan disse økonomiske dimensioner er knyttet til hovedkontiene og andre økonomiske dimensioner, og også hvordan disse transaktioner er angivet. 

Kontoplanen er en struktureret oversigt over en juridisk enheds finanskonti. Oversigten bruges til at udarbejde økonomiske rapporter til myndigheder og til ejerne. Kontiene er grupperet efter kontotype og derefter yderligere opsummeret i større kategorier. På det mest generelle niveau er kontiene grupperet som indtægter og udgifter (driftskonti) og aktiver og passiver (statuskonti). 

En kontoplan kan deles og bruges af alle de juridiske enheder i en organisation. Kontoplanen, der bruges af en juridisk enhed, defineres på siden **Finans**. 

Her er nogle af de faktorer, du bør overveje, når du planlægger strukturen af kontoplanen for din organisation:

-   Hvilke rapporteringskrav der gælder i det land eller den region, hvor organisationen er hjemmehørende
-   Hvilke rapporteringskrav der gælder for den juridiske enhed
-   Detaljeringsgraden, som kræves, både for eksterne organisationer og for din organisation

Opret kontoplanen på siden **Kontoplan**. Hovedkonti kan oprettes fra siden **Kontoplan** eller siden **Hovedkonti**. Dine hovedkonti bør ikke bruge specialtegn, der bruges som afgrænsningstegn i kontoplaner. Hvis du har et specialtegn, der er det samme som afgrænsningstegnet i din kontoplan, kan du opleve ustabilitet, eller der kan opstå behov for hele tiden at skulle bruge opslag eller pop op-vinduet, når du angiver kombinationer af konto og dimension. Du kan finde flere oplysninger i [Oprette en hovedkonto](tasks/create-account-structures.md).


Det er en god ide at knytte hovedkontiene til hovedkontokategorier, så du kan drage fordel af økonomiske standardrapporter uden at skulle foretage ændringer. Derfor kan du hurtigere og nemmere designe og vedligeholde rapporter. 

Brug siden **Konfigurer kontostrukturer** til at oprette kontostrukturer. Kontostrukturer definerer gyldige kombinationer. Kombinationerne udgør, sammen med hovedkontiene, en kontoplan.  Du kan finde flere oplysninger under [Oprette kontostrukturer](tasks/create-main-account.md).

**Tilsidesættelser af juridisk enhed** 

Ikke alle hovedkonti er gyldige for alle juridiske enheder, og nogle er muligvis kun relevante for en bestemt tidsperiode. I dette scenarie kan sektionen Tilsidesættelser af juridisk enhed bruges til at identificere, hvilke regnskaber hovedkontoen bør suspenderes for, hvem der er ejer, og hvor lang tid dimensionen er aktiv. Tilsidesættelser på det delte niveau må ikke være mere restriktive end tilsidesættelser på niveauet for den juridiske enhed.

Yderligere oplysninger finder du i følgende emner: [Økonomiske dimensioner](financial-dimensions.md)
[Opret og tildel avancerede regelstrukturer](tasks/create-assign-advanced-rule-structures.md)




