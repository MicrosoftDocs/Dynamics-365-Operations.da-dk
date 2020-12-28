---
title: Modtagelse af blandede id'er
description: I dette emne beskrives, hvordan du bruger Modtagelse af blandede id'er til at registrere og oprette arbejde for flere varer med en mobilenhed.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc87da5fefde33832fc0be1cfef3aa44b155c0d0
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424943"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="f04de-103">Modtagelse af blandede id'er</span><span class="sxs-lookup"><span data-stu-id="f04de-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f04de-104">Med Modtagelse af blandede id'er kan du oprette et id, der består af flere varer, før du registrerer og opretter læg-på-lager-arbejde.</span><span class="sxs-lookup"><span data-stu-id="f04de-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="f04de-105">Et id, der består af flere varer, behøver ikke at blive opdelt i modtagelsesområdet, for at du kan registrere de enkelte varer.</span><span class="sxs-lookup"><span data-stu-id="f04de-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="f04de-106">Når du bruger en varerelateret proces til at identificere kildedokumentlinjerne, kan du scanne stregkoder på varekontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="f04de-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="f04de-107">Hvis der er konfigureret et antal og en måleenhed (UOM) i stregkoden, føjes varen og antallet automatisk til det blandede id, og du sendes tilbage til skærmbilledet for at scanne et andet element.</span><span class="sxs-lookup"><span data-stu-id="f04de-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="f04de-108">Dette gør det muligt hurtigt at scanne alle varer uden at skulle foretage en bekræftelse på hvert trin.</span><span class="sxs-lookup"><span data-stu-id="f04de-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="f04de-109">I processen til modtagelse af blandede id'er kan du få vist listen over varer, der allerede er indscannet i id'et, og herfra kan du ændre eller rette mængde eller antallet af en vare.</span><span class="sxs-lookup"><span data-stu-id="f04de-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f04de-110">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="f04de-110">Where it applies</span></span>

<span data-ttu-id="f04de-111">Modtagelse af blandede id'er er en modtagelsesproces til mobilenheder, hvor du kan registrere og oprette arbejde for flere linjer/varer på samme tid.</span><span class="sxs-lookup"><span data-stu-id="f04de-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="f04de-112">Dette er nyttigt, hvis du modtager indgående id'er med flere elementer.</span><span class="sxs-lookup"><span data-stu-id="f04de-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="f04de-113">Sådan konfigurerer du modtagelse af blandede id'er</span><span class="sxs-lookup"><span data-stu-id="f04de-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="f04de-114">Modtagelse af blandet nummerplade konfigureres som et menupunkt på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="f04de-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="f04de-115">Du skal oprette et nyt menupunkt med tilstandsarbejde, der ikke bruger eksisterende arbejde, og bruge en af følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="f04de-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="f04de-116">Modtagelse af blandede id'er</span><span class="sxs-lookup"><span data-stu-id="f04de-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="f04de-117">Modtagelse af blandede id'er og placering på lager</span><span class="sxs-lookup"><span data-stu-id="f04de-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="f04de-118">Indstillingerne til identifikation af kildedokumentlinjerne er indkøbsordrevare, indkøbsordrelinje, returordre, vare i flytteordre og flytteforslagslinje.</span><span class="sxs-lookup"><span data-stu-id="f04de-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="f04de-119">Disse indstillinger kan ændre modtagelsesordren på et enkelt id.</span><span class="sxs-lookup"><span data-stu-id="f04de-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="f04de-120">Den sidste indstilling er vare efter last.</span><span class="sxs-lookup"><span data-stu-id="f04de-120">The last option is by load item.</span></span> <span data-ttu-id="f04de-121">Du kan føje flere varer til et id, men du kan ikke skifte mellem flere laster.</span><span class="sxs-lookup"><span data-stu-id="f04de-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
