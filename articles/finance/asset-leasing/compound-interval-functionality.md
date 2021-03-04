---
title: Sammensætning af intervalfunktioner
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at vælge mellem måneds-, kvartårlige-, halvårlige og årlige sammensætningsintervaller.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c37da09f50448c27b20dfacccf2e7134b828f13b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441767"
---
# <a name="compounding-interval-functionality"></a>Sammensætning af intervalfunktioner

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne indeholder oplysninger, der kan hjælpe dig med at vælge mellem måneds-, kvartårlige-, halvårlige og årlige sammensætningsintervaller. Sammensætningsintervalfunktionen bruges til at bestemme antallet af perioder pr. år i en leasingaftales betalingsplan. Hver af de fire eksempler i dette emne viser, hvordan en leasingaftales betalingsplan vil se ud for et andet interval.

Du kan ikke vælge et sammensætningsinterval, der er mindre hyppig end leasingaftalens betalingsfrekvens. Et kvartårligt sammensætningsinterval kan f. eks. ikke bruges med en månedlig ydelsesfrekvens, og et årligt sammensætningsinterval kan ikke bruges med en halvårlig betalingsfrekvens. Hvis du prøver at vælge et sammensætningsinterval, der er mindre hyppig end leasingaftalens betalingsfrekvens, modtager du en fejlmeddelelse.

> [!NOTE]
> I alle fire eksempler i dette emne svarer sammensætningsintervallet til betalingsfrekvensen.

## <a name="examples"></a>Eksempler

### <a name="setup-for-all-four-leases"></a>Opsætning af alle fire leasingaftaler

Følgende tabeller viser de værdier, der er angivet under fanerne **Generelt** og **Betalingsplanlinjer** for de fire leasingaftaler, der bruges i eksemplerne.

Fanen **Generelt**

| Felt                      | Værdi                        |
|----------------------------|------------------------------|
| Trinvis lånesats | **5 %**                       |
| Annuitetstype               | **Almindelig annuitet**         |
| Sammensætningsinterval       | Se de individuelle eksempler. |
| Betalingshyppighed          | **Månedligt**                  |
| Dato for påbegyndelse          | **1-1-2020**                 |

**Betalingsplanlinjer-fane**

| Felt             | Værdi                        |
|-------------------|------------------------------|
| Igangsæt dato        | **1-1-2020**                 |
| Perioder           | **120**                      |
| Periodeinterval   | **Måneder**                   |
| Slutdato          | **31-12-2029**               |
| Betalingshyppighed | Se de individuelle eksempler. |
| Betalingsbeløb    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Leasingaftale 1: Månedlig sammensætningsinterval og månedlig betalingsfrekvens

Følgende tabel viser de første 12 måneder i betalingsplanen. Bemærk følgende oplysninger:

- Værdien i kolonnen "Periode" øges med 1. hver måned, fordi hver måned er et nyt sammensætningsinterval.
- I formlen i kolonnen "Nutidsværdi" divideres satsen med 12, fordi der er 12 sammensætningsperioder pr. år. Eksponenten (dvs. hævet skrift) svarer til værdien i kolonnen "Periode".

| Termin | Måned | Dato       | Betalingsbeløb | Nutidsværdi                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 1/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49.792,53  |
| 2      | 2     | 2/29/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49.585,92  |
| 3      | 3     | 3/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49.380,17  |
| 4      | 4     | 4/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49.175,28  |
| 5      | 5     | 5/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48.971,23  |
| 6      | 6     | 6/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48.768,03  |
| 7      | 7     | 7/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48.565,67  |
| 8      | 8     | 8/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48.364,15  |
| 9      | 9     | 9/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48.163,47  |
| 10     | 10    | 10/31/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47.963,62 |
| 11     | 11    | 11/30/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47.764,61 |
| 12     | 12    | 12/31/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47.566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Leasingaftale 2: Kvartårlig sammensætningsinterval og kvartårlig betalingsfrekvens

Følgende tabel viser de første 12 måneder i betalingsplanen. Bemærk følgende oplysninger:

- Værdien i kolonnen "Periode" øges med 1. hver måned, fordi hver måned er et nyt sammensætningsinterval.
- I formlen i kolonnen "Nutidsværdi" divideres satsen med 4, fordi der er fire sammensætningsperioder pr. år. Eksponenten er lig med værdien i kolonnen "Periode".

| Termin | Måned | Dato       | Betalingsbeløb | Nutidsværdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 1/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 2/29/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 3/31/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49.382,72 |
| 2      | 4     | 4/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 5/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 6/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48.773,05 |
| 3      | 7     | 7/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 8/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 9/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48.170,92 |
| 4      | 10    | 10/31/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 11/30/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 12/31/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47.576,21 |

> [!NOTE]
> Hvis annuiteten ændres til **Forfalden annuitet**, skal betalingen falde i begyndelsen af kvartalet i stedet for ved kvartalets slutning.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Leasingaftale 3: Halvårlig sammensætningsinterval og halvårlig betalingsfrekvens

Følgende tabel viser de første 12 måneder i betalingsplanen. Bemærk følgende oplysninger:

- Værdien i kolonnen "Periode" øges med 1. hver sjette måned (dvs halvårligt), fordi hver halve år er et nyt sammensætningsinterval.
- I formlen i kolonnen "Nutidsværdi" divideres satsen med 2, fordi der er to sammensætningsperioder pr. år. Eksponenten er lig med værdien i kolonnen "Periode".

| Termin | Måned | Dato       | Betalingsbeløb | Nutidsværdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 1/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 2/29/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 3/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 4/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 5/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 6/30/2020  | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48.780,49 |
| 2      | 7     | 7/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 8/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 9/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 10/31/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 11/30/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 12/31/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47.590,72 |

> [!NOTE]
> Hvis annuiteten ændres til **Forfalden annuitet**, vil betalingen ligge i januar og juli i stedet for juni og december.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Leasingaftale 4: Årlig sammensætningsinterval og årlig betalingsfrekvens

Følgende tabel viser de første 12 måneder i betalingsplanen. Bemærk følgende oplysninger:

- Værdien i kolonnen "Periode" øges med 1. hver sjette 12. måned (dvs årligt), fordi hver år er et nyt sammensætningsinterval.
- I formlen i kolonnen "Nutidsværdi" divideres satsen med 1, fordi der er en sammensætningsperiode pr. år. Eksponenten er lig med værdien i kolonnen "Periode".

| Termin | Måned | Dato       | Betalingsbeløb | Nutidsværdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 1/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 2/29/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 3/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 4/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 5/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 6/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 7/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 8/31/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 9/30/2020  | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 10/31/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 11/30/2020 | 0,00           | 0.00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 12/31/2020 | 50,000.00      | 50.000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47.619,05 |

> [!NOTE]
> Hvis annuiteten ændres til **Forfalden annuitet**, vil betalingen ligge i januar i stedet for december.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]