---
title: Forudsætninger for konfiguration af kanal
description: Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
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
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800513"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="3d9a5-103">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d9a5-104">Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d9a5-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3d9a5-105">Før en Dynamics 365 Commerce-kanal kan oprettes, skal der udføres flere nødvendige opgaver.</span><span class="sxs-lookup"><span data-stu-id="3d9a5-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="3d9a5-106">Følgende lister med nødvendige opgaver er organiseret efter kanaltype.</span><span class="sxs-lookup"><span data-stu-id="3d9a5-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="3d9a5-107">Der skrives stadig en dokumentation, og links opdateres, efterhånden som der udgives nyt indhold.</span><span class="sxs-lookup"><span data-stu-id="3d9a5-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="3d9a5-108">Initialisering</span><span class="sxs-lookup"><span data-stu-id="3d9a5-108">Initialization</span></span>

- [<span data-ttu-id="3d9a5-109">Initialisere oprindelsesdata</span><span class="sxs-lookup"><span data-stu-id="3d9a5-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="3d9a5-110">Globale forudsætninger kræves til alle kanaltyper</span><span class="sxs-lookup"><span data-stu-id="3d9a5-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="3d9a5-111">Definere og konfigurere strukturen for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="3d9a5-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="3d9a5-112">Konfigurere dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3d9a5-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="3d9a5-113">Konfigurer et lagersted</span><span class="sxs-lookup"><span data-stu-id="3d9a5-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="3d9a5-114">Konfigurere moms</span><span class="sxs-lookup"><span data-stu-id="3d9a5-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="3d9a5-115">Konfigurere en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="3d9a5-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="3d9a5-116">Oprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="3d9a5-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="3d9a5-117">Oprette en standardkunde og -adressekartotek</span><span class="sxs-lookup"><span data-stu-id="3d9a5-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="3d9a5-118">Forudsætninger for detailkanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="3d9a5-119">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="3d9a5-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="3d9a5-120">Oprette en profil for detailfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="3d9a5-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="3d9a5-121">Oprette et medarbejderadressekartotek</span><span class="sxs-lookup"><span data-stu-id="3d9a5-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="3d9a5-122">Konfigurere et skærmlayout</span><span class="sxs-lookup"><span data-stu-id="3d9a5-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="3d9a5-123">Oprette en hardwarestation</span><span class="sxs-lookup"><span data-stu-id="3d9a5-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="3d9a5-124">Forudsætninger for callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="3d9a5-125">Call center-parametre</span><span class="sxs-lookup"><span data-stu-id="3d9a5-125">Call center parameters</span></span>
- [<span data-ttu-id="3d9a5-126">Callcenter-ordre og refusionsbetalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="3d9a5-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="3d9a5-127">Callcenterets leveringsmåder og -gebyrer</span><span class="sxs-lookup"><span data-stu-id="3d9a5-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="3d9a5-128">Forudsætninger for onlinekanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="3d9a5-129">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="3d9a5-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="3d9a5-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3d9a5-130">Additional resources</span></span>

[<span data-ttu-id="3d9a5-131">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="3d9a5-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3d9a5-132">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3d9a5-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3d9a5-133">Konfigurer organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3d9a5-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="3d9a5-134">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="3d9a5-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="3d9a5-135">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="3d9a5-136">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="3d9a5-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
