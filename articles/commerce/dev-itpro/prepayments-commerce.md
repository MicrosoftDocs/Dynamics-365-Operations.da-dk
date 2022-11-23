---
title: Forudbetalinger i Dynamics 365 Commerce
description: Denne artikel indeholder en oversigt over behandlingen af forudbetalingstransaktioner i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780352"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Forudbetalinger i Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over behandlingen af forudbetalingstransaktioner i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce behandler forudbetalingsposteringer for følgende betalingstyper, der bruges i Debitor eller Handel:

- **Indbetaling på debitorkonto** – En kunde betaler en indbetaling på POS. Ved handel behandles indbetalingsbetalingen som en forudbetalingspostering. Når du bogfører posteringen, oprettes og bogføres der en betalingskladde på siden **Kladdebilag** i Commerce Headquarters. Afkrydsningsfeltet **Kladdebilag for forudbetaling** under fanen **Betaling** markeres automatisk for betalingskladden. Yderligere oplysninger, herunder forudbetaling og skattespecifikke oplysninger, der er relevante for målområdet, finder du i [Globaliseringsressourcer – indhold med lande-/regionsspecifik hjælp](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Debitorordre med et depositum** – En kunde opretter en debitorordre i POS. Kunden kan betale en indbetaling for ordren baseret på den standardindbetalingsprocent, der er konfigureret på siden **Kundeordrer** i Commerce Headquarters (**Commerce-parametre \> Kundeordrer**). Ved handel behandles indbetalingsbetalingen for kundeordrer som en forudbetalingspostering. Når du bogfører posteringen, oprettes og bogføres der en betalingskladde på siden **Kladdebilag** i Commerce Headquarters. Afkrydsningsfeltet **Kladdebilag for forudbetaling** under fanen **Betaling** markeres automatisk for betalingskladden. Betalingen udlignes, og debitorfakturaen udstedes automatisk, når ordren afhentes eller leveres.
- **Salgsordre til callcenter** – En kundeservicemedarbejder hos callcenter opretter en salgsordre på vegne af en kunde, og **forudbetalingsattributten** angives til **Ja** under betalingsregistreringen.

Ved handel udføres følgende opgaver for at behandle en forudbetaling:

- **Behandling af indbetalinger på en debitorkonto** – En indbetalingsbetaling, som en kunde foretager, overføres til Commerce ved hjælp af en tjeneste, der synkroniserer data. Ved Commerce oprettes en detailbetalingstransaktion for betalingen. Når du bogfører detailtransaktionen, bogføres en kontantkladde eller en debitorbetalingskladde. Afkrydsningsfeltet **Bilag for forudbetalingskladde** under fanen **Betaling** på siden **Kladdebilag** i Commerce Headquarters markeres automatisk for betalingskladden. Forudbetalinger kan ikke behandles, hvis betalingsbeløbet er negativt.
- **Behandling af en debitorordre eller salgsordre med en indbetaling** – En kunde betaler en påkrævet indbetaling for en debitorordre ved hjælp af Commerce Data Exchange: Realtidsservice. Ved handel oprettes enten en debitorbetalingskladde eller en kontantkladde, afhængigt af den betalingsmåde, kunden bruger. Afkrydsningsfeltet **Bilag for forudbetalingskladde** under fanen **Betaling** på siden **Kladdebilag** markeres automatisk for betalingskladden i Commerce Headquarters. Hvis en kunde bruger flere betalingsmåder til delvise betalinger, behandler Commerce hver delbetaling baseret på den betalingsmåde, der er brugt.

I forbindelse med kreditkort og for digitale kreditkort, der har underliggende betalingsmåder med kreditkort, sender Commerce en anmodning om hentning, efter at den er godkendt korrekt. (Der registreres midler, før salgsordren faktureres).

Hvis du annullerer en kundeordre, refunderes forudbetalingsbeløbet, og der bogføres en betalingskladde for indbetalingsbeløbet. Refusionsbeløbet beregnes og bogføres på baggrund af den betalingsmåde, du angav, da du bogførte refusionsbetalingen. Handel kan anvende et annulleringsgebyr baseret på den procentdel, du har angivet på siden **Commerce-parametre** i Commerce headquarters.

Hvis du returnerer en kundeordre, oprettes der en returordre og en betalingskladde for refusion. Når du bogfører returordren, opretter Commerce enten en debitorbetalingskladde eller en kontantkladde, afhængigt af den betalingsmåde, kunden har brugt til den oprindelige transaktion.
