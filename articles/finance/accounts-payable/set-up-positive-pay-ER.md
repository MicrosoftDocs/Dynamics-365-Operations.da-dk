---
title: Konfigurere og generere positive betalingsfiler ved hjælp af elektronisk rapportering
description: I dette emne beskrives, hvordan du konfigurerer positive betalinger med elektronisk rapportering.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544469"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Konfigurere positive betalingsfiler ved hjælp af elektronisk rapportering

Konfigurer en positiv betaling til at generere en elektronisk liste over checks, der er leveret til banken. Når checken derefter skal indløses hos banken, sammenligner banken den med listen over checks. Hvis checken svarer til en check på listen, indløser banken den. Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfigurere elektronisk rapportering

1. Gå til **Arbejdsområder \> Elektronisk rapportering**.
2. På feltet for **Microsoft**-konfigurationsudbyderen skal du vælg **Lagre**.
3. Vælg **Global**, og vælg derefter **Åbn**.
4. Hvis der skal oprettes en forbindelse til lageret, skal du vælge det blå link i dialogboksen.
5. Søg efter og vælg **Positiv betalingsmodel \> Format for positiv betaling** på konfigurationslisten.
6. I oversigtspanelet **Versioner** skal du vælge den seneste version og derefter vælge **Importér**.

## <a name="set-up-a-positive-pay-format"></a>Konfigurere et format for positiv betaling

1. Gå til **Kontant- og bankstyring \> Konfiguration \> Positive betalingsformater**.
2. Vælg **Ny**.
3. Angiv felterne **Betalingsformat** og **Beskrivelse**.
4. Markér afkrydsningsfeltet **Generisk elektronisk eksportformat**.
5. Angiv feltet **Konfiguration af eksportformat** til **Format for positiv betaling**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Tildele et format for positiv betaling til en bankkonto

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn bankkontoen.
3. Angiv feltet **Positivt betalingsformat** til det format, der blev oprettet tidligere, i oversigtspanelet **Generelt**.
4. Angiv feltet **Startdato for positiv betaling** til dags dato.

## <a name="generate-a-positive-pay-file"></a>Generér en fil til positive betalinger

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn en bankkonto, der er konfigureret positiv betaling for.
3. Vælg **Administrer betalinger \> Positiv betaling \> Positiv betalingsfil**.
4. Angiv feltet **Skæringsdato**. Checks, der blev genereret før denne dato, inkluderes.

Den XML-fil, der oprettes, bliver downloadet.
