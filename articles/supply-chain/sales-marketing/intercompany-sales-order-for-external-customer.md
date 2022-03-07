---
title: Oprette og fakturere en intern salgsordre til en ekstern kunde
description: Dette emne beskriver oprettelse og fakturering af en intern salgsordre til ekstern brug
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548165"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Oprette og fakturere en intern salgsordre til en ekstern kunde

[!include [banner](../../includes/banner.md)]

Du kan bruge intern handel til at registrere salget af et produkt fra én juridisk enhed til en anden juridisk enhed inden for den samme organisation.

Når du opretter den oprindelige salgsordre, kan du automatisk oprette en intern indkøbsordre til den interne kreditor. Herved oprettes der automatisk en intern salgsordre i den interne kreditors juridiske enhed.

I følgende illustration vises flow for posteringer, når du opretter en salgsordre til en ekstern debitor, men produktet skal bestilles fra en anden juridisk enhed i organisationen, før du kan levere det til debitor. I så fald oprettes der en intern indkøbsordre for den kreditorkonto, der repræsenterer den anden juridiske enhed. En intern salgsordre oprettes igen i den anden juridiske enhed for den debitorkonto, der repræsenterer din juridiske enhed. Når interne indkøbsordrer faktureres, posteres fakturaen for den oprindelige salgsordre automatisk, hvis der er tale om en direkte levering.

![Intern til ekstern salgsproces](media/intercompanyexternalsalesprocess.png)

Hvis du bruger direkte levering, og du vælger **Følgeseddel** i feltet **Mængde** på siden **Bogføring af faktura**, er den interne kreditorfaktura baseret på den interne produktkvittering, der tidligere er bogført.

## <a name="prerequisites"></a>Forudsætninger

Før du begynder, skal du sørge for, at følgende forudsætninger er opfyldt for at bogføre og udskrive interne fakturaer automatisk.

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Marker afkrydsningsfeltet **Bogfør faktura automatisk** i feltgruppen **Intern indkøbsordre (direkte levering)** på siden **Intern** for kreditoren eller debitoren i området **Indkøbsordrepolitikker**.
1. Marker afkrydsningsfeltet **Bogfør faktura automatisk** i feltgruppen **Oprindelig salgsordre (direkte levering)** under **Politikker for indkøbsordrer**. Markér dette afkrydsningsfelt, hvis du ønsker, at fakturaen til den oprindelige salgsordre skal udskrives automatisk, når du bogfører den interne kreditorfaktura.

> [!NOTE]
> Udskriftsindstillinger for fakturaen bestemmes af opsætningen af modulet, dokumentet eller transaktionen på siden **Opsætning af udskriftsstyring**.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Oprette en oprindelig salgsordre for en ekstern kunde

Udføre disse trin i juridisk enhed A. Denne procedure svarer til afkrydsningsfeltet 1 i illustrationen.

1. Gå til **Debitor \> Salgsordrer \> Alle salgsordrer**.
1. Opret den oprindelige salgsordre fra listen **Alle salgsordrer**. Feltværdierne kopieres fra debitorkontoen til salgsordren.
1. I handlingsruden skal du vælge **Overskriftsvisning** på siden **Salgsordre**.
1. Marker afkrydsningsfeltet **Opret interne ordrer automatisk** i oversigtspanelet **Interne indstillinger**.
1. Hvis den interne kreditor skal levere varen direkte til den eksterne kunde, skal du markere afkrydsningsfeltet **Direkte levering**.
1. Når ordren er færdig, skal du lukke siden **Salgsordre**.

Den interne indkøbsordre oprettes automatisk for alle de varer, der er tildelt en intern kreditor, og derefter oprettes den interne salgsordre. Der vises en meddelelse med oplysninger om, at der er oprettet en intern indkøbsordre og en intern salgsordre. Meddelelsen indeholder også links til disse ordrer. Hvis en vare ikke blev fundet, vises der en rød advarsel, hvilket betyder, at ordreoprettelsesprocessen ikke blev fuldført.

> [!NOTE]
> Hvis du opretter flere ordrer i forskellige juridiske enheder, og varerne ikke kunne findes i én af de juridiske enheder, stopper processen til ordreoprettelser, også for de juridiske enheder, der kunne opfylde ordrerne.

## <a name="invoice-an-intercompany-sales-order"></a>Fakturere en intern salgsordre

Når en intern salgsordre faktureres, faktureres den tilsvarende interne indkøbsordre automatisk. Hvis den oprindelige salgsordre er til en direkte leveringsordre, faktureres den oprindelige salgsordre derefter automatisk.

Udføre disse trin i juridisk enhed B. Denne procedure svarer til afkrydsningsfeltet 2 i illustrationen.

1. Gå til **Debitor \> Salgsordrer \> Alle salgsordrer**.
1. Vælg en intern salgsordre i listen på listesiden **Alle salgsordrer**.
1. I handlingsruden skal du vælge fanen **Faktura** og derefter vælge **Faktura**.
1. Marker afkrydsningsfeltet **Postering**.
1. Markér salgsordren, og vælg derefter **OK**.

Debitorfakturaen for den interne salgsordre bogføres automatisk i juridisk enhed B. Den interne kreditorfaktura oprettes derefter automatisk og bogføres i juridisk enhed A. Hvis den oprindelige salgsordre er konfigureret som en direkte levering, oprettes debitorfakturaen for den oprindelige salgsordre i juridisk enhed A.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
