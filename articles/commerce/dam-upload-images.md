---
title: Overføre billeder
description: I dette emne beskrives, hvordan du overfører billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799223"
---
# <a name="upload-images"></a><span data-ttu-id="10ef4-103">Overføre billeder</span><span class="sxs-lookup"><span data-stu-id="10ef4-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10ef4-104">I dette emne beskrives, hvordan du overfører billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="10ef4-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="10ef4-105">I Commerce-webstedsgeneratorens mediebibliotek kan du uploade billeder enkeltvist eller masseupload ved hjælp af mapper.</span><span class="sxs-lookup"><span data-stu-id="10ef4-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="10ef4-106">Du bør altid uploade billedet med den højeste opløsning og kvalitet, da funktionen til tilpasning af billedstørrelsen optimerer automatisk billedet for forskellige billeder og pausepunkterne.</span><span class="sxs-lookup"><span data-stu-id="10ef4-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="10ef4-107">Billedoplysninger, der er angivet under upload</span><span class="sxs-lookup"><span data-stu-id="10ef4-107">Image information specified during upload</span></span>

<span data-ttu-id="10ef4-108">Når du uploader et billede, kan du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="10ef4-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="10ef4-109">**Titel, Alternativ tekst, Beskrivelse, Nøgleord**: Metadata for billedet eller billederne.</span><span class="sxs-lookup"><span data-stu-id="10ef4-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="10ef4-110">Titel og alternativ tekst er obligatoriske værdier.</span><span class="sxs-lookup"><span data-stu-id="10ef4-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="10ef4-111">**Vælg kategori**:</span><span class="sxs-lookup"><span data-stu-id="10ef4-111">**Select category**:</span></span>
    - <span data-ttu-id="10ef4-112">**Ingen**: Bruges til en e-handelsbilledhistorie eller -billeder.</span><span class="sxs-lookup"><span data-stu-id="10ef4-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="10ef4-113">**Produkt, Kategori, Kunde, Medarbejder, Katalog**: Bruges til Dynamics 365 Commerce-omni-kanalbillede eller -billeder.</span><span class="sxs-lookup"><span data-stu-id="10ef4-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="10ef4-114">**Publicer aktiver efter upload**: Når dette afkrydsningsfelt er markeret, udgives billedet eller billederne straks efter upload.</span><span class="sxs-lookup"><span data-stu-id="10ef4-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="10ef4-115">Billedaktiver med en tildelt kategori mærkes også automatisk med kategorien som et nøgleord for at hjælpe med at søge efter aktiver af en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="10ef4-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="10ef4-116">Navngivningskonventioner for omni-kanalbilleder</span><span class="sxs-lookup"><span data-stu-id="10ef4-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="10ef4-117">Hvis du har konfigureret mediebiblioteket som back-end for omni-kanalbilledet, kan du bruge billedkategorier til at angive, hvilken kategori det uploadede billede tilhører.</span><span class="sxs-lookup"><span data-stu-id="10ef4-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="10ef4-118">Der findes også en navngivningsregel, der skal følges for at sikre, at billeder hentes korrekt af andre kanaler, f.eks. POS (Point Of Sale).</span><span class="sxs-lookup"><span data-stu-id="10ef4-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="10ef4-119">Standardnavngivningskonventionen varierer, afhængigt af kategorien:</span><span class="sxs-lookup"><span data-stu-id="10ef4-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="10ef4-120">Katalogbilleder skal navngives "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="10ef4-121">Kategoribilleder skal navngives "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="10ef4-122">Kundebilleder skal navngives "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="10ef4-123">Medarbejderbilleder skal navngives "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="10ef4-124">Produktbilleder skal navngives "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="10ef4-125">001 er rækkefølgen af billedet, og det kan være 001, 002, 003, 004 eller 005</span><span class="sxs-lookup"><span data-stu-id="10ef4-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="10ef4-126">Produktvariantbilleder skal navngives "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="10ef4-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="10ef4-127">For eksempel: 93039 \^ \^ 2 \^ Black \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="10ef4-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="10ef4-128">Upload et billede</span><span class="sxs-lookup"><span data-stu-id="10ef4-128">Upload an image</span></span>

<span data-ttu-id="10ef4-129">Følg disse trin for at uploade et billede i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="10ef4-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="10ef4-130">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="10ef4-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="10ef4-131">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="10ef4-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="10ef4-132">Naviger til og vælg en eller flere billedfiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="10ef4-133">Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="10ef4-134">Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori.</span><span class="sxs-lookup"><span data-stu-id="10ef4-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="10ef4-135">Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="10ef4-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="10ef4-136">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="10ef4-137">Uploade en mappe med billeder</span><span class="sxs-lookup"><span data-stu-id="10ef4-137">Upload a folder of images</span></span>

<span data-ttu-id="10ef4-138">Følg disse trin for at masseuploade en mappe med billeder i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="10ef4-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="10ef4-139">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="10ef4-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="10ef4-140">Vælg **Upload \> Uploadmappe** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="10ef4-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="10ef4-141">Naviger til, og vælg en mappe, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="10ef4-142">Angiv valgfrie nøgleord, og vælg en kategori efter behov i dialogboksen **Upload medieelementer**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="10ef4-143">Hvis du vil udgive billederne i en mappe umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="10ef4-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="10ef4-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ef4-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10ef4-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="10ef4-145">Additional resources</span></span>

[<span data-ttu-id="10ef4-146">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="10ef4-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="10ef4-147">Overføre video</span><span class="sxs-lookup"><span data-stu-id="10ef4-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="10ef4-148">Uploade filer</span><span class="sxs-lookup"><span data-stu-id="10ef4-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="10ef4-149">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="10ef4-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="10ef4-150">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="10ef4-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="10ef4-151">Overføre og håndtere statiske filer</span><span class="sxs-lookup"><span data-stu-id="10ef4-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
