---
title: Brødkrummemodul
description: Dette emne omhandler brødkrummemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 050ba58073d6e7e7710ab768e7ce3ea628440f4d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346942"
---
# <a name="breadcrumb-module"></a>Brødkrummemodul

[!include [banner](includes/banner.md)]

Dette emne omhandler brødkrummemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Brødkrummemoduler bruges til at tillade sekundær navigation på webstedssider. De vises normalt øverst på en side under overskriften. Selvom der kan føjes brødkrummemoduler til en hvilken som helst side, bruges de oftest på sider med produktoplysninger (PDP'er) til visning af produktkategorihierarkiet og er en hurtig måde at bevæge dig rundt på et websted på. Et brødkrummemodul kan også bruges til at vise et "Tilbage til resultater"-link, når brugerne åbner en PDP fra en søge- eller listeside. På denne måde kan brugerne hurtigt vende tilbage til deres filtrerede listeside for at fortsætte med at handle.

På sider med produktkategorikontekst, f.eks. PDP'er og kategorisider, viser brødkrummemoduler kategorihierarkiet. På sider, der ikke har kategorikontekst, viser brødkrummemoduler som standard **&lt;Webstedsrod&gt; / &lt;Aktuel side&gt;**. Brødkrummemoduler kan også konfigureres manuelt på andre typer webstedssider, så der vises links til bestemte sider på webstedet.

> [!NOTE]
> Brødkrummemodulet er tilgængeligt i Dynamics 365 Commerce version 10.0.12.

Det følgende billede viser et eksempel på et brødkrummemodul, der viser kategorihierarkiet på en PDP.

![Eksempel på et brødkrummemodul.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Indstillinger for brødkrummemodul

Brødkrummemodulet er afhængigt af indstillingen **Visningstype for brødkrumme på PDP**, som defineres i **Webstedsindstillinger \> Udvidelser** i webstedsgeneratoren. Denne indstilling har tre mulige værdier:

- **Vis kategorihierarki** – Når denne værdi er valgt, vil brødkrummemodulet vise hele kategorihierarkiet for det produkt, der ses på PDP'en.
- **Vis tilbage til resultater** – Når denne værdi er valgt, vil brødkrummemodulet vise linket "Tilbage til resultater" på en PDP, hvis brugeren åbnede PDP'en fra et modul, der tillader linket "Tilbage til resultater". Denne funktionalitet er tilgængelig, når brugere navigerer fra listesider for kategorier, søgninger, lister og anbefalinger. For at understøtte denne funktion har moduler med produktsamlinger og søgeresultater en egenskab, der har fået navnet **Tillad tilbage til resultater på PDP**. Denne egenskab giver dig fleksibiliteten til at definere, hvilke moduler der skal understøtte linkfunktionen "Tilbage til resultater" på PDP'en. Hvis f.eks. **Vis tilbage til resultater** er valgt for indstillingen **Visningstype for brødkrumme på PDP** for brødkrummemodulet, og **Tillad tilbage til resultater på PDP** er valgt for søgesidens modul for søgeresultater, vises linket "Tilbage til resultater", når brugere går fra søgesiden til en PDP.
- **Vis kategorihierarki og tilbage til resultater** – Denne værdi er en kombination af de to foregående. Når denne værdi er valgt, viser brødkrummemodulet både det fulde kategorihierarki og linket "Tilbage til resultater" (hvis det er konfigureret) på en PDP.

> [!IMPORTANT]
> Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Egenskaber for brødkrummemodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Rod | Tekst eller link| Denne valgfrie egenskab angiver linktekst og en linkdestination for brødkrummens webstedsrod. Hvis denne egenskab ikke er konfigureret, vil der ikke blive defineret en rod. |
| Link til brødkrumme | Binding | Denne valgfrie egenskab angiver links til en manuelt konfigureret brødkrumme, hvis disse links er påkrævede. Links vises i den rækkefølge, de er angivet i. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Føje et brødkrummemodul til en ny side

Hvis du vil føje et brødkrummemodul til en PDP og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Indstillinger for websted \> Udvidelser** og derefter til **Visningstype for brødkrumme på PDP**, vælg **Vis kategorihierarki**.
1. Gå til **Skabeloner**, og vælg PDP-skabelonen.
1. På pladsen **Container**, der indeholder købefeltmodulet, skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn en PDP, der bruger PDP-skabelonen. Hvis der endnu ikke findes en PDP, skal du oprette en.
1. På pladsen **Container**, der indeholder købefeltmodulet, skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.
1. I egenskabsruden for pladsen **Brødkrumme** skal du under **Rod** vælge **Linktekst**.
1. I dialogboksen **Linktekst** skal du skrive **Start** og derefter under **Linkdestination** vælge **Tilføj et link**.
1. I dialogboksen **Tilføj et link** skal du vælge et link for brødkrummeroden og derefter vælge **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Navigationsmenumodul](nav-menu-module.md)

[Webstedsvælgermodul](site-selector.md)

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Produktsamlingsmoduler](product-collection-module-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]