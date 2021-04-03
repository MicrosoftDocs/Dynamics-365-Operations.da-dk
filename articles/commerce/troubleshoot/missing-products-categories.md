---
title: Manglende produkter og kategorier efter miljøkopi
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når produkter og kategorier mangler, efter at et websted er kopieret mellem miljøer eller i det samme miljø.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585257"
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
