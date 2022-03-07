---
title: Vedligeholdelsesattributtyper
description: Dette emne beskriver, hvordan du opretter attributtyper i Styring af aktiver.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec5552d96473403931bbd513ae68ef0fe3069209f52e813963914417ad41b88a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739125"
---
# <a name="maintenance-attribute-types"></a>Vedligeholdelsesattributtyper

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver, hvordan du opretter attributtyper i Styring af aktiver. Attributter bruges til at beskrive egenskaberne for forskellige elementer. Du kan konfigurere attributter for følgende elementer:

- [Arbejdsstedstyper](../setup-for-functional-locations/functional-location-types.md)
- [Oprette arbejdssteder](../functional-locations/create-functional-locations.md)
- [Aktivtyper](../setup-for-objects/object-types.md)
- Aktiver

De attributter, du kan angive, varierer afhængigt af elementet. For et arbejdssted kan du eksempelvis oprette attributter til konfigurationen og den fysiske størrelse af stedet. For en aktivtype eller et aktiv kan du konfigurere attributter for motorvolumen, strømforbrug og maksimal belastningskapacitet under forskellige forhold.

## <a name="create-attribute-types"></a>Oprette attributtyper

Du kan oprette dine egne attributtyper. Derudover kan du overføre produktdimensioner til siden **Attributtyper**.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Attributtyper**.
2. Første gang du konfigurerer attributtyper, skal du vælge **Opret produktdimensioner** for automatisk at overføre standarderne for produktdimensioner.
3. Vælg **Ny** for at oprette en ny attributtype.
4. Angiv et navn for attributtypen i feltet **Attributtype**.
5. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Vælg den relevante attributenhed efter behov i feltet **Enhed**.
7. Vælg en datatype for enheden i feltet **Datatype**.
8. Hvis du har valgt **Streng** som datatype, skal du følge disse trin for at oprette værdier for attributtypen:

    1. Vælg attributtypen, og vælg dernæst **Værdier**.
    2. Vælg **Ny** i feltet **Attributværdier**.
    3. Vælg en attributtype (dimension) i feltet **Attributtype**.
    4. Indtast en relateret værdi i feltet **Værdi**.
    5. Indtast en beskrivelse i feltet **Beskrivelse**.
    6. Gem posten.
    7. Vend tilbage til siden **Attributtyper**.

9. Gem posten.

    Feltet **Arbejdsstedstyper** viser antallet af arbejdssteder, der bruger attributtypen. Feltet **Aktivtyper** viser antallet af aktivtyper, der bruger det.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]