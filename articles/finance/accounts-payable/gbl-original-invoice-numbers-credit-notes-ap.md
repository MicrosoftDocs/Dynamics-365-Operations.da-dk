---
title: Reference til oprindelige fakturaer på kreditnotaer (kreditfakturaer)
description: Denne artikel beskriver, hvordan du kan oprette en reference til en oprindelig faktura, når du opretter en kreditnota.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e05dddf056d86513d86ea925349f60ca25f191ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901483"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Reference til oprindelige fakturaer på kreditnotaer (kreditfakturaer)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan oprette en reference til en oprindelig faktura, når du opretter en kreditnota.

## <a name="prerequisites"></a>Forudsætninger

I arbejdsområdet i **Funktionsstyring** skal du aktivere funktionen **Til kreditfakturaer for kreditorfakturaer**. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De funktioner, der er beskrevet i denne artikel, gælder for følgende virksomhedsdokumenter.

**Kreditorer:**

- Indkøbsordre
- Fakturajournal
- Indgangsbog

**Finans:**

- Finanskladde

## <a name="define-a-reference-to-an-original-invoice"></a>Definere referencer til oprindelige fakturaer

Benyt følgende procedurer til at definere referencer til oprindelige fakturaer på basis af dokumenttypen.

### <a name="vendor-credit-note-purchase-order"></a>Kreditorkreditnota (indkøbsordre)

1. Gå til **Kreditor** \> **Indkøbsordrer** \> **Alle indkøbsordrer**.
2. Opret en ny indkøbsordre, eller brug en eksisterende til at oprette en kreditnota.
3. Vælg **Kreditfaktura** i gruppen **Introducer** under fanen **Faktura** i handlingsruden.
4. Angiv referencen til den oprindelige faktura, og vælg årsagen til rettelsen.

### <a name="vendor-credit-note-ledger-journals"></a>Kreditorkreditnota (finanskladder)

1. Udfør ét af følgende trin:

    - Gå til **Kreditor** \> **Fakturajournaler**.
    - Gå til **Kreditor** \> **Fakturaregister**.
    - Gå til **Finans** \> **Kladdeposteringer** \> **Finanskladder**.

2. Opret en ny kladde og nye kladdelinjer.
3. Vælg **Funktioner** \> **Kreditnota** i handlingsruden.
4. Angiv referencen til den oprindelige faktura, og vælg årsagen til rettelsen.

> [!NOTE]
> Kommandoen **Fakturakreditering** kan ses i et finanskladdebilag, hvis feltet **Kontotype** er angivet til **Kreditor**.
