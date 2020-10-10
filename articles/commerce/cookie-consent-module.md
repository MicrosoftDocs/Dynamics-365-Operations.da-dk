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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817276"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="de05b-103">Cookie-samtykkemodul</span><span class="sxs-lookup"><span data-stu-id="de05b-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de05b-104">Dette emne omhandler cookie-samtykkemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="de05b-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de05b-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="de05b-105">Overview</span></span>

<span data-ttu-id="de05b-106">Cookie-samtykkemodulet beder brugerne af webstedet om udtrykkeligt at give samtykke til at tillade cookies for enhver funktion eller ethvert modul, der registrerer browsercookies.</span><span class="sxs-lookup"><span data-stu-id="de05b-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="de05b-107">Samtykket kræves, første gang en bruger besøger et websted i en ny browsersession.</span><span class="sxs-lookup"><span data-stu-id="de05b-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="de05b-108">Når samtykke er modtaget, registreres det, og brugeren bliver ikke bedt om samtykke igen.</span><span class="sxs-lookup"><span data-stu-id="de05b-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="de05b-109">Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="de05b-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="de05b-110">Hvis webstedets cookie-samtykke ikke modtages fra en bruger, gengives alle funktioner eller moduler, der kræver cookie-samtykke, ikke på siden.</span><span class="sxs-lookup"><span data-stu-id="de05b-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="de05b-111">F.eks. kræver betalingsmodulet, modulet til social deling og funktionen foretrukken butik alle cookie-samtykke og gengives ikke, hvis webstedets brugersamtykke ikke modtages.</span><span class="sxs-lookup"><span data-stu-id="de05b-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="de05b-112">Der kan konfigureres et cookie-samtykkemodul i sidens sidehovedfragment, så det kan gennemtvinges, når siden indlæses.</span><span class="sxs-lookup"><span data-stu-id="de05b-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="de05b-113">Modulet til cookie-samtykke skal have en klar meddelelse, der oplyser brugeren om cookie-anvendelse på webstedet, og skal indeholde et link til webstedets side om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="de05b-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="de05b-114">I følgende illustration fremhæves et eksempel på en meddelelse om cookie-samtykke med et link til webstedets side med politik om beskyttelse af personlige oplysninger, der vises i sidehovedet på en webside.</span><span class="sxs-lookup"><span data-stu-id="de05b-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="de05b-115">![Eksempel på et modul til cookie-samtykke](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="de05b-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="de05b-116">Egenskaber for cookie-samtykkemodul</span><span class="sxs-lookup"><span data-stu-id="de05b-116">Cookie consent module properties</span></span>

| <span data-ttu-id="de05b-117">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="de05b-117">Property name</span></span>             | <span data-ttu-id="de05b-118">Værdi</span><span class="sxs-lookup"><span data-stu-id="de05b-118">Value</span></span>                 | <span data-ttu-id="de05b-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="de05b-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="de05b-120">RTF</span><span class="sxs-lookup"><span data-stu-id="de05b-120">Rich Text</span></span>                  | <span data-ttu-id="de05b-121">RTF</span><span class="sxs-lookup"><span data-stu-id="de05b-121">Rich Text</span></span> | <span data-ttu-id="de05b-122">Angiver en RTF-besked til webstedsbrugere om, at webstedet bruger browsercookies, og at brugerne skal acceptere brugen af cookies, så webstedet fungerer fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="de05b-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="de05b-123">Links</span><span class="sxs-lookup"><span data-stu-id="de05b-123">Links</span></span> | <span data-ttu-id="de05b-124">URL</span><span class="sxs-lookup"><span data-stu-id="de05b-124">URL</span></span> | <span data-ttu-id="de05b-125">En eller flere links kan føjes til et websteds oplysninger om beskyttelse af personlige oplysninger, der beskriver de typer cookies, der spores på webstedet.</span><span class="sxs-lookup"><span data-stu-id="de05b-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="de05b-126">Tilføje et modul til cookie-samtykke på websider</span><span class="sxs-lookup"><span data-stu-id="de05b-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="de05b-127">Hvis du effektivt vil føje et modul til cookie-samtykke til flere websider, kan det føjes til et delt sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="de05b-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="de05b-128">Når sidehovedet er føjet til alle websiderne, gengives der automatisk en besked om cookie-samtykke, første gang en webstedsbruger navigerer til en webside.</span><span class="sxs-lookup"><span data-stu-id="de05b-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="de05b-129">Yderligere oplysninger om sidehovedfragmenter og moduler finder du i [Sidehovedmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="de05b-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de05b-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="de05b-130">Additional resources</span></span>

[<span data-ttu-id="de05b-131">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="de05b-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="de05b-132">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="de05b-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="de05b-133">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="de05b-133">Cookie compliance</span></span>](cookie-compliance.md)
