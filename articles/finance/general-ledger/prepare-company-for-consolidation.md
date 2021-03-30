---
title: Forberede en juridisk enhed til brug i konsolideringsprocessen
description: Under en konsolidering indsamles transaktioner fra flere sæt juridiske enhedskonti til ét sæt juridiske enhedskonti. Dette emne forklarer, hvordan du forbereder en juridisk enhed til en konsolidering.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 07988e71276c6439e392bce2087f3a8923f5f40b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230196"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Forberede en juridisk enhed til brug i konsolideringsprocessen

[!include [banner](../includes/banner.md)]

Under en konsolidering indsamles transaktioner fra flere sæt juridiske enhedskonti til ét sæt juridiske enhedskonti. Dette emne forklarer, hvordan du forbereder en juridisk enhed til en konsolidering.

> [!NOTE]
> Det anbefales, at du bruger Management Reporter til Microsoft Dynamics 365 Finance til at kombinere de økonomiske resultater for flere juridiske enheder i et konsolideret format. Du kan bruge Management Reporter til at oprette konsoliderede regnskabsrapporter på tværs af juridiske enheder, bruge Excel til at importere konsolideringsdata fra andre kilder og oversætte beløb til et vilkårligt antal rapporteringsvalutaer uden at skulle køre konsolideringsprocessen i Dynamics 365 Finance.

Du kan udskrive rapporter, f.eks. årsregnskaber, fra den konsoliderede juridiske enhed. Du kan dog ikke bruge den konsoliderede juridisk enhed til daglige transaktioner.

Du kan konsolidere data fra juridiske enheder, der bruger andre databaser end den konsoliderede juridiske enhed. Denne konsolideringsproces kaldes en *importkonsolidering*. Juridiske enheder kan også bruge den samme database som den konsoliderede juridiske enhed. Denne konsolideringsproces kaldes en *onlinekonsolidering*.

Den konsoliderede juridiske enhed indsamler resultater og saldi fra datterselskaber. Hvis du vil forberede en konsolideret juridisk enhed for en konsolidering, skal du følge disse trin.

1. Gå til **Finans \> Opsætning \> Organisation \> Juridiske enheder**.
2. Vælg **Ny** for at oprette en ny juridisk enhed, som skal være den konsoliderede juridiske enhed.
3. Markér afkrydsningsfeltet **Brug til økonomisk konsolideringsproces**, og angiv derefter oplysninger om den konsoliderede juridiske enhed. Sørg for at indtaste oplysningerne nøjagtigt som de skal vises på opgørelser for den konsoliderede juridiske enhed.
4. Luk siden.
5. Vælg den konsoliderede juridiske enhed i feltet øverst til højre på siden, og vælg derefter **OK**.
6. Gå til **Finans \> Opsætning \> Finans**.
7. Vælg kontoplan, regnskabskalenderen, regnskabsvaluta, en valgfri rapporteringsvaluta og standardvalutakurstypen for den konsoliderede juridiske enhed. 
8. Gå til **Finans \> Opsætning \> Valuta \> Valutakurser**.
9. Angiv valutakurser i relevante perioder for valutaerne for de underliggende juridiske enheder.
10. Luk siden.
11. Hvis den konsoliderede juridiske enhed har datterselskaber, der bruger fremmede valutaer, skal du følge disse trin:

    1. Gå til **Finans \> Opsætning \> Bogføring \> Konti til automatiske posteringer**.
    2. Vælg en relevant konto i feltet **Bogføringstype** :

        - Hvis den juridiske enhed har udenlandske datterselskaber, der er økonomisk eller driftsmæssige afhængige af den overordnede juridiske enhed, skal du vælge en passende konto til **Driftsregnskab for bogføringstypen for konsolideringsafvigelser**-typen.
        - Hvis du konsoliderer et datterselskab, som er økonomisk og driftsmæssigt uafhængigt af den overordnede juridiske enhed, eller en juridisk enhed, der indeholder resultaterne fra flere datterselskaber, som er økonomisk og driftsmæssigt uafhængige af den overordnede juridiske enhed, og hvis du bruger oversættelsesmetoder til konsolidering af data, skal du vælge en relevant konto for bogføringstypen **Driftsregnskab for bogføringstypen for konsolideringsafvigelser**.

    3. Vælg de hovedkonti, der skal bruges til værdireguleringer af fremmed valuta, i feltet **Hovedkonto**.
    4. Luk siden.

    Hvis du opretter den konsoliderede juridiske enhed tidligt i en periode, kan du regulere de udenlandske valutabeløb som valutakursændringer under konsolideringsperioden.

Den konsoliderede juridiske enhed er nu konfigureret til det periodiske job **Konsolider**. Du kan enten udføre en importkonsolidering eller en onlinekonsolidering.

- Du kan udføre en importkonsolidering ved at gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Importer fra\]**.
- Du kan udføre en online-konsolidering ved at gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Online\]**.

> [!NOTE]
> Inden du kan behandle konsolideringen, skal du klargøre de underordnede juridiske enheder til konsolidering. Du kan finde flere oplysninger i [Konfigurere en juridisk datterselskabsenhed til konsolidering](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]