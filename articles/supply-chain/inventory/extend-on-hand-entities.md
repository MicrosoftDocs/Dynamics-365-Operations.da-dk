---
title: Udvide dataenheder for lagerbeholdning
description: Denne artikel indeholder et eksempel, der viser, hvordan du føjer udvidede felter til INVENTORSITEONHANDENTITY og INVENTWAREHOUSEONHANDENTITY, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906031"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Udvide dataenheder for lagerbeholdning

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management leverer funktioner til [udvidelse](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), så du kan [føje felter til tabeller gennem udvidelse](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Denne artikel indeholder et eksempel, der viser, hvordan du føjer udvidede felter til visningerne `INVENTORSITEONHANDENTITY` og `INVENTWAREHOUSEONHANDENTITY`, så funktionerne på dataenhederne for det disponible lager kan fungere sammen med udvidelserne. Få flere oplysninger om dataenheder i [Oversigt over datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Her er en oversigt over nogle af lagerbeholdningsenhederne:
>
> - Disponibelt lager efter sted
> - Disponibelt lager efter sted V2
> - Disponibelt lager efter lagersted
> - Disponibelt lager efter lagersted v2

Når du har føjet felter til tabeller, der bruges af visningen `inventSiteOnHandView`, skal du synkronisere programmet, så filtypenavnene genkendes korrekt.

1. Udvid visningen `InventSiteOnHandView` ved at tilføje udvidelsesfeltet.
1. Udvid visningen `InventSiteOnHandAggregatedView` med udvidelsesfelterne.
1. Udvid viewBuilder-klassen `InventSiteOnHandAggregatedViewBuilder` ved at ændre metoden `getExtensionFields()`. På denne måde knytter du gamle visningsfelter til nye visningsfelter ved kørsel af viewBuilder-synkronisering.

Du har f.eks. føjet følgende fire felter til tabellen `InventTable` ved hjælp af udvidelsen:

- Brugerdefineret felt 1
- Brugerdefineret felt 2
- Brugerdefineret felt 3
- Brugerdefineret felt 4

I så fald skal du redigere metoden `getExtensionFields()` på følgende måde.

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

Når du har gennemført disse trin, kan du udvide det disponible lager gennem dataenhederne efter lokation og disponibelt lager ved at tilføje de nye felter. På denne måde sikrer du dig, at de udvidede felter genkendes og medtages under dataoverflytning, som bruger de pågældende dataenheder.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]