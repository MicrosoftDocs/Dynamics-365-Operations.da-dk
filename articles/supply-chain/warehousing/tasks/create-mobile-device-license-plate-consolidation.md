---
title: Oprette et menupunkt for mobilenhedens nummerpladekonsolidering
description: Denne procedure viser, hvordan du opretter et menupunkt til din mobilenhed for arbejdet med id-konsolidering.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3f5f572461de007f137ffa7ea05c535371f95b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977232"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="4b888-103">Oprette et menupunkt for mobilenhedens nummerpladekonsolidering</span><span class="sxs-lookup"><span data-stu-id="4b888-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b888-104">Denne procedure viser, hvordan du opretter et menupunkt til din mobilenhed for arbejdet med id-konsolidering.</span><span class="sxs-lookup"><span data-stu-id="4b888-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="4b888-105">Det gør det muligt for lagermedarbejderne at konsolidere varer for ét id med varer for et andet id inden for samme lokalitet.</span><span class="sxs-lookup"><span data-stu-id="4b888-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="4b888-106">De kan for eksempel bruge det, hvis efterfølgende midlertidige trin er ens på begge arbejdsordrer, så arbejdet kun skal udføres én gang for de varer, der er flettet.</span><span class="sxs-lookup"><span data-stu-id="4b888-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="4b888-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="4b888-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="4b888-108">Denne opgave udføres normalt af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="4b888-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="4b888-109">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="4b888-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="4b888-110">Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="4b888-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="4b888-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4b888-111">Click New.</span></span>
3. <span data-ttu-id="4b888-112">Skriv en værdi i feltet Menupunktnavn.</span><span class="sxs-lookup"><span data-stu-id="4b888-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="4b888-113">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="4b888-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="4b888-114">Vælg "Indirekte" i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="4b888-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="4b888-115">Vælg 'Konsolider id'er' i feltet Aktivitetskode.</span><span class="sxs-lookup"><span data-stu-id="4b888-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

