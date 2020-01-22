---
title: Tilføje understøttelse af et netværk, der leverer indhold (CDN)
description: Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945622"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="f10a0-103">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="f10a0-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f10a0-104">Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="f10a0-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="f10a0-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f10a0-105">Overview</span></span>

<span data-ttu-id="f10a0-106">Når du konfigurerer et e-handels-miljø i Dynamics 365 Commerce, kan du konfigurere det til at arbejde sammen med CDN-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="f10a0-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="f10a0-107">Dit brugerdefinerede domæne kan aktiveres under klargøringsprocessen for e-handels-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f10a0-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="f10a0-108">Du kan også bruge en serviceanmodning til at konfigurere den, når klargøringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="f10a0-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="f10a0-109">Klargøringsprocessen for e-handels miljøet genererer et værtsnavn, der er knyttet til miljøet.</span><span class="sxs-lookup"><span data-stu-id="f10a0-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="f10a0-110">Dette værtsnavn har følgende format, hvor *e-handels-lejernavn* er navnet på dit miljø:</span><span class="sxs-lookup"><span data-stu-id="f10a0-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="f10a0-111">&lt;e-handels-lejernavn&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="f10a0-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="f10a0-112">Det værtsnavn eller slutpunkt, der genereres under klargøringsprocessen, understøtter kun et SSL-certifikat (Secure Sockets Layer) for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="f10a0-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f10a0-113">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="f10a0-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="f10a0-114">Derfor skal du afslutte SSL for brugerdefinerede domæner i CDN og videresende trafik fra CDN til det værtsnavn eller slutpunkt, som Commerce genererede.</span><span class="sxs-lookup"><span data-stu-id="f10a0-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="f10a0-115">Derudover betjenes *statiske filer* (JavaScript- eller \[CSS\]-filer (overlappende typografiark)) fra Commerce fra det slutpunkt, som Commerce genererede (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="f10a0-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="f10a0-116">De statiske filer kan kun cachelagres, hvis det værtsnavn eller slutpunkt, som Commerce genererede, placeres bag CDN'et.</span><span class="sxs-lookup"><span data-stu-id="f10a0-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="f10a0-117">Konfigurer SSL</span><span class="sxs-lookup"><span data-stu-id="f10a0-117">Set up SSL</span></span>

<span data-ttu-id="f10a0-118">For at sikre, at SSL konfigureres, og at statiske filer cachelagres, skal du konfigurere CDN, så det er knyttet til det værtsnavn, som Commerce genererede for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="f10a0-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="f10a0-119">Du skal også cachelagre følgende mønster udelukkende for statiske filer:</span><span class="sxs-lookup"><span data-stu-id="f10a0-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="f10a0-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="f10a0-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="f10a0-121">Når du har klargjort Commerce-miljøet med det tilpassede domæne, der er angivet, eller når du har angivet det brugerdefinerede domæne for miljøet ved hjælp af en serviceanmodning, skal du sørge for, at det brugerdefinerede domæne peger på det værtsnavn eller slutpunkt, som Commerce genererede.</span><span class="sxs-lookup"><span data-stu-id="f10a0-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="f10a0-122">Som tidligere nævnt understøtter det genererede værtsnavn eller slutpunkt kun et SSL-certifikat for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="f10a0-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f10a0-123">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="f10a0-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="f10a0-124">CDN-tjenester</span><span class="sxs-lookup"><span data-stu-id="f10a0-124">CDN services</span></span>

<span data-ttu-id="f10a0-125">Der kan bruges en CDN-tjeneste sammen med et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="f10a0-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="f10a0-126">Her er to eksempler:</span><span class="sxs-lookup"><span data-stu-id="f10a0-126">Here are two examples:</span></span>

- <span data-ttu-id="f10a0-127">**Microsoft Azure Front Door Service** – Azure CDN-løsningen.</span><span class="sxs-lookup"><span data-stu-id="f10a0-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="f10a0-128">Du kan finde flere oplysninger om Azure Front Door Service i [Dokumentation til Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/) (artiklen er muligvis på engelsk).</span><span class="sxs-lookup"><span data-stu-id="f10a0-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="f10a0-129">**Akamai Dynamic Site Accelerator** – du kan finde flere oplysninger i [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="f10a0-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="f10a0-130">CDN-opsætning</span><span class="sxs-lookup"><span data-stu-id="f10a0-130">CDN setup</span></span>

<span data-ttu-id="f10a0-131">CDN-konfigurationsprocessen består af følgende generelle trin:</span><span class="sxs-lookup"><span data-stu-id="f10a0-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="f10a0-132">Tilføj en front-end-vært.</span><span class="sxs-lookup"><span data-stu-id="f10a0-132">Add a front-end host.</span></span>
1. <span data-ttu-id="f10a0-133">Konfigurer en back-end-pulje.</span><span class="sxs-lookup"><span data-stu-id="f10a0-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="f10a0-134">Konfigurer regler for routing og cachelagring.</span><span class="sxs-lookup"><span data-stu-id="f10a0-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="f10a0-135">Tilføj en front-end-vært</span><span class="sxs-lookup"><span data-stu-id="f10a0-135">Add a front-end host</span></span>

<span data-ttu-id="f10a0-136">Alle CDN-tjenester kan bruges, men i eksemplet i dette emne bruges Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="f10a0-137">Du kan finde oplysninger om, hvordan du konfigurerer Azure Front Door Service, i [Hurtigstart: Opret en Front Door til et globalt webprogram med høj tilgængelighed](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="f10a0-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="f10a0-138">Konfigurere en back-end-pulje i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="f10a0-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="f10a0-139">Benyt følgende fremgangsmåde for at konfigurere en back-end-pulje i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f10a0-140">Føj **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** til en back-end-pulje som en brugerdefineret vært, der har en tom back-end-værtsheader.</span><span class="sxs-lookup"><span data-stu-id="f10a0-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="f10a0-141">Under **Tilstandsundersøgelser** i feltet **Sti** skal du angive **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="f10a0-142">I feltet **Intervaller (sekunder)** skal du indtaste **255**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="f10a0-143">Lad standardværdierne stå under **Belastningsjustering**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="f10a0-144">I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen Tilføj en back-end-pulje](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="f10a0-146">Konfigurere regler i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="f10a0-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="f10a0-147">Benyt følgende fremgangsmåde for at konfigurere en ruteplanlægningsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f10a0-148">Tilføj en ruteplanlægningsregel.</span><span class="sxs-lookup"><span data-stu-id="f10a0-148">Add a routing rule.</span></span>
1. <span data-ttu-id="f10a0-149">I feltet **Navn** skal du angive **standard**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="f10a0-150">I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="f10a0-151">I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="f10a0-152">Under **Mønstre, der skal matche** skal du angive **/\*** i det øverste felt.</span><span class="sxs-lookup"><span data-stu-id="f10a0-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="f10a0-153">Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="f10a0-154">I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="f10a0-155">I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="f10a0-156">Angiv indstillingen **URL Rewrite** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="f10a0-157">Angiv indstillingen **Cachelagring** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="f10a0-158">Benyt følgende fremgangsmåde for at konfigurere en cachelagringsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f10a0-159">Tilføj en cachelagringsregel.</span><span class="sxs-lookup"><span data-stu-id="f10a0-159">Add a caching rule.</span></span>
1. <span data-ttu-id="f10a0-160">I feltet **Navn** skal du angive **statiske filer**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="f10a0-161">I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="f10a0-162">I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="f10a0-163">Under **Mønstre, der skal matche** skal du angive **/\_msdyn365/\_scnr/\*** i det øverste felt.</span><span class="sxs-lookup"><span data-stu-id="f10a0-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="f10a0-164">Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="f10a0-165">I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="f10a0-166">I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="f10a0-167">Angiv indstillingen **URL Rewrite** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="f10a0-168">Angiv indstillingen **Cachelagring** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="f10a0-169">I feltet **Cachefunktionsmåde for forespørgselsstreng** skal du vælge **Cache hver entydige URL**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="f10a0-170">I feltgruppen **Dynamisk komprimering** skal du vælge indstillingen **Aktiveret**.</span><span class="sxs-lookup"><span data-stu-id="f10a0-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="f10a0-171">Følgende illustration viser dialogboksen **Tilføj en regel** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen Tilføj en regel](./media/CDN_CachingRule.png)

<span data-ttu-id="f10a0-173">Når denne indledende konfiguration er installeret, skal du føje det brugerdefinerede domæne til konfigurationen for Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="f10a0-174">Hvis du vil tilføje det brugerdefinerede domæne (f.eks. `www.fabrikam.com`), skal du konfigurere et vedtaget navn (CNAME) for domænet.</span><span class="sxs-lookup"><span data-stu-id="f10a0-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="f10a0-175">I følgende illustration vises dialogboksen **CNAME-konfiguration** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen CNAME-konfiguration](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="f10a0-177">Hvis det domæne, du vil bruge, allerede er aktivt og live, skal du kontakte support for at aktivere dette domæne med Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="f10a0-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="f10a0-178">Du kan bruge Azure Front Door Service til at administrere certifikatet, eller du kan bruge dit eget certifikat til det brugerdefinerede domæne.</span><span class="sxs-lookup"><span data-stu-id="f10a0-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="f10a0-179">I følgende illustration vises dialogboksen **HTTPS for brugerdefineret domæne** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f10a0-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen HTTPS for brugerdefineret domæne](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="f10a0-181">Dit CDN bør nu være korrekt konfigureret, så det kan bruges sammen med Commerce-webstedet.</span><span class="sxs-lookup"><span data-stu-id="f10a0-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f10a0-182">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f10a0-182">Additional resources</span></span>

[<span data-ttu-id="f10a0-183">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="f10a0-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f10a0-184">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="f10a0-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f10a0-185">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="f10a0-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f10a0-186">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="f10a0-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f10a0-187">Administrer robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="f10a0-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f10a0-188">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="f10a0-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f10a0-189">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="f10a0-189">Enable location-based store detection</span></span>](enable-store-detection.md)
