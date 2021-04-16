---
title: Upload andre filer end billeder og videoer
description: I dette emne beskrives, hvordan du kan uploade andre binære filer end billeder og videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799247"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="3a5db-103">Overføre andre filer end billeder og videoer</span><span class="sxs-lookup"><span data-stu-id="3a5db-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a5db-104">I dette emne beskrives, hvordan du kan uploade andre filer end billeder og videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="3a5db-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="3a5db-105">Mediebiblioteket i Commerce-webstedsgenerator understøtter upload af andre binære aktiver end billeder eller videoer.</span><span class="sxs-lookup"><span data-stu-id="3a5db-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="3a5db-106">Du kan f.eks. uploade Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- eller PDF-filer.</span><span class="sxs-lookup"><span data-stu-id="3a5db-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="3a5db-107">Følgende dokumenttyper understøttes:</span><span class="sxs-lookup"><span data-stu-id="3a5db-107">The following document types are supported:</span></span>
- <span data-ttu-id="3a5db-108">7Z</span><span class="sxs-lookup"><span data-stu-id="3a5db-108">7Z</span></span>
- <span data-ttu-id="3a5db-109">AVI</span><span class="sxs-lookup"><span data-stu-id="3a5db-109">AVI</span></span>
- <span data-ttu-id="3a5db-110">CS</span><span class="sxs-lookup"><span data-stu-id="3a5db-110">CS</span></span>
- <span data-ttu-id="3a5db-111">CSS</span><span class="sxs-lookup"><span data-stu-id="3a5db-111">CSS</span></span>
- <span data-ttu-id="3a5db-112">DOC</span><span class="sxs-lookup"><span data-stu-id="3a5db-112">DOC</span></span>
- <span data-ttu-id="3a5db-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="3a5db-113">DOCX</span></span>
- <span data-ttu-id="3a5db-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="3a5db-114">EPUB</span></span>
- <span data-ttu-id="3a5db-115">GIF</span><span class="sxs-lookup"><span data-stu-id="3a5db-115">GIF</span></span>
- <span data-ttu-id="3a5db-116">INDD</span><span class="sxs-lookup"><span data-stu-id="3a5db-116">INDD</span></span>
- <span data-ttu-id="3a5db-117">JAR</span><span class="sxs-lookup"><span data-stu-id="3a5db-117">JAR</span></span>
- <span data-ttu-id="3a5db-118">JPG</span><span class="sxs-lookup"><span data-stu-id="3a5db-118">JPG</span></span>
- <span data-ttu-id="3a5db-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="3a5db-119">JPEG</span></span>
- <span data-ttu-id="3a5db-120">JS</span><span class="sxs-lookup"><span data-stu-id="3a5db-120">JS</span></span>
- <span data-ttu-id="3a5db-121">MP3</span><span class="sxs-lookup"><span data-stu-id="3a5db-121">MP3</span></span>
- <span data-ttu-id="3a5db-122">MP4</span><span class="sxs-lookup"><span data-stu-id="3a5db-122">MP4</span></span>
- <span data-ttu-id="3a5db-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="3a5db-123">MPEG</span></span>
- <span data-ttu-id="3a5db-124">MPG</span><span class="sxs-lookup"><span data-stu-id="3a5db-124">MPG</span></span>
- <span data-ttu-id="3a5db-125">ODP</span><span class="sxs-lookup"><span data-stu-id="3a5db-125">ODP</span></span>
- <span data-ttu-id="3a5db-126">ODS</span><span class="sxs-lookup"><span data-stu-id="3a5db-126">ODS</span></span>
- <span data-ttu-id="3a5db-127">ODT</span><span class="sxs-lookup"><span data-stu-id="3a5db-127">ODT</span></span>
- <span data-ttu-id="3a5db-128">PDF</span><span class="sxs-lookup"><span data-stu-id="3a5db-128">PDF</span></span>
- <span data-ttu-id="3a5db-129">PNG</span><span class="sxs-lookup"><span data-stu-id="3a5db-129">PNG</span></span>
- <span data-ttu-id="3a5db-130">PPT</span><span class="sxs-lookup"><span data-stu-id="3a5db-130">PPT</span></span>
- <span data-ttu-id="3a5db-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="3a5db-131">PPTX</span></span>
- <span data-ttu-id="3a5db-132">PS</span><span class="sxs-lookup"><span data-stu-id="3a5db-132">PS</span></span>
- <span data-ttu-id="3a5db-133">QXP</span><span class="sxs-lookup"><span data-stu-id="3a5db-133">QXP</span></span>
- <span data-ttu-id="3a5db-134">RAR</span><span class="sxs-lookup"><span data-stu-id="3a5db-134">RAR</span></span>
- <span data-ttu-id="3a5db-135">RTF</span><span class="sxs-lookup"><span data-stu-id="3a5db-135">RTF</span></span>
- <span data-ttu-id="3a5db-136">SVG</span><span class="sxs-lookup"><span data-stu-id="3a5db-136">SVG</span></span>
- <span data-ttu-id="3a5db-137">TAR</span><span class="sxs-lookup"><span data-stu-id="3a5db-137">TAR</span></span>
- <span data-ttu-id="3a5db-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="3a5db-138">TGZ</span></span>
- <span data-ttu-id="3a5db-139">TXT</span><span class="sxs-lookup"><span data-stu-id="3a5db-139">TXT</span></span>
- <span data-ttu-id="3a5db-140">WMV</span><span class="sxs-lookup"><span data-stu-id="3a5db-140">WMV</span></span>
- <span data-ttu-id="3a5db-141">XLS</span><span class="sxs-lookup"><span data-stu-id="3a5db-141">XLS</span></span>
- <span data-ttu-id="3a5db-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="3a5db-142">XLSX</span></span>
- <span data-ttu-id="3a5db-143">XML</span><span class="sxs-lookup"><span data-stu-id="3a5db-143">XML</span></span>
- <span data-ttu-id="3a5db-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="3a5db-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="3a5db-145">Overfør en fil</span><span class="sxs-lookup"><span data-stu-id="3a5db-145">Upload a file</span></span>

<span data-ttu-id="3a5db-146">Følg disse trin for at uploade en fil til Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="3a5db-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3a5db-147">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="3a5db-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3a5db-148">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="3a5db-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3a5db-149">Vælg en eller flere filer i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="3a5db-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="3a5db-150">Angiv titel, beskrivelse og nøgleordsmetadata i dialogboksen **Upload medieelement** efter behov.</span><span class="sxs-lookup"><span data-stu-id="3a5db-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="3a5db-151">Hvis du vil udgive en eller flere filer umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="3a5db-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="3a5db-152">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a5db-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a5db-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3a5db-153">Additional resources</span></span>

[<span data-ttu-id="3a5db-154">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="3a5db-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3a5db-155">Overføre billeder</span><span class="sxs-lookup"><span data-stu-id="3a5db-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3a5db-156">Overføre video</span><span class="sxs-lookup"><span data-stu-id="3a5db-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="3a5db-157">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="3a5db-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3a5db-158">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="3a5db-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="3a5db-159">Overføre og håndtere statiske filer</span><span class="sxs-lookup"><span data-stu-id="3a5db-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
