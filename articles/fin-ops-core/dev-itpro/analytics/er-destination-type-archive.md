---
title: ER-destinationstype for arkiv
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere en arkivdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745579"
---
# <a name="archive-destination"></a><span data-ttu-id="6dfd3-103">Arkivdestination</span><span class="sxs-lookup"><span data-stu-id="6dfd3-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dfd3-104">Du kan konfigurere en arkivdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="6dfd3-105">På baggrund af destinationsindstillingen gemmes et genereret dokument som en vedhæftet fil til en post på ER-joblisten.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="6dfd3-106">Du kan bruge denne indstilling til at sende det genererede dokument til en Microsoft SharePoint-mappe eller Microsoft Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="6dfd3-107">Indstil **Aktiveret** til **Ja** for at sende output til en destination, der er defineret af den valgte dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="6dfd3-108">Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="6dfd3-109">Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) i **Organisationsadministration** \> **Dokumentstyring** \> **Dokumenttyper**.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="6dfd3-110">Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="6dfd3-111">[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="6dfd3-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="6dfd3-112">Lokaliteten bestemmer, hvor filen gemmes.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-112">The location determines where the file is saved.</span></span> <span data-ttu-id="6dfd3-113">Når destinationen **Arkiv** er aktiveret, kan resultaterne gemmes i jobarkivet.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="6dfd3-114">Du kan få vist resultaterne i **Virksomhedsadministration** \> **elektronisk rapportering** \> **Elektronisk rapportering af arkiverede job**.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="6dfd3-115">Vælg en dokumenttype til jobarkivet ved at navigere til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering** \> **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="6dfd3-116">Du kan finde flere oplysninger under [Konfigurere den elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="6dfd3-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="6dfd3-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="6dfd3-117">SharePoint</span></span>

<span data-ttu-id="6dfd3-118">Du kan gemme en fil i en angivet SharePoint-mappe.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="6dfd3-119">Når du vil definere SharePoint-standardserveren, skal du gå til **Organisationsadministration** \> **Dokumentstyring** \> **Dokumentstyringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="6dfd3-120">Under fanen **SharePoint** skal du konfigurere SharePoint-mappen.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="6dfd3-121">Derefter kan du vælge den som den mappe, hvor ER-outputtet skal gemmes.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="6dfd3-122">**SharePoint**-placeringen skal vælges i denne dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="6dfd3-123">[![Valg af en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="6dfd3-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="6dfd3-124">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="6dfd3-124">Azure Storage</span></span>

<span data-ttu-id="6dfd3-125">Når dokumenttypens placering er angivet til **Azure-lager**, kan du gemme en fil på Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6dfd3-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dfd3-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6dfd3-126">Additional resources</span></span>

- [<span data-ttu-id="6dfd3-127">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="6dfd3-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6dfd3-128">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="6dfd3-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="6dfd3-129">Konfigurere dokumentstyring</span><span class="sxs-lookup"><span data-stu-id="6dfd3-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
