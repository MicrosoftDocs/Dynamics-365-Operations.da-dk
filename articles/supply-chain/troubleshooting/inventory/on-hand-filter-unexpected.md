---
title: Filterruden på listesiden Ruder virker ikke som forventet
description: Filtrene i filteruden på siden "Beholdningsliste" filtrerer ikke resultater som forventet.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686677"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Filterruden på listesiden Ruder virker ikke som forventet

## <a name="symptoms"></a>Symptomer

Filtrene i filteruden på siden **Beholdningsliste** filtrerer ikke resultater som forventet.

## <a name="resolution"></a>Løsning

Siden **Beholdningsliste** samles fra en detaljeret disponibel lagerbeholdningstabel, der omfatter alle tilgængelige dimensioner. Listen på denne side er dog en oversigt. Derfor kan den kombinere rækker fra kildetabellen ved at aggregere værdier i henhold til de viste dimensioner.

Filtre, der er konfigureret i filterruden, gælder for kildetabellen, ikke den samlede liste. Denne adfærd kan nogle gange give uventede resultater, som det fremgår af [disse eksempler](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

De [filtre, der findes i gitteret](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters), *bliver* anvendt på den samlede liste. Disse filtre omfatter både QuickFilter øverst i gitteret og filteret for hver kolonneoverskrift.
