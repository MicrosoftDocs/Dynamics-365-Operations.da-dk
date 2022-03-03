---
title: Evaluer alle handlinger for direktiver med flere SKU-lokationer
description: En ny funktion er blevet tilføjet for at evaluere alle handlinger med flere SKU-placeringsdirektiver. Denne side viser dig oplysninger om, hvordan du aktiverer den.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102957"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Indstillingen Flere SKU-indstillinger evaluerer ikke flere lokalitetsdirektivhandlinger

## <a name="symptoms"></a>Symptomer

Lokationsvejledninger for arbejdsordretypen *Salgsordrer* og arbejdstypen *Læg på lager* evaluerer ikke flere handlinger for lokationsvejledninger, når indstillingen **Flere SKU'er** er valgt. Det er kun den første handling i lokationsvejledningen, der evalueres.

## <a name="resolution"></a>Løsning

En ny funktion, *Evaluer alle handlinger for lokationsvejledninger med flere SKU'er*, er blevet tilføjet i version 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Denne funktion evaluerer alle handlinger for lokationsvejledninger med flere SKU'er. Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret.  Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Administratorer kan bruge siden [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere eller deaktivere den, hvis det er nødvendigt.
