---
title: Rette en fritekstfaktura
description: I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3cc07a1f0ba444250eddcf892681e2ca63e9c1a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780469"
---
# <a name="correct-a-free-text-invoice"></a>Rette en fritekstfaktura

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.

Ret en fritekstfaktura, der allerede er bogført: 
1. Åbn bogførte fritekstfakturaer. 
2. På siden **Faktura** skal vælge **Annuller** og derefter vælge **Ret faktura**. 
3. Vælg en årsagskode, tilføj kommentarer, og vælg datoen for den nye rettede faktura.
4. Du kan ændre den rettede faktura og bogføre den. 

Når du bogfører den rettede faktura, oprettes der en annullering af fakturaen for et kreditbeløb, der er lig med det oprindelige fakturabeløb. Derfor bliver den samlede saldo af den oprindelige faktura og annulleringen af fakturaen 0 (nul). Annulleringen af fakturaen udlignes mod den oprindelige faktura. 

Når du bogfører den rettede faktura, har du tre fakturaer:

-   **Oprindelig faktura** – Den faktura, der indeholder de oplysninger, du skal rette.
-   **Annulleringsfaktura** – Den systemgenererede kreditfaktura, der er oprettet for at annullere den faktura, der senest er rettet.
-   **Rettet faktura** – Den faktura, der indeholder oplysninger om den rettede faktura.

Du kan identificere annullerede og rettede fakturaer på to måder:

-   Siden **Alle fritekstfakturaer** indeholder en kolonne af typen **Rettelse**, hvor du kan se, hvilke fakturaer der er annullerede fakturaer og rettede fakturaer.
-   Overskriften for fritekstfakturaen viser en status for **Annulleringsfaktura '\[fakturanummer\]'** eller **Rettet faktura '\[fakturanummer\]'**.

> [!NOTE]
> Denne funktion er kun tilgængelig, hvis konfigurationsnøglen **Fri tekst til rettelse af faktura** er valgt. Du kan finde flere oplysninger om, hvordan du aktiverer konfigurationsnøgler, i afsnittet Aktivere (eller deaktivere) konfigurationsnøgler i artiklen [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
