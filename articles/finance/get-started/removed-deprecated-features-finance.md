---
title: Fjernede eller udfasede funktioner i Dynamics 365 Finance
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127971"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="9b90f-103">Fjernede eller udfasede funktioner i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9b90f-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b90f-104">Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9b90f-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="9b90f-105">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="9b90f-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="9b90f-106">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="9b90f-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="9b90f-107">Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="9b90f-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="9b90f-108">Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="9b90f-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="9b90f-109">Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="9b90f-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="9b90f-110">Fjernede eller udfasede funktioner i Finance 10.0.12 udgaven</span><span class="sxs-lookup"><span data-stu-id="9b90f-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="9b90f-111">Polske SSRS-rapporter: registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister– funktionsreference PL-00014</span><span class="sxs-lookup"><span data-stu-id="9b90f-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="9b90f-112">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="9b90f-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9b90f-113">Ikke juridisk krævet.</span><span class="sxs-lookup"><span data-stu-id="9b90f-113">Not legally required.</span></span>  |
| <span data-ttu-id="9b90f-114">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="9b90f-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9b90f-115">Ja (Excel-format til standardrevisionsfil med momsopgørelse – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="9b90f-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="9b90f-116">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="9b90f-116">**Product areas affected**</span></span>         | <span data-ttu-id="9b90f-117">Applikation</span><span class="sxs-lookup"><span data-stu-id="9b90f-117">Application</span></span> |
| <span data-ttu-id="9b90f-118">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="9b90f-118">**Deployment option**</span></span>              | <span data-ttu-id="9b90f-119">Alt</span><span class="sxs-lookup"><span data-stu-id="9b90f-119">All</span></span> |
| <span data-ttu-id="9b90f-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b90f-120">**Status**</span></span>                         | <span data-ttu-id="9b90f-121">Udfases: Fra og med d. 1. juli 2021 planlægger vi ikke længere at understøtte SSRS-rapporter: **Registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister – funktionsreference PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="9b90f-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="9b90f-122">Eksempel i Excel-format til standardrevisionsfil med momsopgørelse (JPK_VDEK) vil blive introduceret i stedet.</span><span class="sxs-lookup"><span data-stu-id="9b90f-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="9b90f-123">Fjernede eller udfasede funktioner i Finance 10.0.7 udgaven</span><span class="sxs-lookup"><span data-stu-id="9b90f-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="9b90f-124">Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg</span><span class="sxs-lookup"><span data-stu-id="9b90f-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9b90f-125">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="9b90f-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9b90f-126">Ændret til funktionen med valg af kontogrupper.</span><span class="sxs-lookup"><span data-stu-id="9b90f-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="9b90f-127">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="9b90f-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9b90f-128">Ja</span><span class="sxs-lookup"><span data-stu-id="9b90f-128">Yes</span></span> |
| <span data-ttu-id="9b90f-129">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="9b90f-129">**Product areas affected**</span></span>         | <span data-ttu-id="9b90f-130">Arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="9b90f-130">Workflow</span></span> |
| <span data-ttu-id="9b90f-131">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="9b90f-131">**Deployment option**</span></span>              | <span data-ttu-id="9b90f-132">Alt</span><span class="sxs-lookup"><span data-stu-id="9b90f-132">All</span></span> |
| <span data-ttu-id="9b90f-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b90f-133">**Status**</span></span>                         | <span data-ttu-id="9b90f-134">Frarådes: Pr. 1. december 2020 planlægger vi ikke længere at understøtte opsætning af kinesiske bilagstyper uden valg af kontogrupper.</span><span class="sxs-lookup"><span data-stu-id="9b90f-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="9b90f-135">Få flere oplysninger om den nye design i [Nyheder i 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="9b90f-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="9b90f-136">Tidligere meddelelser om fjernede eller udfasede funktioner</span><span class="sxs-lookup"><span data-stu-id="9b90f-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="9b90f-137">Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="9b90f-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
