---
title: Oprette et menupunkt for mobilenhedens nummerpladekonsolidering
description: Denne procedure viser, hvordan du opretter et menupunkt til din mobilenhed for arbejdet med id-konsolidering.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc610a16f4b0e574b5d5e7f8fc9ecf1e12534645
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847297"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="b2d84-103">Oprette et menupunkt for mobilenhedens nummerpladekonsolidering</span><span class="sxs-lookup"><span data-stu-id="b2d84-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2d84-104">Denne procedure viser, hvordan du opretter et menupunkt til din mobilenhed for arbejdet med id-konsolidering.</span><span class="sxs-lookup"><span data-stu-id="b2d84-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="b2d84-105">Det gør det muligt for lagermedarbejderne at konsolidere varer for ét id med varer for et andet id inden for samme lokalitet.</span><span class="sxs-lookup"><span data-stu-id="b2d84-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="b2d84-106">De kan for eksempel bruge det, hvis efterfølgende midlertidige trin er ens på begge arbejdsordrer, så arbejdet kun skal udføres én gang for de varer, der er flettet.</span><span class="sxs-lookup"><span data-stu-id="b2d84-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="b2d84-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b2d84-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b2d84-108">Denne opgave udføres normalt af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="b2d84-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="b2d84-109">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="b2d84-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="b2d84-110">Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="b2d84-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="b2d84-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b2d84-111">Click New.</span></span>
3. <span data-ttu-id="b2d84-112">Skriv en værdi i feltet Menupunktnavn.</span><span class="sxs-lookup"><span data-stu-id="b2d84-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="b2d84-113">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="b2d84-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="b2d84-114">Vælg "Indirekte" i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="b2d84-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="b2d84-115">Vælg 'Konsolider id'er' i feltet Aktivitetskode.</span><span class="sxs-lookup"><span data-stu-id="b2d84-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

