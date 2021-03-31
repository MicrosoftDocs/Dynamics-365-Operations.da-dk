---
title: Cookie-samtykkemodul
description: Dette emne omhandler cookie-samtykkemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213932"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="62753-103">Modul til cookie-samtykke</span><span class="sxs-lookup"><span data-stu-id="62753-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62753-104">Dette emne omhandler cookie-samtykkemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62753-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="62753-105">Cookie-samtykkemodulet beder brugerne af webstedet om udtrykkeligt at give samtykke til at tillade cookies for enhver funktion eller ethvert modul, der registrerer browsercookies.</span><span class="sxs-lookup"><span data-stu-id="62753-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="62753-106">Samtykket kræves, første gang en bruger besøger et websted i en ny browsersession.</span><span class="sxs-lookup"><span data-stu-id="62753-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="62753-107">Når samtykke er modtaget, registreres det, og brugeren bliver ikke bedt om samtykke igen.</span><span class="sxs-lookup"><span data-stu-id="62753-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="62753-108">Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="62753-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="62753-109">Hvis webstedets cookie-samtykke ikke modtages fra en bruger, gengives alle funktioner eller moduler, der kræver cookie-samtykke, ikke på siden.</span><span class="sxs-lookup"><span data-stu-id="62753-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="62753-110">F.eks. kræver betalingsmodulet, modulet til social deling og funktionen foretrukken butik alle cookie-samtykke og gengives ikke, hvis webstedets brugersamtykke ikke modtages.</span><span class="sxs-lookup"><span data-stu-id="62753-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="62753-111">Der kan konfigureres et cookie-samtykkemodul i sidens sidehovedfragment, så det kan gennemtvinges, når siden indlæses.</span><span class="sxs-lookup"><span data-stu-id="62753-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="62753-112">Modulet til cookie-samtykke skal have en klar meddelelse, der oplyser brugeren om cookie-anvendelse på webstedet, og skal indeholde et link til webstedets side om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="62753-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="62753-113">I følgende illustration fremhæves et eksempel på en meddelelse om cookie-samtykke med et link til webstedets side med politik om beskyttelse af personlige oplysninger, der vises i sidehovedet på en webside.</span><span class="sxs-lookup"><span data-stu-id="62753-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="62753-114">![Eksempel på et modul til cookie-samtykke](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="62753-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="62753-115">Egenskaber for cookie-samtykkemodul</span><span class="sxs-lookup"><span data-stu-id="62753-115">Cookie consent module properties</span></span>

| <span data-ttu-id="62753-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="62753-116">Property name</span></span>             | <span data-ttu-id="62753-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="62753-117">Value</span></span>                 | <span data-ttu-id="62753-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="62753-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="62753-119">RTF</span><span class="sxs-lookup"><span data-stu-id="62753-119">Rich Text</span></span>                  | <span data-ttu-id="62753-120">RTF</span><span class="sxs-lookup"><span data-stu-id="62753-120">Rich Text</span></span> | <span data-ttu-id="62753-121">Angiver en RTF-besked til webstedsbrugere om, at webstedet bruger browsercookies, og at brugerne skal acceptere brugen af cookies, så webstedet fungerer fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="62753-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="62753-122">Links</span><span class="sxs-lookup"><span data-stu-id="62753-122">Links</span></span> | <span data-ttu-id="62753-123">URL</span><span class="sxs-lookup"><span data-stu-id="62753-123">URL</span></span> | <span data-ttu-id="62753-124">En eller flere links kan føjes til et websteds oplysninger om beskyttelse af personlige oplysninger, der beskriver de typer cookies, der spores på webstedet.</span><span class="sxs-lookup"><span data-stu-id="62753-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="62753-125">Tilføje et modul til cookie-samtykke på websider</span><span class="sxs-lookup"><span data-stu-id="62753-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="62753-126">Hvis du effektivt vil føje et modul til cookie-samtykke til flere websider, kan det føjes til et delt sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="62753-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="62753-127">Når sidehovedet er føjet til alle websiderne, gengives der automatisk en besked om cookie-samtykke, første gang en webstedsbruger navigerer til en webside.</span><span class="sxs-lookup"><span data-stu-id="62753-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="62753-128">Yderligere oplysninger om sidehovedfragmenter og moduler finder du i [Sidehovedmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="62753-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62753-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="62753-129">Additional resources</span></span>

[<span data-ttu-id="62753-130">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="62753-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="62753-131">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="62753-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="62753-132">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="62753-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]