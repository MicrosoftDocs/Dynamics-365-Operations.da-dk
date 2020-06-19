---
title: Lagertilgængelighed i dobbeltskrivning
description: I dette emne får du oplysninger om kontrol af lagertilgængelighed i dobbeltskrivning.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426976"
---
# <a name="inventory-availability"></a><span data-ttu-id="65895-103">Lagertilgængelighed</span><span class="sxs-lookup"><span data-stu-id="65895-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="65895-104">Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i modelbaserede apps i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="65895-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="65895-105">Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en hovedopgave i [processen for kundeemne til kontant](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="65895-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="65895-106">Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange.</span><span class="sxs-lookup"><span data-stu-id="65895-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="65895-107">Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="65895-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="65895-108">Disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="65895-108">On-hand Inventory</span></span> 

<span data-ttu-id="65895-109">I sidehovedet for formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="65895-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="65895-110">Når du klikker på knappen, vises en dialogboks, og du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for.</span><span class="sxs-lookup"><span data-stu-id="65895-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="65895-111">Den returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management og viser de samme oplysninger som [Disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="65895-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="65895-112">Oplysningerne omfatter disse antal:</span><span class="sxs-lookup"><span data-stu-id="65895-112">The information includes these quantities:</span></span>

- <span data-ttu-id="65895-113">**Disponibelt antal**</span><span class="sxs-lookup"><span data-stu-id="65895-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="65895-114">**Reserveret disponibelt antal**</span><span class="sxs-lookup"><span data-stu-id="65895-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="65895-115">**Tilgængeligt disponibelt antal**</span><span class="sxs-lookup"><span data-stu-id="65895-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="65895-116">**Bestilt antal**</span><span class="sxs-lookup"><span data-stu-id="65895-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="65895-117">**Antal i bestilling**</span><span class="sxs-lookup"><span data-stu-id="65895-117">**On-order Quantity**</span></span>
- <span data-ttu-id="65895-118">**Reserveret bestilt antal**</span><span class="sxs-lookup"><span data-stu-id="65895-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="65895-119">**Disponibelt antal i alt**</span><span class="sxs-lookup"><span data-stu-id="65895-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="65895-120">DTT-oplysninger</span><span class="sxs-lookup"><span data-stu-id="65895-120">ATP information</span></span>

<span data-ttu-id="65895-121">Til linjeelementerne på formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i Dynamics 365 Sales er der føjet en ny knap **DTT-oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="65895-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="65895-122">Når du klikker på knappen, vises en dialogboks, og du kan angive firma, produkt, lagersted, lagervarehus og ordreantal.</span><span class="sxs-lookup"><span data-stu-id="65895-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="65895-123">Den returnerer **DTT-oplysningerne** fra Supply Chain Management og viser indstillingerne beskrevet i [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="65895-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="65895-124">Oplysningerne omfatter **DTT-antal**, **Tilgangsantal**, **Afgangsantal** og **Disponibelt antal**.</span><span class="sxs-lookup"><span data-stu-id="65895-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
