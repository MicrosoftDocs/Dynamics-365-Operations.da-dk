---
title: Levere Mixed-Reality-vejledninger til arbejdere i produktion
description: Dette emne forklarer, hvordan du kan integrere modulet til produktionsstyring i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 59fe3996013737198d4fbc86d64f8ef9dbe035e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829348"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="11a7b-103">Levere Mixed-Reality-vejledninger til arbejdere i produktion</span><span class="sxs-lookup"><span data-stu-id="11a7b-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="11a7b-104">Arbejdere i produktionsprocesser vil nyde godt af relevante instruktioner, der er tilgængelige på det rette tidspunkt i forbindelse med deres arbejde.</span><span class="sxs-lookup"><span data-stu-id="11a7b-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="11a7b-105">*Instruktioner* gælder i flere arbejdsdomæner, herunder: montage, service, drift, certificering og sikkerhed.</span><span class="sxs-lookup"><span data-stu-id="11a7b-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="11a7b-106">Løbende uddannelsesinstruktioner kan gøre det lettere for medarbejderne at udrette mere og arbejde bedre på tværs af alle disse kernefunktioner i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="11a7b-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="11a7b-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="11a7b-107">Introduction</span></span>

<span data-ttu-id="11a7b-108">Du kan levere instruktioner på forskellige måder.</span><span class="sxs-lookup"><span data-stu-id="11a7b-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="11a7b-109">Et effektivt standardsystem, der bruger [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="11a7b-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="11a7b-110">Dynamics 365 Guides kan hjælpe medarbejderne med praktisk læring.</span><span class="sxs-lookup"><span data-stu-id="11a7b-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="11a7b-111">Du kan definere standardiserede processer med trinvise instruktioner, der fører medarbejderne til de værktøjer og dele, de har brug for, og viser medarbejderne, hvordan disse værktøjer bruges i ægte arbejdssituationer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="11a7b-112">Du kan knytte guider til forskellige aspekter af produktionsstyring, herunder:</span><span class="sxs-lookup"><span data-stu-id="11a7b-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="11a7b-113">Ressourcer</span><span class="sxs-lookup"><span data-stu-id="11a7b-113">Resources</span></span>](#resources)
- [<span data-ttu-id="11a7b-114">Ressourcegrupper</span><span class="sxs-lookup"><span data-stu-id="11a7b-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="11a7b-115">Frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="11a7b-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="11a7b-116">Formler</span><span class="sxs-lookup"><span data-stu-id="11a7b-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="11a7b-117">Formelversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="11a7b-118">Styklister</span><span class="sxs-lookup"><span data-stu-id="11a7b-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="11a7b-119">Styklisteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="11a7b-120">Ruter</span><span class="sxs-lookup"><span data-stu-id="11a7b-120">Routes</span></span>](#routes)
- [<span data-ttu-id="11a7b-121">Ruteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="11a7b-122">Ruteoperationsrelationer</span><span class="sxs-lookup"><span data-stu-id="11a7b-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="11a7b-123">Du kan også tilknytte guider med Aktivstyring.</span><span class="sxs-lookup"><span data-stu-id="11a7b-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="11a7b-124">Du kan finde flere oplysninger under [Integrere Dynamics 365 Supply Chain Management (Aktivstyring) med Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="11a7b-125">Når en medarbejder i forreste linje vælger et job i produktionen via Supply Chain Management, kan arbejderen se [de relevante guider](#logic) på jobkortet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="11a7b-126">Når arbejderen vælger en specifik vejledning, vises en QR-kode for den pågældende vejledning på skærmen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="11a7b-127">Arbejderen bruger derefter sin HoloLens til at scanne QR-koden, der starter vejledninger og viser de nødvendige instruktioner.</span><span class="sxs-lookup"><span data-stu-id="11a7b-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="11a7b-128">Følgende underafsnit beskriver et par udvalgte scenarier, hvor firmaer på tværs af brancher kan se den største værdi, når der bruges vejledninger til at præsentere instruktioner til produktion.</span><span class="sxs-lookup"><span data-stu-id="11a7b-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="11a7b-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="11a7b-129">Assembly</span></span>

<span data-ttu-id="11a7b-130">![Bruge guider i assembly-opgaver](media/instruction-guides-hero-assembly.png "Bruge guider i serviceopgaver")</span><span class="sxs-lookup"><span data-stu-id="11a7b-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="11a7b-131">Instruktionerne i assembly-drift viser arbejdere de værktøjer og dele, de har brug for, og hvordan de bruges i reelle arbejdssituationer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="11a7b-132">Produktionschefer kan oprette og tildele guider, f.eks. til [produktionsruter](routes-operations.md), [operationsrelationer](routes-operations.md#operation-relations) eller [styklister](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="11a7b-133">Arbejdere kan finde de relevante instruktioner om den pågældende operationsoplevelse i produktionen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="11a7b-134">Ydelse</span><span class="sxs-lookup"><span data-stu-id="11a7b-134">Service</span></span>

<span data-ttu-id="11a7b-135">![Bruge guider i serviceopgaver](media/instruction-guides-hero-service.png "Bruge guider i serviceopgaver")</span><span class="sxs-lookup"><span data-stu-id="11a7b-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="11a7b-136">Udstyr teknikere med instruktioner på arbejdspladsen, hvilket eliminerer behovet for at planlægge yderligere besøg.</span><span class="sxs-lookup"><span data-stu-id="11a7b-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="11a7b-137">Servicechefer kan f.eks. tildele guider til bestemte [produkter](../../commerce/product.md), der gennemgår rutinerne for kvalitetsvurdering.</span><span class="sxs-lookup"><span data-stu-id="11a7b-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="11a7b-138">Kvalitet</span><span class="sxs-lookup"><span data-stu-id="11a7b-138">Quality</span></span>

<span data-ttu-id="11a7b-139">![Bruge guider i kvalitetssikringsopgaver](media/instruction-guides-hero-quality.png "Bruge guider i kvalitetssikringsopgaver")</span><span class="sxs-lookup"><span data-stu-id="11a7b-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="11a7b-140">Udrul nye processer for at sikre øget konsistens ved at omdanne medarbejdernes viden til et rutineværktøj.</span><span class="sxs-lookup"><span data-stu-id="11a7b-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="11a7b-141">Kvalitetssikringschefer kan f.eks. tildele guider til [produkter](../../commerce/product.md), der gennemgår rutinerne for kvalitetsvurdering.</span><span class="sxs-lookup"><span data-stu-id="11a7b-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="11a7b-142">Certificeringer</span><span class="sxs-lookup"><span data-stu-id="11a7b-142">Certifications</span></span>

<span data-ttu-id="11a7b-143">![Bruge guider til certificeringsrelaterede opgaver](media/instruction-guides-hero-certification.png "Bruge guider til certificeringsrelaterede opgaver")</span><span class="sxs-lookup"><span data-stu-id="11a7b-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="11a7b-144">Sørg for, at hver medarbejder overholder høje standarder, ved hurtigt at identificere, hvem der har brug for hjælp og hvor.</span><span class="sxs-lookup"><span data-stu-id="11a7b-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="11a7b-145">Sikkerhed</span><span class="sxs-lookup"><span data-stu-id="11a7b-145">Safety</span></span>

<span data-ttu-id="11a7b-146">![Bruge guider til instruktionerne for arbejdssikkerhed](media/instruction-guides-hero-safety.png "Bruge guider til instruktionerne for arbejdssikkerhed")</span><span class="sxs-lookup"><span data-stu-id="11a7b-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="11a7b-147">Udlevér vejledninger, der gennemgår de farlige procedurer virtuelt inden forsøg på at udføre dem i det fysiske miljø.</span><span class="sxs-lookup"><span data-stu-id="11a7b-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="11a7b-148">Med en Mixed Reality-tilgang kan arbejderne opleve farlige procedurer virtuelt.</span><span class="sxs-lookup"><span data-stu-id="11a7b-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="11a7b-149">Produktionschefer kan levere dedikerede håndteringsinstruktioner for farligt materiale eller delikate håndteringsprocedurer ved at tildele instruktioner til [produktvarer](../../commerce/product.md), [ruter](routes-operations.md) og [operationer](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="11a7b-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="11a7b-150">Introduktion til vejledninger og Guides</span><span class="sxs-lookup"><span data-stu-id="11a7b-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="11a7b-151">Hvis du vil aktivere instruktioner i produktionsprocesser, giver Supply Chain Management en standardintegration med Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="11a7b-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="11a7b-152">Der kræves en licenseret og installeret programforekomst af Guides for at opbygge, vedligeholde og tildele Mixed Reality-instruktioner til produktionsaktiver og arbejde.</span><span class="sxs-lookup"><span data-stu-id="11a7b-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="11a7b-153">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="11a7b-153">Prerequisites</span></span>

<span data-ttu-id="11a7b-154">Hvis du vil bruge denne funktion, skal systemet indeholde følgende:</span><span class="sxs-lookup"><span data-stu-id="11a7b-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="11a7b-155">Dynamics 365 Supply Chain Management version 10.0.15 eller nyere</span><span class="sxs-lookup"><span data-stu-id="11a7b-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="11a7b-156">[Dobbeltskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) til Supply Chain Management-apps.</span><span class="sxs-lookup"><span data-stu-id="11a7b-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="11a7b-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 eller nyere</span><span class="sxs-lookup"><span data-stu-id="11a7b-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="11a7b-158">Slå funktionen til</span><span class="sxs-lookup"><span data-stu-id="11a7b-158">Turn on the feature</span></span>

<span data-ttu-id="11a7b-159">Hvis du vil gøre funktionen tilgængelig på systemet, skal du aktivere dens konfigurationsnøgler.</span><span class="sxs-lookup"><span data-stu-id="11a7b-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="11a7b-160">Du behøver kun at gøre dette én gang.</span><span class="sxs-lookup"><span data-stu-id="11a7b-160">You only need to do this once.</span></span> <span data-ttu-id="11a7b-161">For at kunne gøre dette skal en administrator udføre følgende:</span><span class="sxs-lookup"><span data-stu-id="11a7b-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="11a7b-162">Sæt systemet i vedligeholdelsestilstand som beskrevet i [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="11a7b-163">Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="11a7b-164">Udvid afsnittet **Mixed Reality**, og markér derefter afkrydsningsfeltet **Mixed Reality-guide**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="11a7b-165">Udvid afsnittet **Administration af produktion**, og markér derefter afkrydsningsfeltet **Produktionsinstruktioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="11a7b-166">Slå vedligeholdelsestilstand fra som beskrevet i [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="11a7b-167">Konfigurere, hvordan guider vises i produktionen</span><span class="sxs-lookup"><span data-stu-id="11a7b-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="11a7b-168">Hvis du vil konfigurere, hvordan guider vises i produktionen, skal du gå til **Mixed Reality \> Dynamics 365 Guides \> Konfigurer guideintegration**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="11a7b-169">![Konfigurere guideintegration i produktion](media/instruction-guides-configure-integration.png "Konfigurere guideintegration i produktion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="11a7b-170">Angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="11a7b-170">Set the following fields:</span></span>

- <span data-ttu-id="11a7b-171">**Microsoft Dataverse-URL-adresse** - Angiv URL-adressen til det Microsoft Dataverse-miljø, hvor du opretter din Guides.</span><span class="sxs-lookup"><span data-stu-id="11a7b-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="11a7b-172">Formatet er "contoso.crm4.dynamics.com", hvor den første del af URL-adressen typisk er navngivet efter din organisation (f.eks. "contoso."), den anden del er specifik for dit miljøs dataområde (som f.eks. "crm4"), og den sidste del er domænet (f.eks. "dynamics.com").</span><span class="sxs-lookup"><span data-stu-id="11a7b-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="11a7b-173">En måde at finde den rigtige URL-adresse på er at gå til [home.dynamics.com](https://home.dynamics.com/) og derefter åbne din Guides-app.</span><span class="sxs-lookup"><span data-stu-id="11a7b-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="11a7b-174">Når Guides åbnes, kan du se URL-adressen på adresselinjen i din browser (tag kun basis-URL-adressen, som ligner det foregående eksempel).</span><span class="sxs-lookup"><span data-stu-id="11a7b-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="11a7b-175">Denne værdi bruges til at oprette adresser til dine guider og vil blive kodet i QR-koderne."</span><span class="sxs-lookup"><span data-stu-id="11a7b-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="11a7b-176">**QR-kodestørrelse** - Angiv størrelsen på den gengivne QR-kode.</span><span class="sxs-lookup"><span data-stu-id="11a7b-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="11a7b-177">Det anbefales, at du vælger en størrelse, der vil udfylde det meste af din skærm, men ikke mere.</span><span class="sxs-lookup"><span data-stu-id="11a7b-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="11a7b-178">*15* er typisk en god værdi.</span><span class="sxs-lookup"><span data-stu-id="11a7b-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="11a7b-179">**Rettelsesniveau for QR-kodefejl** - Angiv QR-kodens granularitet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="11a7b-180">En højere granularitet kan hjælpe med at øge kodens pålidelighed, men **størrelsen på QR-koden** skal være stor nok til at understøtte det detaljeringsniveau, der kræves af det valgte rettelsesniveau.</span><span class="sxs-lookup"><span data-stu-id="11a7b-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="11a7b-181">QR-kodestørrelser, der er for store til skærmen, tager lidt længere tid at gengive og skal derefter skaleres ned, så de passer til skærmen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="11a7b-182">Disse giver ikke nogen fordel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="11a7b-183">QR-kodestørrelser, der er for små, kan reducere muligheden for HoloLens at læse koden korrekt i visse miljøer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="11a7b-184">Det anbefales, at du tester indstillingerne for de enkelte enheder, der skal vise QR-koder for HoloLens-brugere.</span><span class="sxs-lookup"><span data-stu-id="11a7b-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="11a7b-185">Vælg indstillinger, der giver tilstrækkelig læsbarhed i produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="11a7b-186">Få vist en oversigt over alle guidetildelinger</span><span class="sxs-lookup"><span data-stu-id="11a7b-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="11a7b-187">Du kan bruge siden **Alle guider** til at få vist listen over alle tilgængelige guider i organisationen og alle tildelinger til dine produktionsprocesser og ressourcer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="11a7b-188">Hvis du vil åbne den, skal du gå til **Mixed Reality \> Guider \> Alle guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="11a7b-189">Oversigten øverst viser alle tilgængelige guider, og du kan bruge feltet her til at filtrere listen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="11a7b-190">På listen nederst vises alle guidetildelinger, og der findes en værktøjslinje til styring af dem.</span><span class="sxs-lookup"><span data-stu-id="11a7b-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="11a7b-191">![Administrere guider](media/instruction-guides-allguides.png "Administrere guider")</span><span class="sxs-lookup"><span data-stu-id="11a7b-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="11a7b-192">I følgende afsnit beskrives de objekttyper, du kan tildele guider.</span><span class="sxs-lookup"><span data-stu-id="11a7b-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="11a7b-193">Hver enkelt tildelte guide indeholder instruktioner, der automatisk knyttes til de enkelte produktionsjob og vil være tilgængelige i produktionen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="11a7b-194">Knytte en guide til en ressource</span><span class="sxs-lookup"><span data-stu-id="11a7b-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="11a7b-195">Føj en guide til en [ressource](operations-resources.md) for at tilbyde guiden i forbindelse med de relevante produktionsjob.</span><span class="sxs-lookup"><span data-stu-id="11a7b-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="11a7b-196">Typisk scenarie, der bruger ressourcer</span><span class="sxs-lookup"><span data-stu-id="11a7b-196">Typical scenario using resources</span></span>

<span data-ttu-id="11a7b-197">Du kan f.eks. knytte en guide med generel maskinsikkerhed eller håndteringsoplysninger til en ressource af typen maskine.</span><span class="sxs-lookup"><span data-stu-id="11a7b-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="11a7b-198">Derefter vil guiden være tilgængelig på alle de job, der udføres på maskinen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="11a7b-199">Føje en guide til en ressource</span><span class="sxs-lookup"><span data-stu-id="11a7b-199">Add a Guide to a resource</span></span>

<span data-ttu-id="11a7b-200">Sådan føjer du en guide til en ressource:</span><span class="sxs-lookup"><span data-stu-id="11a7b-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="11a7b-201">Gå til **Produktionsstyring \> Opsætning \> Ressourcer \> Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="11a7b-202">Vælg den ressource, du vil tildele en guide, i listeruden.</span><span class="sxs-lookup"><span data-stu-id="11a7b-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-203">Udvid oversigtspanelet **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="11a7b-204">Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="11a7b-205">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="11a7b-206">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="11a7b-207">Hvis du har et stort antal guider, kan du filtrere listen for at finde den, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="11a7b-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="11a7b-208">![Administrere guider](media/instruction-guides-allguides.png "Administrere guider")</span><span class="sxs-lookup"><span data-stu-id="11a7b-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="11a7b-209">Knytte en guide til en ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="11a7b-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="11a7b-210">Du kan føje en guide til [ressourcegrupper](tasks/define-discrete-manufacturing-resource-group.md), hvis du bruger dem til at administrere grupper af maskiner, produktionslinjer eller arbejdsceller.</span><span class="sxs-lookup"><span data-stu-id="11a7b-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="11a7b-211">Typiske scenarier, der bruger ressourcegrupper</span><span class="sxs-lookup"><span data-stu-id="11a7b-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="11a7b-212">**Eksempel 1:** Du har defineret en ressourcegruppe til flere maskiner af samme model.</span><span class="sxs-lookup"><span data-stu-id="11a7b-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="11a7b-213">I stedet for at tildele den relevante vejledning til håndtering af maskinmodellen til alle relevante ressourcer, kan du i stedet tildele guiden til den ressourcegruppe, der afspejler maskinmodellen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="11a7b-214">**Eksempel 2:** Du har defineret en ressourcegruppe for en arbejdscelle, der indeholder forskellige maskiner, og du har en guide, der giver generelle instruktioner til, hvordan arbejdscellen vedligeholdes.</span><span class="sxs-lookup"><span data-stu-id="11a7b-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="11a7b-215">Guiden gælder for alle produktionsaktiviteter i denne arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="11a7b-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="11a7b-216">Føje en guide til en ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="11a7b-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="11a7b-217">Sådan føjer du en guide til en ressourcegruppe:</span><span class="sxs-lookup"><span data-stu-id="11a7b-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="11a7b-218">Gå til **Produktionsstyring \> Opsætning \> Ressourcer \> Ressourcegrupper**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="11a7b-219">Vælg den ressourcegruppe, du vil tildele en guide, i listeruden.</span><span class="sxs-lookup"><span data-stu-id="11a7b-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-220">Udvid oversigtspanelet **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="11a7b-221">Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="11a7b-222">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="11a7b-223">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="11a7b-224">Hvis du har et stort antal guider, kan du filtrere listen for at finde den, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="11a7b-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="11a7b-225">![Føje en guide til en ressourcegruppe](media/instruction-guides-resourcegroup.png "Føje en guide til en ressourcegruppe")</span><span class="sxs-lookup"><span data-stu-id="11a7b-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="11a7b-226">Knytte en guide til et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="11a7b-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="11a7b-227">Du kan føje en guide til et hvilket som helst [frigivet produkt](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="11a7b-228">Typisk scenarie, der bruger frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="11a7b-228">Typical scenario using released products</span></span>

<span data-ttu-id="11a7b-229">Guider på produktniveau hjælper produktionsarbejdere med instruktioner, der er relevante for driften eller håndteringen af et bestemt frigivet produkt eller en vare.</span><span class="sxs-lookup"><span data-stu-id="11a7b-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="11a7b-230">Føje en guide til et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="11a7b-230">Add a Guide to a released product</span></span>

<span data-ttu-id="11a7b-231">Sådan føjer du en guide til et frigivet produkt:</span><span class="sxs-lookup"><span data-stu-id="11a7b-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="11a7b-232">Gå til **Administration af produktionsoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="11a7b-233">Åbn det produkt, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-234">Åbn fanen **Tekniker** i handlingsruden, og vælg **Tilknyttede guider** i gruppen **Vis**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="11a7b-235">Siden **Tilknyttede guider** åbnes for det valgte produkt.</span><span class="sxs-lookup"><span data-stu-id="11a7b-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="11a7b-236">Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="11a7b-237">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-238">![Føje en guide til et frigivet produkt](media/instruction-guides-ReleasedProduct-AddGuides.png "Føje en guide til et frigivet produkt")</span><span class="sxs-lookup"><span data-stu-id="11a7b-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="11a7b-239">Knytte en guide til en formel</span><span class="sxs-lookup"><span data-stu-id="11a7b-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="11a7b-240">Du kan føje en guide til enhver [formel](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="11a7b-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="11a7b-241">Typisk scenarie, der bruger formler</span><span class="sxs-lookup"><span data-stu-id="11a7b-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="11a7b-242">Guider på formelniveau giver produktionsarbejdere instruktioner i konteksten af en formel eller opskrift.</span><span class="sxs-lookup"><span data-stu-id="11a7b-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="11a7b-243">Guider kan også tildeles versioner af en formel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="11a7b-244">Du kan tildele vejledning, der er relevant for produktionsprocesser, ud fra en formel til en rute-, ruteversions- eller ruteoperationsrelation.</span><span class="sxs-lookup"><span data-stu-id="11a7b-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="11a7b-245">Guider kan i øjeblikket ikke knyttes til individuelle formellinjer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="11a7b-246">Føje en guide til en formel</span><span class="sxs-lookup"><span data-stu-id="11a7b-246">Add a Guide to a formula</span></span>

<span data-ttu-id="11a7b-247">Sådan føjer du en guide til en formel:</span><span class="sxs-lookup"><span data-stu-id="11a7b-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="11a7b-248">Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Formler**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="11a7b-249">Åbn den formel, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-250">Åbn fanen **Overskrift** over det øverste oversigtspanel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="11a7b-251">Udvid oversigtspanelet **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="11a7b-252">Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="11a7b-253">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="11a7b-254">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-255">![Føje en guide til en formel](media/instruction-guides-Formula.png "Føje en guide til en formel")</span><span class="sxs-lookup"><span data-stu-id="11a7b-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="11a7b-256">Knytte en guide til en formelversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="11a7b-257">Du kan føje en guide til enhver [formelversion](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="11a7b-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="11a7b-258">Typisk scenarie, der bruger formelversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="11a7b-259">Guider, der er tilknyttet en enkelt version af en formel, giver produktionsarbejdere vejledning, som gennemgår produktionen af den pågældende version af formelopskriften.</span><span class="sxs-lookup"><span data-stu-id="11a7b-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="11a7b-260">Du kan tildele vejledning, der er relevant for produktionsprocesser, ud fra denne formelversion til en rute-, ruteversions- eller ruteoperationsrelation.</span><span class="sxs-lookup"><span data-stu-id="11a7b-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="11a7b-261">Guider kan i øjeblikket ikke knyttes til individuelle formellinjer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="11a7b-262">Føje en guide til en formelversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="11a7b-263">Sådan føjer du en guide til en formelversion:</span><span class="sxs-lookup"><span data-stu-id="11a7b-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="11a7b-264">Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Formler**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="11a7b-265">Åbn den formel, der indeholder en version, som du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-266">Åbn fanen **Overskrift** over det øverste oversigtspanel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="11a7b-267">Vælg den version, du vil tildele en guide, i oversigtspanelet **Formelversioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-268">Vælg **Tilknyttede guider** på værktøjslinjen **Formelversioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="11a7b-269">![Åbn de guider, der er tilknyttet en valgt formelversion](media/instruction-guides-FormulaVersion.png "Åbne de guider, der er tilknyttet en valgt formelversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="11a7b-270">Siden **Tilknyttede guider** åbnes for din formelversion.</span><span class="sxs-lookup"><span data-stu-id="11a7b-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="11a7b-271">Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="11a7b-272">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-273">![Føje en guide til en formelversion](media/instruction-guides-FormulaVersionAddGuide.png "Føje en guide til en formelversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="11a7b-274">Knytte en guide til en stykliste</span><span class="sxs-lookup"><span data-stu-id="11a7b-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="11a7b-275">Du kan føje en guide til enhver [stykliste](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="11a7b-276">Typisk scenarie, der bruger styklister</span><span class="sxs-lookup"><span data-stu-id="11a7b-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="11a7b-277">Guider, der er tilknyttet en stykliste, giver produktionsarbejdere en vejledning, der forklarer, hvordan materiale forberedes og håndteres fra en stykliste.</span><span class="sxs-lookup"><span data-stu-id="11a7b-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="11a7b-278">Guider kan også tildeles versioner af en stykliste.</span><span class="sxs-lookup"><span data-stu-id="11a7b-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="11a7b-279">Guider kan i øjeblikket ikke knyttes til individuelle styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="11a7b-280">Føje en guide til en stykliste</span><span class="sxs-lookup"><span data-stu-id="11a7b-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="11a7b-281">Sådan føjer du en guide til en stykliste:</span><span class="sxs-lookup"><span data-stu-id="11a7b-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="11a7b-282">Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Styklister**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="11a7b-283">Åbn den stykliste, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-284">Åbn fanen **Overskrift** over det øverste oversigtspanel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="11a7b-285">Udvid oversigtspanelet **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="11a7b-286">Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="11a7b-287">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="11a7b-288">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-289">![Føje en guide til en stykliste](media/instruction-guides-BOM.png "Føje en guide til en stykliste")</span><span class="sxs-lookup"><span data-stu-id="11a7b-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="11a7b-290">Knytte en guide til en styklisteversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="11a7b-291">Du kan føje en guide til enhver [styklisteversion](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="11a7b-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="11a7b-292">Typisk scenarie, der bruger styklisteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="11a7b-293">Guider, der er tilknyttet en individuel styklisteversion, giver produktionsarbejdere en vejledning, der forklarer, hvordan materiale forberedes og håndteres til en version af en stykliste, der er forskellig fra den almindelige stykliste eller andre versioner af den.</span><span class="sxs-lookup"><span data-stu-id="11a7b-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="11a7b-294">Guider kan i øjeblikket ikke knyttes til individuelle styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="11a7b-295">Føje en guide til en styklisteversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="11a7b-296">Sådan føjer du en guide til en styklisteversion:</span><span class="sxs-lookup"><span data-stu-id="11a7b-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="11a7b-297">Gå til **Administration af produktionsoplysninger \> Styklister og formler \> Styklister**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="11a7b-298">Åbn den stykliste, der indeholder en version, som du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-299">Åbn fanen **Overskrift** over det øverste oversigtspanel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="11a7b-300">Vælg den version, du vil tildele en guide, i oversigtspanelet **Styklisteversioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-301">Vælg **Tilknyttede guider** på værktøjslinjen **Styklisteversioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="11a7b-302">![Åbn de guider, der er tilknyttet en valgt styklisteversion](media/instruction-guides-BOMVersion.png "Åbne de guider, der er tilknyttet en valgt styklisteversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="11a7b-303">Siden **Tilknyttede guider** åbnes for din styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="11a7b-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="11a7b-304">Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="11a7b-305">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-306">![Føje en guide til en styklisteversion](media/instruction-guides-BOMVersionAddGuide.png "Føje en guide til en styklisteversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="11a7b-307">Knytte en guide til en rute</span><span class="sxs-lookup"><span data-stu-id="11a7b-307">Associate a Guide to a route</span></span>

<span data-ttu-id="11a7b-308">Du kan føje en guide til enhver [rute](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="11a7b-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="11a7b-309">Typisk scenarie, der bruger ruter</span><span class="sxs-lookup"><span data-stu-id="11a7b-309">Typical scenario using routes</span></span>

<span data-ttu-id="11a7b-310">Ruter bruges typisk til at angive, hvordan et bestemt frigiveret produkt skal produceres på basis af en stykliste eller styklisteversion og med et sæt ressourcer eller ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="11a7b-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="11a7b-311">Tildel en guide en rute for at få trinvise instruktioner til den pågældende produktionsproces.</span><span class="sxs-lookup"><span data-stu-id="11a7b-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="11a7b-312">Føje en guide til en rute</span><span class="sxs-lookup"><span data-stu-id="11a7b-312">Add a Guide to a route</span></span>

<span data-ttu-id="11a7b-313">Sådan føjer du en guide til en rute:</span><span class="sxs-lookup"><span data-stu-id="11a7b-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="11a7b-314">Gå til **Produktionsstyring \> Alle ruter**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="11a7b-315">Åbn den rute, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-316">Udvid oversigtspanelet **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="11a7b-317">Vælg **Tilføj** på værktøjslinjen **Tilknyttede guider**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="11a7b-318">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="11a7b-319">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-320">![Føje en guide til en rute](media/instruction-guides-Route.png "Føje en guide til en rute")</span><span class="sxs-lookup"><span data-stu-id="11a7b-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="11a7b-321">Knytte en guide til en ruteversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="11a7b-322">Du kan føje en guide til enhver [ruteversion](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="11a7b-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="11a7b-323">Typisk scenarie, der bruger ruteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-323">Typical scenario using route versions</span></span>

<span data-ttu-id="11a7b-324">Ruteversioner bruges typisk til at angive varianter af produktionsprocesser baseret på en eksisterende rute.</span><span class="sxs-lookup"><span data-stu-id="11a7b-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="11a7b-325">Du kan tildele forskellige guider til hver ruteversion.</span><span class="sxs-lookup"><span data-stu-id="11a7b-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="11a7b-326">Føje en guide til en ruteversion</span><span class="sxs-lookup"><span data-stu-id="11a7b-326">Add a Guide to a route version</span></span>

<span data-ttu-id="11a7b-327">Sådan føjer du en guide til en ruteversion:</span><span class="sxs-lookup"><span data-stu-id="11a7b-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="11a7b-328">Gå til **Produktionsstyring \> Alle ruter**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="11a7b-329">Åbn den rute, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-330">Vælg den version, du vil tildele en guide, i oversigtspanelet **Versioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-331">Vælg **Tilknyttede guider** på værktøjslinjen **Versioner**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="11a7b-332">![Åbn de guider, der er tilknyttet en valgt ruteversion](media/instruction-guides-RouteVersion.png "Åbne de guider, der er tilknyttet en valgt ruteversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="11a7b-333">Siden **Tilknyttede guider** åbnes for din styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="11a7b-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="11a7b-334">Vælg **Tilføj** i handlingsruden for at føje en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="11a7b-335">For den nye linje skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="11a7b-336">![Føje en guide til en ruteversion](media/instruction-guides-RouteVersionAddGuide.png "Føje en guide til en ruteversion")</span><span class="sxs-lookup"><span data-stu-id="11a7b-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="11a7b-337">Knytte en guide til en ruteoperationsrelation</span><span class="sxs-lookup"><span data-stu-id="11a7b-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="11a7b-338">Du kan føje en guide til enhver [ruteoperationsrelation](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="11a7b-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="11a7b-339">Typisk scenarie, der bruger ruteoperationsrelationer</span><span class="sxs-lookup"><span data-stu-id="11a7b-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="11a7b-340">Operationsrelationer er den mest specifikke måde at føje guider til en produktproces og dens relaterede operationer.</span><span class="sxs-lookup"><span data-stu-id="11a7b-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="11a7b-341">Du kan angive retningslinjer for hver operation i en rute og angive en anden vejledning for alle typer relationskontekster, der er angivet for en rute, f.eks. for bestemte varer, konfigurationer og meget mere.</span><span class="sxs-lookup"><span data-stu-id="11a7b-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="11a7b-342">Du kan også angive, hvilke faser i operationen retningslinjerne skal gælde for (f.eks. opsætning, kø, proces eller transport).</span><span class="sxs-lookup"><span data-stu-id="11a7b-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="11a7b-343">Hvis du angiver guider for flere operationsrelationer for en rute, vil der blandt disse guider kun blive vist guiden fra den mest specifikke relation i produktionen for det oprettede job.</span><span class="sxs-lookup"><span data-stu-id="11a7b-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="11a7b-344">Føje en guide til en ruteoperationsrelation</span><span class="sxs-lookup"><span data-stu-id="11a7b-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="11a7b-345">Sådan føjer du en guide til en ruteoperationsrelation:</span><span class="sxs-lookup"><span data-stu-id="11a7b-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="11a7b-346">Gå til **Produktionsstyring \> Alle ruter**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="11a7b-347">Åbn den rute, du vil tildele en guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="11a7b-348">Åbn fanen **Rute** i handlingsruden, og vælg **Rutedetaljer** i gruppen **Vedligehold**.</span><span class="sxs-lookup"><span data-stu-id="11a7b-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="11a7b-349">Siden **Rutedetaljer** åbnes for den valgte rute.</span><span class="sxs-lookup"><span data-stu-id="11a7b-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="11a7b-350">Vælg den handling, du vil give vejledning til, i det øverste gitter.</span><span class="sxs-lookup"><span data-stu-id="11a7b-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="11a7b-351">Vælg en specifik relation (eller den generiske **All**-relation) i nederste gitter.</span><span class="sxs-lookup"><span data-stu-id="11a7b-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="11a7b-352">![Vælge en operation og derefter en relation](media/instruction-guides-RouteOperationRelation.png "Vælge en operation og derefter en relation")</span><span class="sxs-lookup"><span data-stu-id="11a7b-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="11a7b-353">Åbn fanen **Tilknyttede guider** oven over det nederste gitter. ![Fanen Tilknyttede guider](media/instruction-guides-RouteOperationRelation-AddGuide.png "Fanen Tilknyttede guider")</span><span class="sxs-lookup"><span data-stu-id="11a7b-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="11a7b-354">Vælg **Tilføj** på værktøjslinjen øverst i det nederste gitter for at føje en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="11a7b-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="11a7b-355">For den nye række skal du bruge rullelisten i kolonnen **Navn** til at vælge den guide, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="11a7b-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="11a7b-356">I resten af rækken skal du markere afkrydsningsfeltet for hver kontekst, hvor den valgte guide skal være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="11a7b-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="11a7b-357">Du kan tilføje en eller flere guider for hver fase i hver handling.</span><span class="sxs-lookup"><span data-stu-id="11a7b-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="11a7b-358">Valgte guider fra produktionens udførelsesgrænseflade</span><span class="sxs-lookup"><span data-stu-id="11a7b-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="11a7b-359">Når en arbejder åbner en jobliste i produktionens udførelsesgrænseflade finder Supply Chain Management de relevante guider for de viste job.</span><span class="sxs-lookup"><span data-stu-id="11a7b-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="11a7b-360">Du kan bruge knappen **Guider** til at få vist de relevante guider.</span><span class="sxs-lookup"><span data-stu-id="11a7b-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="11a7b-361">![Knappen Guider i produktionens udførelsesgrænseflade](media/instruction-guides-Shopfloor1.png "Knappen Guider i produktionens udførelsesgrænseflade")</span><span class="sxs-lookup"><span data-stu-id="11a7b-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="11a7b-362">Tag derefter en HoloLens på, og få adgang til den tilhørende guide ved at studere QR-koden og aktivere den respektive guide.</span><span class="sxs-lookup"><span data-stu-id="11a7b-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="11a7b-363">![QR-kode for adgang til guider ved hjælp af en HoloLens](media/instruction-guides-Shopfloor2.png "QR-kode for adgang til guider ved hjælp af en HoloLens")</span><span class="sxs-lookup"><span data-stu-id="11a7b-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="11a7b-364">Fortolkning af logikken for valg af guider</span><span class="sxs-lookup"><span data-stu-id="11a7b-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="11a7b-365">Du kan føje guider til følgende produktionsdata:</span><span class="sxs-lookup"><span data-stu-id="11a7b-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="11a7b-366">Ressourcer</span><span class="sxs-lookup"><span data-stu-id="11a7b-366">Resources</span></span>](#resources)
- [<span data-ttu-id="11a7b-367">Ressourcegrupper</span><span class="sxs-lookup"><span data-stu-id="11a7b-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="11a7b-368">Frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="11a7b-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="11a7b-369">Formler</span><span class="sxs-lookup"><span data-stu-id="11a7b-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="11a7b-370">Formelversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="11a7b-371">Styklister</span><span class="sxs-lookup"><span data-stu-id="11a7b-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="11a7b-372">Styklisteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="11a7b-373">Ruter</span><span class="sxs-lookup"><span data-stu-id="11a7b-373">Routes</span></span>](#routes)
- [<span data-ttu-id="11a7b-374">Ruteversioner</span><span class="sxs-lookup"><span data-stu-id="11a7b-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="11a7b-375">Ruteoperationsrelationer</span><span class="sxs-lookup"><span data-stu-id="11a7b-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="11a7b-376">Når Supply Chain Management genererer jobbene til produktionen, vil det indsamle de relevante guider fra disse kilder.</span><span class="sxs-lookup"><span data-stu-id="11a7b-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="11a7b-377">Bemærk følgende vigtige regler.</span><span class="sxs-lookup"><span data-stu-id="11a7b-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="11a7b-378">Hvis du knytter en styklisteversion eller en formelversion til en rute eller produktionsordre, vises alle de guider, der er tilknyttet denne version, samt de guider, der er knyttet til den overordnede stykliste eller formel af denne version, i jobbet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="11a7b-379">Hvis du knytter en ruteversion til en produktionsordre, vises alle de guider, der er tilknyttet denne version, samt de guider, der er knyttet til den overordnede rute af denne version, i jobbet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="11a7b-380">Hvis du definerer flere ruteoperationsrelationer, der omfatter *Alle*-relationen, og tildeler dem guider, vises kun guiderne fra den mest specifikke relation for jobbet.</span><span class="sxs-lookup"><span data-stu-id="11a7b-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="11a7b-381">![Diagram til fortolkning af relevante guider](media/instruction-guides-Resolve.png "Diagram til fortolkning af relevante guider")</span><span class="sxs-lookup"><span data-stu-id="11a7b-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]