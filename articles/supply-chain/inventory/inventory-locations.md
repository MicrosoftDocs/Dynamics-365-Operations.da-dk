---
title: Lagerlokationer
description: Lagerlokationer bruges sammen med grundlæggende lagersted (WMS I) til at bestemme, hvor varerne opbevares, og hvor varerne plukkes fra i et WMS I-lagersted.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31096aa9c97f0307c7004d1af1e424dde1dc65cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264060"
---
# <a name="inventory-locations"></a>Lagerlokationer

[!include [banner](../includes/banner.md)]

Lagerlokationer bruges sammen med grundlæggende lagersted (WMS I) til at bestemme, hvor varerne opbevares, og hvor varerne plukkes fra i et WMS I-lagersted.

Dette emne gælder for funktioner i modulet Lagerstyring. Det gælder ikke for funktioner i modulet Lagerstedsstyring.

Betegnelsen lokalitet henviser til det sted, som varer opbevares på og trækkes fra.

For hver lokation kan der også angives det sted, hvor varen indsættes. Som standard er de ens. Varer indsættes og trækkes normalt fra den samme side af en lokation, men ikke altid. Varer, der opbevares i lagerreoler med rullebaner, indsættes fra én gang og trækkes fra en anden. Hovedindlagringsstedet angives i form af et lokationsnavn, der normalt bestemmes ved dets koordinater: lager, gang, reol, hylde og beholder. Dette navn eller id kan angives manuelt eller genereres på basis af lokationens koordinater – f.eks. 01-02-03-4, som står for gang 1, reol 2, hylde 3, beholder 4 på siden Lagerlokationer.
Lokationsegenskaber

Lokationen har følgende koordinater:
-   Størrelse (højde, bredde, dybde og derved rumfang)
-   Lagersted, gang, reol, hylde og beholder
-   Placeringstype (bulkvarelokation, plukplads, modtagelsesområde, forsendelsesområde, produktionsindlagringslokation, inspektionssted eller kanban-supermarked)

I onlinesystemer kan der anvendes kontroltekst, som sikrer, at operatøren har valgt den rigtige lokation til en bestemt vare. Kontrolteksten kan oprettes manuelt, eller der kan indsættes en standardtekst.

## <a name="sort-codes"></a>Sorteringskoder
Håndteringen af pluklinjer kan optimeres, hvis der anvendes sorteringskoder, der beskriver de detaljerede oplysninger, som skal bruges til plukning af varer fra lageret, herunder plukrækkefølgen. Sorteringskoder kan angives på basis af lagergangen og andre koordinater, eller de kan tildeles manuelt for en bestemt lokation.

## <a name="blocked-locations"></a>Spærrede lokationer
Det kan ske, at du vil angive en lokation som spærret i en vis periode, f.eks. fordi der skal udføres reparationer. Det kan også ske, at det kun er nødvendigt at spærre for indlagrings- eller udlagringsstedet.

## <a name="tree-structure"></a>Træstruktur

Du kan få vist lagerlayoutet i en træstruktur baseret på koordinaterne for lagerlokationer i et visningsformat på siden Lagerlokationer.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Vedligehold lagerlokationer via lagerstedsformen

Det er muligt at kopiere lokationer fra ét lagersted til et andet og oprette steder via en guide. Inden du kører guiden, skal du kontrollere, at du har defineret standardlokalitetsnavnene på siden Lagersted.



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oprette en ny lageropbygning](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]