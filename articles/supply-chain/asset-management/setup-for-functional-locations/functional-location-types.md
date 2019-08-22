---
title: Arbejdsstedstyper
description: Dette emne beskriver, hvordan du opretter arbejdsstedstyper i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: eb758f9ef205c06cbb9d18b498a5cd7c36012714
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783162"
---
# <a name="functional-location-types"></a>Arbejdsstedstyper

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emne beskriver, hvordan du opretter arbejdsstedstyper i Styring af aktiver. Arbejdsstedstyper bruges til at administrere krav til arbejdssteder, herunder hvordan aktiver installeres på et arbejdssted. Du kan oprette aktivtyper, vedligeholdelsesplaner, attributter for arbejdssteder og attributkrav til aktiver, der skal bruges på et arbejdssted, som bruger den specifikke arbejdsstedstype. Når du opretter et arbejdssted, er arbejdsstedstypen obligatorisk.

>[!NOTE] 
>For at kunne arbejde med arbejdssteder skal du oprette et standardarbejdssted, der kun skal bruges til at oprette nye aktiver. For dette standardarbejdssted skal du oprette en standardarbejdsstedstype, der er virkelig enkel og tillader, at flere aktiver installeres på standardarbejdsstedet. Du finder flere oplysninger om, hvordan du konfigurerer arbejdssteder, under [Oprette arbejdssteder](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Oprette en standardarbejdsstedstype

Denne procedure viser, hvordan du opretter en standardarbejdsstedstype, der skal bruges til et standardarbejdssted.

1. Vælg **Styring af aktiver** > **Opsætning** > **Arbejdssteder** > **Arbejdsstedstyper**.
2. Vælg **Ny** for at oprette en ny arbejdsstedstype.
3. Indsæt et arbejdsstedstype-id i feltet **Arbejdsstedstype**, for eksempel "Standard", og et navn i feltet **Navn**.
4. Vælg en livscyklusmodel i feltet **Livscyklusmodel for arbejdssted**.
5. Vælg "Ja" på til/fra-knappen **Flere aktiver** for at tillade, at flere aktiver installeres på et arbejdssted (standardarbejdsstedet) ved hjælp af denne type.

Nu oprettes den standardarbejdsstedstype, der kun skal bruges til et standardarbejdssted. Du bør ikke føje flere krav eller begrænsninger til denne standardarbejdsstedstype.


## <a name="create-functional-location-types"></a>Oprette arbejdsstedstyper

1. Vælg **Styring af aktiver** > **Opsætning** > **Arbejdssteder** > **Arbejdsstedstyper**.
2. Vælg **Ny** for at oprette en ny arbejdsstedstype.
3. Indsæt et arbejdsstedstype-id i feltet **Arbejdsstedstype** og et navn i feltet **Navn**.
4. Vælg en livscyklusmodel i feltet **Livscyklusmodel for arbejdssted**. Se [Livscyklustilstande for arbejdssted](../setup-for-functional-locations/functional-location-stages.md) for at få flere oplysninger om livscyklustilstande for arbejdssteder og livscyklusmodeller.
5. Vælg "Ja" på til/fra-knappen **Flere aktiver** for at tillade, at flere aktiver må installeres på et arbejdssted ved hjælp af denne arbejdsstedstype. Hvis du vælger "Nej", kan du kun installere *ét* aktiv på et arbejdssted ved hjælp af denne arbejdsstedstype.
6. Vælg "Ja" på til/fra-knappen **Opdater aktivdimension**, hvis du ønsker, at aktiver, der er installeret på et arbejdssted af denne type, automatisk skal bruge de økonomiske dimensioner, der er relateret til arbejdsstedet. Det betyder, at hvis du ændrer økonomiske dimensioner i formen [Arbejdssted](../functional-locations/create-functional-locations.md), og arbejdsstedet bruger en arbejdsstedstype, hvor denne til/fra-knap er angivet til "Ja", opdateres økonomiske dimensioner automatisk på alle aktiver, der er installeret på dette arbejdssted.
7. Feltet **Aktivtype** bruges, hvis du automatisk vil oprette *ét* aktiv for arbejdsstedet med det samme id og navn som det arbejdssted, du opretter. Dette kan for eksempel være relevant, hvis du opretter et statisk arbejdssted, f.eks en bygning eller pipeline. I så fald skal du vælge den aktivtype, du vil bruge til det automatisk oprettede aktiv. Husk, at hvis du foretager et valg i dette felt, skal til/fra-knappen **Flere aktiver** være indstillet til "Nej".
8. I oversigtspanelet **Aktivtyper** skal du vælge de aktivtyper, der skal relateres til arbejdsstedstypen. Vælg **Tilføj linje**, og vælg aktivtyperne. Hvis du tilføjer aktivtyper her, kan kun aktiver, der bruger disse aktivtyper, installeres på et arbejdssted ved hjælp af denne arbejdsstedstype. Hvis der ikke er valgt nogen aktivtyper i oversigtspanelet **Aktivtyper**, kan alle aktivtyper være installeret.
9. I oversigtspanelet **Vedligeholdelsesplaner** skal du vælge de vedligeholdelsesplaner, der automatisk skal konfigureres på nye arbejdssteder ved hjælp af denne arbejdsstedstype. Vælg **Tilføj linje**, og vælg vedligeholdelsesplanerne. Hvis du tilføjer vedligeholdelsesplaner her, er det kun disse planer, der kan bruges på et arbejdssted ved hjælp af denne arbejdsstedstype.
10. I oversigtspanelet **Krav til aktivattribut** skal du vælge de aktivattributter, der automatisk skal konfigureres på nye arbejdssteder ved hjælp af denne arbejdsstedstype. Vælg **Tilføj linje**, og vælg attributten. Disse attributkrav fungerer som retningslinjer. De valideres ikke i forhold til attributter, der er oprettet på et aktiv (**Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver** > vælg aktiv på listesiden > **Generelt**-fane > **Attributter**-knap). Attributkravene vises, når du installerer aktiver på arbejdssteder.
11. I oversigtspanelet **Tilladte typer** skal du vælge de arbejdsstedstyper, der skal være gyldige for underordnede arbejdsstedstyper, der er relateret til en overordnet arbejdsstedstype, som bruger den valgte arbejdsstedstype.
12. I oversigtspanelet **Attributter** skal du vælge de arbejdsstedsattributter, der automatisk skal konfigureres på nye arbejdssteder ved hjælp af denne arbejdsstedstype. Vælg **Tilføj linje**, og vælg attributten.


>[!NOTE] 
>I oversigtspanelet **Generelt** kan du se en oversigt over antallet af aktivtyper, vedligeholdelsesplaner, krav til aktivattribut, tilladte typer, attributter og arbejdssteder, der er konfigureret på arbejdsstedstypen. Feltet **Arbejdssteder** viser antallet af arbejdssteder, der bruger arbejdsstedstypen. Du kan bruge knappen **Kopiér** til at kopiere indstillinger fra en arbejdsstedstype til den valgte arbejdsstedstype.
