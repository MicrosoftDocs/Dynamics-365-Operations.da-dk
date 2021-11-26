---
title: Startside for IoT-intelligens
description: Dette emne indeholder links til oplysninger om IoT-intelligens.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782675"
---
# <a name="iot-intelligence-home-page"></a>Startside for IoT-intelligens

[!include [banner](../../includes/banner.md)]

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

+ **Produktionsforsinkelser** – I dette scenario sammenlignes faktisk cyklustid med den planlagte cyklustid. Supply Chain Management giver dig besked, når produktionen ikke kærer efter planen, så du kan maksimere driftseffektivitet og undgå ordreforsinkelser.
+ **Nedetid for udstyr** – I dette scenarie sammenlignes målt oppetid med brugerdefinerede parametre. Supply Chain Management giver dig besked, når en nedetidsgrænse overskrides, så du kan udføre handlinger som f.eks. at ændre planlægningen af en produktionsordre eller oprette en arbejdsordre til vedligeholdelse.
+ **Produktkvalitet** – I dette scenario sammenlignes føleraflæsninger som f.eks. fugtighed og temperatur med brugerdefinerede kvalitetsmålepunkter. Supply Chain Management giver dig besked, når der indtræffer en afvigelse, så du kan gribe ind og bevare kvalitetsstandarderne og minimere spild.

Følgende illustration viser interaktionen mellem Azure IoT Hub, IoT-intelligens og Supply Chain Management.

![IoT Hub, IoT-intelligens og Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Konfiguration

Du kan opsætte og konfigurere IoT-intelligens uden at skrive nogen kode. Her er de grundlæggende trin.

1. [Konfigurer Azure-ressourcer](iot-azure-setup.md) – Opret en IoT Hub, en Redis Cache og en Key Vault, der kan åbnes fra Supply Chain Management.
2. [Meddelelsesskemaformater for IoT Hub](iot-schema-format.md) – Konfigurer dine enheder til at sende meddelelser til IoT Hub, og definer meddelelsesformatet JSON (JavaScript Object Notation).
3. I funktionsstyring skal du aktivere flaget for funktionen IoT-intelligens. 
4. [Installer IoT-intelligens-tilføjelsesprogrammet i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Installer tilføjelsesprogrammet i LCS, og konfigurer Azure-hemmeligheder.
5. [Konfigurer målepunkter](iot-metrics-setup.md) – Konfigurer målepunkter i Supply Chain Management.
6. [Opsætning af scenarie](iot-scenario-setup.md) – Konfigurer scenarierne i Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Sporing og vedligeholdelse

+ [Overvågningsscenarier i Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Deaktivere et scenarie](iot-scenario-setup.md#disable-a-scenario)
+ [Fjern tilføjelsesprogrammet](iot-lcs-setup.md#uninstall-addin)
+ [Redigere et kørende IoT-viden-scenarie](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simuleringsindstillinger](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]