---
title: Oprette en simuleret opsætning til test
description: I denne artikel beskrives det, hvordan du kan konfigurere en simulator, som du kan bruge til at teste Sensordataintelligens uden at installere fysiske oplysninger.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643970"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Oprette en simuleret opsætning til test

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Hvis du vil teste Azure Data Intelligence uden at installere fysiske oplysninger, kan du bruge *Raspberry PI Azure IoT Online Simulator* til at emulere sensorsignaler og sende dem til din IoT-løsning (Internet of Things) på Microsoft Azure. Du kan finde flere oplysninger om dette eksempel i [Online Connect Raspberry Pi online to Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Videovejledning

I følgende video vises, hvordan du kan konfigurere et simuleret forsøg til test. De resterende afsnit i denne artikel indeholder de samme instruktioner i et tekstbaseret format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Oprette en enhed i Azure IoT Hub

Du skal først konfigurere en enhed for at godkende signalerne til Azure IoT Hub.

1. I Azure skal du gå til listen over ressourcer til den ressourcegruppe, du har oprettet til brug sammen med Sensordataintelligens. (Du kan finde flere oplysninger i [Implementer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md)).
1. Find den post, hvor feltet **Type** er angivet til *IoT Hub*, på ressourcelisten. Vælg navnet i kolonnen **Navn** for at åbne siden Detaljer om ressourcen.
1. Vælg **Enheder** i navigationsruden til venstre.
1. Vælg **Tilføj enhed** på siden **Enheder**.
1. På siden **Opret en enhed** skal du angive følgende felter:

    - **Enheds-id** – Angiv et navn på den nye enhed (f.eks. *Min-IoT-enhed*).
    - **Godkendelsestype** – Vælg *Symmetriske nøgler*.
    - **Automatisk generering af nøgler** – Marker dette afkrydsningsfelt.
    - **Opret forbindelse mellem denne enhed og en IoT-hub** – Vælg *Aktivér*.

1. Vælg **Gem** for at vende tilbage til siden **Enheder**.
1. Find den nye enhed på listen. Vælg navnet i kolonnen **Enheds-id** for at åbne siden Detaljer om enheden. Hvis den nye enhed ikke vises på listen, skal du opdatere siden.
1. Kopier værdien i feltet **Primær forbindelsesstreng** (f.eks. ved at vælge knappen **Kopiér til Udklipsholder**). Denne værdi skal du bruge senere, når du konfigurerer Raspberry Pi IoT-simulator til at emulere sensorsignaler. Derfor bør du overveje at indsætte den i en tekstfil nu.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Føj Azure-forbindelsesstrengen til Azure-pi-IoT-klassen

Følg disse trin for at føje forbindelsesstrengen fra enheden i Azure IoT Hub til scriptet i Raspberry-tjenesten.

1. Åbn [Raspberry Pi IoT-simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Find den linje, der indeholder følgende kommando, i ruden kodeeditor.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Erstat hjælpeteksten, herunder kantede parenteser, med den værdi for den **primære forbindelsesstreng**, du kopierede i forrige afsnit. Resultatet skulle ligne følgende eksempel:

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Føje sensor-id'er og -værdier til nyttelasten i Raspberry Pi IoT-simulator

Du skal nu konfigurere Raspberry Pi IoT-simulator med simulerede oplysninger og de værdier, de vil sende som nyttelast.

- Find funktionen i kodeeditoren for Raspberry Pi IoT-simulator `getMessage`, og rediger den, så den passer til følgende kode. (De forskellige opsætninger oprettes i `cb()`-linjerne).

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > De pålydende id'er, der er defineret i kodeeditoren til Raspberry Pi IoT-simulator, skal være identiske med de identiske id'er, som du senere skal angive for scenarierne i Supply Chain Management. I det foregående eksempel bruges der læsbare id'er. I et faktisk scenario vil sensor-id'erne dog være entydige id'er (Global Unique Identifier), der leveres af sensor-producenten. De human-læsbare ID'er, som bruges i dette eksempel, bruges også i eksemplerne i [produktkvalitetsscenariet](sdi-scenario-product-quality.md), [Scenariet til vedligeholdelse af aktiver](sdi-scenario-asset-maintenance.md), [Scenariet til produktionsforsinkelse](sdi-scenario-production-delays.md) og [scenariet for maskinstatus](sdi-scenario-equipment-downtime.md)). Brug derfor denne kode, hvis du vil gennemgå scenarierne.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Redigere intervallet for afsendelse af sensorsignaler

Du skal nu angive det interval, som Raspberry Pi IoT-simulator skal sende de emulerede sensorsignaler med.

1. Find følgende funktions aktivering i kodeeditoren for Raspberry Pi IoT-simulator i kodeeditoren.

    `setInterval(sendMessage, 2000);`

2. Som standard sender Raspberry Pi IoT-simulator et sensorsignal hver 2.000 millisekunder (to sekunder). Du kan justere værdien efter behov.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Kør Raspberry Pi IoT-simulator

- Vælg **Kør** for at starte simuleringen og begynde at sende simulerede sensordata.
