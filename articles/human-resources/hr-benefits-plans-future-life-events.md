---
title: Konfigurere fremtidige livshændelser
description: Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008501"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="41ebd-103">Konfigurere fremtidige livshændelser</span><span class="sxs-lookup"><span data-stu-id="41ebd-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="41ebd-104">Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="41ebd-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="41ebd-105">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fremtidige livshændelser** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="41ebd-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="41ebd-106">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="41ebd-106">Select **New**.</span></span>

3. <span data-ttu-id="41ebd-107">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="41ebd-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="41ebd-108">Felt</span><span class="sxs-lookup"><span data-stu-id="41ebd-108">Field</span></span> | <span data-ttu-id="41ebd-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="41ebd-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41ebd-110">Dato for livshændelse</span><span class="sxs-lookup"><span data-stu-id="41ebd-110">Life event date</span></span> | <span data-ttu-id="41ebd-111">Systemet behandler alle hændelser under den tilmeldingsperiode, der indtræffer indtil denne dato.</span><span class="sxs-lookup"><span data-stu-id="41ebd-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="41ebd-112">Livshændelse logført</span><span class="sxs-lookup"><span data-stu-id="41ebd-112">Life event logged</span></span> | <span data-ttu-id="41ebd-113">Dato og klokkeslæt, hvor livshændelsen blev logført.</span><span class="sxs-lookup"><span data-stu-id="41ebd-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="41ebd-114">Logtype</span><span class="sxs-lookup"><span data-stu-id="41ebd-114">Log type</span></span> | <span data-ttu-id="41ebd-115">Viser, om handlingen er en af følgende:</span><span class="sxs-lookup"><span data-stu-id="41ebd-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="41ebd-116">- **Opdater** – en ændring af en eksisterende post, der sporer livshændelser</span><span class="sxs-lookup"><span data-stu-id="41ebd-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="41ebd-117">- **Indsæt** – oprettelse af en ny livshændelsespost</span><span class="sxs-lookup"><span data-stu-id="41ebd-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="41ebd-118">Livshændelsestype-id</span><span class="sxs-lookup"><span data-stu-id="41ebd-118">Life event type ID</span></span> | <span data-ttu-id="41ebd-119">Det entydige id for livshændelsestypen.</span><span class="sxs-lookup"><span data-stu-id="41ebd-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="41ebd-120">Livshændelsestype</span><span class="sxs-lookup"><span data-stu-id="41ebd-120">Life event type</span></span> | <span data-ttu-id="41ebd-121">En katalysator til opdatering af en medarbejders tilmelding til frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="41ebd-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="41ebd-122">Du kan finde flere oplysninger i afsnittet om udløsning af livshændelser.</span><span class="sxs-lookup"><span data-stu-id="41ebd-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="41ebd-123">Status</span><span class="sxs-lookup"><span data-stu-id="41ebd-123">Status</span></span> | <span data-ttu-id="41ebd-124">Angiver, om livshændelsen er behandlet eller ej.</span><span class="sxs-lookup"><span data-stu-id="41ebd-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="41ebd-125">Type</span><span class="sxs-lookup"><span data-stu-id="41ebd-125">Line</span></span> | <span data-ttu-id="41ebd-126">Linjenummeret for den fremtidige livshændelse.</span><span class="sxs-lookup"><span data-stu-id="41ebd-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="41ebd-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="41ebd-127">Select **Save**.</span></span> 
