---
title: Konfigurere scenarier for betaling af fakturaer
description: I dette emne beskrives, hvordan du kan konfigurere Dynamics 365 for Retail til at understøtte forskellige scenarier relateret til fakturabetalinger.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "302067"
---
# <a name="set-up-pay-invoice-scenarios"></a>Konfigurere scenarier for betaling af fakturaer

[!include [banner](includes/banner.md)]

Funktionen Betal faktura i Dynamics 365 for Retail er blevet udvidet for at understøtte:

- Betaling af flere salgsordrefakturaer i en enkelt POS-transaktion.
- Betaling af forskellige debitorfakturatyper, herunder fritekstfakturaer, projektbaserede fakturaer og kreditnotaer.

Hvis du vil aktivere disse scenarier, skal funktionalitetsprofilen for butikker være konfigureret som beskrevet nedenfor.

1. Gå til **Detail \> Konfiguration af kanal \> POS setup \> POS-profiler \> Funktionalitetsprofiler**, og vælg en profil, der er knyttet til de butikker, som du vil foretage ændringerne for.
2. På fanen **Funktioner** kan du konfigurere følgende parametre efter behov.

    - **Salgsordrefaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere salgsordrebaserede fakturaer i en enkelt POS-transaktion.
    - **Fritekstfaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere fritekstbaserede fakturaer i en enkelt POS-transaktion.
    - **Projektfaktura** – Vælg **Ja** for at give brugerne mulighed for at betale en eller flere projektbaserede fakturaer i en enkelt POS-transaktion.
    - **Salgsordre kreditnota** – Vælg **Ja** for at tillade brugere at udligne flere salgsordrebaserede kreditnotaer i forhold til åbne fakturaer eller behandle en refusion til kunden for en åben kreditnota.

> [!NOTE]
> Betaling eller udligning af delbeløb understøttes ikke endnu.
