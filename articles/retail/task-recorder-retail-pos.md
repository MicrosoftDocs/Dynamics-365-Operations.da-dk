---
title: "Arbejdsrutineoptager og hjælp til Retail Modern POS (MPOS) og Cloud POS"
description: Dette emne beskriver, hvordan du bruger Arbejdsrutineoptager i Retail Modern POS og Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: a74a1275f08e3dba60a1002a102e143eb37fcd9a
ms.contentlocale: da-dk
ms.lasthandoff: 01/04/2019

---

# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="003a6-103">Arbejdsrutineoptager og hjælp til Retail Modern POS (MPOS) og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="003a6-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="003a6-104">Dette emne beskriver, hvordan du bruger Arbejdsrutineoptager i Retail Modern POS og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="003a6-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="003a6-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="003a6-105">Overview</span></span>

<span data-ttu-id="003a6-106">Arbejdsrutineoptager i Retail Modern POS eller Cloud POS er en ny løsning, der er bygget med fokus på høj tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="003a6-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="003a6-107">Den indeholder en fleksibel API (brugergrænseflade til program) til udvidelse og problemfri integration for forbrugere af registreringer af forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="003a6-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="003a6-108">Derudover er integrationen af Arbejdsrutineoptager med værktøjet Forretningsprocesmodel (BPM) i Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) blevet overført.</span><span class="sxs-lookup"><span data-stu-id="003a6-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="003a6-109">Brugerne kan derfor fortsætte med at producere omfattende forretningsprocesdiagrammer fra registreringer, så de kan analysere og designe deres programmer.</span><span class="sxs-lookup"><span data-stu-id="003a6-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="003a6-110">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="003a6-110">Architecture</span></span>

<span data-ttu-id="003a6-111">Arbejdsrutineoptager kan registrere brugerhandlinger på klienten med stor nøjagtighed.</span><span class="sxs-lookup"><span data-stu-id="003a6-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="003a6-112">Hvert kontrolelement er udstyret til at underrette Arbejdsrutineoptager om udførelsen af en brugerhandling.</span><span class="sxs-lookup"><span data-stu-id="003a6-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="003a6-113">Kontrolelementet underretter Arbejdsrutineoptager om, at der opstod en hændelse, og overfører alle relevante oplysninger om den tilsvarende brugerhandling i realtid.</span><span class="sxs-lookup"><span data-stu-id="003a6-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="003a6-114">Fra disse oplysninger kan Arbejdsrutineoptager hente typen af brugerhandling (f.eks. et klik på en knap, indtastning af en værdi eller navigation) og alle data, der er relateret til brugerhandlingen (f.eks. værdien og typen af inputdata, formularkontekst eller postkontekst).</span><span class="sxs-lookup"><span data-stu-id="003a6-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="003a6-115">Arbejdsrutineoptager bevarer oplysningerne med tilstrækkelige detaljer til at sikre, at en afspilning af registreringen kan udføre de registrerede handlinger, nøjagtigt som brugeren har udført dem.</span><span class="sxs-lookup"><span data-stu-id="003a6-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="003a6-116">(Afspilningsfunktionen er endnu ikke implementeret på Retail Modern POS eller Cloud POS).</span><span class="sxs-lookup"><span data-stu-id="003a6-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="003a6-117">Basiskonfiguration</span><span class="sxs-lookup"><span data-stu-id="003a6-117">Basic configuration</span></span>

<span data-ttu-id="003a6-118">Følg disse trin for at aktivere opgaveregistrering i POS.</span><span class="sxs-lookup"><span data-stu-id="003a6-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="003a6-119">Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **Kasseapparater**.</span><span class="sxs-lookup"><span data-stu-id="003a6-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="003a6-120">Klik på kasseapparatet for at aktivere opgaveregistrering.</span><span class="sxs-lookup"><span data-stu-id="003a6-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="003a6-121">Under fanen **Kasseapparat** på oversigtspanelet **Generelt** skal du angive indstillingen **Aktivér opgaveregistrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="003a6-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="003a6-122">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="003a6-122">Click **Save**.</span></span>
5. <span data-ttu-id="003a6-123">Gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="003a6-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="003a6-124">Vælg jobbet **Kasseapparater (1090)**, og klik derefter på knappen **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="003a6-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="003a6-125">Opret en registrering</span><span class="sxs-lookup"><span data-stu-id="003a6-125">Create a recording</span></span>

<span data-ttu-id="003a6-126">Følg disse trin for at oprette en ny registrering ved hjælp af Arbejdsrutineoptager.</span><span class="sxs-lookup"><span data-stu-id="003a6-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="003a6-127">Start Retail Modern POS eller Cloud POS, og log på.</span><span class="sxs-lookup"><span data-stu-id="003a6-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="003a6-128">På siden **Indstillinger** i afsnittet **Arbejdsrutineoptager** skal du klikke på **Åbn Arbejdsrutineoptager**.</span><span class="sxs-lookup"><span data-stu-id="003a6-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="003a6-129">Ruden **Arbejdsrutineoptager** vises.</span><span class="sxs-lookup"><span data-stu-id="003a6-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="003a6-130">Du kan klikke på knappen **Luk** (**X**) i øverste højre hjørne for at lukke ruden **Arbejdsrutineoptager**, før du starter en ny registrering.</span><span class="sxs-lookup"><span data-stu-id="003a6-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="003a6-131">Gentag trin 2 for at åbne ruden igen.</span><span class="sxs-lookup"><span data-stu-id="003a6-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="003a6-132">[![Ruden Arbejdsrutineoptager](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="003a6-133">Angiv et navn og en beskrivelse for registreringen, og klik derefter på **Start**.</span><span class="sxs-lookup"><span data-stu-id="003a6-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="003a6-134">Registreringssessionen starter, så snart du klikker på **Start**.</span><span class="sxs-lookup"><span data-stu-id="003a6-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="003a6-135">Hvis du klikker på knappen **Luk** (**X**) i øverste højre hjørne, mens registreringen er i gang, lukkes ruden **Arbejdsrutineoptager**, men registreringssessionen afsluttes ikke.</span><span class="sxs-lookup"><span data-stu-id="003a6-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="003a6-136">Klik på **Hjælp** (spørgsmålstegn) øverst på skærmen for at åbne ruden Arbejdsrutineoptager igen.</span><span class="sxs-lookup"><span data-stu-id="003a6-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="003a6-137">[![Spørgsmålstegn](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="003a6-138">Når du klikker på **Start**, går Arbejdsrutineoptager i registreringstilstand.</span><span class="sxs-lookup"><span data-stu-id="003a6-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="003a6-139">Ruden **Arbejdsrutineoptager** viser oplysninger og kontrolelementer, der vedrører registreringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="003a6-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="003a6-140">Udfør de handlinger, du vil udføre i Retail Modern POS- eller Cloud POS-brugergrænsefladen (UI).</span><span class="sxs-lookup"><span data-stu-id="003a6-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="003a6-141">Klik på **Stop** for at stoppe registreringssessionen.</span><span class="sxs-lookup"><span data-stu-id="003a6-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="003a6-142">Downloadindstillinger</span><span class="sxs-lookup"><span data-stu-id="003a6-142">Download options</span></span>

<span data-ttu-id="003a6-143">Når du har afsluttet registreringssessionen, vises flere indstillinger, så du kan hente din registrering.</span><span class="sxs-lookup"><span data-stu-id="003a6-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="003a6-144">[![Downloadindstillinger](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="003a6-145">Gem til denne pc</span><span class="sxs-lookup"><span data-stu-id="003a6-145">Save to this PC</span></span>

<span data-ttu-id="003a6-146">Du kan bruge registreringspakken til at afspille en opgaveguide, vedligeholde registreringen eller redigere anmærkningerne i registreringen.</span><span class="sxs-lookup"><span data-stu-id="003a6-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="003a6-147">(Denne funktion er endnu ikke implementeret i Retail Modern POS eller Cloud POS).</span><span class="sxs-lookup"><span data-stu-id="003a6-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="003a6-148">Eksportér som Word-dokument</span><span class="sxs-lookup"><span data-stu-id="003a6-148">Export as Word document</span></span>

<span data-ttu-id="003a6-149">Du kan gemme registreringen som et Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="003a6-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="003a6-150">Dokumentet indeholder de registrerede trin og de skærmbilleder, der blev hentet.</span><span class="sxs-lookup"><span data-stu-id="003a6-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="003a6-151">Gem som udviklerregistrering</span><span class="sxs-lookup"><span data-stu-id="003a6-151">Save as developer recording</span></span>

<span data-ttu-id="003a6-152">Den rå registreringsfil er nyttig i udviklerscenarier, f.eks. oprettelse af testkode.</span><span class="sxs-lookup"><span data-stu-id="003a6-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="003a6-153">(Denne funktion er ikke implementeret endnu).</span><span class="sxs-lookup"><span data-stu-id="003a6-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="003a6-154">Registreringskontrolelementer</span><span class="sxs-lookup"><span data-stu-id="003a6-154">Recording controls</span></span>

<span data-ttu-id="003a6-155">[![Registreringskontrolelementer](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="003a6-156">Stop</span><span class="sxs-lookup"><span data-stu-id="003a6-156">Stop</span></span>

<span data-ttu-id="003a6-157">Klik på **Stop** for at stoppe registreringssessionen.</span><span class="sxs-lookup"><span data-stu-id="003a6-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="003a6-158">Bemærk, at du ikke kan genstarte en session, når du har afsluttet den.</span><span class="sxs-lookup"><span data-stu-id="003a6-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="003a6-159">Du skal derfor sørge for, at registreringen er fuldført, før du afslutter den.</span><span class="sxs-lookup"><span data-stu-id="003a6-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="003a6-160">Afbryd midlertidigt</span><span class="sxs-lookup"><span data-stu-id="003a6-160">Pause</span></span>

<span data-ttu-id="003a6-161">Klik på **Afbryd midlertidigt** for at stoppe registreringssessionen midlertidigt og fortsætte med handlingen.</span><span class="sxs-lookup"><span data-stu-id="003a6-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="003a6-162">Trin, du udfører, efter at du har klikket på **Afbryd midlertidigt**, registreres ikke.</span><span class="sxs-lookup"><span data-stu-id="003a6-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="003a6-163">Fortsæt</span><span class="sxs-lookup"><span data-stu-id="003a6-163">Continue</span></span>

<span data-ttu-id="003a6-164">Hvis du vil genoptage registreringssessionen, når du har afbrudt den midlertidigt, skal du klikke på **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="003a6-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="003a6-165">Tag skærmbilleder</span><span class="sxs-lookup"><span data-stu-id="003a6-165">Capture screenshots</span></span>

<span data-ttu-id="003a6-166">Arbejdsrutineoptager kan hente skærmbilleder af brugergrænsefladen i Retail Modern POS i takt med, at du registrerer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="003a6-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="003a6-167">Hvis du vil slå funktionen til hentning af skærmbilleder til, skal du angive indstillingen **Tag skærmbilleder** til **Ja** og derefter foretage registreringen.</span><span class="sxs-lookup"><span data-stu-id="003a6-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="003a6-168">Når registreringen er fuldført, skal du klikke på **Stop** og hente Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="003a6-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="003a6-169">Dokumentet indeholder trinene med relevante skærmbilleder.</span><span class="sxs-lookup"><span data-stu-id="003a6-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="003a6-170">Funktionen til hentning af skærmbilleder understøttes ikke i Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="003a6-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="003a6-171">Start opgave, og Afslut opgave</span><span class="sxs-lookup"><span data-stu-id="003a6-171">Start task and End task</span></span>

<span data-ttu-id="003a6-172">Du kan angive begyndelsen og slutningen af et sæt grupperede trin ved hjælp af knapperne **Start opgave** og **Afslut** **opgave**.</span><span class="sxs-lookup"><span data-stu-id="003a6-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="003a6-173">Klik på **Start opgave** for at tilføje et "Start opgave"-trin, og udfør derefter de trin, der skal medtages i gruppen.</span><span class="sxs-lookup"><span data-stu-id="003a6-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="003a6-174">Når du er færdig med at udføre trinnene for gruppen, skal du klikke på **Afslut opgave**.</span><span class="sxs-lookup"><span data-stu-id="003a6-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="003a6-175">Opgaver hjælper dig med at organisere dine procedurer.</span><span class="sxs-lookup"><span data-stu-id="003a6-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="003a6-176">Opgaver kan være indlejret i andre opgaver.</span><span class="sxs-lookup"><span data-stu-id="003a6-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="003a6-177">På denne måde kan du bedre organisere meget lange og komplekse forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="003a6-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="003a6-178">Tilføj anmærkninger</span><span class="sxs-lookup"><span data-stu-id="003a6-178">Adding annotations</span></span>

<span data-ttu-id="003a6-179">En anmærkning er ekstra tekst, du føjer til et trin i en registrering.</span><span class="sxs-lookup"><span data-stu-id="003a6-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="003a6-180">Du kan f.eks. bruge anmærkninger til at give brugeren mere kontekst eller flere instruktioner.</span><span class="sxs-lookup"><span data-stu-id="003a6-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="003a6-181">Du kan tilføje anmærkninger før eller efter et trin.</span><span class="sxs-lookup"><span data-stu-id="003a6-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="003a6-182">Du kan tilføje en anmærkning til ethvert trin ved at klikke på knappen **Rediger** (blyantssymbol) til højre for trinnet.</span><span class="sxs-lookup"><span data-stu-id="003a6-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="003a6-183">[![Knappen Rediger til et trin](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="003a6-184">Tekst og notater</span><span class="sxs-lookup"><span data-stu-id="003a6-184">Texts and notes</span></span>

<span data-ttu-id="003a6-185">Du kan bruge felterne **Tekster** og **Noter** til at tilføje tekst, der skal knyttes til et trin i en opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="003a6-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="003a6-186">[![Felterne Tekster og Noter](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="003a6-187">Tekst</span><span class="sxs-lookup"><span data-stu-id="003a6-187">Text</span></span>

<span data-ttu-id="003a6-188">Tekst, du har angivet i feltet **Tekst**, vises *over* teksten til trinnet i opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="003a6-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="003a6-189">Denne placering er velegnet til tekst, du ønsker, at brugeren skal læse, før han eller hun fuldfører trinnet.</span><span class="sxs-lookup"><span data-stu-id="003a6-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="003a6-190">Notater</span><span class="sxs-lookup"><span data-stu-id="003a6-190">Notes</span></span>

<span data-ttu-id="003a6-191">Tekst, du har angivet i feltet **Notater**, vises *under* teksten til trinnet i opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="003a6-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="003a6-192">For at læse noteteksten skal brugeren udvide teksten til trinnet i pop op-vinduet.</span><span class="sxs-lookup"><span data-stu-id="003a6-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="003a6-193">Denne placering er velegnet til valgfrit læsemateriale eller andre oplysninger, der kan være nyttige for brugeren, men som ikke er nødvendige for brugeren for at fuldføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="003a6-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="003a6-194">Hjælp i Retail Modern POS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="003a6-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="003a6-195">For at få vist dine egne brugerdefinerede opgaveregistreringer i ruden Hjælp i Retail Modern POS og Cloud POS så de kan afspilles som opgaveguider eller vises som tekst, skal du gemme opgaveregistreringerne i dit eget BPM-bibliotek og derefter opdatere dine systemparametre til Hjælp til at pege på BPM-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="003a6-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="003a6-196">Vil du have mere hjælp, kan du se [Forbindelse til hjælpesystemet.](../fin-and-ops/get-started/help-connect.md)</span><span class="sxs-lookup"><span data-stu-id="003a6-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="003a6-197">Hjælpen til Retail Modern POS og Cloud POS søger i LCS i realtid.</span><span class="sxs-lookup"><span data-stu-id="003a6-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="003a6-198">Den søger på tværs af alle BPM-biblioteker, der er valgt i Microsoft Dynamics 365 for Retail Hjælp-systemparametrene og viser de relevante resultater.</span><span class="sxs-lookup"><span data-stu-id="003a6-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="003a6-199">For at få adgang til menuen **Hjælp** skal du klikke på knappen **Hjælp** (spørgsmålstegn) øverst på skærmen, og derefter skal du skrive navnet på din proces i søgefeltet og trykke på søgeknappen.</span><span class="sxs-lookup"><span data-stu-id="003a6-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="003a6-200">[![Knappen Hjælp](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="003a6-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="003a6-201">Når du klikker på en opgaveguide i søgeresultaterne, kan du enten få vist trinnene som et emne i Hjælp eller eksportere trinnene til et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="003a6-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="003a6-202">Hjælp i Retail Modern POS og Cloud POS viser ikke opgavevejledninger i henhold til, hvilken form du er, eller operation, du foretager.</span><span class="sxs-lookup"><span data-stu-id="003a6-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="003a6-203">Du skal skrive procesnavnet i søgefeltet og derefter klikke på **Søg**.</span><span class="sxs-lookup"><span data-stu-id="003a6-203">You have to type the process name in the search box and then click **Search**.</span></span>

