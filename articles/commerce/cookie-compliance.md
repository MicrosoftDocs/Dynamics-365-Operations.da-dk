---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761315"
---
# <a name="cookie-compliance"></a><span data-ttu-id="23f01-103">Cookie-overholdelse</span><span class="sxs-lookup"><span data-stu-id="23f01-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23f01-104">Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="23f01-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="23f01-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="23f01-105">Overview</span></span>

<span data-ttu-id="23f01-106">Beskyttelse af personlige oplysninger er en vigtig faktor, når der gøres brug af sporingsteknologier, som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="23f01-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="23f01-107">På grund af standarderne for overholdelse af beskyttelse af personlige oplysninger, såsom den generelle forordning om databeskyttelse (GDPR) i Den Europæiske Union (EU), skal retningslinjer for elektronisk beskyttelse af personlige oplysninger tages i betragtning for alle websteder, der er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="23f01-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="23f01-108">Da mange e-Commerce-websteder som standard er tilgængelige globalt, er det vigtigt, at du gennemgår overholdelsesstandarderne for dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="23f01-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="23f01-109">Hvis du vil vide mere om de grundlæggende principper, som Microsoft gør brug af for cookie-overholdelse, skal du besøge [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="23f01-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="23f01-110">På dette websted kan du også få flere oplysninger om overholdelsesområder samt beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="23f01-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="23f01-111">I følgende tabel vises den aktuelle referenceliste over cookies, der er placeret efter Dynamics 365 Commerce-websteder.</span><span class="sxs-lookup"><span data-stu-id="23f01-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="23f01-112">Cookie-navn</span><span class="sxs-lookup"><span data-stu-id="23f01-112">Cookie name</span></span>                               | <span data-ttu-id="23f01-113">Brug</span><span class="sxs-lookup"><span data-stu-id="23f01-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="23f01-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="23f01-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="23f01-115">Gem Microsoft Azure Active Directory-godkendelsescookies (Azure AD) for enkeltlogon (SSO).</span><span class="sxs-lookup"><span data-stu-id="23f01-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="23f01-116">Gemmer krypterede hovedoplysninger om bruger (navn, efternavn, mail).</span><span class="sxs-lookup"><span data-stu-id="23f01-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="23f01-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="23f01-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="23f01-118">Gem indkøbsvogn-id, der bruges til at hente en liste over produkter, der er føjet til forekomsten af indkøbskurv.</span><span class="sxs-lookup"><span data-stu-id="23f01-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="23f01-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="23f01-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="23f01-120">Samtykkesporing af cookie-overholdelse af angivne standarder.</span><span class="sxs-lookup"><span data-stu-id="23f01-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="23f01-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="23f01-121">ai_session</span></span>                                  | <span data-ttu-id="23f01-122">Registrerer, hvor mange sessioner af brugeraktivitet der har omfattet visse sider og funktioner i appen.</span><span class="sxs-lookup"><span data-stu-id="23f01-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="23f01-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="23f01-123">ai_user</span></span>                                     | <span data-ttu-id="23f01-124">Registrerer, hvor mange personer der har brugt appen og dens funktioner.</span><span class="sxs-lookup"><span data-stu-id="23f01-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="23f01-125">Brugerne tælles ved hjælp af anonyme id'er.</span><span class="sxs-lookup"><span data-stu-id="23f01-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="23f01-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="23f01-126">b2cru</span></span>                                       | <span data-ttu-id="23f01-127">Gemmer URL-adresser til omdirigering dynamisk.</span><span class="sxs-lookup"><span data-stu-id="23f01-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="23f01-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="23f01-128">JSESSIONID</span></span>                                  | <span data-ttu-id="23f01-129">Bruges af betalings-connector Adyen til at lagre brugersession.</span><span class="sxs-lookup"><span data-stu-id="23f01-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="23f01-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="23f01-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="23f01-131">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="23f01-131">Authentication</span></span>                                               |
| <span data-ttu-id="23f01-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="23f01-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="23f01-133">Bruges til at vedligeholde anmodningstilstanden.</span><span class="sxs-lookup"><span data-stu-id="23f01-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="23f01-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="23f01-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="23f01-135">CRSF-token (forfalskning af anmodning på tværs af websteder), der bruges til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="23f01-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="23f01-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="23f01-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="23f01-137">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="23f01-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="23f01-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="23f01-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="23f01-139">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="23f01-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="23f01-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="23f01-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="23f01-141">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="23f01-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="23f01-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="23f01-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="23f01-143">Bruges til vedligeholdelse af SSO-sessionen.</span><span class="sxs-lookup"><span data-stu-id="23f01-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="23f01-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="23f01-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="23f01-145">Bruges til sporing af posteringer (antallet af åbne faner, der godkender mod et B2C-websted (Business-to-Consumer)), herunder den aktuelle postering.</span><span class="sxs-lookup"><span data-stu-id="23f01-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="23f01-146">Cookie-samtykke på websted for bruger af et e-handels-websted</span><span class="sxs-lookup"><span data-stu-id="23f01-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="23f01-147">Hvis et e-handels-websteds funktion eller modul bruger en ikke-afgørende cookie, skal en webstedsbrugers samtykke anskaffes, før cookien registreres.</span><span class="sxs-lookup"><span data-stu-id="23f01-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="23f01-148">Hvis brugere af webstederne skal kunne give samtykke på e-handels-webstedet, skal en websteds forfatter tilføje og konfigurere et cookie-samtykkemodul i sidens sidehovedmodul for at sikre, at samtykke efterspørges og modtages.</span><span class="sxs-lookup"><span data-stu-id="23f01-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="23f01-149">Brugersamtykke til webstedet skal gives, før en funktion eller et modul, der bruger en ikke-afgørende cookie, kan gengives på en webside.</span><span class="sxs-lookup"><span data-stu-id="23f01-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23f01-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="23f01-150">Additional resources</span></span>

[<span data-ttu-id="23f01-151">Tilgængelighedsfunktioner og -egenskaber</span><span class="sxs-lookup"><span data-stu-id="23f01-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="23f01-152">Oversigt over overholdelse</span><span class="sxs-lookup"><span data-stu-id="23f01-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="23f01-153">Tilføje en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="23f01-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="23f01-154">Erstatte bruger-id'er, der er knyttet til sporede indholdsændringer</span><span class="sxs-lookup"><span data-stu-id="23f01-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="23f01-155">Cookie-samtykkemodul</span><span class="sxs-lookup"><span data-stu-id="23f01-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="23f01-156">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="23f01-156">Header module</span></span>](author-header-module.md)
