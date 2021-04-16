---
title: Komponenter til elektronisk fakturering i administration
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840022"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="19456-103">Komponenter til elektronisk fakturering i administration</span><span class="sxs-lookup"><span data-stu-id="19456-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19456-104">Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="19456-105">Det indeholder også oplysninger om, hvordan du konfigurerer Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="19456-106">Azure</span><span class="sxs-lookup"><span data-stu-id="19456-106">Azure</span></span>

<span data-ttu-id="19456-107">Bruges Microsoft Azure til at oprette Key Vault og lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="19456-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="19456-108">Brug derefter hemmeligheder i konfigurationen af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="19456-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="19456-109">Lifecycle Services</span></span>

<span data-ttu-id="19456-110">Brug Microsoft Dynamics Lifecycle Services (LCS) til at aktivere mikroservices til dit LCS-implementeringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="19456-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="19456-111">Installationen af mikroservice i LCS kræver mindst en virtuel maskine på niveau 2.</span><span class="sxs-lookup"><span data-stu-id="19456-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="19456-112">Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="19456-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="19456-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="19456-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="19456-114">Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="19456-115">Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS.</span><span class="sxs-lookup"><span data-stu-id="19456-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="19456-116">Når ressourcerne er klar, publiceres de til Elektronisk faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="19456-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="19456-117">Vedrørende RCS-tilmelding se [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="19456-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="19456-118">Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="19456-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="19456-119">Integration med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="19456-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="19456-120">Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="19456-121">Du fuldfører denne konfiguration under fanen **Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="19456-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="19456-122">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="19456-122">Service endpoint</span></span>

<span data-ttu-id="19456-123">Elektronisk fakturering er tilgængelig i flere geografiske Azure-datacentre.</span><span class="sxs-lookup"><span data-stu-id="19456-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="19456-124">Følgende tabel viser tilgængeligheden pr. region.</span><span class="sxs-lookup"><span data-stu-id="19456-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="19456-125">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="19456-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="19456-126">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="19456-126">East US</span></span>                    |
| <span data-ttu-id="19456-127">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="19456-127">West US</span></span>                    |
| <span data-ttu-id="19456-128">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="19456-128">North EU</span></span>                   |
| <span data-ttu-id="19456-129">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="19456-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="19456-130">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="19456-130">Service environments</span></span>

<span data-ttu-id="19456-131">Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for elektronisk fakturering i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="19456-132">Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.</span><span class="sxs-lookup"><span data-stu-id="19456-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="19456-133">Kunder kan oprette lige så mange tjenestemiljøer, de ønsker.</span><span class="sxs-lookup"><span data-stu-id="19456-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="19456-134">Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.</span><span class="sxs-lookup"><span data-stu-id="19456-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="19456-135">Tjenestemiljøer skal oprettes og vedligeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="19456-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="19456-136">Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="19456-137">Status for tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="19456-137">Service environment status</span></span>

<span data-ttu-id="19456-138">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="19456-138">Service environments can be managed through status.</span></span> <span data-ttu-id="19456-139">De mulige indstillinger er:</span><span class="sxs-lookup"><span data-stu-id="19456-139">The possible options are:</span></span>

- <span data-ttu-id="19456-140">**Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.</span><span class="sxs-lookup"><span data-stu-id="19456-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="19456-141">**Publiceret** – Miljøet er udgivet til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="19456-142">**Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.</span><span class="sxs-lookup"><span data-stu-id="19456-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="19456-143">Kundehemmeligheder</span><span class="sxs-lookup"><span data-stu-id="19456-143">Customer secrets</span></span>

<span data-ttu-id="19456-144">Tjenesten til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="19456-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="19456-145">Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af Elektronisk fakturering, tilgås korrekt, skal du oprette to hovedressourcer i Azure:</span><span class="sxs-lookup"><span data-stu-id="19456-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="19456-146">En Azure Storage-konto (Blob-lager) der kan opbevare elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="19456-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="19456-147">En Azure Key Vault, der kan opbevare certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="19456-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="19456-148">En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="19456-149">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="19456-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="19456-150">Brugere</span><span class="sxs-lookup"><span data-stu-id="19456-150">Users</span></span>

<span data-ttu-id="19456-151">De enkelte tjenestemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="19456-152">Publikation</span><span class="sxs-lookup"><span data-stu-id="19456-152">Publication</span></span>

<span data-ttu-id="19456-153">Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering, før de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="19456-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="19456-154">Der er kun publicerede miljøer tilgængelige i Finans og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="19456-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="19456-155">Desuden skal et servicemiljø publiceres, før eventuelle opdateringer af attributterne i programmet træder i kraft for den elektroniske faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="19456-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="19456-156">Tilsluttede ansøgninger</span><span class="sxs-lookup"><span data-stu-id="19456-156">Connected applications</span></span>

<span data-ttu-id="19456-157">Tilknyttede applikationer er de forekomster af Finans og Supply Chain Management, som du muligvis vil have kontakt til via RCS.</span><span class="sxs-lookup"><span data-stu-id="19456-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="19456-158">Udover applikationens URL-adresse og dens lejer indeholder en tilknyttet applikation de legitimationsoplysninger, der gør det muligt for RCS at oprette forbindelse til miljøet.</span><span class="sxs-lookup"><span data-stu-id="19456-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="19456-159">Via de tilknyttede applikationer kan du konfigurere en del af funktionen til elektronisk fakturering i Finans og Supply Chain Management, så hele funktionen til elektronisk fakturering fungerer.</span><span class="sxs-lookup"><span data-stu-id="19456-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="19456-160">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="19456-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="19456-161">Integration med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="19456-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="19456-162">Før du kan bruge Finans og Supply Chain Management til at udstede elektroniske fakturaer via Elektronisk fakturering, skal det være konfigureret, så der kan kommunikeres med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="19456-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="19456-163">Funktion til integration af elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="19456-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="19456-164">Hvis du vil aktivere kommunikation mellem Finance og Supply Chain Management og Elektronisk fakturering, skal du aktivere funktionen **Integration af Elektronisk fakturering** i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="19456-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="19456-165">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="19456-165">Service endpoint</span></span>

<span data-ttu-id="19456-166">Tjenesteslutpunktet er den URL-adresse, hvor Elektronisk fakturering er placeret.</span><span class="sxs-lookup"><span data-stu-id="19456-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="19456-167">Før du kan udstede elektroniske fakturaer, skal tjenesteslutpunktet konfigureres i Finans og Supply Chain Management for at tillade kommunikation med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="19456-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="19456-168">Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparameter** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til Elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet i afsnittet **Serviceslutpunkt**.</span><span class="sxs-lookup"><span data-stu-id="19456-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="19456-169">Miljøer</span><span class="sxs-lookup"><span data-stu-id="19456-169">Environments</span></span>

<span data-ttu-id="19456-170">Det miljønavn, der angives i Finance og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="19456-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="19456-171">Miljøet skal konfigureres under fanen **Overførselstjenester** på **Elektronisk dokumentparameter**, så alle anmodninger om udstedelse af elektroniske fakturaer indeholder det miljø, hvor Elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.</span><span class="sxs-lookup"><span data-stu-id="19456-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19456-172">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="19456-172">Additional resources</span></span>

- [<span data-ttu-id="19456-173">Konfiguration af elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="19456-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="19456-174">Udsted elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="19456-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
