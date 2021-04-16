---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796021"
---
# <a name="cookie-compliance"></a><span data-ttu-id="98433-103">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="98433-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98433-104">Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="98433-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="98433-105">Beskyttelse af personlige oplysninger er en vigtig faktor, når der gøres brug af sporingsteknologier, som påvirker e-handelskunder.</span><span class="sxs-lookup"><span data-stu-id="98433-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="98433-106">På grund af standarderne for overholdelse af beskyttelse af personlige oplysninger, såsom den generelle forordning om databeskyttelse (GDPR) i Den Europæiske Union (EU), skal retningslinjer for elektronisk beskyttelse af personlige oplysninger tages i betragtning for alle websteder, der er aktive i dag.</span><span class="sxs-lookup"><span data-stu-id="98433-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="98433-107">Da mange e-Commerce-websteder som standard er tilgængelige globalt, er det vigtigt, at du gennemgår overholdelsesstandarderne for dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="98433-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="98433-108">Hvis du vil vide mere om de grundlæggende principper, som Microsoft gør brug af for cookie-overholdelse, skal du besøge [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="98433-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="98433-109">På dette websted kan du også få flere oplysninger om overholdelsesområder samt beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="98433-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="98433-110">I følgende tabel vises den aktuelle referenceliste over cookies, der er placeret efter Dynamics 365 Commerce-websteder.</span><span class="sxs-lookup"><span data-stu-id="98433-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="98433-111">Cookie-navn</span><span class="sxs-lookup"><span data-stu-id="98433-111">Cookie name</span></span>                               | <span data-ttu-id="98433-112">Brug</span><span class="sxs-lookup"><span data-stu-id="98433-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="98433-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="98433-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="98433-114">Gem Microsoft Azure Active Directory-godkendelsescookies (Azure AD) for enkeltlogon (SSO).</span><span class="sxs-lookup"><span data-stu-id="98433-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="98433-115">Gemmer krypterede hovedoplysninger om bruger (navn, efternavn, mail).</span><span class="sxs-lookup"><span data-stu-id="98433-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="98433-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="98433-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="98433-117">Gem indkøbsvogn-id, der bruges til at hente en liste over produkter, der er føjet til forekomsten af indkøbskurv.</span><span class="sxs-lookup"><span data-stu-id="98433-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="98433-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="98433-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="98433-119">Samtykkesporing af cookie-overholdelse af angivne standarder.</span><span class="sxs-lookup"><span data-stu-id="98433-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="98433-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="98433-120">ai_session</span></span>                                  | <span data-ttu-id="98433-121">Registrerer, hvor mange sessioner af brugeraktivitet der har omfattet visse sider og funktioner i appen.</span><span class="sxs-lookup"><span data-stu-id="98433-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="98433-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="98433-122">ai_user</span></span>                                     | <span data-ttu-id="98433-123">Registrerer, hvor mange personer der har brugt appen og dens funktioner.</span><span class="sxs-lookup"><span data-stu-id="98433-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="98433-124">Brugerne tælles ved hjælp af anonyme id'er.</span><span class="sxs-lookup"><span data-stu-id="98433-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="98433-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="98433-125">b2cru</span></span>                                       | <span data-ttu-id="98433-126">Gemmer URL-adresser til omdirigering dynamisk.</span><span class="sxs-lookup"><span data-stu-id="98433-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="98433-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="98433-127">JSESSIONID</span></span>                                  | <span data-ttu-id="98433-128">Bruges af betalings-connector Adyen til at lagre brugersession.</span><span class="sxs-lookup"><span data-stu-id="98433-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="98433-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="98433-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="98433-130">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="98433-130">Authentication</span></span>                                               |
| <span data-ttu-id="98433-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="98433-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="98433-132">Bruges til at vedligeholde anmodningstilstanden.</span><span class="sxs-lookup"><span data-stu-id="98433-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="98433-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="98433-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="98433-134">CRSF-token (forfalskning af anmodning på tværs af websteder), der bruges til beskyttelse fra CRSF.</span><span class="sxs-lookup"><span data-stu-id="98433-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="98433-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="98433-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="98433-136">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="98433-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="98433-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="98433-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="98433-138">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="98433-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="98433-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="98433-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="98433-140">Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver.</span><span class="sxs-lookup"><span data-stu-id="98433-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="98433-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="98433-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="98433-142">Bruges til vedligeholdelse af SSO-sessionen.</span><span class="sxs-lookup"><span data-stu-id="98433-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="98433-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="98433-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="98433-144">Bruges til sporing af posteringer (antallet af åbne faner, der godkender mod et B2C-websted (Business-to-Consumer)), herunder den aktuelle postering.</span><span class="sxs-lookup"><span data-stu-id="98433-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="98433-145">Cookie-samtykke på websted for bruger af et e-handels-websted</span><span class="sxs-lookup"><span data-stu-id="98433-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="98433-146">Hvis et e-handels-websteds funktion eller modul bruger en ikke-afgørende cookie, skal en webstedsbrugers samtykke anskaffes, før cookien registreres.</span><span class="sxs-lookup"><span data-stu-id="98433-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="98433-147">Hvis brugere af webstederne skal kunne give samtykke på e-handels-webstedet, skal en websteds forfatter tilføje og konfigurere et cookie-samtykkemodul i sidens sidehovedmodul for at sikre, at samtykke efterspørges og modtages.</span><span class="sxs-lookup"><span data-stu-id="98433-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="98433-148">Brugersamtykke til webstedet skal gives, før en funktion eller et modul, der bruger en ikke-afgørende cookie, kan gengives på en webside.</span><span class="sxs-lookup"><span data-stu-id="98433-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98433-149">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="98433-149">Additional resources</span></span>

[<span data-ttu-id="98433-150">Tilgængelighedsfunktioner og -egenskaber</span><span class="sxs-lookup"><span data-stu-id="98433-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="98433-151">Oversigt over overholdelse</span><span class="sxs-lookup"><span data-stu-id="98433-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="98433-152">Tilføje en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="98433-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="98433-153">Erstatte bruger-id'er, der er knyttet til sporede indholdsændringer</span><span class="sxs-lookup"><span data-stu-id="98433-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="98433-154">Cookie-samtykkemodul</span><span class="sxs-lookup"><span data-stu-id="98433-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="98433-155">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="98433-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
