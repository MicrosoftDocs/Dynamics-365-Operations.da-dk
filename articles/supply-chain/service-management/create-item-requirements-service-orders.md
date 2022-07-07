---
title: Oprette varebehov til serviceordrer
description: Denne artikel beskriver, hvordan du opretter et varebehov for tjenesteordrer.
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
ms.openlocfilehash: f21cda0abb334432d22cc7e0ccfdab724253d91e
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016943"
---
# <a name="create-item-requirements-for-service-orders"></a>Oprette varebehov til serviceordrer

[!include [banner](../includes/banner.md)]

Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer. Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den. Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.

Varebehov til serviceordrer behandles løbende igennem et projekt. Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt. Når du opretter et varebehov for en serviceordre, kan du få vist varebehovet i formularen **Projekter** for det valgte projekt.

## <a name="create-an-item-requirement-for-a-service-order"></a>Opret et varebehov for en serviceordre

1. Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.
1. Vælg den serviceordre, som du vil oprette et varebehov til.
1. Vælg **Varebehov** under fanen **Ekspedition** i **handlingsruden**.
1. Angiv oplysningerne til den påkrævede vare i formularen **Varebehov**. Du kan finde flere oplysninger om de forskellige felter i formularen under [Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Opret et varebehov til en serviceaftale

1. Gå til **Servicestyring** \> **Serviceaftaler** \> **Serviceaftaler**.
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
