---
title: Mediegallerimodul
description: Dette emne omhandler mediegallerimoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: de0bc650393b035adea4570c5e64ecb76283117e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937380"
---
# <a name="media-gallery-module"></a>Mediegallerimodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler mediegallerimoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Mediegallerimoduler vises et eller flere billeder i en gallerivisning. Mediegallerimoduler understøtter miniaturebilleder, som kan arrangeres enten vandret (som en række under billedet) eller lodret (som en kolonne ved siden af billedet). Mediegallerimoduler indeholder også egenskaber, der gør det muligt at zoome billeder (forstørrer) eller få dem vist i fuld skærmtilstand. Hvis det skal gengives i et mediegallerimodul, skal der være et billede i mediebiblioteket til Commerce-webstedsgeneratoren. I øjeblikket understøtter mediegallerimoduler kun billeder.

I standardtilstanden bruger et mediegallerimodul det produkt-id, der er tilgængeligt fra sidekonteksten for en side med produktdetaljer (PDP), til at gengive de tilsvarende produktbilleder. I Commerce Headquarters skal der defineres en sti til en mediefil for alle produkter. Billeder skal derefter overføres til webstedsgeneratorens mediebibliotek i overensstemmelse med den filsti, der blev defineret for produkterne i Commerce Headquarters. Disse billeder omfatter billeder til produkter og produktvarianter. Du kan finde flere oplysninger om, hvordan du overfører billeder til mediebiblioteket i webstedsgeneratoren, under [Overføre billeder](dam-upload-images.md).

Alternativt kan et mediegallerimodul være vært for et fuldt sæt billeder på en billedgalleriside, hvor der ikke er afhængigheder af produkt-id'et eller sidekonteksten. I dette tilfælde skal billederne overføres til webstedsgeneratorens mediebibliotek og angives i webstedsgeneratoren.

Her er nogle eksempel eksempler til mediegallerimoduler:

- Gengivelse af produktbilleder på en PDP
- Gengivelse af produktbilleder på en produktmarketingside
- Fremvisning af et organiseret sæt af billeder på en marketingside, f.eks. en galleriside

I eksemplet i følgende illustration er der et købsfelt på en PDP-vært for produktbilleder ved hjælp af et mediegallerimodul.

![Eksempel på en købsfelt på en side med produktdetaljer, der er vært for produktbilleder ved hjælp af et mediegallerimodul](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Egenskaber for mediegalleri

| Egenskabsbetegnelse | Værdier | Beskrivende tekst |
|---------------|--------|-------------|
| Billedkilde | **Sidekontekst** eller **Produkt-id** | Standardværdien er **Sidekontekst**. Hvis der er valgt **Sidekontekst**, forventer modulet, at siden indeholder oplysninger om produkt-id. Hvis **Produkt-id** er valgt, skal produkt-id'et for et billede angives som værdien af egenskaben **Produkt-id**. Denne funktion er tilgængelig i Commerce version 10.0.12. |
| Produkt-id | Et produkt-id | Denne egenskab kan kun anvendes, hvis værdien af egenskaben **Billedkilde** er **Produkt-id**. |
| Billedzoom | **Indbygget** eller **Container** | Denne egenskab giver brugeren mulighed for at zoome billeder i mediegallerimodulet. Et billede kan zoomes enten indbygget eller i en separat container ved siden af billedet. Denne funktion er tilgængelig i 10.0.12. |
| Zoomfaktor | Et decimaltal | Denne egenskab specificerer den skaleringsfaktor, der skal anvendes til zoom af billeder. Hvis f.eks. værdien er indstillet til **2,5**, forstørres billederne 2,5 gange. |
| Fuld skærm | **Sand** eller **Falsk** | Denne egenskab specificerer, om billeder kan vises i fuld skærmtilstand. I fuld skærmtilstand kan billeder også forstørres, hvis zoomfunktionen er slået til. Denne funktion er tilgængelig fra frigivelsen af Commerce version 10.0.13. |
| Kvalitet af zoomet billede | Et tal fra 1 til og med 100, der repræsenterer en procentdel og vælges ved hjælp af en skyder | Denne egenskab definerer billedkvaliteten for zoomede billeder. Den kan angives til 100 procent for at sikre, at et billede altid bruger den højest mulige opløsning. Denne egenskab kan ikke anvendes til PNG-filer, da de bruger et format uden tab. Denne funktion er tilgængelig fra frigivelsen af Commerce version 10.0.19. |
| Billeder | Billeder, der er valgt fra mediebiblioteket til webstedsgenerator | Ud over at blive gengivet fra et produkt kan billeder organiseres for et mediegallerimodul. Disse billeder vil blive føjet til alle de produktbilleder, der er tilgængelige. Denne funktion er tilgængelig i Commerce version 10.0.12. |
| Miniatureretning | **Lodret** eller **Vandret** | Denne egenskab specificerer, om miniaturebilleder skal vises i en lodret stribe eller i en vandret stribe. |
| Skjule masterproduktbilleder for variant | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, når der vælges en variant, skjules billeder af masterproduktet, medmindre varianten ikke har nogen billeder. Denne egenskab påvirker ikke produkter, der ikke har varianter. |

I følgende illustration vises et eksempel på et mediegallerimodul, hvor indstillingerne af fuld skærm og zoom er tilgængelige.

![Eksempel på et mediegallerimodul, hvor indstillingerne af fuld skærm og zoom er tilgængelige](./media/ecommerce-media-zoom.png)

Følgende illustration viser et eksempel på et mediegallerimodul, der indeholder organiserede billeder (dvs. de angivne billeder ikke er afhængige af produkt-id'et eller sidekonteksten).

![Eksempel på et mediegallerimodul med organiserede billeder](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Når billedkilden er afledt fra sidekonteksten, bruges produkt-id'et fra PDP til at hente billederne. Mediegallerimodulet henter billedfilstien til produkter ved hjælp af Commerce Scale Unit-API'er (Application Programming Interfaces). Billederne hentes derefter fra mediebiblioteket, så de kan gengives i modulet.

## <a name="add-a-media-gallery-module-to-a-page"></a>Føje et mediegallerimodul til en side

Hvis du vil tilføje et mediegallerimodul på en marketingside, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Marketingskabelon** og derefter klikke på **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge skabelonen **Marketingskabelon**. Under **Sidenavn** skal du angive **Mediegalleriside** og derefter vælge **OK**.
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Media Gallery** og derefter **OK**.
1. Vælg **Produkt-id** under **Billedkilde** i egenskabsruden for mediegallerimodulet. Indtast produkt-id i feltet **Produkt-id**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Du bør kunne se billederne for produktet i en gallerivisning.
1. Hvis du kun vil bruge organiserede billeder, skal du vælge **Produkt-id** under **Billedkilde** i egenskabsruden. Derefter skal du under **Billeder** vælge **Tilføj et billede** så mange gange, som det kræves for at tilføje billeder fra mediebiblioteket.
1. Angiv de yderligere egenskaber, du vil, f.eks **Billedzoom**, **Zoomfaktor** og **Miniatureretning**.
1. Vælg **Gem**, når du er færdig, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Container-modul](add-container-module.md)

[Overføre billeder](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
