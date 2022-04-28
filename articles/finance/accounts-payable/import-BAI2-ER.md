---
title: Konfigurere avanceret import af bankafstemning ved hjælp af elektronisk rapportering
description: Dette emne forklarer, hvordan du bruger elektronisk rapportering til at konfigurere importprocessen til avanceret bankafstemning af BAI2-opgørelser.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544477"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Konfigurere avanceret import af bankafstemning ved hjælp af elektronisk rapportering

[!include [banner](../includes/banner.md)]

Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 Finance. Dette emne beskriver, hvordan du konfigurerer importfunktionen for dine BAI2-bankkontoudtog.

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfigurere elektronisk rapportering

1. Gå til **Arbejdsområder \> Elektronisk rapportering**.
2. På feltet for **Microsoft**-konfigurationsudbyderen skal du vælg **Lagre**.
3. Vælg **Global**, og vælg derefter **Åbn**.
4. Hvis der skal oprettes en forbindelse til lageret, skal du vælge det blå link i dialogboksen.
5. Find **Bankkontoudtogsmodel \> Bankkontoudtogsmodel for BAI2** på konfigurationslisten.
6. Vælg formatet **BAI2**.
7. I oversigtspanelet **Versioner** skal du vælge den seneste version og derefter vælge **Importér**.

## <a name="set-up-the-bank-statement-format"></a>Konfigurere formatet af bankkontoudtog

1. Gå til **Kontant- og bankstyring \> Konfiguration \> Konfiguration af avanceret bankafstemning \> Bankkontoudtogsformat**.
2. Vælg **Ny**.
3. Angiv felterne **Kontoudtogsformat** og **Navn**.
4. Markér afkrydsningsfeltet **Generisk elektronisk importformat**.
5. Angiv feltet **Konfiguration af importformat** til **BAI2**.

## <a name="set-up-the-bank-account"></a>Konfigurere bankkontoen

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn bankkontoen.
3. I oversigtspanelet **Afstemning** skal du vælge indstillingen **Ja** for **Avanceret bankafstemning**.
4. Indstil feltet **Kontoudtogsformat** til det **BAI2**-format, du oprettede tidligere.

## <a name="import-the-bank-statement"></a>Importere bankkontoudtoget

1. Gå til **Kontant- og bankstyring \> Afstemning af bankkontoudtog \> Bankkontoudtog**.
2. Vælg **Importér kontoudtog** øverst på siden **Bankkontoudtog**.
3. Indstil feltet **Bankkonto** til bankkontoen i kontoudtoget.
4. Indstil feltet **Kontoudtogsformat** til det **BAI2**-format, du oprettede tidligere.
5. Vælg **Gennemse**, og vælg **BAI**-filen.
6. Vælg **Overfør**.
7. Vælg **OK** for at importere den valgte fil.
