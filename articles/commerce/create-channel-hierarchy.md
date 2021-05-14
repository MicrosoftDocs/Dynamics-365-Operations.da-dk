---
title: Opret et navigationshierarki for kanal
description: Dette emne beskriver, hvordan du opretter et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951902"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Oprette et navigationshierarki for kanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Et navigationshierarki for en kanal bruges til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller ved POS.

## <a name="create-a-channel-navigation-hierarchy"></a>Opret et navigationshierarki for kanal

Benyt følgende fremgangsmåde for at oprette et navigationshierarki for en kanal.

1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Navigationskategorier for kanal** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Indtast et navn i feltet **Navn**.
1. Indtast en beskrivelse i feltet **Beskrivelse**.
1. Vælg **Opret**.
1. Vælg **Ny kategorinode** i handlingsruden for at oprette en rodnode.
1. Indtast et navn i feltet **Navn**.
1. Indtast en beskrivelse i feltet **Beskrivelse**.
1. Indtast et brugervenligt navn i feltet **Brugervenligt navn**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en rodnode.

![Eksempel på rodnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Oprette navigationskategorinoder

Følge disse trin for at oprette yderligere navigationskategorinoder, der repræsenterer produktkategorierne i kanalen.

1. Vælg den overordnede node, du vil føje en kategori til, i navigationsruden.
1. Vælg **Ny kategorinode** i handlingsruden.
1. Indtast et navn i feltet **Navn**.
1. Indtast en beskrivelse i feltet **Beskrivelse**.
1. Indtast et brugervenligt navn i feltet **Brugervenligt navn**.
1. Angiv en visningsrækkefølge i feltet **Visningsrækkefølge** (valgfrit).
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på et fuldført navigationshierarki for kanal.

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Føje produkter til kategorinoder

Følg disse trin for at føje produkter til kategorinoder.

1. Vælg en kategorinode.
1. Vælg **Tilføj** under **Produkter**.
1. Find de nye produkter, du vil tilføje, ved hjælp af produktnummer eller produktnavn, og vælg derefter **OK**.
1. Gå til handlingsruden, og vælg **Gem**.

> [!NOTE]
> Tilføjelse af produkter til en node i kanalnavigationshierarkiet er ikke tilstrækkeligt for at få vist produkterne på en valgt kanal. Produkterne skal også være tildelt en kanal. Yderligere oplysninger om tildeling finder du under [Administration af tildeling](assortments.md).

Følgende billede viser en eksempelnode med tilføjede produkter.

![Produkter føjet til en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Føje produktattributgrupper til kategorinoder

> [!NOTE]
> Der skal oprettes attributgrupper, før du kan føje dem til en node i navigationshierarkiet for en kanal.

Følg disse trin for at føje en produktattributgruppe til en kategorinode.

1. Vælg en kategorinode.
1. Vælg **Tilføj** under **Produktattributgruppe**.
1. Find de attributgrupper, du vil tilføje, og vælg derefter **OK**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser en eksempelnode med tilføjede produktattributgrupper.

![Produktattributgrupper på en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere udvalg](set-up-assortments.md)

[Administrere attributter for attributgrupper](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
