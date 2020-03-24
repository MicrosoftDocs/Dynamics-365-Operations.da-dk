---
title: Uploade billeder
description: Dette emne indeholder en beskrivelse af, hvordan du uploader billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096989"
---
# <a name="upload-images"></a><span data-ttu-id="db600-103">Uploade billeder</span><span class="sxs-lookup"><span data-stu-id="db600-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db600-104">Dette emne indeholder en beskrivelse af, hvordan du uploader billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="db600-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="db600-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="db600-105">Overview</span></span>

<span data-ttu-id="db600-106">I Commerce-webstedsgeneratorens mediebibliotek kan du uploade billeder enkeltvist eller masseupload ved hjælp af mapper.</span><span class="sxs-lookup"><span data-stu-id="db600-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="db600-107">Du bør altid uploade billedet med den højeste opløsning og kvalitet, da funktionen til tilpasning af billedstørrelsen optimerer automatisk billedet for forskellige billeder og pausepunkterne.</span><span class="sxs-lookup"><span data-stu-id="db600-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="db600-108">Billedoplysninger, der er angivet under upload</span><span class="sxs-lookup"><span data-stu-id="db600-108">Image information specified during upload</span></span>

<span data-ttu-id="db600-109">Når du uploader et billede, kan du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="db600-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="db600-110">**Titel, Alternativ tekst, Beskrivelse, Nøgleord**: Metadata for billedet eller billederne.</span><span class="sxs-lookup"><span data-stu-id="db600-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="db600-111">Titel og alternativ tekst er obligatoriske værdier.</span><span class="sxs-lookup"><span data-stu-id="db600-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="db600-112">**Vælg kategori**:</span><span class="sxs-lookup"><span data-stu-id="db600-112">**Select category**:</span></span>
    - <span data-ttu-id="db600-113">**Ingen**: Bruges til en e-handelsbilledhistorie eller -billeder.</span><span class="sxs-lookup"><span data-stu-id="db600-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="db600-114">**Produkt, Kategori, Kunde, Medarbejder, Katalog**: Bruges til Dynamics 365 Commerce-omni-kanalbillede eller -billeder.</span><span class="sxs-lookup"><span data-stu-id="db600-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="db600-115">**Publicer aktiver efter upload**: Når dette afkrydsningsfelt er markeret, udgives billedet eller billederne straks efter upload.</span><span class="sxs-lookup"><span data-stu-id="db600-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="db600-116">Billedaktiver med en tildelt kategori mærkes også automatisk med kategorien som et nøgleord for at hjælpe med at søge efter aktiver af en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="db600-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="db600-117">Navngivningskonventioner for omni-kanalbilleder</span><span class="sxs-lookup"><span data-stu-id="db600-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="db600-118">Hvis du har konfigureret mediebiblioteket som back-end for omni-kanalbilledet, kan du bruge billedkategorier til at angive, hvilken kategori det uploadede billede tilhører.</span><span class="sxs-lookup"><span data-stu-id="db600-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="db600-119">Der findes også en navngivningsregel, der skal følges for at sikre, at billeder hentes korrekt af andre kanaler, f.eks. POS (Point Of Sale).</span><span class="sxs-lookup"><span data-stu-id="db600-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="db600-120">Standardnavngivningskonventionen varierer, afhængigt af kategorien:</span><span class="sxs-lookup"><span data-stu-id="db600-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="db600-121">Katalogbilleder skal navngives "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="db600-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="db600-122">Kategoribilleder skal navngives "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="db600-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="db600-123">Kundebilleder skal navngives "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="db600-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="db600-124">Medarbejderbilleder skal navngives "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="db600-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="db600-125">Produktbilleder skal navngives "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="db600-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="db600-126">001 er rækkefølgen af billedet, og det kan være 001, 002, 003, 004 eller 005</span><span class="sxs-lookup"><span data-stu-id="db600-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="db600-127">Produktvariantbilleder skal navngives "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="db600-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="db600-128">Upload et billede</span><span class="sxs-lookup"><span data-stu-id="db600-128">Upload an image</span></span>

<span data-ttu-id="db600-129">Følg disse trin for at uploade et billede i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="db600-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db600-130">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="db600-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="db600-131">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="db600-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="db600-132">Naviger til og vælg en eller flere billedfiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="db600-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="db600-133">Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.</span><span class="sxs-lookup"><span data-stu-id="db600-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="db600-134">Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori.</span><span class="sxs-lookup"><span data-stu-id="db600-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="db600-135">Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="db600-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="db600-136">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="db600-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="db600-137">Uploade en mappe med billeder</span><span class="sxs-lookup"><span data-stu-id="db600-137">Upload a folder of images</span></span>

<span data-ttu-id="db600-138">Følg disse trin for at masseuploade en mappe med billeder i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="db600-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db600-139">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="db600-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="db600-140">Vælg **Upload \> Uploadmappe** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="db600-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="db600-141">Naviger til, og vælg en mappe, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="db600-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="db600-142">Angiv valgfrie nøgleord, og vælg en kategori efter behov i dialogboksen **Upload medieelementer**.</span><span class="sxs-lookup"><span data-stu-id="db600-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="db600-143">Hvis du vil udgive billederne i en mappe umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="db600-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="db600-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="db600-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db600-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="db600-145">Additional resources</span></span>

[<span data-ttu-id="db600-146">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="db600-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="db600-147">Uploade video</span><span class="sxs-lookup"><span data-stu-id="db600-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="db600-148">Uploade filer</span><span class="sxs-lookup"><span data-stu-id="db600-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="db600-149">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="db600-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="db600-150">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="db600-150">Customize image focal points</span></span>](dam-custom-focal-point.md)
