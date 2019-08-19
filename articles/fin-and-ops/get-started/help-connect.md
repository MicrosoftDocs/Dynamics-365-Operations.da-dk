---
title: Oprette forbindelse til Hjælp-systemet
description: I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Finance and Operations, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter en brugerdefineret Hjælp.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
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
ms.openlocfilehash: 929e453987c6e2773d1886d03a4393a68033566b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850895"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="984c2-103">Oprette forbindelse til Hjælp-systemet</span><span class="sxs-lookup"><span data-stu-id="984c2-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="984c2-104">I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="984c2-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="984c2-105">Det giver et overblik over, hvordan du forbinder disse komponenter, og en oversigt over, hvordan du opretter brugerdefinerede Hjælp.</span><span class="sxs-lookup"><span data-stu-id="984c2-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="984c2-106">Hjælp-arkitektur</span><span class="sxs-lookup"><span data-stu-id="984c2-106">Help architecture</span></span>

<span data-ttu-id="984c2-107">I følgende illustration vises de dele, som Finance and Operations Hjælp-systemet består af.</span><span class="sxs-lookup"><span data-stu-id="984c2-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="984c2-108">Hjælpesystemet i produkter trækker artikler fra Finance and Operations-webstedet på https://docs.microsoft.com samt opgaveguides, der er gemt i Forretningsmodeldesigner i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="984c2-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="984c2-109">De funktioner, der vises i diagrammet med en stjerne (\*), er planlagt, men er endnu ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="984c2-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="984c2-110">[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="984c2-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="984c2-111">Forbindelse til Hjælp-systemet</span><span class="sxs-lookup"><span data-stu-id="984c2-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="984c2-112">Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="984c2-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="984c2-113">Vi arbejder aktuelt på at aktivere denne funktion i en senere version.</span><span class="sxs-lookup"><span data-stu-id="984c2-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="984c2-114">Opgaveguiderne i oplevelsen Introduktion i Talent forbliver tilgængelig og dækker de grundlæggende funktioner.</span><span class="sxs-lookup"><span data-stu-id="984c2-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="984c2-115">Automatiseret hjælp er også tilgængelig på webstedet docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for både Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="984c2-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="984c2-116">På siden **Systemparametre** kan systemadministratorer stykke Hjælp-systemet sammen med henblik på implementering.</span><span class="sxs-lookup"><span data-stu-id="984c2-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="984c2-117">[![Formularen Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="984c2-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="984c2-118">På siden **Systemparametre** skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="984c2-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="984c2-119">Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="984c2-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="984c2-120">Du skal klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på **OK** for at få adgang til siden **Systemparametre**.</span><span class="sxs-lookup"><span data-stu-id="984c2-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="984c2-121">[![Oprette forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Oprette forbindelse til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="984c2-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="984c2-122">Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="984c2-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="984c2-123">Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="984c2-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="984c2-124">For Microsoft-indhold i Finance and Operations skal du vælge APQC Unified-biblioteket til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="984c2-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="984c2-125">For Retail frigiver vi et bibliotek i nærmeste fremtid.</span><span class="sxs-lookup"><span data-stu-id="984c2-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="984c2-126">Du behøver ikke at vælge et bibliotek til Talent. Der er oprettet forbindelse til det korrekte bibliotek for dig.</span><span class="sxs-lookup"><span data-stu-id="984c2-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="984c2-127">Angiv visningsrækkefølgen for BPM-bibliotekerne.</span><span class="sxs-lookup"><span data-stu-id="984c2-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="984c2-128">Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="984c2-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="984c2-129">Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="984c2-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="984c2-130">Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="984c2-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="984c2-131">Visning af oversatte opgaveguider</span><span class="sxs-lookup"><span data-stu-id="984c2-131">Showing translated task guides</span></span>

<span data-ttu-id="984c2-132">Oversatte opgaveguider blev introduceret i APQC Unified-biblioteket maj 2016, og introduktionsbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="984c2-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="984c2-133">Når du vil se den lokaliserede hjælp til opgaveguider i Finance and Operations, skal du sørge for, at der er forbindelse til maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="984c2-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="984c2-134">Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="984c2-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="984c2-135">Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i Finance and Operations-klienten lige nu.</span><span class="sxs-lookup"><span data-stu-id="984c2-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="984c2-136">Kun de opgaveguider, der blev udgivet i februar 2016, er tilgængelige i oversatte versioner i maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="984c2-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="984c2-137">Vi udsender et opdateret bibliotek med flere oversættelser.</span><span class="sxs-lookup"><span data-stu-id="984c2-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="984c2-138">Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="984c2-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="984c2-139">Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.</span><span class="sxs-lookup"><span data-stu-id="984c2-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="984c2-140">Oprettelse af tilpasset hjælp</span><span class="sxs-lookup"><span data-stu-id="984c2-140">Creating custom help</span></span>

<span data-ttu-id="984c2-141">Du kan bruge opgaveguider til at oprette brugerdefineret hjælp eller oprette forbindelse til Hjælp-ruden på et websted.</span><span class="sxs-lookup"><span data-stu-id="984c2-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="984c2-142">Oprette tilpasset hjælp til opgaveguider</span><span class="sxs-lookup"><span data-stu-id="984c2-142">Create custom help with task guides</span></span>

<span data-ttu-id="984c2-143">Du kan oprette en brugerdefineret hjælp til Finance and Operations og til Retail ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem på et bibliotek i LCS Business Proces.</span><span class="sxs-lookup"><span data-stu-id="984c2-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="984c2-144">Du kan ikke oprette brugerdefinerede opgaveguider til Talent.</span><span class="sxs-lookup"><span data-stu-id="984c2-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="984c2-145">Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder.</span><span class="sxs-lookup"><span data-stu-id="984c2-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="984c2-146">Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="984c2-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="984c2-147">Du kan finde flere oplysninger under [Sådan opretter du en opgaveregistrering, der skal bruges som dokumentation eller uddannelse](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="984c2-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="984c2-148">Oprette forbindelse til et brugerdefineret websted</span><span class="sxs-lookup"><span data-stu-id="984c2-148">Connect a custom site</span></span>

<span data-ttu-id="984c2-149">Microsoft har udgivet en hvidbog og eksempelkode, der beskriver, hvordan du opretter og tilknytte et brugerdefineret Hjælp-websted til Hjælp-ruden.</span><span class="sxs-lookup"><span data-stu-id="984c2-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="984c2-150">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="984c2-150">For more information, see:</span></span>

- [<span data-ttu-id="984c2-151">Oprette brugerdefineret Hjælp til Finance and Operations (hvidbog)</span><span class="sxs-lookup"><span data-stu-id="984c2-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="984c2-152">Brugerdefineret GitHub-hjælpelager</span><span class="sxs-lookup"><span data-stu-id="984c2-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="984c2-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="984c2-153">Additional resources</span></span>

[<span data-ttu-id="984c2-154">Oversigt over Hjælp</span><span class="sxs-lookup"><span data-stu-id="984c2-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="984c2-155">Oversigt over Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="984c2-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="984c2-156">Sådan opretter du en opgaveregistrering, der kan bruges til dokumentation eller undervisning</span><span class="sxs-lookup"><span data-stu-id="984c2-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
