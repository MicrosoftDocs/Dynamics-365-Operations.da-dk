---
title: Aktiver på flere niveauer
description: Dette emne forklarer, hvordan du opretter og sletter aktiver på flere niveauer.
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
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424764"
---
# <a name="multi-level-assets"></a><span data-ttu-id="5ec32-103">Aktiver på flere niveauer</span><span class="sxs-lookup"><span data-stu-id="5ec32-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5ec32-104">Dette emne forklarer, hvordan du opretter og sletter aktiver på flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="5ec32-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="5ec32-105">Du kan oprette aktiver og relaterede under aktiver i en hierarkisk træstruktur.</span><span class="sxs-lookup"><span data-stu-id="5ec32-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="5ec32-106">På denne måde kan du vise relationer og afhængigheder mellem aktiver.</span><span class="sxs-lookup"><span data-stu-id="5ec32-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="5ec32-107">Vedligeholdelsesjob kan relateres til alle niveauer i træstrukturen.</span><span class="sxs-lookup"><span data-stu-id="5ec32-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="5ec32-108">Der kan også oprettes statistikker for et individuelt niveau eller en sum af alle niveauer for underaktiver.</span><span class="sxs-lookup"><span data-stu-id="5ec32-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="5ec32-109">På listesiden **Alle aktiver** (**Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**) opregner kolonner **Aktiver** aktiverne i hierarkisk orden.</span><span class="sxs-lookup"><span data-stu-id="5ec32-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="5ec32-110">Kolonnen **Overordnet** viser den relaterede overordnede.</span><span class="sxs-lookup"><span data-stu-id="5ec32-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="5ec32-111">Hvis der derudover allerede er oprettet aktiver og underaktiver, vises aktiverne i en træstruktur i sektionen **Aktivtræ** i ruden **Relaterede oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="5ec32-112">Du kan finde flere oplysninger om, hvordan du opretter et aktiv i [Opret et aktiv](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="5ec32-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="5ec32-113">Hvis du vil oprette et underaktiv, skal du vælge det overordnede aktiv i feltet **Overordnet aktiv** på oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="5ec32-114">Kopiér et aktiv eller en aktivstruktur</span><span class="sxs-lookup"><span data-stu-id="5ec32-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="5ec32-115">Hvis din virksomhed har flere ensartede aktivstrukturer, kan du bruge kopieringsfunktionen i Styring af aktiver til hurtigt at oprette dem.</span><span class="sxs-lookup"><span data-stu-id="5ec32-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="5ec32-116">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="5ec32-117">På listesiden **Alle aktiver** skal du vælge, hvilket aktiv, der skal kopieres.</span><span class="sxs-lookup"><span data-stu-id="5ec32-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="5ec32-118">Hvis du for eksempel vil kopiere hele aktivstrukturen, herunder underaktiver, skal du vælge et overordnet aktiv.</span><span class="sxs-lookup"><span data-stu-id="5ec32-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="5ec32-119">Vælg **Kopiér aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-119">Select **Copy asset**.</span></span> <span data-ttu-id="5ec32-120">I sektionen **Kopiér fra** er feltet **Aktiv** angivet til det aktiv, du valgte på listesiden.</span><span class="sxs-lookup"><span data-stu-id="5ec32-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="5ec32-121">Angiv navnet på det nye aktiv i feltet **Aktiv** i sektionen **Kopiér til**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="5ec32-122">Hvis det aktiv, du opretter, skal være en del af en eksisterende aktivstruktur, skal du i feltet **Aktiv** i sektionen **Overordnet aktiv** vælge et overordnet ID.</span><span class="sxs-lookup"><span data-stu-id="5ec32-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="5ec32-123">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-123">Select **OK**.</span></span> <span data-ttu-id="5ec32-124">Den nye aktivstruktur fremgår af listesiden **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="5ec32-125">Alle aktivattributter, vedligeholdelsesplaner og vedligeholdelsesrunder, der er relateret til det aktiv, du kopierede, overføres til det nye aktiv eller aktivstruktur.</span><span class="sxs-lookup"><span data-stu-id="5ec32-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="5ec32-126">Når du kopierer en aktivstruktur, har underaktiverne i den nye struktur samme navn som de underaktiver, du kopierede.</span><span class="sxs-lookup"><span data-stu-id="5ec32-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="5ec32-127">Når kopieringsproceduren er fuldført, kan du nemt ændre navnet og andre indstillinger for et aktiv.</span><span class="sxs-lookup"><span data-stu-id="5ec32-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="5ec32-128">Vælg aktivet på listesiden **Alle aktiver**, og vælg derefter knappen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="5ec32-129">Når du kopierer et aktiv eller en aktivstruktur, nulstilles livscyklussen for de nye aktiver til den tilstand, du definerede som den oprindelige livscyklustilstand for aktiver.</span><span class="sxs-lookup"><span data-stu-id="5ec32-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="5ec32-130">Arbejdsstedet nulstilles til arbejdsstedsstandarden.</span><span class="sxs-lookup"><span data-stu-id="5ec32-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="5ec32-131">Slet et aktiv eller en aktivstruktur</span><span class="sxs-lookup"><span data-stu-id="5ec32-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="5ec32-132">Hvis et aktiv har relaterede underaktiver, kan du kun slette det, hvis der ikke er registreret nogen vedligeholdelsesanmodninger, arbejdsordrejobs, fejlregistreringer eller tilstandsvurderinger på nogen af aktiverne.</span><span class="sxs-lookup"><span data-stu-id="5ec32-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="5ec32-133">På listesiden **Alle aktiver** skal du vælge, hvilket aktiv, der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="5ec32-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="5ec32-134">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ec32-135">Hvis du ikke kan slette et aktiv ved hjælp af denne procedure, er en anden måde at håndtere sletningen på at konfigurere en livscyklustilstand for et aktiv til dette formål.</span><span class="sxs-lookup"><span data-stu-id="5ec32-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="5ec32-136">Du kan eksempelvis konfigurere en **Kasseret** eller **Slettet** livscyklustilstand på siden **Livscyklustilstand for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5ec32-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
