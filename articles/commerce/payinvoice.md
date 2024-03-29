---
title: Konfigurere scenarier for betaling af fakturaer
description: I denne artikel beskrives, hvordan du kan konfigurere Dynamics 365 Commerce til at understøtte forskellige scenarier relateret til fakturabetalinger.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 78af54fec771e5012aca095d07fd772988a56029
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885368"
---
# <a name="set-up-pay-invoice-scenarios"></a>Konfigurere scenarier for betaling af fakturaer

[!include [banner](includes/banner.md)]

Funktionen Betal faktura i Dynamics 365 Commerce er blevet udvidet for at understøtte:

- Betaling af flere salgsordrefakturaer i en enkelt POS-transaktion.
- Betaling af forskellige debitorfakturatyper, herunder fritekstfakturaer, projektbaserede fakturaer og kreditnotaer.

Hvis du vil aktivere disse scenarier, skal funktionalitetsprofilen for butikker være konfigureret som beskrevet nedenfor.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**, og vælg en profil, der er knyttet til de butikker, som du vil foretage ændringerne for.
2. På fanen **Funktioner** kan du konfigurere følgende parametre efter behov.

    - **Salgsordrefaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere salgsordrebaserede fakturaer i en enkelt POS-transaktion.
    - **Fritekstfaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere fritekstbaserede fakturaer i en enkelt POS-transaktion.
    - **Projektfaktura** – Vælg **Ja** for at give brugerne mulighed for at betale en eller flere projektbaserede fakturaer i en enkelt POS-transaktion.
    - **Salgsordre kreditnota** – Vælg **Ja** for at tillade brugere at udligne flere salgsordrebaserede kreditnotaer i forhold til åbne fakturaer eller behandle en refusion til kunden for en åben kreditnota.

> [!NOTE]
> Betaling eller udligning af delbeløb understøttes ikke endnu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]