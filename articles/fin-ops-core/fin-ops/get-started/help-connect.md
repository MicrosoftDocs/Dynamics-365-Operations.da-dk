---
title: Konfigurere hjælp-oplevelsen for Finance and Operations-apps
description: Dette emne giver oplysninger om komponenterne i Hjælp-system til nogle Microsoft Dynamics 365-apps. Det forklarer også, hvordan disse apps tilknyttes, og indeholder en oversigt over den proces, der bruges til at oprette brugerdefineret hjælp.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 467cce5a80dc7577647e82c8652c8a7adc67a498
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565922"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="513cd-104">Konfigurere hjælp-oplevelsen for Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="513cd-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="513cd-105">I dette emne kan du finde en oversigt over komponenterne i Hjælp-systemet til Finance and Operations-apps, f.eks. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="513cd-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="513cd-106">Dette emner forklarer også, hvordan disse komponenter tilknyttes, og indeholder en oversigt over den proces, der bruges til at oprette brugerdefineret hjælp.</span><span class="sxs-lookup"><span data-stu-id="513cd-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="513cd-107">Hjælp-arkitektur</span><span class="sxs-lookup"><span data-stu-id="513cd-107">Help architecture</span></span>

<span data-ttu-id="513cd-108">Finance and Operations-apps omfatter konceptbaserede oversigter og andre emner, der er udgivet på [https://docs.microsoft.com/dynamics365](/dynamics365/)-webstedet.</span><span class="sxs-lookup"><span data-stu-id="513cd-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="513cd-109">Du kan derefter få adgang til dette indhold fra ruden **Hjælp** i produktet.</span><span class="sxs-lookup"><span data-stu-id="513cd-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="513cd-110">I følgende illustration vises delene i Hjælp-systemet.</span><span class="sxs-lookup"><span data-stu-id="513cd-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="513cd-111">[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="513cd-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="513cd-112">Hjælp-systemet i produktet henter artikler fra docs.microsoft.com og andre tilknyttede websteder.</span><span class="sxs-lookup"><span data-stu-id="513cd-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="513cd-113">Det henter også opgavevejledninger, der er gemt i BPM (Business process modeler) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="513cd-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="513cd-114">Tilføje opgaveguider</span><span class="sxs-lookup"><span data-stu-id="513cd-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="513cd-115">Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Human Resources eller Commerce.</span><span class="sxs-lookup"><span data-stu-id="513cd-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="513cd-116">Opgaveguiderne i oplevelsen Introduktion i Personale forbliver imidlertid tilgængelige og dækker de grundlæggende funktioner.</span><span class="sxs-lookup"><span data-stu-id="513cd-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="513cd-117">For både Human Resources og Commerce gælder det, at hjælp til procedurer er tilgængelig på [https://docs.microsoft.com/dynamics365](/dynamics365/)-webstedet.</span><span class="sxs-lookup"><span data-stu-id="513cd-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="513cd-118">På siden **Systemparametre** kan systemadministratorer konfigurere adgang til de relevante biblioteker for opgaveguider til implementering af en installation.</span><span class="sxs-lookup"><span data-stu-id="513cd-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="513cd-119">Hvis du vil konfigurere hjælp, skal du være logget på med en konto i den samme lejer som den lejer, hvor appen er installeret.</span><span class="sxs-lookup"><span data-stu-id="513cd-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="513cd-120">Det er ikke muligt at oprette forbindelse til et LCS-bibliotek fra en forekomst af den app, der kører på en lokal virtuel harddisk (VHD).</span><span class="sxs-lookup"><span data-stu-id="513cd-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="513cd-121">[![Formularen Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="513cd-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="513cd-122">Hvis du vil konfigurere opgaveguides til en løsning, skal du følge disse trin på siden **Systemparametre**.</span><span class="sxs-lookup"><span data-stu-id="513cd-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="513cd-123">Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="513cd-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="513cd-124">Du skal vælge linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter vælge **OK** for at få adgang til siden **Systemparametre**.</span><span class="sxs-lookup"><span data-stu-id="513cd-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="513cd-125">[![Opret forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Opret forbindelse til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="513cd-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="513cd-126">Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="513cd-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="513cd-127">Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="513cd-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="513cd-128">Angiv visningsrækkefølgen for BPM-bibliotekerne.</span><span class="sxs-lookup"><span data-stu-id="513cd-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="513cd-129">Visningsrækkefølgen bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="513cd-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="513cd-130">Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og vælge fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="513cd-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="513cd-131">Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="513cd-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="513cd-132">Visning af oversatte opgaveguider</span><span class="sxs-lookup"><span data-stu-id="513cd-132">Showing translated task guides</span></span>

<span data-ttu-id="513cd-133">Oversatte opgaveguider blev frigivet i APQC Unified-biblioteket maj 2016 og i introduktionsbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="513cd-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="513cd-134">For at få vist lokaliseret opgaveguide-hjælp, skal du sikre dig, at din Dynamics 365-løsning er forbundet til maj 2016-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="513cd-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="513cd-135">Brugere kan ændre det sprog, som en opgaveguide vises i, ved at ændre sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="513cd-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="513cd-136">Selvom mange opgaveguider er blevet oversat, viser klienten i øjeblikket ikke de oversatte opgaveguider.</span><span class="sxs-lookup"><span data-stu-id="513cd-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="513cd-137">Derudover er oversættelser i maj 2016-bibliotekst kun tilgængelige for de opgaveguider, der blev frigivet i februar 2016.</span><span class="sxs-lookup"><span data-stu-id="513cd-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="513cd-138">Microsoft udsender et opdateret bibliotek, der omfatter flere oversættelser.</span><span class="sxs-lookup"><span data-stu-id="513cd-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="513cd-139">Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="513cd-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="513cd-140">Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.</span><span class="sxs-lookup"><span data-stu-id="513cd-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="513cd-141">Tilføjelse af tilpasset hjælp</span><span class="sxs-lookup"><span data-stu-id="513cd-141">Adding custom Help</span></span>

<span data-ttu-id="513cd-142">Du kan bruge opgaveguider til at oprette brugerdefineret hjælp, eller du kan oprette forbindelse til **Hjælp**-ruden på et websted.</span><span class="sxs-lookup"><span data-stu-id="513cd-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="513cd-143">Oprette tilpasset hjælp ved hjælp af opgaveguider</span><span class="sxs-lookup"><span data-stu-id="513cd-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="513cd-144">Du kan oprette brugerdefineret hjælp til de understøttedes apps ved at oprette opgaveregistreringer, der afspejler din implementering, og derefter gemme dem i et bibliotek for forretningsprocesser i LCS.</span><span class="sxs-lookup"><span data-stu-id="513cd-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="513cd-145">Du kan ikke oprette brugerdefinerede opgaveguider til Personale.</span><span class="sxs-lookup"><span data-stu-id="513cd-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="513cd-146">Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder.</span><span class="sxs-lookup"><span data-stu-id="513cd-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="513cd-147">Du kan også oprette en kopi af det APQC Unified-bibliotek og derefter åbne opgaveregistreringen i kopien, redigere dem og gemme dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="513cd-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="513cd-148">Du kan finde flere oplysninger under [Arbejdsrutineoptagerressourcer](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="513cd-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="513cd-149">Oprette forbindelse til et brugerdefineret Hjælp-websted</span><span class="sxs-lookup"><span data-stu-id="513cd-149">Connect a custom Help site</span></span>

<span data-ttu-id="513cd-150">Finance and Operations-apps bruges sjældent i den form, de leveres i fra starten.</span><span class="sxs-lookup"><span data-stu-id="513cd-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="513cd-151">Løsningen bliver i stedet tilpasset og udvidet, så den passer til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="513cd-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="513cd-152">Du kan også tilpasse og udvide Hjælp-funktionerne.</span><span class="sxs-lookup"><span data-stu-id="513cd-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="513cd-153">Du kan f.eks. føje brugerdefineret Hjælp til ruden **Hjælp** i produktet.</span><span class="sxs-lookup"><span data-stu-id="513cd-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="513cd-154">Microsoft har stiller en værktøjskasse til rådighed, der hjælper dig med at implementere og forbinde brugerdefineret hjælp til ruden **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="513cd-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="513cd-155">Få flere oplysninger om, hvordan du kan konfigurere en brugerdefineret Hjælp-løsning, der er forbundet til ruden **Hjælp**, i  [Oversigt over brugerdefineret hjælp](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="513cd-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="513cd-156">Hvis du vil samarbejde med Microsoft om værktøjer og processer til tilpasning af hjælp, skal du udfylde formularen på [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="513cd-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="513cd-157">Se også</span><span class="sxs-lookup"><span data-stu-id="513cd-157">See also</span></span>

[<span data-ttu-id="513cd-158">Hjælp-system</span><span class="sxs-lookup"><span data-stu-id="513cd-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="513cd-159">Oversigt over brugerdefineret hjælp</span><span class="sxs-lookup"><span data-stu-id="513cd-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="513cd-160">Ressourcer til arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="513cd-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="513cd-161">Oprette dokumentation eller kursusmateriale ved hjælp af Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="513cd-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="513cd-162">Brugerdefineret GitHub-hjælpelager</span><span class="sxs-lookup"><span data-stu-id="513cd-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]