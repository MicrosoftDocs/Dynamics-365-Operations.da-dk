---
title: Uploade videoer
description: I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
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
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799199"
---
# <a name="upload-videos"></a><span data-ttu-id="587fc-103">Uploade videoer</span><span class="sxs-lookup"><span data-stu-id="587fc-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="587fc-104">I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="587fc-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="587fc-105">Mediebiblioteket i Commerce-webstedsgenerator giver dig mulighed for at uploade videoer.</span><span class="sxs-lookup"><span data-stu-id="587fc-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="587fc-106">Du bør altid uploade versionen af videoen med den højeste bithastighed og opløsning, da videoen automatisk vil blive konverteret til at være passende for forskellige billeder og deres pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="587fc-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="587fc-107">Videooplysninger, der er angivet under upload</span><span class="sxs-lookup"><span data-stu-id="587fc-107">Video information specified during upload</span></span>

<span data-ttu-id="587fc-108">Når du uploader en video, kan du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="587fc-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="587fc-109">**Titel, Beskrivelse, Nøgleord**: Videoens metadata.</span><span class="sxs-lookup"><span data-stu-id="587fc-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="587fc-110">**Generer undertekster automatisk**: Angiver, om der automatisk skal genereres undertekster til videoen.</span><span class="sxs-lookup"><span data-stu-id="587fc-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="587fc-111">**Undertekster**: Angiver, om undertekster skal bruges.</span><span class="sxs-lookup"><span data-stu-id="587fc-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="587fc-112">**Almindeligt lydsignal**: Angiver det almindelige lydspor, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="587fc-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="587fc-113">**Miniaturebillede**: Angiver miniaturebilledet for videoen.</span><span class="sxs-lookup"><span data-stu-id="587fc-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="587fc-114">Hvis miniaturebilledet ikke angives, genereres det automatisk.</span><span class="sxs-lookup"><span data-stu-id="587fc-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="587fc-115">**Beskrivende lyd**: Angiver det beskrivende lydspor, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="587fc-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="587fc-116">Uploade en video</span><span class="sxs-lookup"><span data-stu-id="587fc-116">Upload a video</span></span>

<span data-ttu-id="587fc-117">Følg disse trin for at uploade en video i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="587fc-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="587fc-118">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="587fc-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="587fc-119">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="587fc-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="587fc-120">Naviger til og vælg en eller flere videofiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="587fc-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="587fc-121">Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.</span><span class="sxs-lookup"><span data-stu-id="587fc-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="587fc-122">Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori.</span><span class="sxs-lookup"><span data-stu-id="587fc-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="587fc-123">Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload**</span><span class="sxs-lookup"><span data-stu-id="587fc-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="587fc-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="587fc-124">Select **OK**.</span></span>

<span data-ttu-id="587fc-125">Hvis du uploader flere typer aktiver på én gang (f.eks. billeder og videoer), kan du kun angive nøgleord i dialogboksen **Upload medieelement**, uanset om filerne skal udgives umiddelbart efter upload, og om der automatisk skal genereres undertekster til videofiler.</span><span class="sxs-lookup"><span data-stu-id="587fc-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="587fc-126">Alle aktiverne vil dele de samme nøgleord.</span><span class="sxs-lookup"><span data-stu-id="587fc-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="587fc-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="587fc-127">Additional resources</span></span>

[<span data-ttu-id="587fc-128">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="587fc-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="587fc-129">Overføre billeder</span><span class="sxs-lookup"><span data-stu-id="587fc-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="587fc-130">Uploade filer</span><span class="sxs-lookup"><span data-stu-id="587fc-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="587fc-131">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="587fc-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="587fc-132">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="587fc-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="587fc-133">Overføre og håndtere statiske filer</span><span class="sxs-lookup"><span data-stu-id="587fc-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
