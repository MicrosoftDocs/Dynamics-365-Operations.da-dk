---
title: Adgang til privatadresser efter sikkerhedsrolle
description: I denne artikel beskrives det, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417782"
---
# <a name="access-to-private-addresses-by-security-role"></a>Adgang til private adresser efter sikkerhedsrolle

**Afgang**

Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.

**Løsning**

For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.

1. Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.
2. Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.
3. Vælg **Gem**.

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
