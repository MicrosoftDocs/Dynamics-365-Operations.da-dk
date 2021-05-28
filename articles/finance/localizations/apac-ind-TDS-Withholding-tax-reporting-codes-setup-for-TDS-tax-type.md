---
title: Konfigurere rapporteringskoder for A-skat for TDS-skattetypen
description: A-skatterapporteringskoder bruges til at generere Formular 26Q- og Formular 27Q-opgørelser til afgifter fratrukket ved kilden (TDS). Dette emne forklarer, hvordan du konfigurerer trin i rapporteringskoder for A-skat, så du kan konfigurere TDS-rapporteringskoder.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023128"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Konfigurere rapporteringskoder for A-skat for TDS-skattetypen

[!include [banner](../includes/banner.md)]

A-skatterapporteringskoder bruges til at generere Formular 26Q- og Formular 27Q-opgørelser til afgifter fratrukket ved kilden (TDS). Dette emne forklarer, hvordan du konfigurerer trin i rapporteringskoder for A-skat, så du kan konfigurere TDS-rapporteringskoder.

1. Gå til **Moms \> Opsætning \> A-skat \> A-skatterapporteringskoder**.

    [![Siden A-skatterapporteringskoder](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. Vælg **TDS** i feltet **Skattetype** for at definere A-skatterapporteringskode for TDS-skattetypen.
3. Vælg den TDS-komponent, du definerer rapporteringskoden for A-skat for, i feltet **A-skat-komponent**. I feltet **A-skat-komponentgruppe** vises den TDS-komponentgruppe, der blev defineret for den TDS-komponent, som du definerer.

    Feltet **Sektionskode** i oversigtspanelet **Generelt** viser den sektionskode, der er knyttet til TDS-komponentgruppen.

4. Vælg TDS-rapporteringskoden i feltet **Rapporteringskode** i oversigtspanelet **Generelt**:

    - TDS
    - TCS
    - Tillæg
    - PE\_Cess
    - SHE\_Cess

5. Luk siden.
