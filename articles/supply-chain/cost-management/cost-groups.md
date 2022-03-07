---
title: Kostprisgrupper
description: Kostgrupper udgør grundlaget for segmentering og analyse af kostbidraget i en færdigvares beregnede omkostninger, såsom kostbidrag til materialer, arbejdsløn og indirekte omkostninger. Der anvendes flere synonymer for kostgruppesegmentering i produktionsmiljøer, f.eks. kostprisopdeling eller klassificering af omkostninger.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b60c8a353a4c545cf5c1f1b1e5565d0d7e2a5bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572140"
---
# <a name="cost-groups"></a>Kostprisgrupper

[!include [banner](../includes/banner.md)]

Kostgrupper udgør grundlaget for segmentering og analyse af kostbidraget i en færdigvares beregnede omkostninger, såsom kostbidrag til materialer, arbejdsløn og indirekte omkostninger. Der anvendes flere synonymer for kostgruppesegmentering i produktionsmiljøer, f.eks. kostprisopdeling eller klassificering af omkostninger. 

Der anvendes flere synonymer for kostgruppesegmentering i produktionsmiljøer, f.eks. kostprisopdeling eller klassificering af omkostninger. Segmentering af kostgrupper kan tjene flere formål. Her er nogle eksempler:

-   Det kan segmentere omkostninger for forskellige materialetyper, f.eks. ingredienser og emballagemateriale for produkter på dåse, baseret på kostgrupper, der er tildelt varer.
-   Det kan segmentere omkostninger for forskellige typer operationsressourcer, f.eks. forskellige typer arbejdskraft eller maskiner, baseret på de kostprisgrupper, der er tildelt til omkostningskategorier, som vedrører operationsressourcer og ruteoperationer.
-   Det kan segmentere omkostninger for opstillings- og procestid i ruteoperationer, baseret på de kostgrupper, som er tildelt omkostningskategorier, der vedrører ruteoperationerne.
-   Det kan segmentere omkostninger for forskellige typer indirekte omkostninger, f.eks. indirekte omkostninger, der vedrører arbejdskraft og maskiner, baseret på kostprisgrupper, der er tildelt til indirekte omkostninger i opsætning af kostprisarket.
-   Det kan fungere som udgangspunkt for beregning af forskellige typer af indirekte produktionsomkostninger i opsætningen til kostprisark. Disse produktionsomkostninger kan omfatte forskellige typer af indirekte omkostninger, der er relateret til oplysninger om operationsressourcer eller til oplysninger om opstillings- og procestid. Indirekte produktionsomkostninger kan også relateres til kostbidrag til komponentmaterialer, hvilket afspejler en filosofi baseret på lean produktion, der fjerner behovet for ruteoplysninger.

Segmentering af kostprisgrupper gælder for de beregnede omkostninger for en produceret vare, uanset om disse omkostninger er baseret på standardomkostninger eller planlagte omkostninger. På siden **Oversigt** vises denne segmentering efter kostgruppe, efter niveau eller efter både kostgruppe og niveau. 

Muligheden for at bevare kostgruppesegmenteringen på tværs af flere niveauer i en produktstruktur kaldes *splitning*. Splitning gælder kun for producerede varer, der bruger lagermodellen Standardomkostning. Hvis splitning ikke bruges, behandles omkostningerne for en produceret komponent som et materialekostbidrag. Lagerparameteren for kostprisopdeling efter reskontro angiver, at kostgruppesegmenteringen bevares på tværs af flere niveauer, når der beregnes standardomkostninger. Hvis der i stedet anvendes en politik uden niveauer, gælder kostgruppesegmenteringen kun ved beregning for et enkelt niveau. På siden **Omkostningstotaler pr. kostgruppe** vises f.eks. kostgruppesegmentering over flere niveauer for standardomkostningsposter. 

Segmentering af kostprisgrupper kan kun gælde for varianter af en standardkostpriser. En anden lagerparameter definerer, om afvigelser skal identificeres vha. kostgrupper eller kun opsummeres. 

En kostprisgruppe kan tildeles en kostprisgruppetype og en funktionsmåde til flere segmenteringsformål.

-   **Kostprisgruppetype** − De enkelte kostprisgrupper skal tildeles en kostprisgruppetype for at angive, at kostprisgruppen vedrører direkte materialer, direkte fremstilling eller direkte outsourcing eller for at angive den som indirekte eller udefineret. En kostprisgruppe, der er angivet som direkte materialer, kan tildeles til varer. En kostprisgruppe for direkte fremstilling kan tildeles til omkostningskategorier. En direkte outsourcingkostprisgruppe kan tildeles produkttypen tjeneste, så du kan som klassificere omkostninger, der er knyttet til tjenestekøbet til aktiviteter i forbindelse med underleverandørarbejde. En indirekte kostprisgruppe kan tildeles til indirekte omkostninger for tillæg eller satser. En kostprisgruppe, der er angivet som udefineret, kan tildeles til varer, omkostningskategorier eller indirekte omkostninger. Tildelingen af en kostprisgruppetype tjener flere formål. For det første begrænser det muligheden for at tildele en kostgruppe og få vist en liste over gældende kostgrupper. For det andet tilbyder den supplerende segmentering med henblik på rapportering. For det tredje kan den bruges til at tildele finanskonti til varianter.
-   **Adfærd** − De enkelte kostgrupper kan evt. tildeles en adfærd for at angive, at kostgruppen vedrører faste omkostninger eller variable omkostninger. Hvis en kostgruppe har en null-værdi for adfærd, behandles den som en variabel omkostning. Tildelingen af en adfærd har kun betydning i forbindelse med rapportering. Omkostninger kan f.eks. vises med segmentering af faste og variable omkostninger på kostprisarket og på siden **Omkostningstotaler pr. kostgruppe**. Hvis du tildeler hver enkelt kostgruppe en procentdel af et avancesæt, foreslår styklisteberegningen en salgspris på basis af en fremgangsmåde, hvor kostprisen lægges sammen med avancen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]