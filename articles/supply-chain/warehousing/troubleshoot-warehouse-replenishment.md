---
title: Foretage fejlfinding i forbindelse med genopfyldning af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644867"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="c3b06-103">Foretage fejlfinding i forbindelse med genopfyldning af lagersted</span><span class="sxs-lookup"><span data-stu-id="c3b06-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3b06-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3b06-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="c3b06-105">Jeg får følgende fejlmeddelelse: "Arbejdet %1 kan ikke ophæves, fordi det har uafsluttet genopfyldningsarbejde".</span><span class="sxs-lookup"><span data-stu-id="c3b06-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c3b06-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c3b06-106">Issue description</span></span>

<span data-ttu-id="c3b06-107">Pluk af arbejde blokeres på grund af afhængigt genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="c3b06-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c3b06-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c3b06-108">Issue resolution</span></span>

<span data-ttu-id="c3b06-109">Når du bruger bølgeefterspørgsel til genopfyldning, opretter systemet både genopfyldningsarbejdet og plukarbejdet, hvis en plukplads skal genopfyldes for at opfylde kildeordrebehovet.</span><span class="sxs-lookup"><span data-stu-id="c3b06-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="c3b06-110">Den blokerer dog plukarbejdet, indtil genopfyldningsarbejdet fuldføres.</span><span class="sxs-lookup"><span data-stu-id="c3b06-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="c3b06-111">Denne funktionsmåde er bevidst, fordi plukpladsen ikke har nok lager, medmindre genopfyldningsarbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="c3b06-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="c3b06-112">Fuldfør genopfyldningsarbejdet, og kør derefter plukarbejdet.</span><span class="sxs-lookup"><span data-stu-id="c3b06-112">Complete the replenishment work, and then process the picking work.</span></span>
