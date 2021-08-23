---
title: Referencer til oprindelige fakturaer på kreditnotaer
description: Dette emne indeholder en forklaring på, hvordan du opretter og udskriver de oprindelige fakturanumre i relaterede kreditnotaer.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6a5ac50c996f92f5cfa569ad00fa4b911827fd4ec8bddb2442bbd6ac67d1f33f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723841"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Referencer til oprindelige fakturaer på kreditnotaer

[!include [banner](../includes/banner.md)]


I nogle lande og områder er der et juridisk krav om, at udskrevne kreditnotaer skal indeholde referencer til de oprindelige fakturaer. Dette emne indeholder en forklaring på, hvordan du opretter og udskriver de oprindelige fakturanumre i relaterede kreditnotaer.

## <a name="prerequisites"></a>Forudsætninger

- Brug arbejdsområdet **Funktionsstyring** til at aktivere funktionen **Layout til fakturakreditering i salgs- og projektfakturarapporter**. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- De formater til krævede dokumenter, der kan udskrives, skal konfigureres i Udskriftsstyring.

De funktioner, der er beskrevet i dette emne, gælder for følgende dokumenter:

**Debitor**

- Fritekstkreditnota
- Kreditnota til kunden

**Projektstyring og regnskab**

- Projektkreditnota

## <a name="configure-accounts-receivable-parameters"></a>Konfigurere debitorparametre

Benyt følgende fremgangsmåde for at angive den parameter, der styrer, om referencer til de oprindelige fakturaer udskrives på relaterede kreditnotaer.

1. Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**.
2. Under fanen **Opdateringer** i oversigtspanelet **Faktura** skal du angive indstillingen **Anvend layoutet for fakturakreditering i rapporter for salgs- og projektfakturaer** til **Ja**.

![Konfigurere debitorparametre.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Definere referencer til oprindelige fakturaer

Benyt følgende procedurer til at definere referencer til oprindelige fakturaer på basis af dokumenttypen.

### <a name="free-text-credit-note"></a>Fritekstkreditnota

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Opret en ny kreditnota, eller vælg en eksisterende kreditnota.
3. Åbn fakturaen.
4. Vælg **Kreditfaktura** i gruppen **Funktioner** under fanen **Faktura** i handlingsruden.
5. Angiv referencen til den oprindelige faktura, og vælg årsagen til rettelsen.

![Definere referencen til en fritekstfaktura.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kreditnota til kunden

1. Gå til **Debitor** \> **Ordrer** \> **Alle salgsordrer**.
2. Vælg og åbn den fakturerede salgsordre, der skal rettes.
3. Klik på **Kreditnota** i gruppen **Kreditnota** under fanen **Sælg** i handlingsruden.
4. Angiv årsagen til rettelsen. Referencen til den oprindelige faktura oprettes automatisk.

![Definere referencen til en salgsordre.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projektkreditnota

1. Gå til **Projektstyring og regnskab** \> **Projektfakturaer** \> **Projektfakturaer**.
2. Vælg og åbn den projektfaktura, der skal rettes.
3. Vælg **Vælg til kreditfaktura** i gruppen **Funktioner** under fanen **Projektfaktura** i handlingsruden.
4. Vælg **Kreditfaktura**.
5. Angiv årsagen til rettelsen. Referencen til den oprindelige faktura oprettes automatisk.

![Definere referencen til en projektfaktura.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Udskrive kreditnotaer

Når du udskriver fritekst-, debitor- og projektkreditnotaer, omfatter de referencen til den oprindelige faktura og årsagen til rettelsen.

![Udskrevet kreditnota.](media/credit-note-FTI.jpg)

> [!NOTE]
> Kontroller, at dokumenternes formater, der kan udskrives, er konfigureret korrekt, efter at det antages, at referencer til oprindelige fakturaer vil blive udskrevet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]