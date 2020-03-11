---
title: Oprette et nyt produkthierarki
description: Dette emne beskriver, hvordan du opretter et nyt produkthierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070415"
---
# <a name="create-a-new-product-hierarchy"></a>Oprette et nyt produkthierarki


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter et nyt produkthierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Dynamics 365 Commerce understøtter flere detailkanaler. Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker). Hver detailbutikskanal kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere. Du skal oprette alle disse elementer, for at du kan oprette en detailbutikskanal. 

Et Commerce-produkthierarki bruges for at definere det generelle produkthierarki for organisationen. Du kan bruge et Commerce-produkthierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg. Der kan kun tildeles ét Commerce-produkthierarki pr. organisation.

## <a name="create-and-configure-a-product-hierarchy"></a>Oprette og konfigurere et produkthierarki

Følg disse trin for at oprette og konfigurere et Commerce-produkthierarki.

1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Commerce-produkthierarki** i navigationsruden.
1. Hvis der endnu ikke findes et hierarki, skal du vælge **Ny** i **handlingsruden** for at oprette roden for hierarkiet.
1. Under **Generelt**:
    1. Indtast et navn i feltet **Navn**.
    1. Indtast en beskrivelse i feltet **Beskrivelse**.
    1. Indtast et brugervenligt navn i feltet **Brugervenligt navn**.
    1. Angiv **Aktiv** til **Ja**.

## <a name="add-hierarchy-nodes"></a>Tilføje hierarkinoder

Følg disse trin for at tilføje hierarkinoder.

1. Vælg **Rediger kategorihierarki** i handlingsruden.
1. Vælg den overordnede node, du vil føje en ny node til, og vælg derefter **Ny kategorinode**.
1. I afsnittet **Generelt** skal du angive **Navn**, **Beskrivelse**, **Brugervenligt navn** og **Nøgleord**.
1. Under **Generelt**:
    1. Indtast et navn i feltet **Navn**.
    1. Indtast en beskrivelse i feltet **Beskrivelse**.
    1. Indtast et brugervenligt navn i feltet **Brugervenligt navn**.
    1. Angiv relevante nøgleord i feltet **Nøgleord**.
    1. Angiv et nummer til visningsrækkefølgen, i feltet **Visningsrækkefølge** (valgfrit).
1. Gå til handlingsruden, og vælg **Gem**.
1. Gentag trinnene ovenfor for at tilføje yderligere noder.

Følgende billede viser oprettelsen af en ny produkthierarkinode.

![Oprette produkthierarki](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Andre indstillinger

Kategoriattributgrupper kan også tildeles til hver gruppe efter behov.  

## <a name="additional-resources"></a>Yderligere ressourcer

[commerce-hierarkier](retail-hierarchies.md)

[Administrere produktkategorier og -produkter ](category-management-product-creation.md)

[Ændre sorteringsrækkefølgen for merchandisingenheder](custom-order-categories-nav-retail-prod-hierarchy.md)
