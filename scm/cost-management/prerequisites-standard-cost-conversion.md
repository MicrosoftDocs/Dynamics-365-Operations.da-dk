---
title: "Forudsætninger for en standardomkostningskonvertering"
description: "Dette emne indeholder en beskrivelse af de opgaver, der skal udføres før kørsel af en standardomkostningskonvertering."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7a9cac200301ea58e4dd9047cd9ff42648126b8e
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="prerequisites-for-a-standard-cost-conversion"></a>Forudsætninger for en standardomkostningskonvertering

[!include[banner](../includes/banner.md)]


Dette emne indeholder en beskrivelse af de opgaver, der skal udføres før kørsel af en standardomkostningskonvertering. 

Udfør følgende trin, før du kører en standardomkostningskonvertering:

1.  Definer en **varemodelgruppe** for standardomkostninger. Brug siden Varemodelgrupper til at oprette en varemodelgruppe med en lagermodel for standardomkostninger. Når du angiver en standardomkostningskonvertering, skal du tildele denne varemodelgruppe til de varer, der konverteres.
2.  Knyt en **kostprisgruppe** til de enkelte varer.
    -   Den kostprisgruppe, der knyttes til en købsvare, fungerer som basis for tildeling af finanskonti, der er relateret til standardomkostninger. Det kan omfatte tildeling af finanskonti til afvigelser i købspris. I et produktionsmiljø udgør den kostprisgruppe, der knyttes til købte komponenter, også grundlaget for segmentering af omkostninger i de beregnede kostpriser for en produceret vare.
    -   Den kostprisgruppe, der er knyttet til en produceret vare, kan fungere som udgangspunkt for tildeling af finanskonti, der er relateret til standardomkostninger, f.eks. tildeling af finanskonti til afvigelser i produktion.

3.  Knyt et **standardordreantal** til en produceret vare, når omkostningerne er konstante. Standardordreantallet for en produceret vare fungerer som en regnskabsmæssig lotstørrelse til amortisering af konstante omkostninger. Det kan omfatte opsætningstider i ruteoperationer eller et konstant komponentantal på styklisten.
4.  Tilknyt **finanskonti**, der er relateret til standardomkostninger, især afvigelsen i revaluering. Brug siden **Postering** (**Lagerstyring** &gt; **Konfiguration**) til at tildele finanskonti, der er relateret til standardomkostninger. Som led i konverteringsprocessen for standardomkostninger skal du som minimum tildele kontoen for afgivelsen i revalueringen for alle varer og alle kostprisgrupper. Brug siden **Kontoplan** til at definere de finanskonti, der skal bruges til standardomkostninger. Brug siden **Transaktionskombinationer** til at aktivere brugen af omkostningsrelationer (for tabeller, grupper og alle), før du definerer regler for varekontering.
5.  Definer de lagerparametre, der er knyttet til standardomkostninger. Brug fanen **Nummerserier** under på siden **Parametre til lager- og lokationsstyring** til at tildele en nummerserie til værdireguleringsbilag. Der oprettes et værdireguleringsbilag, når standardomkostningskonverteringen resulterer i en ændring af en vares lagerværdi. Brug siden **Parametre til lager- og lokationsstyring** til at definere parametre for omkostningsstyring (under fanen **Lagerregnskab**) for at definere to parametre, der er knyttet til standardomkostninger.
    -   Brug feltet **Kostprisopdeling** til at vælge Nej eller Underfinanskonto. Hvis du vælger Underfinanskonto, kaldes det en aktiv kostprisopdeling. En aktiv kostprisopdeling er meget vigtig for beregning, bevarelse og visning af segmentering af omkostningsgrupper på tværs af en produktstruktur med flere niveauer for standardomkostningsvarer. Når kostprisopdelingen er aktiv, kan du rapportere og analysere følgende i på et enkelt niveau, flere niveauer eller i det samlede format:
        1.  Lager
        2.  Igangværende arbejde (IGVA)
        3.  Vareforbrug pr. kostprisgruppe

        En aktiv kostprisopdeling betyder, at aktivering af omkostninger for en produceret vare medfører, at segmenteringen af omkostningsgruppen lagres i varens kostprispost. Hvis du ikke angiver en værdi i feltet **Kostprisopdeling**, vedligeholdes kostgruppesegmenteringen ikke for varer med standardkostpriser. Det vil sige, at standardomkostningerne for en produceret vare beregnes og vedligeholdes som et enkelt beløb uden segmentering af omkostningsgruppen, og kostbidraget for producerede komponenter samles i et enkelt beløb.
    -   Brug feltet **Afvigelser fra standard** til at vælge opsummerede eller omkostningsopdelte grupper. Hvis du vælger den omkostningsopdelte gruppe, kan du identificere afvigelser i indkøbsprisen og produktionsafvigelser pr. omkostningsgruppe. Du kan også identificere de fire typer produktionsafvigelser (afvigelse i lotstørrelse, antal, pris og erstatning). Hvis du vælger den opsummerede gruppe, kan du ikke identificere afgivelser for de enkelte omkostningsgrupper, og du kan ikke identificere de fire typer produktionsafvigelser. Du kan kun se en opsummeret produktionsafvigelse. Politikken for afvigelser fra standarden fungerer uafhængigt af politikken for kostprisopdeling. Det vil sige, at du kan vælge en regel for kostprisopdeling og vælge afvigelser for de enkelte omkostningsgrupper, så du stadig kan registrere produktionsafvigelser for de enkelte omkostningsgrupper.






