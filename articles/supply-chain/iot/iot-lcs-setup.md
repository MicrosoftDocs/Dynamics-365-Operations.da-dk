---
title: Installere tilføjelsesprogrammet IoT-viden i LCS
description: I dette emne forklares, hvordan du kan installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d55ca1975589699cbce03dcc7bf81e0762738d24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963479"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Installere tilføjelsesprogrammet IoT-viden i LCS

[!include [banner](../../includes/banner.md)]

I dette emne forklares, hvordan du kan installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS). Bemærk, at tilføjelsesprogrammer ikke kan installeres i et demo- eller testmiljø. Før du kan installere tilføjelsesprogrammet, skal du [oprette Azure-ressourcerne](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>Konfigurere LCS-miljøet

1. Åbn LCS, og gå til dit Microsoft Dynamics 365 Supply Chain Management-miljø.
2. Rul til sektionen **Tilføjelsesprogrammer for miljø**.
3. Vælg **Installér et nyt tilføjelsesprogram** for at få vist listen over de tilføjelsesprogrammer, der er aktiveret for miljøet.
4. Vælg **IoT-viden** i dialogboksen **Vælg et tilføjelsesprogram, der skal installeres**.
5. Gå til dialogboksen **Konfigurer tilføjelsesprogram**, og angiv detaljerne i din IoT-hub og Redis-cache. Du kan finde de nødvendige værdier i den key vault, du har oprettet under [Oprette Azure-ressourcer](iot-azure-setup.md).

    + **Lejer-id** – gå til key vault'en på Azure-portalen, og vælg derefter **Oversigt** i den venstre navigationsrude, kopiér værdien for **Mappe-id**. Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.
    + **URI-adresse til IoT Event Hub-kompatibel slutpunkts-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**. Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.
    + **Hemmeligt navn for IoT Event Hub-kompatibel slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for IoT-hubben er gemt. Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.
    + **URI-adresse til Redis-cache-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**. Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.
    + **Hemmeligt navn for Redis-cache-slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for Redis-cachen er gemt. Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.

6. Markér afkrydsningsfeltet for at acceptere vilkår og betingelser.
7. Vælg **Installer**.
8. Der vises en meddelelsesboks, som angiver, at "Tilføjelsesprogram er blevet udløst til installation". Vælg **OK**.

LCS-opsætning er nu fuldført. I det næste trin skal du konfigurere [scenarierne](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Fjern tilføjelsesprogrammet

1. I Supply Chain Management skal du [deaktivere scenarierne](iot-scenario-setup.md#disable-a-scenario).
2. I LCS skal du gå til Supply Chain Management-miljødetaljerne.
3. Rul til sektionen **Tilføjelsesprogrammer for miljø**.
4. Vælg **Fjern** for tilføjelsesprogrammet IoT-viden.
