---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (24. september 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e0c1a3bf7613db4887e0943a70ad6262a70997f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460677"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="56244-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (24. september 2018)</span><span class="sxs-lookup"><span data-stu-id="56244-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

<span data-ttu-id="56244-104">**Build 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="56244-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="56244-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="56244-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="56244-106">Valuta er føjet til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="56244-106">Currency added to Benefits</span></span>

<span data-ttu-id="56244-107">Frynsegodsplaner er blevet opdateret for at medtage valutaen for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="56244-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="56244-108">Det nye felt findes også på arbejderens tilmeldte frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="56244-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="56244-109">Det nye felt er en del af sikkerhedsrettigheden Vedligehold frynsegoder og Vis en liste over frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="56244-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="56244-110">Opdateret proportionalitetsproces – Orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="56244-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="56244-111">Organisationer beregner fravær forskelligt afhængigt af, hvornår medarbejdere starter i eller forlader firmaet.</span><span class="sxs-lookup"><span data-stu-id="56244-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="56244-112">Nogle medarbejdere, der forlader organisationen, skal måske afslutte bonus på fratrædelsesdatoen, mens andre bruger den sidste gennemførte arbejdsdag som stop for periodiseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="56244-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="56244-113">Disse ændringer giver organisationer mulighed for at vælge, hvornår de vil afslutte tilmelding under fratrædelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="56244-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="56244-114">De nye muligheder er en del af rettighederne for Opsig en medarbejder og Opsig en arbejder fra selvbetjening for leder.</span><span class="sxs-lookup"><span data-stu-id="56244-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="56244-115">Andre ændringer</span><span class="sxs-lookup"><span data-stu-id="56244-115">Other changes</span></span>

<span data-ttu-id="56244-116">Denne version indeholder flere supplerende fejlrettelser.</span><span class="sxs-lookup"><span data-stu-id="56244-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="56244-117">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="56244-117">Known Issue</span></span>

-   <span data-ttu-id="56244-118">**Problem:** Når du føjer en ny vedhæftet fil til en arbejder, bliver **Ny**- og **Rediger**-knapperne nedtonede. **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukkede.</span><span class="sxs-lookup"><span data-stu-id="56244-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="56244-119">Hvis faktaboksene et lukkede, når siden **Arbejder** indlæses, vil Vedhæftede filer-knapperne blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="56244-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="56244-120">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="56244-120">(This issue will be fixed in the next platform update.)</span></span>
