---
title: Ofte stillede spørgsmål om klienter
description: Denne artikel indeholder svar på ofte stillede spørgsmål om Finance and Operations-klienten.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a7d311bfcd65e23e4062f105435d05cb1ceda6b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567034"
---
# <a name="client-faq"></a><span data-ttu-id="deba4-103">Ofte stillede spørgsmål om klienter</span><span class="sxs-lookup"><span data-stu-id="deba4-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="deba4-104">Denne artikel indeholder svar på ofte stillede spørgsmål om Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="deba4-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="deba4-105">Hvorfor indlæses symboler ikke?</span><span class="sxs-lookup"><span data-stu-id="deba4-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="deba4-106">Sikkerhedsindstillingerne i din browser kan forhindre, at symbolerne indlæses korrekt.</span><span class="sxs-lookup"><span data-stu-id="deba4-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="deba4-107">Hvis du vil løse dette problem, kan du prøve følgende trin:</span><span class="sxs-lookup"><span data-stu-id="deba4-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="deba4-108">Hvis du oplever dette problem i Internet Explorer, skal du klikke på **Funktioner**, og klik derefter på **Internetindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="deba4-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="deba4-109">I dialogboksen Internetindstillinger under fanen **Beskyttelse af personlige oplysninger** skal du klikke på **Brugerdefineret niveau** og kontrollere, at indstillingen **Overførsel af skrifttyper** er markeret.</span><span class="sxs-lookup"><span data-stu-id="deba4-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="deba4-110">Ellers skal du muligvis føje appwebstedet til listen over websteder, du har tillid til.</span><span class="sxs-lookup"><span data-stu-id="deba4-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="deba4-111">Jeg savner båndet fra Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="deba4-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="deba4-112">Kan jeg lade faner i handlingsruden være åbne hele tiden?</span><span class="sxs-lookup"><span data-stu-id="deba4-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="deba4-113">Vi planlægger at implementere denne funktion snart.</span><span class="sxs-lookup"><span data-stu-id="deba4-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="deba4-114">Brugerne vil herefter kunne vælge at beholde fanerne i Handlingsruder åbne hele tiden.</span><span class="sxs-lookup"><span data-stu-id="deba4-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="deba4-115">Ellers skjules fanerne, når de ikke bruges, for at give mere skærmplads til siden.</span><span class="sxs-lookup"><span data-stu-id="deba4-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="deba4-116">Hvorfor kan jeg nogle gange se forskellige genvejsmenuer, når jeg højreklikker?</span><span class="sxs-lookup"><span data-stu-id="deba4-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="deba4-117">Hvis du højreklikker på et redigerbart felt (eller hvis tekst er markeret), vises genvejsmenuen i browseren.</span><span class="sxs-lookup"><span data-stu-id="deba4-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="deba4-118">Denne menu giver dig adgang til kommandoerne **Klip**, **Kopiér** og **Sæt ind** kommandoer.</span><span class="sxs-lookup"><span data-stu-id="deba4-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="deba4-119">Vi kan ikke integrere disse kommandoer i genvejsmenuer af sikkerhedsmæssige årsager, da browsere ikke giver os mulighed for automatisk at få adgang til systemets Udklipsholder.</span><span class="sxs-lookup"><span data-stu-id="deba4-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="deba4-120">Hvis du højreklikker på en feltetiket eller værdien af et skrivebeskyttet kontrolelement, vises genvejsmenuen.</span><span class="sxs-lookup"><span data-stu-id="deba4-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="deba4-121">For at gøre tastaturadgang nemmere planlægger vi at implementere en tastaturgenvej i fremtiden, som vil åbne genvejsmenuen.</span><span class="sxs-lookup"><span data-stu-id="deba4-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="deba4-122">Hvor er funktionen Vis detaljer?</span><span class="sxs-lookup"><span data-stu-id="deba4-122">Where is the View details functionality?</span></span>

<span data-ttu-id="deba4-123">Indstillingen **Vis detaljer** er tilgængelig på flere måder:</span><span class="sxs-lookup"><span data-stu-id="deba4-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="deba4-124">Hvis et kontrolelement har funktionaliteten **Vis detaljer**, og hvis kontrolelementet har en værdi, vises denne værdi som et hyperlink.</span><span class="sxs-lookup"><span data-stu-id="deba4-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="deba4-125">Du kan klikke på hyperlinket for at åbne en side, der indeholder yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="deba4-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="deba4-126">**Vis detaljer** er også en indstilling i genvejsmenuer.</span><span class="sxs-lookup"><span data-stu-id="deba4-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="deba4-127">Du kan finde flere oplysninger om, hvornår genvejsmenuer vises, når du højreklikker, i det forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="deba4-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]