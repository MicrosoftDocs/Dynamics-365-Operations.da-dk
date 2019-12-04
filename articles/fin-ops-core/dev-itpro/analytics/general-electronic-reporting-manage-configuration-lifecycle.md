---
title: Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)
description: I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Microsoft Dynamics 365 Finance-løsningen.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecaeb80f3cda2ee24533ed263df63cc10c5ffc65
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771090"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="47f24-103">Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="47f24-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47f24-104">I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="47f24-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="47f24-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="47f24-105">Overview</span></span>

<span data-ttu-id="47f24-106">Elektronisk rapportering (ER) er et program, der understøtter lovgivningsmæssigt påkrævede og landespecifikke elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="47f24-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="47f24-107">Generelt forudsætter ER evnen til at udføre følgende opgaver for en enkelt elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="47f24-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="47f24-108">Du kan finde flere oplysninger under [Oversigt over Elektronisk rapportering (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="47f24-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="47f24-109">Designe en skabelon til et elektronisk dokument:</span><span class="sxs-lookup"><span data-stu-id="47f24-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="47f24-110">Identificer de nødvendige datakilder, der kan præsenteres i dokumentet:</span><span class="sxs-lookup"><span data-stu-id="47f24-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="47f24-111">Underliggende data som f.eks. datatabeller, dataenheder og klasser.</span><span class="sxs-lookup"><span data-stu-id="47f24-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="47f24-112">Processpecifikke egenskaber som f.eks. afviklingsdato og -klokkeslæt og tidszone.</span><span class="sxs-lookup"><span data-stu-id="47f24-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="47f24-113">Brugerinputparametre, angivet af slutbrugeren ved kørsel.</span><span class="sxs-lookup"><span data-stu-id="47f24-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="47f24-114">Definer de nødvendige dokumentelementer og deres topologi for at angive et endeligt dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="47f24-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="47f24-115">Konfigurer den ønskede datastrøm fra markerede datakilder til definerede dokumentelementer (via datakildebindinger til dokumentets formatkomponenter), og angiv processtyringslogik.</span><span class="sxs-lookup"><span data-stu-id="47f24-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="47f24-116">Gør en skabelon tilgængelig, så den kan bruges i andre forekomster:</span><span class="sxs-lookup"><span data-stu-id="47f24-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="47f24-117">Transformér en dokumentskabelon, der er oprettet til en ER-konfiguration, og eksportér konfigurationen fra den aktuelle forekomst som en XML-pakke, der kan gemmes lokalt eller i LCS.</span><span class="sxs-lookup"><span data-stu-id="47f24-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="47f24-118">Transformér en ER-konfiguration til en programdokumentskabelon.</span><span class="sxs-lookup"><span data-stu-id="47f24-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="47f24-119">Importér en XML-pakke, der er gemt lokalt eller i LCS, til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="47f24-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="47f24-120">Tilpas skabelonen for et elektronisk dokument:</span><span class="sxs-lookup"><span data-stu-id="47f24-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="47f24-121">Bring en skabelon fra LCS til den aktuelle forekomst som en ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="47f24-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="47f24-122">Design en brugerdefineret version af en ER-konfiguration, og bevar en reference til basisversionen.</span><span class="sxs-lookup"><span data-stu-id="47f24-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="47f24-123">Integrer en skabelon med en bestemt forretningsproces, så den er tilgængelig i programmet:</span><span class="sxs-lookup"><span data-stu-id="47f24-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="47f24-124">Konfigurer indstillinger, så programmet begynder at bruge en ER-konfiguration, ved at referere til denne konfiguration i en procesrelateret parameter.</span><span class="sxs-lookup"><span data-stu-id="47f24-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="47f24-125">Se for eksempel ER-konfigurationen i en bestemt kreditorbetalingsmetode for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="47f24-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="47f24-126">Brug en skabelon i en bestemt forretningsproces:</span><span class="sxs-lookup"><span data-stu-id="47f24-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="47f24-127">Kør en ER-konfiguration i en bestemt forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="47f24-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="47f24-128">For eksempel for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer, når betalingsmåde, der refererer til ER-konfigurationen, er markeret.</span><span class="sxs-lookup"><span data-stu-id="47f24-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="47f24-129">Begreber</span><span class="sxs-lookup"><span data-stu-id="47f24-129">Concepts</span></span>
<span data-ttu-id="47f24-130">Følgende roller og relaterede aktiviteter er tilknyttet ER-konfigurations livscyklus.</span><span class="sxs-lookup"><span data-stu-id="47f24-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="47f24-131">Rolle</span><span class="sxs-lookup"><span data-stu-id="47f24-131">Role</span></span>                                       | <span data-ttu-id="47f24-132">Aktiviteter</span><span class="sxs-lookup"><span data-stu-id="47f24-132">Activities</span></span>                                                      | <span data-ttu-id="47f24-133">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="47f24-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="47f24-134">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="47f24-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="47f24-135">Opret og administrer ER-komponenter (modeller og formater).</span><span class="sxs-lookup"><span data-stu-id="47f24-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="47f24-136">En forretningsmand, som designer ER domæne-specifikke datamodeller, designer de krævede skabeloner til elektroniske dokumenter og binder dem i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="47f24-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="47f24-137">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="47f24-137">Electronic reporting developer</span></span>             | <span data-ttu-id="47f24-138">Opret og administrer datamodeltilknytninger.</span><span class="sxs-lookup"><span data-stu-id="47f24-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="47f24-139">En specialist, der vælger de nødvendige Finance-datakilder og binder dem til ER-domænespecifikke datamodeller.</span><span class="sxs-lookup"><span data-stu-id="47f24-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="47f24-140">Regnskabsansvarlig</span><span class="sxs-lookup"><span data-stu-id="47f24-140">Accounting supervisor</span></span>                      | <span data-ttu-id="47f24-141">Konfigurer procesrelaterede indstillinger, der refererer til ER-artefakter.</span><span class="sxs-lookup"><span data-stu-id="47f24-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="47f24-142">For eksempel rollen **Regnskabsansvarlig**, der gør det muligt, at bruge indstillingerne for en ER-konfiguration i en bestemt kreditorbetalingsmetode til at generere en elektronisk betalingsmeddelelse til behandling af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="47f24-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="47f24-143">Ansvarlig for kreditorbetalinger</span><span class="sxs-lookup"><span data-stu-id="47f24-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="47f24-144">Brug ER-artefakter i en bestemt forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="47f24-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="47f24-145">For eksempel rollen **Ansvarlig for kreditorbetalinger**, der gør det muligt at generere elektroniske betalingsmeddelelser til behandling af fakturaer baseret på det ER-format, som er konfigureret til en specifik betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="47f24-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="47f24-146">Udviklingsfase i ER-konfiguration</span><span class="sxs-lookup"><span data-stu-id="47f24-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="47f24-147">Af følgende ER-relaterede årsager anbefales du at designe ER-konfigurationer i udviklingsmiljøet som en adskilt forekomst af Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="47f24-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="47f24-148">Brugere i rollen som **Udvikler til elektronisk rapportering** eller **Funktionel konsulent i elektronisk rapportering** kan redigere konfigurationer og køre dem til testformål.</span><span class="sxs-lookup"><span data-stu-id="47f24-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="47f24-149">Denne situation kan medføre kald af metoder for klasser og tabeller, der kan være skadelige for virksomhedens data og forekomstens ydeevne.</span><span class="sxs-lookup"><span data-stu-id="47f24-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="47f24-150">Kald af metoder for klasser og tabeller som ER-datakilder til ER-konfigurationer er ikke begrænset af indgangspunkter og logført firmaindhold.</span><span class="sxs-lookup"><span data-stu-id="47f24-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="47f24-151">Derfor kan brugere i rollen **Udvikler til elektronisk rapportering** eller rollen **Funktionel konsulent i elektronisk rapportering** få adgang til forretningsfølsomme data.</span><span class="sxs-lookup"><span data-stu-id="47f24-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="47f24-152">ER-konfigurationer, der designet i udviklingsmiljøet, kan overføres til testmiljøet til konfigurationen af evaluering (korrekt procesintegration, rigtigheden af resultater og ydeevne) og kvalitetssikring som f.eks. rigtigheden af rollebaserede adgangsrettigheder og opdeling af opgaver.</span><span class="sxs-lookup"><span data-stu-id="47f24-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="47f24-153">De funktioner, der aktiverer ER-konfigurationsudvekslingen, kan bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="47f24-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="47f24-154">Endelig kan afprøvede ER-konfigurationer overføres til enten LCS, hvor de kan deles med serviceabonnenter, eller til produktionsmiljøet til intern brug som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="47f24-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![Livscyklus for ER-konfiguration](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="47f24-156">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="47f24-156">Additional resources</span></span>

[<span data-ttu-id="47f24-157">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="47f24-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
