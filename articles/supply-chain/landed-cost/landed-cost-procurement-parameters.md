---
title: Indkøbs- og forsyningsparametre for Landingsomkostninger
description: Dette emne beskriver, hvordan de relevante indkøbs- og forsyningsparametre defineres, når du bruger modulet Landingsomkostninger.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833923"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="b18a1-103">Indkøbs- og forsyningsparametre for Landingsomkostninger</span><span class="sxs-lookup"><span data-stu-id="b18a1-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b18a1-104">Siden **Indkøbs- og forsyningsparametre** indeholder nogle få indstillinger, der især er relevante, når du bruger modulet **Landingsomkostninger**.</span><span class="sxs-lookup"><span data-stu-id="b18a1-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="b18a1-105">Brug dialogboksen **Opdater ordrelinjer**, der åbnes fra siden **Indkøbs- og forsyningsparametre**, til at angive, om indkøbsordrelinjer skal opdateres automatisk, når der foretages ændringer i indkøbsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="b18a1-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="b18a1-106">Gør følgende for at fuldføre konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b18a1-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="b18a1-107">Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.</span><span class="sxs-lookup"><span data-stu-id="b18a1-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="b18a1-108">Vælg linket **Opdater ordrelinjer** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="b18a1-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="b18a1-109">I dialogboksen **Opdater ordrelinjer** vises de felter i ordrehovedet, som også kan anvende automatiske opdateringer på de tilknyttede felter på ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="b18a1-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="b18a1-110">Indstil hvert felt på listen til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b18a1-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="b18a1-111">**Altid** – Ordrelinjerne opdateres automatisk, når ordrehovedet opdateres.</span><span class="sxs-lookup"><span data-stu-id="b18a1-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b18a1-112">**Aldrig** – Ordrelinjerne opdateres aldrig, når ordrehovedet opdateres.</span><span class="sxs-lookup"><span data-stu-id="b18a1-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b18a1-113">**Prompt** – Brugeren bliver bedt om at vælge, om ordrelinjerne skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="b18a1-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
