---
title: Produktsammenligningsmoduler
description: Denne artikel beskriver moduler til produktsammenligning og implementering af dem, så kunder kan foretage produktsammenligninger på Microsoft Dynamics 365 Commerce-e-handelswebsteder.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474120"
---
# <a name="product-comparison-modules"></a>Produktsammenligningsmoduler

[!include [banner](../includes/banner.md)]

Denne artikel beskriver moduler til produktsammenligning og implementering af dem, så kunder kan foretage produktsammenligninger på Microsoft Dynamics 365 Commerce-e-handelswebsteder.

> [!NOTE]
> Modulerne til produktsammenligning og knappen til produktsammenligning er tilgængelige i Dynamics 365 Commerce version 10.0.29. De kan både bruges til B2C-websteder (business-to-consumer) og B2B-websteder (business-to-business).

Funktioner til produktsammenligning giver mulighed for at sammenligne produktoplysninger på en produktsammenligningsside så kunder kan foretage bedre købsbeslutninger. Denne funktionalitet er konfigureret i Commerce-webstedsgenerator ved hjælp af modulet til produktsammenligning. På sider med produktoversigter som f.eks. kategoriresultater, søgeresultater og sider med produktsamlinger kan du konfigurere en knap til produktsammenligning, så kunderne kan føje produkter til en sammenligningspulje. Denne funktionalitet er konfigureret i webstedsgeneratoren ved hjælp af knapmodulet til produktsammenligning, som fungerer ligesom [modulet Hurtig visning](quick-view-module.md).

Når webstedsbrugere tilføjer produkter til sammenligning ved at vælge dem i produktfelter, vises der en sammenligningsbakke nederst på siden. Sammenligningsbakken viser de produkter, som kunden i øjeblikket sammenligner, sammen med korte forhåndsvisninger af produkterne. Webstedsbrugere kan også tilføje produkter fra sider med produktdetaljer, og de kan tilføje specifikke produktvarianter for at sammenligne med produktmastere.

Når kunder har føjet et par produkter til sammenligningsbakken, kan de vælge **Sammenlign**, så de bliver omdirigeret til en produktsammenligningsside. På siden til produktsammenligning vises produktoplysninger for hvert valgt produkt, så kunder kan sammenligne billeder, priser, produktdimensioner (størrelse, type og farve), oplysninger om samlede vurderinger og andre produktattributter.

I følgende illustration vises eksempler på knappen Sammenlign produkt, knappen Fjern fra sammenligning, sammenligningsikonet og siden til produktsammenligning.

![Oversigten over produktsammenligning viser knappen Sammenlign produkt, knappen Fjern fra sammenligning, sammenligningspanelet og siden til produktsammenligning.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Produktsammenligningssiden sammenligner et standardsæt af produktegenskaber og alle attributter, der kan vises på en PDP for et bestemt produkt.
> - Egenskaber som leveringsmåde, lagerbeholdning og måleenhed kan ikke ses på en produktsammenligningsside.
> - Kunder kan tilføje produkter fra forskellige kategorier til sammenligningen, forudsat at produkterne er fra samme katalog.
> - Funktionaliteten til produktsammenligning er i øjeblikket begrænset til sammenligning af produkter i et enkelt katalog. Webstedsbrugere kan ikke foretage sammenligninger på tværs af kataloger.
> - Du skal sikre dig, at egenskaben **Gengivelsesmodul på klientside** er ryddet for alle moduler til produktsammenligning.
> - Du skal sikre, at cachelagring på sideniveau er deaktiveret for alle sider, hvor modulet til produktsammenligning bruges. Disse sider omfatter PDP'er, PLP'er og sider til produktsammenligning. Du kan finde flere oplysninger under [Konfigurere sidelagring](e-commerce-extensibility/page-caching.md).

Følgende illustration viser et eksempel på en side med produktsammenligning.

![Produktsammenligningsside.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Føje produktsammenligningsmodulet til en ny side med produktsammenligning

Du kan oprette en dedikeret side til produktsammenligning ved at føje et modul for produktsammenligning til en sides brødtekst. Udover at give kunder mulighed for at sammenligne produktoplysninger om forskellige produkter kan du konfigurere modulet til produktsammenligning, så kunder kan vælge at gennemføre deres køb hurtigt, når de sammenligner produkter. Modulet til produktsammenligning indeholder også en plads til **Tom sammenligning**, hvor du kan tilføje et indholdsblokmodul, der beskriver den tomme tilstand (f.eks. "Din produktsammenligning er tom").

Hvis du vil føje produktsammenligningsmodulet til en ny side med produktsammenligning, skal du følge disse trin.

1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Angiv et passende sidenavn (f.eks. **Produktsammenligning**) under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg den ønskede skabelon (der f.eks. bruges på din standardkategoriside) under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du skal redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**.
1. På pladsen **Hoved** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Produktsammenligning** og derefter **OK**.
1. Vælg ellipseknappen (**...**) i pladsen **Hurtig visningsknap**, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Kvikvisning af produkt** og derefter **OK**.
1. Angiv egenskaber for modulet i ruden Egenskaber til højre ved at konfigurere **Kvikvisning af produkt**.
1. På pladsen **Tom sammenligning** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Indholdsblok** og derefter **OK**.
1. Angiv egenskaber for modulet i ruden Egenskaber til højre ved at konfigurere **Indholdsblok**. 
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

I følgende illustration vises et eksempel på en tom sammenligningsside i webstedsgeneratoren.

![Produktsammenligningsmodul.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Tilføje en knap til produktsammenligning i produktfelter på sider med søge- og kategoriresultater

Knappen til produktsammenligning giver brugerne mulighed for hurtigt at føje et produkt til sammenligningen, når de gennemser produkter på en listeside. De kan tilføje et eller flere produkter til sammenligningen fra en listeside uden at skulle gå til PDP.

Knappen til produktsammenligning understøttes af modulerne produktsamling, søgeresultater og PDP-købsboks.

Tilføj en knap til produktsammenligning i produktfelter på sider med søge- og kategoriresultater ved at følge disse trin.

1. Gå til **Sider** i webstedsgeneratoren, og åbn den kategoriside, hvor du vil føje en knap til produktsammenligning.
1. På pladsen **Hoved** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Søgeresultater** og derefter **OK**.
1. Vælg pladsen til **Knappen til produktsammenligning** i modulet **Søgeresultater** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Knap til produktsammenligning** og derefter **OK**.
1. Angiv egenskaber for modulet i ruden Egenskaber til højre ved at konfigurere **Knap til produktsammenligning**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Angiv det maksimale antal produkter, der skal vises i sammenligningen.

Du kan angive det maksimale antal produkter, der kan vises i sammenligningen, ved at gå til **Webstedsindstillinger \> Udvidelser** i webstedsgeneratoren. Du kan konfigurere separate maksimumgrænser for visninger til skriveborde og mobiler/tablets. Der gennemtvinges som standard ingen grænse, hvis der ikke er defineret en maksimumgrænse.

> [!NOTE]
> Hvis du vil opnå en optimal gennemsynsoplevelse, anbefales det, at du angiver det maksimale antal produkter i sammenligningen til **2** for mobilbilledet og **4** for skrivebordsbilledet for at reducere mængden af vandret rulning.

Angiv det maksimale antal produkter, der skal vises i sammenligningen, ved at følge disse trin.

1. Gå i webstedsgenerator til **Webstedsindstillinger \> Udvidelser**.
1. For **Grænse for produkter i sammenligning – stationære computere** skal du angive det maksimale antal produkter, der skal vises i sammenligningen for skrivebordsvinduer.
1. For **Grænse for produkter i sammenligning – mobil- og tabletenheder** skal du angive det maksimale antal produkter, der skal vises i sammenligningen for mobil- og tabletvinduer.
1. Vælg **Gem og publicer** på kommandolinjen.

![Indstillinger af websted for at begrænse produkter til sammenligningen.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
