---
title: A-skatopgørelse for Egypten
description: Dette emne forklarer, hvordan du konfigurerer og genererer A-skatopgørelse til Egypten.
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574318"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="5911f-103">A-skatopgørelse for Egypten (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="5911f-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="5911f-104">Overblik</span><span class="sxs-lookup"><span data-stu-id="5911f-104">Overview</span></span>
<span data-ttu-id="5911f-105">Dette emne forklarer, hvordan du opretter og genererer A-skatteopgørelsen og formularer til A-skatteopgørelsen 41 og 11 til juridiske enheder i Egypten</span><span class="sxs-lookup"><span data-stu-id="5911f-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="5911f-106">Alle egyptiske enheder skal forberede formular 41, der opsummerer al skat, der tilbageholdes fra lokale leverandører og serviceudbydere.</span><span class="sxs-lookup"><span data-stu-id="5911f-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="5911f-107">Ud over formular 41 skal formular 11 genereres med detaljer for alle tilbageholdte skatter fra udenlandske leverandører.</span><span class="sxs-lookup"><span data-stu-id="5911f-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="5911f-108">Rapporten **A-skatteopgørelse** indeholder følgende rapporter i Dynamics 365 Finance:</span><span class="sxs-lookup"><span data-stu-id="5911f-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="5911f-109">Rapportformular-nr.</span><span class="sxs-lookup"><span data-stu-id="5911f-109">Declaration form No.</span></span> <span data-ttu-id="5911f-110">41</span><span class="sxs-lookup"><span data-stu-id="5911f-110">41</span></span>
- <span data-ttu-id="5911f-111">Rapportformular-nr.</span><span class="sxs-lookup"><span data-stu-id="5911f-111">Declaration form No.</span></span> <span data-ttu-id="5911f-112">11</span><span class="sxs-lookup"><span data-stu-id="5911f-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="5911f-113">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="5911f-113">Prerequisites</span></span>
<span data-ttu-id="5911f-114">Den primære adresse for den juridiske enhed være i Egypten.</span><span class="sxs-lookup"><span data-stu-id="5911f-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="5911f-115">I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktion:</span><span class="sxs-lookup"><span data-stu-id="5911f-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="5911f-116">**Globalt A-skat**</span><span class="sxs-lookup"><span data-stu-id="5911f-116">**Global withholding tax**</span></span>

<span data-ttu-id="5911f-117">Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5911f-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="5911f-118">Gå til **Moms** > **Opsætning** > **Parametre** > **Finansparametre** og på fanen **A-skat** skal du angive **Aktiver global A-skat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5911f-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="5911f-119">I arbejdsområdet for **elektronisk rapportering** skal du importere følgende format for elektronisk rapportering fra lageret:</span><span class="sxs-lookup"><span data-stu-id="5911f-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="5911f-120">WHT-opgørelse Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="5911f-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="5911f-121">Formatet ovenfor er baseret på **Momsopgørelsesmodel** og bruger **Tilknytning til momsopgørelsesmodel**.</span><span class="sxs-lookup"><span data-stu-id="5911f-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="5911f-122">Denne ekstra konfiguration importeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="5911f-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="5911f-123">Du kan finde flere oplysninger om, hvordan du importerer konfigurationer af elektronisk rapportering, i [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="5911f-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="5911f-124">Hent konfigurationer for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="5911f-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="5911f-125">Implementeringen af WHT-formularen til indberetning for Egypten er baseret på konfigurationen af Elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="5911f-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="5911f-126">Du kan finde flere oplysninger om egenskaberne og koncepterne ved konfigurerbar rapportering under [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="5911f-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="5911f-127">I forbindelse med produktions- og brugermodtagelsestestmiljøer (UAT) skal du følge vejledningen i emnet [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="5911f-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="5911f-128">Hvis du vil generere A-opgørelserne i en egyptisk enhed medstyring, skal du overføre følgende konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="5911f-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="5911f-129">Momsopgørelsesmodel.version.82.xml eller senere version</span><span class="sxs-lookup"><span data-stu-id="5911f-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="5911f-130">Momsopgørelsesmodel mapping.version.82.133.xml eller senere version</span><span class="sxs-lookup"><span data-stu-id="5911f-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="5911f-131">Momsopgørelse Excel (EG).version.82.21 eller en senere version</span><span class="sxs-lookup"><span data-stu-id="5911f-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="5911f-132">Når du har hentet ER-konfigurationerne fra Lifecycle Services (LCS) eller det globale lager, skal du gennemføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="5911f-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="5911f-133">Gå til arbejdsområdet **Elektronisk rapportering** og vælg feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="5911f-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="5911f-134">Gå til siden **Konfigurationer**, og vælg **Kurs > Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5911f-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="5911f-135">Overfør alle filerne i den rækkefølge, som de er angivet i de forrige punkttegn.</span><span class="sxs-lookup"><span data-stu-id="5911f-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="5911f-136">Når alle konfigurationerne er overført, skal konfigurationstræet være til stede i Finans.</span><span class="sxs-lookup"><span data-stu-id="5911f-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="5911f-137">Oprette ansøgningsspecifikke parametre</span><span class="sxs-lookup"><span data-stu-id="5911f-137">Set up application-specific parameters</span></span>

<span data-ttu-id="5911f-138">Den programspecifikke indstilling giver brugerne mulighed for at opstille kriterierne for, hvordan momstransaktioner skal klassificeres og beregnes på hver linje i en genereret rapport, afhængigt af konfigurationen af **varegruppe for A-skat** eller andre kriterier, der er defineret i definitionen af opslag.</span><span class="sxs-lookup"><span data-stu-id="5911f-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="5911f-139">A-opgørelsesform 41 indeholder en specifik kolonne, hvor A-skatteposteringen skal klassificeres i overensstemmelse med skattemyndighedsklassifikationen med navnet **Rabatkodetype**.</span><span class="sxs-lookup"><span data-stu-id="5911f-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="5911f-140">I stedet for at medtage disse nye klassifikationer som nye postdata, når posteringerne bogføres, vil klassifikationerne blive fastlagt på basis af forskellige opslag, der er indført i **Konfigurationer** > **Konfigurer programspecifikke parametre** > **Konfiguration** for at opfylde kravene i opgørelsesrapporter for Egypten.</span><span class="sxs-lookup"><span data-stu-id="5911f-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="5911f-141">Følgende konfiguration bruges til klassificering af posteringerne i A-opgørelsesform 41-rapporten:</span><span class="sxs-lookup"><span data-stu-id="5911f-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="5911f-142">**DiscountTaxTypeLookup** -> Kolonnenr. 18</span><span class="sxs-lookup"><span data-stu-id="5911f-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="5911f-143">Gennemfør følgende trin for at konfigurere de forskellige opslag, der bruges til at oprette momsopgørelser og relaterede bograpporter.</span><span class="sxs-lookup"><span data-stu-id="5911f-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="5911f-144">I arbejdsområdet for **elektronisk rapportering** skal du vælge **Konfigurationer** > **Opsætning** for at oprette regler, der identificerer hvordan transaktioner klassificeres i momsrapporteringsrapporten.</span><span class="sxs-lookup"><span data-stu-id="5911f-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="5911f-145">Vælg den aktuelle version, og vælg opslagsnavnet på oversigtspanelet **Opslag**.</span><span class="sxs-lookup"><span data-stu-id="5911f-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="5911f-146">F.eks. **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="5911f-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="5911f-147">Dette opslag identificerer listen over rabattyper, der kræves af skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="5911f-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="5911f-148">I oversigtspanelet **Betingelser** skal du vælge **Tilføj** og på den nye linje i kolonnen **Opslagsresultat** vælge den relaterede linje, der repræsenterer klassifikationen i **Kolonne 18**.</span><span class="sxs-lookup"><span data-stu-id="5911f-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="5911f-149">Vælg i kolonnen **A-skatgruppe** den kode, der bruges til at identificere klassifikationen.</span><span class="sxs-lookup"><span data-stu-id="5911f-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="5911f-150">F.eks. **Tilladt rabat**.</span><span class="sxs-lookup"><span data-stu-id="5911f-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="5911f-151">Gentag trin 3 og 4 for alle tilgængelige opslag.</span><span class="sxs-lookup"><span data-stu-id="5911f-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="5911f-152">Vælg **Tilføj** igen for at medtage den sidste postlinje, og vælg **Ikke relevant** i kolonnen **Opslagsresultat**.</span><span class="sxs-lookup"><span data-stu-id="5911f-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="5911f-153">Vælg **Ikke tom** i resten af kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="5911f-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="5911f-154">Konfigurer økonomiparametre</span><span class="sxs-lookup"><span data-stu-id="5911f-154">Set up General ledger parameters</span></span>

<span data-ttu-id="5911f-155">Hvis du vil generere momsindberetningsformularrapporten i Microsoft Excel-format, skal du definere et ER-format på siden **Økonomiparametre**.</span><span class="sxs-lookup"><span data-stu-id="5911f-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="5911f-156">Gå til **Moms** > **Opsætning** > **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="5911f-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="5911f-157">Under fanen **A-skat** skal du i feltet **Formattilknytning af WHT-opgørelse** vælge **WHT-opgørelse i Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="5911f-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="5911f-158">Hvis du lader feltet stå tomt, genereres standardrapporten for moms i SSRS-format.</span><span class="sxs-lookup"><span data-stu-id="5911f-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Rapport formular](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="5911f-160">Generere A-opgørelsesformularer</span><span class="sxs-lookup"><span data-stu-id="5911f-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="5911f-161">Processen til forberedelse og afsendelse af en form for A-opgørelse for en bestemt periode er baseret på de posteringer for A-skat, der er bogført under afregnings- og postering af betalingsskatjobbet.</span><span class="sxs-lookup"><span data-stu-id="5911f-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="5911f-162">Du kan finde flere oplysninger om global A-skat i [Global A-skat](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5911f-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="5911f-163">Fuldfør følgende trin, hvis du vil generere den elektroniske momsopgørelse:</span><span class="sxs-lookup"><span data-stu-id="5911f-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="5911f-164">Gå til **Moms** > **Opgørelse** > **A-skat** > \**Betaling af A-skat*.</span><span class="sxs-lookup"><span data-stu-id="5911f-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="5911f-165">Vælg afregningsperioden, og vælg fra-datoen til rapporten.</span><span class="sxs-lookup"><span data-stu-id="5911f-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="5911f-166">Angiv transaktionsdatoen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5911f-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="5911f-167">I den dialogboks, der åbnes, skal du vælge en eller flere formtyper **Formularnr. 41**, **Formular nr. 11** eller **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="5911f-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="5911f-168">Hvis du vælger **Ingen**, genereres standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="5911f-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="5911f-169">Vælg sprog.</span><span class="sxs-lookup"><span data-stu-id="5911f-169">Select the language.</span></span> <span data-ttu-id="5911f-170">Alle rapporter oversættes i **en-us** og **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="5911f-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="5911f-171">Angiv afdelingen og navnet på den bank, hvor skattebetalingen skal betales.</span><span class="sxs-lookup"><span data-stu-id="5911f-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="5911f-172">Vælg forretningstype, og angiv derefter check- og dokumentnumrene.</span><span class="sxs-lookup"><span data-stu-id="5911f-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="5911f-173">Angiv enhedstypen.</span><span class="sxs-lookup"><span data-stu-id="5911f-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="5911f-174">Angiv navnet på den person, der er registreret for at tildele formen, og vælg **OK** for at bekræfte generering af rapporter.</span><span class="sxs-lookup"><span data-stu-id="5911f-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
