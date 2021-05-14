---
title: Opret og vedligehold en lagerblokering
description: Dette emne beskriver, hvordan du kan bruge lagerblokeringen til at forhindre, at den fysiske disponible lagerbeholdning reserveres af andre udgående kildedokumenter.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956152"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opret og vedligehold en lagerblokering

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan bruge lagerblokeringen til at forhindre, at den fysiske disponible lagerbeholdning reserveres af andre udgående kildedokumenter. Før du starter procedurerne i dette emne, skal du have en vare, der er tilgængelig i den fysiske disponibke lagerbeholdning.

## <a name="block-inventory"></a>Bloker lager

Hvis du vil oprette en lagerblokeringspost, så lageret blokeres, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I overskriften i den nye blokeringspost skal du angive feltet **Varenummer** til den vare, der skal spærres, og angive en beskrivelse.
1. Indtast antallet af varer til blokering i feltet **Antal** i oversigtspanelet **Generelt**.
1. I oversigtspanelet **Lagerdimensioner** skal du angive den lokation og det lagersted, hvor de varer, du vil blokere, er placeret i øjeblikket.
1. Vælg **Gem** i handlingsruden.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Opdater betingelserne for lagerblokeringen

Benyt følgende fremgangsmåde for at opdatere en lagerblokeringspost.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.
1. Vælg den relevante blokeringspost i listeruden.
1. Rediger posten efter behov. Du kan f.eks ændre værdien for feltet **Forventet dato** for at angive, hvornår det blokerede lager forventes at blive tilgængeligt for reservation. Hvis indstillingen **Forventede tilgange** er valgt, vises datoen i den forventede transaktion. (Indstillingen **Forventede tilgange** vælges som standard, når du opretter en blokeringspost manuelt.)
1. Vælg **Gem** i handlingsruden.

## <a name="unblock-inventory"></a>Blokere lager

Hvis du vil fjerne en lagerblokeringspost, så lagerets blokering ophæves, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.
1. Vælg den relevante blokeringspost i listeruden.
1. Vælg **Slet** i handlingsruden.
1. Du bliver bedt om at bekræfte handlingen. Vælg **Ja** for at fortsætte.
1. Luk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
