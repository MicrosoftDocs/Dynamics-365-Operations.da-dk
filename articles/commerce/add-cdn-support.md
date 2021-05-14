---
title: Tilføje understøttelse af et netværk, der leverer indhold (CDN)
description: Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.
author: brianshook
ms.date: 03/17/2021
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
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936824"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="fccff-103">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="fccff-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fccff-104">Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="fccff-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="fccff-105">Når du konfigurerer et e-handels-miljø i Dynamics 365 Commerce, kan du konfigurere det til at arbejde sammen med CDN-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="fccff-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="fccff-106">Dit brugerdefinerede domæne kan aktiveres under klargøringsprocessen for e-handels-miljøet.</span><span class="sxs-lookup"><span data-stu-id="fccff-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="fccff-107">Du kan også bruge en serviceanmodning til at konfigurere den, når klargøringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="fccff-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="fccff-108">Klargøringsprocessen for e-handelsmiljøet genererer et værtsnavn, der er knyttet til miljøet.</span><span class="sxs-lookup"><span data-stu-id="fccff-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="fccff-109">Dette værtsnavn har følgende format, hvor \<*e-commerce-tenant-name*\> er navnet på dit miljø:</span><span class="sxs-lookup"><span data-stu-id="fccff-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="fccff-110">&lt;e-handels-lejernavn&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="fccff-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="fccff-111">Det værtsnavn eller slutpunkt, der genereres under klargøringsprocessen, understøtter kun et SSL-certifikat (Secure Sockets Layer) for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="fccff-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="fccff-112">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="fccff-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="fccff-113">Derfor skal du afslutte SSL for brugerdefinerede domæner i CDN og videresende trafik fra CDN til det værtsnavn eller slutpunkt, som Commerce genererede.</span><span class="sxs-lookup"><span data-stu-id="fccff-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="fccff-114">Derudover betjenes *statiske filer* (JavaScript- eller \[CSS\]-filer (overlappende typografiark)) fra Commerce fra det slutpunkt, som Commerce genererede (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="fccff-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="fccff-115">De statiske filer kan kun cachelagres, hvis det værtsnavn eller slutpunkt, som Commerce genererede, placeres bag CDN'et.</span><span class="sxs-lookup"><span data-stu-id="fccff-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="fccff-116">Konfigurer SSL</span><span class="sxs-lookup"><span data-stu-id="fccff-116">Set up SSL</span></span>

<span data-ttu-id="fccff-117">Når du har klargjort Commerce-miljøet med det brugerdefinerede domæne, der er leveret, eller når du har angivet det brugerdefinerede domæne for dit miljø ved hjælp af en serviceanmodning, skal du samarbejde med Commerce-onboardingteamet omkring planlægning af DNS.</span><span class="sxs-lookup"><span data-stu-id="fccff-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="fccff-118">Som tidligere nævnt understøtter det genererede værtsnavn eller slutpunkt kun et SSL-certifikat for \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="fccff-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="fccff-119">Det understøtter ikke SSL for brugerdefinerede domæner.</span><span class="sxs-lookup"><span data-stu-id="fccff-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="fccff-120">CDN-tjenester</span><span class="sxs-lookup"><span data-stu-id="fccff-120">CDN services</span></span>

<span data-ttu-id="fccff-121">Der kan bruges en CDN-tjeneste sammen med et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="fccff-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="fccff-122">Her er to eksempler:</span><span class="sxs-lookup"><span data-stu-id="fccff-122">Here are two examples:</span></span>

- <span data-ttu-id="fccff-123">**Microsoft Azure Front Door Service** – Azure CDN-løsningen.</span><span class="sxs-lookup"><span data-stu-id="fccff-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="fccff-124">Du kan finde flere oplysninger om Azure Front Door Service i [Dokumentation til Azure Front Door Service](/azure/frontdoor/) (artiklen er muligvis på engelsk).</span><span class="sxs-lookup"><span data-stu-id="fccff-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="fccff-125">**Akamai Dynamic Site Accelerator** – du kan finde flere oplysninger i [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="fccff-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="fccff-126">CDN-opsætning</span><span class="sxs-lookup"><span data-stu-id="fccff-126">CDN setup</span></span>

<span data-ttu-id="fccff-127">CDN-konfigurationsprocessen består af følgende generelle trin:</span><span class="sxs-lookup"><span data-stu-id="fccff-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="fccff-128">Tilføj en front-end-vært.</span><span class="sxs-lookup"><span data-stu-id="fccff-128">Add a front-end host.</span></span>
1. <span data-ttu-id="fccff-129">Konfigurer en back-end-pulje.</span><span class="sxs-lookup"><span data-stu-id="fccff-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="fccff-130">Konfigurer regler for ruteplanlægning.</span><span class="sxs-lookup"><span data-stu-id="fccff-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="fccff-131">Tilføj en front-end-vært</span><span class="sxs-lookup"><span data-stu-id="fccff-131">Add a front-end host</span></span>

<span data-ttu-id="fccff-132">Alle CDN-tjenester kan bruges, men i eksemplet i dette emne bruges Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="fccff-133">Du kan finde oplysninger om, hvordan du konfigurerer Azure Front Door Service, i [Hurtigstart: Opret en Front Door til et globalt webprogram med høj tilgængelighed](/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="fccff-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="fccff-134">Konfigurere en back-end-pulje i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="fccff-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="fccff-135">Benyt følgende fremgangsmåde for at konfigurere en back-end-pulje i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="fccff-136">Føj **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** til en backend-pulje som en brugerdefineret vært, der har et backend-værtshoved, der er det samme som **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="fccff-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="fccff-137">Lad standardværdierne stå under **Belastningsjustering**.</span><span class="sxs-lookup"><span data-stu-id="fccff-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="fccff-138">Deaktiver sundhedstjek for backend-puljen.</span><span class="sxs-lookup"><span data-stu-id="fccff-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="fccff-139">I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med back-end-værtsnavnet indtastet.</span><span class="sxs-lookup"><span data-stu-id="fccff-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogboksen Tilføj en back-end-pulje](./media/CDN_BackendPool.png)

<span data-ttu-id="fccff-141">I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med standardværdier for justering af belastning.</span><span class="sxs-lookup"><span data-stu-id="fccff-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Dialogboksen Tilføj en back-end-pulje fortsat](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="fccff-143">Sørg for at deaktivere **Tilstandsundersøgelser**, når du konfigurerer din egen Azure Front Door Service til Commerce.</span><span class="sxs-lookup"><span data-stu-id="fccff-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="fccff-144">Konfigurere regler i Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="fccff-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="fccff-145">Benyt følgende fremgangsmåde for at konfigurere en ruteplanlægningsregel i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="fccff-146">Tilføj en ruteplanlægningsregel.</span><span class="sxs-lookup"><span data-stu-id="fccff-146">Add a routing rule.</span></span>
1. <span data-ttu-id="fccff-147">I feltet **Navn** skal du angive **standard**.</span><span class="sxs-lookup"><span data-stu-id="fccff-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="fccff-148">I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="fccff-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="fccff-149">I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="fccff-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="fccff-150">Under **Mønstre, der skal matche** skal du angive **/\*** i det øverste felt.</span><span class="sxs-lookup"><span data-stu-id="fccff-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="fccff-151">Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="fccff-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="fccff-152">I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.</span><span class="sxs-lookup"><span data-stu-id="fccff-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="fccff-153">I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.</span><span class="sxs-lookup"><span data-stu-id="fccff-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="fccff-154">Angiv indstillingen **URL Rewrite** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="fccff-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="fccff-155">Angiv indstillingen **Cachelagring** til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="fccff-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="fccff-156">Hvis det domæne, du vil bruge, allerede er aktivt og live, kan du oprette en supportanmodning fra **Support**-feltet i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for at få hjælp til de næste trin.</span><span class="sxs-lookup"><span data-stu-id="fccff-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="fccff-157">Du kan finde flere oplysninger i [Få support til Finance and Operations-apps eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="fccff-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="fccff-158">Hvis dit domæne er nyt og ikke er et eksisterende Live-domæne, kan du føje dit tilpassede domæne til konfigurationen for Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="fccff-159">Dette gør det muligt for webtrafik at dirigere til dit websted via forekomsten af Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="fccff-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="fccff-160">Hvis du vil tilføje det brugerdefinerede domæne (f.eks. `www.fabrikam.com`), skal du konfigurere et vedtaget navn (CNAME) for domænet.</span><span class="sxs-lookup"><span data-stu-id="fccff-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="fccff-161">I følgende illustration vises dialogboksen **CNAME-konfiguration** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen CNAME-konfiguration](./media/CNAME_Configuration.png)

<span data-ttu-id="fccff-163">Du kan bruge Azure Front Door Service til at administrere certifikatet, eller du kan bruge dit eget certifikat til det brugerdefinerede domæne.</span><span class="sxs-lookup"><span data-stu-id="fccff-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="fccff-164">I følgende illustration vises dialogboksen **HTTPS for brugerdefineret domæne** i Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="fccff-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogboksen HTTPS for brugerdefineret domæne](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="fccff-166">Detaljerede oplysninger om, hvordan du føjer et brugerdefineret domæne Azure Front Door, finder du under [Føje et brugerdefineret domæne til Front Door](/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="fccff-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="fccff-167">Dit CDN bør nu være korrekt konfigureret, så det kan bruges sammen med Commerce-webstedet.</span><span class="sxs-lookup"><span data-stu-id="fccff-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fccff-168">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fccff-168">Additional resources</span></span>

[<span data-ttu-id="fccff-169">Indstillinger for implementering af netværk for indholdslevering</span><span class="sxs-lookup"><span data-stu-id="fccff-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]