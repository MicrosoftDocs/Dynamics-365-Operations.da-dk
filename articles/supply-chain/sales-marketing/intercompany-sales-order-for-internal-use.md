---
title: Oprette en intern salgsordre til intern brug
description: Dette emne beskriver oprettelse og fakturering af en intern salgsordre til intern brug
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
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548167"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Oprette en intern salgsordre til intern brug

[!include [banner](../../includes/banner.md)]

Som regel oprettes en intern salgsordre automatisk på baggrund af en intern indkøbsordre. Du kan også oprette en intern salgsordre manuelt, som derefter genererer en intern indkøbsordre i den interne kundes juridiske enhed.

![Intern salgsproces](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Opret en intern salgsordre manuelt

Udfør disse trin i den juridiske enhed B som vist i illustrationen.

1. Gå til **Debitor \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Salgsordre** i handlingsruden for at oprette en salgsordre.
1. Vælg en debitorkonto på siden **Opret salgsordre**. Kontrollér, at afkrydsningsfeltet **Intern** i oversigtspanelet **Generelt** er markeret. Dette angiver, at den valgte kunde er en intern kunde.
1. Angiv eller rediger oplysningerne, vælg **OK**, og udfyld derefter ordrelinjerne, som du plejer.

    Værdien i feltet **Leveringsadresse** kopieres fra det interne salgsordrehoved til det interne indkøbsordrehoved. Værdien i feltet **varenummer**, herunder produktdimensioner, og værdien i felterne **Leveringsdato** og **valutakode** kopieres fra de interne salgsordrelinjer til de interne indkøbsordrelinjer.

1. Vælg **Intern** i ordrehovedet for at få vist den relaterede interne indkøbsordre.
1. Vælg **Intern** på ordrelinjerne for at få vist oplysninger om den disponible lagerbeholdning for samhandel internt i firmaet.

> [!TIP]
> Du kan få vist interne salgsordrer på siden **Interne ordrer**.

> [!NOTE]
> Når du arbejder med intern handel, anbefales det, at du fjerner markeringen i afkrydsningsfeltet **Slet ordre efter fakturering** på siden **Debitorparametre**. Ellers slettes den relaterede indkøbsordre. Det anbefales også, at du fjerner markeringen i afkrydsningsfeltet **Slet købsordre efter fakturering** på siden **Kreditorparametre**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
