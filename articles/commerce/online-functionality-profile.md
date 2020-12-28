---
title: Oprette en onlinefunktionalitetsprofil
description: Dette emne beskriver, hvordan du opretter en onlineprofil for funktionalitet i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411202"
---
# <a name="create-an-online-functionality-profile"></a>Oprette en onlinefunktionalitetsprofil


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over opsætningen af en onlinefunktionalitetsprofil til Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Profilen for onlinefunktionalitet giver forskellige indstillinger, der bruges til onlinekanaler. Hver onlinekanal skal angive en profil for onlinefunktionalitet.

## <a name="create-an-online-functionality-profile"></a>Oprette en onlinefunktionalitetsprofil

Følgende procedure forklarer, hvordan du kan oprette en onlinefunktionalitetsprofil i Commerce Headquarters-appen.

1. I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et id for profilen i feltet **Profil**.
1. Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.
1. Rediger indstillingerne for **Indkøbskurv**, **Detaildebitorer** eller **Betaling ved kassen** i sektionen **Funktioner**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en profil for onlinefunktionalitet.
  
![Eksempel på profil for onlinefunktionalitet](media/online-functionality-profile.png)

## <a name="functions"></a>Funktioner

- **Samling af produkter**: Når funktionen er aktiveret, tillader den, at der opdateres antal i indkøbskurven, når samme vare tilføjes flere gange.
- **Tillad udtjekning uden betaling ved kassen**: Når funktionen er aktiveret, vil den håndtere scenariet, når varer, der føjes til indkøbsvognen, har en pris på 0,00 kr.
- **Opret kunde i asynkron tilstand**: Dette er en ældre indstilling, der gælder for tredjeparts e-handelskanaler, og som ikke kan anvendes på Dynamics 365 e-handelsstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurere en onlinekanal](channel-setup-online.md)

[Konfigurer en detailkanal](channel-setup-retail.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)
