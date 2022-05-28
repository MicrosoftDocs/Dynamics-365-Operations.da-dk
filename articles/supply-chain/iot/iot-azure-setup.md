---
title: Konfigurere Azure-ressourcer til IoT-viden
description: I dette emne forklares det, hvordan du opretter og konfigurerer de Microsoft Azure-ressourcer, du skal bruge til IoT-viden.
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
ms.openlocfilehash: 7099604caa33b2a74252b48ac4eec6bc4c28ef51
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673124"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Konfigurere Azure-ressourcer til IoT-viden

[!include [banner](../../includes/banner.md)]

I dette emne forklares det, hvordan du opretter og konfigurerer de Microsoft Azure-ressourcer, du skal bruge til IoT-viden.

## <a name="create-azure-resources"></a>Oprette Azure-ressourcer

Udfør følgende trin for at oprette en IoT-hub, en Redis-cache og en key vault, som Microsoft Dynamics 365 Supply Chain Management kan få adgang til.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Kontrollér, at det Microsoft Dynamics RP Microservices-førsteparts-id findes i din lejer

Benyt følgende fremgangsmåde for at kontrollere, at app-id'et for Microsoft Dynamics ERP Microservices-førstepartsappen følger disse trin.

1. Log på Azure-portalen på <https://portal.azure.com>.
2. Gå til **Azure Active Directory**.
3. Gå til **Virksomhedsprogrammer**.
4. I feltet **Programtype** skal du vælge **Microsoft-programmer**.
5. Angiv **Microsoft Dynamics ERP Microservices** i søgefeltet.
6. Kontrollér, at **Microsoft Dynamics ERP Microservices** er på listen. Andre programmer har lignende navne. Du skal derfor sikre dig, at du finder det rigtige program. App-id'et er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Hvis programmet ikke findes på listen, skal du føje det til din lejer:

    1. På værktøjslinjen i Azure Portal skal du vælge knappen for at åbne Azure Cloud Shell.
    2. Kør kommandoen **Install-Module AzureAD**. Angiv **Y** for at installere modulet.
    3. Kør kommandoen **Get-InstalledModule -Name "AzureAD"** for at kontrollere, at modulet er installeret.
    4. Kør kommandoen **Connect-AzureAD -Confirm** for at køre godkendelsen.
    5. Kør kommandoen **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Du kan nu gentage trin 1 til 6 for at kontrollere, at app-id'et findes i din lejer.

### <a name="create-a-key-vault-resource"></a>Oprette en ny key vault-ressource

Benyt følgende fremgangsmåde for at oprette en ny key vault-ressource.

1. Opret eller gå til en ressourcegruppe i Azure-portalen.
2. Vælg **Tilføj**.
3. Gå til siden **Ny**, og angiv **Key vault** i søgefeltet. Vælg derefter **Opret**.
4. Gå til siden **Opret key vault**, og angiv et navn i **Key vault-navn**.
5. Gennemse standardværdierne, og vælg derefter **Gennemgå + Opret**.
6. Vælg **Opret**.

Key vaulten oprettes i baggrunden.

### <a name="create-an-iot-hub-resource"></a>Oprette en IoT Hub-ressource

Benyt følgende fremgangsmåde for at oprette en IoT Hub-ressource.

1. Oprette eller gå til en ressourcegruppe.
2. Vælg **Tilføj**.
3. Gå til siden **Ny**, og angiv **Iot Hub** i søgefeltet. Vælg derefter **Opret**.
4. Angiv et navn i feltet **IoT Hub-navn**.
5. Gennemse standardværdierne, og vælg derefter **Gennemgå + Opret**.
6. Vælg **Opret**.

IoT Hub'en oprettes i baggrunden.

> [!NOTE]
> Det anbefales, at du kun opretter én IoT Hub-ressource pr. miljø.

### <a name="create-a-redis-cache-resource"></a>Oprette en Redis-cacheressource

Benyt følgende fremgangsmåde for at oprette en Redis-cacheressource.

1. Oprette eller gå til en ressourcegruppe.
2. Vælg **Tilføj**.
3. Gå til siden **Ny**, og angiv **Azure Cache for Redis** i søgefeltet. Vælg derefter **Opret**.
4. Indtast et navn i feltet **DNS-navn**.
5. Gennemse standardværdierne, og vælg derefter **Opret**.

Redis-cachen oprettes i baggrunden.

> [!NOTE]
> Det anbefales, at du kun opretter én Redis-cacheressource pr. miljø.

Alle ressourcerne er blevet oprettet.

## <a name="configure-the-azure-resources"></a>Konfigurere Azure-ressourcerne

### <a name="configure-the-iot-hub"></a>Konfigurere IoT Hub

Hvis du vil konfigurere IoT hub, skal du følge disse trin.

1. Vælg IoT hub-ressourcen i dine ressourcer.
2. Vælg **Indbyggede slutpunkter** i venstre navigationsrude.
3. Indsæt følgende forbrugergrupper under **Forbrugergrupper**. Disse brugergrupper svarer til de færdiglavede scenarier.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Konfigurere key vaulten

Benyt følgende fremgangsmåde for at konfigurere key vaulten.

1. Vælg key vault-ressourcen i dine ressourcer.
2. Vælg **Adgangspolitikker** i den venstre navigationsrude.
3. Vælg **Tilføj en adgangspolitik**.
4. Gå til siden **Tilføj adgangspolitik**, og vælg **Hent** og **Vis** i feltet **Hemmelige tilladelser**.
5. Klik i feltet **Vælg hoved**.
6. I dialogboksen **Principal** skal du søge efter og vælge **Microsoft Dynamics ERP Microservices**. Vælg derefter **Vælg**.
7. Vælg **Tilføj**.
8. Vælg **Gem**.

Appen har nu adgang til hemmeligheder i key vaulten.

### <a name="save-the-iot-hub-connection-string-secret"></a>Gemme hemmeligheden for IoT Hub-forbindelsesstrengen

Benyt følgende fremgangsmåde, hvis du vil gemme hemmeligheden for IoT Hub-forbindelsesstrengen.

1. Vælg IoT hub-ressourcen i dine ressourcer.
2. Vælg **Indbyggede slutpunkter** i venstre navigationsrude.
3. Kopiér værdien i feltet **Event Hub-kompatibel slutpunkts-key vault**.
4. Gå til key vault-ressourcen.
5. Vælg **Hemmeligheder** i navigationsruden til venstre.
6. Vælg **Generer/importer**.
7. Indtast et navn i feltet **Navn**.
8. I feltet **Værdi** skal du indsætte den værdi for slutpunktet, du har kopieret tidligere.
9. Vælg **Opret**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Gemme hemmeligheden for Redis-cacheforbindelsesstrengen

Benyt følgende fremgangsmåde, hvis du vil gemme hemmeligheden for Redis-cacheforbindelsesstrengen.

1. Vælg Redis-cacheressourcen i dine ressourcer.
2. Vælg **Adgangsnøgler**.
3. Kopiér værdien i feltet **Primær forbindelsesstreng**.
4. Gå til key vault-ressourcen.
5. Vælg **Hemmeligheder** i navigationsruden til venstre.
6. Vælg **Generer/importer**.
7. Indtast et navn i feltet **Navn**.
8. I feltet **Værdi** skal du indsætte den forbindelsesstreng, du har kopieret tidligere.
9. Vælg **Opret**.

> [!NOTE]
> Når du opdaterer en af forbindelsesstrengene, skal du også opdatere de hemmelige værdier.

Nu er du færdig med at klargøre de krævede Azure-ressourcer. Det næste skridt er at [installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
