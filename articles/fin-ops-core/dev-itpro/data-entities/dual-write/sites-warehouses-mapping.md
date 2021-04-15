---
title: Integrerede lokationer og lagersteder
description: I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750660"
---
# <a name="integrated-sites-and-warehouses"></a>Integrerede lokationer og lagersteder

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Dataverse. Operationelle steder og lagersteder er almindelige begreber i et Supply Chain Management-program. De bruges til at modellere forsyningskæden i dit firma.

## <a name="templates"></a>Skabeloner

Med integrationen med Dataverse kan disse begreber og alle tilhørende oplysninger være tilgængelige i Dataverse ved hjælp af tabellerne for lokationer og lagersteder i følgende tabel.

Finance and Operations-apps | Andre Dynamics 365-apps | Betegnelse
--------------------------|---------------------------|---
Steder | msdyn_operationalsites | 
Lagersteder | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]