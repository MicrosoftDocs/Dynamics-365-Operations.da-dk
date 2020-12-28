---
title: Produktbekræftelse for klyngepluk
description: I dette emne beskrives, hvordan du opretter varebekræftelse sammen med klyngepluk.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424667"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="3f4c6-103">Produktbekræftelse for klyngepluk</span><span class="sxs-lookup"><span data-stu-id="3f4c6-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f4c6-104">Med pluk af klyngen kan du plukke varer til flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="3f4c6-105">Når der anvendes en klyngepluk, er varebekræftelse afgørende for kontrol af de varer, der føjes til klynger.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="3f4c6-106">Du kan kontrollere varer i klyngepluk under klyngeplukprocessen.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3f4c6-107">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="3f4c6-107">Where it applies</span></span>

<span data-ttu-id="3f4c6-108">Varekontrol for klyngepluk fungerer på samme måde, som når du kontrollerer varer i en ikke-klynge plukproces.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="3f4c6-109">Opsætningen er baseret på opsætningen af produktets stregkode.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="3f4c6-110">Konfigurer varekontrol med klyngepluk</span><span class="sxs-lookup"><span data-stu-id="3f4c6-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="3f4c6-111">I menupunktet på en mobilenhed skal du åbne opsætningsformularen for arbejdsbekræftelse: **Lokationsstyring** > **Lokationsstyring** > **Opsætning** > **Mobilenhed** > **Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="3f4c6-112">Åbn **Konfiguration af arbejdsbekræftelse** fra menupunktet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="3f4c6-113">Indstilling</span><span class="sxs-lookup"><span data-stu-id="3f4c6-113">Option</span></span>        |                                    <span data-ttu-id="3f4c6-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3f4c6-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3f4c6-115">Bekræftelse af produkt</span><span class="sxs-lookup"><span data-stu-id="3f4c6-115">Product confirmation</span></span> | <span data-ttu-id="3f4c6-116">Gør det muligt for dig at kontrollere hver enkelt vare på lageret fra mobilenheden, når den scannes.</span><span class="sxs-lookup"><span data-stu-id="3f4c6-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |
