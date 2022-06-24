---
title: Definere parametre for bogføring af en intern ordre
description: Denne artikel forklarer, hvordan du konfigurerer parametre til bogføring af en intern ordre
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 97ea0061d57beede6350eecfd497c12dd37aea31
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900790"
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
