---
title: Arkivér udskrevne debitorfakturaer med hash-numre
description: Dette emne forklarer, hvordan du aktiverer arkivering for at gemme udskrevne kundefakturaer med hash-numre.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018972"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arkivér udskrevne debitorfakturaer med hash-numre

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

I nogle lande er der et juridisk krav om at gemme beregnede hash-numre i systemet sammen med udskrifter af visse dokumenter. Hash-numre kan bruges til rapportering til myndigheder og under revisioner.

Dette emne forklarer, hvordan du konfigurere arkivering for at gemme udskrevne kundefakturaer med hash-numre.

## <a name="prerequisites"></a>Forudsætninger

- I arbejdsområdet **Funktionsstyring** aktiveres funktionen **Arkivér udskrevne kundefakturaer med hash-numre**. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurer de formater, de kan udskrives af de ønskede dokumenter i **Udskriftsstyring**.

Denne funktionalitet kan anvendes på følgende dokumenter.

**Debitor**
- Debitorfaktura
- Kreditnota til kunden
- Fritekstfaktura
- Fritekstkreditnota

**Projektstyring og regnskab**
- Projektfaktura
- Projektkreditnota

## <a name="configure-customer-master-data"></a>Konfigurer kundemasterdata
Gennemfør følgende trin for at konfigurere kundedata, og aktivfør muligheden for automatisk at gemme udskrevne fakturaer som vedhæftede filer.

1. Gå til **Debitor** > **Alle debitorer**. 
2. Vælg en debitor, og i oversigtsfeltet **Faktura og levering** i sektionen **E-FAKTURA** i feltet **Vedhæftet til e-faktura** vælges **Ja**.

## <a name="print-invoices"></a>Udskriv fakturaer
Du kan bogføre og udskrive en hvilken som helst fritekst-, debitor- og projektfaktura eller -kreditnota for kunden, som er konfigureret i den forrige procedure.

Åbn siden **Vedhæftede filer** for den udskrevne faktura. I oversigtsfeltet **Vedhæftede filer** i feltgruppen **Yderligere detaljer** i feltet **Hash-nummer til dokument** skal du finde det gemte hash-nummer, der er beregnet til den udskrevne faktura.

![Hash-nummer på vedhæftet fil](media/attach-hash-num.jpg)

