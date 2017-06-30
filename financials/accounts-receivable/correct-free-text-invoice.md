---
title: Rette en fritekstfaktura
description: "I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a143a373a63ab145ee4c25bb1abfab777cca6619
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="correct-a-free-text-invoice"></a>Rette en fritekstfaktura

[!include[banner](../includes/banner.md)]


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
> Denne funktion er kun tilgængelig, hvis konfigurationsnøglen **Fri tekst til rettelse af faktura** er valgt.




