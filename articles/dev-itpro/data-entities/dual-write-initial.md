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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797292"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="a94e5-103">Udførelsesrækkefølge for indledende synkronisering af Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a94e5-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="a94e5-104">Før du bruger dataintegration, skal du oprette de oprindelige data, der kræves til debitorer, kreditorer og kontakter.</span><span class="sxs-lookup"><span data-stu-id="a94e5-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="a94e5-105">Hvis du for eksempel vil oprette et nyt **Leverandørgruppe**-element og angive **Betalingsbetingelser** som **Net30**, skal du, før du forsøger at oprette **Leverandørgruppe**-elementet, sikre dig, at **Net30** findes i både Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a94e5-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="a94e5-106">(I fremtiden vil vi frigive en dobbeltskrivningsplatform med en funktionalitet kaldet **Første synkronisering**. Den vil udføre en engangsdatasynkronisering mellem Finance and Operations og Common Data Service som en del af dobbeltskrivningsopsætningen).</span><span class="sxs-lookup"><span data-stu-id="a94e5-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="a94e5-107">Tips: Vi udgiver et kort med dobbeltskrivning for alle referencedata, herunder **Betalingsbetingelser** (betalingsvilkår).</span><span class="sxs-lookup"><span data-stu-id="a94e5-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="a94e5-108">Hvis du allerede har de første data i ét system, kan en lille opdateringshandling på en post udløse dobbeltskrivning på den pågældende post.</span><span class="sxs-lookup"><span data-stu-id="a94e5-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="a94e5-109">Du skal følge følgende prioriteringsrækkefølge og sørge for, at de første data er tilgængelige på både Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a94e5-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="a94e5-110">Leverandør</span><span class="sxs-lookup"><span data-stu-id="a94e5-110">Vendor</span></span>

<span data-ttu-id="a94e5-111">Udførelsesrækkefølgen for leverandøren er:</span><span class="sxs-lookup"><span data-stu-id="a94e5-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="a94e5-112">Kunde (organisation)</span><span class="sxs-lookup"><span data-stu-id="a94e5-112">Customer (Organization)</span></span>

<span data-ttu-id="a94e5-113">Udførelsesrækkefølgen for kunden er:</span><span class="sxs-lookup"><span data-stu-id="a94e5-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="a94e5-114">Kontakt (person)</span><span class="sxs-lookup"><span data-stu-id="a94e5-114">Contact (Person)</span></span>

<span data-ttu-id="a94e5-115">Udførelsesrækkefølgen for kontakten er:</span><span class="sxs-lookup"><span data-stu-id="a94e5-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
