---
title: Revider fakturaer og nøgledata i kreditorsystem
description: Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139931"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="c0505-103">Revider fakturaer og nøgledata i kreditorsystem</span><span class="sxs-lookup"><span data-stu-id="c0505-103">Audit invoices and key data in AP system</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0505-104">Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling.</span><span class="sxs-lookup"><span data-stu-id="c0505-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="c0505-105">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="c0505-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="c0505-106">På siden Kreditorparametre skal du sørge for, at indstillingen Aktivér validering af fakturasammenholdelse er valgt, at feltet Aktivér validering af fakturasammenholdelse er angivet til Kræv godkendelse, og at feltet Sammenholdelsespolitik for linjer er angivet til Trevejs-sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="c0505-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="c0505-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c0505-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="c0505-108">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="c0505-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="c0505-109">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="c0505-109">Create a purchase order</span></span>
1. <span data-ttu-id="c0505-110">Gå til **Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="c0505-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="c0505-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c0505-111">Click **New**.</span></span>
3. <span data-ttu-id="c0505-112">Skriv en værdi i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="c0505-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="c0505-113">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0505-113">Click **OK**.</span></span>
5. <span data-ttu-id="c0505-114">Klik på **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="c0505-114">Click **Add line**.</span></span>
6. <span data-ttu-id="c0505-115">Indtast en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="c0505-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="c0505-116">Klik på **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c0505-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="c0505-117">Klik på **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="c0505-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="c0505-118">Bogfør en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="c0505-118">Post a product receipt</span></span>
1. <span data-ttu-id="c0505-119">Klik på **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c0505-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="c0505-120">Klik på **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="c0505-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="c0505-121">Skriv en værdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="c0505-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="c0505-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0505-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="c0505-123">Registrere og sammenholde en kreditorfaktura med en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="c0505-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="c0505-124">Klik på **Faktura > Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c0505-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="c0505-125">Skriv en værdi i feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="c0505-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="c0505-126">Klik på **Modtag fra: Bestilt antal** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="c0505-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="c0505-127">Vælg en indstilling i feltet **Standardmængde for linjer**.</span><span class="sxs-lookup"><span data-stu-id="c0505-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="c0505-128">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0505-128">Click **OK**.</span></span>
6. <span data-ttu-id="c0505-129">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c0505-129">Click **Yes**.</span></span>
7. <span data-ttu-id="c0505-130">Klik på **Sammenhold produktkvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="c0505-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="c0505-131">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0505-131">Click **OK**.</span></span>
9. <span data-ttu-id="c0505-132">Klik på **Gennemse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c0505-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="c0505-133">Klik på **Detaljer om sammenholdelse**.</span><span class="sxs-lookup"><span data-stu-id="c0505-133">Click **Matching details**.</span></span>

