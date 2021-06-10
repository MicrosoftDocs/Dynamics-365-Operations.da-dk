---
title: Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer
description: Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049458"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="43f04-103">Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer</span><span class="sxs-lookup"><span data-stu-id="43f04-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="43f04-104">KB-nummer: 4615588</span><span class="sxs-lookup"><span data-stu-id="43f04-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="43f04-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="43f04-105">Symptoms</span></span>

<span data-ttu-id="43f04-106">I nogle scenarier kan du få vist følgende meddelelse, når du åbner siden **Varedisponering**, efter du har importeret varer via objektet *Varedisponering V2*:</span><span class="sxs-lookup"><span data-stu-id="43f04-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="43f04-107">Vil du gemme dine ændringer, før der lukkes?</span><span class="sxs-lookup"><span data-stu-id="43f04-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="43f04-108">Du modtager denne meddelelse, selvom du ikke har foretaget nogen ændringer.</span><span class="sxs-lookup"><span data-stu-id="43f04-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="43f04-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="43f04-109">Resolution</span></span>

<span data-ttu-id="43f04-110">Siden **Varedisponering** indeholder kompleks standardlogik, der kan medføre, at meddelelsen vises, når der for nylig er foretaget direkte ændringer i databasen, f.eks. via import af objekt.</span><span class="sxs-lookup"><span data-stu-id="43f04-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="43f04-111">`AREGENERALSETTINGSOVERRIDDEN`-objektfeltet er f.eks. angivet til *Nej*, men du kan importere en fil, der indeholder nye eller ændrede værdier for felter, f.eks. `PRODUCTCOVERAGEGROUPID` og/eller `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="43f04-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="43f04-112">Da `AREGENERALSETTINGSOVERRIDDEN`-feltet er angivet til *Nej*, fjernes værdierne i dette tilfælde automatisk fra felterne, når du åbner siden **Varedisponering** første gang efter importen.</span><span class="sxs-lookup"><span data-stu-id="43f04-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="43f04-113">Hvis du gemmer ændringerne, som meddelelsesfeltet beder om, gemmes de i databasen.</span><span class="sxs-lookup"><span data-stu-id="43f04-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="43f04-114">Ellers modtager du den samme meddelelse, næste gang du åbner siden.</span><span class="sxs-lookup"><span data-stu-id="43f04-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="43f04-115">Hvis du vil forhindre denne funktionsmåde, men også medtage værdier for felter, f.eks. `PRODUCTCOVERAGEGROUPID` via import af objekter, skal du angive `AREGENERALSETTINGSOVERRIDDEN` til *Ja*, når du importerer.</span><span class="sxs-lookup"><span data-stu-id="43f04-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
