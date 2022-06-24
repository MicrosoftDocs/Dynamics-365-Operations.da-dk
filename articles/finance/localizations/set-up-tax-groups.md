---
title: Konfigurere momsgrupper
description: Denne artikel beskriver, hvordan du konfigurerer momsgrupper i momsberegningstjenesten.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862893"
---
# <a name="set-up-tax-groups"></a>Konfigurere momsgrupper

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer momsgrupper i momsberegningstjenesten. Det forklarer også, hvordan du konfigurerer matrixen for regler for anvendelse af momsgrupper og konfigurerer linjer i matrixen.

Begrebet momsgrupper i tjenesten Momsberegning minder om begrebet momsgrupper i Microsoft Dynamics 365 Finance. Det er grupper af momskoder. Tjenesten Momsberegning bruger skæringspunktet for en momsgruppe og en varemomsgruppe til at fastlægge momskoderne.

Momsgrupperne i tjenesten Momsberegning er dog anderledes end momsgrupperne i Finans, fordi der ikke er yderligere parametre til dem, for eksempel **Importmoms** og **Momsfritagelse**. Disse parametre er i stedet tilgængelige på momskodeniveau.

> [!IMPORTANT]
> Opsætningen af momsgrupper i tjenesten Momsberegning er afhængig af en juridisk enhed. Du kan kun fuldføre denne opsætning i Regulatory Configuration Service (RCS) én gang. Når du aktiverer tjenesten Momsberegning i Finans, synkroniseres momsgrupper automatisk for den valgte juridiske enhed.

## <a name="set-up-a-tax-group"></a>Konfigurere en momsgruppe

Følg disse trin for at konfigurere en momsgruppe.

1. Log på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbejdsområder** \> **Globaliseringsfunktioner** \> **Momsberegning**.
3. Vælg den funktion og version, du vil konfigurere, og vælg derefter **Rediger**.
4. Vælg **Konfigurationsversion** under fanen **Generelt**.
5. Vælg **Administrer kolonne** under fanen **Momsgruppe**. Hvis du konfigurerer en momsgruppe første gang, angives felterne i dialogboksen **Administrer kolonne** automatisk.
6. På listen til venstre skal du udvide noden **Linjer** og markere afkrydsningsfeltet for **Momsgruppe**.

    ![Momsgruppe, der er valgt under noden Linjer i dialogboksen Administrer kolonner.](media/select-tax-group.png)

7. Vælg knappen med højre pil for at føje **Momsgruppe** til listen **Valgte kolonner** til højre.

    ![Momsgruppe, der er føjet til listen Valgte kolonner.](media/add-tax-group.png)

8. Vælg **OK**.

## <a name="configure-a-tax-group"></a>Konfigurere en momsgruppe

Når du har konfigureret en momsgruppe, oprettes matrixen for reglen for anvendelse af momsgruppen. Du kan føje linjer til matrixen for at konfigurere momsgruppen.

1. Vælg **Tilføj** under fanen **Momsgruppe**.
2. Skriv navnet på momsgruppen i feltet **Momsgruppe**.

    > [!IMPORTANT]
    > Det anbefales, at du begrænser navnet på momsgruppen til 10 tegn. Dette navn synkroniseres med Finans, hvilket har en grænse på 10 tegn for navne på momsgrupperne.

3. Markér afkrydsningsfeltet for hver momskode, du vil medtage i momsgruppen, i feltet **Momskoder**. Du kan medtage flere momskoder i én momsgruppe.

    ![Flere momskoder, der er valgt i feltet Momskoder.](media/multiple-tax-codes-selection.png)

4. Gentag trin 1-3 for at tilføje flere momsgrupper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
