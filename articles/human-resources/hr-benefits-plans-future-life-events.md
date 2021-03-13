---
title: Konfigurere fremtidige livshændelser
description: Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111969"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="adbf2-103">Konfigurere fremtidige livshændelser</span><span class="sxs-lookup"><span data-stu-id="adbf2-103">Configure future life events</span></span>

<span data-ttu-id="adbf2-104">Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="adbf2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="adbf2-105">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fremtidige livshændelser** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="adbf2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="adbf2-106">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="adbf2-106">Select **New**.</span></span>

3. <span data-ttu-id="adbf2-107">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="adbf2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="adbf2-108">Felt</span><span class="sxs-lookup"><span data-stu-id="adbf2-108">Field</span></span> | <span data-ttu-id="adbf2-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="adbf2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="adbf2-110">Dato for livshændelse</span><span class="sxs-lookup"><span data-stu-id="adbf2-110">Life event date</span></span> | <span data-ttu-id="adbf2-111">Systemet behandler alle hændelser under den tilmeldingsperiode, der indtræffer indtil denne dato.</span><span class="sxs-lookup"><span data-stu-id="adbf2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="adbf2-112">Livshændelse logført</span><span class="sxs-lookup"><span data-stu-id="adbf2-112">Life event logged</span></span> | <span data-ttu-id="adbf2-113">Dato og klokkeslæt, hvor livshændelsen blev logført.</span><span class="sxs-lookup"><span data-stu-id="adbf2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="adbf2-114">Logtype</span><span class="sxs-lookup"><span data-stu-id="adbf2-114">Log type</span></span> | <span data-ttu-id="adbf2-115">Viser, om handlingen er en af følgende:</span><span class="sxs-lookup"><span data-stu-id="adbf2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="adbf2-116">- **Opdater** – en ændring af en eksisterende post, der sporer livshændelser</span><span class="sxs-lookup"><span data-stu-id="adbf2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="adbf2-117">- **Indsæt** – oprettelse af en ny livshændelsespost</span><span class="sxs-lookup"><span data-stu-id="adbf2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="adbf2-118">Livshændelsestype-id</span><span class="sxs-lookup"><span data-stu-id="adbf2-118">Life event type ID</span></span> | <span data-ttu-id="adbf2-119">Det entydige id for livshændelsestypen.</span><span class="sxs-lookup"><span data-stu-id="adbf2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="adbf2-120">Livshændelsestype</span><span class="sxs-lookup"><span data-stu-id="adbf2-120">Life event type</span></span> | <span data-ttu-id="adbf2-121">En katalysator til opdatering af en medarbejders tilmelding til frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="adbf2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="adbf2-122">Du kan finde flere oplysninger i afsnittet om udløsning af livshændelser.</span><span class="sxs-lookup"><span data-stu-id="adbf2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="adbf2-123">Status</span><span class="sxs-lookup"><span data-stu-id="adbf2-123">Status</span></span> | <span data-ttu-id="adbf2-124">Angiver, om livshændelsen er behandlet eller ej.</span><span class="sxs-lookup"><span data-stu-id="adbf2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="adbf2-125">Type</span><span class="sxs-lookup"><span data-stu-id="adbf2-125">Line</span></span> | <span data-ttu-id="adbf2-126">Linjenummeret for den fremtidige livshændelse.</span><span class="sxs-lookup"><span data-stu-id="adbf2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="adbf2-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="adbf2-127">Select **Save**.</span></span> 
