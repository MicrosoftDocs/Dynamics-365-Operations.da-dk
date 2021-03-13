---
title: Importér kreditorkataloger
description: Dette emne beskriver processen for import af data fra kreditorkataloget.
author: RichardLuan
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: riluan
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 6a6fc2b4fe4245a1fe5b5a7eaafe8cc7fd337ab9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020748"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="19757-103">Importér kreditorkataloger</span><span class="sxs-lookup"><span data-stu-id="19757-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="19757-104">Import af kreditorkataloger</span><span class="sxs-lookup"><span data-stu-id="19757-104">Vendor catalogs import</span></span>

<span data-ttu-id="19757-105">I Dynamics 365 Supply Chain Management kan indkøbsmedarbejderne oprette og vedligeholde kataloger, som virksomhedens medarbejdere derefter kan bruge, når de bestiller varer og tjenesteydelser til intern brug.</span><span class="sxs-lookup"><span data-stu-id="19757-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="19757-106">Hvis du vil oprette et indkøbskatalog, kan du tilføje de varer og tjenester, som du vil gøre tilgængelige for medarbejderne, enten ved at importere produktkataloget eller ved manuelt at tilføje data fra produktkataloget til produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="19757-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="19757-107">Du kan overføre katalogdata, som er indsendt af en kreditor, fra klienten for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="19757-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="19757-108">De produktdata, som en kreditor sender til dig i form af en CMR-fil (Catalog Maintenance Request – anmodning om katalogvedligeholdelse), skal være i filformatet XML.</span><span class="sxs-lookup"><span data-stu-id="19757-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="19757-109">CMR-filen skal indeholde alle oplysninger om de produkter, som kreditoren leverer til dit firma.</span><span class="sxs-lookup"><span data-stu-id="19757-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="19757-110">Importere oplysninger fra et kreditorkatalog</span><span class="sxs-lookup"><span data-stu-id="19757-110">Import vendor catalog data</span></span>

<span data-ttu-id="19757-111">Hvis du vil importere oplysninger fra et kreditorkatalog, skal du fuldføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="19757-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="19757-112">Opret et projekt i det arbejdsområde for Datastyring, hvor du har defineret dine regler for tilknytning af data.</span><span class="sxs-lookup"><span data-stu-id="19757-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="19757-113">Vælg **Datastyring** og derefter **Opsætning af roller for dataprojekter**.</span><span class="sxs-lookup"><span data-stu-id="19757-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="19757-114">Opret et indkøbskategorihierarki, og knyt dine leverandører til bestemte indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="19757-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="19757-115">Hvis du bruger varekoder, skal du føje varekoder til indkøbskategorierne.</span><span class="sxs-lookup"><span data-stu-id="19757-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="19757-116">Du kan finde flere oplysninger om opsætning af et hierarki af indkøbskategorier under [Konfigurere et indkøbskategorihierarki](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="19757-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="19757-117">Konfigurer kreditoren til katalogimport.</span><span class="sxs-lookup"><span data-stu-id="19757-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="19757-118">Vælg en kreditor, og vælg derefter **Indkøb** > **Opsætning** > **Konfigurer kreditor til katalogimport**.</span><span class="sxs-lookup"><span data-stu-id="19757-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="19757-119">Konfigurer arbejdsgangen til katalogimport.</span><span class="sxs-lookup"><span data-stu-id="19757-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="19757-120">Opret en skabelon for CMR-filen, og del den med kreditoren.</span><span class="sxs-lookup"><span data-stu-id="19757-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="19757-121">Vælg **Indkøb og forsyning** \> **Generelt** \> **Kataloger** \> **Kreditorkataloger** for at oprette et kreditorkatalog.</span><span class="sxs-lookup"><span data-stu-id="19757-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="19757-122">De CMR-filer, som du modtager fra leverandøren, grupperes i dette katalog.</span><span class="sxs-lookup"><span data-stu-id="19757-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="19757-123">Overfør CMR-filen.</span><span class="sxs-lookup"><span data-stu-id="19757-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="19757-124">Gennemgå, godkend eller afvis produkterne i kreditorkataloget.</span><span class="sxs-lookup"><span data-stu-id="19757-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="19757-125">Produkterne knyttes automatisk til indkøbskategorierne.</span><span class="sxs-lookup"><span data-stu-id="19757-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="19757-126">Godkendte produkter føjes til produktmasteren og frigives til de valgte juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="19757-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="19757-127">Kun godkendte produkter kan føjes til indkøbskataloget.</span><span class="sxs-lookup"><span data-stu-id="19757-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="19757-128">Generere en filskabelon til katalogimport</span><span class="sxs-lookup"><span data-stu-id="19757-128">Generate a catalog import file template</span></span>

<span data-ttu-id="19757-129">Filskabelonen til katalogimport er en XSD-fil, som du kan bruge til at oprette en CMR-fil til kreditorens produkter.</span><span class="sxs-lookup"><span data-stu-id="19757-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="19757-130">Du kan bruge CMR-filen til at oprette et nyt katalog, erstatte et eksisterende katalog eller redigere et eksisterende katalog.</span><span class="sxs-lookup"><span data-stu-id="19757-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="19757-131">Vælg **Indkøb og forsyning** \> **Kataloger** \> **Kreditorkataloger**, og dobbeltklik på det katalog, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="19757-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="19757-132">Hent den aktuelle katalogimportskabelon (XSD-fil).</span><span class="sxs-lookup"><span data-stu-id="19757-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="19757-133">På siden **Opdater katalog** i **Handlingsrude** på fanen **Kataloger** i gruppen **Relaterede oplysninger** skal du klikke på **Generér skabelon til katalog** og vælge **Indkøbskategori**.</span><span class="sxs-lookup"><span data-stu-id="19757-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="19757-134">Med indstillingen **Indkøbskategori** kan du generere en katalogskabelon, der omfatter de indkøbskategorier, som kreditoren har tilladelse til at levere produkter fra.</span><span class="sxs-lookup"><span data-stu-id="19757-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="19757-135">Vælg **Gem som** i dialogboksen, vælg den placering, hvor du vil gemme katalogfilskabelonen, og gem filen.</span><span class="sxs-lookup"><span data-stu-id="19757-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="19757-136">Yderligere oplysninger og eksempler finder du i dette blogindlæg: [Kreditorkataloger i Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="19757-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
