---
title: Udvide dataenheder for lagerbeholdning
description: Dette emne indeholder et eksempel, der viser, hvordan du føjer udvidede felter til INVENTORSITEONHANDENTITY og INVENTWAREHOUSEONHANDENTITY, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2e805b9379c73f7b7eb2820662fad70e28181ebf
ms.sourcegitcommit: f59df61799915f6a79aec7e3e8664c02df6597da
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/22/2021
ms.locfileid: "5043387"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="eb6b3-103">Udvide dataenheder for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="eb6b3-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb6b3-104">Microsoft Dynamics 365 Supply Chain Management leverer funktioner til [udvidelse](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), så du kan [føje felter til tabeller gennem udvidelse](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="eb6b3-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="eb6b3-105">Dette emne indeholder et eksempel, der viser, hvordan du føjer udvidede felter til visningerne `INVENTORSITEONHANDENTITY` og `INVENTWAREHOUSEONHANDENTITY`, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="eb6b3-106">Få flere oplysninger om dataenheder i [Oversigt over datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="eb6b3-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="eb6b3-107">Her er en oversigt over nogle af lagerbeholdningsenhederne:</span><span class="sxs-lookup"><span data-stu-id="eb6b3-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="eb6b3-108">Disponibelt lager efter sted</span><span class="sxs-lookup"><span data-stu-id="eb6b3-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="eb6b3-109">Disponibelt lager efter sted V2</span><span class="sxs-lookup"><span data-stu-id="eb6b3-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="eb6b3-110">Disponibelt lager efter lagersted</span><span class="sxs-lookup"><span data-stu-id="eb6b3-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="eb6b3-111">Disponibelt lager efter lagersted v2</span><span class="sxs-lookup"><span data-stu-id="eb6b3-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="eb6b3-112">Når du har føjet felter til tabeller, der bruges af visningen `inventSiteOnHandView`, skal du synkronisere programmet, så filtypenavnene genkendes korrekt.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="eb6b3-113">Udvid visningen `InventSiteOnHandView` ved at tilføje udvidelsesfeltet.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="eb6b3-114">Udvid visningen `InventSiteOnHandAggregatedView` med udvidelsesfelterne.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="eb6b3-115">Udvid viewBuilder-klassen `InventSiteOnHandAggregatedViewBuilder` ved at ændre metoden `getExtensionFields()`.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="eb6b3-116">På denne måde knytter du gamle visningsfelter til nye visningsfelter ved kørsel af viewBuilder-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="eb6b3-117">Du har f.eks. føjet følgende fire felter til tabellen `InventTable` ved hjælp af udvidelsen:</span><span class="sxs-lookup"><span data-stu-id="eb6b3-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="eb6b3-118">Brugerdefineret felt 1</span><span class="sxs-lookup"><span data-stu-id="eb6b3-118">Custom field 1</span></span>
- <span data-ttu-id="eb6b3-119">Brugerdefineret felt 2</span><span class="sxs-lookup"><span data-stu-id="eb6b3-119">Custom field 2</span></span>
- <span data-ttu-id="eb6b3-120">Brugerdefineret felt 3</span><span class="sxs-lookup"><span data-stu-id="eb6b3-120">Custom field 3</span></span>
- <span data-ttu-id="eb6b3-121">Brugerdefineret felt 4</span><span class="sxs-lookup"><span data-stu-id="eb6b3-121">Custom field 4</span></span>

<span data-ttu-id="eb6b3-122">I så fald skal du redigere metoden `getExtensionFields()` på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="eb6b3-123">Når du har gennemført disse trin, kan du udvide det disponible lager gennem dataenhederne efter lokation og disponibelt lager ved at tilføje de nye felter.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="eb6b3-124">På denne måde sikrer du dig, at de udvidede felter genkendes og medtages under dataoverflytning, som bruger de pågældende dataenheder.</span><span class="sxs-lookup"><span data-stu-id="eb6b3-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
