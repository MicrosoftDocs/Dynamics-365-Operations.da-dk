---
title: Kritikalitetstyper for aktiver
description: I emnet forklares kritikalitetstyper for aktiver i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb2da2d58b7f98fad80d0ea63bf4445ec4d08163
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808346"
---
# <a name="asset-criticality-types"></a>Kritikalitetstyper for aktiver

[!include [banner](../../includes/banner.md)]

 

I emnet forklares kritikalitetstyper for aktiver i Styring af aktiver. Aktivers kritikalitet er relateret til aktiver og overføres til arbejdsordrer. Den kan ikke ændres på en arbejdsordre. Aktivers kritikalitet bruges til at beregne arbejdsordrens kritikalitet i forbindelse med planlægningen af arbejdsordre. Det bruges med andre ord til at beregne, i hvilket omfang et vedligeholdelsesjob på et aktiv påvirker produktionsplanen og produktiviteten i virksomheden. Du finder flere oplysninger om den opsætning, der er relateret til beregningen af rangeringsresultater for planlægning af arbejdsordre under [Parametre for Styring af aktiver](../setup-for-objects/enterprise-asset-management-parameters.md).

Hvis du vil konfigurere kritikalitet, skal du først oprette de kritikalitetstyper, der bør bruges i opsætningen af aktiver. Du kan derefter oprette aktivkritikaliteter.

## <a name="set-up-criticality-types"></a>Konfigurer kritikalitetstyper

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **kritikalitetstyper**.
2. Vælg **Ny** for at oprette en post.
3. Indtast et tal, der angiver kritikaliteten, i feltet **Kritikalitet**.
4. Angiv et navn for kritikalitetstypen i feltet **Navn**.
5. Angiv en faktor i feltet **Faktor**. Denne faktor bruges i forbindelse med beregning af arbejdsordreplanlægningen til at bestemme den kritikalitetspost, der skal bruges. (Den post, der har den højeste faktor, bruges altid.) Denne indstilling er relevant, hvis der, som vist i følgende illustration, oprettes kritikalitetslinjer med samme kritikalitetsværdi.

    ![Siden Kritikalitetstyper](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Opsætning af aktivkritikaliteter

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivkritikaliteter**.
2. Vælg **Ny** for at oprette en post.
3. Afhængigt af det påkrævede detaljeringsniveau for aktivkritikalitet skal du foretage relevante valg i felterne **Arbejdssted**, **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Jobtypekategori**, **Jobtype**, **Jobtypevariant** og **sagskrav**.

    > [!NOTE]
    > Når en aktivkritikalitet er valgt, gennemgår Styring af aktiver alle aktivkritikalitetsposter for at kontrollere, om der er et muligt match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord kontrollerer Styring af aktiver først **Jobkrav**. Hvis der ikke findes et match, kontrolleres **Jobtypevarianten**. Hvis der ikke findes et match, kontrolleres **Jobtypn** osv. Som du kan se i sidens layout, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination. Hvis der ikke findes et match, bruges posten "standard", som ikke har nogen markeringer.

4. I feltet **Kritikalitet** skal du vælge en af de kritikalitetskoder, som du oprettede under den forrige procedure.

### <a name="notes-about-criticality-setup"></a>Bemærkninger til opsætning af kritikalitet

- Hvis du ændrer en aktivkritikalitet i denne opsætning, efter at du allerede har brugt den på en arbejdsordre, opdateres kritikaliteten på arbejdsordren ikke i overensstemmelse hermed.
- Kritikaliteten på en arbejdsordre genberegnes, hver gang en arbejdsordrelinje føjes til eller slettes fra arbejdsordren.
- Hvis en arbejdsordre indeholder flere arbejdsordrejobs, bruges den højeste kritikalitet i henhold til feltet **Faktor** på siden **Kritikalitetstyper** altid på arbejdsordren.
- Generelt set kan aktivkritikalitet ændre sig over en periode. Kritikalitet kan påvirkes af køb af nyt udstyr, renovering osv. Overvej at revurdere dine aktivkritikaliteter med jævne mellemrum (f.eks. én gang om året eller hvert andet år) for at sikre, at dine kritikalitetsdefinitioner svarer til din aktuelle produktionsopsætning.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]