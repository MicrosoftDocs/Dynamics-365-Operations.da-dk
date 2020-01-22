---
title: Produktsamlingsmoduler
description: Dette emne indeholder en oversigt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/07/2020
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
ms.openlocfilehash: 31307035014f2fae6146f33bc23e3e06103f82eb
ms.sourcegitcommit: c237123ad94d9418994ac095fbd8634c05a927b1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943257"
---
# <a name="product-collection-modules"></a>Produktsamlingsmoduler

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Produktregistrering er et primært værktøj, som forhandlere bruger til at skabe kundeengagement et e-handelswebsted. Produktsamlingsmoduler hjælper forhandlerne med at skabe overbevisende indkøbsoplevelser ved at levere en intuitiv visuel brugergrænseflade, der kan bruges til hurtigt at oprette produktsamlinger.

Produktsamlingsmoduler repræsenterer fysiske produkter og serviceydelser på webstedet. Et produktsamlingsmodul er typisk kædet sammen med en detaljeside, hvor kunderne kan købe et produkt eller en serviceydelse eller få mere at vide om det. 

Kilderne til produktsamlinger kan være lister af følgende fire typer:

- Redaktionelle lister over produkter, der er defineret manuelt i Dynamics 365 Retail som relaterede produkter til et produkt, eller produktlister
- Algoritmiske lister, f.eks. lister over nye eller bedst sælgende eller populære produkter
- Anbefalingslister, der er baseret på maskinel indlæring
- Tilpasningslister, der understøtter personlige resultater for en kunde. Kunderne skal være logget på e-Commerce-webstedet for at se personlige resultater. Gæstebrugere kan ikke se personlige resultater. Kunderne kan fravælge personalisering fra [kontoadministrationssiden](account-management.md).

I følgende illustration vises de forskellige typer produktsamlinger, der bruges på et e-handelswebsted.

![Eksempel på de forskellige typer produktsamlinger på et e-handelswebsted](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Brug altid produktsamlingsmoduler til at vise en gruppe produkter af samme type.

## <a name="product-collection-modules-and-types"></a>Produktsamlingsmoduler og -typer

I følgende tabel beskrives de forskellige typer produktsamlingsmoduler i Dynamics 365 Commerce.

| Produktsamlingsmodul  | Type | Beskrivelse |
|----------------------------|------|-------------|
| Kategori                   | Kategori | Dette modul viser en liste over produkter i en kategori, der er defineret af navigationskategorihierarkiet, som detailhandleren har oprettet for en detailkanal. |
| Relaterede produkter           | Leder | Dette modul viser en liste over produkter, som en produktchef har konfigureret som relaterede produkter i Retail, for den relationstype, som forfatteren har valgt. |
| Overvågede produktlister      | Leder | Dette modul viser brugerdefinerede lister, som varemedarbejdere og redaktører har oprettet i Retail. |
| Ny(t)                        | Algoritmisk | Dette modul viser en liste over de nyeste produkter, der er blevet udvalgt til kanaler og kataloger. Denne liste kan vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling. |
| Bedst sælgende               | Algoritmisk | Dette modul viser en liste over produkter, der er rangeret efter det højeste salgsantal. Denne liste kan vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling. |
| Tendenser                   | Algoritmisk | Dette modul viser en liste over de mest populære produkter i en given periode. Denne liste kan vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling. |
| Ofte købt sammen | Kunstig intelligens/maskinel indlæring | Dette modul anvender maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale relaterede varer, der ofte indkøbes sammen med et bestemt produkt. Denne liste kan vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling. |
| Folk kan også godt lide           | Kunstig intelligens/maskinel indlæring | Dette modul bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale varer, der er relateret til et bestemt produkt. Denne liste kan vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling. |
| Muligheder til dig              | Kunstig intelligens/maskinel indlæring | Dette modul bruger maskinel indlæring til at analysere købsmønstrene for den bruger, der er logget på, og levere personlige anbefalinger, som er baseret på disse købsmønstre. For en gæstebruger vil denne liste være skjult. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Føje et produktsamlingsmodul til en kategoriside

Hvis du vil føje et produktsamlingsmodul til en kategoriside skal du følge disse trin.

1. Gå til dit websted i Dynamics 365 Commerce, og opret en side, der bruger samme skabelon som din standardkategoriside.
1. Vælg pladsen **Underordnet sidefod** i sidedispositionen, og vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Container** og derefter vælge **OK**.
1. Vælg ellipseknappen i containermodulet, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Produktsamling** og derefter vælge **OK**.  
![Eksempel på procesguiden for produktsamlingsmodul](./media/productCollectionModule.png)
1. Konfigurer indstillinger ved at vælge en passende datakilde og input til produktsamlingen.
1. Vælg **Tilføj en produktliste** i egenskabsruden for produktsamlingsmodulet.
1. Vælg listetypen i dialogboksen **Vælg produktlistekonfiguration**, angiv antallet af varer, og vælg evt. andre indstillinger, der er tilgængelige for listetypen. Du kan finde flere oplysninger om listetyper i tabellen nedenfor. 
1. Vælg **OK**.
1. Gem siden, og check den ind.

Følgende tabel viser de listetyper, der kan vælges i dialogboksen **Vælg produktlistekonfiguration**.

| Type                       | Beskrivelse | Brug | Sidekontekst | Specifik kontekst | Brugertilpasning |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produkter efter kategori       | En liste over produkter, der tilhører en given kategori. Denne kategori bestemmes enten af sidekonteksten eller den kontekst, forfatteren leverer. | Denne type liste kan bruges på alle sider (f.eks. en startside, kategoriside, marketingside eller en side med produktdetaljer \[PDP\]) til at fremme en bestemt kategori af produkter. | Kategori fra sidekonteksten, hvis den er tilgængelig (f.eks. en kategoriside) | Forfatteren kan angive en bestemt kategori som kontekst for listen. | Ikke relevant |
| Relaterede produkter           | En liste over produkter, som en produktchef har konfigureret som relaterede produkter for relationstypen i Retail. | Denne type liste bruges primært på PDP'er, men den kan bruges på alle sider, hvis der leveres et overordnet produkt. | Produkt fra siden, relationstype (obligatorisk) | Produktet kan vælges i vælgeren, og relationstypen bruges. | Ikke relevant |
| Organiseret                    | En brugerdefineret liste, som varemedarbejdere og redaktører har oprettet i Retail. | Forbedring af kategoriside, startside, sider for betaling og indkøbsvogn samt produktsider | Ikke relevant | Ikke relevant | Ikke relevant |
| Algoritmisk                | <ul><li>**Ny** – En liste over de nyeste produkter, der er blevet udvalgt til kanaler og kataloger.</li><li>**Bedst sælgende** – En liste over produkter, der er rangeret efter det højeste salgsantal.</li><li>**Mest populære** – En liste over de mest populære produkter i en given periode.</li></ul> | Startside, forbedring af kategoriside og sider for betaling og indkøbsvogn | Kategori fra sidekonteksten (f.eks. en kategoriside) | Den kategori, der bestemmes af webstedets forfatter | Understøttet |
| Ofte købt sammen | En liste, der bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale relaterede varer, der ofte indkøbes sammen med et bestemt produkt. | Denne type liste gælder kun for siden med indkøbskurven. | Indkøbskurv | Ikke relevant | Understøttet |
| Folk kan også godt lide           | En liste, der bruger maskinel indlæring til at analysere forbrugeres indkøbsmønstre og anbefale varer, der er relateret til et bestemt produkt. | Denne type liste bruges på PDP'er til at vise produkter, som andre kunder har købt. | Produktkontekst fra siden | Det produkt, der leveres af webstedets forfatter | Understøttet |
| Muligheder til dig              | En liste, der bruger maskinel indlæring til at bestemme kundernes præferencer. | Denne type liste kan bruges på alle sider. | Ikke relevant| Ikke relevant | Understøttet | 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Indholdsrigt blokmodul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Container-modul](add-container-module.md)

[Boksmodul til køb](add-buy-box.md)

[Oversigt over produktanbefalinger](product-recommendations.md)