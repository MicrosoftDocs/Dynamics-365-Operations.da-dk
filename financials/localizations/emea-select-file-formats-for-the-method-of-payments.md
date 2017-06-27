---
title: "Filformater for betalingsmåder"
description: "Dette emne beskriver de to metoder til hentning af filformater, som du kan bruge til betalingsmåder."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b3cf1d469998389895c137fa842b73adb0eeddc
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Filformater for betalingsmåder

[!include[banner](../includes/banner.md)]


Dette emne beskriver de to metoder til hentning af filformater, som du kan bruge til betalingsmåder.

Der er to metoder, som du kan bruge til at få filformater, der kan bruges til betalingsmetoder, filformater til elektronisk indberetning (ER) eller X++-filformater. Når du konfigurerer en betalingsmåde for en debitor eller kreditor, angiver du, hvilke filformater og standarder, der skal bruges til betalinger, og hvordan betalinger bliver behandlet. Du kan vælge mellem følgende typer af formater:

-   Eksporter
-   Importer
-   Returner
-   Remittering

### <a name="method-1-electronic-reporting-file-formats"></a>Metode 1: Filformater til elektronisk rapportering

Ved filformater, der er baseret på ER-konfigurationer, skal du importere konfigurationerne fra Lifecycle Services (LCS). Du kan finde flere oplysninger i [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Når du har importeret rapporteringskonfigurationer for de pågældende filformater, kan de importerede formater vælges på siden **Betalingsmåder**. Processen til import og valg af filformater for Europa minder om proceduren for Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Metode 2: X++-filformater

For at vælge filformater, der er baseret på X++-kode, skal du benytte følgende fremgangsmåde.

1.  Gå til siden **Betalingsmåder**.
2.  I **Filformater** oversigtspanelet skal du klikke på **Opsætning**.
3.  Vælg den fane, der svarer til filformattypen.
4.  Vælg et filformat på listen **Tilgængelige**, og flyt det til listen **Valgte** med pilkontrolelementet.
5.  Luk siden **Filformater for betalingsmåder**.
6.  Vælg det filformat i oversigtspanelet **Filformater**, der skal bruges til betalingsmåden fra det relevante filformatfelt. De generelle indstillinger for elektronisk rapportering skal indstilles til **Ingen** for X++-filformater.





