---
title: Der opstår en fejl, når lokationen vælges under registrering af pluklisten
description: Der opstår en fejl, når lokationen vælges under registrering af pluklisten.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026355"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="c1514-103">Der opstår en fejl, når lokationen vælges under registrering af pluklisten</span><span class="sxs-lookup"><span data-stu-id="c1514-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="c1514-104">KB-nummer: 4613106</span><span class="sxs-lookup"><span data-stu-id="c1514-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="c1514-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c1514-105">Symptoms</span></span>

<span data-ttu-id="c1514-106">Dette problem opstår, når systemet er konfigureret til automatisk at reservere salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c1514-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="c1514-107">Hvis du prøver at vælge lokationen for en pluklisteregistreringslinje, modtager du følgende fejlmeddelelse, når du bruger reservationsprocesser i lokationsstyring (WMS):</span><span class="sxs-lookup"><span data-stu-id="c1514-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="c1514-108">Antallet kan ikke opdateres med nye dimensioner</span><span class="sxs-lookup"><span data-stu-id="c1514-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="c1514-109">Denne fejl kan forekomme, fordi du ikke har tilstrækkelig lagerbeholdning på en angivet lokation.</span><span class="sxs-lookup"><span data-stu-id="c1514-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="c1514-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="c1514-110">Resolution</span></span>

<span data-ttu-id="c1514-111">Systemet fungerer som designet.</span><span class="sxs-lookup"><span data-stu-id="c1514-111">The system is behaving as designed.</span></span>

<span data-ttu-id="c1514-112">Hvis du f.eks. bruger reservationsprocessen på lagerstedsniveau, anbefales det, at du bruger den manuelle reservationsproces fra pluklinjen, hvis beholdningen på en bestemt lokation ikke er tilstrækkelig, og der ikke reserveres nok på alle lagerdimensionsniveauer.</span><span class="sxs-lookup"><span data-stu-id="c1514-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="c1514-113">Du kan derefter bruge funktionen *Reserver parti* til at fordele de lavere reservationer, f.eks. lokation, til alle tilgængelige disponible lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="c1514-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
