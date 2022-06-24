---
title: Importere og eksportere momsberegninger
description: Denne artikel indeholder oplysninger om import- og eksportfunktionen i tjenesten til momsberegning.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 9daee683763d7cb0eb9573497eb4e20cba9b1863
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855167"
---
# <a name="import-and-export-tax-calculations"></a>Importere og eksportere momsberegninger

Denne artikel indeholder oplysninger om import- og eksportfunktionen i tjenesten til momsberegning. Denne funktionalitet er med til at sikre en fleksibel og effektiv konfigurationsoplevelse.

## <a name="import-and-export-tax-codes"></a>Importere og eksportere momskoder

### <a name="export-templates"></a>Eksportere skabeloner

1. Log på [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/).
2. I arbejdsområdet **Globaliseringsfunktioner** skal du vælge **Funktioner** og derefter markere feltet **Momsberegning**.
3. Vælg en eksisterende funktion, eller [opret en ny funktion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Vælg **Rediger** i gitteret **Versioner**.
5. På siden med funktionen **Momsberegning** skal du angive [konfigurationsversionen](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Vælg **Importér** under fanen **Momskoder**.
7. Vælg **Eksportér en momskodeskabelon** for at hente filen **TaxCodesTemplate.zip**.
8. Pak **TaxCodesTemplate.zip** ud. Momskodeskabelonerne komprimeres separat i henhold til værdien for **beregningsgrundlaget**.
9. Pak **Efter nettobeløb.zip** ud for at få følgende CSV-filer (filer med kommaseparerede værdier):

    - **TaxCode.csv** – Angiv momskoderne.
    - **TaxLimit.csv** – Angiv momsgrænserne for de enkelte momskoder.
    - **TaxRate.csv** – Angiv momssatserne for de enkelte momskoder.

> [!NOTE]
> Posterne for momskoden **Eksempel** er som standard tilgængelige i skabelonerne. Hvis momskoden **Eksempel** ikke fjernes fra CSV-filerne, importeres den til funktionen.

### <a name="import-tax-codes"></a>Importere momskoder

Benyt følgende fremgangsmåde for at importere momskoden **Eksempel** i skabelonen til funktionen til momsberegning.

1. I RCS skal du vælge **Importér** under fanen **Momskoder** på siden med funktionen **Momsberegning**.
2. Vælg **Gennemse**, find og vælg filen **TaxCode.csv**, og vælg derefter **Momskode** i feltet **Måltabel**.
3. Vælg **OK** for at importere momskoden.
4. Find og vælg filen **TaxCode.csv**, og vælg derefter **Momssats** i feltet **Måltabel**.
5. Vælg **OK** for at importere momssatsen.
6. Find og vælg filen **TaxLimit.csv**, og vælg derefter **Momsgrænse** i feltet **Måltabel**.
7. Vælg **OK** for at importere momsgrænsen.

Du kan også importere den zip-fil, der indeholder alle tre CSV-filer, direkte. På den måde kan du hurtigt og nemt fuldføre importen.

1. I RCS skal du vælge **Importér** under fanen **Momskoder** på siden med funktionen **Momsberegning**.
2. Vælg **Gennemse**, find og vælg filen **Efter nettobeløb.zip**, og vælg derefter **OK**.

### <a name="export-tax-codes"></a>Eksportere momskoder

1. I RCS skal du vælge **Eksportér** under fanen **Momskoder** på siden med funktionen **Momsberegning**.

    Knappen **Eksportér** er tilgængelig, når der er mindst én momskode i gitteret **Momskoder**.

2. Vælg **OK** for at eksportere alle momskoder i en zip-fil.

> [!NOTE]
> Brug den eksporterede fil som skabelon til at importere momskoder til den tilsvarende funktion.

## <a name="import-and-export-applicability-rules"></a>Importere og eksportere anvendelighedsregler

### <a name="export-applicability-rules"></a>Eksportere anvendelighedsregler

1. Log på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbejdsområdet **Globaliseringsfunktioner** skal du vælge **Funktioner** og derefter markere feltet **Momsberegning**.
3. Vælg en eksisterende funktion, eller [opret en ny funktion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Vælg **Rediger** i gitteret **Versioner**.
5. På siden med funktionen **Momsberegning** skal du angive [konfigurationsversionen](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Under fanen **Anvendelse af momsgruppe** skal du markere rækkerne i gitteret **Opsætning af anvendelighed af momsgruppe**.
7. Vælg knappen **Åbn i Microsoft Office**, og vælg derefter **Matrix for dynamisk anvendelse af momstjenesten**.

    [![Eksportere anvendelsesregler til Microsoft Excel på siden med funktionen Momsberegning.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Vælg **Hent** for at eksportere de markerede rækker til et Microsoft Excel-regneark.

### <a name="import-applicability-rules"></a>Importere anvendelighedsregler

Det Excel-regneark, du har hentet, indeholder strukturen i gitteret **Opsætning af anvendelighed af momsgruppe**. Du kan tilføje nye regler direkte i regnearket. Når du er færdig, skal du følge nedenstående trin for at importere de nye regler tilbage til gitteret **Opsætning af anvendelighed af momsgruppe**.

1. Markér og kopiér de rækker, der skal importeres, i Excel-regnearket.
2. I RCS skal du vælge **Tilføj** under fanen **Anvendelse af momsgruppe** på siden med funktionen **Momsberegning** for at indsætte en tom post nederst i gitteret **Opsætning af anvendelighed af momsgruppe**.
3. Vælg **Ctrl+V** for at indsætte de kopierede rækker i gitteret.
4. Vælg **Gem**.
