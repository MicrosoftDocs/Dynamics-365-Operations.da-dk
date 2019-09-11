---
title: Udførelsesrækkefølge for indledende synkronisering af Finance and Operations og Common Data Service
description: Dette emne angiver den synkroniseringsrækkefølge, du skal følge for at oprette de første data.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873122"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="440d8-103">Udførelsesrækkefølge for indledende synkronisering af Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="440d8-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="440d8-104">Før du bruger dataintegration, skal du oprette de første data, der kræves til debitorer, kreditorer og kontakter.</span><span class="sxs-lookup"><span data-stu-id="440d8-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="440d8-105">Du kan f.eks. oprette en ny **Leverandørgruppe** og angive dens **Betalingsbetingelser** til **Net30**.</span><span class="sxs-lookup"><span data-stu-id="440d8-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="440d8-106">I dette tilfælde skal du sikre dig, at **Net30** findes i både Microsoft Dynamics 365 for Finance and Operations og Common Data Service, inden du forsøger at oprette elementet **Leverandørgruppe**.</span><span class="sxs-lookup"><span data-stu-id="440d8-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="440d8-107">(I fremtiden vil Microsoft frigive en dobbeltskrivningsplatform med en funktionalitet kaldet Første synkronisering. Den vil udføre en engangsdatasynkronisering mellem Finance and Operations og Common Data Service som en del af dobbeltskrivningsopsætningen).</span><span class="sxs-lookup"><span data-stu-id="440d8-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="440d8-108">Microsoft frigiver et kort med dobbeltskrivning for alle referencedata, herunder **Betalingsbetingelser** (betalingsvilkår).</span><span class="sxs-lookup"><span data-stu-id="440d8-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="440d8-109">Hvis du allerede har de første data i ét system, kan en lille opdateringshandling på en post udløse dobbeltskrivning på den pågældende post.</span><span class="sxs-lookup"><span data-stu-id="440d8-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="440d8-110">Du skal følge nedenstående prioriteringsrækkefølge og sørge for, at de første data er tilgængelige i både Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="440d8-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="440d8-111">Leverandør</span><span class="sxs-lookup"><span data-stu-id="440d8-111">Vendor</span></span>

<span data-ttu-id="440d8-112">Her er afviklingsrækkefølgen for objektet **Leverandør**:</span><span class="sxs-lookup"><span data-stu-id="440d8-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="440d8-113">Leverandørgruppe</span><span class="sxs-lookup"><span data-stu-id="440d8-113">Vendor group</span></span>

    1. <span data-ttu-id="440d8-114">Betalingsbetingelse</span><span class="sxs-lookup"><span data-stu-id="440d8-114">Terms of payment</span></span>

        1. <span data-ttu-id="440d8-115">Betalingsdag og -linjer</span><span class="sxs-lookup"><span data-stu-id="440d8-115">Payment day and lines</span></span>
        2. <span data-ttu-id="440d8-116">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="440d8-116">Payment schedule</span></span>

2. <span data-ttu-id="440d8-117">Kreditorbetalingsmetode</span><span class="sxs-lookup"><span data-stu-id="440d8-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="440d8-118">Kunde (organisation)</span><span class="sxs-lookup"><span data-stu-id="440d8-118">Customer (Organization)</span></span>

<span data-ttu-id="440d8-119">Her er afviklingsrækkefølgen for objektet **Kunde**:</span><span class="sxs-lookup"><span data-stu-id="440d8-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="440d8-120">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="440d8-120">Customer group</span></span>

    1. <span data-ttu-id="440d8-121">Betalingsbetingelse</span><span class="sxs-lookup"><span data-stu-id="440d8-121">Terms of payment</span></span>

        1. <span data-ttu-id="440d8-122">Betalingsdag og -linjer</span><span class="sxs-lookup"><span data-stu-id="440d8-122">Payment day and lines</span></span>
        2. <span data-ttu-id="440d8-123">Betaling</span><span class="sxs-lookup"><span data-stu-id="440d8-123">Payment</span></span> 

2. <span data-ttu-id="440d8-124">Debitorbetalingsmetode</span><span class="sxs-lookup"><span data-stu-id="440d8-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="440d8-125">Kontakt (person)</span><span class="sxs-lookup"><span data-stu-id="440d8-125">Contact (Person)</span></span>

<span data-ttu-id="440d8-126">Her er afviklingsrækkefølgen for objektet **Kontakt**:</span><span class="sxs-lookup"><span data-stu-id="440d8-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="440d8-127">Debitor </span><span class="sxs-lookup"><span data-stu-id="440d8-127">Customer</span></span>
2. <span data-ttu-id="440d8-128">Leverandør</span><span class="sxs-lookup"><span data-stu-id="440d8-128">Vendor</span></span>
