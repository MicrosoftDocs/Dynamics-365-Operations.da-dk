---
title: ER-destinationstype for arkiv
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en arkivdestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72b896ca692a54200ff79b14d0b5dc6ab4b0fe27
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562040"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="5cbaf-103">ER-destinationstype for arkiv</span><span class="sxs-lookup"><span data-stu-id="5cbaf-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cbaf-104">Du kan konfigurere en arkivdestination for hver komponent af typen **Mappe** eller **Fil** i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="5cbaf-105">På baggrund af destinationsindstillingen gemmes et genereret dokument som en vedhæftet fil til en post på ER-joblisten.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="5cbaf-106">Du kan få vist resultaterne ved at gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Elektronisk rapportering af job**.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="5cbaf-107">Du kan bruge denne indstilling til at sende det genererede dokument til en Microsoft SharePoint-mappe eller Microsoft Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="5cbaf-108">Indstil **Aktiveret** til **Ja** for at sende output til en destination, der er defineret af den valgte dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="5cbaf-109">Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="5cbaf-110">Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) i **Organisationsadministration** \> **Dokumentstyring** \> **Dokumenttyper**.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="5cbaf-111">Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="5cbaf-112">[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="5cbaf-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="5cbaf-113">Lokaliteten bestemmer, hvor filen gemmes.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-113">The location determines where the file is saved.</span></span> <span data-ttu-id="5cbaf-114">Når destinationen **Arkiv** er aktiveret, kan resultaterne gemmes i jobarkivet.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="5cbaf-115">Du kan få vist resultaterne i **Virksomhedsadministration** \> **elektronisk rapportering** \> **Elektronisk rapportering af arkiverede job**.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="5cbaf-116">Vælg en dokumenttype til jobarkivet ved at navigere til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering** \> **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="5cbaf-117">Du kan finde flere oplysninger under [Konfigurere den elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="5cbaf-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="5cbaf-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="5cbaf-118">SharePoint</span></span>

<span data-ttu-id="5cbaf-119">Du kan gemme en fil i en angivet SharePoint-mappe.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="5cbaf-120">Når du vil definere SharePoint-standardserveren, skal du gå til **Organisationsadministration** \> **Dokumentstyring** \> **Dokumentstyringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="5cbaf-121">Under fanen **SharePoint** skal du konfigurere SharePoint-mappen.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="5cbaf-122">Derefter kan du vælge den som den mappe, hvor ER-outputtet skal gemmes.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="5cbaf-123">**SharePoint**-placeringen skal vælges i denne dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="5cbaf-124">[![Valg af en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="5cbaf-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="5cbaf-125">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="5cbaf-125">Azure Storage</span></span>

<span data-ttu-id="5cbaf-126">Når dokumenttypens placering er angivet til **Azure-lager**, kan du gemme en fil på Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="5cbaf-127">ER-strukturen gemmer filer i Azure Blob Storage permanent i modsætning til dataadministrationsstrukturen, der anvender den syv-dages opbevaringspolitik for dokumenter, der skal behandles.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="5cbaf-128">Du kan finde flere oplysninger under [API til hentning af meddelelsesstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [API til statuskontrol](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="5cbaf-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="5cbaf-129">De ER-relaterede filer gemmes i Azure Blob Storage som vedhæftede filer i programtabelposter, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="5cbaf-130">En enkelt fil slettet fra Azure Blob Storage sammen med den programtabelpost, som denne fil var knyttet til.</span><span class="sxs-lookup"><span data-stu-id="5cbaf-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cbaf-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5cbaf-131">Additional resources</span></span>

- [<span data-ttu-id="5cbaf-132">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="5cbaf-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5cbaf-133">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="5cbaf-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="5cbaf-134">Konfigurere dokumentstyring</span><span class="sxs-lookup"><span data-stu-id="5cbaf-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]