---
title: Visning af aktiver
description: Dette emne beskriver visning af aktiver i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14dc2cd95a47931ae4941b87205f2104891af404
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208219"
---
# <a name="asset-view"></a><span data-ttu-id="1cc85-103">Visning af aktiver</span><span class="sxs-lookup"><span data-stu-id="1cc85-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1cc85-104">Dette emne beskriver visning af aktiver i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="1cc85-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="1cc85-105">Siden **Visning af aktiver** viser aktive aktiver og arbejdssteder i en trævisning.</span><span class="sxs-lookup"><span data-stu-id="1cc85-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="1cc85-106">Du kan derved nemt danne dig et overblik over aktivrelationer til arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="1cc85-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="1cc85-107">Du kan også få vist detaljerede oplysninger om arbejdssteder, aktiver og relaterede styklister (BOM'er).</span><span class="sxs-lookup"><span data-stu-id="1cc85-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="1cc85-108">Du kan også få et hurtigt overblik over aktive vedligeholdelsesanmodninger og arbejdsordrer, der er relateret til et aktiv.</span><span class="sxs-lookup"><span data-stu-id="1cc85-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="1cc85-109">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Visning af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="1cc85-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="1cc85-110">Hvis du vil ændre den visning, der fremgår af siden, skal du vælge en ny værdi i feltet **Visning**.</span><span class="sxs-lookup"><span data-stu-id="1cc85-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cc85-111">Den standardvisning, der vises, når du åbner siden **Visning af aktiver**, afhænger af den værdi, der er valgt i feltet **Visning** under fanen **Aktiver** på siden **Parametre for Styring af aktiver** (**Styring af aktiver** \> **Opsætning** \> **Parametre for Styring af aktiver)**.</span><span class="sxs-lookup"><span data-stu-id="1cc85-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="1cc85-112">I højre side af siden viser oversigtspaneler oplysninger om den valgte visning.</span><span class="sxs-lookup"><span data-stu-id="1cc85-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="1cc85-113">Den breadcrumb-sti, der vises over trævisningen, viser det aktuelle udvalg i træstrukturen.</span><span class="sxs-lookup"><span data-stu-id="1cc85-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="1cc85-114">Denne breadcrumb-sti bruger følgende format:</span><span class="sxs-lookup"><span data-stu-id="1cc85-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="1cc85-115">ID for arbejdssted/ID for arbejdssted (hvis der er mere end et arbejdssted) \> Aktiv-ID/Aktiv-ID (hvis der er mere end ét aktiv) - varenummer.</span><span class="sxs-lookup"><span data-stu-id="1cc85-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="1cc85-116">Hvis du har valgt et aktiv i træstrukturen, kan du vælge **Aktive anmodninger** eller **Aktive arbejdsordrer** for at få vist de vedligeholdelsesanmodninger eller arbejdsordrer, der er relateret til aktivet.</span><span class="sxs-lookup"><span data-stu-id="1cc85-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="1cc85-117">Du kan også vælge **Åbn** \> **Arbejdssted**, **Aktiv** eller **Aktivstykliste** for at åbne den relaterede visning.</span><span class="sxs-lookup"><span data-stu-id="1cc85-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="1cc85-118">Indstillingen **Aktivers arbejdssteder**, som du kan vælge i feltet **Visning**, er også tilgængelig i alle aktivopslag, hvor du kan vælge et aktiv.</span><span class="sxs-lookup"><span data-stu-id="1cc85-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="1cc85-119">Trævisningen vises eksempelvis på fanen **Visning af aktiv**, hvor du [opretter et aktiv](../objects/create-an-object.md), opretter en vedligeholdelsesanmodning eller opretter en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="1cc85-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
