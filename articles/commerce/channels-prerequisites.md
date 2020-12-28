---
title: Forudsætninger for konfiguration af kanal
description: Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411039"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="61e68-103">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="61e68-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="61e68-104">Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="61e68-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="61e68-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="61e68-105">Overview</span></span>

<span data-ttu-id="61e68-106">Før en Dynamics 365 Commerce-kanal kan oprettes, skal der udføres flere nødvendige opgaver.</span><span class="sxs-lookup"><span data-stu-id="61e68-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="61e68-107">Følgende lister med nødvendige opgaver er organiseret efter kanaltype.</span><span class="sxs-lookup"><span data-stu-id="61e68-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="61e68-108">Der skrives stadig en dokumentation, og links opdateres, efterhånden som der udgives nyt indhold.</span><span class="sxs-lookup"><span data-stu-id="61e68-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="61e68-109">Initialisering</span><span class="sxs-lookup"><span data-stu-id="61e68-109">Initialization</span></span>

- [<span data-ttu-id="61e68-110">Initialisere oprindelsesdata</span><span class="sxs-lookup"><span data-stu-id="61e68-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="61e68-111">Globale forudsætninger kræves til alle kanaltyper</span><span class="sxs-lookup"><span data-stu-id="61e68-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="61e68-112">Definere og konfigurere strukturen for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="61e68-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="61e68-113">Konfigurere dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="61e68-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="61e68-114">Konfigurer et lagersted</span><span class="sxs-lookup"><span data-stu-id="61e68-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="61e68-115">Konfigurere moms</span><span class="sxs-lookup"><span data-stu-id="61e68-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="61e68-116">Konfigurere en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="61e68-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="61e68-117">Oprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="61e68-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="61e68-118">Oprette en standardkunde og -adressekartotek</span><span class="sxs-lookup"><span data-stu-id="61e68-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="61e68-119">Forudsætninger for detailkanal</span><span class="sxs-lookup"><span data-stu-id="61e68-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="61e68-120">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="61e68-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="61e68-121">Oprette en profil for detailfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="61e68-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="61e68-122">Oprette et medarbejderadressekartotek</span><span class="sxs-lookup"><span data-stu-id="61e68-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="61e68-123">Konfigurere et skærmlayout</span><span class="sxs-lookup"><span data-stu-id="61e68-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="61e68-124">Oprette en hardwarestation</span><span class="sxs-lookup"><span data-stu-id="61e68-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="61e68-125">Forudsætninger for callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="61e68-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="61e68-126">Call center-parametre</span><span class="sxs-lookup"><span data-stu-id="61e68-126">Call center parameters</span></span>
- [<span data-ttu-id="61e68-127">Callcenter-ordre og refusionsbetalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="61e68-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="61e68-128">Callcenterets leveringsmåder og -gebyrer</span><span class="sxs-lookup"><span data-stu-id="61e68-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="61e68-129">Forudsætninger for onlinekanal</span><span class="sxs-lookup"><span data-stu-id="61e68-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="61e68-130">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="61e68-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="61e68-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="61e68-131">Additional resources</span></span>

[<span data-ttu-id="61e68-132">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="61e68-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="61e68-133">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="61e68-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="61e68-134">Konfigurer organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="61e68-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="61e68-135">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="61e68-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="61e68-136">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="61e68-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="61e68-137">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="61e68-137">Set up an online channel</span></span>](channel-setup-online.md)
