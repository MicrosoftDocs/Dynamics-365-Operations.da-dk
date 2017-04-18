---
title: Rette en fritekstfaktura
description: "I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Rette en fritekstfaktura

I denne artikel beskrives det, hvordan du retter en fritekstfaktura, der er bogført, og genudsteder den som en rettet faktura.

For at rette en fritekstfaktura, der allerede er bogført, skal du åbne den bogførte fritekstfaktura. På den **faktura** side, vælge **annullere**, og vælg derefter **korrekte faktura**. Vælg en årsagskode, tilføj kommentarer, og vælg datoen for den nye rettede faktura. Du kan ændre den rettede faktura og bogføre den. 

Når du bogfører den rettede faktura, oprettes der en annullering af fakturaen for et kreditbeløb, der er lig med det oprindelige fakturabeløb. Derfor bliver den samlede saldo af den oprindelige faktura og annulleringen af fakturaen 0 (nul). Annulleringen af fakturaen udlignes mod den oprindelige faktura. 

Når du bogfører den rettede faktura, har du tre fakturaer:

-   **Oprindelig faktura** – Den faktura, der indeholder de oplysninger, du skal rette.
-   **Annulleringsfaktura** – Den systemgenererede kreditfaktura, der er oprettet for at annullere den faktura, der senest er rettet.
-   **Rettet faktura** – Den faktura, der indeholder oplysninger om den rettede faktura.

Du kan identificere annullerede og rettede fakturaer på to måder:

-   Siden **Alle fritekstfakturaer** indeholder en kolonne af typen **Rettelse**, hvor du kan se, hvilke fakturaer der er annullerede fakturaer og rettede fakturaer.
-   Overskriften for fritekstfakturaen viser en status for **Cancelling faktura '\[fakturanummer\]'** eller **Corrected faktura '\[fakturanummer\]'**.

> [!NOTE]
> Denne funktion er tilgængelig kun, hvis den **gratis rettelse af fritekstfaktura** er valgt som konfigurationsnøgle.

