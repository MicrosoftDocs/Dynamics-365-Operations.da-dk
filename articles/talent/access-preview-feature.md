---
title: Administrere funktioner
description: Dette emne beskriver, hvordan administratorer kan aktivere funktioner til forhåndsvisning i Microsoft Dynamics 365 Talent, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124790"
---
# <a name="manage-features"></a><span data-ttu-id="2bf09-103">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="2bf09-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2bf09-104">Som en del af vores fortløbende implementering af HCM-funktioner til styring af menneskelig kapital for Microsoft Dynamics 365 Human Resources, vil vi give kunderne mulighed for at udnytte nye funktioner, så hurtigt som muligt.</span><span class="sxs-lookup"><span data-stu-id="2bf09-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="2bf09-105">Administratorer kan se og bruge funktioner til visning i deres miljøer.</span><span class="sxs-lookup"><span data-stu-id="2bf09-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="2bf09-106">Disse funktioner bliver snart almindeligt tilgængelige og har gennemgået omfattende test.</span><span class="sxs-lookup"><span data-stu-id="2bf09-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="2bf09-107">Vi mangler kun en sidste runde af kundefeedback og validering, før vi gør dem almindeligt tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="2bf09-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="2bf09-108">Dette emne beskriver, hvordan du kan aktivere funktioner til visning, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner.</span><span class="sxs-lookup"><span data-stu-id="2bf09-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="2bf09-109">Denne liste opdateres, efterhånden som funktioner bliver gjort almindeligt tilgængelige og nye visningsfunktioner frigives.</span><span class="sxs-lookup"><span data-stu-id="2bf09-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="2bf09-110">Der gives ikke besked, når der frigives nye funktioner til visning.</span><span class="sxs-lookup"><span data-stu-id="2bf09-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="2bf09-111">Funktionerne bliver bare synlige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="2bf09-111">Users will just start to see the features.</span></span> <span data-ttu-id="2bf09-112">Yderligere oplysninger om de nye funktioner i Talent finder du i [Nyheder eller ændringer i Dynamics 365 Talent](./whats-new.md) og [Dynamics 365 samt Power Platform-produktbemærkninger](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="2bf09-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="2bf09-113">Aktivere eller deaktivere funktioner i prøveversion</span><span class="sxs-lookup"><span data-stu-id="2bf09-113">Enable or disable preview features</span></span>

<span data-ttu-id="2bf09-114">Hvis du vil have adgang til visningsfunktionerne, skal du først aktivere dem i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="2bf09-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="2bf09-115">Aktivering eller deaktivering af funktioner til visning er specifik for miljøet.</span><span class="sxs-lookup"><span data-stu-id="2bf09-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bf09-116">Når du slår indstillingen **Prøveversioner** til, aktiverer du visningsfunktioner for alle brugere i organisationen, der arbejder i det pågældende miljø.</span><span class="sxs-lookup"><span data-stu-id="2bf09-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="2bf09-117">Når du deaktiverer indstillingen, slår du funktioner til forhåndsvisning fra og gør dem utilgængelige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="2bf09-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="2bf09-118">Visningsfunktioner understøttes kun i begrænset omfang i Talent.</span><span class="sxs-lookup"><span data-stu-id="2bf09-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="2bf09-119">Der er en mindre grad af beskyttelse af personlige oplysninger og færre sikkerhedsfunktioner, og visningsfunktionerne medtages ikke i Talent-serviceaftalen (SLA).</span><span class="sxs-lookup"><span data-stu-id="2bf09-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="2bf09-120">Du bør ikke bruge visningsfunktioner til behandling af personoplysninger (dvs. alle oplysninger, der kan identificere dig) eller til at behandle andre data, der er omfattet af lovbestemte overholdelseskrav.</span><span class="sxs-lookup"><span data-stu-id="2bf09-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="2bf09-121">Attract</span><span class="sxs-lookup"><span data-stu-id="2bf09-121">Attract</span></span>

1. <span data-ttu-id="2bf09-122">Log på Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="2bf09-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="2bf09-123">I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administration**.</span><span class="sxs-lookup"><span data-stu-id="2bf09-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="2bf09-124">Under fanen **Administration af funktioner** skal du vælge indstillingen ud for **Funktioner i prøveversion**, så den bliver blå, og der står **Til**.</span><span class="sxs-lookup"><span data-stu-id="2bf09-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Aktivér funktioner i Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="2bf09-126">Vælg eller annuller markeringen af individuelle forhåndsvisningsfunktioner.</span><span class="sxs-lookup"><span data-stu-id="2bf09-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="2bf09-127">Hvis du ikke gør noget, er alle tilgængelige forhåndsvisningsfunktioner aktiverede.</span><span class="sxs-lookup"><span data-stu-id="2bf09-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="2bf09-128">Opdater browseren for at begynde at se de nye funktioner.</span><span class="sxs-lookup"><span data-stu-id="2bf09-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="2bf09-129">Alle brugere, der allerede er logget på, kan se funktionerne, næste gang de logger på, eller de kan opdatere deres webbrowser for at få vist funktionerne med det samme.</span><span class="sxs-lookup"><span data-stu-id="2bf09-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="2bf09-130">Nogle visningsfunktioner kræver muligvis yderligere konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bf09-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="2bf09-131">Følg linkene ud for visningsfunktionen for at fuldføre opsætningen af det.</span><span class="sxs-lookup"><span data-stu-id="2bf09-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="2bf09-132">Tilbagemelding</span><span class="sxs-lookup"><span data-stu-id="2bf09-132">Feedback</span></span>

<span data-ttu-id="2bf09-133">Vi vil gerne høre fra dig om din oplevelse med disse visningsfunktioner.</span><span class="sxs-lookup"><span data-stu-id="2bf09-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="2bf09-134">Vi opfordrer dig til jævnligt at opslå din feedback på følgende websteder, når du bruger disse eller andre funktioner:</span><span class="sxs-lookup"><span data-stu-id="2bf09-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="2bf09-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Dette websted er en nyttig ressource, hvor brugere kan diskutere eksempler på brug, stille spørgsmål og få hjælp fra community'et.</span><span class="sxs-lookup"><span data-stu-id="2bf09-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="2bf09-136">Fortæl os om de funktioner, som du gerne vil have i produktet, eller gør os opmærksom på eventuelle ændringer, som du synes, vi skal foretage af eksisterende funktioner.</span><span class="sxs-lookup"><span data-stu-id="2bf09-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="2bf09-137">Du kan komme med ideer til produkter på følgende websteder:</span><span class="sxs-lookup"><span data-stu-id="2bf09-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="2bf09-138">Attract-ideer</span><span class="sxs-lookup"><span data-stu-id="2bf09-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="2bf09-139">Onboard-ideer</span><span class="sxs-lookup"><span data-stu-id="2bf09-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="2bf09-140">Undgå at medtage personlige oplysninger (oplysninger, der kan identificere dig) i din feedback eller indsendelser af produktanmeldelser.</span><span class="sxs-lookup"><span data-stu-id="2bf09-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="2bf09-141">Indsamlede oplysninger kan blive analyseret yderligere, men de bruges ikke til at besvare spørgsmål i henhold til gældende love om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2bf09-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="2bf09-142">Personlige data, der indsamles særskilt i henhold til disse programmer, er underlagt [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="2bf09-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="2bf09-143">Sæt et bogmærke ved dette emne, og kom tilbage ofte for at holde dig opdateret om nye eksempelfunktioner, efterhånden som vi frigiver dem.</span><span class="sxs-lookup"><span data-stu-id="2bf09-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bf09-144">Se også</span><span class="sxs-lookup"><span data-stu-id="2bf09-144">See also</span></span>

- [<span data-ttu-id="2bf09-145">Prøv eller køb Talent-apps</span><span class="sxs-lookup"><span data-stu-id="2bf09-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="2bf09-146">Nyheder eller ændringer i Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="2bf09-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="2bf09-147">Frigivelsesplaner</span><span class="sxs-lookup"><span data-stu-id="2bf09-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="2bf09-148">Få support til Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="2bf09-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
