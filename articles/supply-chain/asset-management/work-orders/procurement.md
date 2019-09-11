---
title: Indkøb
description: I dette emne beskrives indkøb i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875565"
---
# <a name="procurement"></a>Indkøb


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Styring af aktiver kan du få vist en oversigt over indkøbsrekvisitioner og indkøbsordrer, der er relateret til arbejdsordrer. Det er også muligt at oprette en indkøbsordre eller en indkøbsrekvisition fra en arbejdsordre.

På listen **Indkøbsrekvisition i arbejdsordre** (**Styring af aktiver** > **Almindelig** > **Indkøb** > **Indkøbsrekvisition i arbejdsordre**) kan du se en liste over indkøbsrekvisitioner, der er relateret til arbejdsordrer.

- Vælg et arbejdsordrejob på listen **Indkøbsrekvisition i arbejdsordre**, og klik på knappen **Indkøbsrekvisition** for at åbne den relaterede indkøbsrekvisition.  
- Vælg et arbejdsordrejob på listen **Indkøbsrekvisition i arbejdsordre**, og klik på knappen **Arbejdsordre** for at åbne den relaterede arbejdsordre.  
- Vælg et arbejdsordrejob på listen **Indkøbsrekvisition i arbejdsordre**, og klik på knappen **Hvor er varen brugt?**, hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges i relation til aktiver, typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer. 

![Figur 1](media/08-work-orders.png)


På listen **Indkøb i arbejdsordre** (**Styring af virksomhedsaktiv** > **Almindelig** > **Indkøb** > **Indkøb i arbejdsordre**) kan du se en liste over indkøbsordrer, der er relateret til arbejdsordrer.

- Vælg et arbejdsordrejob på listen **Indkøbsrekvisition i arbejdsordre**, og klik på knappen **Indkøbsordre** for at åbne den relaterede indkøbsordre.  
- Vælg et arbejdsordrejob på listen **Indkøb i arbejdsordre**, og klik på knappen **Arbejdsordre** for at åbne den relaterede arbejdsordre.  
- Vælg et arbejdsordrejob på listen **Arbejdsordre**, og klik på knappen **Hvor er varen brugt?**, hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges i relation til aktiver, typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer. 

![Figur 2](media/09-work-orders.png)


På ovennævnte lister findes der et ikon for kontrol af leveringsdato til højre på hver linje. Hvis der vises et udråbstegn i en rød cirkel på ikonet, betyder det, at leveringen på den relaterede indkøbsrekvisition eller indkøbsordre kan være forsinket.

På en indkøbsrekvisition findes den dato, der bruges til at beregne en mulig forsinkelse, i formularen **Indkøbsrekvisitioner** > oversigtspanelet **Indkøbsrekvisitionshoved** > **Ønsket dato**. Denne dato sammenlignes med den tilgængelige dato på arbejdsordren eller arbejdsordrejobbet på samme måde som indkøbsordredatoen.

På en indkøbsordre er den dato, der bruges til beregning af en mulig forsinkelse, den dato, der er relateret til indkøbsordrelinjen, som vises i formularen **Indkøbsordre** > vælg indkøbsordrelinje > oversigtspanelet **Linjedetaljer** > fanen **Opsætning** > **Bekræftet leveringsdato**. Hvis dette felt ikke udfyldes, bruges datoen i feltet **Leveringsdato** i oversigtspanelet **Indkøbsordrehoved**. En af disse datoer sammenlignes med den tilgængelige dato på arbejdsordren eller arbejdsordrejobbet i denne rækkefølge:

- Faktisk startdato på arbejdsordren eller  

- Planlagt startdato for det relaterede arbejdsordrejob eller  

- Planlagt startdato på arbejdsordren eller  

- Forventet startdato på arbejdsordren  


## <a name="create-purchase-order-from-a-work-order"></a>Oprette indkøbsordre fra en arbejdsordre

I **Alle arbejdsordrer** skal du vælge et job i en arbejdsordre og oprette en relateret indkøbsordre eller en indkøbsrekvisition. Dette gøres for at sikre projektrelationer mellem indkøbsordren eller indkøbsrekvisitionen og arbejdsordren.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil oprette en indkøbsordre for, på listen **Alle arbejdsordrer** eller **Aktive arbejdsordrer**, og klik på **Rediger**.

3. I formularen **Arbejdsordre** > oversigtspanelet **Vedligeholdelsesjob for arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette indkøbsordren for.

4. Klik på **Vareopgaver** > **Indkøbsordre fra arbejdsordrejob**.

5. Klik på **Ny** på listesiden **Projektindkøbsordrer**.

6. Opret indkøbsordren.

>[!NOTE]
>Oprettelse af en indkøbsrekvisition er næsten identisk med oprettelse af en indkøbsordre. Den eneste forskel er, at du i ovenstående procedure skal klikke på **Vareopgaver** > **Indkøbsrekvisition fra arbejdsordrejob** i trin 2.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projektrelation mellem en arbejdsordre og indkøbsordre eller indkøbsrekvisition

En indkøbsordrelinje eller indkøbsrekvisitionslinje er relateret til et job i en arbejdsordre via arbejdsordreprojektet og det relaterede projektaktivitetsnummer. Når du opretter en indkøbsordre eller en indkøbsrekvisition fra et arbejdsordrejob, er det relaterede projektaktivitetsnummer obligatorisk. Projektaktivitetsnummeret indsættes automatisk på en indkøbsordre eller indkøbsrekvisition, hvis den relaterede arbejdsordre indeholder arbejdsordrejob, der alle bruger samme vedligeholdelsesjobtype. Hvis arbejdsordrejobbene indeholder forskellige vedligeholdelsesjobtyper, skal projektaktivitetsnummeret indsættes manuelt.

Hvis du vil have vist eller indsætte det aktivitetsnummer, der er knyttet til en indkøbsordrelinje, skal du åbne **Indkøb i arbejdsordre** > vælge indkøbsordreposten > klikke på indkøbsordren i kolonnen **Indkøbsordre** > oversigtspanelet **Linjedetaljer** > fanen **Projekt** > feltet **Aktivitetsnummer**.


![Figur 3](media/10-work-orders.png)


Hvis du vil have vist eller indsætte det aktivitetsnummer, der er knyttet til en indkøbsrekvisition for en arbejdsordrelinje, skal du åbne **Indkøbsrekvisition i arbejdsordre** > vælge indkøbsrekvisitionsposten > klikke på indkøbsrekvisitionen i kolonnen **Indkøbsrekvisition** > oversigtspanelet **Linjedetaljer** > fanen **Projekt** > feltet **Aktivitetsnummer**.

