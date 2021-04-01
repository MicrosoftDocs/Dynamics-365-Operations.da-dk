---
title: Scanne stregkoder med et kamera i lagerstedsappen
description: I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 28a49736f43bd2d3bfd4c6856f2f87079a005ba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239296"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="f3f62-103">Scanne stregkoder med et kamera i lagerstedsappen</span><span class="sxs-lookup"><span data-stu-id="f3f62-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3f62-104">I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="f3f62-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f3f62-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f3f62-105">Prerequisites</span></span>
<span data-ttu-id="f3f62-106">For at bruge denne funktion skal du have version 1.2.0.0 af lagerstedsappen installeret, og enheden skal have et kamera.</span><span class="sxs-lookup"><span data-stu-id="f3f62-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="f3f62-107">Når du åbner appen efter opdateringen, bliver du spurgt, om du vil tillade, at appen bruger kameraet.</span><span class="sxs-lookup"><span data-stu-id="f3f62-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="f3f62-108">Hvis enheden ikke har et kamera, vises der ikke et prompt, og du kan ikke bruge et kamera som scanner.</span><span class="sxs-lookup"><span data-stu-id="f3f62-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="f3f62-109">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f3f62-109">Setup</span></span>
<span data-ttu-id="f3f62-110">I skærmindstillingerne i lagerstedsprogrammet kan du vælge, om kameraet skal bruges til scanning af stregkoder.</span><span class="sxs-lookup"><span data-stu-id="f3f62-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="f3f62-111">Hvis du aktiverer **Brug kameraet som scanner**, kan du bruge kameraet til alle inputfelter, hvor den foretrukne inputtilstand er indstillet til **Scannes**.</span><span class="sxs-lookup"><span data-stu-id="f3f62-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="f3f62-112">Hvis du vil styre, om et inputfelt skal kunne scannes, skal du på siden **Feltnavne for lagerstedsapp** indstille **Foretrukket inputtilstand** til **Scanning**.</span><span class="sxs-lookup"><span data-stu-id="f3f62-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="f3f62-113">Når denne indstilling er markeret, kan et kamera bruges til scanning i lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="f3f62-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="f3f62-114">Du kan finde oplysninger om, hvordan du konfigurerer appfeltnavne i Lagersted, under [Konfigurere appfeltnavne i lagerstedsappen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="f3f62-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="f3f62-115">Understøttede stregkodeformater</span><span class="sxs-lookup"><span data-stu-id="f3f62-115">Supported bar code formats</span></span>
<span data-ttu-id="f3f62-116">De mest almindelige stregkodeformater understøttes, herunder kode 128, kode 39, kode 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.</span><span class="sxs-lookup"><span data-stu-id="f3f62-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="f3f62-117">Navigation</span><span class="sxs-lookup"><span data-stu-id="f3f62-117">Navigation</span></span>
<span data-ttu-id="f3f62-118">Kamerasiden bliver initieret på hver side, hvor inputfeltets foretrukne inputtilstand er indstillet til Scannes. Når du er på kamerasiden, skal du bruge følgende indstillinger til at navigere:</span><span class="sxs-lookup"><span data-stu-id="f3f62-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="f3f62-119">Klik på Tilbage-knappen for at gå tilbage til siden med opgaver og detaljer.</span><span class="sxs-lookup"><span data-stu-id="f3f62-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="f3f62-120">Klik på blyanten på siden med opgaver og detaljer for at gå til den side, hvor du kan skrive input manuelt.</span><span class="sxs-lookup"><span data-stu-id="f3f62-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="f3f62-121">Klik på kameraet på siden med opgaver og detaljer for at gå tilbage til kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="f3f62-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="f3f62-122">Side med opgaver og detaljer</span><span class="sxs-lookup"><span data-stu-id="f3f62-122">Task and details page</span></span> | <span data-ttu-id="f3f62-123">Kameraside</span><span class="sxs-lookup"><span data-stu-id="f3f62-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Detaljeside med opgaveeksempel på kamerascanning](./media/camera-scanning-example-task-detail-page50.png)          | ![Mindre kameraside med eksempel på kamerascanning](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="f3f62-126">Når du klikker på knappen Kamera på kamerasiden, vises den nedtonet under forsøg på at identificere en stregkode.</span><span class="sxs-lookup"><span data-stu-id="f3f62-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="f3f62-127">Hvis der ikke findes en stregkode i løbet af 5 sekunder, afbrydes processen, og kameraknappen bliver tilgængelig igen.</span><span class="sxs-lookup"><span data-stu-id="f3f62-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="f3f62-128">Du kan derefter prøve at scanne en stregkode igen.</span><span class="sxs-lookup"><span data-stu-id="f3f62-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="f3f62-129">Når du holder kameraet over en stregkode, får du det bedste resultat, hvis stregkoden er justeret med parenteserne.</span><span class="sxs-lookup"><span data-stu-id="f3f62-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="f3f62-130">Når en stregkode er blevet scannet, bliver resultatet behandlet, og du føres til næste trin.</span><span class="sxs-lookup"><span data-stu-id="f3f62-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="f3f62-131">Hvis det næste trin indeholder endnu et inputfelt, hvor den foretrukne inputtilstand er indstillet til Scannes, starter kamerasiden igen.</span><span class="sxs-lookup"><span data-stu-id="f3f62-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="f3f62-132">Hvis det næste trin ikke er et scanningsfelt, initieres kamerasiden ikke.</span><span class="sxs-lookup"><span data-stu-id="f3f62-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]