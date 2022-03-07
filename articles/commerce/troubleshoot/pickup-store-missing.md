---
title: Retail-butik vises ikke på listen over butikker, der kan vælges
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en detailbutik ikke vises på listen over butikker, hvor der kan afhentes varer.
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
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020811"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Retail-butik vises ikke på listen over butikker, der kan vælges

[!include [banner](../../includes/banner.md)]

Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en detailbutik ikke vises på listen over butikker, hvor der kan afhentes varer.

## <a name="description"></a>Betegnelse

En detailbutik vises ikke på listen over butikker, hvor varerne kan afhentes.

## <a name="resolution"></a>Løsning

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Konfigurere længde- og breddegrad for butiksadressen i Commerce Headquarters

Følg disse trin for at fonfigurere længde- og breddegrad for butiksadressen i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker**.
1. Find den butik, du vil have vist blandt afhentningsindstillingerne på e-handelswebstedet. Noter værdien for **driftsenhedsnummer**.
1. Gå til **Organisationsadministration \> Organisationer \> Driftsenheder**.
1. Søg efter det driftsenhedsnummer, du har angivet tidligere, og vælg derefter driftsenheden i søgeresultaterne.
1. Vælg **Flere indstillinger** i oversigtspanelet **Adresser**, og vælg derefter **Avanceret**.
1. Kontroller, at felterne **Længdegrad** og **Breddegrad** i oversigtspanelet **Generelt** er indstillet korrekt. Som en del af dette trin skal du sikre dig, at værdierne er angivet korrekt som positive eller negative tal.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Konfigurere opfyldningsgrupper i Commerce Headquarters

Følg disse trin for at konfigurere opfyldningsgrupper i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.
1. Vælg den onlinebutik, der skal konfigureres.
1. Vælg fanen Handling skal du vælge **Opsætning** og derefter **Gruppetildeling for opfyldelse**.
1. På siden **Tildeling af opfyldningsgruppe** skal du vælge opfyldningsgruppen for onlinebutikken.
1. Under **Opsætning** skal du sikre dig, at detailbutikken er konfigureret korrekt til opfyldningsgruppen.

## <a name="additional-resources"></a>Yderligere ressourcer 

[Oprette en driftsenhed](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Konfigurere en onlinekanal](../channel-setup-online.md)