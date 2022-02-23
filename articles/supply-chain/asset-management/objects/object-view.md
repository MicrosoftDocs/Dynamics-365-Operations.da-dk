---
title: Visning af aktiver
description: Dette emne beskriver visning af aktiver i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0256cc86dc306c8addb37d2c8f335470b19177a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019398"
---
# <a name="asset-view"></a>Visning af aktiver

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver visning af aktiver i Styring af aktiver. Siden **Visning af aktiver** viser aktive aktiver og arbejdssteder i en trævisning. Du kan derved nemt danne dig et overblik over aktivrelationer til arbejdssteder. Du kan også få vist detaljerede oplysninger om arbejdssteder, aktiver og relaterede styklister (BOM'er). Du kan også få et hurtigt overblik over aktive vedligeholdelsesanmodninger og arbejdsordrer, der er relateret til et aktiv.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Visning af aktiver**.
2. Hvis du vil ændre den visning, der fremgår af siden, skal du vælge en ny værdi i feltet **Visning**.

    > [!NOTE]
    > Den standardvisning, der vises, når du åbner siden **Visning af aktiver**, afhænger af den værdi, der er valgt i feltet **Visning** under fanen **Aktiver** på siden **Parametre for Styring af aktiver** (**Styring af aktiver** \> **Opsætning** \> **Parametre for Styring af aktiver)**.

I højre side af siden viser oversigtspaneler oplysninger om den valgte visning.

Den breadcrumb-sti, der vises over trævisningen, viser det aktuelle udvalg i træstrukturen. Denne breadcrumb-sti bruger følgende format:

ID for arbejdssted/ID for arbejdssted (hvis der er mere end et arbejdssted) \> Aktiv-ID/Aktiv-ID (hvis der er mere end ét aktiv) - varenummer.

Hvis du har valgt et aktiv i træstrukturen, kan du vælge **Aktive anmodninger** eller **Aktive arbejdsordrer** for at få vist de vedligeholdelsesanmodninger eller arbejdsordrer, der er relateret til aktivet. Du kan også vælge **Åbn** \> **Arbejdssted**, **Aktiv** eller **Aktivstykliste** for at åbne den relaterede visning.

Indstillingen **Aktivers arbejdssteder**, som du kan vælge i feltet **Visning**, er også tilgængelig i alle aktivopslag, hvor du kan vælge et aktiv. Trævisningen vises eksempelvis på fanen **Visning af aktiv**, hvor du [opretter et aktiv](../objects/create-an-object.md), opretter en vedligeholdelsesanmodning eller opretter en arbejdsordre.
