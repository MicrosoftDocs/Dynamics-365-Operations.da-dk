---
title: Oprette varebehov til serviceordrer
description: Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b342b20cc11addc53fc6ea4e1a23d3b449eb9ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257935"
---
# <a name="create-item-requirements-for-service-orders"></a>Oprette varebehov til serviceordrer 

[!include [banner](../includes/banner.md)]


Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer. Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den. Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.

Varebehov til serviceordrer behandles løbende igennem et projekt. Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt. Når du opretter et varebehov for en serviceordre, kan du få vist varebehovet i formularen **Projekter** for det valgte projekt.

## <a name="create-an-item-requirement-for-a-service-order"></a>Opret et varebehov for en serviceordre

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Vælg den serviceordre, som du vil oprette et varebehov til.

3.  Klik på **Varebehov** under fanen **Ekspedition** i **handlingsruden**.

4.  Angiv oplysningerne til den påkrævede vare i formularen **Varebehov**. Du kan finde flere oplysninger om de forskellige felter i formularen under [Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Opret et varebehov til en serviceaftale

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.

2.  Åbn den serviceaftale, hvortil du vil oprette et varebehov.

3.  I oversigtspanelet **Linjer** skal du klikke på **Tilføj** for at oprette en ny linje.

4.  Vælg **Care** i feltet **Transaktionstype**.

5.  I feltet **Vareopsætning** skal du vælge **Varebehov**.

6.  I feltet **Varenummer** skal du markere den vare, der kræves til serviceaftalen.

7.  I oversigtspanelet **Linjedetaljer** under fanen **Produktdimensioner** skal du i feltet **Sted** vælge lagerstedet for varen.

8.  Hvis du vil oprette en serviceordre i aftalelinjen, skal du i oversigtspanelet **Linjer** klikke på **Opret serviceordrer** og derefter angive de relevante oplysninger i formularen **Opret serviceordrer**. 


## <a name="see-also"></a>Se også

[Oprette serviceordrer automatisk](create-service-orders-automatically.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]