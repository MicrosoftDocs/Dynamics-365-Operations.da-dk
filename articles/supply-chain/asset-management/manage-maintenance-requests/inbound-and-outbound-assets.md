---
title: Indgående og udgående aktiver
description: Dette emne forklarer, hvordan du registrerer indgående og udgående aktiver i "Styring af aktiver".
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018065"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="a3c97-103">Indgående og udgående aktiver</span><span class="sxs-lookup"><span data-stu-id="a3c97-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a3c97-104">Hvis din virksomhed udfører reparationsarbejde eller vedligeholdelsesarbejde på aktiver, som er modtaget fra andre lokationer eller kunder, kan "Styring af aktiver" spore både indgående aktiver, der er på vej til din virksomhed, og udgående aktiver, der returneres.</span><span class="sxs-lookup"><span data-stu-id="a3c97-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c97-105">Hvis du ønsker at bruge indgående og udgående livscyklustilstande til at administrere aktiver, der kommer ind og returneres, skal du konfigurere vedligeholdelsesanmodning for livscyklustilstande og livscyklusmodeller for at understøtte disse handlinger.</span><span class="sxs-lookup"><span data-stu-id="a3c97-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="a3c97-106">Du kan finde flere oplysninger i [Vedligeholdelsesanmodninger](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="a3c97-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="a3c97-107">Opsætningen af "Styring af aktiver" afgør, om du kan arbejde med indgående og udgående aktiver.</span><span class="sxs-lookup"><span data-stu-id="a3c97-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="a3c97-108">Registrer aktiver som indgående</span><span class="sxs-lookup"><span data-stu-id="a3c97-108">Register assets as inbound</span></span>

1. <span data-ttu-id="a3c97-109">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a3c97-110">Vælg vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a3c97-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="a3c97-111">Vælg **Opdater vedligeholdelsesanmodningens tilstand**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="a3c97-112">Vælg **Indgående** (eller en anden livscyklustilstand, som du har oprettet for indgående aktiver), og vælg dernæst **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registrer aktiver som indgående](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="a3c97-114">Registrer indgående aktiver som modtaget</span><span class="sxs-lookup"><span data-stu-id="a3c97-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="a3c97-115">Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Indgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="a3c97-116">Vælg aktivet eller vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a3c97-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="a3c97-117">Vælg **Modtag aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="a3c97-118">Angiv datoen og tidspunktet i feltet **Modtaget**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="a3c97-119">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-119">Then select **OK**.</span></span> <span data-ttu-id="a3c97-120">Posten blev fjernet fra listesiden **Indgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registrer indgående aktiver som modtaget](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="a3c97-122">Registrer aktiver som udgående</span><span class="sxs-lookup"><span data-stu-id="a3c97-122">Register assets as outbound</span></span>

<span data-ttu-id="a3c97-123">Når du har fuldført vedligeholdelses-eller reparationsopgaven, kan du registrere aktivet som returneret.</span><span class="sxs-lookup"><span data-stu-id="a3c97-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="a3c97-124">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a3c97-125">Vælg vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a3c97-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="a3c97-126">Vælg **Opdater vedligeholdelsesanmodningens tilstand**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="a3c97-127">Vælg **Udgående** (eller en anden livscyklustilstand, som du har oprettet for udgående aktiver), og vælg dernæst **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="a3c97-128">Registrer udgående aktiver som leveret</span><span class="sxs-lookup"><span data-stu-id="a3c97-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="a3c97-129">Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Udgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="a3c97-130">Vælg aktivet eller vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a3c97-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="a3c97-131">Vælg **Levér aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="a3c97-132">Angiv datoen og tidspunktet i feltet **Leveret**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="a3c97-133">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-133">Then select **OK**.</span></span> <span data-ttu-id="a3c97-134">Posten blev fjernet fra listesiden **Udgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="a3c97-134">The record is removed from the **Outbound assets** list page.</span></span>
