---
title: Redigere onboardingguider og -skabeloner i Dynamics 365 Talent - Onboard
description: Dette emne forklarer, hvordan du kan føje aktiviteter og andre oplysninger til onboardingguider og -skabeloner i Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897114"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="51bf9-103">Redigere onboardingguider og -skabeloner</span><span class="sxs-lookup"><span data-stu-id="51bf9-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51bf9-104">Når du har oprettet en onboardingguide eller -skabelon i Microsoft Dynamics 365 Talent: Onboard, skal du tilføje en introduktion, aktiviteter, kontakter og ressourcer.</span><span class="sxs-lookup"><span data-stu-id="51bf9-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="51bf9-105">Onboard giver dig omfattende indhold i dine onboardingguider, herunder:</span><span class="sxs-lookup"><span data-stu-id="51bf9-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="51bf9-106">YouTube-videoer</span><span class="sxs-lookup"><span data-stu-id="51bf9-106">YouTube videos</span></span>
- <span data-ttu-id="51bf9-107">Microsoft Sway-præsentationer</span><span class="sxs-lookup"><span data-stu-id="51bf9-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="51bf9-108">Microsoft PowerApps-apps</span><span class="sxs-lookup"><span data-stu-id="51bf9-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="51bf9-109">Microsoft Stream-videoer</span><span class="sxs-lookup"><span data-stu-id="51bf9-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="51bf9-110">Microsoft Forms-formularer</span><span class="sxs-lookup"><span data-stu-id="51bf9-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="51bf9-111">Iframes, der har webindhold</span><span class="sxs-lookup"><span data-stu-id="51bf9-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="51bf9-112">Redigere introduktioner eller aktiviteter, der er importeret fra en skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="51bf9-113">Hvis du opretter en onboardingguide ud fra en skabelon, eller hvis du importerer aktiviteter fra én skabelon til en anden, vil du bemærke **Lås**-knappen på de importerede aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="51bf9-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="51bf9-114">Disse kaldes *administrerede aktiviteter*.</span><span class="sxs-lookup"><span data-stu-id="51bf9-114">These are called *managed activities*.</span></span>

<span data-ttu-id="51bf9-115">[![Administrerede aktiviteter](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="51bf9-116">Når du vælger en administreret aktivitet, kan du se kildeskabelonen øverst i aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="51bf9-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="51bf9-117">[![Administreret aktivitetskilde](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="51bf9-118">Hvis du redigerer en aktivitet i en skabelon, vil Onboard overføre ændringerne til alle skabeloner og ikke-sendte guider, der er baseret på denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="51bf9-119">Hvis du vælger en ikke-afsendt guide, der er baseret på en skabelon, du har redigeret, og derefter vælger fanen **Aktiviteter** i guiden, vises en meddelelse om, at guiden er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="51bf9-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="51bf9-120">Vælg **OK** for at lukke beskeden.</span><span class="sxs-lookup"><span data-stu-id="51bf9-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="51bf9-121">[![Besked om ændring](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="51bf9-122">Der vises en sort prik ud for de opdaterede aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="51bf9-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="51bf9-123">[![Ændret aktivitet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="51bf9-124">Du kan ikke redigere administrerede aktiviteter uden for den oprindelige skabelon, undtagen for at tilføje en modtager, en forfaldsdato eller andre oplysninger i højre sektion af aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="51bf9-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="51bf9-125">Hvis du vil redigere en administreret aktivitet, eller hvis du ikke ønsker, at en aktivitet skal modtage opdateringer fra den skabelon, den kommer fra, skal du vælge knappen **Lås** for den pågældende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="51bf9-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="51bf9-126">Knappen **Lås** forsvinder.</span><span class="sxs-lookup"><span data-stu-id="51bf9-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="51bf9-127">Aktiviteten vil ikke længere blive administreret af den oprindelige skabelon, og den vil ikke længere modtage opdateringer fra denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="51bf9-128">De opdateringer, du foretager i en aktivitet, påvirker ikke den oprindelige skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="51bf9-129">Hvis du sletter en aktivitet fra en guide og overfører ændringer fra den pågældende guides skabelon, vil aktiviteten forblive slettet i guiden.</span><span class="sxs-lookup"><span data-stu-id="51bf9-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="51bf9-130">Kontakter og ressourcer administreres ikke af skabeloner.</span><span class="sxs-lookup"><span data-stu-id="51bf9-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="51bf9-131">Sektioner administreres heller ikke, så hvis du tilføjer eller redigerer en sektion i en skabelon, vil ændringerne ikke blive overført til guider eller skabeloner, der bruger den pågældende skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="51bf9-132">Hvis du føjer nye aktiviteter til en skabelon, overføres de nye aktiviteter til guider og skabeloner, der er baseret på skabelonen, og de nye aktiviteter vises øverst.</span><span class="sxs-lookup"><span data-stu-id="51bf9-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="51bf9-133">Importere aktiviteter fra en anden skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-133">Import activities from another template</span></span>

<span data-ttu-id="51bf9-134">Du kan importere aktiviteter fra en eller flere skabeloner til en guide eller skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="51bf9-135">Vælg den guide eller skabelon, du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="51bf9-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="51bf9-136">Vælg fanen **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="51bf9-137">Vælg fanen **Importér** i sektionen til højre.</span><span class="sxs-lookup"><span data-stu-id="51bf9-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="51bf9-138">[![Importere aktiviteter](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="51bf9-139">Hvis du vil have vist opgaverne som eksempel under en ny fane i browseren, skal du vælge knappen **Åbn på ny fane** i en skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="51bf9-140">[![Importere aktiviteter](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="51bf9-141">Træk den ønskede skabelon til det sted i din guideskabelon, hvor aktiviteterne skal vises, og slip den.</span><span class="sxs-lookup"><span data-stu-id="51bf9-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="51bf9-142">Fortsæt med at redigere din guide eller skabelon.</span><span class="sxs-lookup"><span data-stu-id="51bf9-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="51bf9-143">De importerede aktiviteter vil indeholde knappen **Lås**, som angiver, at disse aktiviteter administreres af den skabelon, du har importeret fra.</span><span class="sxs-lookup"><span data-stu-id="51bf9-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="51bf9-144">Når du foretager ændringer i den importerede skabelon, opdateres disse aktiviteter i den skabelon, du har importeret dem til.</span><span class="sxs-lookup"><span data-stu-id="51bf9-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="51bf9-145">Ændringerne overføres dog ikke automatisk til de guider, der er oprettet ud fra den skabelon, du har importeret til.</span><span class="sxs-lookup"><span data-stu-id="51bf9-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="51bf9-146">Overføre ændringer fra en skabelon til andre skabeloner eller guider</span><span class="sxs-lookup"><span data-stu-id="51bf9-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="51bf9-147">Hvis du redigerer en skabelon, der indeholder aktiviteter, som bruges i andre skabeloner eller guider, skal du overføre ændringerne, hvis du ønsker, at de skal vises i andre skabeloner eller guider.</span><span class="sxs-lookup"><span data-stu-id="51bf9-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="51bf9-148">Hvis du ikke er sikker på, om aktiviteterne i skabelonen bruges i andre skabeloner eller guider, skal du vælge fanen **Anvendt i** for at se, hvor disse aktiviteter vises.</span><span class="sxs-lookup"><span data-stu-id="51bf9-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="51bf9-149">[![Se guider og skabelonaktiviteter, der bruges i](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="51bf9-150">Sådan overføres dine ændringer:</span><span class="sxs-lookup"><span data-stu-id="51bf9-150">To push your changes:</span></span>

1. <span data-ttu-id="51bf9-151">Gem ændringerne ved at vælge knappen **Gem**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="51bf9-152">Hvis du ikke gør det, bliver du bedt om at gemme ændringerne i næste trin.</span><span class="sxs-lookup"><span data-stu-id="51bf9-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="51bf9-153">Vælg **Overfør disse ændringer**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="51bf9-154">Tilføje eller redigere en introduktion</span><span class="sxs-lookup"><span data-stu-id="51bf9-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="51bf9-155">Angiv en titel til din guide og en åbningsmeddelelse under fanen **Introduktion**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="51bf9-156">Hvis du vil bruge eksempelteksten, skal du vælge **Brug denne meddelelse**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="51bf9-157">[![Fanen Introduktion i en Onboard-skabelon](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="51bf9-158">Brug formateringsknapperne til at fremhæve tekst, som du har brug for, eller til at tilføje billeder eller links.</span><span class="sxs-lookup"><span data-stu-id="51bf9-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="51bf9-159">Vælg **Gem** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="51bf9-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="51bf9-160">Tilføje eller redigere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="51bf9-160">Add or edit activities</span></span>

1. <span data-ttu-id="51bf9-161">Under fanen **Aktiviteter** skal du trække elementer fra højre til redigeringsområdet.</span><span class="sxs-lookup"><span data-stu-id="51bf9-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="51bf9-162">Hvis du vil organisere din guide i sektioner, skal du trække elementet **Ny sektion** til redigeringsområdet og angive et navn og en valgfri beskrivelse af sektionen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="51bf9-163">Tilføjelse af en ny sektion til en onboardingguide eller -skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="51bf9-164">Hvis du vil tilføje aktiviteter, som din nyansatte skal udføre, skal du trække elementet **Ny aktivitet** til redigeringsområdet og angive et navn og en beskrivelse for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="51bf9-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="51bf9-165">Tilføjelse af en ny aktivitet til en onboardingguide eller -skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="51bf9-166">Føje avanceret indhold til din onboardingguide:</span><span class="sxs-lookup"><span data-stu-id="51bf9-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="51bf9-167">Hvis du vil tilføje en YouTube-video, skal du trække **YouTube**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive URL-adressen til YouTube-videoen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="51bf9-168">Hvis du vil tilføje en Sway-præsentation eller et nyhedsbrev, skal du trække **Sway**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive den integrerede URL-adresse til Sway-præsentationen eller -nyhedsbrevet.</span><span class="sxs-lookup"><span data-stu-id="51bf9-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="51bf9-169">Hvis du vil tilføje en Microsoft Power Apps-app, skal du trække **Power Apps**-elementet til redigeringsområdet, angive et navn og en beskrivelse for aktiviteten og enten vælge Power Apps-appen eller angive Power Apps-app-id.</span><span class="sxs-lookup"><span data-stu-id="51bf9-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="51bf9-170">Hvis du vil tilføje en Microsoft Stream-video, skal du trække **Microsoft Stream**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive URL-adressen til Microsoft Stream-videoen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="51bf9-171">Hvis du vil tilføje en Microsoft forms-formular, skal du trække **Microsoft Forms**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten, angive URL-adressen til formen Microsoft Forms og angive størrelsen på skærmområdet.</span><span class="sxs-lookup"><span data-stu-id="51bf9-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="51bf9-172">Hvis du vil tilføje en Iframe, der har webindhold, skal du trække elementet **Webindhold (iframe)** til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten, angive URL-adressen til webindholdet og angive størrelsen på skærmområdet.</span><span class="sxs-lookup"><span data-stu-id="51bf9-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="51bf9-173">Tilføjelse af rigt indhold til en onboardingguide eller -skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="51bf9-174">Valgfrit: I området til højre for hver aktivitet skal du tildele aktiviteten en bestemt person eller rolle, tilføje en forfaldsdato og kontaktperson og tildele en kategorifarve.</span><span class="sxs-lookup"><span data-stu-id="51bf9-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="51bf9-175">Når du tildeler en person eller rolle en aktivitet, oprettes der en opgave for hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="51bf9-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="51bf9-176">Denne opgave vises i menuen **Opgaver** i Onboard.</span><span class="sxs-lookup"><span data-stu-id="51bf9-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="51bf9-177">[![Tildeling af en aktivitet i en onboardguide eller -skabelon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="51bf9-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="51bf9-178">Vælg **Gem** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="51bf9-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="51bf9-179">Hvis du vil slette en aktivitet eller sektion, skal du vælge knappen **Slet** (papirkurvssymbolet) i øverste højre hjørne af aktiviteten eller sektionen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="51bf9-180">Hvis du vil omarrangere aktiviteter og sektioner, skal du trække dem til et nyt sted.</span><span class="sxs-lookup"><span data-stu-id="51bf9-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="51bf9-181">Tilføje eller redigere kontakter</span><span class="sxs-lookup"><span data-stu-id="51bf9-181">Add or edit contacts</span></span>

<span data-ttu-id="51bf9-182">Du kan tilføje kontaktpersoner, der kan hjælpe din nyansatte med at komme godt fra start.</span><span class="sxs-lookup"><span data-stu-id="51bf9-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="51bf9-183">Disse kontaktpersoner kan være rekrutteringsmedarbejdere, teammedlemmer, onboardingkammerater, vejledere, administratorer og it-supportmedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="51bf9-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="51bf9-184">Vælg **Ny kontakt** under fanen **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="51bf9-185">Angiv kontaktpersonens navn eller mailadresse i dialogboksen **Tilføj teammedlem**, angiv en kort beskrivelse, der forklarer, hvordan kontaktpersonen kan hjælpe den nyansatte, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="51bf9-186">Tilføjelse af kontakter til en onboardingguide eller -skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="51bf9-187">Du kan også vælge en eller flere kontaktpersoner under **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="51bf9-188">Vælg **Gem** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="51bf9-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="51bf9-189">Hvis du vil slette en kontakt, skal du vælge knappen **Slet** (papirkurvssymbolet) til højre for kontakten.</span><span class="sxs-lookup"><span data-stu-id="51bf9-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="51bf9-190">Hvis du vil redigere en kontakt, skal du vælge knappen **Rediger** (blyantssymbolet) til højre for kontakten.</span><span class="sxs-lookup"><span data-stu-id="51bf9-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="51bf9-191">Tilføje eller redigere ressourcer</span><span class="sxs-lookup"><span data-stu-id="51bf9-191">Add or edit resources</span></span>

<span data-ttu-id="51bf9-192">Du kan tilføje nyttige filer, kort og links i sektionen **Ressourcer** i din onboardingguide.</span><span class="sxs-lookup"><span data-stu-id="51bf9-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="51bf9-193">Vælg **Ny ressource** under fanen **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="51bf9-194">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="51bf9-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="51bf9-195">Hvis du vil tilføje en fil, skal du vælge fanen **Fil** og trække filen til det afsatte område.</span><span class="sxs-lookup"><span data-stu-id="51bf9-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="51bf9-196">(Du kan også klikke på et vilkårligt sted i området for at søge efter filen på din computer eller vælge **Gennemse OneDrive**). Angiv et navn til filen, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="51bf9-197">Hvis du vil tilføje et link, skal du vælge fanen **Link**, angive et navn og en adresse for linket og derefter vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="51bf9-198">Hvis du vil tilføje et kort, skal du vælge fanen **Kort**, angive et navn og en adresse for kortet og derefter vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="51bf9-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="51bf9-199">Onboard vil medtage et kort over den adresse, du angiver.</span><span class="sxs-lookup"><span data-stu-id="51bf9-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="51bf9-200">Tilføjelse af ressourcer til en onboardingguide eller -skabelon</span><span class="sxs-lookup"><span data-stu-id="51bf9-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="51bf9-201">Vælg **Gem** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="51bf9-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="51bf9-202">Hvis du vil slette en ressource, skal du vælge knappen **Slet** (papirkurvssymbolet) til højre for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="51bf9-203">Hvis du vil redigere en ressource, skal du vælge knappen **Rediger** (blyantssymbolet) til højre for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="51bf9-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51bf9-204">Næste trin</span><span class="sxs-lookup"><span data-stu-id="51bf9-204">Next steps</span></span>

- [<span data-ttu-id="51bf9-205">Dele indhold med andre bidragydere</span><span class="sxs-lookup"><span data-stu-id="51bf9-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="51bf9-206">Se status for opgaver og onboarding af medarbejdere</span><span class="sxs-lookup"><span data-stu-id="51bf9-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="51bf9-207">Oprette ansættelsesteam i Onboard</span><span class="sxs-lookup"><span data-stu-id="51bf9-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="51bf9-208">Se også</span><span class="sxs-lookup"><span data-stu-id="51bf9-208">See also</span></span>

- [<span data-ttu-id="51bf9-209">Prøve eller købe appen Onboard</span><span class="sxs-lookup"><span data-stu-id="51bf9-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="51bf9-210">Nyheder eller ændringer i Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="51bf9-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="51bf9-211">Frigivelsesplaner</span><span class="sxs-lookup"><span data-stu-id="51bf9-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="51bf9-212">Få support til Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="51bf9-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
