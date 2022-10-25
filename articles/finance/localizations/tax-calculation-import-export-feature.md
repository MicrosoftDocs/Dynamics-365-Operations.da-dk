---
title: Importere og eksportere momsberegninger
description: Denne artikel indeholder oplysninger om import- og eksportfunktionen i tjenesten til momsberegning.
author: Kai-Cloud
ms.date: 10/17/2022
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
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690227"
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

## <a name="import-feature-demo-data"></a>Importere demodata til funktion

Følg disse trin for at importere demodata til funktioner.

1. Log på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbejdsområdet **Globaliseringsfunktioner** skal du vælge **Funktioner** og derefter markere feltet **Momsberegning**.
3. Vælg **Importér**, og vælg derefter **Synkroniser** på siden **Importér funktion fra den globale lagermappe**. 
4. Vælg funktionen **tax-calculation-feature-demo-data** i tabellen, og vælg derefter **Importér**.
5. Vælg **Vis** for at gennemse de momskoder, grupper og anvendelsesregler, der er defineret i den importerede funktion.
6. I Finance skal du gå til den juridiske enhed **DEMF** og gå til **Moms** \> **Opsætning** \> **Momskonfiguration** \> **Momsberegningsparametre**.
7. Under fanen **Generelt** skal du vælge **Aktivér momsberegningstjeneste**.
8. Vælg **tax-calculation-feature-demo-data** i feltet **Navn på funktionskonfiguration**.
9. Vælg en **Afregningsperiode** og en **Finanskonteringsgruppe** til de nye demomomskoder, og vælg derefter **Bekræft**.
10. Vælg **Gem**.

> [!NOTE]
> Demofunktionen **tax-calculation-feature-demo-data** er baseret på funktionsversionen **40.54.234**, der er udviklet til den juridiske demoenhed **DEMF**. Kontrollér, at Finance og RCS er opgraderet til version 10.0.26 eller senere.
