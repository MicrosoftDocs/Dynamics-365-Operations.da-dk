---
title: Scanne stregkoder med et kamera i mobilappen Lokationsstyring
description: I dette emne beskrives, hvordan du konfigurerer mobilappen Lokationsstyring til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831212"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="38eeb-103">Scanne stregkoder med et kamera i mobilappen Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="38eeb-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38eeb-104">I dette emne beskrives, hvordan du konfigurerer mobilappen Lokationsstyring til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="38eeb-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="38eeb-105">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="38eeb-105">Setup</span></span>

<span data-ttu-id="38eeb-106">I skærmindstillingerne i mobilappen Lokationsstyring kan du vælge, om kameraet skal bruges til scanning af stregkoder.</span><span class="sxs-lookup"><span data-stu-id="38eeb-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="38eeb-107">Hvis du aktiverer **Brug kameraet som scanner**, kan du bruge kameraet til alle inputfelter, hvor den foretrukne inputtilstand er indstillet til **Scannes**.</span><span class="sxs-lookup"><span data-stu-id="38eeb-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="38eeb-108">Hvis du vil styre, om et inputfelt skal kunne scannes, skal du på siden **Feltnavne for lagerstedsapp** indstille **Foretrukket inputtilstand** til **Scanning**.</span><span class="sxs-lookup"><span data-stu-id="38eeb-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="38eeb-109">Når denne indstilling er markeret, kan et kamera bruges til scanning i mobilappen Lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="38eeb-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="38eeb-110">Du kan finde flere oplysninger i [Konfigurere felter til mobilappen Lokationsstyring](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="38eeb-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="38eeb-111">Understøttede stregkodeformater</span><span class="sxs-lookup"><span data-stu-id="38eeb-111">Supported bar code formats</span></span>

<span data-ttu-id="38eeb-112">De mest almindelige stregkodeformater understøttes, herunder kode 128, kode 39, kode 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.</span><span class="sxs-lookup"><span data-stu-id="38eeb-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="38eeb-113">Navigation</span><span class="sxs-lookup"><span data-stu-id="38eeb-113">Navigation</span></span>

<span data-ttu-id="38eeb-114">Kamerasiden bliver initieret på hver side, hvor inputfeltets **Foretrukne inputtilstand** er indstillet til *Scanning*. Når du er på kamerasiden, skal du bruge følgende indstillinger til at navigere:</span><span class="sxs-lookup"><span data-stu-id="38eeb-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="38eeb-115">Vælg Tilbage-knappen for at gå tilbage til siden med **Opgaver og detaljer**.</span><span class="sxs-lookup"><span data-stu-id="38eeb-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="38eeb-116">Vælg blyanten på siden **Opgaver og detaljer** for at gå til den side, hvor du kan skrive input manuelt.</span><span class="sxs-lookup"><span data-stu-id="38eeb-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="38eeb-117">Væl kameraet på siden **Opgaver og detaljer** for at gå tilbage til kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="38eeb-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="38eeb-118">Når du vælger knappen Kamera på kamerasiden, vises den nedtonet under forsøg på at identificere en stregkode.</span><span class="sxs-lookup"><span data-stu-id="38eeb-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="38eeb-119">Hvis der ikke findes en stregkode i løbet af 5 sekunder, får processen timeout, og kameraknappen bliver tilgængelig igen.</span><span class="sxs-lookup"><span data-stu-id="38eeb-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="38eeb-120">Du kan derefter prøve at scanne en stregkode igen.</span><span class="sxs-lookup"><span data-stu-id="38eeb-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="38eeb-121">Når du holder kameraet over en stregkode, får du det bedste resultat, hvis stregkoden er justeret med parenteserne.</span><span class="sxs-lookup"><span data-stu-id="38eeb-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="38eeb-122">Når en stregkode er blevet scannet, bliver resultatet behandlet, og du føres til næste trin.</span><span class="sxs-lookup"><span data-stu-id="38eeb-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="38eeb-123">Hvis det næste trin indeholder endnu et inputfelt, hvor den foretrukne inputtilstand er indstillet til Scannes, starter kamerasiden igen.</span><span class="sxs-lookup"><span data-stu-id="38eeb-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="38eeb-124">Hvis det næste trin ikke er et scanningsfelt, initieres kamerasiden ikke.</span><span class="sxs-lookup"><span data-stu-id="38eeb-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]