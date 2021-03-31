---
title: Føje en adresse til en serviceordre
description: Dette emne beskriver, hvordan du føjer en kundeadresse til en serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b9c6a410acbfebb3a83e753c422dd87dbf52566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205851"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="e7356-103">Føje en adresse til en serviceordre</span><span class="sxs-lookup"><span data-stu-id="e7356-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e7356-104">Dette emne beskriver, hvordan du føjer en kundeadresse til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="e7356-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="e7356-105">Når du opretter en serviceordre, overføres adresseoplysningerne fra det projekt, som serviceordren er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="e7356-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="e7356-106">Du kan dog vælge en alternativ placering fra adresser, der allerede er angivet i Microsoft Dynamics AX for debitorer, kreditorer, websteder, lagre, serviceordrer og projekter.</span><span class="sxs-lookup"><span data-stu-id="e7356-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="e7356-107">Du kan også oprette en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="e7356-107">You can also create a new address.</span></span> <span data-ttu-id="e7356-108">Den nye adresse overføres som standard til projektet.</span><span class="sxs-lookup"><span data-stu-id="e7356-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="e7356-109">Du kan dog angive, at den nye adresse kun er relevant for denne forekomst af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="e7356-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="e7356-110">Hvis du gør det, overføres den nye adresse ikke til projektet.</span><span class="sxs-lookup"><span data-stu-id="e7356-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="e7356-111">Oprette en debitoradresse for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="e7356-111">Create a customer address for a service order</span></span>

<span data-ttu-id="e7356-112">Hvis du vil føje en adresse til en serviceordre, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="e7356-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="e7356-113">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="e7356-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e7356-114">Åbn den serviceordre, som du vil oprette en adresse for.</span><span class="sxs-lookup"><span data-stu-id="e7356-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="e7356-115">Klik på **Rediger** i **handlingsruden**, og klik derefter på **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="e7356-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="e7356-116">Klik på **Tilføj** i oversigtspanelet **Tilføj adresse**.</span><span class="sxs-lookup"><span data-stu-id="e7356-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="e7356-117">I formularen **Ny adresse** skal du indtaste et entydigt navn til adressen og udfylde de resterende felter.</span><span class="sxs-lookup"><span data-stu-id="e7356-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="e7356-118">Hvis du angiver det samme navn som en eksisterende adresse, overskriver de oplysninger, du angiver i resterende felter, oplysninger for den eksisterende adresse.</span><span class="sxs-lookup"><span data-stu-id="e7356-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="e7356-119">Klik på **OK** for at kopiere den nye adresse til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="e7356-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="e7356-120">Angive en alternativ adresse på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="e7356-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="e7356-121">Hvis du vil føje en alternativ adresse til en serviceordre, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="e7356-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="e7356-122">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="e7356-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e7356-123">Åbn den serviceordre, som du vil angive en alternativ adresse for.</span><span class="sxs-lookup"><span data-stu-id="e7356-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="e7356-124">Klik på **Rediger** i **handlingsruden**, og klik derefter på **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="e7356-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="e7356-125">Klik på **Tilføj** i oversigtspanelet **Anden adresse**.</span><span class="sxs-lookup"><span data-stu-id="e7356-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="e7356-126">I formularen **Adressevalg** skal du i feltet **Posttype** vælge **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="e7356-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="e7356-127">Vælg en adresse, og klik derefter på **OK** for at kopiere den til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="e7356-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]