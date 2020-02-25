---
title: Forudsætninger for konfiguration af kanal
description: Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002283"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="8d13f-103">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8d13f-104">Dette emne indeholder en oversigt over forudsætninger for konfiguration af kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d13f-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8d13f-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="8d13f-105">Overview</span></span>

<span data-ttu-id="8d13f-106">Før en Dynamics 365 Commerce-kanal kan oprettes, skal der udføres flere nødvendige opgaver.</span><span class="sxs-lookup"><span data-stu-id="8d13f-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="8d13f-107">Følgende lister med nødvendige opgaver er organiseret efter kanaltype.</span><span class="sxs-lookup"><span data-stu-id="8d13f-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="8d13f-108">Der skrives stadig en dokumentation, og links opdateres, efterhånden som der udgives nyt indhold.</span><span class="sxs-lookup"><span data-stu-id="8d13f-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="8d13f-109">Initialisering</span><span class="sxs-lookup"><span data-stu-id="8d13f-109">Initialization</span></span>

- [<span data-ttu-id="8d13f-110">Initialisere oprindelsesdata</span><span class="sxs-lookup"><span data-stu-id="8d13f-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="8d13f-111">Globale forudsætninger kræves til alle kanaltyper</span><span class="sxs-lookup"><span data-stu-id="8d13f-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="8d13f-112">Definere og konfigurere strukturen for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="8d13f-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="8d13f-113">Konfigurere dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="8d13f-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="8d13f-114">Konfigurer et lagersted</span><span class="sxs-lookup"><span data-stu-id="8d13f-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="8d13f-115">Konfigurere moms</span><span class="sxs-lookup"><span data-stu-id="8d13f-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8d13f-116">Konfigurere en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="8d13f-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="8d13f-117">Oprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="8d13f-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8d13f-118">Oprette en standardkunde og -adressekartotek</span><span class="sxs-lookup"><span data-stu-id="8d13f-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="8d13f-119">Forudsætninger for detailkanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="8d13f-120">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="8d13f-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8d13f-121">Oprette en profil for detailfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="8d13f-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="8d13f-122">Oprette et medarbejderadressekartotek</span><span class="sxs-lookup"><span data-stu-id="8d13f-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="8d13f-123">Konfigurere et skærmlayout</span><span class="sxs-lookup"><span data-stu-id="8d13f-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8d13f-124">Oprette en hardwarestation</span><span class="sxs-lookup"><span data-stu-id="8d13f-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="8d13f-125">Forudsætninger for callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="8d13f-126">Call center-parametre</span><span class="sxs-lookup"><span data-stu-id="8d13f-126">Call center parameters</span></span>
- <span data-ttu-id="8d13f-127">Call center-refusionsmetoder</span><span class="sxs-lookup"><span data-stu-id="8d13f-127">Call center refund methods</span></span>
- <span data-ttu-id="8d13f-128">Lejetyper</span><span class="sxs-lookup"><span data-stu-id="8d13f-128">Rental types</span></span>
- <span data-ttu-id="8d13f-129">Betalingstjenester</span><span class="sxs-lookup"><span data-stu-id="8d13f-129">Payment services</span></span>
- <span data-ttu-id="8d13f-130">Koder for ordrehold</span><span class="sxs-lookup"><span data-stu-id="8d13f-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="8d13f-131">Forudsætninger for onlinekanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="8d13f-132">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="8d13f-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="8d13f-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8d13f-133">Additional resources</span></span>

[<span data-ttu-id="8d13f-134">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="8d13f-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8d13f-135">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="8d13f-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="8d13f-136">Konfigurer organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="8d13f-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="8d13f-137">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="8d13f-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="8d13f-138">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="8d13f-139">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="8d13f-139">Set up an online channel</span></span>](channel-setup-online.md)
