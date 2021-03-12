---
title: Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer
description: Dette emne forklarer, hvordan du filtrerer interne ordrer, så ordrerne og ordrelinjerne ikke synkroniseres.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 342db8c1b4337145bfd61f5698ff6de25434a400
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796600"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer

[!include [banner](../../includes/banner.md)]

Du kan filtrere interne ordrer for at undgå synkronisering af tabellerne **Ordrer** og **Ordrelinjer**. I visse scenarier er de interne ordreoplysninger ikke påkrævet i appen Customer Engagement.

De enkelte Dataverse-standardtabeller udvides med referencer til kolonnen **IntercompanyOrder**, og dobbeltskrivningstilknytningerne ændres, så de henviser til de ekstra kolonner i filtrene. Derfor synkroniseres de interne ordrer ikke længere. Denne proces er med til at undgå unødvendige data i kundeengagementsappen.

1. Udvid tabellen **CDS-salgsordrehoveder** ved at tilføje en reference til kolonnen **IntercompanyOrder**. Denne kolonne udfyldes kun på interne ordrer. Kolonnen **IntercompanyOrder** er tilgængelig i tabellen **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgsordrehoveder":::

2. Når **CDS-salgsordrehoveder** udvides, bliver kolonnen **IntercompanyOrder** tilgængelig i tilknytningen. Anvend et filter med `INTERCOMPANYORDER == ""` som forespørgselsstreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgsordrehoveder":::

3. Udvid tabellen **CDS-salgsordrelinjer** ved at tilføje en reference til kolonnen **IntercompanyInventTransId**. Denne kolonne udfyldes kun på interne ordrer. Kolonnen **InterCompanyInventTransId** er tilgængelig i tabellen **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgsordrelinjer":::

4. Når **CDS-salgsordrelinjer** udvides, bliver kolonnen **IntercompanyInventTransId** tilgængelig i tilknytningen. Anvend et filter med `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgsordrelinjer":::

5. Gentag trin 1 og 2 for at udvide tabellen **Salgsfakturahoved V2**, og tilføj en filterforespørgsel. I dette tilfælde skal du bruge `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` som forespørgselsstreng til filteret.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Knytte midlertidig lagring til målside for Salgsfakturahoved V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogboksen Rediger forespørgsler for Salgsfakturahoved V2":::

6. Gentag trin 3 og 4 for at udvide tabellen **Salgsfakturalinjer V2**, og tilføj en filterforespørgsel. I dette tilfælde skal du bruge `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng til filteret.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogboksen Rediger forespørgsler for Salgsfakturalinjer V2":::

7. Tabellen **Tilbud** har ikke en intern relation. Hvis en person opretter et tilbud for en af dine interne kunder, kan du anbringe alle disse kunder i én kundegruppe ved hjælp af kolonner **CustGroup**. Du kan udvide hovedet og linjerne ved at tilføje kolonnen **CustGroup** og derefter filtrere, så gruppen ikke bliver medtaget.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgstilbudshoved":::

8. Når du har udvidet **Tilbud**, skal du anvende et filter med `CUSTGROUP != "<company>"` som forespørgselsstreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgstilbudshoved":::
