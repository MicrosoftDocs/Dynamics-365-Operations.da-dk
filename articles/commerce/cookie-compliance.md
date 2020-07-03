---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446907"
---
# <a name="cookie-compliance"></a><span data-ttu-id="2dea1-103">Cookie-overholdelse</span><span class="sxs-lookup"><span data-stu-id="2dea1-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2dea1-104">Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2dea1-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2dea1-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="2dea1-105">Overview</span></span>

<span data-ttu-id="2dea1-106">Beskyttelse af personlige oplysninger er en vigtig faktor, når der gøres brug af sporingsteknologier, som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="2dea1-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="2dea1-107">På grund af standarderne for overholdelse af beskyttelse af personlige oplysninger, såsom den generelle forordning om databeskyttelse (GDPR) i Den Europæiske Union (EU), skal retningslinjer for elektronisk beskyttelse af personlige oplysninger tages i betragtning for alle websteder, der er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="2dea1-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="2dea1-108">Da mange e-Commerce-websteder som standard er tilgængelige globalt, er det vigtigt, at du gennemgår overholdelsesstandarderne for dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="2dea1-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="2dea1-109">Hvis du vil vide mere om de grundlæggende principper, som Microsoft gør brug af for cookie-overholdelse, skal du besøge [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="2dea1-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="2dea1-110">På dette websted kan du også få flere oplysninger om overholdelsesområder samt beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2dea1-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="2dea1-111">I følgende tabel vises den aktuelle referenceliste over cookies, der er placeret efter Dynamics 365 Commerce-websteder.</span><span class="sxs-lookup"><span data-stu-id="2dea1-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="2dea1-112">Cookie-navn</span><span class="sxs-lookup"><span data-stu-id="2dea1-112">Cookie name</span></span>                               | <span data-ttu-id="2dea1-113">Brug</span><span class="sxs-lookup"><span data-stu-id="2dea1-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="2dea1-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="2dea1-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="2dea1-115">Gem Microsoft Azure Active Directory-godkendelsescookies (Azure AD) for enkeltlogon (SSO).</span><span class="sxs-lookup"><span data-stu-id="2dea1-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="2dea1-116">Gemmer krypterede hovedoplysninger om bruger (navn, efternavn, mail).</span><span class="sxs-lookup"><span data-stu-id="2dea1-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="2dea1-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="2dea1-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="2dea1-118">Gem indkøbsvogn-id, der bruges til at hente en liste over produkter, der er føjet til forekomsten af indkøbskurv.</span><span class="sxs-lookup"><span data-stu-id="2dea1-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="2dea1-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="2dea1-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="2dea1-120">Samtykkesporing af cookie-overholdelse af angivne standarder.</span><span class="sxs-lookup"><span data-stu-id="2dea1-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="2dea1-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="2dea1-121">ai_session</span></span>                                  | <span data-ttu-id="2dea1-122">Registrerer, hvor mange sessioner af brugeraktivitet der har omfattet visse sider og funktioner i appen.</span><span class="sxs-lookup"><span data-stu-id="2dea1-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="2dea1-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="2dea1-123">ai_user</span></span>                                     | <span data-ttu-id="2dea1-124">Registrerer, hvor mange personer der har brugt appen og dens funktioner.</span><span class="sxs-lookup"><span data-stu-id="2dea1-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="2dea1-125">Brugerne tælles ved hjælp af anonyme id'er.</span><span class="sxs-lookup"><span data-stu-id="2dea1-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="2dea1-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="2dea1-126">b2cru</span></span>                                       | <span data-ttu-id="2dea1-127">Gemmer URL-adresser til omdirigering dynamisk.</span><span class="sxs-lookup"><span data-stu-id="2dea1-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="2dea1-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="2dea1-128">JSESSIONID</span></span>                                  | <span data-ttu-id="2dea1-129">Bruges af betalings-connector Adyen til at lagre brugersession.</span><span class="sxs-lookup"><span data-stu-id="2dea1-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="2dea1-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="2dea1-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="2dea1-131">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="2dea1-131">Authentication</span></span>                                               |
| <span data-ttu-id="2dea1-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="2dea1-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="2dea1-133">Bruges til at vedligeholde anmodningstilstanden.</span><span class="sxs-lookup"><span data-stu-id="2dea1-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="2dea1-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="2dea1-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="2dea1-135">CRSF-token (forfalskning af anmodning på tværs af websteder), der bruges til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="2dea1-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="2dea1-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="2dea1-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="2dea1-137">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="2dea1-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="2dea1-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="2dea1-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="2dea1-139">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="2dea1-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="2dea1-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="2dea1-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="2dea1-141">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="2dea1-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="2dea1-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="2dea1-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="2dea1-143">Bruges til vedligeholdelse af SSO-sessionen.</span><span class="sxs-lookup"><span data-stu-id="2dea1-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="2dea1-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="2dea1-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="2dea1-145">Bruges til sporing af posteringer (antallet af åbne faner, der godkender mod et B2C-websted (Business-to-Consumer)), herunder den aktuelle postering.</span><span class="sxs-lookup"><span data-stu-id="2dea1-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2dea1-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2dea1-146">Additional resources</span></span>

[<span data-ttu-id="2dea1-147">Tilgængelighedsfunktioner og -egenskaber</span><span class="sxs-lookup"><span data-stu-id="2dea1-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="2dea1-148">Oversigt over overholdelse</span><span class="sxs-lookup"><span data-stu-id="2dea1-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="2dea1-149">Tilføje en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="2dea1-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="2dea1-150">Erstatte bruger-id'er, der er tilknyttet sporede indholdsændringer</span><span class="sxs-lookup"><span data-stu-id="2dea1-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
