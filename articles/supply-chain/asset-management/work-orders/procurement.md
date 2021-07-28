---
title: Indkøb
description: I dette emne beskrives indkøb i Styring af aktiver.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3e01dd85cbe8e2b2c9095431f3e0aead817a5a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352756"
---
# <a name="procurement"></a>Indkøb

[!include [banner](../../includes/banner.md)]

I Styring af aktiver kan du få vist en oversigt over indkøbsrekvisitioner og indkøbsordrer, der er relateret til arbejdsordrer. Det er også muligt at oprette en indkøbsordre eller en indkøbsrekvisition fra en arbejdsordre.

På listen **Indkøbsrekvisition i arbejdsordre** (**Styring af aktiver** > **Almindelig** > **Indkøb** > **Indkøbsrekvisition i arbejdsordre**) kan du se en liste over indkøbsrekvisitioner, der er relateret til arbejdsordrer. Når du vælger et arbejdsordrejob på denne side, kan du bruge knapperne i gruppen **Vis** under fanen **Indkøbsrekvisition for arbejdsordre** i handlingsruden til at udføre forskellige handlinger:

- Hvis du vil åbne den relaterede indkøbsrekvisition, skal du vælge **Indkøbsrekvisition**. 
- Hvis du vil åbne den relaterede arbejdsordre , skal du vælge **Arbejdsordre**.
- Hvis du vil have en oversigt over, hvor varen på den valgte linje bruges i relation til aktiver,typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer i Styring af aktiver, skal du vælge **Hvor er varen brugt?**. Yderligere oplysninger om denne oversigt finder du under [Hvor er varen brugt?](../controlling-and-reporting/item-where-used.md).

I illustrationen herunder vises et eksempel på listesiden **Indkøbsrekvisition for arbejdsordre**.

![Figur 1.](media/08-work-orders.png)


På listesiden **Indkøbsrekvisition i arbejdsordre** (**Styring af aktiver** > **Almindelig** > **Indkøb** > **Indkøbsrekvisition i arbejdsordre**) kan du se en liste over indkøbsordrer, der er relateret til arbejdsordrer. Når du vælger et arbejdsordrejob på denne side, kan du bruge knapperne i gruppen **Vis** under fanen **Arbejdsordreindkøb** i handlingsruden til at udføre forskellige handlinger:

- Hvis du vil åbne den relaterede indkøbsordre, skal du vælge **Indkøbsordre**. 
- Hvis du vil åbne den relaterede arbejdsordre , skal du vælge **Arbejdsordre**.
- Hvis du vil have en oversigt over, hvor varen på den valgte linje bruges i relation til aktiver,typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer i Styring af aktiver, skal du vælge **Hvor er varen brugt?**. Yderligere oplysninger om denne oversigt finder du under [Hvor er varen brugt?](../controlling-and-reporting/item-where-used.md).

I illustrationen herunder vises et eksempel på listesiden **Arbejdsordreindkøb**.

![Figur 2.](media/09-work-orders.png)


Der vises et symbol, der er relateret til leveringsdatokontrol, i højre side af hver linje på både listesiden **Arbejdsordreindkøb** og **Indkøbsrekvisition for arbejdsordre**. Hvis der vises et udråbstegn i en rød cirkel på symbolet, betyder det, at leveringen af den relaterede indkøbsrekvisition eller indkøbsordre kan være forsinket.

I forbindelse med en indkøbsordre bruges den dato, der er knyttet til indkøbsordrelinjen, til beregning af en mulig forsinkelse. Hvis du vil have vist denne dato, skal du vælge indkøbsordrelinjen på siden **Indkøbsordre**. Datoen vises i feltet **Bekræftet leveringsdato** under fanen **Opsætning** i oversigtspanelet **Linjedetaljer**. Hvis feltet **Bekræftet leveringsdato** ikke er angivet, bruges datoen i feltet **Leveringsdato** i oversigtspanelet **Indkøbsordrehoved** til beregningen. En af disse datoer sammenlignes med den tilgængelige dato på arbejdsordren eller arbejdsordrejobbet i denne rækkefølge:

1. Faktisk startdato på arbejdsordren  

2. Planlagt startdato for det relaterede arbejdsordrejob 

3. Planlagt startdato på arbejdsordren 

4. Forventet startdato på arbejdsordren 

Foren indkøbsrekvisition findes den dato, der bruges til at beregne en mulig forsinkelse, i feltet **Ønsket dato** i oversigtspanelet **Indkøbsrekvisitionshoved** på siden **Indkøbsrekvisitioner**. Datoen i dette felt sammenlignes med den tilgængelige dato på arbejdsordren eller arbejdsordrejobbet i samme rækkefølge som for en indkøbsordre.


## <a name="create-a-purchase-order-from-a-work-order"></a>Oprette en indkøbsordre ud fra en arbejdsordre

På listesiden **Alle arbejdsordrer** kan du vælge et job i en arbejdsordre og oprette en relateret indkøbsordre eller indkøbsrekvisition. Det er med til at sikre, at der findes projektrelationer mellem indkøbsordren eller indkøbsrekvisitionen og arbejdsordren.

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil oprette en indkøbsordre for, og vælg derefter **Rediger**.

3. I oversigtspanelet **Vedligeholdelsesjob for arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette indkøbsordren for.

4. Vælg **Vareopgaver** > **Indkøbsordre fra arbejdsordrejob**.

5. Klik på **Ny** på listesiden **Projektindkøbsordrer**.

6. Opret indkøbsordren.

>[!NOTE]
>Hvis du vil oprette en relateret indkøbsrekvisition, skal du følge samme fremgangsmåde. Du skal dog vælge **Vareopgaver** > **Indkøbsrekvisition fra arbejdsordrejob** i trin 4.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projektrelation mellem en arbejdsordre og indkøbsordre eller indkøbsrekvisition

En indkøbsordrelinje eller indkøbsrekvisitionslinje er relateret til et job i en arbejdsordre via arbejdsordreprojektet og det relaterede projektaktivitetsnummer. Når du opretter en indkøbsordre eller en indkøbsrekvisition fra et arbejdsordrejob, er det relaterede projektaktivitetsnummer obligatorisk. Projektaktivitetsnummeret indsættes automatisk på indkøbsordren eller indkøbsrekvisitionen, hvis alle arbejdsordrejob i den relaterede arbejdsordre bruger samme vedligeholdelsesjobtype. Du skal indtaste projektaktivitetsnummeret manuelt på indkøbsordren eller indkøbsrekvisitionen, hvis arbejdsordrejobbene har forskellige vedligeholdelsesjobtyper.

Hvis du vil se eller angive det aktivitetsnummer, der er knyttet til en indkøbsordrelinje, skal du vælge indkøbsordreposten på siden **Arbejdsordreindkøb** og derefter vælge linket for indkøbsordren i kolonnen **Indkøbsordre**. Du kan finde feltet **Aktivitetsnummer** under fanen **Projekt** i oversigtspanelet **Linjedetaljer**.

I illustrationen nedenfor vises et eksempel på siden **Indkøbsordre** med fokus på **Aktivitetsnummeret**.

![Figur 3.](media/10-work-orders.png)

Hvis du vil se eller angive det aktivitetsnummer, der er knyttet til en indkøbsordres indkøbsrekvisition, skal du vælge indkøbsrekvisitionsposten på siden **Indkøbsrekvisition for arbejdsordre** og derefter vælge linket for indkøbsrekvisitionen i kolonnen **Indkøbsrekvisition**. Du kan finde feltet **Aktivitetsnummer** under fanen **Projekt** i oversigtspanelet **Linjedetaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]