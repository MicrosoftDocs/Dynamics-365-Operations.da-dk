---
title: Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer
description: Dette emne forklarer, hvordan du filtrerer interne ordrer, så ordrerne og ordrelinjerne ikke synkroniseres.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568096"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="a68ae-103">Filtrere interne ordrer for at undgå synkronisering af ordrer og ordrelinjer</span><span class="sxs-lookup"><span data-stu-id="a68ae-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a68ae-104">Du kan filtrere interne ordrer for at undgå synkronisering af tabellerne **Ordrer** og **Ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="a68ae-105">I visse scenarier er de interne ordreoplysninger ikke påkrævet i appen Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="a68ae-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="a68ae-106">De enkelte Dataverse-standardtabeller udvides med referencer til kolonnen **IntercompanyOrder**, og dobbeltskrivningstilknytningerne ændres, så de henviser til de ekstra kolonner i filtrene.</span><span class="sxs-lookup"><span data-stu-id="a68ae-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="a68ae-107">Derfor synkroniseres de interne ordrer ikke længere.</span><span class="sxs-lookup"><span data-stu-id="a68ae-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="a68ae-108">Denne proces er med til at undgå unødvendige data i kundeengagementsappen.</span><span class="sxs-lookup"><span data-stu-id="a68ae-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="a68ae-109">Udvid tabellen **CDS-salgsordrehoveder** ved at tilføje en reference til kolonnen **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="a68ae-110">Denne kolonne udfyldes kun på interne ordrer.</span><span class="sxs-lookup"><span data-stu-id="a68ae-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="a68ae-111">Kolonnen **IntercompanyOrder** er tilgængelig i tabellen **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgsordrehoveder":::

2. <span data-ttu-id="a68ae-113">Når **CDS-salgsordrehoveder** udvides, bliver kolonnen **IntercompanyOrder** tilgængelig i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="a68ae-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="a68ae-114">Anvend et filter med `INTERCOMPANYORDER == ""` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="a68ae-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgsordrehoveder":::

3. <span data-ttu-id="a68ae-116">Udvid tabellen **CDS-salgsordrelinjer** ved at tilføje en reference til kolonnen **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="a68ae-117">Denne kolonne udfyldes kun på interne ordrer.</span><span class="sxs-lookup"><span data-stu-id="a68ae-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="a68ae-118">Kolonnen **InterCompanyInventTransId** er tilgængelig i tabellen **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgsordrelinjer":::

4. <span data-ttu-id="a68ae-120">Når **CDS-salgsordrelinjer** udvides, bliver kolonnen **IntercompanyInventTransId** tilgængelig i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="a68ae-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="a68ae-121">Anvend et filter med `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="a68ae-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgsordrelinjer":::

5. <span data-ttu-id="a68ae-123">Gentag trin 1 og 2 for at udvide tabellen **Salgsfakturahoved V2**, og tilføj en filterforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="a68ae-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="a68ae-124">I dette tilfælde skal du bruge `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` som forespørgselsstreng til filteret.</span><span class="sxs-lookup"><span data-stu-id="a68ae-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Knytte midlertidig lagring til målside for Salgsfakturahoved V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogboksen Rediger forespørgsler for Salgsfakturahoved V2":::

6. <span data-ttu-id="a68ae-127">Gentag trin 3 og 4 for at udvide tabellen **Salgsfakturalinjer V2**, og tilføj en filterforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="a68ae-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="a68ae-128">I dette tilfælde skal du bruge `INTERCOMPANYINVENTTRANSID == ""` som forespørgselsstreng til filteret.</span><span class="sxs-lookup"><span data-stu-id="a68ae-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogboksen Rediger forespørgsler for Salgsfakturalinjer V2":::

7. <span data-ttu-id="a68ae-130">Tabellen **Tilbud** har ikke en intern relation.</span><span class="sxs-lookup"><span data-stu-id="a68ae-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="a68ae-131">Hvis en person opretter et tilbud for en af dine interne kunder, kan du anbringe alle disse kunder i én kundegruppe ved hjælp af kolonner **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="a68ae-132">Du kan udvide hovedet og linjerne ved at tilføje kolonnen **CustGroup** og derefter filtrere, så gruppen ikke bliver medtaget.</span><span class="sxs-lookup"><span data-stu-id="a68ae-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Knytte midlertidig lagring til målside for CDS-salgstilbudshoved":::

8. <span data-ttu-id="a68ae-134">Når du har udvidet **Tilbud**, skal du anvende et filter med `CUSTGROUP != "<company>"` som forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="a68ae-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogboksen Rediger forespørgsler for CDS-salgstilbudshoved":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]