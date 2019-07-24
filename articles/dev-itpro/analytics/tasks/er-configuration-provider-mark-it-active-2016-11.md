---
title: Oprette konfigurationsudbydere og markere dem som aktive
description: Dette emne forklarer, hvordan en bruger med rollen som Systemadministrator eller Udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER) i Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
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
ms.openlocfilehash: e02cd51478528db56a4f50b134fabf7f9e1dc8ea
ms.sourcegitcommit: a1354c6218b328d4d7dcc149d1339a7af10c48bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2019
ms.locfileid: "1723114"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="f0463-103">Oprette konfigurationsudbydere og markere dem som aktive</span><span class="sxs-lookup"><span data-stu-id="f0463-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0463-104">Dette emne forklarer, hvordan en bruger med rollen som Systemadministrator eller Udvikler til elektronisk rapportering kan oprette en konfigurationsudbyder til elektronisk rapportering (ER) i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0463-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER) in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f0463-105">Hver ER-konfiguration refererer til udbyderen som konfigurations forfatter.</span><span class="sxs-lookup"><span data-stu-id="f0463-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="f0463-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationsudbydere deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="f0463-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="f0463-107">Opret en udbyder</span><span class="sxs-lookup"><span data-stu-id="f0463-107">Create a provider</span></span>
1. <span data-ttu-id="f0463-108">Gå til **navigationsruden** i øverste venstre hjørne, og vælg **Virksomhedsadministration**.</span><span class="sxs-lookup"><span data-stu-id="f0463-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="f0463-109">Gå til **Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f0463-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="f0463-110">Gå til **Relaterede links > Konfigurationsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="f0463-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="f0463-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f0463-111">Select **New**.</span></span>
    - <span data-ttu-id="f0463-112">En udbyderpost har et entydigt ved navn og URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="f0463-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="f0463-113">Gennemse indholdet af denne side, og spring denne procedure over, hvis der allerede findes en post for Litware, Inc. (https://www.litware.com).</span><span class="sxs-lookup"><span data-stu-id="f0463-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="f0463-114">Skriv `Litware, Inc.` i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f0463-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="f0463-115">Indtast `https://www.litware.com` i feltet Internetadresse.</span><span class="sxs-lookup"><span data-stu-id="f0463-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="f0463-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f0463-116">Select **Save**.</span></span>
8. <span data-ttu-id="f0463-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0463-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="f0463-118">Vælg en aktiv udbyder</span><span class="sxs-lookup"><span data-stu-id="f0463-118">Select as an active provider</span></span>
1. <span data-ttu-id="f0463-119">Vælg udbyderen Litware, Inc., .</span><span class="sxs-lookup"><span data-stu-id="f0463-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="f0463-120">Vælg **Angiv aktive**.</span><span class="sxs-lookup"><span data-stu-id="f0463-120">Select **Set active**.</span></span>

