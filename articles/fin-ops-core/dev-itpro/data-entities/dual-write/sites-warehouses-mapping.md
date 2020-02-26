---
title: Integrerede lokationer og lagersteder
description: I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019695"
---
# <a name="integrated-sites-and-warehouses"></a>Integrerede lokationer og lagersteder

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Common Data Service. Operationelle steder og lagersteder er almindelige begreber i et Supply Chain Management-program. De bruges til at modellere forsyningskæden i dit firma.

## <a name="templates"></a>Skabeloner

Med integrationen med Common Data Service kan disse begreber og alle tilhørende oplysninger være tilgængelige i Common Data Service ved hjælp af enhederne for lokationer og lagersteder i følgende tabel.

Finance and Operations-apps | Andre Dynamics 365-apps | Beskrivelse
--------------------------|---------------------------|---
Steder | msdyn_operationalsites | 
Lagersteder | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

