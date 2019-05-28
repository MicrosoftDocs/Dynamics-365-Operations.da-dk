---
title: Modtagelse af blandede id'er
description: I dette emne beskrives, hvordan du bruger Modtagelse af blandede id'er til at registrere og oprette arbejde for flere varer med en mobilenhed.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44165bc59d65a9dfdf8e591152f427b97930b34
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569376"
---
# <a name="mixed-license-plate-receiving"></a>Modtagelse af blandede id'er

[!include [banner](../includes/banner.md)]

Med Modtagelse af blandede id'er kan du oprette et id, der består af flere varer, før du registrerer og opretter læg-på-lager-arbejde. 

Et id, der består af flere varer, behøver ikke at blive opdelt i modtagelsesområdet, for at du kan registrere de enkelte varer. 

Når du bruger en varerelateret proces til at identificere kildedokumentlinjerne, kan du scanne stregkoder på varekontrolelementet. Hvis der er konfigureret et antal og en måleenhed (UOM) i stregkoden, føjes varen og antallet automatisk til det blandede id, og du sendes tilbage til skærmbilledet for at scanne et andet element. Dette gør det muligt hurtigt at scanne alle varer uden at skulle foretage en bekræftelse på hvert trin. 

I processen til modtagelse af blandede id'er kan du få vist listen over varer, der allerede er indscannet i id'et, og herfra kan du ændre eller rette mængde eller antallet af en vare.

## <a name="where-it-applies"></a>Hvor det er relevant

Modtagelse af blandede id'er er en modtagelsesproces til mobilenheder, hvor du kan registrere og oprette arbejde for flere linjer/varer på samme tid. Dette er nyttigt, hvis du modtager indgående id'er med flere elementer. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Sådan konfigurerer du modtagelse af blandede id'er
Modtagelse af blandet nummerplade konfigureres som et menupunkt på en mobilenhed.

Du skal oprette et nyt menupunkt med tilstandsarbejde, der ikke bruger eksisterende arbejde, og bruge en af følgende metoder:

- Modtagelse af blandede id'er
- Modtagelse af blandede id'er og placering på lager

Indstillingerne til identifikation af kildedokumentlinjerne er indkøbsordrevare, indkøbsordrelinje, returordre, vare i flytteordre og flytteforslagslinje. Disse indstillinger kan ændre modtagelsesordren på et enkelt id. Den sidste indstilling er vare efter last. Du kan føje flere varer til et id, men du kan ikke skifte mellem flere laster.
