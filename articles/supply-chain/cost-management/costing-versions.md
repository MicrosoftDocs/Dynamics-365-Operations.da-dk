---
title: Oversigt over efterkalkulationsversioner
description: Denne artikel indeholder oplysninger om efterkalkulationsversioner, hvordan du vedligeholder dem, og de typer data, som du kan medtage i dem. Det primære formål med en efterkalkulationsversion er at opbevare omkostningsposter om varer, omkostningskategorier og formler til beregning af indirekte omkostninger.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "54532"
- intro-internal
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 355721d5ac313553bd573665c616bfb155b70826
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339637"
---
# <a name="costing-versions-overview"></a>Oversigt over efterkalkulationsversioner

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om efterkalkulationsversioner, hvordan du vedligeholder dem, og de typer data, som du kan medtage i dem. Det primære formål med en efterkalkulationsversion er at opbevare omkostningsposter om varer, omkostningskategorier og formler til beregning af indirekte omkostninger.

En efterkalkulationsversion kan have et eller flere formål, afhængigt af de data der findes i efterkalkulationsversionen. Det primære formål med en efterkalkulationsversion er at opbevare omkostningsposter om varer, omkostningskategorier og formler til beregning af indirekte omkostninger. En efterkalkulationsversion kan indeholde standardkostprisposter eller planlagte kostprisposter, der er baseret på den efterkalkulationstype, som er tildelt til efterkalkulationsversionen.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Efterkalkulationsversioner for standardomkostninger eller planlagte omkostninger.
### <a name="standard-costs"></a>Standardomkostninger

En efterkalkulationsversion kan understøtte en lagermodel med standardomkostninger for varer, hvor efterkalkulationsversionen indeholder standardomkostningsposter for varer og produktionsprocesser. Omkostningsoplysninger om produktionsprocesser er udtrykt i forhold til omkostningskategorierne for ruteoperationer og formlerne til beregning af indirekte omkostninger ved produktion.

### <a name="planned-costs"></a>Planlagte omkostninger

En efterkalkulationsversion kan indeholde et sæt planlagte omkostningsposter om varer og produktionsprocesser. En efterkalkulationsversion, der indeholder planlagte omkostninger, bruges ofte som et led i simuleringer af omkostningsberegning, f.eks. simulering af den effekt, som ændringer af omkostningen for købte materialer eller produktionsprocesser vil have på de beregnede omkostninger for producerede varer. Vareomkostningsposter for planlagte omkostninger kan også bruges som et led i en lagermodel over faktiske omkostninger, hvor de udgør initialværdierne for vareomkostningerne. Disse værdier omfatter beregningen af planlagte omkostninger for producerede varer.

## <a name="entering-costs"></a>Angivelse af omkostninger
Datavedligeholdelse af omkostningsposter i en efterkalkulationsversion omfatter angivelse af omkostninger for købte varer og for varer, der overføres mellem lokationer. Ekstra vedligeholdelse af data for producenter omfatter angivelse af omkostninger for omkostningskategorier, der er knyttet til ruteoperationer, angivelse af formler til beregning af indirekte omkostninger, der afspejler indirekte produktionsomkostninger, og beregning af omkostninger for producerede varer. 

Vareomkostningsoplysningerne i en efterkalkulationsversion består af en eller flere omkostningsposter for de enkelte varer. Når en vares omkostningspost angives først, har den statussen **Venter** og en ønsket ikrafttrædelsesdato. Når du aktiverer omkostningsposten, opdateres statussen til **Aktiv**, og ikrafttrædelsesdatoen opdateres til aktiveringsdatoen. Forskellige omkostningsposter kan afspejle forskellige lokationer, ikrafttrædelsesdatoer eller statusser. Når du beregner omkostninger for producerede varer for en fremtidig dato, bruger beregning af styklisten omkostningsposter, der har den relevante ikrafttrædelsesdato, uanset om statussen er **Venter** eller **Aktiv**. En vares aktuelle omkostningspost bruges til at beregne omkostninger på produktionsordrer og til at værdisætte lagertransaktioner efter en standardlagermodel for efterkalkulation. Vedligeholdelse af omkostningsposter for omkostningskategorier og formler til beregning af indirekte omkostninger minder om vedligeholdelse af varens omkostningsposter. 

De to blokeringsregler for en efterkalkulationsversion bestemmer, om ventende omkostninger kan vedligeholdes, og om de ventende omkostninger kan aktiveres. Brug blokeringsreglerne til at tillade vedligeholdelse af data og derefter til at forhindre vedligeholdelse af data for omkostningsposter i en efterkalkulationsversion. 

En efterkalkulationsversion kan også indeholde data om salgspriser eller indkøbspriser for varer med henblik på beregning af styklister.

## <a name="item-sales-prices-for-bom-calculations"></a>Salgspriser til styklistekalkulationer
Den vigtigste årsag til inkludering af data om salgspriser er at bevare en produceret vares beregnede salgspris. De beregnede salgspriser kan derefter analyseres for at bestemme, hvordan komponenter, ruteoperationer og indirekte omkostninger bidrager til kost- og salgsprisen. 

En sekundær årsag til inkludering af data om salgspriser er at definere salgsprisposter for indgående varer. Disse poster kan derefter bruges til at beregne salgsprisen for producerede varer. Du angiver først den salgsprismodel, der er integreret i en styklisteberegningsgruppe, og knytter styklisteberegningsgruppen til købte varer. Når du derefter udfører beregninger for styklisten, der anvender planlagte omkostninger, kan du vælge en kostprismodel for styklisteberegningsgruppen. 

Ellers bruges salgsprisposterne for varer kun som referenceoplysninger, uanset om posterne angives manuelt eller beregnes. Du kan opdatere basissalgsprisen for en vare ved at aktivere en vares salgsprispost. Basissalgsprisen er dog ikke lokationsspecifik, og den kan tilsidesættes manuelt. Varens basissalgspris bruges som en standardsalgspris på salgsordrer og salgstilbud.

## <a name="item-purchase-prices-for-bom-calculations"></a>Købspriser til styklistekalkulationer
Hovedårsagen til aktivering af købsprisdata er at definere købsprisposter for indgående varer, så disse poster kan bruges til at beregne omkostningerne for de producerede varer. Varens indkøbsprisposter skal angives manuelt. 

For at aktivere indhold om købspris skal du først definere en styklistekalkulationsgruppe, der indeholder en kostprismodel for varens købspris, og derefter knytte en styklistekalkulationsgruppe til købte varer. Du skal derefter bruge en kostprismodel for styklistekalkulationsgruppen, når du udfører styklistekalkulationer, der bruger planlagte omkostninger, for at beregne salgsprisen for producerede varer. 

Købsprisposterne for varer bruges også kun som referenceoplysninger. Ved at ændre status for en vares købsprispost fra **Venter** til **Aktiv** kan du opdatere varens basiskøbspris. Basiskøbsprisen er dog ikke lokationsspecifik, og den kan tilsidesættes manuelt. Varens basiskøbspris bruges som standardkøbspris på indkøbsordrer.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]