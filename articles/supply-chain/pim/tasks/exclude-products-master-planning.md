---
title: Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering
description: Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818031"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]