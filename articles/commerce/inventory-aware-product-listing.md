---
title: Lagerbaseret produktnotering
description: Denne artikel beskriver, hvordan organisationer kan konfigurere produktnoteringssider på deres Microsoft Dynamics 365 Commerce-e-handelswebsted, så de er lagerbaserede.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: e33a4dd8650ee2e371c51c5a19e955f2d2bdade2
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405544"
---
# <a name="inventory-aware-product-listing"></a>Lagerbaseret produktnotering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel beskriver, hvordan organisationer kan konfigurere produktnoteringssider på deres Microsoft Dynamics 365 Commerce-e-handelswebsted, så de er lagerbaserede. Produktnoteringssider omfatter kategorilandingssider og søgeresultatsider.

Kunder forventer generelt, at et e-handelswebsted er lagerbaseret i produktsøgningen, så de kan beslutte, hvad de skal gøre, hvis et bestemt produkt ikke er på lager. Kategorien [Commerce-modulbibliotek](starter-kit-overview.md) og moduler med søgeresultater kan konfigureres, så de omfatter lagerdata. På den måde kan de give følgende oplevelser:

- Vis lagerniveaulabels sammen med produkter.
- Skjul produkter, der ikke er på lager, på produktlisten.
- Flytte produkter, der ikke er på lager, nederst på produktlisten.
- Understøt lagerbaseret produktfiltrering.

Hvis du vil aktivere disse erfaringer, skal du først aktivere **Udvidet e-handels-produktregistrering, der er lagerfølsom** i Commerce headquarters.

> [!NOTE]
> Funktionen **Udvidet e-handelsproduktregistrering, der er lagerfølsom** er som standard aktiveret fra og med Commerce version 10.0.29.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Konfigurere produktattribut for tilgængelighed af lager

En lagerbaseret produktnotering bruger struktur for produktattributter. Der skal som en forudsætning oprettes en dedikeret produktattribut til registrering af data for lagertilgængelighed.

Følg disse trin for at konfigurere produktattribut for lagertilgængelighed i Commerce headquarters.

1. Gå til **Retail og Commerce \> Detail- og handels-it \> Produkter og lager \> Udfyld produktattributter med lagerniveau**.
1. I feltet **Produktattributter og -typenavn** i dialogboksen **Udfyld produktattributter med lagerniveau** skal du angive et brugerdefineret navn til den dedikerede produktattribut, der skal oprettes til registrering af lagerdata.
1. I feltet **Lagertilgængelighed baseret på** skal du vælge det antal, som beregningen af lagerniveau skal baseres på: **Fysisk disponibelt** eller **I alt disponibelt**
1. Angiv indstillingen **Batchbehandling** til **Ja**.
1. Vælg **OK**.

> [!NOTE]
> Hvis du vil udføre ensartede beregninger af lagerniveau på tværs af sider på e-handelswebstedet, skal du sikre dig, at du vælger den samme indstilling for antal i både feltet **Lagertilgængelighed baseret på** til jobbet **Udfyld produktattributter med lagerniveau** og indstillingen **Lagerniveau baseret på** i Commerce-webstedsgeneratoren.

Når den dedikerede produktattribut er oprettet, er næste trin at konfigurere attributten til onlinekanalen.

Følg disse trin for at konfigurere attributten for onlinekanalen i Commerce headquarters.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg den onlinekanal, du vil aktivere lagerbaseret produktnotering for.
1. Vælg og åbn en tilknyttet attributgruppe, og føj den nye produktattribut til den.
1. Gå til **Retail og Commerce \> Detail- og handels-it \> Dostributionsplan**, og kør job **1150** (**Katalog**). Vi anbefaler, at du planlægger dette job som en batchproces, der kører med samme frekvens som jobbet **Udfyld produktattributter med lagerniveau**.

> [!NOTE]
> I Commerce version 10.0.26 og tidligere, efter at du har føjet produktattributten for lagertilgængelighed til en attributgruppe, skal du også vælge **Indstil attributmetadata** og derefter aktivere **Vis attribut på kanal**, **Kan hentes**, **Kan redigeres** og **Kan forespørges** for den nye produktattribut.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Konfigurere visningsmåden for produkter, der ikke er på lager, på produktnoteringssider

Når alle de foregående konfigurationstrin er udført, kan kategori- og søgeresultatsiderne redigeres med en lagerbaseret filterindstilling. Der vises en label på lagerniveau for hvert produktfelt, der ses på siden.

På siden med kategori- og søgeresultater vises produkter på masterniveau, ikke på produktvariantniveau. Det lagerniveau, der vises sammen med hvert produkt, er et samlet lagerniveau, der bestemmes af lagerniveauet for alle et produkts varianter. Lagerniveauet for en variant beregnes på basis af den tilgængelige lagerbeholdning af denne variant på standardlagerstedet for onlinekanalen i Commerce headquarters. Lagerniveauet for et masterprodukt har to mulige værdier, der repræsenterer varer på lager og ikke-lagervarer. Et masterprodukt anses kun for ikke at være på lager, når alle varianterne ikke er på lager. Ellers betragtes det som værende på lager. Den faktiske tekst til værdierne hentes fra definitionen på [lagerniveau](inventory-buffers-levels.md). Hvis der ikke er defineret noget lagerniveau, er standardlabels (på dansk) **Tilgængelig** og **Udsolgt**.

Du kan konfigurere indstillingen **Lagerindstillinger for produktlistesider** i Commerce-webstedsgeneratoren til at styre, hvordan kategori- og søgeresultatsiden viser produkter, der ikke er på lager. Du finder flere oplysninger under [Anvendelse af lagerindstillinger](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
