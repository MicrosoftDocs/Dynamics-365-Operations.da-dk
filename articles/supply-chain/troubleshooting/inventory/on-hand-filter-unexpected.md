---
title: Filterruden på listesiden Ruder virker ikke som forventet
description: Filtrene i filteruden på siden Beholdningslistefiltrerer ikke resultater som forventet.
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475933"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Filterruden på listesiden Ruder virker ikke som forventet

## <a name="symptoms"></a>Symptomer

Filtrene i filteruden på siden **Beholdningsliste** filtrerer ikke resultater som forventet.

## <a name="resolution"></a>Løsning

Siden  **Beholdningsliste** samles fra en detaljeret disponibel lagerbeholdningstabel, der omfatter alle tilgængelige dimensioner. Listen på denne side er dog en oversigt. Derfor kan den kombinere rækker fra kildetabellen ved at aggregere værdier i henhold til de viste dimensioner.

Filtre, der er konfigureret i filterruden, gælder for kildetabellen, ikke den samlede liste. Denne adfærd kan nogle gange give uventede resultater, som det fremgår af [disse eksempler](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

De  [filtre, der findes i gitteret](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters),  *bliver* anvendt på den samlede liste. Disse filtre omfatter både QuickFilter øverst i gitteret og filteret for hver kolonneoverskrift.
