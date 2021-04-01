---
title: Fordele tid til job i et jobbundt
description: Ved udførelse af Produktion kan du bundte job. Derefter kan du starte flere job samtidig på siden Jobliste.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88c75c67cadcde57f981f4e357b40855709d072d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246495"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Fordele tid til job i et jobbundt

[!include [banner](../includes/banner.md)]

Ved udførelse af Produktion kan du bundte job. Derefter kan du starte flere job samtidig på siden Jobliste.

Hvis du kan bundte job, skal du definere, hvordan den samlede registrerede tid for alle job bør tildeles hvert job. Du kan definere fordelingen ved at vælge en af følgende indstillinger i feltet **Bundttype** på siden **Fordelingsnøgler**:

-   **Forkalkulation** – Tid er opdelt mellem job, baseret på estimeret tid for jobbet.
-   **Job** – Tiden er opdelt efter, hvor mange job der er bundet i alt, og hvor lang tid der er brugt på at færdiggøre alle job.
-   **Nettotid** – Tid er fordelt ligeligt mellem de job, der findes i bundtet på et vilkårligt tidspunkt.
-   **Realtid** – Faktisk jobtid fordeles. Omkostningerne kan beregnes på basis af faktiske lønudgifter. **Bemærk:** Fordelingsnøglen **Realtid** er kun tilgængelig, hvis dit firma bruger lønfunktionen i Tid og fremmøde.

Følgende eksempler viser resultatet af de forskellige fordelingsnøgler.

## <a name="example-scenario"></a>Eksempelscenario
Tre job i jobkøen skal udføres. Du starter det første job, og derefter, mens dette job er i gang, starter du det andet og tredje job. Der er derfor et bundt af tre job. Følgende tabel viser den forventede produktionstid for hvert job.

| Stilling   | Produktionstid |
|-------|-----------------|
| Job 1 | 1 time          |
| Job 2 | 3 timer         |
| Job 3 | 4 timer         |
| I alt | 8 timer         |

Følgende tabel viser de faktiske arbejdstimer, der er brugt på hvert job.

| Stilling    | Starttidspunkt | Sluttidspunkt | Bundttid |
|--------|------------|----------|-------------|
| Job 1  | 09:00      | 11:00    | 2 timer     |
| Job 2  | 10:00      | 13:00    | 3 timer     |
| Job 3  | 10:00      | 15:00    | 5 timer     |
| Bundt | 09:00      | 15:00    | 6 timer     |

Følgende afsnit beskriver resultaterne af den beregnede tid for hver fordelingsnøgle.

## <a name="estimation-allocation-key"></a>Forkalkulation for fordelingsnøgle
Følgende tabel illustrerer formlen til beregning af tildelt tid. Her er formlen: Tid pr. job = Samlet bundttid × (forkalkuleret jobtid ÷ samlet forkalkuleret tid)

| Stilling   | Formel           | Tildelt tid |
|-------|-------------------|----------------|
| Job 1 | 6 × (1 ÷ 8) timer | 0,75 timer      |
| Job 2 | 6 × (3 ÷ 8) timer | 2,25 timer     |
| Job 3 | 6 × (4 ÷ 8) timer | 3,00 timer     |

## <a name="jobs-allocation-key"></a>Jobfordelingsnøgle
Følgende tabel illustrerer formlen til beregning af tildelt tid. Her er formlen: Tid pr. job = Samlet bundt tid ÷ antal job

| Stilling   | Formel | Tildelt tid |
|-------|---------|----------------|
| Job 1 | 6 ÷ 3   | 2 timer        |
| Job 2 | 6 ÷ 3   | 2 timer        |
| Job 3 | 6 ÷ 3   | 2 timer        |

## <a name="net-time-allocation-key"></a>Nøgle til nettotidsfordeling
Følgende tabel illustrerer formlen til beregning af tildelt tid. Her er formlen: Beregnet tid pr. rapportering = Bundttid ÷ Antal job

|                              | 09:00-10:00 (1 time) | 10:00-11:00 (1 time) | 11:00-13:00 (2 timer) | 13:00-15:00 (2 timer) | Tildelt tid |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Antal job i bundtet | 1                    | 3                    | 2                     | 1                     | Ikke tilgængelig |
| Job 1                        | 1 ÷ 1 = 1 time       | 1 ÷ 3 = 0,33 time    | Ikke tilgængelig        | Ikke tilgængelig        | 1,33 timer     |
| Job 2                        | Ikke tilgængelig       | 1 ÷ 3 = 0,33 time    | 2 ÷ 2 = 1 time        | Ikke tilgængelig        | 1,33 timer     |
| Job 3                        | Ikke tilgængelig       | 1 ÷ 3 = 0,33 time    | 2 ÷ 2 = 1 time        | 2 ÷ 1 = 2 timer       | 3,33 timer     |

## <a name="real-time-allocation-key"></a>Fordelingsnøgle for realtid
Hvis du vil have, at produktionsomkostninger beregnes på grundlag af de reelle omkostninger, skal du fjerne markeringen i indstillingen **Omkostningsart** på siden **Produktionsordrestandarder**. Følgende tabel illustrerer formlen til beregning af tildelt tid. Her er formlen: Faktisk tid pr. job = Faktisk tid i bundt

| Stilling   | Faktisk tidspunkt |
|-------|-------------|
| Job 1 | 2 timer     |
| Job 2 | 3 timer     |
| Job 3 | 5 timer     |

Overvej de tre job, der udføres af en arbejder, der har en timeløn på DKK 12,00. Der blev ikke opnået overtidsbetaling eller løntillæg i den tid, der blev brugt på job. Arbejderen har arbejdet på disse 3 bundtede job i 6 timer i alt. Lønomkostningerne er derfor 6 × DKK 12,00 = DKK 72,00. Når du bruger fordeling i realtid, genberegnes kostpris pr. time ved hjælp af faktoren fra formlen Nettotid. Den faktiske tid, der blev brugt på hvert job, overføres derefter sammen med den korrigerede kostpris pr. time. I eksemplet bruges der 6 timer, selvom der er fordelt 10 timer. Følgende tabel illustrerer formlen til beregning af omkostning. Her er formlen: Omkostninger pr. time = (Samlet bundttid pr. job (nettotid) ÷ faktisk tid pr. job) × standardkostpris pr. time

| Stilling   | Beregning af korrigeret omkostning pr. time | Korrigeret omkostning pr. time | Tildelt tid | Samlede jobomkostninger |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Job 1 | (1,33 ÷ 2) × DKK 12,00                 | DKK 8,00                | 2 timer        | DKK 16,00         |
| Job 2 | (1,33 ÷ 3) × DKK 12,00                 | DKK 5,33                | 3 timer        | DKK 16,00         |
| Job 3 | (3,33 ÷ 5) × DKK 12,00                 | DKK 8,00                | 5 timer        | DKK 40,00         |

Den korrigerede omkostning pr. time og jobtiden posteres i produktionskladden. **Bemærk:** Hvis du vælger indstillingen **Omkostningsart** på fanen **Generelt** på siden **Produktionsordrestandarder**, overføres den faktiske tid for hvert job til en produktionskladde, hvor omkostningerne er anvendt til omkostningsarten for det aktuelle job.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]