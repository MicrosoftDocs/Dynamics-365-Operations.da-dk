---
title: Adgang til privatadresser efter sikkerhedsrolle
description: Dette emne forklarer, hvordan du håndterer, at en kunde ikke kan få adgang til private adresser.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0b96733946e4ef79de244730d0c442b9900426c1
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413333"
---
# <a name="access-to-private-addresses-by-security-role"></a>Adgang til privatadresser efter sikkerhedsrolle

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
