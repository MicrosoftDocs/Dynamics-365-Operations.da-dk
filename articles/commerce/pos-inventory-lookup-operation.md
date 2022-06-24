---
title: Lagersøgningshandling i POS
description: Denne artikel beskriver, hvordan du kan bruge lagersøgningshandlingen i Dynamics 365 Commerce POS til at få vist den disponible lagerbeholdning af produkter på tværs af butikker og lagersteder.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 01f10c348c61ffbcb30be26a57b3edd436aacc8f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850243"
---
# <a name="inventory-lookup-operation-in-pos"></a>Lagersøgningshandling i POS

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan bruge lagersøgningshandlingen i Dynamics 365 Commerce POS til at få vist den disponible lagerbeholdning af produkter på tværs af butikker og lagersteder.

En præcis visning af lageret for hele virksomheden hjælper lagermedarbejdere med at levere rettidig og effektiv kundeservice. Det vigtigste tidspunkt er det øjeblik, hvor en kunde er klar til at træffe en købsbeslutning. Det er vigtigt, at kasserere i en detailbutik har lageroplysninger i realtid eller næsten i realtid ved hånden, så de kan garantere præcis produktlevering og afhentning.

Lagersøgningshandlingen i Commerce POS hjælper detailforretninger med at få driftssikkerhed og få indsigt ved at knytte butikker til Commerce Headquarters. Denne funktionalitet giver en visning af lagertilgængelighed for produkter på tværs af butikker og lagersteder. Det hjælper også detailhandlere med at fremme effektiviteten og omkostningsbesparelser ved at forbedre lagerplanlægning i realtid.

Når lagersøgningshandlingen startes fra POS-programmet, bruger POS-kassereren det numeriske tastatur til at angive et produktnummer for at forespørge på lageroplysningerne. Hvis det angivne produkt har varianter, kan kassereren vælge dimensioner eller andre værdier for at kontrollere lageroplysningerne for en bestemt produktvariant.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Lagersøgningslistevisning for individuelle produkter

For enkeltprodukter giver lagersøgningshandlingen en lagersøgningslistevisning, der viser følgende produktoplysninger for en liste over lokationer:

- **Lager** – Refererer til det "fysisk disponible" antal af et produkt.
- **Reserveret** – Refererer til det "fysisk reserverede" antal, der hentes fra hovedkontoret.
- **Bestilt** – Refererer til det antal, der er "bestilt i alt" fra hovedkontoret.
- **Enhed** – Refererer til den lagermåleenhed, der er konfigureret i hovedkontoret.

Listevisningen over lokationer omfatter alle butikker og lagersteder, der er konfigureret i de opfyldningsgrupper, som den aktuelle butik er tilknyttet, som vist i følgende eksempelbillede.

![Lagersøgehandling i listevisning.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Sørg for, at den aktuelle butik er inkluderet i de tilknyttede opfyldningsgrupper.

De følgende handlinger er tilgængelige på POS-applinjen:

- **Sortér** – Denne handling giver POS-brugeren mulighed for at sortere dataene i listevisningen ud fra forskellige kriterier. Lokationsbaseret sortering er standardindstillingen for sortering.

    - **Geografisk placering** (fra den nærmeste placering til den placering, der ligger længst væk baseret på afstanden til den aktuelle butik)
    - **Navn** (i stigende eller faldende rækkefølge)
    - **Butiksnummer** (i stigende eller faldende rækkefølge)
    - **Lager** (i faldende rækkefølge)
    - **Reserveret** (i faldende rækkefølge)
    - **Bestilt** (i faldende rækkefølge)

- **Filter** – Denne handling giver POS-brugeren mulighed for at få vist filtrerede data for en bestemt placering.
- **Vis butikkens tilgængelighed** – Denne handling giver POS-brugeren mulighed for at se DTT-antallet (disponibel for tilsagn) for et produkt i den valgte butik.
- **Vis butiksplacering** – Denne handling åbner en separat side med kortvisning, adresse og butikstimer for den valgte butik.
- **Afhent i butik** – Denne handling opretter en debitorordre for det produkt, som vil blive plukket fra den valgte butik, og omdiriger brugeren til transaktionsskærmen.
- **Afsend produkt** – Denne handling opretter en debitorordre for det produkt, som vil blive afsendt fra den valgte butik, og omdiriger brugeren til transaktionskærmen.
- **Vis alle varianter** – For et produkt med varianter skifter denne handling fra en listevisning til en matrixvisning, der viser lageroplysninger for alle varianter af produktet.
- **Føj til transaktion** – Denne handling føjer produktet til indkøbsvognen og omdirigerer brugeren til transaktionsskærmen.

> [!NOTE]
> Den placeringsbaserede sortering, der blev introduceret i Commerce version 10.0.17, viser den aktuelle butik øverst. Ved andre placeringer bestemmes afstanden mellem placeringen og den aktuelle butik ud fra de koordinater (breddegrad og længdegrad), der er defineret i Commerce Headquarters. For en butik defineres placeringsoplysningerne i den primære adresse for den driftsenhed, der er knyttet til butikken. Hvis det drejer sig om et ikke-butikslagersted, defineres lokalitetsoplysningerne i lagerstedsadressen. Før version 10.0.17 viser listevisningen altid den aktuelle butik øverst og sorterer andre placeringer alfabetisk.
>
> Handlingerne **Vis butikkens tilgængelighed**, **Vis butiksplacering**, **Afhent i butik** og **Afsend produkt** er ikke tilgængelige for lokationer, som ikke er butiksplaceringer.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Lagersøgningsmatrixvisning for varianter

For et masterprodukt med varianter giver lagersøgningshandlingen også en dimensionsbaseret matrixvisning, der viser oplysninger om lagertilgængelighed for alle varianter af masterproduktet på en valgt lokation. Som standard viser matrixvisningen data for den aktuelle butik. Du kan bruge **Butik**-handlingen på applinjen til at slå lageroplysninger op i andre butikker, der er konfigureret i de opfyldningsgrupper, som den aktuelle butik er tilknyttet.

På følgende eksempelbillede ses visningen af lageropslagsmatrixen i POS.

![Lagersøgehandling i matrixvisning.](media/inventory-lookup-matrix-view.png)

I matrixvisningen repræsenterer hver celle en individuel variant og viser en værdi for den disponible lagerbeholdning (fysisk tilgængelige) i nederste højre hjørne, og de **reserverede** (fysisk reserverede) og **bestilte** værdier (bestilt i alt) vises i øverste venstre hjørne. Følgende tabel forklarer betydningen af de forskellige disponible værdier.

| Beholdningsværdi                            | Betegnelse |
|------------------------------------------|-------------|
| Numerisk værdi, der er større end 0 (nul) | En variant er frigivet til den valgte lokation, og du kan udføre yderligere handlinger i cellen. |
| **0** (nul)                             | En variant er blevet frigivet til den valgte lokation, men varen er ikke tilgængelig på den valgte lokation. Du kan udføre yderligere handlinger i cellen. |
| **i/t** eller en inaktiv celle              | En variant er blevet frigivet til den valgte lokation, og du kan ikke udføre yderligere handlinger i cellen. |

Visningsrækkefølgen for dimensionsværdierne i matrixvisningen er baseret på konfigurationen af dimensionsvisningsrækkefølgen i Commerce Headquarters. Du kan ændre konfigurationen af dimensionsvisningsrækkefølgen ved at vælge en ny dimension, der skal bruges. 

Følgende handlinger er tilgængelige i matrixvisningscellen:

- **Sælg nu** – Denne handling føjer den valgte variant til indkøbsvognen og omdirigerer brugeren til transaktionsskærmen.
- **Afhent i butik** – Denne handling opretter en debitorordre for den valgte variant, som vil blive plukket fra den valgte butik, og omdiriger brugeren til transaktionsskærmen.
- **Afsend produkt** – Denne handling opretter en debitorordre for den valgte variant, som vil blive afsendt fra den valgte butik, og omdiriger brugeren til transaktionsskærmen.
- **Tilgængelighed** – Denne handling fører brugeren til en separat side, der viser DTT-antallet for den valgte variant i den valgte butik.
- **Vis alle placeringer** – Denne handling skifter til listevisningen af standardlagerets tilgængelighed med lageroplysninger for den valgte variant.
- **Få vist produktoplysninger** – Denne handling omdirigerer brugeren til siden med produktdetaljer (PDP) for den valgte variant.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Adgang til lageropslag fra andre sider i POS

POS-brugere har adgang til lageropslagshandlingen fra andre sider i POS.

På følgende eksempelbillede ses lageropslagsresultater fra en PDP i POS.

![Lageropslag fra siden med produktdetaljer.](media/inventory-lookup-from-product-details-page.png)

I PDP for et masterprodukt kan du bruge handlingen **Vis alle varianter** på applinjen til at starte den lageropslagsmatrixvisning, der viser oplysninger om lagertilgængelighed for den aktuelle butik for alle varianter af et produkt. For et enkelt produkt viser PDP værdien for den disponible lagerbeholdning (fysisk tilgængelig) af det pågældende produkt for den aktuelle butik. Du kan også vælge linket **Andre butikslagre** for at starte lagersøgningshandlingen og kontrollere, om et produkt er til rådighed på tværs af andre butikker eller lagersteder.

> [!NOTE]
> Handlingen **Vis alle varianter** på PDP er kun tilgængelig for masterprodukter, der har varianter. Den er ikke tilgængelig for bestemte produkter eller pakker.

Du kan konfigurere, at lagersøgningshandlingen skal vises som et link i knapgitteret på POS-transaktionsskærmbilledet. Når brugeren vælger en indkøbsvognslinje og derefter vælger knappen **Lagersøgning**, vises lagersøgningslisten for det valgte produkt efter konfigurationen. Yderligere oplysninger om, hvordan du konfigurerer knapgitre ved hjælp af værktøjet POS-skærmlayoutdesigner, finder du i [Visuelle konfigurationer af POS-brugergrænseflade](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Lageropslag med beregning på kanalsiden

I Commerce version 10.0.9 og tidligere versioner hentes den **fysisk tilgængelige** værdi i lagersøgningshandlingen fra Commerce Headquarters via et servicekald i realtid. I Commerce version 10.0.10 og senere versioner kan du konfigurere POS-lagersøgningshandlingen til at bruge beregning på kanalsiden på Commerce-serveren for at bestemme værdien af fysisk tilgængelige, hvilket kan give en mere driftssikker og mere præcis forkalkulation af den disponible lagerbeholdning ved at indregne de transaktionsdata, der endnu ikke er synkroniseret med hovedkontoret. Du kan finde flere oplysninger om lagerberegning på kanalsiden og relateret POS-konfiguration på hovedkontoret i [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Visuelle konfigurationer af POS-brugergrænseflade](pos-screen-layouts.md)

[Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
