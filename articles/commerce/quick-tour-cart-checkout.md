---
title: Oversigt over sider til indkøbsvogn og betaling ved kassen
description: Dette emne indeholder en oversigt over sider til indkøbsvogn og betaling ved kassen i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f7c708aa7f1a858e78cdbda809b90b944606022
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244785"
---
# <a name="cart-and-checkout-pages-overview"></a>Oversigt over sider til indkøbsvogn og betaling ved kassen

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over sider til indkøbsvogn og betaling ved kassen i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

På indkøbsvognssiden på et e-handels-websted vises alle de varer, som en kunde har lagt i indkøbsvognen. Siden med indkøbsvognen opbygges ved hjælp af indkøbsvognsmodulet. Indkøbsvognsmodulet er en container, der agerer vært for alle de moduler, der kræves for at fremvise varerne i indkøbsvognen. Modulet til indkøbsvognen kan også bruge andre moduler til at vise ordreoversigten og eventuelle kampagnekoder, der er anvendt på kundeordren.

Betalingssiden på et e-handels-websted indeholder en trinvis proces, som kunderne følger for at angive alle de oplysninger, der kræves for at afgive en ordre. Et betalingsmodul kan omfatte moduler, der håndterer leveringsadressen, leveringsmetoderne, faktureringsoplysningerne, ordreoversigten og andre oplysninger, der er relateret til kundeordrer.

## <a name="cart-page"></a>Siden med indkøbsvogn

Indkøbsvognens side fungerer som indkøbspose og indeholder alle de varer, der er lag i indkøbsvognen.

I følgende illustration vises et eksempel på en indkøbsvognside, der er oprettet ved hjælp af modulbiblioteket og temaet "Fabrikam".

![Eksempel på en indkøbsvognside](./media/cart2.PNG)

Hovedindholdet af indkøbsvognens side viser alle de varer, som kunden har lagt i indkøbsvognen. Alle relevante rabatter fremvises. Disse rabatter omfatter komplekse rabatter. Eksemplerne omfatter "Køb 3 varer, og få 10 % rabat" eller "Køb en flaske og en rygsæk, så du får 10 % rabat". Modulet Ordreoversigt viser det beløb, der skal betales efter fradrag af rabat, forsendelse, moms og andet, der er anvendt. Der findes også et kampagnekodemodul, hvor kunden kan anvende eller fjerne kampagnekoder.

En kunde kan købe anonymt eller som en bruger, der er logget på. Hvis en kunde er logget på, bevares varer i indkøbsvognen mellem sessioner. På denne måde kan kunden fortsætte med at handle fra flere enheder.

Fra indkøbsvognen kan kunden fortsætte til kassen. En kunde kan starte betaling som gæstebruger eller som en bruger, der er logget på.

Du kan finde oplysninger om, hvordan du opretter en indkøbsvognside, under [Føje et indkøbsvognmodul til en side](add-cart-module.md).

## <a name="checkout-page"></a>Siden Betaling ved kassen

Siden med betaling ved kassen er det sted, hvor kunderne angiver de oplysninger, der skal bruges til afgivelsen af ordren.

I følgende illustration vises et eksempel på en betalingsside, der er oprettet ved hjælp af modulbiblioteket.

![Eksempel på en betalingsside](./media/Checkout.PNG)

Hovedindholdet af betalingssiden er det sted, hvor alle ordreoplysningerne indsamles. Disse oplysninger omfatter leveringsadresse, leveringsindstillinger og betalingsoplysninger. Betalingen er en trinvis proces, da oplysningerne skal angives i en bestemt rækkefølge for at blive behandlet. Leveringsadressen skal f.eks. angives, før der kan beregnes forsendelsesomkostninger, og betalingen kan godkendes.

### <a name="shipping-address"></a>Leveringsadresse

Der skal angives en leveringsadresse, hvis der skal leveres varer. Formatet for forsendelsesadresser for hver landestandard kan konfigureres i Dynamics 365 Commerce. Hvis varerne f.eks. skal sendes til USA, skal leveringsadressen indeholde en gadeadresse, stat og postnummer. Der udføres grundlæggende validering af leveringsadresser, f.eks. validering af alfanumeriske tegn, maksimumlængde og tal. Selvom gyldigheden af selve adressen ikke bekræftes, kan denne kontrol udføres ved hjælp af tilpassede tredjepartstjenester.

Leveringsadressen anvendes på alle de varer i indkøbsvognen, som indstillingen "afsendelse" er valgt for. Hvis du bruger flowet for betaling, der findes i modulbiblioteket, kan individuelle varer i indkøbsvognen ikke leveres til forskellige adresser. Hvis du har brug for denne egenskab, kan den implementeres ved at tilpasse betalingsmodulerne.

Når leveringsadressen er angivet, vises de leveringsmetoder, der er tilgængelige fra Dynamics 365 Commerce-onlinebutikken. De leveringsmetoder og adresser, de understøtter, kan konfigureres i Commerce.

### <a name="payment"></a>Betaling

Det næste trin i kasseprocessen er betalingen. I e-handel kan flere betalingsmåder bruges til at afgive ordrer, f.eks. kreditkort, gavekort og fordelskundepoint. Der kan også bruges en kombination af disse betalingsmetoder. Afhængigt af de anvendte betalingsmetoder kan der være brug for flere oplysninger. En kreditkortbetaling kræver f.eks. en faktureringsadresse. Kreditkortbetalinger behandles ved hjælp af Adyen-betalingsconnectoren.

#### <a name="loyalty-points"></a>Fordelskundepoint

Under processen til betaling ved kassen kan en kunde, der er medlem af et fordelskundeprogram, og som har periodiserede fordelingskundepoint, indløse disse fordelskundepoint for en ordre. Modulet til kundefordelspoint vises kun, hvis kunden har et eksisterende fordelskundemedlemskab. Dette modul er skjult for ikke-medlemmer og gæstebrugere.

#### <a name="gift-cards"></a>Gavekort

Med modulbiblioteket kan interne gavekort indløses for en ordre. For at anvende et internt gavekort skal kunden være logget på. Af hensyn til øget sikkerhed anbefales det, at du tilpasser processen ved at bruge et personligt identifikationsnummer (PIN) til interne gavekort.

### <a name="signed-in-and-guest-users"></a>Brugere, der er logget på, og gæstebrugere

Kunden kan gennemføre betalingsprocessen som gæstebruger eller som en bruger, der er logget på. Hvis kunden logger på, hentes der automatisk kontooplysninger som f.eks. gemte leveringsadresser og gemte oplysninger om kreditkort.

### <a name="order-summary"></a>Ordreoversigt

Ved kassen vises en oversigt over linjevarerne i indkøbsvognen, så kunden kan bekræfte ordren, før den afgives. Linjevarerne kan ikke redigeres i betalingsprocessen. Men der findes et link til indkøbsvognen, hvis brugeren vil gå tilbage og redigere linjevarer.

Når kunden har angivet forsendelses- og faktureringsoplysninger, afspejler ordreoversigten det beløb, der skal betales, når fordelskundepoint, gavekort og andre betalinger er anvendt.

### <a name="order-confirmation-and-email"></a>Mail med ordrebekræftelse

Når kunden afgiver en ordre, udstedes et bekræftelsesnummer. På dette tidspunkt er betalingen godkendt, men ikke opkrævet. Betalingen opkræves kun, når ordren er opfyldt (dvs. når den enten er leveret eller afhentet).

Når en ordre er oprettet, sendes der en ordrebekræftelse via mail til kunden.

Du kan finde flere oplysninger om, hvordan du opretter en betalingsside, under [Føje et betalingsmodul til en side](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startside](quick-tour-home-page.md)

[Oversigt over sider med produktdetaljer](quick-tour-pdp.md)

[Oversigt over sider til kontostyring](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]