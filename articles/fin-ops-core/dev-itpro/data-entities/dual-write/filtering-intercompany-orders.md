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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="ab0de-103">Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer</span><span class="sxs-lookup"><span data-stu-id="ab0de-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab0de-104">Du kan filtrere interne ordrer for at undgå synkronisering af enhederne **Ordrer** og **Ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="ab0de-105">I visse scenarier er de interne ordreoplysninger ikke nødvendige i appen Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ab0de-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="ab0de-106">De enkelte Common Data Service-standardenheder udvides med referencer til feltet **IntercompanyOrder**, og dobbeltskrivningstilknytningerne ændres, så de henviser til de ekstra felter i filtrene.</span><span class="sxs-lookup"><span data-stu-id="ab0de-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="ab0de-107">Resultatet er, at de interne ordrer ikke længere synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="ab0de-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="ab0de-108">Denne proces undgår unødvendige data i appen Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ab0de-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="ab0de-109">Føj en reference til **IntercompanyOrder** til **CDS-salgsordrehoveder**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="ab0de-110">Den udfyldes kun på interne ordrer.</span><span class="sxs-lookup"><span data-stu-id="ab0de-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="ab0de-111">Feltet **IntercompanyOrder** er tilgængeligt i **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, SalesOrderHeader":::
    
2. <span data-ttu-id="ab0de-113">Når **CDS-salgsordrehoveder** udvides, bliver feltet **IntercompanyOrder** tilgængeligt i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ab0de-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="ab0de-114">Anvend et filter med `INTERCOMPANYORDER == ""` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="ab0de-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Salgsordrehoveder, rediger forespørgsel":::

3. <span data-ttu-id="ab0de-116">Føj en reference til **IntercompanyInventTransId** til **CDS-salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="ab0de-117">Den udfyldes kun på interne ordrer.</span><span class="sxs-lookup"><span data-stu-id="ab0de-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="ab0de-118">Feltet **InterCompanyInventTransID** er tilgængeligt i **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, SalesOrderLine":::

4. <span data-ttu-id="ab0de-120">Når **CDS-salgsordrelinjer** udvides, bliver feltet **IntercompanyInventTransId** tilgængeligt i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ab0de-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="ab0de-121">Anvend et filter med `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="ab0de-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Salgsordrelinjer, rediger forespørgsel":::

5. <span data-ttu-id="ab0de-123">Udvid **Salgsfakturahoveder V2** og **Salgsfakturalinjer V2** på samme måde, som du udvidede Common Data Service-enhederne i trin 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="ab0de-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="ab0de-124">Tilføj derefter filterforespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="ab0de-124">Then add the filter queries.</span></span> <span data-ttu-id="ab0de-125">Filterstrengen for **Salgsfakturahoveder V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="ab0de-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="ab0de-126">Filterstrengen for **Salgsfakturalinjer V2** er `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="ab0de-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Tilknyt midlertidig lagring til mål, Salgsfakturahoveder":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Salgsfakturahoveder, rediger forespørgsel":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Salgsfakturalinjer, rediger forespørgsel":::

6. <span data-ttu-id="ab0de-130">Enheden **Tilbud** har ikke en intern relation.</span><span class="sxs-lookup"><span data-stu-id="ab0de-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="ab0de-131">Hvis en person opretter et tilbud for en af dine interne kunder, kan du anbringe alle disse kunder i én debitorgruppe ved hjælp af feltet **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="ab0de-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="ab0de-132">Hovedet og linjerne kan udvides for at tilføje feltet **CustGroup** og derefter filtreres, så denne gruppe ikke medtages.</span><span class="sxs-lookup"><span data-stu-id="ab0de-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Tilknyt midlertidig lagring til mål, Salgstilbudshoved":::

7. <span data-ttu-id="ab0de-134">Når du har udvidet enheden **Tilbud**, skal du anvende et filter med `CUSTGROUP !=  "<company>"` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="ab0de-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Salgstilbudshoved, rediger forespørgsel":::
