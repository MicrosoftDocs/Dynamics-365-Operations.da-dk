---
title: Definere parametre for bogføring af en intern ordre
description: Dette emne forklarer, hvordan du konfigurerer parametre til bogføring af en intern ordre.
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
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548169"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Definere parametre for bogføring af en intern ordre

[!include [banner](../../includes/banner.md)]

Når en intern debitorfaktura bogføres, kan du vælge indstillinger, så den interne indkøbsordre og den oprindelige debitorfaktura begge bogføres automatisk.

> [!NOTE]
> Før du udfører denne procedure, skal du konfigurere udskriftsstyringen i organisationen, så der peges på den rigtige fakturaprinter. På den måde sikres det, at fakturaen for den oprindelige salgsordre udskrives på den rigtige printer.

Du skal angive følgende parametre:

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**. Vælg den salgsordre, som du vil arbejde med.
1. I salgsordren skal du i Handlingsrude vælge **Overskrift** og derefter vælge oversigtspanelet **Interne indstillinger** og åbne det.
1. Gå til handlingsruden på fanen **Salgsordre**, og vælg **Rediger**.
1. Gå tilbage til oversigtspanelet **Interne indstillinger**, og vælg **Direkte levering** for at aktivere direkte levering overalt i den interne kæde (alle ordrer).
1. Vælg **Gem** for at gemme salgsordren sammen med den nye indstilling. Vælg derefter på **Luk** for at lukke salgsordren.
1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**. Under fanen **Generelt** skal du vælge en **Intern**.
1. Vælg linket **Indkøbsordrepolitikker** på siden **Intern**. Vælg **Bogfør faktura automatisk** i feltgruppen **Intern indkøbsordre (direkte levering)**, og fjern markeringen i afkrydsningsfeltet **Udskriv faktura automatisk**.
1. Vælg **Bogfør faktura automatisk** i feltgruppen **Oprindelig salgsordre (direkte levering)**, og fjern markeringen i afkrydsningsfeltet **Udskriv faktura automatisk**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
