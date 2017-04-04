---
title: "Projekt periodisering på købsleverancer"
description: "Dette emne beskriver, hvordan periodiseret projektomkostninger i forbindelse med indkøb, tilgange kan spores i Microsoft Dynamics 365 for operationer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projekt periodisering på købsleverancer

Dette emne beskriver, hvordan periodiseret projektomkostninger i forbindelse med indkøb, tilgange kan spores i Microsoft Dynamics 365 for operationer. 

Fakturaer for et projekt ankommer ofte senere end varerne og tjenester er leveret, som kan have betydelig indvirkning på projekt nøgletal (KPI'er). Det er vigtigt at være i stand til at spore disse transaktioner i både finansielle og projekt rapporter.

I følgende eksempel scenario illustrerer dette. 

Contoso høring er startet et nyt projekt med sky installation. Der oprettes en indkøbsordre for at købe en computer for projektet. Computeren vil koste $1500 og installationsservices koster $150. Leverandøren har leveret og installeret på computeren, men fakturaen er endnu ikke har nået Contoso høring. Projektlederen vil gerne se projektet periodisering af $1650, før fakturaen er leveret. Denne omkostning bør også afspejles i virksomhedens måned slut balancer. 

De påløbne omkostninger skal registreres på økonomisk niveau- og projektniveau til rapporteringsformål. I Dynamics 365 for operationer, kan den økonomiske opdatering af produktkvitteringen spores for kategorierne vare og indkøb. 

For varer, på den **konti Kreditorparametre** side, vælge den **bogføre produktkvitteringer Finans** indstilling.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

For indkøbskategorier, på den **Kategoripolitikreglen** side, vælge **indkøb** politikker, og vælg derefter **periodiseret køb udgift på tilgang** for hver indkøbskategori.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Den **købe udgifter ikke-faktureret** og **købsperiodisering** firmaer i **opsætning af finanskontering** skal bruges til bogføring af bilag, der er knyttet til produktkvitteringen.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Ved hjælp af denne samme scenarie, Lad os se, hvordan bogføring af en produktkvittering påvirker finansmodulet og projektoplysninger. 

**Trin 1:** Opret og Bekræft en ny indkøbsordre for projektet til at registrere købet af en computer til installation og $1500 services for $150.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Når indkøbsordren er bekræftet, oprettes der posteringer for den bindende omkostning for projektet. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Posteringerne for den bindende omkostning vil have den **posteringsgrundlaget** indstillet til **indkøbsordre**. Opretter og bekræfter en indkøbsordre oprettes der ikke posteringer for et projekt. 

**Trin 2:** få leveret varer og tjenesteydelser, og som er registreret en produktkvittering. 

Bogføring af en produktkvittering genererer og bogfører et bilag til Finans. Bilaget debitere indkøb udgifter, ikke-faktureret konto og kreditere en konto til periodisering af køb. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Bogføring af en produktkvittering vil bruge posteringsopsætningen til indkøbskategorier og produkter og ikke konteringsopsætningen for projektarter. Denne opsætning skal justeres for at afspejle korrekt økonomiske virkning af køb periodiseringer. 

Det er muligt at knytte indkøbskategorier til projektarter på den **indkøbskategori** side.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Trin 3:** oprette en kreditorfaktura i kladden. 

I Dynamics 365 for handlinger påvirker bogføring af en produktkvittering ikke projektoplysninger. Som en løsning kan du generere en kreditorfaktura udkast til direkte efter bogføring købsleverancen. Gå til den **indkøbsordre** side &gt;**faktura under fanen**&gt;**Generer**&gt;**faktura**. Dette opretter en ventende faktura-dokument, der opdaterer projektoplysningerne. 

Oprette en kreditorfaktura i kladden oprettes ventende projektposteringer. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

I den **bindende omkostning** side, poster, der er oprettet i trin 1 vil blive lukket, og der oprettes nye poster for at afspejle omkostningerne engagement kommer fra ventende kreditorfakturaen. Den **posteringsgrundlaget** felt for den bindende omkostning vil blive indstillet til **kreditorfaktura**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Kreditorfakturaen forbliver i tilstanden Afventer, indtil den faktiske kreditorfaktura ankommer.


