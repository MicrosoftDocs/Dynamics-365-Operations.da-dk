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
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175102"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="66d94-103">Fjernede eller udfasede funktioner i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="66d94-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66d94-104">Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="66d94-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="66d94-105">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="66d94-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="66d94-106">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="66d94-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="66d94-107">Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="66d94-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="66d94-108">Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="66d94-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="66d94-109">Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="66d94-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="66d94-110">Fjernede eller udfasede funktioner i Finance 10.0.12 udgaven</span><span class="sxs-lookup"><span data-stu-id="66d94-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="66d94-111">Polske SSRS-rapporter: registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister– funktionsreference PL-00014</span><span class="sxs-lookup"><span data-stu-id="66d94-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="66d94-112">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="66d94-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="66d94-113">Ikke juridisk krævet.</span><span class="sxs-lookup"><span data-stu-id="66d94-113">Not legally required.</span></span>  |
| <span data-ttu-id="66d94-114">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="66d94-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="66d94-115">Ja (Excel-format til standardrevisionsfil med momsopgørelse – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="66d94-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="66d94-116">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="66d94-116">**Product areas affected**</span></span>         | <span data-ttu-id="66d94-117">Applikation</span><span class="sxs-lookup"><span data-stu-id="66d94-117">Application</span></span> |
| <span data-ttu-id="66d94-118">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="66d94-118">**Deployment option**</span></span>              | <span data-ttu-id="66d94-119">Alt</span><span class="sxs-lookup"><span data-stu-id="66d94-119">All</span></span> |
| <span data-ttu-id="66d94-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="66d94-120">**Status**</span></span>                         | <span data-ttu-id="66d94-121">Udfases: Fra og med d. 1. juli 2021 planlægger vi ikke længere at understøtte SSRS-rapporter: **Registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister – funktionsreference PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="66d94-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="66d94-122">Eksempel i Excel-format til standardrevisionsfil med momsopgørelse (JPK_VDEK) vil blive introduceret i stedet.</span><span class="sxs-lookup"><span data-stu-id="66d94-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="66d94-123">Fjernede eller udfasede funktioner i Finance 10.0.11 udgaven</span><span class="sxs-lookup"><span data-stu-id="66d94-123">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="66d94-124">Norske standardhovedkonti</span><span class="sxs-lookup"><span data-stu-id="66d94-124">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="66d94-125">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="66d94-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="66d94-126">Omdesign</span><span class="sxs-lookup"><span data-stu-id="66d94-126">Redesign</span></span>  |
| <span data-ttu-id="66d94-127">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="66d94-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="66d94-128">Ja (erstattet af programspecifikke parametre for ER-format)</span><span class="sxs-lookup"><span data-stu-id="66d94-128">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="66d94-129">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="66d94-129">**Product areas affected**</span></span>         | <span data-ttu-id="66d94-130">Applikation</span><span class="sxs-lookup"><span data-stu-id="66d94-130">Application</span></span> |
| <span data-ttu-id="66d94-131">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="66d94-131">**Deployment option**</span></span>              | <span data-ttu-id="66d94-132">Alt</span><span class="sxs-lookup"><span data-stu-id="66d94-132">All</span></span> |
| <span data-ttu-id="66d94-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="66d94-133">**Status**</span></span>                         | <span data-ttu-id="66d94-134">Udfases: Fra og med d. 1. april 2021 planlægger vi ikke længere at understøtte funktionalitet, der er relateret til standardhovedkonti: Referencefelt, relateret tabel, dataobjekt.</span><span class="sxs-lookup"><span data-stu-id="66d94-134">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="66d94-135">Fjernede eller udfasede funktioner i Finance 10.0.7 udgaven</span><span class="sxs-lookup"><span data-stu-id="66d94-135">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="66d94-136">Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg</span><span class="sxs-lookup"><span data-stu-id="66d94-136">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="66d94-137">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="66d94-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="66d94-138">Ændret til funktionen med valg af kontogrupper.</span><span class="sxs-lookup"><span data-stu-id="66d94-138">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="66d94-139">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="66d94-139">**Replaced by another feature?**</span></span>   | <span data-ttu-id="66d94-140">Ja</span><span class="sxs-lookup"><span data-stu-id="66d94-140">Yes</span></span> |
| <span data-ttu-id="66d94-141">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="66d94-141">**Product areas affected**</span></span>         | <span data-ttu-id="66d94-142">Arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="66d94-142">Workflow</span></span> |
| <span data-ttu-id="66d94-143">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="66d94-143">**Deployment option**</span></span>              | <span data-ttu-id="66d94-144">Alt</span><span class="sxs-lookup"><span data-stu-id="66d94-144">All</span></span> |
| <span data-ttu-id="66d94-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="66d94-145">**Status**</span></span>                         | <span data-ttu-id="66d94-146">Frarådes: Pr. 1. december 2020 planlægger vi ikke længere at understøtte opsætning af kinesiske bilagstyper uden valg af kontogrupper.</span><span class="sxs-lookup"><span data-stu-id="66d94-146">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="66d94-147">Få flere oplysninger om den nye design i [Nyheder i 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="66d94-147">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="66d94-148">Tidligere meddelelser om fjernede eller udfasede funktioner</span><span class="sxs-lookup"><span data-stu-id="66d94-148">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="66d94-149">Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="66d94-149">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
