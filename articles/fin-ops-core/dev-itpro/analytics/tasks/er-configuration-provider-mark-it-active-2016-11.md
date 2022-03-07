---
title: Oprette konfigurationsudbydere og markere dem som aktive
description: Dette emne forklarer, hvordan en bruger med rollen som Systemadministrator eller Udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5b429badcbcc0e9829d82785a6e1f1a2504f5ec9b9ac74d249032f272dea103
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747241"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Oprette konfigurationsudbydere og markere dem som aktive

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan en bruger med rollen som Systemadministrator eller Udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER). Hver ER-konfiguration refererer til udbyderen som konfigurations forfatter. I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationsudbydere deles af alle firmaer.

## <a name="create-a-provider"></a>Opret en udbyder
1. Gå til **navigationsruden** i øverste venstre hjørne, og vælg **Virksomhedsadministration**.
2. Gå til **Arbejdsområder > Elektronisk rapportering**.
3. Gå til **Relaterede links > Konfigurationsudbydere**.
4. Vælg **Ny**.
    - En udbyderpost har et entydigt ved navn og URL-adresse. Gennemse indholdet af denne side, og spring denne procedure over, hvis der allerede findes en post for Litware, Inc. (https://www.litware.com).  
5. Skriv `Litware, Inc.` i feltet Navn.
6. Indtast `https://www.litware.com` i feltet Internetadresse.
7. Vælg **Gem**.
8. Luk siden.

## <a name="select-as-an-active-provider"></a>Vælg en aktiv udbyder
1. Vælg udbyderen Litware, Inc., .
2. Vælg **Angiv aktive**.

![Arbejdsområdeside til elektronisk rapportering.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]