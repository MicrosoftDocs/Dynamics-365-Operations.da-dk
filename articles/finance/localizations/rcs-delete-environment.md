---
title: Regulatory Configuration Service (RCS) – Slette et RCS-miljø
description: I dette emne forklares, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295812"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="899cb-103">Regulatory Configuration Service (RCS) – Slette et RCS-miljø</span><span class="sxs-lookup"><span data-stu-id="899cb-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="899cb-104">I dette emne forklares, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.</span><span class="sxs-lookup"><span data-stu-id="899cb-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="899cb-105">Før du kan fuldføre trinnene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="899cb-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="899cb-106">Du skal have tildelt rollen **Systemadministrator** for RCS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="899cb-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="899cb-107">Rollen **Systemadministrator** skal være tildelt rollen **RCSDeleteEnvironmentDuty**.</span><span class="sxs-lookup"><span data-stu-id="899cb-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="899cb-108">Slette et RCS-miljø</span><span class="sxs-lookup"><span data-stu-id="899cb-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="899cb-109">Åbn RCS, og vælg arbejdsområdefeltet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="899cb-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="899cb-110">Vælg **Slet RCS-miljø** i afsnittet **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="899cb-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Linket Slet RCS-miljø i afsnittet Relaterede links](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="899cb-112">Gennemse meddelelserne om området for sletning af miljøet i den dialogboks, der vises.</span><span class="sxs-lookup"><span data-stu-id="899cb-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Meddelelser i dialogboksen Slet RCS-miljø](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="899cb-114">Du kan ikke fortryde sletning af et RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="899cb-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="899cb-115">Handlingen sletter det valgte RCS-miljø og eventuelle relaterede data, herunder funktioner og konfigurationer, der er lagret i det globale lager.</span><span class="sxs-lookup"><span data-stu-id="899cb-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="899cb-116">Funktioner og konfigurationer, der deles med andre organisationer, deles ikke længere og slettes, hvis de ikke har nogen afhængigheder.</span><span class="sxs-lookup"><span data-stu-id="899cb-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="899cb-117">Funktioner og konfigurationer, der har afhængigheder, markeres som afbrudt.</span><span class="sxs-lookup"><span data-stu-id="899cb-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="899cb-118">I det felt, der er angivet, skal du angive RCS-miljøets GUID (Global Unique Identifier) for at bekræfte, at du vil slette det.</span><span class="sxs-lookup"><span data-stu-id="899cb-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="899cb-119">Miljøets GUID medtages i meddelelsen om sletning.</span><span class="sxs-lookup"><span data-stu-id="899cb-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="899cb-120">Vælg **Slet miljø**.</span><span class="sxs-lookup"><span data-stu-id="899cb-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="899cb-121">RCS-miljøet og eventuelle relaterede data er nu slettet.</span><span class="sxs-lookup"><span data-stu-id="899cb-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="899cb-122">Når du har slettet et RCS-miljø, kan dataene ikke gendannes.</span><span class="sxs-lookup"><span data-stu-id="899cb-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="899cb-123">Der kan oprettes et nyt RCS-miljø i alle tilgængelige RCS-områder.</span><span class="sxs-lookup"><span data-stu-id="899cb-123">A new RCS environment can be created in any available RCS region.</span></span>
