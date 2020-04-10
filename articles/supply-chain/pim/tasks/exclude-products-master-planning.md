---
title: Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering
description: Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62de37b5a84a1771b77ef2566942b7ffe8895f16
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149935"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.


## <a name="create-an-obsolete-state"></a>Oprette en forældet tilstand
1. Gå til Administration af produktoplysninger > Konfiguration > Status for produktlivscyklus.
2. Klik på Ny.
3. Skriv en værdi i feltet Status.
4. Vælg Nej i feltet Er aktiv for planlægning.
5. Skriv en værdi i feltet Beskrivelse.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Knytte den forældede tilstand til en frigivet produkt
1. Luk siden.
2. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
3. Brug Quick Filter til at finde poster. Du kan for eksempel filtrere på feltet Søgenavn med værdien 'M00'.
4. Klik på Rediger.
5. Markér den valgte række på listen.
6. Indtast eller vælg en værdi i feltet Status for produktlivscyklus.

