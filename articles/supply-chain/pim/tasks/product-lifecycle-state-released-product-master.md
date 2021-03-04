---
title: Tildele en status for produktlivscyklus til en frigivet produktmaster
description: Denne fremgangsmåde viser, hvordan du tildeler en status for produktlivscyklus til en frigivet produktmaster og dens varianter.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424481"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Tildele en status for produktlivscyklus til en frigivet produktmaster

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du tildeler en status for produktlivscyklus til en frigivet produktmaster og dens varianter. Forudsætning: Du skal afspille opgaveguiden "Opret en ny status for produktlivscyklus" først for at sikre, at du har oprettet mindst én status for produktlivscyklus, før du kan afspille denne opgaveguide.


## <a name="find-a-released-product-master"></a>Find en frigiven produktmaster.
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Find og vælg den ønskede post på listen.

> [!NOTE]
> En produktmaster har produktundertypen Produktmaster.  

## <a name="update-the-lifecycle-state"></a>Opdatere livscyklussen
1. Klik på Rediger.
2. Indtast eller vælg en værdi i feltet Status for produktlivscyklus.
3. Klik på Gem.
4. Klik på Ja.

> [!NOTE]
> Hvis Ja er markeret, opdateres alle de relaterede frigivne produktvarianter, der har samme oprindelige status som den frigivne produktmaster, også til den nye status for produktlivscyklus. Hvis Nej er markeret, bevarer alle varianter deres aktuelle tilstand. Varianter, der har en anden status for produktlivscyklus end den frigivet produktmaster, opdateres ikke.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Kontroller livscyklussen for varianterne
1. Klik på Frigivne produktvarianter.

> [!NOTE]
> Bemærk, at alle varianter har arvet den valgte status for produktlivscyklus fra den frigivne produktmaster.  

2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Status for produktlivscyklus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]