---
title: "Simulere ændringer i omkostningen ved hjælp af en efterkalkulationsversion for planlagte omkostninger"
description: "Denne artikel forklarer, hvordan du kan simulere effekterne ved omkostningsændringer af de beregnede omkostninger for producerede varer med en separat efterkalkulationsversion for planlagte omkostninger."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07dc838b38b060d45930a24b13be3dc283457282
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Simulere ændringer i omkostningen ved hjælp af en efterkalkulationsversion for planlagte omkostninger

[!include[banner](../includes/banner.md)]


Denne artikel forklarer, hvordan du kan simulere effekterne ved omkostningsændringer af de beregnede omkostninger for producerede varer med en separat efterkalkulationsversion for planlagte omkostninger.

Du kan simulere effekterne ved omkostningsændringer af de beregnede omkostninger for en produceret vare med en separat efterkalkulationsversion for planlagte omkostninger. Brug denne separate efterkalkulationsversion til at angive ventende omkostningsposter, der afspejler trinvise omkostningsændringer, og til at beregne omkostningens indflydelse på producerede varer. Fordi reserveprincippet for aktive omkostninger bruges i beregningerne af styklister, er det kun trinvise ændringer i omkostningen, som skal angives.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Retningslinjer for definition af simuleret efterkalkulationsversionen
Brug følgende retningslinjer til at definere simuleringer af efterkalkulationsversionen:

-   Tildel en omkostningstype af **planlagte omkostninger**.
-   Tildel efterkalkulationsversionen et sigende id, f.eks. **simulering**.
-   Sørg for, at indholdet omfatter omkostningsposter.
-   Tillad indtastning af omkostningsposter. Bloker ikke for indtastning af ventende omkostninger.
-   Tillad, at der angives omkostningsposter for alle steder. Hvis du angiver et sted, begrænser du angivelsen af omkostningsposter til det pågældende sted.
-   Undgå aktivering af ventende omkostninger. Det er kun ventende omkostninger, der skal angives for kostprisposter i den simulerede efterkalkulationsversion.
-   Du skal ikke angive en "fra"-dato. Der angives en beregningsdato for alle beregninger af styklister, der bruger den simulerede efterkalkulationsversion.
-   Angiv et reserveprincip som **aktuelt aktiv**. Reserveprincippet gør det muligt at angive trinvise omkostningsændringer med henblik på simulering, men der bruges aktuelle, aktive omkostninger som kilde til alle andre omkostningsposter. Det antages, at alle aktuelle, aktive omkostninger kan anvendes på alle andre omkostningsposter.
-   Angiv en kostprismodel som **kostprisen for versionen**, men begræns ikke beregninger. Der kan f.eks. også bruge en kostprismodel af **styklisteberegningsgruppen** i simuleringerne, som angiver kilden til kostbidragsdataene for indkøbte varer.
-   Angiv en udfoldningstilstand på **flere niveauer**, men begræns ikke beregninger. Simuleringerne kan bruge andre udfoldningstilstande.

## <a name="costing-versions"></a>Efterkalkulationsversioner
I følgende scenarier vises, hvordan den simulerede efterkalkulationsversion bruges til at simulere indvirkningen af ændringer i omkostningen. Før du angiver en simuleret omkostningsændring, skal du slette posterne for ventende omkostninger i den simulerede efterkalkulationsversion, så du har et tomt udgangspunkt. Brug siden **Varepris** til at se og slette posterne for ventende omkostninger, der vedrører varepriser og priser på omkostningskategorier.

-   Simuler ændringen af kostprisen for en købt vare. Ændringen af omkostningen kan f.eks. afspejle en forventet stigning eller et forventet fald i omkostningerne for vigtige, købte materialer. Hvis du vil angive den ændrede omkostning for en købt vare, skal du bruge siden **Varepris** til angive en ventende omkostningspost i efterkalkulationsversionen til simuleringen.
-   Simuler ændringen af kostprisen for en omkostningskategori. Ændringen af omkostningen kan f.eks. afspejle en forventet stigning eller et forventet fald i lønsatserne eller timesatserne for operationsressourcerne. Hvis du vil angive den ændrede omkostning i en omkostningskategori, skal du bruge siden **Pris for omkostningsart** til at angive en ventende omkostningspost i efterkalkulationsversionen til simuleringen.
-   Simuler ændringen af kostprisen i en formel til beregning af indirekte omkostninger. Ændringen af omkostningen kan f.eks. afspejle en forventet stigning eller et forventet fald i produktionsomkostningerne. Hvis du vil angive ændringen i en formel til beregning af indirekte omkostninger, skal du bruge siden **Opsætning af efterkalkulationsark** til at angive en ventende omkostningspost i efterkalkulationsversionen til simuleringen og til at validere og gemme ændringen.

Når du har angivet de simulerede omkostningsændringer, skal du beregne omkostningerne for producerede varer, der påvirkes af omkostningsændringerne. Brug siden **Beregning** til den simulerede efterkalkulationsversion, og identificer de valgte producerede varer, der påvirkes af omkostningsændringerne. Beregningen af styklister gælder for alle producerede varer, medmindre du vælger specifikke varer. Du kan også anvende indstillingen til beregning af styklister til opdateringer af indgår-i. Se poster med varens kostpris i den simulerede efterkalkulationsversion for at analysere, hvordan de simulerede ændringer i kostprisen påvirker kostpriserne på de valgte producerede varer. Brug siden **Varepris** og siden **Beregn vareomkostninger** til at se og analysere omkostningerne.




