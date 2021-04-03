---
title: Tilføje understøttelse af et netværk, der leverer indhold (CDN)
description: Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582713"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="9dad3-103">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="9dad3-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9dad3-104">Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="9dad3-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="9dad3-105">Når du konfigurerer et e-handels-miljø i Dynamics 365 Commerce, kan du konfigurere det til at arbejde sammen med CDN-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9dad3-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="9dad3-106">Dit brugerdefinerede domæne kan aktiveres under klargøringsprocessen for e-handels-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9dad3-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="9dad3-107">Du kan også bruge en serviceanmodning til at konfigurere den, når klargøringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="9dad3-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="9dad3-108">Klargøringsprocessen for e-handelsmiljøet genererer et værtsnavn, der er knyttet til miljøet.</span><span class="sxs-lookup"><span data-stu-id="9dad3-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="9dad3-109">Dette værtsnavn har følgende format, hvor \<*e-commerce-tenant-name*\> er navnet på dit miljø:</span><span class="sxs-lookup"><span data-stu-id="9dad3-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="9dad3-110">&lt;e-handels-lejernavn&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="9dad3-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="9dad3-111">Det værtsnavn eller slutpunkt, der genereres under klargøringsprocessen, understøtter kun et SSL-certifikat (Secure Sockets Layer) for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9dad3-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9dad3-112">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="9dad3-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="9dad3-113">Derfor skal du afslutte SSL for brugerdefinerede domæner i CDN og videresende trafik fra CDN til det værtsnavn eller slutpunkt, som Commerce genererede.</span><span class="sxs-lookup"><span data-stu-id="9dad3-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="9dad3-114">Derudover betjenes *statiske filer* (JavaScript- eller \[CSS\]-filer (overlappende typografiark)) fra Commerce fra det slutpunkt, som Commerce genererede (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9dad3-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="9dad3-115">De statiske filer kan kun cachelagres, hvis det værtsnavn eller slutpunkt, som Commerce genererede, placeres bag CDN'et.</span><span class="sxs-lookup"><span data-stu-id="9dad3-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="9dad3-116">Konfigurer SSL</span><span class="sxs-lookup"><span data-stu-id="9dad3-116">Set up SSL</span></span>

<span data-ttu-id="9dad3-117">For at sikre, at SSL konfigureres, og at statiske filer cachelagres, skal du konfigurere CDN, så det er knyttet til det værtsnavn, som Commerce genererede for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="9dad3-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="9dad3-118">Du skal også cachelagre følgende mønster udelukkende for statiske filer:</span><span class="sxs-lookup"><span data-stu-id="9dad3-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="9dad3-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="9dad3-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="9dad3-120">Når du har klargjort Commerce-miljøet med det tilpassede domæne, der er angivet, eller når du har angivet det brugerdefinerede domæne for miljøet ved hjælp af en serviceanmodning, skal du sørge for, at det brugerdefinerede domæne peger på det værtsnavn eller slutpunkt, som Commerce genererede.</span><span class="sxs-lookup"><span data-stu-id="9dad3-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="9dad3-121">Som tidligere nævnt understøtter det genererede værtsnavn eller slutpunkt kun et SSL-certifikat for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9dad3-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9dad3-122">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="9dad3-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="9dad3-123">CDN-tjenester</span><span class="sxs-lookup"><span data-stu-id="9dad3-123">CDN services</span></span>

<span data-ttu-id="9dad3-124">Der kan bruges en CDN-tjeneste sammen med et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="9dad3-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="9dad3-125">Her er to eksempler:</span><span class="sxs-lookup"><span data-stu-id="9dad3-125">Here are two examples:</span></span>

- <span data-ttu-id="9dad3-126">**Microsoft Azure Front Door Service** – Azure CDN-løsningen.</span><span class="sxs-lookup"><span data-stu-id="9dad3-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="9dad3-127">Du kan finde flere oplysninger om Azure Front Door Service i [Dokumentation til Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/) (artiklen er muligvis på engelsk).</span><span class="sxs-lookup"><span data-stu-id="9dad3-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="9dad3-128">**Akamai Dynamic Site Accelerator** – du kan finde flere oplysninger i [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="9dad3-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="9dad3-129">CDN-opsætning</span><span class="sxs-lookup"><span data-stu-id="9dad3-129">CDN setup</span></span>

<span data-ttu-id="9dad3-130">CDN-konfigurationsprocessen består af følgende generelle trin:</span><span class="sxs-lookup"><span data-stu-id="9dad3-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="9dad3-131">Tilføj en front-end-vært.</span><span class="sxs-lookup"><span data-stu-id="9dad3-131">Add a front-end host.</span></span>
1. <span data-ttu-id="9dad3-132">Konfigurer en back-end-pulje.</span><span class="sxs-lookup"><span data-stu-id="9dad3-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="9dad3-133">Konfigurer regler for routing og cachelagring.</span><span class="sxs-lookup"><span data-stu-id="9dad3-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="9dad3-134">Tilføj en front-end-vært</span><span class="sxs-lookup"><span data-stu-id="9dad3-134">Add a front-end host</span></span>

<span data-ttu-id="9dad3-135">Alle CDN-tjenester kan bruges, men i eksemplet i dette emne bruges Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="9dad3-136">Du kan finde oplysninger om, hvordan du konfigurerer Azure Front Door Service, i [Hurtigstart: Opret en Front Door til et globalt webprogram med høj tilgængelighed](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="9dad3-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="9dad3-137">Konfigurere en back-end-pulje i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="9dad3-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="9dad3-138">Benyt følgende fremgangsmåde for at konfigurere en back-end-pulje i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9dad3-139">Føj **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** til en back-end-pulje som en brugerdefineret vært, der har en tom back-end-værtsheader.</span><span class="sxs-lookup"><span data-stu-id="9dad3-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="9dad3-140">Lad standardværdierne stå under **Belastningsjustering**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="9dad3-141">I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med back-end-værtsnavnet indtastet.</span><span class="sxs-lookup"><span data-stu-id="9dad3-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogboksen Tilføj en back-end-pulje](./media/CDN_BackendPool.png)

<span data-ttu-id="9dad3-143">I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med standardværdier for justering af belastning.</span><span class="sxs-lookup"><span data-stu-id="9dad3-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Dialogboksen Tilføj en back-end-pulje fortsat](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="9dad3-145">Konfigurere regler i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="9dad3-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="9dad3-146">Benyt følgende fremgangsmåde for at konfigurere en ruteplanlægningsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9dad3-147">Tilføj en ruteplanlægningsregel.</span><span class="sxs-lookup"><span data-stu-id="9dad3-147">Add a routing rule.</span></span>
1. <span data-ttu-id="9dad3-148">I feltet **Navn** skal du angive **standard**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="9dad3-149">I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9dad3-150">I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9dad3-151">Under **Mønstre, der skal matche** skal du angive **/\*** i det øverste felt.</span><span class="sxs-lookup"><span data-stu-id="9dad3-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="9dad3-152">Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9dad3-153">I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9dad3-154">I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="9dad3-155">Angiv indstillingen **URL Rewrite** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9dad3-156">Angiv indstillingen **Cachelagring** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="9dad3-157">Benyt følgende fremgangsmåde for at konfigurere en cachelagringsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9dad3-158">Tilføj en cachelagringsregel.</span><span class="sxs-lookup"><span data-stu-id="9dad3-158">Add a caching rule.</span></span>
1. <span data-ttu-id="9dad3-159">I feltet **Navn** skal du angive **statiske filer**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="9dad3-160">I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9dad3-161">I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9dad3-162">Under **Mønstre, der skal matche** skal du angive **/\_msdyn365/\_scnr/\*** i det øverste felt.</span><span class="sxs-lookup"><span data-stu-id="9dad3-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="9dad3-163">Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9dad3-164">I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9dad3-165">I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="9dad3-166">Angiv indstillingen **URL Rewrite** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9dad3-167">Angiv indstillingen **Cachelagring** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="9dad3-168">I feltet **Cachefunktionsmåde for forespørgselsstreng** skal du vælge **Cache hver entydige URL**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="9dad3-169">I feltgruppen **Dynamisk komprimering** skal du vælge indstillingen **Aktiveret**.</span><span class="sxs-lookup"><span data-stu-id="9dad3-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="9dad3-170">Følgende illustration viser dialogboksen **Tilføj en regel** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen Tilføj en regel](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="9dad3-172">Hvis det domæne, du vil bruge, allerede er aktivt og live, kan du oprette en supportanmodning fra **Support**-feltet i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for at få hjælp til de næste trin.</span><span class="sxs-lookup"><span data-stu-id="9dad3-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="9dad3-173">Du kan finde flere oplysninger i [Få support til Finance and Operations-apps eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="9dad3-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="9dad3-174">Hvis dit domæne er nyt og ikke er et eksisterende Live-domæne, kan du føje dit tilpassede domæne til konfigurationen for Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="9dad3-175">Dette gør det muligt for webtrafik at dirigere til dit websted via forekomsten af Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="9dad3-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="9dad3-176">Hvis du vil tilføje det brugerdefinerede domæne (f.eks. `www.fabrikam.com`), skal du konfigurere et vedtaget navn (CNAME) for domænet.</span><span class="sxs-lookup"><span data-stu-id="9dad3-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="9dad3-177">I følgende illustration vises dialogboksen **CNAME-konfiguration** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen CNAME-konfiguration](./media/CNAME_Configuration.png)

<span data-ttu-id="9dad3-179">Du kan bruge Azure Front Door Service til at administrere certifikatet, eller du kan bruge dit eget certifikat til det brugerdefinerede domæne.</span><span class="sxs-lookup"><span data-stu-id="9dad3-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="9dad3-180">I følgende illustration vises dialogboksen **HTTPS for brugerdefineret domæne** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="9dad3-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen HTTPS for brugerdefineret domæne](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="9dad3-182">Detaljerede oplysninger om, hvordan du føjer et brugerdefineret domæne Azure Front Door, finder du under [Føje et brugerdefineret domæne til Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="9dad3-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="9dad3-183">Dit CDN bør nu være korrekt konfigureret, så det kan bruges sammen med Commerce-webstedet.</span><span class="sxs-lookup"><span data-stu-id="9dad3-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dad3-184">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9dad3-184">Additional resources</span></span>

[<span data-ttu-id="9dad3-185">Indstillinger for implementering af netværk for indholdslevering</span><span class="sxs-lookup"><span data-stu-id="9dad3-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
