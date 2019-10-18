---
title: Oprette forbindelse til Hjælp-systemet
description: I dette emne beskrives komponenterne i Hjælp-systemet til Finance and Operations-apps, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter brugerdefineret Hjælp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537849"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="b25c8-103">Oprette forbindelse til Hjælp-systemet</span><span class="sxs-lookup"><span data-stu-id="b25c8-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b25c8-104">Dette emne beskriver komponenterne i Hjælp-systemet til Finance and Operations-apps, f.eks. Dynamics 365 Finance Supply Chain Management, Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="b25c8-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="b25c8-105">Det giver et overblik over, hvordan du forbinder disse komponenter, og en oversigt over, hvordan du opretter brugerdefinerede Hjælp.</span><span class="sxs-lookup"><span data-stu-id="b25c8-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="b25c8-106">Hjælp-arkitektur</span><span class="sxs-lookup"><span data-stu-id="b25c8-106">Help architecture</span></span>

<span data-ttu-id="b25c8-107">I følgende illustration vises delene i Hjælp-systemet.</span><span class="sxs-lookup"><span data-stu-id="b25c8-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="b25c8-108">Hjælp-systemet i produkter henter artikler fra https://docs.microsoft.com samt opgaveguides, der er gemt i Forretningsmodeldesigner i LCS (Lifecycle Services).</span><span class="sxs-lookup"><span data-stu-id="b25c8-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="b25c8-109">De funktioner, der vises i diagrammet med en stjerne (\*), er planlagt, men er endnu ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="b25c8-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="b25c8-110">[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="b25c8-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="b25c8-111">Forbindelse til Hjælp-systemet</span><span class="sxs-lookup"><span data-stu-id="b25c8-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="b25c8-112">Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Dynamics 365 Talent eller Retail.</span><span class="sxs-lookup"><span data-stu-id="b25c8-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="b25c8-113">Vi arbejder aktuelt på at aktivere denne funktion i en senere version.</span><span class="sxs-lookup"><span data-stu-id="b25c8-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="b25c8-114">Opgaveguiderne i oplevelsen Introduktion i Talent forbliver tilgængelig og dækker de grundlæggende funktioner.</span><span class="sxs-lookup"><span data-stu-id="b25c8-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="b25c8-115">Automatiseret hjælp er også tilgængelig på docs.microsoft.com-webstedet for både Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="b25c8-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="b25c8-116">På siden **Systemparametre** kan systemadministratorer stykke Hjælp-systemet sammen med henblik på implementering.</span><span class="sxs-lookup"><span data-stu-id="b25c8-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="b25c8-117">[![Formularen Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="b25c8-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="b25c8-118">På siden **Systemparametre** skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="b25c8-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b25c8-119">Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="b25c8-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="b25c8-120">Du skal klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på **OK** for at få adgang til siden **Systemparametre**.</span><span class="sxs-lookup"><span data-stu-id="b25c8-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="b25c8-121">[![Oprette forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Oprette forbindelse til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="b25c8-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="b25c8-122">Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="b25c8-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="b25c8-123">Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="b25c8-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="b25c8-124">Angiv visningsrækkefølgen for BPM-bibliotekerne.</span><span class="sxs-lookup"><span data-stu-id="b25c8-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="b25c8-125">Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="b25c8-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="b25c8-126">Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se de opgaveguider, der gælder for den aktuelle side i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b25c8-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="b25c8-127">Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="b25c8-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="b25c8-128">Visning af oversatte opgaveguider</span><span class="sxs-lookup"><span data-stu-id="b25c8-128">Showing translated task guides</span></span>

<span data-ttu-id="b25c8-129">Oversatte opgaveguider blev introduceret i APQC Unified-biblioteket maj 2016, og introduktionsbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="b25c8-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="b25c8-130">Når du vil se den lokaliserede hjælp til opgaveguider i Finance and Operations-apps, skal du sørge for, at der er forbindelse til maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="b25c8-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="b25c8-131">Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="b25c8-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="b25c8-132">Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i klienten lige nu.</span><span class="sxs-lookup"><span data-stu-id="b25c8-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="b25c8-133">Kun de opgaveguider, der blev udgivet i februar 2016, er tilgængelige i oversatte versioner i maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="b25c8-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="b25c8-134">Vi udsender et opdateret bibliotek med flere oversættelser.</span><span class="sxs-lookup"><span data-stu-id="b25c8-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="b25c8-135">Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="b25c8-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="b25c8-136">Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.</span><span class="sxs-lookup"><span data-stu-id="b25c8-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="b25c8-137">Oprettelse af tilpasset hjælp</span><span class="sxs-lookup"><span data-stu-id="b25c8-137">Creating custom help</span></span>

<span data-ttu-id="b25c8-138">Du kan bruge opgaveguider til at oprette brugerdefineret hjælp eller oprette forbindelse til Hjælp-ruden på et websted.</span><span class="sxs-lookup"><span data-stu-id="b25c8-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="b25c8-139">Oprette tilpasset hjælp til opgaveguider</span><span class="sxs-lookup"><span data-stu-id="b25c8-139">Create custom help with task guides</span></span>

<span data-ttu-id="b25c8-140">Du kan oprette en brugerdefineret hjælp til Finance, Supply Chain Management og til Retail ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem i et bibliotek i en LCS-forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="b25c8-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="b25c8-141">Du kan ikke oprette brugerdefinerede opgaveguider til Talent.</span><span class="sxs-lookup"><span data-stu-id="b25c8-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="b25c8-142">Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder.</span><span class="sxs-lookup"><span data-stu-id="b25c8-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="b25c8-143">Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="b25c8-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="b25c8-144">Du kan finde flere oplysninger under [Sådan opretter du en opgaveregistrering, der skal bruges som dokumentation eller uddannelse](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="b25c8-144">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="b25c8-145">Oprette forbindelse til et brugerdefineret websted</span><span class="sxs-lookup"><span data-stu-id="b25c8-145">Connect a custom site</span></span>

<span data-ttu-id="b25c8-146">Microsoft har udgivet en hvidbog og eksempelkode, der beskriver, hvordan du opretter og tilknytte et brugerdefineret Hjælp-websted til Hjælp-ruden.</span><span class="sxs-lookup"><span data-stu-id="b25c8-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="b25c8-147">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="b25c8-147">For more information, see:</span></span>

- [<span data-ttu-id="b25c8-148">Oprette brugerdefineret Hjælp til Finance and Operations-apps (hvidbog)</span><span class="sxs-lookup"><span data-stu-id="b25c8-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="b25c8-149">Brugerdefineret GitHub-hjælpelager</span><span class="sxs-lookup"><span data-stu-id="b25c8-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="b25c8-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b25c8-150">Additional resources</span></span>

[<span data-ttu-id="b25c8-151">Oversigt over Hjælp</span><span class="sxs-lookup"><span data-stu-id="b25c8-151">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="b25c8-152">Oversigt over Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="b25c8-152">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="b25c8-153">Sådan opretter du en opgaveregistrering, der kan bruges til dokumentation eller undervisning</span><span class="sxs-lookup"><span data-stu-id="b25c8-153">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
