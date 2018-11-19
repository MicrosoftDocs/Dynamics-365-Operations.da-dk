---
title: Regnskabsintegration for detailkanal
description: Dette emne indeholder en oversigt over regnskabsintegrationen for Retail POS.
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: da-dk
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="e416c-103">Regnskabsintegration for detailkanal</span><span class="sxs-lookup"><span data-stu-id="e416c-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e416c-104">Dette emne indeholder en oversigt over funktionen til regnskabsintegration, der er tilgængelig i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e416c-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="e416c-105">Regnskabsintegrationsfunktionen er en struktur, der er udviklet til at understøtte lokal regnskabslovgivning, som har til formål at hindre svindel i detailbranchen.</span><span class="sxs-lookup"><span data-stu-id="e416c-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="e416c-106">Typiske scenarier, som regnskabsintegrationen kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="e416c-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="e416c-107">Udskrivning af en regnskabskvittering, som gives til kunden.</span><span class="sxs-lookup"><span data-stu-id="e416c-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="e416c-108">Sikring af indsendelse af de oplysninger, der vedrører salg og returneringer i POS til en ekstern tjeneste, der leveres af myndigheden.</span><span class="sxs-lookup"><span data-stu-id="e416c-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="e416c-109">Brug af databeskyttelse med en digital signatur, der er godkendt af myndigheden.</span><span class="sxs-lookup"><span data-stu-id="e416c-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="e416c-110">Dette emne indeholder retningslinjer for konfiguration af regnskabsintegration, så brugerne kan udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="e416c-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="e416c-111">Konfigurere regnskabsforbindelser, som er regnskabsenheder eller -tjenester, der bruges til regnskabsmæssig registrering som lagring, digitale signaturer og beskyttet indsendelse af regnskabsdata.</span><span class="sxs-lookup"><span data-stu-id="e416c-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="e416c-112">Konfigurere den dokumentudbyder, der definerer en outputmetode og en algoritme til generering af regnskabsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="e416c-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="e416c-113">Konfigurere den regnskabsmæssige registreringsproces, som definerer en række trin og en gruppe af forbindelser, der bruges på hvert trin.</span><span class="sxs-lookup"><span data-stu-id="e416c-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="e416c-114">Tildele regnskabsregistreringsprocesser til POS-funktionalitetsprofiler.</span><span class="sxs-lookup"><span data-stu-id="e416c-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="e416c-115">Tildele tekniske connectorprofiler, enten til hardwareprofiler (til de lokale regnskabsforbindelser) eller til POS-funktionalitetsprofiler (til andre regnskabsconnectortyper).</span><span class="sxs-lookup"><span data-stu-id="e416c-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="e416c-116">Kørselsproces for regnskabsintegration</span><span class="sxs-lookup"><span data-stu-id="e416c-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="e416c-117">Følgende eksempel viser den almindelige kørselsproces for regnskabsintegration.</span><span class="sxs-lookup"><span data-stu-id="e416c-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="e416c-118">Initialisering af regnskabsregistreringprocessen.</span><span class="sxs-lookup"><span data-stu-id="e416c-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="e416c-119">Når du har udført nogle handlinger, hvor regnskabsregistrering er nødvendig, f.eks. når en detailtransaktion er fuldført, knyttes regnskabsregistreringsprocessen til den aktuelle POS-funktionalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="e416c-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="e416c-120">Søg efter en regnskabsconnector.</span><span class="sxs-lookup"><span data-stu-id="e416c-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="e416c-121">For hvert trin i regnskabsregistreringen, der indgår i regnskabsregistreringsprocessen, sammenligner systemet listen over regnskabsconnectorer.</span><span class="sxs-lookup"><span data-stu-id="e416c-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="e416c-122">Disse connectorer har en funktionel profil, der indgår i angivne connectorgruppe, med en liste over connectorer, der har en teknisk profil knyttet til den aktuelle hardwareprofil (kun for en connectortype, der er lig med **Lokal**) eller til den aktuelle POS-funktionalitetsprofil (for andre typer af connectorer).</span><span class="sxs-lookup"><span data-stu-id="e416c-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="e416c-123">Udfør regnskabsintegrationen.</span><span class="sxs-lookup"><span data-stu-id="e416c-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="e416c-124">Systemet udfører alle nødvendige handlinger, der er defineret af en assembly, der er knyttet til den fundne connector.</span><span class="sxs-lookup"><span data-stu-id="e416c-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="e416c-125">Dette gøres i overensstemmelse med indstillingerne for den funktionelle profil og den tekniske profil, der blev fundet i det forrige trin for denne connector.</span><span class="sxs-lookup"><span data-stu-id="e416c-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="e416c-126">Nødvendig konfiguration før brug af regnskabsintegration</span><span class="sxs-lookup"><span data-stu-id="e416c-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="e416c-127">Før du bruger funktionen til regnskabsintegration, skal du definere følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="e416c-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="e416c-128">Definer nummerserien på siden **Detailparametre** for regnskabsfunktionens profilnummer.</span><span class="sxs-lookup"><span data-stu-id="e416c-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="e416c-129">Definer nummerserierne på siden **Delte parametre for detail** for følgende referencer:</span><span class="sxs-lookup"><span data-stu-id="e416c-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="e416c-130">Regnskabsteknisk profilnummer</span><span class="sxs-lookup"><span data-stu-id="e416c-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="e416c-131">Regnskabsconnectorgruppenummer</span><span class="sxs-lookup"><span data-stu-id="e416c-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="e416c-132">Registreringsprocesnummer</span><span class="sxs-lookup"><span data-stu-id="e416c-132">Registration process number</span></span>

- <span data-ttu-id="e416c-133">Opret en **Regnskabsconnector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Regnskabsconnectorer** for hver enhed eller tjeneste, du planlægger at bruge med henblik på regnskabsintegration.</span><span class="sxs-lookup"><span data-stu-id="e416c-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="e416c-134">Opret en **Udbyder af regnskabsdokumenter** i **Retail > Konfiguration af kanal > Regnskabsintegration > Udbydere af regnskabsdokumenter** for alle regnskabsconnectorer.</span><span class="sxs-lookup"><span data-stu-id="e416c-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="e416c-135">Datatilknytning betragtes som en del af regnskabsdokumentudbyderen.</span><span class="sxs-lookup"><span data-stu-id="e416c-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="e416c-136">Hvis du vil oprette andre datatilknytninger for samme connector (som f.eks. specifik lovgivning), skal du oprette forskellige regnskabsdokumentudbydere.</span><span class="sxs-lookup"><span data-stu-id="e416c-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="e416c-137">Opret en **Funktionel profil for connector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Funktionelle profiler for connector** for hver regnskabsdokumentudbyder.</span><span class="sxs-lookup"><span data-stu-id="e416c-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="e416c-138">Vælg et connectornavn.</span><span class="sxs-lookup"><span data-stu-id="e416c-138">Select a connector name.</span></span>
  - <span data-ttu-id="e416c-139">Vælg en dokumentudbyder.</span><span class="sxs-lookup"><span data-stu-id="e416c-139">Select a document provider.</span></span>
  - <span data-ttu-id="e416c-140">Angiv indstillinger for momssatser under fanen **Konfiguration af tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="e416c-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="e416c-141">Angiv tilknytning af momskoder og betalingsmiddeltype under fanen **Tilknytning af data**.</span><span class="sxs-lookup"><span data-stu-id="e416c-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="e416c-142">Eksempler</span><span class="sxs-lookup"><span data-stu-id="e416c-142">Examples</span></span> 

  |  | <span data-ttu-id="e416c-143">Format</span><span class="sxs-lookup"><span data-stu-id="e416c-143">Format</span></span> | <span data-ttu-id="e416c-144">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e416c-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="e416c-145">Indstillinger for momssats</span><span class="sxs-lookup"><span data-stu-id="e416c-145">VAT rates settings</span></span> | <span data-ttu-id="e416c-146">værdi : VATrate</span><span class="sxs-lookup"><span data-stu-id="e416c-146">value : VATrate</span></span> | <span data-ttu-id="e416c-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="e416c-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="e416c-148">Tilknytning af momskoder</span><span class="sxs-lookup"><span data-stu-id="e416c-148">VAT codes mapping</span></span> | <span data-ttu-id="e416c-149">VATcode : værdi</span><span class="sxs-lookup"><span data-stu-id="e416c-149">VATcode : value</span></span> | <span data-ttu-id="e416c-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="e416c-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="e416c-151">Tilknytning af betalingsmiddeltyper</span><span class="sxs-lookup"><span data-stu-id="e416c-151">Tender types mapping</span></span> | <span data-ttu-id="e416c-152">TenderTyp : værdi</span><span class="sxs-lookup"><span data-stu-id="e416c-152">TenderTyp : value</span></span> | <span data-ttu-id="e416c-153">Kontant : 1, Kort : 2</span><span class="sxs-lookup"><span data-stu-id="e416c-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="e416c-154">Opret **Regnskabsconnectorgrupper** i **Retail > Konfiguration af kanal > Regnskabsintegration > Regnskabsconnectorgruppe**.</span><span class="sxs-lookup"><span data-stu-id="e416c-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="e416c-155">En connectorgruppe er et undersæt af funktionelle profiler, der er knyttet til regnskabsconncetorer, der udfører samme funktioner og bruges på samme stadie i en regnskabsregistreringsproces.</span><span class="sxs-lookup"><span data-stu-id="e416c-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="e416c-156">Tilføj funktionelle profiler til connectorgruppen.</span><span class="sxs-lookup"><span data-stu-id="e416c-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="e416c-157">Klik på **Tilføj** på siden **Funktionelle profiler**, og vælg et profilnummer.</span><span class="sxs-lookup"><span data-stu-id="e416c-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="e416c-158">Hvis du vil afbryde brugen af den funktionelle profil, kan du indstille **Deaktiver** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e416c-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="e416c-159">Denne ændring påvirker kun den aktuelle connectorgruppe.</span><span class="sxs-lookup"><span data-stu-id="e416c-159">This change affects the current connector group only.</span></span> <span data-ttu-id="e416c-160">Du kan fortsætte med at bruge den samme funktionelle profil i andre connectorgrupper.</span><span class="sxs-lookup"><span data-stu-id="e416c-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="e416c-161">I en connectorgruppe kan hver regnskabsconnector kun have én funktionel profil.</span><span class="sxs-lookup"><span data-stu-id="e416c-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="e416c-162">Opret en **Teknisk profil for connector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Tekniske profiler for connector** for hver regnskabsconnector.</span><span class="sxs-lookup"><span data-stu-id="e416c-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="e416c-163">Vælg et connectornavn.</span><span class="sxs-lookup"><span data-stu-id="e416c-163">Select a connector name.</span></span>
  - <span data-ttu-id="e416c-164">Vælg en connectortype:</span><span class="sxs-lookup"><span data-stu-id="e416c-164">Select a connector type:</span></span> 
      - <span data-ttu-id="e416c-165">**Lokal** - Indstil denne type til fysiske enheder eller programmer, der er installeret på en lokal computer.</span><span class="sxs-lookup"><span data-stu-id="e416c-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="e416c-166">**Intern** - Indstil denne type til regnskabsenheder og -tjenester, der er tilknyttet Retail Server.</span><span class="sxs-lookup"><span data-stu-id="e416c-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="e416c-167">**Ekstern** - Til eksterne regnskabstjenester som f.eks. en webportal, der er leveret af en skattemyndighed.</span><span class="sxs-lookup"><span data-stu-id="e416c-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="e416c-168">Angiv indstillinger under fanen **Forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="e416c-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="e416c-169">En opdateret version af en konfiguration, der blev indlæst tidligere, indlæses for både funktionelle og tekniske profiler.</span><span class="sxs-lookup"><span data-stu-id="e416c-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="e416c-170">Hvis en passende connector eller dokumentudbyder allerede er i brug, får du besked.</span><span class="sxs-lookup"><span data-stu-id="e416c-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="e416c-171">Som standard gemmes alle ændringer, der er oprettet manuelt i funktionelle og tekniske profiler.</span><span class="sxs-lookup"><span data-stu-id="e416c-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="e416c-172">For at tilsidesætte disse profiler med standardsættet af parametre fra en konfiguration, skal du klikke på **Opdater** på siden **Funktionelle profiler for connector** og siden **Tekniske profiler for connector**.</span><span class="sxs-lookup"><span data-stu-id="e416c-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="e416c-173">Opret en **Proces for regnskabsregistrering** i **Retail > Konfiguration af kanal > Regnskabsintegration > Processer for regnskabsregistrering** for hver entydige proces til en regnskabsintegration.</span><span class="sxs-lookup"><span data-stu-id="e416c-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="e416c-174">En registreringsproces defineres af rækkefølgen af trinnene i registreringen og den connectorgruppe, der er brugt i hvert trin.</span><span class="sxs-lookup"><span data-stu-id="e416c-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="e416c-175">Føj registreringstrin til processen:</span><span class="sxs-lookup"><span data-stu-id="e416c-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="e416c-176">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e416c-176">Click **Add**.</span></span>
      - <span data-ttu-id="e416c-177">Vælg en connectortype.</span><span class="sxs-lookup"><span data-stu-id="e416c-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="e416c-178">Dette felt definerer, hvor systemet søger i en teknisk profil for connectoren, enten i hardwareprofiler for connectortypen at skrive **Lokal** eller i POS-funktionalitetsprofiler for andre regnskabsconnectortyper.</span><span class="sxs-lookup"><span data-stu-id="e416c-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="e416c-179">Vælg en connectorgruppe.</span><span class="sxs-lookup"><span data-stu-id="e416c-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="e416c-180">Klik på **Valider** for at kontrollere integriteten af registreringsprocesstrukturen.</span><span class="sxs-lookup"><span data-stu-id="e416c-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="e416c-181">Det anbefales, at der foretages valideringer i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="e416c-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="e416c-182">Ved en ny registreringsproces, når alle indstillinger er fuldført, herunder binding til POS-funktionalitetsprofiler og hardwareprofiler.</span><span class="sxs-lookup"><span data-stu-id="e416c-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="e416c-183">Når du har foretaget opdateringer af en eksisterende registreringsproces.</span><span class="sxs-lookup"><span data-stu-id="e416c-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="e416c-184">Bind regnskabsregistreringsprocesser til POS-funktionalitetsprofiler i **Retail > Konfiguration af kanal > POS-opsætning > POS-profiler > Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="e416c-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="e416c-185">Klik på **Rediger**, og vælg et **Procesnummer** under fanen **Regnskabsregistreringsproces**.</span><span class="sxs-lookup"><span data-stu-id="e416c-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="e416c-186">Bind tekniske connectorprofiler til hardwareprofiler i **Retail > Konfiguration af kanal > POS-opsætning > POS-profiler > Hardwareprofiler**.</span><span class="sxs-lookup"><span data-stu-id="e416c-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="e416c-187">Klik på **Rediger**, og klik derefter på **Ny** under fanen **Regnskabsteknisk profil**.</span><span class="sxs-lookup"><span data-stu-id="e416c-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="e416c-188">Vælg en teknisk connectorprofil i feltet **Profilnummer**.</span><span class="sxs-lookup"><span data-stu-id="e416c-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="e416c-189">Du kan tilføje flere tekniske profiler til en hardwareprofil.</span><span class="sxs-lookup"><span data-stu-id="e416c-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="e416c-190">Men dette understøttes ikke, hvis en hardwareprofil har mere end ét skæringspunkt med en connectorgruppe.</span><span class="sxs-lookup"><span data-stu-id="e416c-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="e416c-191">Hvis du vil undgå forkerte indstillinger, anbefales det, at du validerer registreringsprocessen, når du har opdateret alle hardwareprofiler.</span><span class="sxs-lookup"><span data-stu-id="e416c-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

