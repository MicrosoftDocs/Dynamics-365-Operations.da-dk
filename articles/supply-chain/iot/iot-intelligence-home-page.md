---
title: Startside for IoT-intelligens
description: Denne artikel indeholder links til oplysninger om IoT-intelligens.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8b2be25abaeff7404d7f4ef3cd825a50147fef
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228351"
---
# <a name="iot-intelligence-home-page"></a>Startside for IoT-intelligens

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

> [!IMPORTANT]
> Denne funktion er aktuelt kun tilgængelig i følgende lande/områder:
>
> - USA (Amerikas Forenede Stater)
> - EU (Europæiske Union)
> - AU (Australien)
> - CA (Canada)
> - UK (Storbritannien)

IoT-intelligens er et tilføjelsesprogrammet til Microsoft Dynamics 365 Supply Chain Management. Det integrerer IoT-signaler (Tingenes internet) med data i Supply Chain Management for at producere handlingsbar indsigt.

IoT-intelligens understøtter følgende scenarier:

- **Produktionsforsinkelser** – I dette scenario sammenlignes faktisk cyklustid med den planlagte cyklustid. Supply Chain Management giver dig besked, når produktionen ikke kærer efter planen, så du kan maksimere driftseffektivitet og undgå ordreforsinkelser.
- **Nedetid for udstyr** – I dette scenarie sammenlignes målt oppetid med brugerdefinerede parametre. Supply Chain Management giver dig besked, når en nedetidsgrænse overskrides, så du kan udføre handlinger som f.eks. at ændre planlægningen af en produktionsordre eller oprette en arbejdsordre til vedligeholdelse.
- **Produktkvalitet** – I dette scenario sammenlignes føleraflæsninger som f.eks. fugtighed og temperatur med brugerdefinerede kvalitetsmålepunkter. Supply Chain Management giver dig besked, når der indtræffer en afvigelse, så du kan gribe ind og bevare kvalitetsstandarderne og minimere spild.

Følgende illustration viser interaktionen mellem Azure IoT Hub, IoT-intelligens og Supply Chain Management.

![IoT Hub, IoT-intelligens og Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Sporing og vedligeholdelse

- [Overvågningsscenarier i Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Deaktivere et scenarie](iot-scenario-setup.md#disable-a-scenario)
- [Redigere et kørende IoT-viden-scenarie](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simuleringsindstillinger](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]