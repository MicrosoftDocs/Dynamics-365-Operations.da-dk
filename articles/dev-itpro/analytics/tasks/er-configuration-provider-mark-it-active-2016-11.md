---
title: Oprette konfigurationsudbydere og markere dem som aktive
description: Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595389"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Oprette konfigurationsudbydere og markere dem som aktive

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER). Hver ER-konfiguration refererer til udbyderen som konfigurations forfatter. I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationsudbydere deles af alle firmaer.


## <a name="create-a-provider"></a>Opret en udbyder
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Konfigurationsudbydere.
3. Klik på Ny.
    * En udbyderpost har et entydigt ved navn og URL-adresse. Gennemse indholdet af denne side, og spring denne procedure over, hvis der allerede findes en post for Litware, Inc. (https://www.litware.com).  
4. Skriv "Litware, Inc." i feltet Navn.
    * Litware, Inc.  
5. Indtast 'https://www.litware.com' i feltet Internetadresse.
    * https://www.litware.com  
6. Klik på Gem.
7. Luk siden.

## <a name="select-as-an-active-provider"></a>Vælg en aktiv udbyder
1. Vælg udbyderen Litware, Inc., .
2. Klik på Angiv som aktiv.

