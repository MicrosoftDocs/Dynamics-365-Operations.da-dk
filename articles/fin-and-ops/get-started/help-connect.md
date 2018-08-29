---
title: "Forbind hjælpesystemet"
description: "I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Finance and Operations, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter en brugerdefineret Hjælp."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1449d44149f328f780f02e798c5200595557474
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="2caa0-103">Forbind hjælpesystemet</span><span class="sxs-lookup"><span data-stu-id="2caa0-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2caa0-104">Dette emne indeholder beskrivelser af komponenter i Hjælp-systemet til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2caa0-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2caa0-105">Det giver et overblik over, hvordan du forbinder disse komponenter, og en oversigt over, hvordan du opretter brugerdefinerede Hjælp.</span><span class="sxs-lookup"><span data-stu-id="2caa0-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="2caa0-106">Hjælp-arkitektur</span><span class="sxs-lookup"><span data-stu-id="2caa0-106">Help architecture</span></span>
<span data-ttu-id="2caa0-107">I følgende illustration vises de dele, som Finance and Operations Hjælp-systemet består af.</span><span class="sxs-lookup"><span data-stu-id="2caa0-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="2caa0-108">Hjælpesystemet i produkter trækker artikler fra Finance and Operations-webstedet på https://docs.microsoft.com samt opgaveguides, der er gemt i Forretningsmodeldesigner i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2caa0-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="2caa0-109">De funktioner, der vises i diagrammet med en stjerne (\*), er planlagt, men er endnu ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="2caa0-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="2caa0-110">[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="2caa0-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="2caa0-111">Forbindelse til Hjælp-systemet</span><span class="sxs-lookup"><span data-stu-id="2caa0-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="2caa0-112">Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="2caa0-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="2caa0-113">Vi arbejder aktuelt på at aktivere denne funktion i en senere version.</span><span class="sxs-lookup"><span data-stu-id="2caa0-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="2caa0-114">Opgaveguiderne i oplevelsen Introduktion i Talent forbliver tilgængelig og dækker de grundlæggende funktioner.</span><span class="sxs-lookup"><span data-stu-id="2caa0-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="2caa0-115">Automatiseret hjælp er også tilgængelig på webstedet docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for både Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="2caa0-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>


<span data-ttu-id="2caa0-116">På siden **Systemparametre** kan systemadministratorer stykke Hjælp-systemet sammen med henblik på implementering.</span><span class="sxs-lookup"><span data-stu-id="2caa0-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="2caa0-117">[![Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På siden **Systemparametre** skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="2caa0-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2caa0-118">Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="2caa0-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="2caa0-119">Husk at klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på **OK** for at få adgang til siden **Systemparametre**.[![Opret forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Opret forbindelse til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="2caa0-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="2caa0-120">Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="2caa0-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="2caa0-121">Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="2caa0-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="2caa0-122">For Microsoft-indhold i Finance and Operations skal du vælge APQC Unified-biblioteket til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2caa0-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="2caa0-123">For Retail frigiver vi et bibliotek i nærmeste fremtid.</span><span class="sxs-lookup"><span data-stu-id="2caa0-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="2caa0-124">Du behøver ikke at vælge et bibliotek til Talent. Der er oprettet forbindelse til det korrekte bibliotek for dig.</span><span class="sxs-lookup"><span data-stu-id="2caa0-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="2caa0-125">Angiv visningsrækkefølgen for BPM-bibliotekerne.</span><span class="sxs-lookup"><span data-stu-id="2caa0-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="2caa0-126">Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="2caa0-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="2caa0-127">Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2caa0-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="2caa0-128">Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="2caa0-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="2caa0-129">Visning af oversatte opgaveguider</span><span class="sxs-lookup"><span data-stu-id="2caa0-129">Showing translated task guides</span></span>

<span data-ttu-id="2caa0-130">Oversatte opgaveguider blev introduceret i APQC Unified-biblioteket maj 2016, og introduktionsbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="2caa0-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="2caa0-131">Når du vil se den lokaliserede hjælp til opgaveguider i Finance and Operations, skal du sørge for, at der er forbindelse til maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="2caa0-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="2caa0-132">Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2caa0-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2caa0-133">Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i Finance and Operations-klienten lige nu.</span><span class="sxs-lookup"><span data-stu-id="2caa0-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="2caa0-134">Kun de opgaveguider, der blev udgivet i februar 2016, er tilgængelige i oversatte versioner i maj-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="2caa0-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="2caa0-135">Vi udsender et opdateret bibliotek med flere oversættelser.</span><span class="sxs-lookup"><span data-stu-id="2caa0-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="2caa0-136">Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="2caa0-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="2caa0-137">Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.</span><span class="sxs-lookup"><span data-stu-id="2caa0-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="2caa0-138">Oprettelse af tilpasset hjælp</span><span class="sxs-lookup"><span data-stu-id="2caa0-138">Creating custom help</span></span>
<span data-ttu-id="2caa0-139">Du kan oprette en brugerdefineret hjælp til Finance and Operations og til Retail ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem på et bibliotek i LCS Business Proces.</span><span class="sxs-lookup"><span data-stu-id="2caa0-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="2caa0-140">Du kan ikke oprette brugerdefinerede opgaveguider til Talent.</span><span class="sxs-lookup"><span data-stu-id="2caa0-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="2caa0-141">Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder.</span><span class="sxs-lookup"><span data-stu-id="2caa0-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="2caa0-142">Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="2caa0-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="2caa0-143">Du kan finde flere oplysninger under [Sådan opretter du en opgaveregistrering, der skal bruges som dokumentation eller uddannelse](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="2caa0-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="2caa0-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2caa0-144">Additional resources</span></span>
--------

[<span data-ttu-id="2caa0-145">Oversigt over Hjælp</span><span class="sxs-lookup"><span data-stu-id="2caa0-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="2caa0-146">Oversigt over Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="2caa0-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="2caa0-147">Sådan opretter du en opgaveregistrering, der kan bruges til dokumentation eller undervisning</span><span class="sxs-lookup"><span data-stu-id="2caa0-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





