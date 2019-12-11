---
title: Produktsamlingsmoduler
description: Dette emne indeholder en oversigt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785461"
---
# <a name="product-collection-modules"></a>Produktsamlingsmoduler  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Produktregistrering er et primært værktøj, som forhandlere bruger til at skabe kundeengagement et e-handelswebsted. Produktsamlingsmoduler hjælper forhandlerne med at skabe overbevisende indkøbsoplevelser ved at levere en intuitiv visuel brugergrænseflade, der kan bruges til hurtigt at oprette produktsamlinger.

Produktsamlingsmoduler repræsenterer fysiske produkter og serviceydelser på webstedet. Et produktsamlingsmodul er typisk kædet sammen med en detaljeside, hvor kunderne kan købe et produkt eller en serviceydelse eller få mere at vide om det. 

Kilderne til produktsamlinger kan være lister af tre typer:

- Redaktionelle lister over produkter, der er defineret manuelt i Dynamics 365 Retail som relaterede produkter til et produkt, eller produktlister
- Algoritmiske lister, f.eks. lister over nye eller bedst sælgende eller populære produkter
- Anbefalingslister, der er baseret på maskinel indlæring

I følgende illustration vises de forskellige typer produktsamlinger, der bruges på et e-handelswebsted.

![Eksempel på de forskellige typer produktsamlinger på et e-handelswebsted](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Brug altid produktsamlingsmoduler til at vise en gruppe produkter af samme type eller med samme tema.

## <a name="product-collection-modules-and-types"></a>Produktsamlingsmoduler og -typer

I følgende tabel beskrives de forskellige typer produktsamlingsmoduler i Dynamics 365 Commerce.

| Produktsamlingsmodul  | Type | Beskrivelse |
|----------------------------|------|-------------|
| Gennemsøgning af kategorier            | Leder | Denne type produktsamlingsmodul bruger det navigationskategorihierarki, som forhandleren har oprettet for en detailkanal, til at vise et gennemsøgningsforløb for produkter, der tilbydes i en bestemt webstedskategori. |
| Søgeresultater             | Søgeforespørgsel | Denne type produktsamlingsmodul viser en liste over produkter, der passer bedst til den søgeforespørgsel, som kunden har angivet. |
| Relaterede produkter           | Leder | Denne type produktsamlingsmodul viser en liste over produkter, som en produktchef har konfigureret som relaterede produkter i Retail, for den relationstype, som forfatteren har valgt. |
| Overvågede produktlister      | Leder | Denne type produktsamlingsmodul viser brugerdefinerede lister, som varemedarbejdere og redaktører har oprettet i Retail. |
| Nyt                        | Algoritmisk | Denne type produktsamlingsmodul viser en liste over de nyeste produkter, der er blevet udvalgt til kanaler og kataloger. |
| Bedst sælgende               | Algoritmisk | Denne type produktsamlingsmodul viser en liste over produkter, der er rangeret efter det højeste salgsantal. |
| Tendenser                   | Algoritmisk | Denne type produktsamlingsmodul viser en liste over de mest populære produkter i et givet tidsinterval. |
| Ofte købt sammen | Kunstig intelligens/maskinel indlæring | Denne type produktsamlingsmodul bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale relaterede varer, der ofte købes sammen med et bestemt produkt. |
| Folk kan også godt lide           | Kunstig intelligens/maskinel indlæring | Denne type produktsamlingsmodul bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale varer, der ofte er relateret til et bestemt produkt. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Føje et produktsamlingsmodul til en kategoriside

Hvis du vil føje et produktsamlingsmodul til en kategoriside skal du følge disse trin.

1. Gå til dit websted i Dynamics 365 Commerce, og opret en side, der bruger samme skabelon som din standardkategoriside.
1. Vælg pladsen **Underordnet sidefod** i sidedispositionen, og vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Container** og derefter vælge **OK**.
1. Vælg ellipseknappen i containermodulet, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Produktsamling** og derefter vælge **OK**.
1. Konfigurer indstillinger ved at vælge en passende datakilde og input til produktsamlingen.
1. Vælg **Tilføj en produktliste** i egenskabsruden for produktsamlingsmodulet.
1. Vælg listetypen i dialogboksen **Vælg produktlistekonfiguration**, angiv antallet af varer, og vælg evt. andre indstillinger, der er tilgængelige for listetypen. Du kan finde flere oplysninger om listetyper i tabellen nedenfor. 
1. Vælg **OK**.
1. Gem siden, og check den ind.

Følgende tabel viser de listetyper, der kan vælges i dialogboksen **Vælg produktlistekonfiguration**.
   
| Type                       | Beskrivelse | Generel praksis | Kontekst, der kan afledes af sidekonteksten | Kontekst, som forfatteren kan tilsidesætte sidekonteksten med |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Produkter efter kategori       | En liste over produkter, der tilhører en given kategori. Denne kategori bestemmes enten af sidekonteksten eller den kontekst, forfatteren leverer. | Forbedring af kategoriside, startside, sider for betaling og indkøbsvogn samt produktsider | Kategori | Kategori, der bestemmes af forfatteren |
| Relaterede produkter           | En liste over produkter, som en produktchef har konfigureret som relaterede produkter i Retail for relationstypen. | Produktsider, sider for betaling og indkøbsvogn, side med ønskeliste og kundekontoside | Produkt, relationstype (obligatorisk)  | Produkt, relationstype |
| Organiseret                    | En brugerdefineret liste, som varemedarbejdere og redaktører har oprettet i Retail. | Forbedring af kategoriside, startside, sider for betaling og indkøbsvogn samt produktsider | Ikke tilgængelig | Listevælger |
| Algoritmisk                | <ul><li>**Ny** – En liste over de nyeste produkter, der er blevet udvalgt til kanaler og kataloger.</li><li>**Bedst sælgende** – En liste over produkter, der er rangeret efter det højeste salgsantal.</li><li>**Mest populære** – En liste over de mest populære produkter i en given periode.</li></ul> | Startside, forbedring af kategoriside og sider for betaling og indkøbsvogn | Kategori | Kategori, der bestemmes af forfatteren |
| Ofte købt sammen | En liste, der bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale relaterede varer, der ofte købes sammen med et bestemt produkt. | Produktsider og sider for betaling og indkøbsvogn | Produkt, indkøbsvogn | Medtag indkøbsvogn |
| Folk kan også godt lide           | En liste, der bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale varer, der er relateret til et bestemt produkt. | Produktsider og sider for betaling og indkøbsvogn | Produkt, indkøbsvogn | Ikke tilgængelig |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

