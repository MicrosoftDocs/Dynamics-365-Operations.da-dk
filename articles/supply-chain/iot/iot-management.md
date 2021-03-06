---
title: Overvåge og administrere IoT-viden
description: Dette emne forklarer, hvordan du kan overvåge og administrere IoT-viden.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86e20b9e60e890833c0eb8573e92c0fbb27f8c9a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908413"
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

+ [Forbinde IoT DevKit AZ3166 til Azure IoT Hub](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Forbinde Raspberry Pi-onlinesimulator til Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Oversigt over løsningsaccelerator til enhedsimuleringer](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]