---
title: Tilpasse billedets fokuspunkter
description: Dette emne indeholder en beskrivelse af, hvordan du tilpasser billedets fokuspunkter i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 9c8fc9a1f944d24aff3ab2923ca2715209a674e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972926"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="c99a8-103">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="c99a8-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c99a8-104">Dette emne indeholder en beskrivelse af, hvordan du tilpasser billedets fokuspunkter i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="c99a8-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c99a8-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="c99a8-105">Overview</span></span>

<span data-ttu-id="c99a8-106">Når et billede uploades til mediebiblioteket i Commerce-webstedsgenerator, forsøger systemet at bestemme billedets fokuspunkt.</span><span class="sxs-lookup"><span data-stu-id="c99a8-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="c99a8-107">Hvis der f.eks. er en person på billedet, vil systemet som standard sætte fokuspunktet til personens ansigt.</span><span class="sxs-lookup"><span data-stu-id="c99a8-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="c99a8-108">I de fleste tilfælde fungerer det automatisk angivne fokuspunkt godt for alle billeder, men nogle gange kan det være en god ide at justere fokuspunktet for at sikre, at en bestemt del af billedet altid er synligt.</span><span class="sxs-lookup"><span data-stu-id="c99a8-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="c99a8-109">Definere et brugerdefineret fokuspunkt for et billede</span><span class="sxs-lookup"><span data-stu-id="c99a8-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="c99a8-110">Hvis du vil definere et brugerdefineret fokuspunkt for et billede, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c99a8-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="c99a8-111">Vælg **Mediebibliotek** i venstre navigationsrude i Commerce-webstedgenerator.</span><span class="sxs-lookup"><span data-stu-id="c99a8-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="c99a8-112">Vælg det billede, du vil redigere, i hovedvinduet.</span><span class="sxs-lookup"><span data-stu-id="c99a8-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="c99a8-113">Vælg **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="c99a8-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="c99a8-114">Vælg billedet for at skifte til **Redigeringstilstand**.</span><span class="sxs-lookup"><span data-stu-id="c99a8-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="c99a8-115">Vælg **Skift fokuspunkt** under **Redigeringstilstand**.</span><span class="sxs-lookup"><span data-stu-id="c99a8-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="c99a8-116">Der vises et cirkulært fokuspunkt for billedet.</span><span class="sxs-lookup"><span data-stu-id="c99a8-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="c99a8-117">Vælg kontrolelementet til fokuspunktet for at flytte det hen over det ønskede fokuspunkt.</span><span class="sxs-lookup"><span data-stu-id="c99a8-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="c99a8-118">Når du er færdig, skal du vælge **Gem** på kommandolinjen og derefter vælge **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="c99a8-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c99a8-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c99a8-119">Additional resources</span></span>

[<span data-ttu-id="c99a8-120">Oversigt over styring af digitale aktiver</span><span class="sxs-lookup"><span data-stu-id="c99a8-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c99a8-121">Overføre billeder</span><span class="sxs-lookup"><span data-stu-id="c99a8-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c99a8-122">Overføre video</span><span class="sxs-lookup"><span data-stu-id="c99a8-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="c99a8-123">Uploade filer</span><span class="sxs-lookup"><span data-stu-id="c99a8-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="c99a8-124">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="c99a8-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c99a8-125">Overføre og håndtere statiske filer</span><span class="sxs-lookup"><span data-stu-id="c99a8-125">Upload and serve static files</span></span>](upload-serve-static-files.md)
