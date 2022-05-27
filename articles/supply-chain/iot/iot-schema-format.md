---
title: Skemaformater for IoT Hub-meddelelser
description: Dette emne forklarer, hvordan du designer et meddelelsesskema, som du kan bruge i IoT-intelligens.
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
ms.openlocfilehash: 60d5bc4eacdd7e7d713490998bd1d20c9271ad02
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673936"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Skemaformater for IoT Hub-meddelelser

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du designer et meddelelsesskema, som du kan bruge i IoT-intelligens.

## <a name="message-requirements"></a>Meddelelseskrav

Der gælder følgende regler for overvågning af meddelelser i IoT-intelligens:

+ Meddelelsesskemaer skal være i formatet JavaScript Object Notation (JSON).
+ En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Microsoft Azure IoT Hub-meddelelsen.
+ En meddelelse spores kun, hvis den indeholder alle de egenskaber, der er defineret i opsætningen af scenariet. Hvis du f.eks. definerer egenskaberne **id**, **tidsstempel** og **værdi**, overvåges følgende meddelelse.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Denne meddelelse overvåges ikke, fordi egenskaben **værdi** mangler.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-intelligens ignorerer egenskaberne i den meddelelse, der ikke defineres i scenariekonfigurationen. Hvis du f.eks. definerer egenskaberne **id**, **tidsstempel** og **værdi**, overvåger IoT-intelligens alle følgende meddelelser.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-intelligens ignorerer uovervåget meddelelser, der ikke svarer til scenariekonfigurationens kriterier.
+ Du kan definere og bruge flere typer meddelelsesskemaer.
+ Ikke alle typer meddelelsesskemaer skal defineres. Der skal kun defineres skemaer, der skal bruges til IoT-intelligensscenarier.

## <a name="id-value-pair-schema"></a>Id-værdiparskema

Et id-værdipar er et fælles mønster for meddelelsesskemaer til IoT-intelligens. Ved at bruge et id-værdipar sikrer du, at meddelelsesskemaet er det samme i alle scenarier. Her er f.eks. en meddelelse til scenariet **Nedetid for udstyr** eller **Produktionsforsinkelser**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Her er en meddelelse til scenariet **Produktkvalitet**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Begge ovenstående meddelelser indeholder **id**- og **værdi**-egenskaber. **Id**-værdierne kan tilknyttes i tabellen **Signaldataværdier** under opsætning af scenarier. Til scenariet **Nedetid for udstyr** skal du tilknytte værdien **IoTInt.Machine1225.PartOut**. Til scenariet **Produktkvalitet** skal du tilknytte værdien **IoTInt.Machine1225.Temperature**.

Du kan finde flere oplysninger i [dokumentationen til Azure IoT Hub](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]