---
title: Justering af datoscenarier
description: Dette emne indeholder eksempler på, hvordan justeringsdatoer fungerer i abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 91480fecd16cf8417722df73c28bbd81d029fb07
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690467"
---
# <a name="alignment-date-scenarios"></a>Justering af datoscenarier

Dette emne indeholder eksempler på, hvordan justeringsdatoer fungerer i abonnementsfakturering.

I disse eksempler har en faktureringsdetalje for en faktureringsplan 31. oktober 2019 en justeringsdato. Den første faktureringsdetalje for linjen slutter d. 31. oktober 2019 og forholdsmæssigt. Linjen fornys automatisk med startdatoen for fornyelse den 11. november.

> [!NOTE]
> Året er relevant, da det kan medføre, at justeringsdatoen er mere eller mindre end et år. Den metode, der bruges til beregning af proportionalitet, er angivet på til **Månedlig** på siden **Parametre for tilbagevendende kontraktfakturering**. Hvis den er angivet til **Daglig**, er der nogle delbeløb, der er forskellige.

## <a name="scenario-1-no-alignment"></a>Eksempel 1: Ingen justering

Faktureringsplanen konfigureres med følgende data:

- **Startdato:** 1 maj 2019
- **Slutdato:** 31 december 2024
- **Beløb:** $1.000

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.5.2019 | 4/30/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.5.2020 | 30.4.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.5.2021 | 30.4.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.5.2022 | 30.4.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.5.2023 | 30.4.2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.5.2024 | 31-12-2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Eksempel 2: Afkortet justering

Faktureringsplanen konfigureres med følgende data:

- **Startdato:** 1 maj 2019
- **Slutdato:** 31 december 2024
- **Beløb:** $1.000
- **Justeringsdato:** 31. december 2019

Det første fornyelsesbeløb er for mindre end et år.

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.5.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 12/31/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Eksempel 3: Udvidet justering

Faktureringsplanen konfigureres med følgende data:

- **Startdato:** 1 maj 2019
- **Slutdato:** 31 december 2024
- **Beløb:** $1.000
- **Justeringsdato:** 31. december 2020

Det første fornyelsesbeløb er for mere end et år.

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.5.2019 | 12/31/2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1.1.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Eksempel 4: Justering med en anden slutmåned

Faktureringsplanen konfigureres med følgende data:

- **Startdato:** 1 maj 2019
- **Slutdato:** 31. oktober 2024
- **Beløb:** $1.000
- **Justeringsdato:** 31. december 2019

> [!NOTE]
> Dette scenarie er ikke almindeligt.

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.5.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 12/31/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Eksempel 5: Enkelt delår

Faktureringsplanen konfigureres med følgende data:

- **Startdato:** 1 maj 2019
- **Slutdato:** 31 december 2019
- **Beløb:** $1.000
- **Justeringsdato**: 31. december 2019

I dette scenario er det ikke nødvendigt med justeringsdatoen. Dette scenario bruges ofte til automatisk fornyelse.

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.5.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Eksempel 6: Beregnede datoer

Understøttelse og fornyelse er konfigureret med følgende data:

- **Tilsidesæt startdato:** Nej
- **Understøttelses- og fornyelsesdatoer:** Startdato for næste måned
- **Faktura, bogføringsdato:** 22 juni 2019
- **Justeringsdato:** 31. december 2020

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 1.7.2019 | 31.7.2019 | | | 1.00 | | 1.00 | 297.60 |
| 1.8.2019 | 12/31/2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Eksempel 7: Beregnede datoer og fremtidig bogføring

Understøttelse og fornyelse er konfigureret med følgende data:

- **Tilsidesæt startdato:** Nej
- **Understøttelses- og fornyelsesdatoer:** Startdato for næste måned
- **Faktura, bogføringsdato:** 22 juni 2019
- **Justeringsdato:** 31. december 2020

I dette scenario ændres justeringsdatoen til 31. december 2021.

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 22.6.2019 | 22.6.2019 | | | 1.00 | | 1.00 | 0,00 |
| 1.8.2019 | 12/31/2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Eksempel 8: Manuelle datoer og flere år

Understøttelse og fornyelse er konfigureret med følgende data:

- **Tilsidesæt startdato:** Ja
- **Startdato for fornyelse:** 1 juli 2020
- **Slutdato for fornyelse:** 31 december 2024
- **Justeringsdato:** 31. december 2021

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 22.6.2019 | 22.6.2019 | | | 1.00 | | 1.00 | 0,00 |
| 1.7.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 1.1.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 1.1.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Eksempel 9: Manuelle datoer, flere år og en anden slutmåned

Understøttelse og fornyelse er konfigureret med følgende data:

- **Tilsidesæt startdato:** Ja
- **Startdato for fornyelse:** 1 juli 2020
- **Slutdato for fornyelse:** 31 oktober 2024
- **Justeringsdato:** 31. december 2021

| Faktureringsstartdato | Faktureringsslutdato | Forrige læsning | Aktuel læsning | Angivet antal | Ledigt antal | Fakturerbart antal | Enhedspris |
|---|---|---|---|---|---|---|---|
| 22.6.2019 | 22.6.2019 | | | 1.00 | | 1.00 | 0,00 |
| 1.7.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 1.1.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 1.1.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Eksempel 10: Justering uden forholdsmæssig justering

Understøttelse og fornyelse er konfigureret med følgende data:

- **Tilsidesæt startdato:** Nej
- **Faktura, bogføringsdato:** 22 juni 2019
- **Justeringsdato:** 31. december 2019

Startdatoen for fornyelse og justeringsdatoerne justeres, så begge startdatoer ligger efter bogføringsdatoen.

- **Startdato for fornyelse:** 1 januar 2020
- **Slutdato for fornyelse:** 31 december 2020
