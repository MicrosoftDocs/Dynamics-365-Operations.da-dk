---
title: Zonemaster i transportstyring
description: I dette emne beskrives, hvordan transportstyring kan opdele geografiske steder i zoner.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425095"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="9ae2b-103">Zonemaster i transportstyring</span><span class="sxs-lookup"><span data-stu-id="9ae2b-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ae2b-104">I transportstyring kan du opdele geografiske steder i zoner.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="9ae2b-105">Opdeling af steder i zoner kan hjælpe med at:</span><span class="sxs-lookup"><span data-stu-id="9ae2b-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="9ae2b-106">**Forenkle transportprisen** – Zonevis prissætning kan være mere enkel end en individuel stedbaseret prisfastsættelse, især når transportadresser er spredte.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="9ae2b-107">**Optimere lastplanlægning** – Ved at konsolidere laster efter zoner.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="9ae2b-108">**Optimere ruteplanlægning** – Ved at tildele bestemte ruteplaner i bestemte zoner.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="9ae2b-109">Du kan definere zoner på baggrund af metadatafeltværdier (f.eks. land/område, postnummer eller fragttjeneste), der skal kvalificere de enkelte zoner.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="9ae2b-110">Der kræves ikke zonedefinitioner, hvis din transportpris ikke anvender et zonebegreb.</span><span class="sxs-lookup"><span data-stu-id="9ae2b-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>