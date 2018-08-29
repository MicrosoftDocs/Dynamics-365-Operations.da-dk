---
title: Importere data fra Excel-dataenhedsskabeloner, der har flere regneark
description: "I dette emne beskrives, hvordan du kan importere data ved hjælp af Excel-dataenhedsskabeloner i Microsoft Dynamics 365 for Finance and Operations."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5bc021ce9f0835f2eda310ef7818c9bc9be749f2
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="fb5cc-103">Importere data fra Excel-dataenhedsskabeloner, der har flere regneark</span><span class="sxs-lookup"><span data-stu-id="fb5cc-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb5cc-104">Administration af data i Microsoft Dynamics 365 for Finance and Operations understøtter Microsoft Excel-baserede skabeloner til dataenheder.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="fb5cc-105">Disse skabeloner kan indeholde et eller flere regneark.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="fb5cc-106">Skabeloner med flere regneark bruges ofte, når det passer til at administrere data i en enkelt fil og importere den til flere dataenheder.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="fb5cc-107">Et eksempel er lokationer og lagersteder.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="fb5cc-108">Overføre en fil én gang og knytte den til alle enheder</span><span class="sxs-lookup"><span data-stu-id="fb5cc-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="fb5cc-109">Lad os tage et eksempel, hvor der er én Excel-fil med regnearkene **Lokationer** og **Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="fb5cc-110">For at konfigurere dataimportprojektet skal du tilføje den første dataenhed **Lokationer** og derefter overføre filen.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="fb5cc-111">Du kan vælge **Lokationer** som det regneark, der skal bruges til denne enhed.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="fb5cc-112">Hvis du tilføjer den anden enhed, **Lagersteder**, uden at forlade formularen **Tilføj fil**, gør regnearksopslaget det muligt for dig at vælge regnearket **Lagersteder** uden at skulle overføre filen igen.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="fb5cc-113">Den eneste grund til at overføre en ny fil er, hvis **Lagersteder**-dataene er i en anden fil.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Flere regneark](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="fb5cc-115">Rette regneark til enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="fb5cc-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="fb5cc-116">Tilknytningen af regnearket til en dataenhed i importjobbet kan rettes i gitteret.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="fb5cc-117">Kolonnen **Regneark** i gitteret viser de regneark fra den fil, der blev tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="fb5cc-118">Du kan vælge et andet regneark i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="fb5cc-119">Hvis det valgte regneark allerede er knyttet til en enhed i dataprojektet, beder systemet dig om at bekræfte ændringen.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="fb5cc-120">Det anbefales, at du retter alle tilknytninger i gitteret.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-120">We recommend that you fix all mappings in the grid.</span></span>

![Opdatere tilknytning af regneark](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="fb5cc-122">Tilknytte igen til en ny fil</span><span class="sxs-lookup"><span data-stu-id="fb5cc-122">Re-map to a new file</span></span>

<span data-ttu-id="fb5cc-123">I tilfælde, hvor der skal overføres en ny version af den samme fil eller en helt ny fil til eksisterende objekter i et dataprojekt, skal du bruge **Tilføj fil**-oplevelsen og tilføje enhederne igen, som om de blev tilføjet for første gang.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="fb5cc-124">Systemet bekræfter, at du vil overskrive de eksisterende enheder i dataprojektet, før du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="fb5cc-125">Enheder, der ikke tilføjes igen (eller overskrives) fortsætter med at have de tidligere tilknytninger fra den tidligere fil.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="fb5cc-126">Overføre en fil ved hjælp af Kør projekt</span><span class="sxs-lookup"><span data-stu-id="fb5cc-126">Upload a file using Run project</span></span>

<span data-ttu-id="fb5cc-127">Du kan overføre en Excel-fil, mens du bruger indstillingen **Kør projekt** til at udføre et importprojekt.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="fb5cc-128">Du skal være omhyggelig med kun at overføre de filer, der har de samme regneark som de eksisterende tilknytninger på dataenhederne i dataprojektet.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="fb5cc-129">Hvis der ikke findes et regneark i den fil, der netop er overført, vises der en fejlmeddelelse i systemet, og importen stopper.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="fb5cc-130">Hvis tilknytningen til regnearket skal ændres for et objekt, skal tilknytningerne i dataprojektet først opdateres fra dataprojektet, før du kan bruge filen i **Kør projekt**-oplevelsen.</span><span class="sxs-lookup"><span data-stu-id="fb5cc-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


