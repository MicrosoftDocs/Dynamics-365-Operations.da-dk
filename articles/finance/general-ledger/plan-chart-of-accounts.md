---
title: Planlægge din kontoplan
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8650b24ac8e1c7feab2a9e5c4c4f98f7f573f340
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815518"
---
# <a name="plan-your-chart-of-accounts"></a>Planlægge din kontoplan

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen for organisationen.

Du kan oprette en kontoplan, når du vil registrere og vedligeholde økonomiske oplysninger. En kontoplan er en samling konti, der definerer en økonomisk ramme. For at spore transaktionerne på disse konti yderligere, kan du tilføje segmenter. Disse segmenter kaldes økonomiske dimensioner. En udgiftskonto kan f.eks. indeholde økonomiske dimensioner med navnene Afdeling, Bærer og Formål. Brugerdefinerede regler bestemmer, hvordan økonomiske dimensioner knyttes til hovedkontiene og andre økonomiske dimensioner, samt hvordan disse transaktioner angives. Disse brugerdefinerede regler er kendt som kontostrukturer og avancerede regler.

Kontoplanen er en struktureret oversigt over en juridisk enheds finanskonti. Oversigten bruges til at udarbejde økonomiske rapporter til myndigheder og til ejerne. Kontiene grupperes først efter kontotype og samles derefter yderligere i større kategorier. På det mest generelle niveau er kontiene grupperet som indtægter og udgifter (driftskonti) og aktiver og passiver (statuskonti).

En kontoplan kan deles og bruges af alle de juridiske enheder i en organisation. Kontoplanen, der bruges af en juridisk enhed, defineres på siden **Finans**.

Her er nogle af de faktorer, du bør overveje, når du planlægger strukturen af kontoplanen for din organisation:

- De rapporteringskrav, der gælder i det land eller område, hvor organisationen er hjemmehørende
- Hvilke rapporteringskrav der gælder for den juridiske enhed
- Detaljeringsgraden, som kræves, både for eksterne organisationer og for din organisation

Du kan oprette kontoplanen på siden **Kontoplan**. Du kan oprette hovedkonti fra siden **Kontoplan** eller **Hovedkonti**. Dine hovedkonti bør ikke omfatte specialtegn, der bruges som afgrænsningstegn i kontoplaner. Ellers kan funktionerne være ustabile, eller du er nødt til at bruge opslag eller dialogboksen, når du angiver kombinationer af konti og dimensioner. Du kan finde flere oplysninger i [Oprette en hovedkonto](tasks/create-main-account.md).

> [!NOTE]
> I Dynamics 365 for Finance and Operations version 8.0 (april 2018) kan du redigere afgrænsningstegnet for kontoplanen fra siden **Finansparametre**.

Det er en god ide at knytte hovedkontiene til hovedkontokategorier, så du kan drage fordel af økonomiske standardrapporter uden at skulle foretage ændringer. Derfor kan du hurtigere og nemmere designe og vedligeholde rapporter.

Du kan oprette kontostrukturer på siden **Konfigurer kontostrukturer**. Kontostrukturer definerer gyldige kombinationer. Disse kombinationer udgør sammen med hovedkontiene en kontoplan. Du kan finde flere oplysninger under [Oprette kontostrukturer](tasks/create-account-structures.md).

**Tilsidesættelser af juridisk enhed**

Ikke alle hovedkonti er gyldige for alle juridiske enheder, og nogle hovedkonti er muligvis kun relevante for en bestemt periode. I dette scenarie kan du bruge sektionen **Tilsidesættelser af juridisk enhed** for at identificere, hvilke firmaer hovedkontoen tilsidesættes for, ejeren, og den periode, hvor dimensionen er aktiv. Tilsidesættelser på det delte niveau må ikke være mere restriktive end tilsidesættelser på niveauet for den juridiske enhed.

Du kan finde flere oplysninger under følgende emner:

- [Økonomiske dimensioner](financial-dimensions.md)
- [Oprette og tildele avancerede regelstrukturer](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]