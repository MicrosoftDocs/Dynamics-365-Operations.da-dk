---
title: Overvåge og administrere IoT-viden
description: Dette emne forklarer, hvordan du kan overvåge og administrere IoT-viden.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386496"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Overvåge og administrere IoT-viden

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du kan overvåge og administrere IoT-viden.

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

Du kan simulere fabriksmaskinsignaler. Du kan finde flere oplysninger i disse emner:

+ [Forbinde IoT DevKit AZ3166 til Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Forbinde Raspberry Pi-onlinesimulator til Azure IoT Hub (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Oversigt over løsningsaccelerator til enhedsimuleringer](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
