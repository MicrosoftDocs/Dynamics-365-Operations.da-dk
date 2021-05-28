---
title: Manglende produkter og kategorier efter miljøkopi
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når produkter og kategorier mangler, efter at et websted er kopieret mellem miljøer eller i det samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022392"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Manglende produkter og kategorier efter miljøkopi

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når produkter og kategorier mangler, efter at et websted er kopieret mellem miljøer eller i det samme miljø.

## <a name="description"></a>Betegnelse

Når en lokation er kopieret fra ét miljø til et andet eller i det samme miljø, mangler produkterne og kategorierne fra lokationen. Produkterne og kategorierne mangler i e-commerce-butikken og fra fanen **Produkter** i Commerce Site Builder.

## <a name="resolution"></a>Løsning

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Knytte nummeret på kanalens driftsenhed til et nyligt kopieret websted i Commerce Site Builder

Følg disse trin,for at knytte nummeret på kanalens driftsenhed (OUN) til et nyligt kopieret websted i Commerce Site Builder

1. Vælg det nyligt kopierede sted.
1. Vælg **Kanaler** nedenunder **Indstillinger for websted**.
1. Vælg ellipsen (**...**) ud for kanalnavnet, og vælg derefter **Skift onlinebutikskanal**.
1. Vælg den kanal, du vil knytte til det nyligt kopierede websted, i dialogboksen **Skift onlinebutikskanal**, og vælg derefter **OK**.
1. Vælg **Gem og udgiv**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](../associate-site-online-store.md)
