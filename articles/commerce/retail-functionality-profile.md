---
title: Oprette en detailfunktionalitetsprofil
description: Denne artikel beskriver, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f006aaf594f1df097f80c77794e34f9b831e9949
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280235"
---
# <a name="create-a-retail-functionality-profile"></a>Oprette en detailfunktionalitetsprofil

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.

Commerce-funktionalitetsprofilen giver forskellige indstillinger, der bruges til onlinekanaler. Hver kanal skal angive en funktionalitetsprofil.

## <a name="create-a-functionality-profile"></a>Opret en funktionalitetsprofil

Benyt følgende fremgangsmåde for at oprette en ny funktionalitetsprofil.

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
  
Følgende billede viser et eksempel på en funktionalitetsprofil.
  
![Eksempel på funktionalitetsprofil.](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Infokoder og infokodegrupper](info-codes-retail.md)           

[Oprette nyt adressekartotek](new-address-book.md) 

[Oversigt over skærmlayout](pos-screen-layouts.md)       

[Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
