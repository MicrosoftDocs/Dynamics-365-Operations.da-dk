---
title: Konfigurer betalingsfakturascenarier
description: "I dette emne beskrives, hvordan du kan konfigurere Dynamics 365 for Retail til at understøtte forskellige scenarier relateret til fakturabetalinger."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a>Konfigurer betalingsfakturascenarier

[!include [banner](includes/banner.md)]

Funktionen Betale en faktura i Dynamics 365 for Retail er blevet udvidet for at understøtte:
- Udbetaling af flere salgsordrefakturaer i en enkelt POS-transaktion.
- Betaling af forskellige debitorfakturatyper, herunder fritekstfakturaer, projektbaserede fakturaer og kreditnotaer.

Hvis du vil aktivere disse scenarier, skal funktionalitetsprofilen for butikker være konfigureret som beskrevet nedenfor.  

1. Gå til **Detail > Konfiguration af kanal > POS setup > POS-profiler > Funktionalitetsprofiler**, og vælg en profil, der er knyttet til de butikker, som du vil foretage ændringerne for.

1. På fanen **Funktioner** kan du konfigurere følgende parametre efter behov.

    - **Salgsordrefaktura** - Vælg **Ja** for at give brugere mulighed for at betale en eller flere salgsordrebaserede fakturaer i en enkelt POS-transaktion.

    - **Fritekstfaktura** - Vælg **Ja** for at give brugere mulighed for at betale en eller flere fritekstbaserede fakturaer i en enkelt POS-transaktion.

    - **Projektfaktura** - Vælg **Ja** for at give brugerne mulighed for at betale en eller flere projektbaserede fakturaer i en enkelt POS-transaktion.

    - **Salgsordre kreditnota** – Vælg **Ja** for at tillade brugere at udligne flere salgsordrebaserede kreditnotaer i forhold til åbne fakturaer eller behandle en refundering til kunden for en åben kreditnota.

> [!NOTE]
> Betaling eller udligning af delbeløb understøttes ikke endnu.

