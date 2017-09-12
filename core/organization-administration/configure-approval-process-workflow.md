---
title: Konfigurere en godkendelsesproces i en arbejdsgang
description: "Brug nedenstående procedure til at konfigurere egenskaberne for godkendelsesprocessen."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: eedadfcbfac9d792a5ab80c1dcd8f3abfaddca08
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="configure-an-approval-process-in-a-workflow"></a><span data-ttu-id="f1fd6-103">Konfigurere en godkendelsesproces i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="f1fd6-103">Configure an approval process in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f1fd6-104">Brug nedenstående procedure til at konfigurere egenskaberne for godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="f1fd6-105">Hvis du vil konfigurere en godkendelsesproces i arbejdsgangseditoren, skal du højreklikke på godkendelsesprocessen og derefter klikke på **Egenskaber** for at åbne formularen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="f1fd6-106">Navngive godkendelsesprocessen</span><span class="sxs-lookup"><span data-stu-id="f1fd6-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="f1fd6-107">Udfør følgende trin for at angive et navn til godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="f1fd6-108">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f1fd6-109">Skriv et entydigt navn til godkendelsesprocessen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="f1fd6-110">Angive, hvornår systemet automatisk skal behandle dokumentet</span><span class="sxs-lookup"><span data-stu-id="f1fd6-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="f1fd6-111">Du kan konfigurere systemet, så et dokument behandles automatisk, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="f1fd6-112">Systemet kan f.eks. godkende udgiftsrapporter med totalbeløb på mindre end 100 kr.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="f1fd6-113">Udfør disse trin for at angive, hvornår systemet skal behandle dokumentet automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="f1fd6-114">Klik på **Automatiske handlinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="f1fd6-115">Marker afkrydsningsfeltet **Aktivér automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="f1fd6-116">Klik på **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="f1fd6-117">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-117">Enter a condition.</span></span>
5.  <span data-ttu-id="f1fd6-118">Angive yderligere betingelser, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="f1fd6-119">Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="f1fd6-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="f1fd6-120">Klik på **Test** for at åbne formen **Test betingelse for arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="f1fd6-121">Vælg en post i området **Valider betingelse** i formen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="f1fd6-122">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-122">Click **Test**.</span></span> <span data-ttu-id="f1fd6-123">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="f1fd6-124">Klik på **OK** eller **Annuller** for at vende tilbage til formen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="f1fd6-125">Vælg den handling, som systemet skal udføre på dokumentet, på listen **Handling til automatisk udførelse**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f1fd6-126">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="f1fd6-126">Specify when notifications are sent</span></span>
<span data-ttu-id="f1fd6-127">Du kan sende beskeder til personer, når et dokument er godkendt, afvist, delegeret videre eller eskaleret - eller når der er anmodet om en ændring.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="f1fd6-128">Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="f1fd6-129">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="f1fd6-130">Markér afkrydsningsfeltet ud for de hændelser, der skal sendes beskeder i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="f1fd6-131">**Deleger** – når et dokument er tildelt til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="f1fd6-132">**Eskaler** – når den tildelte bruger ikke har udført nogen handling i forbindelse med dokumentet inden for den tildelte tid.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="f1fd6-133">**Godkend** – når et dokument er blevet godkendt.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="f1fd6-134">**Afvis** – når et dokument er blevet afvist.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="f1fd6-135">**Anmod om ændring** – når den bruger, der har fået opgaven tildelt, har anmodet om en ændring i et fremsendt dokument.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="f1fd6-136">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="f1fd6-137">Klik på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="f1fd6-138">Angiv beskedteksten i tekstboksen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="f1fd6-139">Hvis du vil personalisere teksten, kan du indsætte pladsholdere, som erstattes af de korrekte data, når de vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="f1fd6-140">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="f1fd6-141">Klik i tekstboksen på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="f1fd6-142">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="f1fd6-143">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="f1fd6-144">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="f1fd6-145">Klik på **Oversættelser** for at tilføje oversættelser af beskeden.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="f1fd6-146">Udfør følgende trin i den form, der vises:</span><span class="sxs-lookup"><span data-stu-id="f1fd6-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="f1fd6-147">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="f1fd6-148">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="f1fd6-149">Indtast teksten i tekstfeltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="f1fd6-150">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="f1fd6-151">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-151">Click **Close**.</span></span>

8.  <span data-ttu-id="f1fd6-152">Klik på fanen **Modtager**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="f1fd6-153">Angiv, hvem beskederne sendes til.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="f1fd6-154">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin i forbindelse med indstillingen, før du går videre til trin 10.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f1fd6-155">Indstilling</span><span class="sxs-lookup"><span data-stu-id="f1fd6-155">Option</span></span></th>
    <th><span data-ttu-id="f1fd6-156">Modtagere af besked</span><span class="sxs-lookup"><span data-stu-id="f1fd6-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="f1fd6-157">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="f1fd6-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f1fd6-158"><strong>Deltager</strong></span><span class="sxs-lookup"><span data-stu-id="f1fd6-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="f1fd6-159">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="f1fd6-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f1fd6-160">Når du har valgt <strong>Deltager</strong>, skal du klikke på fanen <strong>Rollebaseret</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1fd6-161">Vælg den type gruppe eller rolle, du vil have sendt beskeder til, på listen <strong>Deltagertype</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f1fd6-162">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f1fd6-163"><strong>Arbejdsgangsbruger</strong></span><span class="sxs-lookup"><span data-stu-id="f1fd6-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="f1fd6-164">Brugere, som deltager i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="f1fd6-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f1fd6-165">Når du har valgt <strong>Arbejdsgangsbruger</strong>, skal du klikke på fanen <strong>Arbejdsgangsbruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1fd6-166">På listen <strong>Arbejdsgangsbruger</strong> skal du vælge en bruger, som deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f1fd6-167"><strong>Brugere</strong></span><span class="sxs-lookup"><span data-stu-id="f1fd6-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="f1fd6-168">Bestemte Microsoft Dynamics 365 for Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="f1fd6-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f1fd6-169">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1fd6-170">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere af Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="f1fd6-171">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="f1fd6-172">Gentag trin 3 til 9 for hvert af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="f1fd6-173">Angive en endelig godkender</span><span class="sxs-lookup"><span data-stu-id="f1fd6-173">Specify a final approver</span></span>
<span data-ttu-id="f1fd6-174">Det kan være en god ide at udpege en endelig godkender for scenarier, hvor godkenderen er den person, der har sendt dokumentet til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="f1fd6-175">Udfør følgende trin for at angive en endelig godkender.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="f1fd6-176">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f1fd6-177">Markér afkrydsningsfeltet **Brug endelig godkender**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="f1fd6-178">Vælg den bruger på listen, der skal være endelig godkender.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="f1fd6-179">Angive en tidsgrænse</span><span class="sxs-lookup"><span data-stu-id="f1fd6-179">Set a time limit</span></span>
<span data-ttu-id="f1fd6-180">Udfør følgende trin, hvis godkendelsesprocessen skal fuldføres inden en bestemt tidsgrænse.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-180">Follow these steps if the approval process must be completed in a specific time.</span></span>
| <span data-ttu-id="f1fd6-181">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="f1fd6-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fd6-182">De indstillinger, du vælger under udførelsen af disse trin, tilsidesætter de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** for hvert godkendelsestrin.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="f1fd6-183">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f1fd6-184">Markér afkrydsningsfeltet **Angiv en tidsgrænse for** **arbejdsgangselementet**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="f1fd6-185">Angiv, hvornår godkendelsesprocessen skal fuldføres, i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="f1fd6-186">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f1fd6-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="f1fd6-187">**Timer** – angiv det antal timer, inden for hvilke godkendelsesprocessen skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="f1fd6-188">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f1fd6-189">**Dage** – angiv det antal dage, inden for hvilke godkendelsesprocessen skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="f1fd6-190">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f1fd6-191">**Uger** – angiv det antal uger, inden for hvilke godkendelsesprocessen skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="f1fd6-192">**Måneder** – vælg den dag og uge, hvor godkendelsesprocessen senest skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="f1fd6-193">Måske ønsker du godkendelsesprocessen fuldført f.eks. senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="f1fd6-194">**År** – vælg den dag, uge og måned, hvor godkendelsesprocessen senest skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="f1fd6-195">Måske ønsker du godkendelsesprocessen fuldført f.eks. senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="f1fd6-196">Hvis tidsfristen overskrides, behandles dokumentet af systemet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="f1fd6-197">Vælg den handling, der skal udføres, på listen **Handling**.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="f1fd6-198">Angiv, hvilke handlinger der er tilgængelige for brugeren</span><span class="sxs-lookup"><span data-stu-id="f1fd6-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="f1fd6-199">Når en bruger tildeles et dokument, som skal godkendes, skal han eller hun behandle dokumentet som angivet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="f1fd6-200">Udfør følgende trin for at angive, hvilke handlinger brugeren kan udføre med det dokument, der er sendt.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="f1fd6-201">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f1fd6-202">Markér afkrydsningsfeltet **Godkend**, hvis brugeren kan godkende dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="f1fd6-203">Markér afkrydsningsfeltet **Afvis**, hvis brugeren kan afvise dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="f1fd6-204">Markér afkrydsningsfeltet **Anmod om ændring**, hvis brugeren kan anmode om ændringer af dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="f1fd6-205">Marker afkrydsningsfeltet **Deleger**, hvis brugeren kan tildele dokumentet til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="f1fd6-206">**Bemærk**: Afkrydsningsfeltet **Aktivér handlinger fra opgavelisten i Enterprise Portal** frarådes.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="f1fd6-207"> Konfigurere godkendelsestrinene</span><span class="sxs-lookup"><span data-stu-id="f1fd6-207">Configure the approval steps</span></span>
<span data-ttu-id="f1fd6-208">En godkendelsesproces består af godkendelsestrin.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="f1fd6-209">Fuldfør følgende procedure for at tilføje trin til godkendelsesprocessen og konfigurere trinene.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="f1fd6-210">Dobbeltklik på godkendelsesprocessen i arbejdsgangseditoren.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="f1fd6-211">I arbejdsgangseditoren vises trinene i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="f1fd6-212">Du kan tilføje et godkendelsestrin ved at trække trinnet fra området **Arbejdsgangselementer** til lærredet.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="f1fd6-213">Hvis du vil konfigurere et godkendelsestrin, skal du se [Konfigurere et godkendelsestrin](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f1fd6-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






