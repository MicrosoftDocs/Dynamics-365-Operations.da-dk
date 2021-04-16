---
title: Framelde webaktivitetshændelser
description: Dette emne forklarer, hvordan du kan give besøgende på dit websted mulighed for at framelde indsamlingen af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791551"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="de899-103">Fravælge samling af webaktivitetshændelse</span><span class="sxs-lookup"><span data-stu-id="de899-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="de899-104">I dette emne forklares det, hvordan du kan lade kunderne framelde indsamling af webaktivitetshændelser i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="de899-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="de899-105">Dynamics 365 Commerce lad webstedsadministratorer analysere webaktiviteten for brugere af deres e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="de899-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="de899-106">På denne måde kan de bedre forstå, hvordan deres websteder bruges, og de kan optimere webstederne, så det er muligt at sikre en forbedret brugeroplevelse og opfylde forretningsmålsætningerne.</span><span class="sxs-lookup"><span data-stu-id="de899-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="de899-107">Forskellige måder for administratorer at implementere fravalg på</span><span class="sxs-lookup"><span data-stu-id="de899-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="de899-108">Administratorer kan implementere framelding på tre måder.</span><span class="sxs-lookup"><span data-stu-id="de899-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="de899-109">Framelding på vegne af brugere</span><span class="sxs-lookup"><span data-stu-id="de899-109">Opt out on behalf of users</span></span>

<span data-ttu-id="de899-110">I Kontostyring i Commerce Headquarters (HQ) kan administratorer vælge framelding på brugernes vegne.</span><span class="sxs-lookup"><span data-stu-id="de899-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="de899-111">Gå til HQ-klienten, og søg efter og vælg en kunde på siden **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="de899-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="de899-112">Gå til siden Kundeoplysninger, og indstil indstillingen **Spor ikke webaktivitet** til **Ja** i sektionen **Beskyttelse af personlige oplysninger** i oversigtspanelet **Detail**.</span><span class="sxs-lookup"><span data-stu-id="de899-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Indstillinger for beskyttelse af personlige oplysninger](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="de899-114">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="de899-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="de899-115">Modulbaseret framelding</span><span class="sxs-lookup"><span data-stu-id="de899-115">Module-based opt-out experience</span></span>

<span data-ttu-id="de899-116">Administratorer kan lade godkendte brugere selv framelde sig indsamlingen af webaktivitetshændelser.</span><span class="sxs-lookup"><span data-stu-id="de899-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="de899-117">Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.</span><span class="sxs-lookup"><span data-stu-id="de899-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="de899-118">Brugerdefinerede udvidelser</span><span class="sxs-lookup"><span data-stu-id="de899-118">Custom extensions</span></span>

<span data-ttu-id="de899-119">Administratorer kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding.</span><span class="sxs-lookup"><span data-stu-id="de899-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="de899-120">Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="de899-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
