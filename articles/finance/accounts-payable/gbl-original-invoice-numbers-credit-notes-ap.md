---
title: Reference til oprindelige fakturaer på kreditnotaer (kreditfakturaer)
description: I dette emne beskrives, hvordan du kan oprette en reference til en oprindelig faktura, når du opretter en kreditnota.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562220"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Reference til oprindelige fakturaer på kreditnotaer (kreditfakturaer)

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan oprette en reference til en oprindelig faktura, når du opretter en kreditnota.

## <a name="prerequisites"></a>Forudsætninger

I arbejdsområdet i **Funktionsstyring** skal du aktivere funktionen **Til kreditfakturaer for kreditorfakturaer**. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De funktioner, der er beskrevet i dette emne, gælder for følgende virksomhedsdokumenter.

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
