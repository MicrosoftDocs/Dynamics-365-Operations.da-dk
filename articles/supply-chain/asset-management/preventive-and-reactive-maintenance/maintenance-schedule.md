---
title: Vedligeholdelsestidsplan
description: I dette emne beskrives vedligeholdelsestidsplaner i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d235a3797b1acee9c92c3d81e8b4a20e1f7c5c75
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017943"
---
# <a name="maintenance-schedule"></a>Vedligeholdelsestidsplan

[!include [banner](../../includes/banner.md)]

 

Vedligeholdelsestidsplanen indeholder en liste over alle de forventede forebyggende vedligeholdelsesplaner, vedligeholdelsesanmodninger og vedligeholdelsesrunder, der skal udføres. Nogle tidsplanslinjer kan være blevet konverteret til arbejdsordrer.

De fire visninger for vedligeholdelsestidsplanen er lidt forskellige, afhængigt af hvilke vedligeholdelsestidsplanlinjer du vil have vist.

| Menupunkt                  | Indholdsbeskrivelse                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hele vedligeholdelsestidsplanen       | Alle vedligeholdelsestidsplanslinjer vises.     |
| Min aktivtidsplan        | Alle vedligeholdelsestidsplanslinjer, der indeholder aktiver, som er installeret på arbejdssteder, som du er relateret til som arbejder (konfigureret i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md)), vises på denne liste. |
| Åbn vedligeholdelsestidsplanslinjer | Vedligeholdelsestidsplanslinjer med status "Oprettet" - det vil sige, at de endnu ikke er blevet konverteret til en arbejdsordre eller slettet - vises på denne liste.                                            |
| Åbn vedligeholdelsestidsplanspuljer | Vedligeholdelsestidsplanslinjer, der er relateret til en arbejdsordrepulje, vises på denne liste.                                                                                                                  |

>[!NOTE]
>Hvis en vedligeholdelsestidsplanlinje er medtaget i flere arbejdsordrepuljer (referer til [Arbejdsordrepuljer](../work-orders/work-order-pools.md)), vises der én post for hver pulje i **Åbne vedligeholdelsestidsplanspuljer**. Dette gøres for at optimere filtreringsindstillinger i arbejdsordrepuljer.

Sådan åbnes en vedligeholdelsestidsplan:

1. Klik på **Styring af aktiver** > **Generelt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.

2. Hvis du vil opdatere vedligeholdelsesplanen, skal du klikke på **Vedligeholdelsesplan** eller **Vedligeholdelsesrunder**. 

3. Du kan redigere en vedligeholdelsesplanlinje ved at markere den og klikke på **Rediger**. Du kan f.eks. nemt opdatere serviceniveauet eller den arbejder, der er ansvarlig for jobbet. Du kan kun redigere de vedligeholdelsestidsplanslinjer, der endnu ikke er knyttet til en arbejdsordre.

4. Du kan slette en vedligeholdelsestidsplanslinje ved at vælge den på listesiden og klikke på **Slet**.

5. Du kan kassere en vedligeholdelsestidsplanslinje ved at vælge den på listesiden og klikke på **Kassér**. Denne funktion er nyttig, hvis et aktiv f.eks. har en vedligeholdelsesplan på 2.000 km og en vedligeholdelsesplan på 10.000 km. Du kan derefter vælge at kassere den linje, der er oprettet fra vedligeholdelsesplanen for 2.000 km, når den falder sammen med 10.000 km, 20.000 km, 30.000 km osv. Hvis du sletter en vedligeholdelsestidsplanslinje, der er relateret til en vedligeholdelsesplan, vises den pågældende linje aldrig igen, når vedligeholdelsesplanen er planlagt.

6. Du kan vælge et antal vedligeholdelsestidsplanslinjer i **Alle vedligeholdelsestidsplaner** og klikke på **Arbejdsordrepulje**, hvis alle valgte linjer skal medtages i den samme arbejdsordrepulje.

7. Du kan vælge et antal vedligeholdelsestidsplanlinjer i **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer** og klikke på **Juster tidsplan**, hvis du vil foretage de samme reguleringer på flere linjer. Du kan ændre de forventede start- og slutdatoer, serviceniveauet og den ansvarlige vedligeholdelsesarbejdergruppe eller den ansvarlige vedligeholdelsesarbejder, der er relateret til de valgte vedligeholdelsestidsplanslinjer.

- Når en vedligeholdelsestidsplanslinje er relateret til en arbejdsordre, vises arbejdsordre-id'et i feltet **Arbejdsordre**.  
- I detaljevisningen **Alle aktiver** > oversigtspanelet **Vedligeholdelsesplaner for aktiver** kan du vælge vedligeholdelsesplaner for aktivet. Hvis du senere hen sletter en vedligeholdelsesplanlinje, der er relateret til et aktiv i **Alle aktiver**, sletter du også automatisk alle vedligeholdelsestidsplanlinjer med statussen "Oprettet", der er oprettet på baggrund af den pågældende vedligeholdelsesplan. Se også [Oprette et aktiv](../objects/create-an-object.md).

I illustrationen nedenfor vises listesiden **Hele vedligeholdelsestidsplanen**.

![Figur 1](media/16-preventive-maintenance.png)

