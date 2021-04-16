---
title: Udskriv rapporten Momsbetaling efter kode
description: Dette emne indeholder oplysninger om de indstillinger og handlinger, der kræves for at udskrive rapporten Momsafregning efter kode i regnskabs- eller momskodevalutaen.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815446"
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

    ![Dialogboksen Momsafregning pr. kode](media/Sales-tax-payment-by-code.png)

I følgende illustration vises et eksempel på den rapport, der genereres. Rapporten viser, at rapporteringskode **101** har valutaen **EUR**, hvis feltet **Momsvaluta** er angivet til **EUR** for den momskode, som rapporteringskoden er tildelt.

![Eksempel på rapporten Momsbetaling efter kode](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]