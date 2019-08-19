---
title: Registrere kreditorfaktura og sammenligne med modtaget antal
description: Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling.
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834385"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="f56a4-103">Registrere kreditorfaktura og sammenligne med modtaget antal</span><span class="sxs-lookup"><span data-stu-id="f56a4-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f56a4-104">Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling.</span><span class="sxs-lookup"><span data-stu-id="f56a4-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f56a4-105">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="f56a4-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f56a4-106">På siden Kreditorparametre skal du sørge for, at indstillingen Aktivér validering af fakturasammenholdelse er valgt, at feltet Aktivér validering af fakturasammenholdelse er angivet til Kræv godkendelse, og at feltet Sammenholdelsespolitik for linjer er angivet til Trevejs-sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="f56a4-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f56a4-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f56a4-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f56a4-108">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="f56a4-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f56a4-109">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="f56a4-109">Create a purchase order</span></span>
1. <span data-ttu-id="f56a4-110">Gå til Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="f56a4-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f56a4-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f56a4-111">Click New.</span></span>
3. <span data-ttu-id="f56a4-112">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f56a4-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f56a4-113">Skriv en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="f56a4-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="f56a4-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f56a4-114">Click OK.</span></span>
6. <span data-ttu-id="f56a4-115">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="f56a4-115">Click Add line.</span></span>
7. <span data-ttu-id="f56a4-116">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="f56a4-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="f56a4-117">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f56a4-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="f56a4-118">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="f56a4-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f56a4-119">Bogfør en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="f56a4-119">Post a product receipt</span></span>
1. <span data-ttu-id="f56a4-120">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f56a4-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f56a4-121">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f56a4-121">Click Product receipt.</span></span>
3. <span data-ttu-id="f56a4-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f56a4-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f56a4-123">Skriv en værdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f56a4-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="f56a4-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f56a4-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f56a4-125">Registrere og sammenholde en kreditorfaktura med en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="f56a4-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f56a4-126">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f56a4-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f56a4-127">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="f56a4-127">Click Invoice.</span></span>
3. <span data-ttu-id="f56a4-128">Skriv en værdi i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="f56a4-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="f56a4-129">Klik på Modtag fra: Bestilt antal for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="f56a4-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="f56a4-130">Vælg en indstilling i feltet Standardmængde for linjer.</span><span class="sxs-lookup"><span data-stu-id="f56a4-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="f56a4-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f56a4-131">Click OK.</span></span>
7. <span data-ttu-id="f56a4-132">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="f56a4-132">Click Yes.</span></span>
8. <span data-ttu-id="f56a4-133">Klik på Sammenhold produktkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="f56a4-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="f56a4-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f56a4-134">Click OK.</span></span>
10. <span data-ttu-id="f56a4-135">Klik på Gennemse i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f56a4-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="f56a4-136">Klik på Detaljer om sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="f56a4-136">Click Matching details.</span></span>

