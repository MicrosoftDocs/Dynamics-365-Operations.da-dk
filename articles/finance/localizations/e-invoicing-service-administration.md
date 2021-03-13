---
title: Administrationskomponenter til tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af tilføjelsesprogrammet Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104360"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="93571-103">Administrationskomponenter til tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="93571-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="93571-104">Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="93571-105">Det indeholder også oplysninger om, hvordan du konfigurerer tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="93571-106">Azure</span><span class="sxs-lookup"><span data-stu-id="93571-106">Azure</span></span>

<span data-ttu-id="93571-107">Bruges Microsoft Azure til at oprette Key Vault og lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="93571-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="93571-108">Brug derefter hemmeligheder i konfigurationen af tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="93571-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="93571-109">Lifecycle Services</span></span>

<span data-ttu-id="93571-110">Brug Microsoft Dynamics Lifecycle Services (LCS) for at aktivere tilføjelsesprogrammet til mikroservices til dit LCS-implementeringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="93571-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="93571-111">I LCS skal du vælge **Prøveversion af funktionsstyring** og derefter aktivere funktionen **e-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="93571-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="93571-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="93571-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="93571-113">Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="93571-114">Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS.</span><span class="sxs-lookup"><span data-stu-id="93571-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="93571-115">Når ressourcerne er klar, publiceres de til tilføjelsesprogrammet Elektronisk faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="93571-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="93571-116">Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="93571-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="93571-117">Integration til tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="93571-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="93571-118">Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="93571-119">Du fuldfører denne konfiguration under fanen **Tilføjelsesprogram til Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="93571-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="93571-120">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="93571-120">Service endpoint</span></span>

<span data-ttu-id="93571-121">URL-adressen for slutpunktet til tilføjelsesprogrammet Elektronisk fakturering kan variere alt efter Datacenter Azure-geografisk område.</span><span class="sxs-lookup"><span data-stu-id="93571-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="93571-122">Følgende tabel viser tilgængeligheden pr. region:</span><span class="sxs-lookup"><span data-stu-id="93571-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="93571-123">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="93571-123">Azure datacenter geography</span></span> | <span data-ttu-id="93571-124">URL for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="93571-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="93571-125">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="93571-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="93571-126">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="93571-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="93571-127">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="93571-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="93571-128">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="93571-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="93571-129">Program-id</span><span class="sxs-lookup"><span data-stu-id="93571-129">Application ID</span></span>

<span data-ttu-id="93571-130">Applikations-id er id for tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="93571-131">Her er værdien fastsat: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="93571-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="93571-132">LCS miljø-id</span><span class="sxs-lookup"><span data-stu-id="93571-132">LCS environment ID</span></span>

<span data-ttu-id="93571-133">LCS miljø-id er id for organisationens LCS-abonnement.</span><span class="sxs-lookup"><span data-stu-id="93571-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="93571-134">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="93571-134">Service environments</span></span>

<span data-ttu-id="93571-135">Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for elektronisk fakturering i tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="93571-136">Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.</span><span class="sxs-lookup"><span data-stu-id="93571-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="93571-137">Kunder kan oprette lige så mange tjenestemiljøer, de ønsker.</span><span class="sxs-lookup"><span data-stu-id="93571-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="93571-138">Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.</span><span class="sxs-lookup"><span data-stu-id="93571-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="93571-139">Tjenestemiljøer skal oprettes og vedligeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="93571-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="93571-140">Når tjenestemiljøerne er klar, skal de publiceres til tilføjelsesprogrammet Elektronisk faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="93571-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="93571-141">Status for tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="93571-141">Service environment status</span></span>

<span data-ttu-id="93571-142">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="93571-142">Service environments can be managed through status.</span></span> <span data-ttu-id="93571-143">De mulige indstillinger er:</span><span class="sxs-lookup"><span data-stu-id="93571-143">The possible options are:</span></span>

- <span data-ttu-id="93571-144">**Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.</span><span class="sxs-lookup"><span data-stu-id="93571-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="93571-145">**Udgivet** – Miljøet er udgivet i tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="93571-146">**Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.</span><span class="sxs-lookup"><span data-stu-id="93571-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="93571-147">Kundehemmeligheder</span><span class="sxs-lookup"><span data-stu-id="93571-147">Customer secrets</span></span>

<span data-ttu-id="93571-148">Tjenesten for tilføjelsesprogrammet til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="93571-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="93571-149">Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af tilføjelsesprogrammet til elektronisk fakturering, kun tilgås af tilføjelsesprogrammet, skal du oprette to hovedressourcer i Azure:</span><span class="sxs-lookup"><span data-stu-id="93571-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="93571-150">En Azure Storage-konto (Blob-lager) der kan opbevare elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="93571-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="93571-151">En Azure Key Vault, der kan opbevare certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="93571-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="93571-152">En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="93571-153">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="93571-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="93571-154">Brugere</span><span class="sxs-lookup"><span data-stu-id="93571-154">Users</span></span>

<span data-ttu-id="93571-155">De enkelte tjenestemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="93571-156">Publikation</span><span class="sxs-lookup"><span data-stu-id="93571-156">Publication</span></span>

<span data-ttu-id="93571-157">Når tjenestemiljøerne er klar, skal de publiceres til tilføjelsesprogrammet Elektronisk faktureringstjeneste, før de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="93571-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="93571-158">Der er kun publicerede miljøer tilgængelige i Finans og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="93571-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="93571-159">Desuden skal et servicemiljø publiceres, før eventuelle opdateringer af attributterne i programmet træder i kraft for den elektroniske faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="93571-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="93571-160">Tilsluttede ansøgninger</span><span class="sxs-lookup"><span data-stu-id="93571-160">Connected applications</span></span>

<span data-ttu-id="93571-161">Tilknyttede applikationer er de forekomster af Finans og Supply Chain Management, som du muligvis vil have kontakt til via RCS.</span><span class="sxs-lookup"><span data-stu-id="93571-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="93571-162">Udover applikationens URL-adresse og dens lejer indeholder en tilknyttet applikation de legitimationsoplysninger, der gør det muligt for RCS at oprette forbindelse til miljøet.</span><span class="sxs-lookup"><span data-stu-id="93571-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="93571-163">Via de tilknyttede applikationer kan du konfigurere en del af funktionen til elektronisk fakturering i Finans og Supply Chain Management, så hele funktionen til elektronisk fakturering fungerer.</span><span class="sxs-lookup"><span data-stu-id="93571-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="93571-164">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="93571-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="93571-165">Integration til tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="93571-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="93571-166">Før du kan bruge Finans og Supply Chain Management til at udstede elektroniske fakturaer via tilføjelsesprogrammet Elektronisk fakturering, skal tilføjelsesprogrammet være konfigureret, så der kan kommunikeres med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="93571-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="93571-167">Funktionen i tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="93571-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="93571-168">Hvis du vil aktivere kommunikation mellem Finans og Supply Chain Management og **tilføjelsesprogrammet Elektronisk fakturering**, skal du aktivere funktionen til integration af tilføjelsesprogrammet Elektronisk fakturering i arbejdsområdet til **funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="93571-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="93571-169">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="93571-169">Service endpoint</span></span>

<span data-ttu-id="93571-170">Tjenesteslutpunktet er den URL-adresse, hvor tilføjelsesprogrammet Elektronisk fakturering er placeret.</span><span class="sxs-lookup"><span data-stu-id="93571-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="93571-171">Før du kan udstede elektroniske fakturaer, skal tjenesteslutpunktet konfigureres i Finans og Supply Chain Management for at tillade kommunikation med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="93571-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="93571-172">Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparameter** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til tilføjelsesprogrammet til elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet i afsnittet **Serviceslutpunkt**.</span><span class="sxs-lookup"><span data-stu-id="93571-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="93571-173">Miljøer</span><span class="sxs-lookup"><span data-stu-id="93571-173">Environments</span></span>

<span data-ttu-id="93571-174">Det miljønavn, der angives i Finans og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i tilføjelsesprogrammet Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="93571-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="93571-175">Miljøet skal konfigureres under fanen **Overførselstjenester** på **Elektronisk dokumentparameter**, så alle anmodninger om udstedelse af elektroniske fakturaer indeholder det miljø, hvor tilføjelsesprogrammet Elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.</span><span class="sxs-lookup"><span data-stu-id="93571-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93571-176">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="93571-176">Additional resources</span></span>

- [<span data-ttu-id="93571-177">Konfiguration af elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="93571-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="93571-178">Udsted elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="93571-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
