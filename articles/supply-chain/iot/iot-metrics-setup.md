---
title: Konfigurere målepunkter til IoT-intelligens
description: Denne artikel forklarer, hvordan du kan konfigurere målepunkter til IoT-intelligens.
author: johanhoffmann
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 147df50a9d0baf78f2efc3e57b2cda935e38cee3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882686"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Konfigurere målepunkter til IoT-intelligens

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Konfigurer målepunkter

Hvis du vil have vist tidsseriediagrammerne for dine meddelelser i Microsoft Dynamics 365 Supply Chain Management, skal du konfigurere målepunkter ved at følge disse trin.

1. Kopiér forbindelsesstrengen for Redis-cachen:

    1. Gå til Redis-cachen i Azure-portalen.
    2. Gå til **Indstillinger** \> **Adgangsnøgler**.
    3. Kopiér værdien i feltet **Primær forbindelsesstreng**.

2. I Supply Chain Management skal du gå til **Produktionsstyring \> Konfiguration \> IoT-intelligens \> Scenarieparametre**.
3. På siden **Scenarieparametre** skal du indsætte den forbindelsesstreng, du kopierede tidligere, i feltet **Renis-forbindelsesstreng til metrikværdilager** under fanen **Tidsserie**. Dette trin gør det muligt at visualisere målepunkter fra Azure IoT Hub i Supply Chain Management. Når du indsætter værdien i feltet, vises den som **\*\*\*\*\*\***.

    > [!NOTE]
    > Når du opdaterer forbindelsesstrengen til Redis-cachen, skal du også opdatere dette felt.

4. Gå til **Produktionsstyring \> Forespørgsler og rapporter \> IoT-intelligens \> Metriske nøgler**.
5. Vælg **Opdater** på siden **Metriske nøgler**.
6. Bemærk, at der er valgt **Kør i baggrunden** i feltet i dialogboksen **Opdater metriske nøgler**. Vælg **OK**.

Alle metriske nøgler i Redis-cachen hentes og føjes til listen over **Metriske nøgler**. Metrikværdier vises først, når du har [aktiveret scenarierne](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Konfigurere tidsserien for ressourcestatus

Benyt følgende fremgangsmåde for at konfigurere tidsserien **Ressourcestatus**.

1. I Supply Chain Management skal du gå til **Produktionsstyring \> Produktionsudførelse \> Ressourcestatus**.
2. På siden **Ressourcestatus** skal du vælge **Konfigurer**.
2. Vælg et element, der skal overvåges, på listen **Ressource** i dialogboksen **Konfigurer**.
3. Vælg knappen **Rediger** for **Tidsserie 1**.
4. Vælg en metrikværdi i gitteret i dialogboksen **Vælg tidsserie**. (Du kan også bruge linket **Opdater metriske nøgler** for at opdatere de metriske nøgler fra denne dialogboks.)
5. Vælg **OK** for at vende tilbage til dialogboksen **Konfigurer**.
6. Angiv et vist navn.
7. Vælg en tidsramme i feltet **Vis data fra**.
8. Vælg **OK**.

Diagrammet vises.

## <a name="delete-a-metric-key"></a>Slette en metrisk nøgle

1. Gå i Supply Chain Management til **Produktionsstyring \> Forespørgsler og rapporter \> IoT-intelligens \> Metriske nøgler**.
2. Vælg den metriske nøgle, der skal slettes, på siden **Metriske nøgler**.
3. Vælg **Slet**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]