---
title: Udskriv rapporten Momsbetaling efter kode
description: Denne artikel indeholder oplysninger om de indstillinger og handlinger, der kræves for at udskrive rapporten Momsafregning efter kode i regnskabs- eller momskodevalutaen.
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272362"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Udskriv rapporten Momsbetaling efter kode 

[!include [banner](../includes/banner.md)]

Hvis du vil udskrive rapporten **Momsbetaling efter kode**, skal du gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsrapportér** \> **Momsbetaling efter kode**. Som standard genereres rapportbeløb i regnskabsvalutaen for den juridiske enhed for alle rapporteringskoder, der er konfigureret på siden **Momsrapporteringskoder**.

Du kan også generere denne rapport, så den viser momsafregningsbeløbene i valutaerne for momskoder for alle rapporteringskoder, der er knyttet til momskoder på siden **Momskoder**.

## <a name="turn-on-the-feature"></a>Slå funktionen til

I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktion: **Generér rapport over momsbetaling efter kode i momskodevalutaen**.

## <a name="run-the-report"></a>Kør rapporten

1. Gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsrapporter** \> **Momsbetaling efter kode**.
2. Vælg en af følgende værdier i feltet **Rapportvaluta**:

    - **Regnskabsvaluta** – Udskriv rapport beløbene i regnskabsvalutaen.
    - **Momskodevaluta** – Udskriv rapport beløbene i valutaerne for momskoder.

    ![Dialogboksen Momsbetaling efter kode.](media/Sales-tax-payment-by-code.png)

I følgende illustration vises et eksempel på den rapport, der genereres. Rapporten viser, at rapporteringskode **101** har valutaen **EUR**, hvis feltet **Momsvaluta** er angivet til **EUR** for den momskode, som rapporteringskoden er tildelt.

![Eksempel på rapporten Momsbetaling efter kode.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
