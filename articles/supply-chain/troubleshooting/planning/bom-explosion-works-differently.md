---
title: Udfoldning af styklister fungerer forskelligt for fastlagte og kalkulerede produktionsordrer
description: Styklisteudfoldningen opfører sig forskelligt for autoriserede produktionsordrer og forkalkulerede produktionsordrer for manuelt oprettet arbejde
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475901"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Udfoldning af styklister fungerer forskelligt for fastlagte og kalkulerede produktionsordrer

## <a name="symptoms"></a>Symptomer

Når en produktionsordre autoriseres, udfoldes varerne ikke, når du udfolder styklisten. Men når du opretter en arbejdsordre manuelt og derefter forkalkulerer produktionsordren, udfoldes varerne.

### <a name="resolution"></a>Løsning

Den udfoldning, der opstår, når produktionsordren autoriseres, peger på ordreforslaget, men det ser ikke ud til, at ordreforslaget er autoriseret i dette tilfælde. Men hvis produktionsordren er forkalkuleret, udløses udfoldningen fra den frigivne produktionsordre, når der ikke findes et ordreforslag.
