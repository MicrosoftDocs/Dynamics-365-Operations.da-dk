---
title: Produktdataenheder
description: Dette emne indeholder oplysninger om de forskellige enheder, der kan bruges til at importere og eksportere produktdata.
author: cvocph
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 83191ea3d07ec9e2ed6261ee997e06b802ee7645
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935933"
---
# <a name="product-data-entities"></a>Produktdataenheder

[!include [banner](../includes/banner.md)]

For at importere og eksportere produktdata skal du anvende dataenheder. Følgende tabel indeholder oplysninger om de produktrelaterede dataenheder og beskriver formålet med hver enkelt.

| Enhed | Applikationsobjekttræ (AOT) navn (type) | Kommentarer |
|--------|-------------------------------------------|-------|
| Produkter V2 | EcoResProductV2Entity | Denne enhed bruges til at importere og eksportere delte produkter, specifikke produkter og produktmastere. Det giver mulighed for opdateringer. Den understøtter ikke sætbaserede SQL-handlinger. Det er aktiveret for Open Data Protocol (OData). |
| Frigivne produkter V2 | EcoResReleasedProductV2Entity | Denne enhed bruges til at importere og eksportere udgivne produkter, specifikke produkter og produktmastere. Det giver mulighed for opdateringer. Det kræver, at det delte produkt allerede er oprettet. Når et nyt frigivet produkt importeres, sker der en frigivelse af det delte produkt. Der er også separate enheder, der kan bruges til at importere og eksportere frigivne produktmastere og frigivne specifikke varianter. Denne enhed understøtter ikke sætbaserede SQL-handlinger eller slettehandlinger. Det er aktiveret for OData. |
| Frigivet produktoprettelse V2 | EcoResReleasedProductCreationV2Entity | Denne enhed bruges til at importere delte produkter og frigivne produkter i ét trin. Selvom det understøtter eksport, anbefales denne brug ikke, da formålet med enheden er produktoprettelse. Det understøtter ikke opdateringer. Det understøtter et begrænset sæt felter (felter, der er tilgængelige i dialogboksen produktoprettelse). Den understøtter ikke sætbaserede SQL-handlinger. Det er ikke afsløret gennem OData. |
| Produktvarianter | EcoResProductVariantEntity | Denne enhed bruges til at importere og eksportere delte produktvarianter. Det giver mulighed for opdateringer. Det kræver, at dimensionsværdierne allerede er oprettet. Integrationsnøglen er produktmaster plus produktdimensioner. Denne enhed understøtter ikke sætbaserede SQL-handlinger. Det er aktiveret for OData. Den understøtter slettehandlinger. Den kan ikke udvides ved at tilføje nye produktdimensioner. |
| Produktvarianter efter produktnummeridentifikation | EcoResProductNumberIdentifiedProductVariantEntity | Denne enhed bruges til at importere og eksportere delte produktvarianter. Det giver mulighed for opdateringer. Det kræver, at dimensionsværdierne allerede er oprettet. Integrationsnøglen er produktnummeret (hvorimod integrationsnøglen for enheden **Produktvarianter** er produktmaster plus produktdimensioner). |
| Frigivne produktvarianter | EcoResReleasedProductVariantEntity | Denne enhed bruges til at importere og eksportere udgivne produktvarianter. Det giver mulighed for opdateringer. Det kræver, at delte produktvarianter allerede er oprettet. Når en ny frigivet produktvariant importeres, sker der en frigivelse af den delte produktvariant. Denne enhed understøtter ikke sætbaserede SQL-handlinger. Det er aktiveret for OData. Selvom den understøtter slettehandlinger, forårsager denne brug i øjeblikket databeskadigelse på grund af en fejl i den aktuelle platform. Denne enhed kan ikke udvides ved at tilføje nye produktdimensioner. |
| Frigivne produktvarianter efter produktnummeridentifikation | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Denne enhed ligner enheden **Frigivne produktvarianter**, men integrationsnøglen er produktnummeret fremfor produktmasteren plus produktdimensionerne. Den kan udvides ved at tilføje nye produktdimensioner. |
| Salgbare frigivne produkter | EcoResSellableReleasedProductEntity | Denne enhed bruges kun til at eksportere salgbare produkter. Salgbare produkter er produkter med de oplysninger, der er påkrævet for at kunne bruges på en salgsordre. De samme regler gælder, når et produkt valideres ved brug af funktionen **Valider** på siden **Frigivet produkter**. |
| Frigivne specifikke produkter V2 | EcoResDistinctProductV2Entity | Denne enhed bruges kun til at eksportere specifikke produkter. De pågældende specifikke produkter kan være produkter, undertypeprodukter og produktvarianter. |
| Frigivne produktmastere V2 | EcoResProductMasterV2Entity | Denne enhed bruges til at importere og eksportere produktmastere. Den er ikke aktiveret til datastyring. |
| Vare - stregkode | EcoResProductBarcodeEntity | Denne enhed bruges kun til at eksportere produkter og stregkoder. |
| Tilstande for produktlivscyklus | EcoResProductLifecycleSateEntity | Denne enhed bruges til at importere og eksportere de forskellige produktlivscyklustilstande, der kan tildeles et produkt. |

> [!NOTE]
> Du kan kun bruge dataenheden **Frigivne produkter V2** til at importere produkter til systemet, hvis det delte produkt allerede er oprettet. Ellers skal du, for at importere produkter til systemet, bruge dataenheden **Produktoprettelse**.
