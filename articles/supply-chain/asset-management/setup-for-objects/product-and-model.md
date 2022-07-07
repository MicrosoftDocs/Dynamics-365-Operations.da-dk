---
title: Aktivproducenter og -modeller
description: Denne artikel beskriver, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b00cb62926f3a482ec655235b6e2f5880edbcd04
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016269"
---
# <a name="asset-manufacturers-and-models"></a>Aktivproducenter og -modeller

[!include [banner](../../includes/banner.md)]

 

Denne artikel beskriver, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver. Modeller kan relateres til aktivtyper.

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
    > Du kan også oprette relationer for aktivtyper, producenter og modeller i opslaget **Aktivtyper**. Du kan finde flere oplysninger under [Aktivtyper](../setup-for-objects/object-types.md).

    I oversigtspanelet **Detaljer** viser feltet **Modeller** antallet af aktivmodeller, der er konfigureret for den valgte aktivproducent. Feltet **Aktiver** viser antallet af aktiver, der bruger den valgte producent.
    
    Feltet **Aktiver** viser antallet af objekter, der bruger den valgte producentmodel.

> [!NOTE]
> En aktivtype kan have ingen aktivproducentmodelrelationer, den kan relateres til én aktivproducentmodel eller den kan være relateret til flere aktivproducentmodeller. Hvis en aktivtype er relateret til mindst én producentmodel, kan kun de kombinationer, der er konfigureret i opslaget **Producentmodel**, vælges på disse sider for Styring af aktiver, hvor en kombination af en aktivtype, producent og model kan konfigureres. Disse sider omfatter **Alle aktiver**, **Aktivstjenesteniveauer**, **Jobtypestandarder** og **Vedligeholdelsesbudget linjer**. Hvis nogle af aktivtyperne ikke er relateret til en producentmodel, vises kun de aktivtyper og producentmodeller, der heller ikke har nogen relation til aktivtyper, på siderne.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Vælge en producent og model på et objekt

1. Vælg **Styring af aktiver** \> **_Aktiver_* \> **Alle aktiver**.
2. I kolonnen **Aktiv** skal du vælge linket til aktivet. Siden med **Detaljer** vises.
3. Vælg **Rediger**.
4. I oversigtspanelet **Generelt** skal du vælge værdier i felterne **Producent** og **model**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]