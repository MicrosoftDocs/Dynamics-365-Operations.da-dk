---
title: Komponenter til elektronisk fakturering i administration
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963185"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="ef0cf-103">Komponenter til elektronisk fakturering i administration</span><span class="sxs-lookup"><span data-stu-id="ef0cf-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ef0cf-104">Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="ef0cf-105">Det indeholder også oplysninger om, hvordan du konfigurerer Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="ef0cf-106">Azure</span><span class="sxs-lookup"><span data-stu-id="ef0cf-106">Azure</span></span>

<span data-ttu-id="ef0cf-107">Brug Microsoft Azure til at oprette hemmeligheder for Key Vault og lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="ef0cf-108">Brug derefter hemmeligheder i konfigurationen af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="ef0cf-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ef0cf-109">Lifecycle Services</span></span>

<span data-ttu-id="ef0cf-110">Brug Microsoft Dynamics Lifecycle Services (LCS) til at aktivere mikroservices til dit LCS-implementeringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="ef0cf-111">Installationen af mikroservice i LCS kræver mindst en virtuel maskine på niveau 2.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="ef0cf-112">Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="ef0cf-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="ef0cf-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="ef0cf-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="ef0cf-114">Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="ef0cf-115">Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="ef0cf-116">Når ressourcerne er klar, publiceres de til Elektronisk faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="ef0cf-117">Vedrørende RCS-tilmelding se [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="ef0cf-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="ef0cf-118">Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="ef0cf-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="ef0cf-119">Integration med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="ef0cf-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="ef0cf-120">Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="ef0cf-121">Du fuldfører denne konfiguration under fanen **Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="ef0cf-122">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="ef0cf-122">Service endpoint</span></span>

<span data-ttu-id="ef0cf-123">Elektronisk fakturering er tilgængelig i flere geografiske Azure-datacentre.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="ef0cf-124">Følgende tabel viser tilgængeligheden pr. region.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="ef0cf-125">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="ef0cf-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="ef0cf-126">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="ef0cf-126">East US</span></span>                    |
| <span data-ttu-id="ef0cf-127">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="ef0cf-127">West US</span></span>                    |
| <span data-ttu-id="ef0cf-128">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="ef0cf-128">North EU</span></span>                   |
| <span data-ttu-id="ef0cf-129">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="ef0cf-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="ef0cf-130">Tjenestemiljøer</span><span class="sxs-lookup"><span data-stu-id="ef0cf-130">Service environments</span></span>

<span data-ttu-id="ef0cf-131">Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for elektronisk fakturering i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="ef0cf-132">Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="ef0cf-133">Kunder kan oprette lige så mange tjenestemiljøer, de ønsker.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="ef0cf-134">Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="ef0cf-135">Tjenestemiljøer skal oprettes og vedligeholdes i RCS.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="ef0cf-136">Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="ef0cf-137">Status for tjenestemiljø</span><span class="sxs-lookup"><span data-stu-id="ef0cf-137">Service environment status</span></span>

<span data-ttu-id="ef0cf-138">Tjenestemiljøer kan administreres via status.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-138">Service environments can be managed through status.</span></span> <span data-ttu-id="ef0cf-139">De mulige indstillinger er:</span><span class="sxs-lookup"><span data-stu-id="ef0cf-139">The possible options are:</span></span>

- <span data-ttu-id="ef0cf-140">**Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="ef0cf-141">**Publiceret** – Miljøet er udgivet til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="ef0cf-142">**Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="ef0cf-143">Kundehemmeligheder</span><span class="sxs-lookup"><span data-stu-id="ef0cf-143">Customer secrets</span></span>

<span data-ttu-id="ef0cf-144">Tjenesten til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="ef0cf-145">Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af Elektronisk fakturering, tilgås korrekt, skal du oprette to hovedressourcer i Azure:</span><span class="sxs-lookup"><span data-stu-id="ef0cf-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="ef0cf-146">En Azure Storage-konto (Blob-lager) der kan opbevare elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="ef0cf-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="ef0cf-147">En Azure Key Vault, der opbevarer certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="ef0cf-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="ef0cf-148">En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="ef0cf-149">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og en Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="ef0cf-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="ef0cf-150">Hvis du vil overvåge sundheden af Key Vault og modtage advarsler, skal du konfigurere Azure Monitor til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="ef0cf-151">Ved at aktivere logføring af Key Vault kan du overvåge, hvordan, hvornår og hvem der tilgår Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="ef0cf-152">Du kan finde flere oplysninger i [Overvågning og advarsler for Azure Key Vault](/azure/key-vault/general/alert), og [Hvordan du aktiverer logning af Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="ef0cf-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="ef0cf-153">Som bedste praksis skal hemmeligheder jævnligt ombyttes.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="ef0cf-154">Yderligere oplysninger finder du i [Dokumentation af hemmeligheder](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="ef0cf-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="ef0cf-155">Brugere</span><span class="sxs-lookup"><span data-stu-id="ef0cf-155">Users</span></span>

<span data-ttu-id="ef0cf-156">De enkelte tjenestemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="ef0cf-157">Publikation</span><span class="sxs-lookup"><span data-stu-id="ef0cf-157">Publication</span></span>

<span data-ttu-id="ef0cf-158">Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering, før de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="ef0cf-159">Der er kun publicerede miljøer tilgængelige i Finans og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="ef0cf-160">Desuden skal et servicemiljø publiceres, før eventuelle opdateringer af attributterne i programmet træder i kraft for den elektroniske faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="ef0cf-161">Tilsluttede ansøgninger</span><span class="sxs-lookup"><span data-stu-id="ef0cf-161">Connected applications</span></span>

<span data-ttu-id="ef0cf-162">Tilknyttede applikationer er de forekomster af Finans og Supply Chain Management, som du muligvis vil have kontakt til via RCS.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="ef0cf-163">Udover applikationens URL-adresse og dens lejer indeholder en tilknyttet applikation de legitimationsoplysninger, der gør det muligt for RCS at oprette forbindelse til miljøet.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="ef0cf-164">Via de tilknyttede applikationer kan du konfigurere en del af funktionen til elektronisk fakturering i Finans og Supply Chain Management, så hele funktionen til elektronisk fakturering fungerer.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="ef0cf-165">Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ef0cf-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="ef0cf-166">Integration med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="ef0cf-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="ef0cf-167">Før du kan bruge Finans og Supply Chain Management til at udstede elektroniske fakturaer via Elektronisk fakturering, skal det være konfigureret, så der kan kommunikeres med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="ef0cf-168">Funktion til integration af elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="ef0cf-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="ef0cf-169">Hvis du vil aktivere kommunikation mellem Finance og Supply Chain Management og Elektronisk fakturering, skal du aktivere funktionen **Integration af Elektronisk fakturering** i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="ef0cf-170">Tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="ef0cf-170">Service endpoint</span></span>

<span data-ttu-id="ef0cf-171">Tjenesteslutpunktet er den URL-adresse, hvor Elektronisk fakturering er placeret.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="ef0cf-172">Før du kan udstede elektroniske fakturaer, skal tjenesteslutpunktet konfigureres i Finans og Supply Chain Management for at tillade kommunikation med tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="ef0cf-173">Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparameter** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til Elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet i afsnittet **Serviceslutpunkt**.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="ef0cf-174">Miljøer</span><span class="sxs-lookup"><span data-stu-id="ef0cf-174">Environments</span></span>

<span data-ttu-id="ef0cf-175">Det miljønavn, der angives i Finance og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="ef0cf-176">Miljøet skal konfigureres under fanen **Overførselstjenester** på **Elektronisk dokumentparameter**, så alle anmodninger om udstedelse af elektroniske fakturaer indeholder det miljø, hvor Elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.</span><span class="sxs-lookup"><span data-stu-id="ef0cf-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef0cf-177">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ef0cf-177">Additional resources</span></span>

- [<span data-ttu-id="ef0cf-178">Konfiguration af elektroniske fakturaer i RCS</span><span class="sxs-lookup"><span data-stu-id="ef0cf-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="ef0cf-179">Udsted elektroniske fakturaer i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ef0cf-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
