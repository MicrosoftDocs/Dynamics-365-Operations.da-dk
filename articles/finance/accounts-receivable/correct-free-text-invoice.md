---
title: Rette en fritekstfaktura
description: I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fccd6dbb33efd1556c56a6d92ad191ecfd317fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878183"
---
# <a name="correct-a-free-text-invoice"></a>Rette en fritekstfaktura

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.

Hvis du vil rette en fritekstfaktura eller salgsfaktura, der allerede er bogført, skal du åbne den bogførte fritekstfaktura. På siden **Faktura** skal vælge **Annuller** og derefter vælge **Ret faktura**. Vælg en årsagskode, tilføj kommentarer, og vælg datoen for den nye rettede faktura. Du kan ændre den rettede faktura og bogføre den. 

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
