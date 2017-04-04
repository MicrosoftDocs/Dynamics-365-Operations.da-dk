---
title: "Filformater for betalingsmåder"
description: "Dette emne beskriver de to metoder til hentning af filformater, som du kan bruge til en betalingsmåder."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Filformater for betalingsmåder

Dette emne beskriver de to metoder til hentning af filformater, som du kan bruge til en betalingsmåder.

Der er to metoder, du kan bruge til at få filformater til brug med metoder for betaling, elektronisk indberetning (ER)-filformater eller filformater X ++. Når du konfigurerer en betalingsmåde for en debitor eller kreditor, du angiver, hvilke filformater og standarder, der skal bruges til betalinger, og hvordan betalinger vil blive behandlet. Du kan vælge mellem følgende typer af formater:

-   Eksporter
-   Importer
-   Returner
-   Remittering

### <a name="method-1-electronic-reporting-file-formats"></a>Metode 1: Elektronisk indberetning-filformater

Filformater, der er baseret på ER konfigurationer, skal du importere konfigurationerne fra livscyklus Services (LCS). Yderligere oplysninger finder du [hente elektronisk indberetning konfigurationer fra levetidsservices](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Når du importerer rapportering konfigurationer for de filformater, bliver de importerede formater kan vælges på den **betalingsmåder** side. Processen til import og vælge filformater for Europa minder om proceduren for Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Metode 2: X ++-filformater

For at vælge de filformater, der er baseret på X ++-kode, skal du benytte følgende fremgangsmåde.

1.  Gå til den **betalingsmåder** side.
2.  På den **filformater** oversigtspanelet, skal du klikke på **Setup**.
3.  Vælg fanen, der svarer til formatet filtype.
4.  Vælg et filformat fra den **findes** og flytte den til den **valgte** liste med kontrolelementet pil.
5.  Luk den **-filformater for betalingsmåder** side.
6.  På den **-filformater** skal vælge filformatet, der bruges til betalingsmåden i feltet relevante fil format. De generelle indstillinger for elektronisk indberetning skal indstilles til **ingen** for X ++-filformater.



