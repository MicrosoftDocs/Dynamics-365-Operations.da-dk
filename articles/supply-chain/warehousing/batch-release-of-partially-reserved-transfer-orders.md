---
title: Batch-udgivelse af delvist reserverede flytteordrer
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende batchudlevering af delvist reserverede overførselsordrer fra en mobilenhed."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="7c8ad-103">Batch-udgivelse af delvist reserverede flytteordrer</span><span class="sxs-lookup"><span data-stu-id="7c8ad-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7c8ad-104">Funktionen til batchfrigivelse af delvist reserveret overførselsordrer giver dig mulighed for delvist at frigive overførselsordrer til et lagersted ved hjælp af et batchjob.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="7c8ad-105">Da du har mulighed for at frigive en delmængde, behøver du ikke vente på, at hele ordreantallet er tilgængeligt på lageret, før du frigiver en ordre.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="7c8ad-106">Frigivelsen af ordrer til et lagersted er en proces til avanceret lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="7c8ad-107">Denne proces omfatter aktiviteter, f.eks. plukning, pakning og levering, som en lagermedarbejder kan udføre ved hjælp af en mobil enhed.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="7c8ad-108">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="7c8ad-108">Where it applies</span></span>

<span data-ttu-id="7c8ad-109">I denne funktion frigives overførselsordrer til et lagersted ved hjælp af et batchjob.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="7c8ad-110">Denne funktion er nyttig, når du ikke har tilstrækkelig lagerbeholdning på lagerstedet, men du stadig ønsker at overføre varer fra ét lagersted til en anden.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="7c8ad-111">Sådan konfigureres den</span><span class="sxs-lookup"><span data-stu-id="7c8ad-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="7c8ad-112">Angive opfyldelseskriterier for overførsels- og salgsordrer</span><span class="sxs-lookup"><span data-stu-id="7c8ad-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="7c8ad-113">Inden en ordre kan frigives delvist til et lagersted i en batch, skal opfyldelseskriterierne være opfyldt.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="7c8ad-114">Disse opfyldelseskriterier bestemmes af opfyldelsespolitikken</span><span class="sxs-lookup"><span data-stu-id="7c8ad-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="7c8ad-115">Opfyldelsespolitikker for overførselsordrer og salgsordrer angives på firmaniveau.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="7c8ad-116">Afhængigt af konfigurationen af opfyldelsespolitikken kan frigivelse af ordrer i en batch accepteres eller afvises.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="7c8ad-117">Ordrerne behandles derefter i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="7c8ad-118">Hvis du vil oprette opfyldelsespolitikker for overførsels- og salgsordrer, skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Frigiv til lagersted** \> **Opfyldelsespolitik** og derefter oprette en opfyldelsespolitik ved at angive et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="7c8ad-119">Hvis du vil angive en opfyldelsessats, en værditype og den meddelelse, der vises, hvis opfyldelsespolitikken overtrædes, skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Frigiv til lagersted** \> **Opfyldelsespolitik** og derefter angive felterne **Opfyldelsessats**, **Værditype** og **Meddelelser om opfyldelsesovertrædelse**.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="7c8ad-120">Angive opfyldelsespolitikker for overførsels- og salgsordrer</span><span class="sxs-lookup"><span data-stu-id="7c8ad-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="7c8ad-121">Hvis du vil angive opfyldelsespolitikkerne for overførselsordrer, skal du klikke på **Lagerstyring** \> **Konfiguration** \> **arametre til lager- og lokationsstyring** \> **Flytteordrer** \> **Lokationsstyring** og derefter vælge en opfyldelsespolitik for flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="7c8ad-122">Hvis du vil angive opfyldelsespolitikker for salgsordrer, skal du klikke på **Debitor** \> **Konfiguration** \> **Debitorparametre** \> **Lokationsstyring** og derefter vælge en opfyldelsespolitik for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="7c8ad-123">Tillade frigivelse i en batch og angive det antal, der skal frigives i en batch</span><span class="sxs-lookup"><span data-stu-id="7c8ad-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="7c8ad-124">Et batchjob bruges til at frigive ordrer til et lagersted i en batch.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="7c8ad-125">De parametre, som adskiller de ordrer, der skal køres i et batchjob, angives i selve batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="7c8ad-126">Parameteren **Antal** angiver, om hele antallet skal frigives, eller om det fysisk reserverede antal skal frigives i en batch.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="7c8ad-127">Parameteren **Tillad frigivelse af delvis frigivne ordrer** bestemmer, om ordrer i batchen skal godkendes eller afvises, hvis de tidligere er frigivet delvist.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="7c8ad-128">Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for flytteordrer, skal du klikke på **Lokationsstyring** \> **Frigiv til lagersted** \> **Frigiv flytteordrer automatisk**.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="7c8ad-129">Hvis du vil angive parametrene **Antal** og **Tillad frigivelse af delvis frigivne ordrer** for salgsordrer, skal du klikke på **Lokationsstyring** \> **Frigiv til lagersted** \> **Frigiv salgsordrer automatisk**.</span><span class="sxs-lookup"><span data-stu-id="7c8ad-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

