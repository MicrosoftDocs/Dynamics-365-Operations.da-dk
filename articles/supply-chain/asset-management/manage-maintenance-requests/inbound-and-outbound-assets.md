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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a7239bf5f8e53e61c4259abbcbf2ff740f4cef55
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889931"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="f782e-103">Indgående og udgående aktiver</span><span class="sxs-lookup"><span data-stu-id="f782e-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f782e-104">Hvis din virksomhed udfører reparationsarbejde eller vedligeholdelsesarbejde på aktiver, som er modtaget fra andre lokationer eller kunder, kan "Styring af aktiver" spore både indgående aktiver, der er på vej til din virksomhed, og udgående aktiver, der returneres.</span><span class="sxs-lookup"><span data-stu-id="f782e-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="f782e-105">Hvis du ønsker at bruge indgående og udgående livscyklustilstande til at administrere aktiver, der kommer ind og returneres, skal du konfigurere vedligeholdelsesanmodning for livscyklustilstande og livscyklusmodeller for at understøtte disse handlinger.</span><span class="sxs-lookup"><span data-stu-id="f782e-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="f782e-106">Du kan finde flere oplysninger i [Vedligeholdelsesanmodninger](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="f782e-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="f782e-107">Opsætningen af "Styring af aktiver" afgør, om du kan arbejde med indgående og udgående aktiver.</span><span class="sxs-lookup"><span data-stu-id="f782e-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="f782e-108">Registrer aktiver som indgående</span><span class="sxs-lookup"><span data-stu-id="f782e-108">Register assets as inbound</span></span>

1. <span data-ttu-id="f782e-109">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="f782e-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f782e-110">Vælg vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="f782e-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="f782e-111">Vælg **Opdater vedligeholdelsesanmodningens tilstand**.</span><span class="sxs-lookup"><span data-stu-id="f782e-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f782e-112">Vælg **Indgående** (eller en anden livscyklustilstand, som du har oprettet for indgående aktiver), og vælg dernæst **OK**.</span><span class="sxs-lookup"><span data-stu-id="f782e-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registrer aktiver som indgående](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="f782e-114">Registrer indgående aktiver som modtaget</span><span class="sxs-lookup"><span data-stu-id="f782e-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="f782e-115">Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Indgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="f782e-116">Vælg aktivet eller vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="f782e-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f782e-117">Vælg **Modtag aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="f782e-118">Angiv datoen og tidspunktet i feltet **Modtaget**.</span><span class="sxs-lookup"><span data-stu-id="f782e-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="f782e-119">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f782e-119">Then select **OK**.</span></span> <span data-ttu-id="f782e-120">Posten blev fjernet fra listesiden **Indgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registrer indgående aktiver som modtaget](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="f782e-122">Registrer aktiver som udgående</span><span class="sxs-lookup"><span data-stu-id="f782e-122">Register assets as outbound</span></span>

<span data-ttu-id="f782e-123">Når du har fuldført vedligeholdelses-eller reparationsopgaven, kan du registrere aktivet som returneret.</span><span class="sxs-lookup"><span data-stu-id="f782e-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="f782e-124">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="f782e-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f782e-125">Vælg vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="f782e-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="f782e-126">Vælg **Opdater vedligeholdelsesanmodningens tilstand**.</span><span class="sxs-lookup"><span data-stu-id="f782e-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f782e-127">Vælg **Udgående** (eller en anden livscyklustilstand, som du har oprettet for udgående aktiver), og vælg dernæst **OK**.</span><span class="sxs-lookup"><span data-stu-id="f782e-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="f782e-128">Registrer udgående aktiver som leveret</span><span class="sxs-lookup"><span data-stu-id="f782e-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="f782e-129">Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Udgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="f782e-130">Vælg aktivet eller vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="f782e-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f782e-131">Vælg **Levér aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="f782e-132">Angiv datoen og tidspunktet i feltet **Leveret**.</span><span class="sxs-lookup"><span data-stu-id="f782e-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="f782e-133">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f782e-133">Then select **OK**.</span></span> <span data-ttu-id="f782e-134">Posten blev fjernet fra listesiden **Udgående aktiver**.</span><span class="sxs-lookup"><span data-stu-id="f782e-134">The record is removed from the **Outbound assets** list page.</span></span>
