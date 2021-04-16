---
title: Oversigt over kanaler
description: Dette emne indeholder en oversigt over kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800537"
---
# <a name="channels-overview"></a><span data-ttu-id="64846-103">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="64846-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="64846-104">Dette emne indeholder en oversigt over kanaler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="64846-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="64846-105">Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet hver kanal.</span><span class="sxs-lookup"><span data-stu-id="64846-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="64846-106">Kanaltyper</span><span class="sxs-lookup"><span data-stu-id="64846-106">Types of Channels</span></span>

<span data-ttu-id="64846-107">Dynamics 365 Commerce understøtter tre forskellige kanaltyper: detail, callcenter og onlinekanaler.</span><span class="sxs-lookup"><span data-stu-id="64846-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="64846-108">Detailkanaler</span><span class="sxs-lookup"><span data-stu-id="64846-108">Retail channels</span></span>

<span data-ttu-id="64846-109">Detailkanaler repræsenterer standardbutikker til fysisk produkter.</span><span class="sxs-lookup"><span data-stu-id="64846-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="64846-110">Hver butik kan have sine egne POS-kasseapparater, indtægt- og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="64846-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="64846-111">Call center-kanaler</span><span class="sxs-lookup"><span data-stu-id="64846-111">Call center channels</span></span>

<span data-ttu-id="64846-112">Callcenter-kanaler viser callcenter-ordrer og kundestyring.</span><span class="sxs-lookup"><span data-stu-id="64846-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="64846-113">Onlinekanaler</span><span class="sxs-lookup"><span data-stu-id="64846-113">Online channels</span></span>

<span data-ttu-id="64846-114">Onlinekanaler viser online e-handelsudstillingsvinduer.</span><span class="sxs-lookup"><span data-stu-id="64846-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="64846-115">Når der er oprettet en onlinekanal, skal der oprettes et websted vha. værktøjet Microsoft Dynamics 365 Commerce Site Builder eller en anden tredjeparts e-handelsløsning.</span><span class="sxs-lookup"><span data-stu-id="64846-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="64846-116">Grundlæggende konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="64846-116">Channel setup basics</span></span>

<span data-ttu-id="64846-117">Kanalopsætningen udføres i Commerce-værktøjet.</span><span class="sxs-lookup"><span data-stu-id="64846-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="64846-118">Hver kanal kan have sine egne betalingsmetoder, prisgrupper, produkthierarkier, sortimenter og sæt af produkter.</span><span class="sxs-lookup"><span data-stu-id="64846-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="64846-119">Når du har oprettet en kanal, kan du tildele de produkter, som skal føres i denne butik.</span><span class="sxs-lookup"><span data-stu-id="64846-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="64846-120">Hver kanaltype har et unikt sæt funktioner, der evt. skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="64846-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="64846-121">En detailkanal skal f.eks. have tildelt medarbejdere, kasseapparater og kunder.</span><span class="sxs-lookup"><span data-stu-id="64846-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="64846-122">Når der er oprettet en ny kanal, skal den tildeles et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="64846-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="64846-123">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="64846-123">Channel setup prerequisites</span></span>

<span data-ttu-id="64846-124">Før du kan konfigurere en kanal, skal du fuldføre nogle forudsætningsopgaver ud fra kanaltypen.</span><span class="sxs-lookup"><span data-stu-id="64846-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="64846-125">Du kan finde flere oplysninger i [Forudsætninger for konfiguration af kanal](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="64846-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="64846-126">Konfigurer en kanal</span><span class="sxs-lookup"><span data-stu-id="64846-126">Set up a channel</span></span>

<span data-ttu-id="64846-127">Når du har fuldført de nødvendige opgaver, skal du bruge følgende links for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="64846-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="64846-128">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="64846-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="64846-129">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="64846-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="64846-130">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="64846-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="64846-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="64846-131">Additional resources</span></span>

[<span data-ttu-id="64846-132">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="64846-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="64846-133">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="64846-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="64846-134">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="64846-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="64846-135">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="64846-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="64846-136">Konfigurer organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="64846-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]