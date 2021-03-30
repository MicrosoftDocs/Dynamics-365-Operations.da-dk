---
title: Framelde webaktivitetshændelser
description: Dette emne forklarer, hvordan du kan give besøgende på dit websted mulighed for at framelde indsamlingen af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210917"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="a984d-103">Fravælge samling af webaktivitetshændelse</span><span class="sxs-lookup"><span data-stu-id="a984d-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="a984d-104">I dette emne forklares det, hvordan du kan lade kunderne framelde indsamling af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a984d-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a984d-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a984d-105">Overview</span></span>

<span data-ttu-id="a984d-106">Dynamics 365 Commerce lad webstedsadministratorer analysere webaktiviteten for brugere af deres e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="a984d-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="a984d-107">På denne måde kan de bedre forstå, hvordan deres websteder bruges, og de kan optimere webstederne, så det er muligt at sikre en forbedret brugeroplevelse og opfylde forretningsmålsætningerne.</span><span class="sxs-lookup"><span data-stu-id="a984d-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="a984d-108">Forskellige måder for administratorer at implementere fravalg på</span><span class="sxs-lookup"><span data-stu-id="a984d-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="a984d-109">Administratorer kan implementere framelding på tre måder.</span><span class="sxs-lookup"><span data-stu-id="a984d-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="a984d-110">Framelding på vegne af brugere</span><span class="sxs-lookup"><span data-stu-id="a984d-110">Opt out on behalf of users</span></span>

<span data-ttu-id="a984d-111">I Kontostyring i Commerce Headquarters (HQ) kan administratorer vælge framelding på brugernes vegne.</span><span class="sxs-lookup"><span data-stu-id="a984d-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="a984d-112">Gå til HQ-klienten, og søg efter og vælg en kunde på siden **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="a984d-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="a984d-113">Gå til siden Kundeoplysninger, og indstil indstillingen **Spor ikke webaktivitet** til **Ja** i sektionen **Beskyttelse af personlige oplysninger** i oversigtspanelet **Detail**.</span><span class="sxs-lookup"><span data-stu-id="a984d-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Indstillinger for beskyttelse af personlige oplysninger](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="a984d-115">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="a984d-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="a984d-116">Modulbaseret framelding</span><span class="sxs-lookup"><span data-stu-id="a984d-116">Module-based opt-out experience</span></span>

<span data-ttu-id="a984d-117">Administratorer kan lade godkendte brugere selv framelde sig indsamlingen af webaktivitetshændelser.</span><span class="sxs-lookup"><span data-stu-id="a984d-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="a984d-118">Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.</span><span class="sxs-lookup"><span data-stu-id="a984d-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="a984d-119">Brugerdefinerede udvidelser</span><span class="sxs-lookup"><span data-stu-id="a984d-119">Custom extensions</span></span>

<span data-ttu-id="a984d-120">Administratorer kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding.</span><span class="sxs-lookup"><span data-stu-id="a984d-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="a984d-121">Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="a984d-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]