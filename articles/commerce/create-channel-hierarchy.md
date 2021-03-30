---
title: Opret et navigationshierarki for kanal
description: Dette emne beskriver, hvordan du opretter et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e1462c10dfe1c858429e9f4cc5d720ca43df609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221323"
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
> Hvis du føjer produkter til en node i navigationshierarkiet for en kanal, er det ikke tilstrækkeligt, at produkterne vises i en valgt kanal – produkterne skal også være udvalgt til et produkt.

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