---
title: Oprette konfigurationsudbydere og markere dem som aktive
description: Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595389"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="d251f-103">Oprette konfigurationsudbydere og markere dem som aktive</span><span class="sxs-lookup"><span data-stu-id="d251f-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d251f-104">Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="d251f-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="d251f-105">Hver ER-konfiguration refererer til udbyderen som konfigurations forfatter.</span><span class="sxs-lookup"><span data-stu-id="d251f-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="d251f-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationsudbydere deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="d251f-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="d251f-107">Opret en udbyder</span><span class="sxs-lookup"><span data-stu-id="d251f-107">Create a provider</span></span>
1. <span data-ttu-id="d251f-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d251f-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d251f-109">Klik på Konfigurationsudbydere.</span><span class="sxs-lookup"><span data-stu-id="d251f-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="d251f-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d251f-110">Click New.</span></span>
    * <span data-ttu-id="d251f-111">En udbyderpost har et entydigt ved navn og URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="d251f-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="d251f-112">Gennemse indholdet af denne side, og spring denne procedure over, hvis der allerede findes en post for Litware, Inc. (https://www.litware.com).</span><span class="sxs-lookup"><span data-stu-id="d251f-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="d251f-113">Skriv "Litware, Inc." i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d251f-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="d251f-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d251f-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="d251f-115">Indtast 'https://www.litware.com' i feltet Internetadresse.</span><span class="sxs-lookup"><span data-stu-id="d251f-115">In the Internet address field, type 'https://www.litware.com'.</span></span>
    * https://www.litware.com  
6. <span data-ttu-id="d251f-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d251f-116">Click Save.</span></span>
7. <span data-ttu-id="d251f-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d251f-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="d251f-118">Vælg en aktiv udbyder</span><span class="sxs-lookup"><span data-stu-id="d251f-118">Select as an active provider</span></span>
1. <span data-ttu-id="d251f-119">Vælg udbyderen Litware, Inc., .</span><span class="sxs-lookup"><span data-stu-id="d251f-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="d251f-120">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d251f-120">Click Set active.</span></span>

