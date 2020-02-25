---
title: Oprette en profil for detailfunktionalitet
description: Dette emne beskriver, hvordan du opretter en profil for detailfunktionalitet i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002837"
---
# <a name="create-a-retail-functionality-profile"></a>Oprette en profil for detailfunktionalitet


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en profil for detailfunktionalitet i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Profilen for detailfunktionalitet giver forskellige indstillinger, der bruges til onlinekanaler. Hver detailkanal skal angive en profil for detailfunktionalitet.

## <a name="create-a-retail-functionality-profile"></a>Oprette en profil for detailfunktionalitet

Benyt følgende fremgangsmåde for at oprette en ny profil for detailfunktionalitet.

1. I navigationsruden skal du gå til **Moduler \> Konfiguration af kanal \> POS-profiler \> Funktionalitetsprofiler**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et id for profilen ("FN006" i eksempelbilledet nedenfor) i feltet **Profil**.
1. Angiv en værdi ("Adventure Works Profile" i eksempelbilledet nedenfor) i feltet **Beskrivelse**.
1. Vælg et land til **ISO**-landestandarden i sektionen **Generelt**.
1. Rediger andre indstillinger i sektionen **Generelt** efter behov.
1. I sektionen **Generelt** skal du vælge et **Kvitteringsprofil-id** for mailkvitteringer.
1. Rediger indstillinger i sektionen **Funktioner** efter behov.
1. Rediger indstillinger i sektionen **Beløb** efter behov.
1. Rediger indstillinger i sektionen **Infokoder** efter behov.
1. Rediger indstillinger i sektionen **Kvitteringsnummerering** efter behov. 
  
Følgende billede viser et eksempel på en profil for detailfunktionalitet.
  
![Eksempel på profil for detailfunktionalitet](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Infokoder og infokodegrupper](info-codes-retail.md)           

[Oprette nyt adressekartotek](new-address-book.md) 

[Oversigt over skærmlayout](pos-screen-layouts.md)       

[Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) 
