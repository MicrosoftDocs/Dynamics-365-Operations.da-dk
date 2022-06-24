---
title: Adgang til privatadresser efter sikkerhedsrolle
description: Denne artikel forklarer, hvordan du håndterer, at en kunde ikke kan få adgang til private adresser.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7102bbcbecec0d88351e796e2c63663d956b86f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849675"
---
# <a name="access-to-private-addresses-by-security-role"></a>Adgang til privatadresser efter sikkerhedsrolle


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Afgang**

Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.

**Løsning**

For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.

1. Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.
2. Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.
3. Vælg **Gem**.

![Siden Parametre for globalt adressekartotek.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
