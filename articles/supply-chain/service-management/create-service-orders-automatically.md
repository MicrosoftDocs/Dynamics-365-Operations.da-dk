---
title: Oprette serviceordrer automatisk
description: Du kan oprette serviceordrer for én serviceaftale eller flere serviceaftaler.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014688"
---
# <a name="create-service-orders-automatically"></a>Oprette serviceordrer automatisk    

[!include [banner](../includes/banner.md)]


Du kan oprette serviceordrer for én serviceaftale eller flere serviceaftaler. Når de er oprettet, kan du få vist dine serviceaftaler i formularen **Serviceordrer**.

Serviceordrer kan kun oprettes for den gyldighedsperiode, der er defineret i serviceaftalen. Hvis du definerer et tidsrum i formularen **Opret serviceordrer**, der begynder før startdatoen eller slutter efter slutdatoen for serviceaftalen, oprettes serviceordrerne kun for den del af tidsrummet, der ligger inden for serviceaftalens datoer.

Når du opretter serviceordrer manuelt eller automatisk fra serviceaftalelinjen, skal serviceordren ligge inden for det tidsinterval, der er angivet ved start- og slutdatoerne for linjen, medmindre du ikke angiver en slutdato på linjen.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Oprette serviceordrer for en serviceaftale automatisk

1.  Klik på **Servicestyring** \> **Serviceaftaler** \> **Serviceaftaler**.

2.  Vælg en serviceaftale.

3.  Klik på fanen **Levér**, og klik derefter på **Planlagte serviceordrer**.

4.  Angiv datoerne i felterne **Fra dato** og **Til dato** for at definere serviceperioden.

5.  Markér afkrydsningsfeltet **Vis infolog** for at få vist en liste over de serviceordrer, der er oprettet.

6.  Vælg transaktionstyperne i feltgruppen **Medtag posteringstyper**. Transaktionstyperne er de linjer, der oprettes i en serviceaftale, og hver af de transaktionstyper, du vælger, genererer flere serviceordrer ud fra den serviceperiode, der er angivet i serviceaftalelinjen.

7.  Markér afkrydsningsfeltet **Fortløbende**, hvis du vil oprette serviceordrer, der mangler i en fortløbende serie af serviceaftaler.

8.  Klik på **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Oprette serviceordrer automatisk for flere serviceaftaler

1.  Klik på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Opret serviceordrer**.

2.  Klik på **Vælg** for at tilføje eller fjerne kriterier, som bruges til at oprette serviceordrer.

3.  Klik på **OK**.

## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Oprette serviceordrer automatisk](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]