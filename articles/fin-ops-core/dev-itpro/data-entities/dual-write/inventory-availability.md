---
title: Lagertilgængelighed i dobbeltskrivning
description: I dette emne får du oplysninger om, hvordan du kontrollerer lagertilgængelighed i dobbeltskrivning.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997886"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="c62b7-103">Lagertilgængelighed i dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="c62b7-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c62b7-104">Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til siden **Tilbud** , **Ordrer** eller **Fakturaer** i Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="c62b7-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="c62b7-105">Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en nøgleopgave i processen for [kundeemne til kontant](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="c62b7-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="c62b7-106">Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange.</span><span class="sxs-lookup"><span data-stu-id="c62b7-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="c62b7-107">Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="c62b7-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="c62b7-108">Disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c62b7-108">On-hand inventory</span></span>

<span data-ttu-id="c62b7-109">I sidehovedet for formularerne **Tilbud** , **Ordrer** og **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="c62b7-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="c62b7-110">Når du vælger knappen, vises en dialogboks, hvor du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for.</span><span class="sxs-lookup"><span data-stu-id="c62b7-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="c62b7-111">I denne dialogboks vises de samme oplysninger som [disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="c62b7-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="c62b7-112">Dialogboksen returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c62b7-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c62b7-113">Disse oplysninger indeholder følgende antal:</span><span class="sxs-lookup"><span data-stu-id="c62b7-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="c62b7-114">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="c62b7-114">On-hand quantity</span></span>
- <span data-ttu-id="c62b7-115">Reserveret disponibelt antal</span><span class="sxs-lookup"><span data-stu-id="c62b7-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="c62b7-116">Tilgængeligt disponibelt antal</span><span class="sxs-lookup"><span data-stu-id="c62b7-116">Available on-hand quantity</span></span>
- <span data-ttu-id="c62b7-117">Bestilt antal</span><span class="sxs-lookup"><span data-stu-id="c62b7-117">Ordered quantity</span></span>
- <span data-ttu-id="c62b7-118">Antal i bestilling</span><span class="sxs-lookup"><span data-stu-id="c62b7-118">On-order quantity</span></span>
- <span data-ttu-id="c62b7-119">Reserveret bestilt mængde</span><span class="sxs-lookup"><span data-stu-id="c62b7-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="c62b7-120">Disponibelt antal i alt</span><span class="sxs-lookup"><span data-stu-id="c62b7-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="c62b7-121">DTT-oplysninger</span><span class="sxs-lookup"><span data-stu-id="c62b7-121">ATP information</span></span>

<span data-ttu-id="c62b7-122">I Sales er der føjet en ny knap for **DTT-oplysninger** til linjeelementer på siderne **Tilbud** , **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="c62b7-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="c62b7-123">Når du vælger knappen, vises en dialogboks, hvor du kan angive firma, produkt, lagerlokation, lagersted og ordreantal.</span><span class="sxs-lookup"><span data-stu-id="c62b7-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="c62b7-124">Denne dialogboks har de samme indstillinger, som er beskrevet under [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="c62b7-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="c62b7-125">Dialogboksen returnerer DTT-oplysningerne fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c62b7-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="c62b7-126">Disse oplysninger indeholder følgende antal:</span><span class="sxs-lookup"><span data-stu-id="c62b7-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="c62b7-127">DTT-antal</span><span class="sxs-lookup"><span data-stu-id="c62b7-127">ATP quantity</span></span>
- <span data-ttu-id="c62b7-128">Tilgangsantal</span><span class="sxs-lookup"><span data-stu-id="c62b7-128">Receipt quantity</span></span>
- <span data-ttu-id="c62b7-129">Afgangsantal</span><span class="sxs-lookup"><span data-stu-id="c62b7-129">Issue quantity</span></span>
- <span data-ttu-id="c62b7-130">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="c62b7-130">On-hand quantity</span></span>
