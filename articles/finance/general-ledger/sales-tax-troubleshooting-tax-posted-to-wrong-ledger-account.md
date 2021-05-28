---
title: Momsen er bogført på den forkerte finanskonto i bilaget
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe, når moms bogføres på den forkerte finanskonto i bilaget.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020085"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Momsen er bogført på den forkerte finanskonto i bilaget

[!include [banner](../includes/banner.md)]

Under bogføringen kan momsen blive bogført på den forkerte finanskonto i bilaget. Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov. I eksemplerne i dette emne bruges en salgsordre som virksomhedsdokument.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Find momskoden for den forkerte bogførte momspostering

1. Vælg den postering, du vil arbejde med, på siden **Bilagsposteringer**, og vælg derefter **Bogført moms**.

    [![Knappen Bogført moms på siden Bilagsposteringer](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Gennemse værdien i feltet **Momskode**. I dette eksempel er værdien **Moms 19**.

    [![Feltet Momskode på siden Bogført moms](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Kontrollere finanskonteringsgruppen for momskoden

1. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.
2. Find og vælg momskoden, og gennemse derefter værdien i feltet **Finanskonteringsgruppe**. I dette eksempel er værdien **Moms**.

    [![Feltet Finanskonteringsgruppe på siden Momskoder](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Værdien i feltet **Finanskonteringsgruppe** er et link. Vælg linket for at få vist detaljerne om gruppens konfiguration. Du kan også vælge og holde (eller højreklikke) i feltet og derefter vælge **Vis detaljer**.

    [![Kommandoen Vis detaljer](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Kontrollér, at kontonummeret er korrekt i overensstemmelse med transaktionstypen i feltet **Skyldig moms**. Hvis ikke, skal du vælge den rette konto til bogføringen. I dette eksempel skal momsen for salgsordren bogføres på kontoen for skyldig moms 222200.

    [![Feltet Skyldig moms på siden Finanskonteringsgrupper](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Følgende tabel indeholder oplysninger om hvert felt på siden **Finanskonteringsgrupper**.

    | Felt                  | Betegnelse |
    |------------------------|-------------|
    | Moms, der skal betales      | Hovedkontoen for udgående salgsmoms, der er skyldig til skattevæsenet. |
    | Moms, der skal modtages   | Hovedkontoen for indgående moms, der er modtaget fra skattevæsenet. |
    | Udgift for importmoms        | Den hovedkonto, der bruges til at bogføre fradragsberettiget brugsafgifter, som leverandører ikke indberetter til skattevæsenet som del af EU's modtagermoms for varer og tjenesteydelser (GST)/Harmonized Sales Tax (HST). **Importmoms** skal være valgt for momskoden i den momsgruppe, der bruges i transaktionen. Dette felt er ikke tilgængeligt, hvis indstillingen **Anvend momsregler** er valgt på siden **Finansparametre**. |
    | Skyldig importmoms        | Den hovedkonto, der bruges til at bogføre indgående importmoms, som skal betales til skattevæsenet. |
    | Afregningskonto     | Den hovedkonto, der bruges til at bogføre nettosaldoen for de finanskonti, der er angivet i felterne **Skyldig importmoms** og **Indgående moms**. |
    | Kreditor kasserabat   | Den hovedkonto, der bruges til at bogføre en kasserabat for de momskoder, der er tilknyttet denne finanskonteringsgruppe. |
    | Debitor, kasserabat | Den hovedkonto, der bruges til at bogføre en kasserabat for de momskoder, der er tilknyttet denne finanskonteringsgruppe. |

    Du kan finde flere oplysninger i [Opsætning af finanskonteringsgrupper til moms](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Løse fejl i kode for at kontrollere finansdimensioner

I koden bestemmes bogføringskontoen af finansdimensionen. Finansdimensionen gemmer post-id'et for en konto i databasen.

1. I forbindelse med en salgsordre skal du tilføje et pausepunkt ved metoderne **Moms::saveAndPost()** og **Moms::post()**. Vær opmærksom på værdien af **\_ledgerDimension**.

    [![Eksempel på en salgsordrekode med et pausepunkt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    For en indkøbsordre skal du tilføje et pausepunkt ved metoderne **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()**. Vær opmærksom på værdien af **\_ledgerDimension**.

    [![Eksempel på en indkøbsordrekode med et pausepunkt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Kør følgende SQL-forespørgsel for at finde frem til visningsværdien for kontoen i databasen baseret på det post-id, der er gemt af finansdimensionen.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Visningsværdi for post-id'et](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Undersøg kaldstakken for at finde den værdi for **_ledgerDimension**, der er tildelt. Normalt hentes værdien fra **TmpTaxWorkTrans**. I dette tilfælde skal du tilføje et pausepunkt ved **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** for at finde den tildelte værdi.

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger

Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
