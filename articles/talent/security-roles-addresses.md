---
title: Adgang til private adresser efter sikkerhedsrolle
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ikke kan få adgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517610"
---
# <a name="access-to-private-addresses-by-security-role"></a>Adgang til private adresser efter sikkerhedsrolle

[!include [banner](includes/banner.md)]

**Afgang**

Når en kunde kopierer en sikkerhedsrolle og logger på som denne nye rolle, kan kunden ikke kan se adresser, der er markeret som privat.

**Løsning**

For at problemet kan løses, skal kunden følge disse trin for den kopierede sikkerhedsrolle.

1. Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Parametre for globalt adressekartotek**.
2. Under fanen **Sikkerhed for privat lokation** skal du flytte den nye sikkerhedsrolle fra listen **Tilgængelige roller** til listen **Valgte roller**.
3. Vælg **Gem**.

![Siden Parametre for globalt adressekartotek](media/GAD-parameters.png)
