---
title: Konfigurere en automatiseret opgave i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer egenskaberne for en automatiseret opgave.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1315dc9d42032087f5de8dfa09bc59382220781
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="6b2ef-103">Konfigurere en automatiseret opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="6b2ef-103">Configure an automated task in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b2ef-104">I dette emne forklares det, hvordan du konfigurerer egenskaberne for en automatiseret opgave.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="6b2ef-105">Hvis du vil konfigurere en automatiseret opgave i arbejdsgangseditoren, skal du højreklikke på opgaven og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6b2ef-106">Brug derefter følgende procedurer for at konfigurere egenskaberne for den automatiserede opgave.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="6b2ef-107">Navngive opgaven</span><span class="sxs-lookup"><span data-stu-id="6b2ef-107">Name the task</span></span>
<span data-ttu-id="6b2ef-108">Udfør følgende trin for at angive et navn på den automatiserede opgave.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="6b2ef-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6b2ef-110">Angiv et entydigt navn til opgaven i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="6b2ef-111">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="6b2ef-111">Specify when notifications are sent</span></span>
<span data-ttu-id="6b2ef-112">Du kan sende beskeder til personer, når en automatiseret opgave er afviklet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="6b2ef-113">Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem de sendes til.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="6b2ef-114">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="6b2ef-115">Markér afkrydsningsfeltet ud for de hændelser, der skal sendes beskeder i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="6b2ef-116">**Udførelse** – der sendes beskeder, når opgaven er afviklet.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="6b2ef-117">**Annulleret** – der sendes beskeder, når opgaven er annulleret.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="6b2ef-118">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="6b2ef-119">Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="6b2ef-120">Hvis du vil personalisere beskeden, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="6b2ef-121">Pladsholderne erstattes med de relevante data, når beskeden vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="6b2ef-122">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6b2ef-123">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6b2ef-124">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6b2ef-125">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6b2ef-126">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="6b2ef-127">Følg disse trin for at tilføje oversættelser af beskeden:</span><span class="sxs-lookup"><span data-stu-id="6b2ef-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="6b2ef-128">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6b2ef-129">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6b2ef-130">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6b2ef-131">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6b2ef-132">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="6b2ef-133">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-133">Click **Close**.</span></span>

7.  <span data-ttu-id="6b2ef-134">På fanen **Modtager** skal du angive, hvem beskederne skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="6b2ef-135">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6b2ef-136">Indstilling</span><span class="sxs-lookup"><span data-stu-id="6b2ef-136">Option</span></span></th>
    <th><span data-ttu-id="6b2ef-137">Modtagere af besked</span><span class="sxs-lookup"><span data-stu-id="6b2ef-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="6b2ef-138">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="6b2ef-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6b2ef-139">Deltager</span><span class="sxs-lookup"><span data-stu-id="6b2ef-139">Participant</span></span></td>
    <td><span data-ttu-id="6b2ef-140">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="6b2ef-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6b2ef-141">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="6b2ef-142">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6b2ef-143">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="6b2ef-143">Workflow user</span></span></td>
    <td><span data-ttu-id="6b2ef-144">Brugere, som deltager i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="6b2ef-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6b2ef-145">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6b2ef-146">Bruger</span><span class="sxs-lookup"><span data-stu-id="6b2ef-146">User</span></span></td>
    <td><span data-ttu-id="6b2ef-147">Bestemte Microsoft Dynamics 365 for Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="6b2ef-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6b2ef-148">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6b2ef-149">Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6b2ef-150">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="6b2ef-151">Gentag trin 3 til 7 for hvert af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





