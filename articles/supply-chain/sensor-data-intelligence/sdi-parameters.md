---
title: Sensor Data Intelligence-parametre
description: Denne artikel indeholder oplysninger om konfigurationsindstillinger, der er tilgængelige på siden Sensor Data Intelligence-parametre for data.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428316"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence-parametre

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

På siden **Sensor Data Intelligence-parametre** kan du finde nogle få indstillinger, som du kan bruge til at konfigurere funktionen. Disse indstillinger omfatter Azure-forbindelsesparametre og en parameter for levetiden på påmindelsesmeddelelser, der sendes til brugere som svar på sensormålinger.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Læse og ændre forbindelsesoplysninger for din Azure IoT-løsning

Du skal typisk oprette en Azure IoT-løsning og knytte den til Microsoft Dynamics 365 Supply Chain Management fra siden **Installer og opret forbindelse til Azure-ressourcer**, som vil føre dig gennem begge procedurer. (Du kan finde flere oplysninger i [Implementer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md)). Du kan også når som helst få vist og redigere forbindelsesoplysningerne i Supply Chain Management ved at følge disse trin.

1. Gå til **Systemadministration \> Opsætning \> Sensordataintelligens \> Sensor Data Intelligence-parametre**.
1. Under fanen **Tidsserier** skal du angive værdien **Primary connection string (StackExchange.Redis)** for den Azure IoT-løsning, du vil oprette forbindelse til, i feltet **Forbindelsesstreng for Redis Metric-lager**. Du kan finde flere oplysninger om, hvordan du finder denne værdi, i [Installer en IoT-eksempelløsning på Azure](sdi-deploy-iot-solution-on-azure.md).
1. Under fanen **Integrationer** skal du i feltet **Azure AD-programklient-id** angive værdien for **klient-id** for den Azure IoT-løsning, du vil oprette forbindelse til. Du kan finde flere oplysninger om, hvordan du finder denne værdi, i [Installer en IoT-eksempelløsning på Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Angive levetiden for påmindelsesmeddelelser

Hver gang Sensordataintelligens registrerer en situation, der kræver brugeropmærksomhed, sendes en besked til den relevante bruger. Hvis du vil forhindre, at disse beskeder får en pil op i systemet, skal du angive dem til at udløbe efter et par dage.

1. Gå til **Systemadministration \> Opsætning \> Sensordataintelligens \> Sensor Data Intelligence-parametre**.
1. Angiv det antal dage, en besked skal bevares i feltet **Dage til live besked** under fanen **Meddelelser**. Når det angivne tidsrum er passeret, slettes beskeden.
