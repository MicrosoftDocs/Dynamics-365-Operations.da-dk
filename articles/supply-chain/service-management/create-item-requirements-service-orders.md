---
title: Oprette varebehov til serviceordrer
description: Dette emne beskriver, hvordan du opretter et varebehov for tjenesteordrer.
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75a05147883f1592b3a09e02e238661f6c20cf27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575285"
---
# <a name="create-item-requirements-for-service-orders"></a>Oprette varebehov til serviceordrer

[!include [banner](../includes/banner.md)]

Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer. Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den. Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.

Varebehov til serviceordrer behandles løbende igennem et projekt. Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt. Når du opretter et varebehov for en serviceordre, kan du få vist varebehovet i formularen **Projekter** for det valgte projekt.

## <a name="create-an-item-requirement-for-a-service-order"></a>Opret et varebehov for en serviceordre

1. Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.
1. Vælg den serviceordre, som du vil oprette et varebehov til.
1. Vælg **Varebehov** under fanen **Ekspedition** i **handlingsruden**.
1. Angiv oplysningerne til den påkrævede vare i formularen **Varebehov**. Du kan finde flere oplysninger om de forskellige felter i formularen under [Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Opret et varebehov til en serviceaftale

1. Gå til **Servicestyring** \> **Fælles** \> **Serviceaftaler** \> **Serviceaftaler**.
1. Åbn den serviceaftale, hvortil du vil oprette et varebehov.
1. I oversigtspanelet **Linjer** skal du vælge **Tilføj** for at oprette en ny linje.
1. Vælg **Care** i feltet **Transaktionstype**.
1. I feltet **Vareopsætning** skal du vælge **Varebehov**.
1. I feltet **Varenummer** skal du markere den vare, der kræves til serviceaftalen.
1. I oversigtspanelet **Linjedetaljer** under fanen **Produktdimensioner** skal du i feltet **Sted** vælge lagerstedet for varen.
1. Hvis du vil oprette en serviceordre i aftalelinjen, skal du i oversigtspanelet **Linjer** vælge **Opret serviceordrer** og derefter angive de relevante oplysninger i formularen **Opret serviceordrer**.

## <a name="see-also"></a>Se også

[Oprette serviceordrer automatisk](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
