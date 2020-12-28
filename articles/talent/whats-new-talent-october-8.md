---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (8. oktober 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460692"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="dd326-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (8. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="dd326-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

<span data-ttu-id="dd326-104">**Build 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="dd326-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="dd326-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="dd326-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="dd326-106">Tillade, at andre datoer bruges på niveaugrundlag for orlov (fraværsstyring)</span><span class="sxs-lookup"><span data-stu-id="dd326-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="dd326-107">Når medarbejdere får tildelt orlov, bestemmer bonusniveaugrundlaget, hvor lang tid en medarbejder periodiserer.</span><span class="sxs-lookup"><span data-stu-id="dd326-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="dd326-108">Disse niveauer er i øjeblikket baseret på startdato for medarbejder og anciennitetsdato.</span><span class="sxs-lookup"><span data-stu-id="dd326-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="dd326-109">I visse scenarier har organisationer brug for, at disse niveauer baseres på andre datoer, som jubilæums- eller oprindelig ansættelsesdato.</span><span class="sxs-lookup"><span data-stu-id="dd326-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="dd326-110">Da disse datoer allerede bruges på orlovsplan til at bestemme, hvornår der forekommer periodiseringer, er muligheden for, at de samme datoer bruges, når medarbejderen er tilmeldt en plan, tilføjet for at bestemme periodiseringsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="dd326-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="dd326-111">Andre ændringer</span><span class="sxs-lookup"><span data-stu-id="dd326-111">Other changes</span></span>
<span data-ttu-id="dd326-112">Diverse rettelser er medtaget i denne version.</span><span class="sxs-lookup"><span data-stu-id="dd326-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="dd326-113">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="dd326-113">Known issue</span></span>

<span data-ttu-id="dd326-114">**Problem:** Når du føjer en ny vedhæftet fil til en arbejder, bliver **Ny**- og **Rediger**-knapperne nedtonede. **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukkede.</span><span class="sxs-lookup"><span data-stu-id="dd326-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="dd326-115">Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="dd326-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="dd326-116">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="dd326-116">(This issue will be fixed in the next platform update.)</span></span>
