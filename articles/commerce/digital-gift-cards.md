---
title: Digitale e-handelsgavekort
description: Dette emne beskriver, hvordan digitale gavekort fungerer i e-handelsimplementeringen af Microsoft Dynamics 365 Commerce. Den giver også en oversigt over vigtige konfigurationstrin.
author: anupamar-ms
ms.date: 05/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: de8811b3265bc582a055aaad1f3dea32def552f4
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809581"
---
# <a name="e-commerce-digital-gift-cards"></a>Digitale e-handelsgavekort

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan digitale gavekort fungerer i e-handelsimplementeringen af Microsoft Dynamics 365 Commerce. Den giver også en oversigt over vigtige konfigurationstrin.

I Dynamics 365 Commerce følger købet af digitale gavekort samme proces som købet af andre produkter i systemet. Der behøver ikke være konfigureret yderligere moduler. Hvis der føjes flere gavekort til indkøbsvognen, aggregeres gavekortvarerne ikke på en enkelt salgslinje. Denne funktionalitet er påkrævet, da hver salgslinje faktureres ved hjælp af et separat gavekortnummer.

Købet af digitale gavekort understøttes i Dynamics 365 Commerce version 10.0.16 og senere.

I følgende illustration vises et eksempel på siden med produktdetaljer (PDP) til et digitalt gavekort på Fabrikams e-handelswebsted.

![Eksempel på digital gavekort-PDP på Fabrikams e-handelswebsted.](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Aktivere funktionen for digitale gavekort i Commerce Headquarters

For at indkøbsflowet for digitale gavekort kan fungere i Dynamics 365 Commerce skal funktionen **Købsgavekort på-handel** være aktiveret i Commerce Headquarters. Du kan finde funktionen i **Funktionsstyring** i Commerce Headquarters, som vist i følgende illustration.

![Arbejdsområdet Funktionsstyring i Commerce Headquarters.](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Konfigurer et digitalt gavekort i Commerce Headquarters

Digitale gavekortprodukter skal konfigureres i Commerce Headquarters. Fremgangsmåden minder om processen for andre produkter. Men følgende vigtige trin gælder specifikt for konfigurationen af gavekort til køb. Yderligere oplysninger om, hvordan du opretter og konfigurerer produkter, finder du i afsnittet [Opret et nyt produkt i Commerce](create-new-product-commerce.md).

- Når du konfigurerer digitale gavekortprodukter i dialogboksen **Nyt produkt**, skal du angive feltet **Produkttype** til **Service**. (Hvis du vil åbne dialogboksen, skal du gå til **Detail og handel \> Produkter og kategorier \> Produkter efter kategori** og vælg **Ny**.) Produkter af typen **Service** kontrolleres ikke for disponible lagerbeholdninger, før der afgives en ordre. Du kan finde flere oplysninger i [Oprette et nyt produkt](create-new-product-commerce.md#create-a-new-product).
- På siden **Commerce-parametre** under fanen **Bogføring** skal feltet **Gavekortprodukt** angives til **Digitalt gavekort** som vist i følgende illustration. Hvis produktet er et eksternt gavekort, kan du finde flere oplysninger i [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).

    ![Feltet Gavekortprodukt i Commerce Headquarters.](./media/PostGiftcard.png)

- Hvis et gavekort skal understøtte flere foruddefinerede beløb (f.eks. $25, $50 og $100), skal dimensionen **Størrelse** bruges til at konfigurere de foruddefinerede beløb. Hvert foruddefineret beløb er en produktvariant. Du kan finde flere oplysninger under [Produktdimensioner](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).
- Hvis kunder skal kunne angive et brugerdefineret beløb for et gavekort i tillæg til forhåndsdefinerede beløb, skal du først oprette en variant, der tillader et brugerdefineret beløb. **Størrelse**-attributten understøtter brugerdefinerede beløbsvarianter. Åbn derefter produktet fra siden **Frigivne produkter i kategori**, og angiv i oversigtspanelet **Commerce** i feltet **Indtast pris** til **Ny pris skal indtastes**, som vist i følgende eksempelillustration. Denne indstilling sikrer, at kunder kan indtaste en pris, når de gennemser produktet på en PDP.

    ![Indtast prisfelt i Commerce Headquarters.](./media/KeyInPrice.png)
    
    I følgende eksempel vises en liste over digitale gavekortproduktvarianter i Commerce headquarters, herunder to brugerdefinerede prisvarianter.
    ![Digitale gavekortproduktvarianter med brugerdefineret prisvariant som eksempel](./media/DigitalGiftCards_ProductVariantsWithCustom.png)

- Leveringsmåden for et digitalt gavekort skal angives til **Elektronisk**. På siden **Leveringsmåder** (**Detail og handel \> Konfiguration af kanal \> Leveringsmåder**) skal du vælge tilstanden leveringsmåde **Elektronisk** i listeruden og derefter tilføje det digitale gavekortprodukt i gitteret i oversigtspanelet **Produkter**, som vist i følgende illustration. Du kan finde flere oplysninger i [Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitale gavekortprodukter på siden Leveringsmåde i Commerce Headquarters.](./media/ElectronicMode.PNG)
    
- Kontroller, at der er oprettet en onlinefunktionsprofil, som er tilknyttet din onlinebutik i Commerce Headquarters. I funktionalitetsprofilen skal du angive indstillingen **Aggreger produkter** til **Ja**. Denne indstilling sikrer, at alle varer undtagen gavekort aggregeres. Du kan finde flere oplysninger under [Oprette en onlinefunktionsprofil](online-functionality-profile.md).
- Hvis du vil sikre, at kunder modtager en e-mail, når et gavekort er faktureret, skal du oprette en ny mailbeskedtype på siden **Mailbeskedprofiler** og angive, at feltet **Mailbeskedtype** skal udstede **gavekort**. Du kan finde flere oplysninger i [Konfigurere en mailbeskedprofil](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Tilføje produktbilleder til Mediebiblioteket i Commerce-webstedsgenerator

Du skal føje produktbilleder for digitale gavekortprodukter til Mediebiblioteket i Commerce-webstedsgenerator. Kontrollér, at filnavnene på billedfilerne med gavekort følger webstedets navngivningskonventioner for produktbilleder. Du kan finde flere oplysninger under [Overfør billeder](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Konfigurere et brugerdefineret beløb for et digitalt gavekort i Commerce site builder

Hvis et digitalt gavekort er konfigureret til at tillade et brugerdefineret beløb, skal denne funktionalitet også aktiveres i [modulet Købsboks](add-buy-box.md), der bruges på webstedets PDP'er. Modulet Købsboks understøtter modulkonfiguration, så der kan tillades brugerdefinerede beløb. Du kan også definere de minimum- og maksimumbeløb, der er tilladt for brugerdefinerede beløb.

Konfigurer et brugerdefineret beløb for et digitalt gavekort i Commerce site builder ved at følge disse trin.

1. Gå til modulet Købsboks, der bruges på webstedets PDP'er. Dette købsboksmodul kan være implementeret i et modul, i en skabelon eller på en side.
1. Vælg **Rediger**.
1. Marker afkrydsningsfeltet **Tillad brugerdefineret pris** i egenskabsruden til højre.
1. Valgfrit: Hvis du vil definere minimum- og maksimumbeløb for brugerdefinerede beløb, skal du angive beløb under **Minimumspris** og **Maksimumpris**.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Boksmodul til køb](add-buy-box.md)

[Betalingsmodul](add-checkout-module.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Oprette et nyt produkt i Commerce](create-new-product-commerce.md)

[Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Produktdimensioner](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[Konfigurere en profil for mailbesked](email-notification-profiles.md)

[Oprette en onlinefunktionalitetsprofil](online-functionality-profile.md)

[Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
