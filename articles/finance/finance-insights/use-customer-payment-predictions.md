---
title: Bruge forudsigelser om kundebetalinger
description: Denne artikel gennemgår forudsætningerne og de generelle trin, der er nødvendige for at kunne bruge en prøveversion af Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 330642624b55a6772ef149b70873021401a6bd83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901396"
---
# <a name="use-customer-payment-predictions"></a>Bruge forudsigelser om kundebetalinger

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan bruge debitorbetalingsforudsigelser. Før du bruger denne funktion, skal du sikre dig, at du har fuldført opsætningstrinnene for den. Du kan finde flere oplysninger under [Aktivere forudsigelser for debitorbetaling](enable-cust-paymnt-prediction.md).

Du kan få vist forudsigelse af debitorbetalinger i arbejdsrådet **Administrer kundekredit og rykkere** og på to nye listesider: **Forudsigelser for transaktionsbetaling** og **Forudsigelser om debitorbetalinger**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Arbejdsområde til at administrere debitors kredit og rykkere

Arbejdsområdet **Administrer kundekredit og rykkere** indeholder to nye felter: **Forudsigelser for transaktionsbetaling** og **Forudsigelser om debitorbetalinger**.

### <a name="transaction-payment-predictions-list-page"></a>Listesiden Forudsigelser for transaktionsbetaling

På listesiden **Forudsigelser for transaktionsbetaling** kan du få vist betalingssandsynligheden for åbne posteringer i områderne **Til tiden**, **Forsinket** og **Meget forsinket**. For hver postering i gitteret vises kolonnen **Til tiden-sandsynlighed** den sandsynlighed, at fakturaen betales på eller før forfaldsdatoen. Hvis sandsynligheden for en betaling til tiden er mindre end 50 procent, vises der en rød cirkel ud for procenttallet i kolonnen **Til tiden-sandsynlighed** for at angive risikoen for forsinket betaling.

[![Betalingsforudsigelse pr. transaktionsside.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Ruden **Relaterede oplysninger** i højre del af siden vises flere oplysninger om forudsigelser:

- For den post, der er valgt i gitteret, viser oversigtspanelet **Betalingsforudsigelse** for områderne **Til tiden**, **Forsinket** og **Meget forsinket**. Sektionen **Topfaktorer** viser de vigtigste faktorer, der har påvirket forudsigelser. Topfaktorer er attributter for den valgte postering og/eller kunden for den pågældende postering.
- Oversigtspanelet **Customer Insights** viser statistik for den aktuelle faktura, betaling og rykker for kunden i den valgte postering.
- Oversigtspanelet **Debitorhistorik** viser debitorens betalingshistorik i områderne **Til tiden**, **Forsinket** og **Meget forsinket**.

Dataene i sektionen **Topfaktorer** og i oversigtspanelerne **Customer Insights** og **Kundehistorik** hjælper med at forklare betalingsforudsigelser. Det kan være med til at øge din tillid til forudsigelsers effektivitet.

[![Grafiske indikatorer for betalingsforudsigelser i ruden Relaterede oplysninger.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Listesiden Forudsigelser om debitorbetalinger

Listesiden **Forudsigelser om debitorbetalinger** viser den samlede åbne saldo og det forventede beløb, der skal betales, i områderne **Til tiden**, **Forsinket** og **Meget forsinket**.

[![Betalingsforudsigelser pr. kundeside.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Betalingsbeløbet i hvert sæt beregnes som summen af det vejede gennemsnit af transaktionssaldoen. Dette beløb beregnes ud fra betalingssandsynlighederne i hvert sæt.

En kunde har f. eks. tre åbne posteringer, der har følgende betalingssandsynligheder i hvert sæt.

| Postering | Beløb | Sandsynlighed for betaling til tiden | Sandsynlighed for forsinket betaling | Sandsynlighed for meget forsinket betaling |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 procent                  | 50 procent               | 40 procent                    |
| T2          | 1.000  | 50 procent                  | 30 procent               | 20 procent                    |
| T3          | 10,000 | 1 procent                   | 4 procent                | 95 procent                    |

I dette tilfælde projiceres betalinger for hver enkelt sæt på følgende måde.

| Sæt   | Postering T1      | Postering T2         | Postering T3            | Sum |
|-----------|---------------------|------------------------|---------------------------|-------|
| Til tiden   | 100 × 10 ÷ 100 = 10 | 1.000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| For sent      | 100 × 50 ÷ 100 = 50 | 1.000 × 30 ÷ 100 = 300 | 10.000 × 4 ÷ 100 = 400    | 750   |
| Meget forsinket | 100 × 40 ÷ 100 = 40 | 1.000 × 20 ÷ 100 = 200 | 10.000 × 95 ÷ 100 = 9.500 | 9,740 |

Sektionen **Relaterede oplysninger** i højre del af siden viser flere oplysninger om forudsigelser:

- For den post, der er valgt i gitteret, viser oversigtspanelet **Betalingsforudsigelser** for områderne **Til tiden**, **Forsinket** og **Meget forsinket**.
- Oversigtspanelet **Customer Insights** viser statistik for den aktuelle faktura, betaling og rykker for kunden i den valgte postering.
- Oversigtspanelet **Debitorhistorik** viser debitorens betalingshistorik i områderne **Til tiden**, **Forsinket** og **Meget forsinket**.

Dataene i oversigtspanelerne **Debitorindsigt** og **Debitorhistorik** hjælper med at forklare betalingsforudsigelser. Det kan være med til at øge din tillid til forudsigelsers effektivitet.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Bedre nøjagtighed af kontantforudsigelser

Du kan få vist nøjagtigheden af kontantforudsigelser ved at gå til **Kredit- og rykkere \> Opsætning \> Finance Insights \> Finance Insights-parametre**. Under fanen **Indsigt i debitorbetaling** viser afsnittet **Forudsigelsesmodel** præcisionen af forudsigelsesmodellen som en procentdel.

Hvis du ikke er tilfreds med nøjagtigheden, skal du vælge linket **Forbedring af modellens nøjagtighed** for at åbne AI Builder-udvidelsesoplevelsen. I udvidelsen af AI Builder kan du vælge eller annullere markeringen af felter, indtil du har valgt de felter, du mener er de vigtigste for præcist at forudsige betalingssandsynligheder. Når du er færdig, kan du nemt genregistrere prognosemodellen og udgive dine ændringer. Den nyoplærte forudsigelsesmodel vælges automatisk til forudsigelser i Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
