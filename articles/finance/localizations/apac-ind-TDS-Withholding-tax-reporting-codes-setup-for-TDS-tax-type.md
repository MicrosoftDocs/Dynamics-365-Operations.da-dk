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
ms.openlocfilehash: c74132af95f088ea88155b722a8270861fba50e7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361280"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Konfigurere rapporteringskoder for A-skat for TDS-skattetypen

[!include [banner](../includes/banner.md)]

A-skatterapporteringskoder bruges til at generere Formular 26Q- og Formular 27Q-opgørelser til afgifter fratrukket ved kilden (TDS). Dette emne forklarer, hvordan du konfigurerer trin i rapporteringskoder for A-skat, så du kan konfigurere TDS-rapporteringskoder.

1. Gå til **Moms \> Opsætning \> A-skat \> A-skatterapporteringskoder**.

    [![Siden A-skatterapporteringskoder.](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

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
