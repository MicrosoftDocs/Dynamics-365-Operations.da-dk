---
title: Konfigurere A-skattekoder for TDS-skattetypen
description: Denne artikel forklarer, hvordan du opretter koder for afgifter fratrukket ved kilden (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fabe14b74c445434c37cb6ee79597d37affb162d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904377"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Konfigurere A-skattekoder for TDS-skattetypen

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du opretter koder for afgifter fratrukket ved kilden (TDS).

1. Gå til **Moms \> Indirekte skatter \> A-skat \> Koder for A-skat**.

    [![Siden Koder for indeholdt skat.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Vælg **Ny** i handlingsruden for at oprette en kode for A-skat til TDS, og angiv de nødvendige oplysninger.
3. I feltet **Skattetype** i oversigtspanelet **Generelt** skal du vælge **TDS** for at kategorisere afgiftskoden som en TDS-afgiftskode.
4. Vælg TDS-afregningsperioden for TDS-afgiftskoden i feltet **Afregningsperiode**.
5. Vælg den finanskonto, som TDS-beløbet skal bogføres på, i feltet **Hovedkonto**.
6. I feltet **Debitorkonto** skal du vælge den debitorkonto, som det TDS-beløb, der trækkes fra i salgstransaktionerne, skal bogføres på.

    Feltet **Grundlag** indstilles automatisk til **Procent af bruttobeløb**, og værdien kan ikke ændres.

    > [!NOTE]
    > Du kan ikke indstille grundlaget til **Procentdel af nettobeløb** for afgiftskoder af TDS-afgiftstypen.

7. Vælg TDS-afgiftskomponenten for TDS-afgiftskoden i feltet **A-skat-komponent**.
8. Vælg **Værdier** i handlingsruden for at åbne siden **Værdier for A-skat**.
9. Angiv startdatoen for TDS-værdien i feltet **Fra-dato**. Angiv slutdatoen i feltet **Til-dato**.

    > [!NOTE]
    > Felterne **Minimumsgrænse**, **Øvre grænse** og **Udelad %** er ikke tilgængelige for afgiftskoder af TDS-afgiftstypen.

10. Angiv procentdel af TDS for TDS-afgiftskoden i feltet **Værdi**.
11. Luk siden **Værdier for A-skat** for at vende tilbage til siden **Koder for indeholdt skat**.

    > [!NOTE]
    > Knappen **Grænser** på siden **Koder for indeholdt skat** er ikke tilgængelig for afgiftskoder af TDS-afgiftstypen.

12. Luk siden.
