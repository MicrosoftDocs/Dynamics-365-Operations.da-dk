---
title: Oprette en detailfunktionalitetsprofil
description: I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410950"
---
# <a name="create-a-retail-functionality-profile"></a>Oprette en detailfunktionalitetsprofil


[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du opretter en funktionalitetsprofil i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

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
  
![Eksempel på funktionalitetsprofil](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Infokoder og infokodegrupper](info-codes-retail.md)           

[Oprette nyt adressekartotek](new-address-book.md) 

[Oversigt over skærmlayout](pos-screen-layouts.md)       

[Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) 
