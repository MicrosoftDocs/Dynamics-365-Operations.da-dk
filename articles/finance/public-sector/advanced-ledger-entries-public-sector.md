---
title: Avancerede finansposter i den offentlige sektor
description: Dette emne forklarer, hvordan organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AdvancedLedgerEntry, BudgetControlConfiguration, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 19511
ms.assetid: 3db0233e-d767-4dc0-b008-733098b6ca70
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72959a232833552e0c9a6c4529c86fe7a66dcc90
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734412"
---
# <a name="advanced-ledger-entries-in-the-public-sector"></a>Avancerede finansposter i den offentlige sektor

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter. For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt.

## <a name="how-do-i-set-up-advanced-ledger-entries"></a>Hvordan konfigurerer jeg avancerede finansposter?

Kontroller, at nøglen **Licenskonfiguration** for **Avanceret finanspost** er valgt på siden **Licenskonfiguration**. Avancerede finansposter kræver bogføringsdefinitioner til Finans. Disse bogføringsdefinitioner kan indstilles til at generere flere, afstemte finansposter baseret på finanskontoen, der er angivet på siden **Avancerede finansposter**. Du kan finde flere oplysninger om bogføringsdefinitioner for avancerede finansposter under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).

## <a name="can-i-use-budget-control-with-advanced-ledger-entries"></a>Kan jeg bruge budgetstyring med avancerede finansposter?
Ja. Hvis organisationen bruger budgetstyring, kan du aktivere budgetstyring for avancerede finansposter på siden **Konfiguration af budgetstyring**.

## <a name="can-i-use-advanced-ledger-entries-with-projects"></a>Kan jeg bruge avancerede finansposter i projekter?
Ja. Hvis du ønsker, at brugere skal kunne ændre de økonomiske dimensioner for et projekt på den avancerede finanspostlinje, skal du vælge indstillingen **Tillad redigering af økonomiske dimensioner i formen for avanceret finanspostering** på siden **Finansparametre**. Hvis du ikke vælger denne indstilling, kan brugere kun ændre de økonomiske dimensioner i feltet **Finanskonto**, hvis de økonomiske dimensioner ikke er de økonomiske standarddimensioner for et projekt.

## <a name="how-do-i-use-advanced-ledger-entries-to-record-year-end-accrual-entries"></a>Hvordan bruger jeg avancerede finansposter til at registrere årsafslutning periodiseringsposter?
Opret en avanceret finanspost, vælg indstillingen **Tilbageførsel** indstilling, og angiv en tilbageførselsdato. Den tilbageførte avancerede finanspost oprettes, når den avancerede finanspost er bogført. Den tilbageførte avancerede finanspost har et nyt posteringsnummer og kladdestatus. Tilbageførselsdatoen bruges som regnskabsdatoen, og debet- eller kreditbeløbet på hver linje i den oprindelige post tilbageføres. Den samme bogføringsdefinition bruges. Posteringstekst til headeren og linjerne indeholder ordene "Tilbagefører post fra", posteringsnummeret for den oprindelige avancerede finanspost og posteringsteksten for den oprindelige avancerede finanspost.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
