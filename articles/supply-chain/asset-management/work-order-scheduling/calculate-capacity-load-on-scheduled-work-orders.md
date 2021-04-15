---
title: Beregne kapacitetsbelastning på planlagte arbejdsordrer
description: Dette emne forklarer, hvordan kapacitetsbelastningen beregnes for planlagte arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09e0fc17a288a278b7b1feaba8c7b73425aa2d52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808154"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]