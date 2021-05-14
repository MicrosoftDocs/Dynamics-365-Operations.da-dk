---
title: Aktivere styring af kvalitet og uoverensstemmelse
description: Dette emne indeholder en oversigt over processen for opsætning og konfiguration af funktioner til kvalitets- og uoverensstemmelsesstyring i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956248"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="77816-103">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="77816-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77816-104">Dette emne indeholder en oversigt over processen for opsætning og konfiguration af funktioner til kvalitets- og uoverensstemmelsesstyring i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="77816-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="77816-105">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="77816-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="77816-106">Benyt denne fremgangsmåde for at aktivere kvalitetsstyring på systemet.</span><span class="sxs-lookup"><span data-stu-id="77816-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="77816-107">Gå til **Lagerstyring \> Opsætning \> Parametre til lager- og lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="77816-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="77816-108">Angiv indstillingen **Brug kvalitetsstyring** til *Ja* under fanen **Kvalitetsstyring**.</span><span class="sxs-lookup"><span data-stu-id="77816-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="77816-109">Brug feltet **Timepris** til at angive en timepris for arbejde i den lokale valuta.</span><span class="sxs-lookup"><span data-stu-id="77816-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="77816-110">Timeprisen bruges til at beregne omkostningerne for operationer, der vedrører en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="77816-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="77816-111">Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="77816-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="77816-112">De agerer ikke sammen med andre funktioner.</span><span class="sxs-lookup"><span data-stu-id="77816-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="77816-113">Vælg **Rapportopsætning**.</span><span class="sxs-lookup"><span data-stu-id="77816-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="77816-114">Tilføj nye linjer for de forskellige rapporttyper, og vælg den dokumenttype, der skal bruges til hver rapport.</span><span class="sxs-lookup"><span data-stu-id="77816-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="77816-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77816-115">Close the page.</span></span>
1. <span data-ttu-id="77816-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77816-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="77816-117">Konfigurationsproces for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="77816-117">Quality management configuration process</span></span>

<span data-ttu-id="77816-118">Før du kan begynde at bruge funktioner til kvalitetsstyring og generere kvalitetsordrer, skal du konfigurere systemet og forudsætningerne.</span><span class="sxs-lookup"><span data-stu-id="77816-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="77816-119">Her er en liste over de trin, der kræves for at konfigurere kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="77816-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="77816-120">[Aktivere styring af kvalitet og uoverensstemmelse](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="77816-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="77816-121">Valgfrit: [Konfigurer testinstrumenter](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="77816-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="77816-122">[Konfigurere test](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="77816-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="77816-123">[Konfigurer testvariabler og -udfald](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="77816-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="77816-124">[Konfigurere testgrupper](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="77816-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="77816-125">Valgfrit: [Konfigurer kvalitetsgrupper, og link til produkter](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="77816-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="77816-126">Valgfrit: [Konfigurer kvalitetstilknytninger](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="77816-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="77816-127">Når konfigurationen er fuldført, kan du begynde at oprette og behandle kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="77816-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="77816-128">Du kan finde flere oplysninger om, hvordan du opretter og arbejder med kvalitetsordrer i [Kvalitetsordrer](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="77816-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="77816-129">Konfigurationsproces for styring af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="77816-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="77816-130">Før du kan begynde at bruge funktioner til styring af uoverenstemmelser og generere uoverensstemmelser, skal du konfigurere systemet og forudsætningerne.</span><span class="sxs-lookup"><span data-stu-id="77816-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="77816-131">Her er en liste over de trin, der kræves for at konfigurere styring af uoverenstemmelser.</span><span class="sxs-lookup"><span data-stu-id="77816-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="77816-132">[Aktivere styring af kvalitet og uoverensstemmelse](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="77816-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="77816-133">[Konfigurer arbejdere, der er ansvarlige for at godkende uoverensstemmelser](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="77816-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="77816-134">[Konfigurer problemtyper](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="77816-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="77816-135">[Konfigurer karantænezoner](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="77816-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="77816-136">[Konfigurer diagnosticeringstyper](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="77816-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="77816-137">[Konfigurer operationer](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="77816-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="77816-138">Valgfrit: [Konfigurer kvalitetsgebyrer](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="77816-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="77816-139">Når konfigurationen er fuldført, kan du begynde at oprette og behandle uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="77816-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="77816-140">Du kan finde flere oplysninger om, hvordan du opretter og arbejder med uoverensstemmelser i [Oprette og behandle uoverensstemmelser](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="77816-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77816-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="77816-141">Additional resources</span></span>

- [<span data-ttu-id="77816-142">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="77816-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="77816-143">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="77816-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="77816-144">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="77816-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
