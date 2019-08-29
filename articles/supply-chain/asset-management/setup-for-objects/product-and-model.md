---
title: Aktivproducenter og -modeller
description: I dette emne beskrives, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783159"
---
# <a name="asset-manufacturers-and-models"></a>Aktivproducenter og -modeller

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I dette emne beskrives, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver. Modeller kan relateres til aktivtyper.

## <a name="set-up-product-model-relations"></a>Konfigurer produktmodelrelationer

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Producent og model**.
2. Vælg **Ny** for at oprette et nyt produkt.
3. I feltet **Producent** skal du indtaste aktivproducentens navn.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I oversigts panelet **Modeller** skal du vælge **Tilføj** for at oprette en aktivmodel, der skal relateres til aktivproducenten.
6. I feltet **Model** skal du indtaste aktivmodellens navn.
7. Indtast en beskrivelse i feltet **Beskrivelse**.
8. I feltet **Aktivtype** skal du vælge den aktivtype, som producentmodellen skal relateres til.

    > [!NOTE]
    > Du kan også oprette relationer for aktivtyper, producenter og modeller i opslaget **Aktivtyper**. Du kan finde flere oplysninger under [Opret en aktivtype](../setup-for-objects/object-types.md).

    I oversigtspanelet **Detaljer** viser feltet **Modeller** antallet af aktivmodeller, der er konfigureret for den valgte aktivproducent. Feltet **Aktiver** viser antallet af aktiver, der bruger den valgte producent.
    
    Feltet **Aktiver** viser antallet af objekter, der bruger den valgte producentmodel.

> [!NOTE]
> En aktivtype kan have ingen aktivproducentmodelrelationer, den kan relateres til én aktivproducentmodel eller den kan være relateret til flere aktivproducentmodeller. Hvis en aktivtype er relateret til mindst én producentmodel, kan kun de kombinationer, der er konfigureret i opslaget **Producentmodel**, vælges på disse sider for Styring af aktiver, hvor en kombination af en aktivtype, producent og model kan konfigureres. Disse sider omfatter **Alle aktiver**, **Aktivstjenesteniveauer**, **Jobtypestandarder** og **Vedligeholdelsesbudget linjer**. Hvis nogle af aktivtyperne ikke er relateret til en producentmodel, vises kun de aktivtyper og producentmodeller, der heller ikke har nogen relation til aktivtyper, på siderne.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Vælge en producent og model på et objekt

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**.
2. I kolonnen **Aktiv** skal du vælge linket til aktivet. Siden med **Detaljer** vises.
3. Vælg **Rediger**.
4. I oversigtspanelet **Generelt** skal du vælge værdier i felterne **Producent** og **model**.