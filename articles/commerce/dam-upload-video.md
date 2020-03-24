---
title: Uploade videoer
description: Dette emne indeholder en beskrivelse af, hvordan du uploader videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
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
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096991"
---
# <a name="upload-videos"></a><span data-ttu-id="f513d-103">Uploade videoer</span><span class="sxs-lookup"><span data-stu-id="f513d-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f513d-104">Dette emne indeholder en beskrivelse af, hvordan du uploader videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="f513d-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="f513d-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="f513d-105">Overview</span></span>

<span data-ttu-id="f513d-106">Mediebiblioteket i Commerce-webstedsgenerator giver dig mulighed for at uploade videoer.</span><span class="sxs-lookup"><span data-stu-id="f513d-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="f513d-107">Du bør altid uploade versionen af videoen med den højeste bithastighed og opløsning, da videoen automatisk vil blive konverteret til at være passende for forskellige billeder og deres pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="f513d-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="f513d-108">Videooplysninger, der er angivet under upload</span><span class="sxs-lookup"><span data-stu-id="f513d-108">Video information specified during upload</span></span>

<span data-ttu-id="f513d-109">Når du uploader en video, kan du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f513d-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="f513d-110">**Titel, Beskrivelse, Nøgleord**: Videoens metadata.</span><span class="sxs-lookup"><span data-stu-id="f513d-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="f513d-111">**Generer undertekster automatisk**: Angiver, om der automatisk skal genereres undertekster til videoen.</span><span class="sxs-lookup"><span data-stu-id="f513d-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="f513d-112">**Undertekster**: Angiver, om undertekster skal bruges.</span><span class="sxs-lookup"><span data-stu-id="f513d-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="f513d-113">**Almindeligt lydsignal**: Angiver det almindelige lydspor, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="f513d-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="f513d-114">**Miniaturebillede**: Angiver miniaturebilledet for videoen.</span><span class="sxs-lookup"><span data-stu-id="f513d-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="f513d-115">Hvis miniaturebilledet ikke angives, genereres det automatisk.</span><span class="sxs-lookup"><span data-stu-id="f513d-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="f513d-116">**Beskrivende lyd**: Angiver det beskrivende lydspor, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="f513d-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="f513d-117">Uploade en video</span><span class="sxs-lookup"><span data-stu-id="f513d-117">Upload a video</span></span>

<span data-ttu-id="f513d-118">Følg disse trin for at uploade en video i webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="f513d-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="f513d-119">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="f513d-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f513d-120">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="f513d-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="f513d-121">Naviger til og vælg en eller flere videofiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="f513d-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="f513d-122">Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.</span><span class="sxs-lookup"><span data-stu-id="f513d-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="f513d-123">Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori.</span><span class="sxs-lookup"><span data-stu-id="f513d-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="f513d-124">Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload**</span><span class="sxs-lookup"><span data-stu-id="f513d-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="f513d-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f513d-125">Select **OK**.</span></span>

<span data-ttu-id="f513d-126">Hvis du uploader flere typer aktiver på én gang (f.eks. billeder og videoer), kan du kun angive nøgleord i dialogboksen **Upload medieelement**, uanset om filerne skal udgives umiddelbart efter upload, og om der automatisk skal genereres undertekster til videofiler.</span><span class="sxs-lookup"><span data-stu-id="f513d-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="f513d-127">Alle aktiverne vil dele de samme nøgleord.</span><span class="sxs-lookup"><span data-stu-id="f513d-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f513d-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f513d-128">Additional resources</span></span>

[<span data-ttu-id="f513d-129">Oversigt over digital aktivstyring</span><span class="sxs-lookup"><span data-stu-id="f513d-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f513d-130">Uploade billeder</span><span class="sxs-lookup"><span data-stu-id="f513d-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="f513d-131">Uploade filer</span><span class="sxs-lookup"><span data-stu-id="f513d-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="f513d-132">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="f513d-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f513d-133">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="f513d-133">Customize image focal points</span></span>](dam-custom-focal-point.md)
