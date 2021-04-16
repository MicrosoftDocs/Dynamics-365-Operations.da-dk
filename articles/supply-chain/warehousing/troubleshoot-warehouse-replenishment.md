---
title: Foretage fejlfinding i forbindelse med genopfyldning af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828076"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="2b71f-103">Foretage fejlfinding i forbindelse med genopfyldning af lagersted</span><span class="sxs-lookup"><span data-stu-id="2b71f-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b71f-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2b71f-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="2b71f-105">Jeg får følgende fejlmeddelelse: "Arbejdet %1 kan ikke ophæves, fordi det har uafsluttet genopfyldningsarbejde".</span><span class="sxs-lookup"><span data-stu-id="2b71f-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b71f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2b71f-106">Issue description</span></span>

<span data-ttu-id="2b71f-107">Pluk af arbejde blokeres på grund af afhængigt genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="2b71f-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b71f-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2b71f-108">Issue resolution</span></span>

<span data-ttu-id="2b71f-109">Når du bruger bølgeefterspørgsel til genopfyldning, opretter systemet både genopfyldningsarbejdet og plukarbejdet, hvis en plukplads skal genopfyldes for at opfylde kildeordrebehovet.</span><span class="sxs-lookup"><span data-stu-id="2b71f-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="2b71f-110">Den blokerer dog plukarbejdet, indtil genopfyldningsarbejdet fuldføres.</span><span class="sxs-lookup"><span data-stu-id="2b71f-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="2b71f-111">Denne funktionsmåde er bevidst, fordi plukpladsen ikke har nok lager, medmindre genopfyldningsarbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="2b71f-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="2b71f-112">Fuldfør genopfyldningsarbejdet, og kør derefter plukarbejdet.</span><span class="sxs-lookup"><span data-stu-id="2b71f-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]