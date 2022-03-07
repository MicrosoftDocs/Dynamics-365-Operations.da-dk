---
title: Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer
description: I dette emne beskrives, hvordan du kan filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701027"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer

[!include [banner](../../includes/banner.md)]

Du kan filtrere interne ordrer for at undgå synkronisering af enhederne **Ordrer** og **Ordrelinjer**. I visse scenarier er de interne ordreoplysninger ikke nødvendige i appen Customer Engagement.

De enkelte Common Data Service-standardenheder udvides med referencer til feltet **IntercompanyOrder**, og dobbeltskrivningstilknytningerne ændres, så de henviser til de ekstra felter i filtrene. Resultatet er, at de interne ordrer ikke længere synkroniseres. Denne proces undgår unødvendige data i appen Customer Engagement.

1. Føj en reference til **IntercompanyOrder** til **CDS-salgsordrehoveder**. Den udfyldes kun på interne ordrer. Feltet **IntercompanyOrder** er tilgængeligt i **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, SalesOrderHeader":::
    
2. Når **CDS-salgsordrehoveder** udvides, bliver feltet **IntercompanyOrder** tilgængeligt i tilknytningen. Anvend et filter med `INTERCOMPANYORDER == ""` som forespørgselsstreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Salgsordrehoveder, rediger forespørgsel":::

3. Føj en reference til **IntercompanyInventTransId** til **CDS-salgsordrelinjer**.  Den udfyldes kun på interne ordrer. Feltet **InterCompanyInventTransID** er tilgængeligt i **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, SalesOrderLine":::

4. Når **CDS-salgsordrelinjer** udvides, bliver feltet **IntercompanyInventTransId** tilgængeligt i tilknytningen. Anvend et filter med `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Salgsordrelinjer, rediger forespørgsel":::

5. Udvid **Salgsfakturahoveder V2** og **Salgsfakturalinjer V2** på samme måde, som du udvidede Common Data Service-enhederne i trin 1 og 2. Tilføj derefter filterforespørgslerne. Filterstrengen for **Salgsfakturahoveder V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Filterstrengen for **Salgsfakturalinjer V2** er `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, Salgsfakturahoveder":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Salgsfakturahoveder, rediger forespørgsel":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Salgsfakturalinjer, rediger forespørgsel":::

6. Enheden **Tilbud** har ikke en intern relation. Hvis en person opretter et tilbud for en af dine interne kunder, kan du anbringe alle disse kunder i én debitorgruppe ved hjælp af feltet **CustGroup**.  Hovedet og linjerne kan udvides for at tilføje feltet **CustGroup** og derefter filtreres, så denne gruppe ikke medtages.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Tilknyt midlertidig lagring til mål, Salgstilbudshoved":::

7. Når du har udvidet enheden **Tilbud**, skal du anvende et filter med `CUSTGROUP !=  "<company>"` som forespørgselsstreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Salgstilbudshoved, rediger forespørgsel":::
