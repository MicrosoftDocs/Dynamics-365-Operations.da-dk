---
title: Overvåge og administrere IoT-viden
description: Denne artikel forklarer, hvordan du kan overvåge og administrere IoT-viden.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a640b523adac619377e19d670f932d4d85cfb6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852412"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Overvåge og administrere IoT-viden

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du kan overvåge og administrere IoT-viden.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Overvågningsscenarier i Microsoft Dynamics 365 Supply Chain Management

Du kan overvåge IoT-viden-behandling fra flere steder:

+ **Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Beskeder** – vis listen over uløste beskeder.
+ **Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Lukkede beskeder** – vis listen over beskeder, der er blevet løst eller afvist.
+ **Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Metriske værdier** – vis de metriske værdier for tidsseriediagrammerne for **Ressourcestatus**.
+ **Moduler \> Produktionsstyring \> Produktionsudførelse \> Ressourcestatus** – spor specifikke metriske værdier ved at bruge dialogboksen **Opsætning**. Hvis et scenarie registrerer en undtagelse, vises der en besked med oplysninger om undtagelsen.
+ **Arbejdsområder \> Administration af produktion \> Beskeder** – vis en løste over uløste beskeder.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Redigere et kørende IoT-viden-scenarie

Når et scenarie kører, kan du foretage disse ændringer:

+ Tilføje nye sensorskemadefinitioner.
+ Vælge nye signaldataværdier.
+ Annullere markeringen af eksisterende signaldataværdier.
+ Tilføje og tilknyt nye signaldataværdier.
+ Opdatere tærskelværdier.

Når et scenarie kører, er disse ændringer ikke tilladt:

+ Slette eller redigere skemadefinitioner, der i øjeblikket forbruges af et aktiveret scenarie.
+ Redigere det aktiverede scenaries valgte skemastier.

## <a name="simulation-options"></a>Simuleringsindstillinger

Du kan simulere fabriksmaskinsignaler. Du kan finde flere oplysninger i disse artikler:

+ [Forbinde IoT DevKit AZ3166 til Azure IoT Hub](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Forbinde Raspberry Pi-onlinesimulator til Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
