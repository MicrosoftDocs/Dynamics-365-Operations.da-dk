---
title: Oprette og sende en onboardingguide ved hjælp af Dynamics 365 Talent - Onboard
description: Dette emne forklarer, hvordan du bruger Microsoft Dynamics 365 Talent - Onboard-appen til at oprette en onboardingguide for dine nyansatte. Denne opgave er et vigtigt første skridt i en totalstrategi for styring af menneskelig kapital (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898242"
---
# <a name="create-and-send-an-onboarding-guide"></a><span data-ttu-id="b3b0b-104">Oprette og sende en onboardingguide</span><span class="sxs-lookup"><span data-stu-id="b3b0b-104">Create and send an onboarding guide</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3b0b-105">Microsoft Dynamics 365 Talent: Onboard giver dig mulighed for at oprette onboardingguider ud fra skabeloner, du har oprettet selv, fra skabeloner, der er tilgængelige i et galleri, eller fra bunden.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-105">Microsoft Dynamics 365 Talent: Onboard lets you create onboarding guides from templates that you created yourself, from templates that are available in a gallery, or from scratch.</span></span>

<span data-ttu-id="b3b0b-106">Når du har oprettet en onboardingguide, kan du sende den til en nyansat.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-106">After you've created an onboarding guide, you can send it to a new hire.</span></span> <span data-ttu-id="b3b0b-107">Alternativt kan du sende den til flere nyansatte, som du angiver i en Microsoft Excel-fil, som du downloader fra Onboard-appen.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-107">Alternatively, you can send it to multiple new hires that you specify in a Microsoft Excel file that you download from the Onboard app.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a><span data-ttu-id="b3b0b-108">Oprette en onboardingguide ud fra en skabelon og sende den til en enkelt nyansat</span><span class="sxs-lookup"><span data-stu-id="b3b0b-108">Create an onboarding guide from a template and send it to a single new hire</span></span>

1. <span data-ttu-id="b3b0b-109">Vælg **Skabeloner** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-109">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="b3b0b-110">Under **Mine skabeloner** skal du vælge den skabelon, du vil oprette som onboardingguide til den nyansatte.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-110">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hire.</span></span>
3. <span data-ttu-id="b3b0b-111">Rediger skabelonen, som du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-111">Edit the template as you desire.</span></span> <span data-ttu-id="b3b0b-112">Husk at gemme dit arbejde jævnligt.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-112">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="b3b0b-113">Når du er færdig med at redigere skabelonen, skal du vælge **Opret guide**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-113">When you've finished editing the template, select **Create guide**.</span></span>

    <span data-ttu-id="b3b0b-114">[![Oprettelse af en onboardingguide ud fra en skabelon](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span><span class="sxs-lookup"><span data-stu-id="b3b0b-114">[![Creating an onboarding guide from a template](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span></span>

5. <span data-ttu-id="b3b0b-115">I vinduet **Opret en guide** skal du under **Hvem onboarder du?** indtaste den nyansattes navn eller mailadresse.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-115">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="b3b0b-116">Hvis den nyansatte endnu ikke er i systemet, skal du vælge **Tilføj nu** og indtaste medarbejderens oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-116">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="b3b0b-117">Indtastning af oplysninger til onboarding-guiden</span><span class="sxs-lookup"><span data-stu-id="b3b0b-117">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. <span data-ttu-id="b3b0b-118">Under **Hvornår starter de?** skal du vælge en startdato.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-118">Under **When do they start**, select a start date.</span></span>
7. <span data-ttu-id="b3b0b-119">Hvis onboardingguiden automatisk skal sendes til den nyansatte på en bestemt dato, skal du sørge for, at indstillingen **Planlæg en automatisk afsendelsesdato** er aktiveret, og vælg derefter den automatiske afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-119">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="b3b0b-120">For at sende guiden straks skal du deaktivere indstillingen **Planlæg en automatisk afsendelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-120">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
8. <span data-ttu-id="b3b0b-121">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-121">Select **Done**.</span></span>
9. <span data-ttu-id="b3b0b-122">Når du er færdig med at redigere onboardingguideen, skal du vælge **Send** i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-122">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="b3b0b-123">Udfør derefter ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="b3b0b-123">Then follow one of these steps:</span></span>

    - <span data-ttu-id="b3b0b-124">Hvis du vil sende den nyansatte et link til onboardingguiden, skal du vælge **kopiér et link** og derefter vælge **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-124">To send the new hire a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="b3b0b-125">Hvis du vil tilpasse mailen for onboardingguiden, før du sender den, skal du vælge **Tilpas mailen, før du sender den**, vælge **Næste**, tilpasse mailen, som du ønsker, og derefter vælge **Send**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-125">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="b3b0b-126">Hvis du vil sende mailen uden at tilpasse den, skal du vælge **Næste** og derefter vælge **Send**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-126">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a><span data-ttu-id="b3b0b-127">Oprette en onboardingguide ud fra en skabelon og sende den til flere nyansatte</span><span class="sxs-lookup"><span data-stu-id="b3b0b-127">Create an onboarding guide from a template and send it to multiple new hires</span></span>

<span data-ttu-id="b3b0b-128">Onboard giver dig mulighed for at sende en onboardingguide til flere nyansatte på samme tid.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-128">Onboard lets you send an onboarding guide to multiple new hires at the same time.</span></span>

1. <span data-ttu-id="b3b0b-129">Vælg **Skabeloner** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-129">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="b3b0b-130">Under **Mine skabeloner** skal du vælge den skabelon, du vil oprette som onboardingguide til de nyansatte.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-130">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hires.</span></span>
3. <span data-ttu-id="b3b0b-131">Rediger skabelonen, som du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-131">Edit the template as you desire.</span></span> <span data-ttu-id="b3b0b-132">Husk at gemme dit arbejde jævnligt.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-132">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="b3b0b-133">Når du er færdig med at redigere skabelonen, skal du vælge **Opret guide**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-133">When you've finished editing the template, select **Create guide**.</span></span>
5. <span data-ttu-id="b3b0b-134">I vinduet **Opret en guide** skal du vælge **Skal du onboarde flere personer på én gang?**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-134">In the **Create a guide** window, select **Need to onboard multiple people at once**.</span></span>

    <span data-ttu-id="b3b0b-135">[![Oprettelse af en onboardingguide til flere nyansatte](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span><span class="sxs-lookup"><span data-stu-id="b3b0b-135">[![Creating an onboarding guide for multiple new hires](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span></span>

6. <span data-ttu-id="b3b0b-136">Vælg **skabelon til nyansatte**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-136">Select **new hire template**.</span></span>
7. <span data-ttu-id="b3b0b-137">Når .xlsx-filen er downloadet, skal du vælge **Åbn**, indtast medarbejdernes oplysninger i Excel-projektmappen og gemme projektmappen.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-137">After the .xlsx file is downloaded, select **Open**, enter the employees' information in the Excel workbook, and save the workbook.</span></span>

    <span data-ttu-id="b3b0b-138">[![Download af Excel-skabelonen for at sende onboardingguiden til flere nyansatte](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="b3b0b-138">[![Downloading the Excel template for sending the onboarding guide to multiple new hires](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3b0b-139">Før du kan redigere projektmappen, skal du vælge **Aktivér redigering** i Excel.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-139">Before you can edit the workbook, you must select **Enable editing** in Excel.</span></span>
    > 
    > <span data-ttu-id="b3b0b-140">[![Aktivering af redigering](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span><span class="sxs-lookup"><span data-stu-id="b3b0b-140">[![Enabling editing](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span></span>

8. <span data-ttu-id="b3b0b-141">Træk Excel-projektmappen til det angivne område i vinduet **Opret flere guider**, eller klik hvor som helst i dette område for at søge efter filen på din computer.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-141">Drag the Excel workbook to the designated area in the **Create multiple guides** window, or click anywhere in that area to browse for the file on your computer.</span></span>

    <span data-ttu-id="b3b0b-142">[![Trækning af den redigerede projektmappe](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="b3b0b-142">[![Dragging the edited workbook](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span></span>

9. <span data-ttu-id="b3b0b-143">Når du er færdig med at redigere onboardingguideen, skal du vælge **Send** i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-143">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="b3b0b-144">Udfør derefter ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="b3b0b-144">Then follow one of these steps:</span></span>

    - <span data-ttu-id="b3b0b-145">Hvis du vil sende de nyansatte et link til onboardingguiden, skal du vælge **kopiér et link** og derefter vælge **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-145">To send the new hires a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="b3b0b-146">Hvis du vil tilpasse mailen for onboardingguiden, før du sender den, skal du vælge **Tilpas mailen, før du sender den**, vælge **Næste**, tilpasse mailen, som du ønsker, og derefter vælge **Send**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-146">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="b3b0b-147">Hvis du vil sende mailen uden at tilpasse den, skal du vælge **Næste** og derefter vælge **Send**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-147">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-a-guide-without-using-a-template"></a><span data-ttu-id="b3b0b-148">Oprette en guide uden at bruge en skabelon</span><span class="sxs-lookup"><span data-stu-id="b3b0b-148">Create a guide without using a template</span></span>

<span data-ttu-id="b3b0b-149">Du behøver ikke altid at oprette en guide ud fra en skabelon.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-149">You don't always have to create a guide from a template.</span></span> <span data-ttu-id="b3b0b-150">Hvis du foretrækker det, kan du i stedet oprette en guide fra bunden.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-150">If you prefer, you can create a guide from scratch instead.</span></span>

1. <span data-ttu-id="b3b0b-151">I menuen til venstre skal du vælge **Guider** og derefter vælge **Tilføj**-knappen (plustegnet \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="b3b0b-151">On the left menu, select **Guides**, and then select the **Add** button (the plus sign \[**+**\]).</span></span>
2. <span data-ttu-id="b3b0b-152">I vinduet **Opret en guide** skal du under **Hvem onboarder du?** indtaste den nyansattes navn eller mailadresse.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-152">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="b3b0b-153">Hvis den nyansatte endnu ikke er i systemet, skal du vælge **Tilføj nu** og indtaste medarbejderens oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-153">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="b3b0b-154">Indtastning af oplysninger til onboarding-guiden</span><span class="sxs-lookup"><span data-stu-id="b3b0b-154">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. <span data-ttu-id="b3b0b-155">Under **Hvornår starter de?** skal du vælge en startdato.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-155">Under **When do they start**, select a start date.</span></span>
4. <span data-ttu-id="b3b0b-156">Hvis onboardingguiden automatisk skal sendes til den nyansatte på en bestemt dato, skal du sørge for, at indstillingen **Planlæg en automatisk afsendelsesdato** er aktiveret, og vælg derefter den automatiske afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-156">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="b3b0b-157">For at sende guiden straks skal du deaktivere indstillingen **Planlæg en automatisk afsendelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-157">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
5. <span data-ttu-id="b3b0b-158">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-158">Select **Done**.</span></span>

## <a name="save-a-guide-as-a-template"></a><span data-ttu-id="b3b0b-159">Gemme en guide som en skabelon</span><span class="sxs-lookup"><span data-stu-id="b3b0b-159">Save a guide as a template</span></span>

<span data-ttu-id="b3b0b-160">Du kan gemme en onboardingguide som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-160">You can save an onboarding guide as a template.</span></span> <span data-ttu-id="b3b0b-161">På denne måde kan du spare tid, når du skal oprette flere onboardingguider senere.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-161">In this way, you can save time when you must create more onboarding guides later.</span></span>

1. <span data-ttu-id="b3b0b-162">Vælg **Guider** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-162">On the left menu, select **Guides**.</span></span>
2. <span data-ttu-id="b3b0b-163">Vælg **Mere**-knappen (ellipsen \[**...**\]) til den guide, du vil oprette en skabelon ud fra, og vælg derefter **Gem som skabelon**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-163">Select the **More** button (the ellipsis \[**...**\]) for the guide that you want to create a template from, and then select **Save as template**.</span></span>

    ![[<span data-ttu-id="b3b0b-164">At gemme en onboardingguide som en skabelon</span><span class="sxs-lookup"><span data-stu-id="b3b0b-164">Saving an onboarding guide as a template</span></span>](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. <span data-ttu-id="b3b0b-165">I vinduet **Gem som en ny skabelon** skal du indtaste et navn til din nye skabelon og derefter vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b3b0b-165">In the **Save as a new template** window, enter a name for your new template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b3b0b-166">Næste trin</span><span class="sxs-lookup"><span data-stu-id="b3b0b-166">Next steps</span></span>

- [<span data-ttu-id="b3b0b-167">Redigere onboardingguider og -skabeloner</span><span class="sxs-lookup"><span data-stu-id="b3b0b-167">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="b3b0b-168">Dele indhold med andre bidragydere</span><span class="sxs-lookup"><span data-stu-id="b3b0b-168">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="b3b0b-169">Se status for opgaver og onboarding af medarbejdere</span><span class="sxs-lookup"><span data-stu-id="b3b0b-169">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="b3b0b-170">Oprette ansættelsesteam i Onboard</span><span class="sxs-lookup"><span data-stu-id="b3b0b-170">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="b3b0b-171">Se også</span><span class="sxs-lookup"><span data-stu-id="b3b0b-171">See also</span></span>

- [<span data-ttu-id="b3b0b-172">Prøve eller købe appen Onboard</span><span class="sxs-lookup"><span data-stu-id="b3b0b-172">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="b3b0b-173">Nyheder eller ændringer i Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b3b0b-173">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="b3b0b-174">Frigivelsesplaner</span><span class="sxs-lookup"><span data-stu-id="b3b0b-174">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="b3b0b-175">Få support til Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b3b0b-175">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
