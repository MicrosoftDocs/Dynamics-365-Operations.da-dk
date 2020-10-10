---
title: Flytte, erstatte og installere aktiver
description: Dette emne forklarer, hvordan du flytter, erstatter og installerer aktiver i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889547"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="9f892-103">Flytte, erstatte og installere aktiver</span><span class="sxs-lookup"><span data-stu-id="9f892-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9f892-104">Dette emne forklarer, hvordan du flytter, erstatter og installerer aktiver i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="9f892-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="9f892-105">Du kan oprette individuelle aktiver, der ikke har relationer til andre aktiver, eller du kan oprette en aktivstruktur, der omfatter et overordnet aktiv (aktiv på øverste niveau) og relaterede underordnede aktiver (underaktiver).</span><span class="sxs-lookup"><span data-stu-id="9f892-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="9f892-106">I Styring af aktiver er der tre metoder til at flytte og ændre placeringen af et aktiv:</span><span class="sxs-lookup"><span data-stu-id="9f892-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="9f892-107">**Flyt** – flyt et aktiv til en anden aktivstruktur eller til et andet sted i samme aktivstruktur.</span><span class="sxs-lookup"><span data-stu-id="9f892-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="9f892-108">**Erstat** – fjern midlertidigt et aktiv fra en aktivstruktur, så det kan repareres eller renoveres, og føj derefter det renoverede aktiv til aktivstrukturen igen.</span><span class="sxs-lookup"><span data-stu-id="9f892-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="9f892-109">Du kan også permanent erstatte et brugt aktiv med et nyt aktiv.</span><span class="sxs-lookup"><span data-stu-id="9f892-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="9f892-110">**Installer** – installer et overordnet aktiv og eventuelle relaterede underordnede aktiver på et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="9f892-111">Det aktiv, du flytter, erstatter eller installerer, kan være relateret til et andet arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="9f892-112">I så fald kan aktivet muligvis bruge arbejdsstedets økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9f892-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="9f892-113">På siden **Arbejdsstedstyper** konfigurerer du håndteringen af arbejdsstedernes økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9f892-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="9f892-114">Flyt aktiv</span><span class="sxs-lookup"><span data-stu-id="9f892-114">Move asset</span></span>

<span data-ttu-id="9f892-115">Anvend funktionen **Flyt aktiv** for at flytte et aktiv til enten en anden aktivstruktur eller til et andet sted i samme aktivstruktur.</span><span class="sxs-lookup"><span data-stu-id="9f892-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="9f892-116">Du kan også flytte et aktiv ud af en aktivstruktur, så det bliver et selvstændigt aktiv uden strukturrelationer.</span><span class="sxs-lookup"><span data-stu-id="9f892-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="9f892-117">Brug ikke denne funktion, hvis aktiverne repareres eller udskiftes midlertidigt.</span><span class="sxs-lookup"><span data-stu-id="9f892-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="9f892-118">Brug i stedet funktionen **Erstat aktiv**, som beskrives senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="9f892-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="9f892-119">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="9f892-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9f892-120">Vælg hvilket aktiv, du ønsker at flytte, på listen.</span><span class="sxs-lookup"><span data-stu-id="9f892-120">In the list, select the asset to move.</span></span> <span data-ttu-id="9f892-121">Hvis aktivet har underordnede aktiver, flytter du også disse aktiver.</span><span class="sxs-lookup"><span data-stu-id="9f892-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="9f892-122">Vælg **Flyt aktiv** for at flytte det.</span><span class="sxs-lookup"><span data-stu-id="9f892-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="9f892-123">Hvis du vil flytte aktivet, så det bliver en del af en aktivstruktur, skal du vælge det nye overordnede aktiv i feltet **Overordnet aktiv**.</span><span class="sxs-lookup"><span data-stu-id="9f892-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="9f892-124">Hvis du flytter et underordnet aktiv, og du vil gøre det til et selvstændigt aktiv uden strukturrelationer, skal du lade feltet **Overordnet aktiv** være tomt.</span><span class="sxs-lookup"><span data-stu-id="9f892-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="9f892-125">Feltet **Effektiv** er angives til den aktuelle dato og tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="9f892-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="9f892-126">Du kan dog vælge en anden dato og et andet klokkeslæt, som flytningen af aktivet skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="9f892-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="9f892-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f892-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="9f892-128">Erstat aktiv</span><span class="sxs-lookup"><span data-stu-id="9f892-128">Replace asset</span></span>

<span data-ttu-id="9f892-129">Brug funktionen **Erstat aktiv** i forbindelse med reparationer, renovering eller permanent udskiftning af et udslidt aktiv med et nyt aktiv.</span><span class="sxs-lookup"><span data-stu-id="9f892-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="9f892-130">Denne funktion bruges til at erstatte underordnede aktiver i en aktivstruktur.</span><span class="sxs-lookup"><span data-stu-id="9f892-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="9f892-131">I forbindelse med overordnede aktiver (altså aktiver, der i øjeblikket ikke har et overordnet aktiv), udføres denne udskiftning på et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="9f892-132">Du finder flere oplysninger om, hvordan du erstatter overordnede aktiver på et arbejdssted i [Installer aktiver på arbejdssteder](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="9f892-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9f892-133">Hvis et værksted er relateret til din produktionsafdeling, kan du oprette arbejdssteder såsom **Værksted**, **Skrot**og **Lager** til håndtering af reparationen og udskiftningen af aktiverne.</span><span class="sxs-lookup"><span data-stu-id="9f892-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="9f892-134">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="9f892-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9f892-135">Du skal vælge det underordnede aktiv, der skal erstattes, på listen.</span><span class="sxs-lookup"><span data-stu-id="9f892-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="9f892-136">Hvis aktivet har underordnede aktiver, erstatter du også disse aktiver.</span><span class="sxs-lookup"><span data-stu-id="9f892-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="9f892-137">Vælg **Erstat aktiv**.</span><span class="sxs-lookup"><span data-stu-id="9f892-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="9f892-138">Feltet **Strukturændring** viser den seneste dato og tidspunkt for, hvor det valgte aktiv og de tilknyttede underordnede aktiver blev flyttet i aktivstrukturen.</span><span class="sxs-lookup"><span data-stu-id="9f892-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="9f892-139">I sektionen **Valgt aktiv** i feltet **Målarbejdssted** skal du vælge det arbejdssted, som du ønsker at flytte aktivet til.</span><span class="sxs-lookup"><span data-stu-id="9f892-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="9f892-140">Vælg eksempelvis stedet **Værksted** eller **Skrot**.</span><span class="sxs-lookup"><span data-stu-id="9f892-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="9f892-141">I sektionen **Overordnet aktiv** viser feltet **Effektiv** den seneste dato og tidspunkt for, hvornår det overordnede aktiv og de relaterede underordnede aktiver blev installeret eller flyttet over på det aktuelle arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="9f892-142">I sektionen **Nyt aktiv** i feltet **Aktiv** skal du vælge det aktiv, der skal indsættes som en midlertidig eller permanent erstatning for det valgte aktiv.</span><span class="sxs-lookup"><span data-stu-id="9f892-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="9f892-143">Dette aktiv kan i øjeblikket være placeret på et andet arbejdssted, såsom **Lager**.</span><span class="sxs-lookup"><span data-stu-id="9f892-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="9f892-144">I sektionen **Gyldig fra** angives som standard den aktuelle dato og tidspunkt i feltet **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="9f892-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="9f892-145">Du kan dog vælge en anden dato og et andet klokkeslæt, som erstatningen af aktivet skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="9f892-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="9f892-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f892-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="9f892-147">Installer aktiv</span><span class="sxs-lookup"><span data-stu-id="9f892-147">Install asset</span></span>

<span data-ttu-id="9f892-148">Brug funktionen **Installer aktiv** til at installere en aktivstruktur på et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="9f892-149">Vælg altid et overordnet aktiv.</span><span class="sxs-lookup"><span data-stu-id="9f892-149">Always select a parent asset.</span></span> <span data-ttu-id="9f892-150">Det overordnede aktiv og de relaterede underordnede aktiver flyttes til det valgte arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="9f892-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="9f892-151">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="9f892-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9f892-152">Vælg det overordnede aktiv, du vil installere på et andet arbejdssted, på listen.</span><span class="sxs-lookup"><span data-stu-id="9f892-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="9f892-153">Vælg **Installer aktiv**.</span><span class="sxs-lookup"><span data-stu-id="9f892-153">Select **Install asset**.</span></span>

    <span data-ttu-id="9f892-154">Sektionen **Attributter** viser de aktivattributter, der er angivet for det overordnede aktiv.</span><span class="sxs-lookup"><span data-stu-id="9f892-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="9f892-155">I feltet **Arbejdssted** vælges det nye sted.</span><span class="sxs-lookup"><span data-stu-id="9f892-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="9f892-156">Feltet **Effektiv** er angives til den aktuelle dato og tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="9f892-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="9f892-157">Du kan dog vælge en anden dato og et andet klokkeslæt, som installationen af aktivstrukturen skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="9f892-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="9f892-158">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f892-158">Select **OK**.</span></span>
