---
title: Oprette en onlinefunktionalitetsprofil
description: Denne artikel beskriver, hvordan du opretter en onlineprofil for funktionalitet i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 686bc6440c31f3a4d729f2d92e3e57a1cc7b641f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895420"
---
# <a name="create-an-online-functionality-profile"></a>Oprette en onlinefunktionalitetsprofil

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over opsætningen af en onlinefunktionalitetsprofil til Microsoft Dynamics 365 Commerce.

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
  
![Eksempel på profil for onlinefunktionalitet.](media/online-functionality-profile.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
