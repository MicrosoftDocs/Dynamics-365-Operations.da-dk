---
title: Metode for halvårligt afskrivningsprincip
description: Denne artikel beskriver den metode, som anlægsaktiver bruger til at beregne afskrivning ved hjælp af halvårsprincippet, der beregner seks måneders afskrivning i et aktivs første og sidste år i brug.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879589"
---
# <a name="half-year-depreciation-convention-methodology"></a>Metode for halvårligt afskrivningsprincip

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel beskriver den metode, der bruges i anlægsaktiver til at beregne afskrivninger ved hjælp af halvårsprincippet. Det halvårlige princip beregner seks afskrivningsmåneder under et anlægs første og sidste år i brug. Du kan finde flere oplysninger om afskrivningsprincipper under [Afskrivningsmetoder og -principper](Fixed-asset-depreciation-conventions.md). 

Når du bruger afskrivningsprincippet på seks måneder, bruger systemet anskaffelsesåret eller det år, hvor anlægsaktivet blev taget i brug, og beregner derefter fem års afskrivning fra det pågældende år og tilføjer derefter seks måneder. For at illustrere denne proces skal du forestille dig et aktiv, der er anskaffet til en pris af 50.000 og taget i brug i april 2020. Det antages også, at aktivet har en levetid på fem år.

Det første år, det er i brug, afsluttes i december 2020, hvilket betyder, at anlægsaktivets fem års levetid vil ophøre i december 2024. I det halvårlige afskrivningsprincip lægges der seks måneder til aktivets levetid, hvilket betyder, at levetiden slutter i juni 2025. 

> Årlig afskrivning 50.000/5 = 10.000 månedlig afskrivning 10.000/12 = 833,33 <br>
> Første års afskrivning 10.000/2 = 5.000 og den efterfølgende månedlige afskrivning 5.000/9 = 555,56

   [![Afskrivningsplan for halvårligt afskrivningsprincip.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

De udvidede afskrivningsperioder, der tilføjes af halvårsprincippet, giver en mere præcis afskrivningsfordeling. Seks måneders princippet fordeler afskrivningsudgifter mere ligeligt, hvilket er nyttigt ved rapportering til driftsregnskabet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
