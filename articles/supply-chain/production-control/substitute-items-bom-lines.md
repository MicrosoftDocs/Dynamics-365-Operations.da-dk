---
title: Materialeerstatning i produktion
description: Dette emne beskriver, hvordan du erstatter materialer i produktionsprocessen.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 461b717acafb5ccf37acae23a1564069cea6828a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327613"
---
# <a name="material-substitution-in-manufacturing"></a>Materialeerstatning i produktion

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du erstatter materialer i produktionsprocessen. 

Der findes tre metoder til erstatning af materialer i produktionsprocessen:

-   Efter dato, når et materiale erstattes med et andet efter en bestemt dato
-   Under varedisponering, når et materiale i er en formel erstattes med et andet materiale, fordi det er udsolgt
-   Under produktionen, når et materiale uventet er udsolgt og erstattes med et andet materiale

## <a name="substituting-material-by-date"></a>Erstatning af materiale efter dato
Overvej følgende scenario: En maskine, som en virksomhed producerer, indeholder en komponent, der udgår af leverandørens katalog inden for to måneder. Fra udløbsdatoen og fremad tilbyder leverandøren en ny komponent, der kan erstatte den gamle komponent. Der kan konfigureres fra og til-gyldighedsdatoer på styklistelinjer. I dette eksempel angiver du, at den gamle komponent skal udløbe, ved at angive udløbsdatoen i feltet **Til-dato**. Derefter skal du på styklisten oprette den nye erstatningskomponent, så det er gyldigt fra dagen, efter at den gamle komponent udløber. For at gøre dette skal du angive startdatoen i feltet **Fra-dato**.

## <a name="substituting-material-by-planning"></a>Erstatning af materiale efter planlægning
Du kan kun erstatte materialer under planlægning, når du bruger formler, ikke når du bruger en stykliste. Overvej følgende scenario: En produktionsvirksomhed inden for fødevarer laver en sauce ud fra en formel, der har 20 ingredienser. En ingrediens i formlen kan erstattes af en af to andre ingredienser. Men da disse to ingredienser er dyrere end den foretrukne ingrediens, bruges erstatningen kun, hvis den foretrukne ingrediens er udsolgt. Det materiale, der kan erstattes, kaldes A, mens de to materialer, der kan erstatte det, kaldes B og C. Materialeerstatning efter planlægning styres af felterne **Planlægningsgruppe** og **Prioritet** på formellinjerne. I dette eksempel skal du oprette formellinjer for de tre materialer og knytte formellinjer til den samme planlægningsgruppe. I opsætningen har formellinjen for materiale A den højeste prioritet (laveste tal), formellinjen for materiale C har den laveste prioritet, og formellinjen for materiale B har en prioritet, der ligger mellem prioriteten af de to andre linjer. Hvis du har behov for den færdige vare, bestemmer varedisponering først, om behovet for en materiale A kan dækkes. Hvis behovet ikke kan dækkes, ser varedisponering på materialerne B og C i prioriteret rækkefølge. Hvis materiale B er på lager, bruges det, når en planlagt batchordre er autoriseret for formlen. Hvis ingen af materialerne er på lager, opretter varedisponering et ordreforslag for materiale A. **Bemærk!** Når du konfigurerer formellinjer i en planlægningsgruppe, skal du kun angive et antal for det materiale, der har den højeste prioritet. Dette antal vil blive brugt til at beregne behovet for alle materialer i planen, selv de materialer, der har lavere prioritet. Du kan ikke angive forskellige mængder for varer med lavere prioritet i planlægningsgruppen.

## <a name="substituting-material-during-production"></a>Erstatning af materiale under produktion
Forestil dig følgende situation: Der kræves et stykke metalplade til en svejsning. Under processen fortæller en lagermedarbejder maskinoperatøren, at pladen er udsolgt. Det er dog besluttet, at pladen kan erstattes med en plade, der er lidt tykkere. På denne måde kan processen afsluttes. Materiale kan føjes til styklisten for en åben produktionsordre. Hvis produktionsordren har statussen **Startet**, bliver brugere bedt om at vurdere ordren igen, når de føjer en ny vare til produktionsstyklisten. Når materialet er tilføjet, kan der oprettes en ny plukliste for den nye vare. Du behøver ikke at føje nyt materiale til produktionsstyklisten. I stedet kan du føje det direkte til produktionspluklisten. Når pluklisten bogføres, tilføjer systemet materialet på produktionsstyklisten.



