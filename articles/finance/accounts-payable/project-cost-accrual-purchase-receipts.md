---
title: Periodisering af projektomkostninger på købsleverancer
description: Dette emne beskriver, hvordan periodiserede projektomkostninger fra købsleverancer kan spores i Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 888ce67f1feba9876f71d2988268b47c9a4ca1dd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358875"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Periodisering af projektomkostninger på købsleverancer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan periodiserede projektomkostninger fra købsleverancer kan spores i Microsoft Dynamics 365 Finance. 

Fakturaer for et projekt ankommer ofte senere end varerne og tjenesterne er leveret, og det kan have betydelig indvirkning på projektets nøgletal (KPI'er). Det er vigtigt at være i stand til at spore disse transaktioner i både finansielle rapporter og projektrapporter.

Følgende eksempelscenarie illustrerer dette. 

Contoso Consulting har startet et nyt projekt med skyinstallation. Der oprettes en indkøbsordre til køb af en computer til projektet. Computeren koster $1500, og installationsservices koster $150. Leverandøren har leveret og installeret på computeren, men fakturaen er endnu ikke har nået frem til Contoso Consulting. Projektlederen vil gerne se periodiserede projektomkostninger på $1650, før fakturaen er leveret. Denne omkostning skal også afspejles i virksomhedens regnskab ved månedsafslutningen. 

De påløbne omkostninger skal registreres både på økonomisk niveau og projektniveau til rapporteringsformål. Den økonomiske opdatering af produktkvitteringen kan spores for vare- og indkøbskategorierne. 

For varer skal du på siden **Kreditorparametre** vælge indstillingen **Bogfør produktkvittering i finans**.
[![Siden kreditorparametre.](./media/accruals1-1024x409.png)](./media/accruals1.png) 

For indkøbskategorier skal du på siden **Kategoripolitikregel** vælge politikkerne **Indkøb** og derefter vælge **Periodiser indkøbsudgifter på kvittering** for hver indkøbskategori.
[![Siden Regel for kategori.](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Kontiene **Udgifter til indkøb, ikke-faktureret** og **Købsperiodisering** i **Opsætning af bogføring** bruges til bogføring af bilag, der er knyttet til produktkvitteringen.

Når vi bruger det samme scenarie, så lad os se, hvordan bogføring af en produktkvittering påvirker finans og projektoplysninger. 

**Trin 1:** Opret og Bekræft en ny indkøbsordre for projektet for at registrere købet af en computer til $1500 og installationsservices for $150.
[![Opret en ny indkøbsordre.](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Når indkøbsordren er bekræftet, oprettes der posteringer for den bindende omkostning for projektet. 
[![Oprettede transaktioner.](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Posteringerne for den bindende omkostning vil have feltet **Posteringsgrundlag** indstillet til **Indkøbsordre**. Oprettelse og bekræftelse af en indkøbsordre opretter ikke posteringer for et projekt. 

**Trin 2:** Varer og tjenesteydelser leveres, og en produktkvittering registreres. 

Bogføring af en produktkvittering genererer og bogfører et bilag til finans. Bilaget debiteres kontoen Udgifter til indkøb, ikke-faktureret og krediteres kontoen Periodisering af køb. 
[![Posteringer på bilag.](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Bogføring af en produktkvittering vil bruge posteringsopsætningen for indkøbskategorier og produkter og ikke posteringsopsætningen til projektkategorier. Denne opsætning skal justeres for korrekt at afspejle den økonomiske virkning af købsperiodiseringer. 

Det er muligt at knytte indkøbskategorier til projektkategorier på siden **Indkøbskategori**.
[![Siden Indkøbskategori.](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Trin 3:** Opret en kladdekreditorfaktura. 

Bogføring af en produktkvittering påvirker ikke projektoplysninger. Som en løsning kan du generere en kladdekreditorfaktura lige efter bogføringen af købskvitteringen. Gå til siden **indkøbsordre** &gt; **fanen Faktura** &gt; **Generer** &gt; **Faktura**. Dette opretter et ventende fakturadokument, der opdaterer projektoplysningerne. 

Oprettelse af en kladdekreditorfaktura genererer ventende projektposteringer. 
[![Ventende projektposter.](./media/accruals8-1024x225.png)](./media/accruals8.png) 

På siden **Bindende omkostning** lukkes poster, der er oprettet i trin 1, og nye poster oprettes for at afspejle en omkostningsbinding, der kommer fra den ventende kreditorfaktura. Feltet **Posteringsgrundlag** for den bindende omkostning angives til **Kreditorfaktura**.
[![Siden Bindende omkostninger.](./media/accruals9-1024x200.png)](./media/accruals9.png)

Kreditorfakturaen forbliver i tilstanden Afventer, indtil den faktiske kreditorfaktura ankommer.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]