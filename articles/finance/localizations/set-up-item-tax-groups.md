---
title: Konfigurere varemomsgrupper
description: I dette emne beskrives, hvordan du konfigurerer varemomsgrupper i momsberegningstjenesten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883848"
---
# <a name="set-up-item-tax-groups"></a>Konfigurere varemomsgrupper

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer varemomsgrupper i momsberegningstjenesten. Det forklarer også, hvordan du konfigurerer matrixen for regler for anvendelse af varemomsgrupper og konfigurerer linjer i matrixen.

Begrebet varemomsgrupper i tjenesten Momsberegning minder om begrebet varemomsgrupper i Microsoft Dynamics 365 Finance. Det er grupper af momskoder. Tjenesten Momsberegning bruger skæringspunktet for en momsgruppe og en varemomsgruppe til at fastlægge momskoderne.

> [!IMPORTANT]
> Opsætningen af varemomsgrupper i tjenesten Momsberegning er afhængig af en juridisk enhed. Du kan kun fuldføre denne opsætning i Regulatory Configuration Service (RCS) én gang. Når du aktiverer tjenesten Momsberegning i Finans, synkroniseres varemomsgrupper automatisk for den valgte juridiske enhed.

## <a name="set-up-an-item-tax-group"></a>Konfigurere en varemomsgruppe 

Følg følgende trin for at konfigurere en varemomsgruppe.

1. Log på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbejdsområder** \> **Globaliseringsfunktioner** \> **Momsberegning**.
3. Vælg den funktion og version, du vil konfigurere, og vælg derefter **Rediger**.
4. Vælg **Konfigurationsversion** under fanen **Generelt**.
5. Vælg **Administrer kolonne** under fanen **Varemomsgruppe**. Hvis du konfigurerer en varemomsgruppe første gang, angives felterne i dialogboksen **Administrer kolonne** automatisk.
6. På listen til venstre skal du udvide noden **Linjer** og markere afkrydsningsfeltet for **Varemomsgruppe**.

    ![Varemomsgruppe, der er valgt under noden Linjer i dialogboksen Administrer kolonner.](media/select-item-tax-group.png)

7. Vælg knappen med højre pil for at føje **Varemomsgruppe** til listen **Valgte kolonner** til højre.

    ![Varemomsgruppe, der er føjet til listen Valgte kolonner.](media/add-item-tax-group.png)

8. Vælg **OK**.

## <a name="configure-an-item-tax-group"></a>Konfigurere en varemomsgruppe

Når du har konfigureret en varemomsgruppe, oprettes matrixen for reglen for anvendelse. Du kan føje linjer til matrixen for at konfigurere varemomsgruppen.

1. Vælg **Tilføj** under fanen **Varemomsgruppe**.
2. Skriv navnet på varemomsgruppen i feltet **Varemomsgruppe**.

    > [!IMPORTANT]
    > Det anbefales, at du begrænser navnet på varemomsgruppen til 10 tegn. Dette navn synkroniseres med Finans, hvilket har en grænse på 10 tegn for navne på varemomsgrupperne.

3. Markér afkrydsningsfeltet for hver momskode, du vil medtage i varemomsgruppen, i feltet **Momskoder**. Du kan medtage flere momskoder i én varemomsgruppe.

    ![Flere momskoder, der er valgt i feltet Momskoder.](media/multiple-tax-codes-selection.png)

4. Gentag trin 1-3 for at tilføje flere varemomsgrupper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
