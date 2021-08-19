---
title: Manglende feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed
description: Der mangler feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738837"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Manglende feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed

KB-nummer: 4612800

## <a name="symptoms"></a>Symptomer

Når du kopierer varemodelgrupper til en anden juridisk enhed (firma) ved hjælp af enheden *Lagerpolitikker for varemodelgruppe*, mangler der nogle feltindstillinger (f.eks. lagermodellen og -beskrivelsen) i den nye modelgruppe i den juridiske destinationsenhed.

## <a name="resolution"></a>Løsning

Hvis du vil oprette en komplet kopi af en varemodelgruppe til en anden juridisk enhed, skal du også vælge både de lagerpolitikker for varemodelgruppen (`InventInventoryPolicyEntity`) og forudsætningspolitikkerne for omkostningsforløb (`InventCostFlowAssumptionPolicyEntity`), der er knyttet til varemodelgruppen.
