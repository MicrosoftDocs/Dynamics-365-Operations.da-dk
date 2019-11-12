---
title: Beregne kapacitetsbelastning på planlagte arbejdsordrer
description: Dette emne forklarer, hvordan kapacitetsbelastningen beregnes for planlagte arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d7684d1a4f78c95ebc7fd0a88f1c7dc7fead0303
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652097"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Beregne kapacitetsbelastning på planlagte arbejdsordrer

[!include [banner](../../includes/banner.md)]

 

Du kan beregne kapacitetsbelastningen for planlagte arbejdsordrer for at få overblik over arbejdsbelastningen for ressourcer i en bestemt periode. Der kan foretage beregninger for følgende ressourcer: vedligeholdelsesarbejdere, arbejdergrupper, værktøjer og aktiver.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Plan** > **Kapacitetsbelastning**.

2. I dialogboksen **Beregn kapacitetsbelastning** > feltet **Vis** skal du vælge den belastningstype, du vil beregne: **Kapacitet**, **Reserveret** eller **Rest**.

3. Vælg **Ja** på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater, der indeholder nul.

4. Vælg de ressourcetyper, som du vil beregne kapacitetsbelastning for, ved at vælge **Ja** i de relevante til/fra-knapper: **Arbejder**, **Vedligeholdelsesarbejdergruppe**, **Værktøj** og **Aktiv**.

5. Vælg startdatoen for beregningen i feltet **Fra-dato**.

6. I feltet **Intervaltype** skal du vælge intervallet for beregningen: **Dag**, **Uge**, **Måned** eller **Kvartal**.

7. Indsæt det antal intervaller, du vil beregne, i feltet **Periodefrekvens**. Hvis du f.eks. har valgt **Dag** som intervaltype, og du indsætter tallet "5" i dette felt, foretages der en beregning på fem dage fra startdatoen.

8. Klik på **OK** for at starte beregningen.

I figuren herunder vises resultatet af en beregning, der dækker tre uger for belastningstypen **Reserveret**.

![Figur 1](media/08-work-order-scheduling.png)

[!NOTE]
Hvis du vælger belastningstyperne **Kapacitet** eller **Rest** for beregningen, vises samme resultat, hvis der ikke er foretaget reservationer for ressourcerne i den valgte periode.

Se [Beregne kapacitetsbelastning](../capacity-planning/calculate-capacity-load.md) for at få oplysninger om, hvordan kapacitetsbelastningen beregnes på vedligeholdelsestidsplanslinjer og ikke planlagte arbejdsordrer.

