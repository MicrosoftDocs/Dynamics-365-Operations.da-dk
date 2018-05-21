--- 
title: Oprette en konfigurationsudbyder og markere den som aktiv til elektronisk rapportering (ER)
description: "Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 018aee917c13f576759ebd812d31cbc9d83e2d1a
ms.contentlocale: da-dk
ms.lasthandoff: 02/23/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a>Oprette en konfigurationsudbyder og markere den som aktiv til elektronisk rapportering (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER). Hver ER-konfiguration refererer til udbyderen som konfigurations forfatter. I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationsudbydere deles af alle firmaer.


## <a name="create-a-provider"></a>Opret en udbyder
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Konfigurationsudbydere.
3. Klik på Ny.
    * En udbyderpost har et entydigt ved navn og URL-adresse. Gennemse indholdet af denne side, og spring denne procedure over, hvis der allerede findes en post for Litware, Inc. (`http://www.litware.com`).  
4. Skriv "Litware, Inc." i feltet Navn.
    * Litware, Inc.  
5. Indtast `http://www.litware.com` i feltet Internetadresse.
6. Klik på Gem.
7. Luk siden.

## <a name="select-as-an-active-provider"></a>Vælg en aktiv udbyder
1. Vælg udbyderen Litware, Inc., .
2. Klik på Angiv som aktiv.


