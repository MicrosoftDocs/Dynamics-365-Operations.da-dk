---
title: Upload andre filer end billeder og videoer
description: I dette emne beskrives, hvordan du kan uploade andre binære filer end billeder og videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
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
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096988"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="dc031-103">Upload andre filer end billeder og videoer</span><span class="sxs-lookup"><span data-stu-id="dc031-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc031-104">I dette emne beskrives, hvordan du kan uploade andre filer end billeder og videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="dc031-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="dc031-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="dc031-105">Overview</span></span>

<span data-ttu-id="dc031-106">Mediebiblioteket i Commerce-webstedsgenerator understøtter upload af andre binære aktiver end billeder eller videoer.</span><span class="sxs-lookup"><span data-stu-id="dc031-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="dc031-107">Du kan f.eks. uploade Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- eller PDF-filer.</span><span class="sxs-lookup"><span data-stu-id="dc031-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="dc031-108">Følgende dokumenttyper understøttes:</span><span class="sxs-lookup"><span data-stu-id="dc031-108">The following document types are supported:</span></span>
- <span data-ttu-id="dc031-109">7Z</span><span class="sxs-lookup"><span data-stu-id="dc031-109">7Z</span></span>
- <span data-ttu-id="dc031-110">AVI</span><span class="sxs-lookup"><span data-stu-id="dc031-110">AVI</span></span>
- <span data-ttu-id="dc031-111">CS</span><span class="sxs-lookup"><span data-stu-id="dc031-111">CS</span></span>
- <span data-ttu-id="dc031-112">CSS</span><span class="sxs-lookup"><span data-stu-id="dc031-112">CSS</span></span>
- <span data-ttu-id="dc031-113">DOC</span><span class="sxs-lookup"><span data-stu-id="dc031-113">DOC</span></span>
- <span data-ttu-id="dc031-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="dc031-114">DOCX</span></span>
- <span data-ttu-id="dc031-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="dc031-115">EPUB</span></span>
- <span data-ttu-id="dc031-116">GIF</span><span class="sxs-lookup"><span data-stu-id="dc031-116">GIF</span></span>
- <span data-ttu-id="dc031-117">INDD</span><span class="sxs-lookup"><span data-stu-id="dc031-117">INDD</span></span>
- <span data-ttu-id="dc031-118">JAR</span><span class="sxs-lookup"><span data-stu-id="dc031-118">JAR</span></span>
- <span data-ttu-id="dc031-119">JPG</span><span class="sxs-lookup"><span data-stu-id="dc031-119">JPG</span></span>
- <span data-ttu-id="dc031-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="dc031-120">JPEG</span></span>
- <span data-ttu-id="dc031-121">JS</span><span class="sxs-lookup"><span data-stu-id="dc031-121">JS</span></span>
- <span data-ttu-id="dc031-122">MP3</span><span class="sxs-lookup"><span data-stu-id="dc031-122">MP3</span></span>
- <span data-ttu-id="dc031-123">MP4</span><span class="sxs-lookup"><span data-stu-id="dc031-123">MP4</span></span>
- <span data-ttu-id="dc031-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="dc031-124">MPEG</span></span>
- <span data-ttu-id="dc031-125">MPG</span><span class="sxs-lookup"><span data-stu-id="dc031-125">MPG</span></span>
- <span data-ttu-id="dc031-126">ODP</span><span class="sxs-lookup"><span data-stu-id="dc031-126">ODP</span></span>
- <span data-ttu-id="dc031-127">ODS</span><span class="sxs-lookup"><span data-stu-id="dc031-127">ODS</span></span>
- <span data-ttu-id="dc031-128">ODT</span><span class="sxs-lookup"><span data-stu-id="dc031-128">ODT</span></span>
- <span data-ttu-id="dc031-129">PDF</span><span class="sxs-lookup"><span data-stu-id="dc031-129">PDF</span></span>
- <span data-ttu-id="dc031-130">PNG</span><span class="sxs-lookup"><span data-stu-id="dc031-130">PNG</span></span>
- <span data-ttu-id="dc031-131">PPT</span><span class="sxs-lookup"><span data-stu-id="dc031-131">PPT</span></span>
- <span data-ttu-id="dc031-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="dc031-132">PPTX</span></span>
- <span data-ttu-id="dc031-133">PS</span><span class="sxs-lookup"><span data-stu-id="dc031-133">PS</span></span>
- <span data-ttu-id="dc031-134">QXP</span><span class="sxs-lookup"><span data-stu-id="dc031-134">QXP</span></span>
- <span data-ttu-id="dc031-135">RAR</span><span class="sxs-lookup"><span data-stu-id="dc031-135">RAR</span></span>
- <span data-ttu-id="dc031-136">RTF</span><span class="sxs-lookup"><span data-stu-id="dc031-136">RTF</span></span>
- <span data-ttu-id="dc031-137">SVG</span><span class="sxs-lookup"><span data-stu-id="dc031-137">SVG</span></span>
- <span data-ttu-id="dc031-138">TAR</span><span class="sxs-lookup"><span data-stu-id="dc031-138">TAR</span></span>
- <span data-ttu-id="dc031-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="dc031-139">TGZ</span></span>
- <span data-ttu-id="dc031-140">TXT</span><span class="sxs-lookup"><span data-stu-id="dc031-140">TXT</span></span>
- <span data-ttu-id="dc031-141">WMV</span><span class="sxs-lookup"><span data-stu-id="dc031-141">WMV</span></span>
- <span data-ttu-id="dc031-142">XLS</span><span class="sxs-lookup"><span data-stu-id="dc031-142">XLS</span></span>
- <span data-ttu-id="dc031-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="dc031-143">XLSX</span></span>
- <span data-ttu-id="dc031-144">XML</span><span class="sxs-lookup"><span data-stu-id="dc031-144">XML</span></span>
- <span data-ttu-id="dc031-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="dc031-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="dc031-146">Overfør en fil</span><span class="sxs-lookup"><span data-stu-id="dc031-146">Upload a file</span></span>

<span data-ttu-id="dc031-147">Følg disse trin for at uploade en fil til Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="dc031-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dc031-148">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="dc031-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="dc031-149">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="dc031-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="dc031-150">Vælg en eller flere filer i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="dc031-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="dc031-151">Angiv titel, beskrivelse og nøgleordsmetadata i dialogboksen **Upload medieelement** efter behov.</span><span class="sxs-lookup"><span data-stu-id="dc031-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="dc031-152">Hvis du vil udgive en eller flere filer umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .</span><span class="sxs-lookup"><span data-stu-id="dc031-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="dc031-153">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc031-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc031-154">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dc031-154">Additional resources</span></span>

[<span data-ttu-id="dc031-155">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="dc031-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="dc031-156">Uploade billeder</span><span class="sxs-lookup"><span data-stu-id="dc031-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="dc031-157">Uploade video</span><span class="sxs-lookup"><span data-stu-id="dc031-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="dc031-158">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="dc031-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="dc031-159">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="dc031-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
