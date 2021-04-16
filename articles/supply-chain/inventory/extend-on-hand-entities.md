---
title: Udvide dataenheder for lagerbeholdning
description: Dette emne indeholder et eksempel, der viser, hvordan du føjer udvidede felter til INVENTORSITEONHANDENTITY og INVENTWAREHOUSEONHANDENTITY, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne.
author: sherry-zheng
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7863f37e66727e2e80ea8c8b013ee49930e7c684
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829902"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="8b4d0-103">Udvide dataenheder for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="8b4d0-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b4d0-104">Microsoft Dynamics 365 Supply Chain Management leverer funktioner til [udvidelse](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), så du kan [føje felter til tabeller gennem udvidelse](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d0-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="8b4d0-105">Dette emne indeholder et eksempel, der viser, hvordan du føjer udvidede felter til visningerne `INVENTORSITEONHANDENTITY` og `INVENTWAREHOUSEONHANDENTITY`, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="8b4d0-106">Få flere oplysninger om dataenheder i [Oversigt over datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="8b4d0-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8b4d0-107">Her er en oversigt over nogle af lagerbeholdningsenhederne:</span><span class="sxs-lookup"><span data-stu-id="8b4d0-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="8b4d0-108">Disponibelt lager efter sted</span><span class="sxs-lookup"><span data-stu-id="8b4d0-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="8b4d0-109">Disponibelt lager efter sted V2</span><span class="sxs-lookup"><span data-stu-id="8b4d0-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="8b4d0-110">Disponibelt lager efter lagersted</span><span class="sxs-lookup"><span data-stu-id="8b4d0-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="8b4d0-111">Disponibelt lager efter lagersted v2</span><span class="sxs-lookup"><span data-stu-id="8b4d0-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="8b4d0-112">Når du har føjet felter til tabeller, der bruges af visningen `inventSiteOnHandView`, skal du synkronisere programmet, så filtypenavnene genkendes korrekt.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="8b4d0-113">Udvid visningen `InventSiteOnHandView` ved at tilføje udvidelsesfeltet.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="8b4d0-114">Udvid visningen `InventSiteOnHandAggregatedView` med udvidelsesfelterne.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="8b4d0-115">Udvid viewBuilder-klassen `InventSiteOnHandAggregatedViewBuilder` ved at ændre metoden `getExtensionFields()`.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="8b4d0-116">På denne måde knytter du gamle visningsfelter til nye visningsfelter ved kørsel af viewBuilder-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="8b4d0-117">Du har f.eks. føjet følgende fire felter til tabellen `InventTable` ved hjælp af udvidelsen:</span><span class="sxs-lookup"><span data-stu-id="8b4d0-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="8b4d0-118">Brugerdefineret felt 1</span><span class="sxs-lookup"><span data-stu-id="8b4d0-118">Custom field 1</span></span>
- <span data-ttu-id="8b4d0-119">Brugerdefineret felt 2</span><span class="sxs-lookup"><span data-stu-id="8b4d0-119">Custom field 2</span></span>
- <span data-ttu-id="8b4d0-120">Brugerdefineret felt 3</span><span class="sxs-lookup"><span data-stu-id="8b4d0-120">Custom field 3</span></span>
- <span data-ttu-id="8b4d0-121">Brugerdefineret felt 4</span><span class="sxs-lookup"><span data-stu-id="8b4d0-121">Custom field 4</span></span>

<span data-ttu-id="8b4d0-122">I så fald skal du redigere metoden `getExtensionFields()` på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="8b4d0-123">Når du har gennemført disse trin, kan du udvide det disponible lager gennem dataenhederne efter lokation og disponibelt lager ved at tilføje de nye felter.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="8b4d0-124">På denne måde sikrer du dig, at de udvidede felter genkendes og medtages under dataoverflytning, som bruger de pågældende dataenheder.</span><span class="sxs-lookup"><span data-stu-id="8b4d0-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]