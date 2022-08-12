---
title: Konfigurere Google Pay med Adyen
description: I denne artikel beskrives det, hvordan du konfigurerer Google Pay med Adyen i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115025"
---
# <a name="configure-google-pay-with-adyen"></a>Konfigurere Google Pay med Adyen

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du konfigurerer Google Pay med Adyen i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce tilbyder integration uden for feltet for Google Pay, når Adyen- betalings-gateway-tjenesten bruges. Google Pay er en digital betalingsmåde, der bruger en Google Pay-forhandlerkonto, der fungerer som overensstemmelse med betalingstjenesten Adyen. Når den er konfigureret, er knappen Google Pay tilgængelig som en betalingsmåde, der kan vælges under betaling via onlineordre ved kassen. Når brugere vælger **Google Pay** i en understøttet browser eller enhed, bliver de afledt til at gennemføre deres betaling direkte med Google Pay-tjenesten. De returneres derefter til onlinebutikken for at fuldføre ordren.

Når Google Pay bruges med modulet til betaling ved kassen i Commerce, forudfyldes brugerens betalingskontooplysninger automatisk i formularen til betaling ved kassen for at hjælpe brugeren med at komme hurtigere igennem processen til betaling ved kassen. Commerce omfatter et betalings express-modul, der giver mulighed for betaling ved kassen. Ekspresbetalingsmodulet kan bruges i et fragment, som kan medtages på en side i kassen eller indkøbsvognen. Dynamics 365 Payment Connector til Google Pay-connector-referencen bruges ud over Dynamics 365 Payment Connector til Ayden til at aktivere både ekspresbetaling og de almindelige betalingsmuligheder med PayPal. Google Pay kan også konfigureres med Adyen-betalingsterminaler og POS (Commerce POS) til brug i butikken.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Google Pay | Kaldes også for Google Pay-"knappen", og Google Pay er et betalingstilbud, der understøttes via Adyen-connector. Det aktiverer kundeoplevelse og integration, der understøttes af Dynamics Google Pay-connectoren. |
| Tegnebog | En betalingstype, der ikke omfatter de traditionelle betalingskarakteristika som f.eks. BIN-området (Bank Identification Number) og udløbsdatoen, som bruges til at skelne mellem kredit- og debetkorttyper. |
| Ekspresbetalingsmodul | Et Dynamics 365 Commerce-modul, der understøtter en hurtigere betaling ved kassen, når der bruges understøttede betalingsmåder. |

## <a name="prerequisites"></a>Forudsætninger

Hvis du Google Pay med Adyen i Commerce, kræver det en Google Merchant-konto. Yderligere oplysninger om, hvordan du konfigurerer din Google Merchant-konto, finder du i [dokumentationen til Google Pay](https://docs.adyen.com/payment-methods/google-pay/) og Googles [integrerede kontrolliste](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Google Pay-metoden skal også integreres med din Adyen-konto. Oplysninger om integrationslinks finder du i [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Du skal også aktivere den udvidede kontantbetalingsfunktion i Dynamics 365 Commerce headquarters. Gå til **Arbejdsområder \> Funktionsstyring**, søg efter funktionen **Udvidet understøttelse til kontantbetaling og betalingsforbedringer**, vælg funktionen og vælg funktionen, og vælg derefter **Aktivér**. Når funktionen er aktiveret, skal du køre **1110**-fordelingsplanen for at gøre ændringen tilgængelig i alle kanaler.

## <a name="map-the-google-pay-payment-method"></a>Tilknytte Google Pay-betalingsmetoden

Google Pay er en digital betalingsmåde. Du kan finde flere oplysninger om, hvordan du konfigurerer betalingstilknytning for Google Pay, i [Betalingssupport til kontantbetaling](../wallets.md).

Benyt følgende fremgangsmåde for at tilknytte Google Pay til betalingsmiddel for både kasse og onlinekanaler.

1. I Commerce Headquarters til **Detail og Commerce \> Konfiguration af kanal \> Betalingsmetoder \> Korttyper**.
1. Vælg **Ny** for at tilføje en linje til Google Pay.
1. Angiv **Id** i feltet **Google Pay**.
1. Vælg **Google Pay** i feltet **Elektronisk betalingsnavn**.
1. I feltet **Type** skal du angive **Kontant**.
1. Angiv **Udsteder** i feltet **Google**.
1. Vælg **Processortilknytning** i handlingsruden for at åbne dialogboksen **Tilknytning af processorbetalingsmåder**.
1. Under **Betalingsmetoder for ikke-tilknyttede processorer** vises en liste over betalingsmetoder for ikke-tilknyttede processorer, som hver især er parret med den relevante connector. Hvis du vil fjerne tilknytning af Google Pay-betalingsmiddelbetalingsmetoder til betalingsmiddeltyper med kort, skal du følge disse trin for hver kortudbydertype:

    1. Vælg **Kortbetalingsmiddeltype** under Kortbudstyper.
    1. I kolonnen **Ikke tilknyttede processorbetalingsmetoder** skal du vælge både **Dynamics 365 Payment Connector for Adyen**-connector (til brug ved POS) og **Dynamics 365 Payment Connector for Google Pay**-connector (til brug i onlinekanaler).
    1. Vælg **Tilføj**. Markeringerne føjes til kolonnen **Tilknyttede betalingsmåder for processorer**.

1. Når du har gjort det, skal du tilknytte betalingsmetoder, vælge **Gem**.
1. Vælg **Gem** på siden **Korttyper**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Konfigurere en Commerce online butik for Google Pay

Hvis du vil konfigurere en Commerce online butik til at bruge google Pay, skal du følge disse trin.

1. Gå til **Detail og Commerce \> Kanaler \> Online-butikker** i Commerce headquarters.
1. Vælg den onlinebutikskanal, der er knyttet til dit websted, ved at vælge værdien for **Detailkanal-id**.
1. I oversigtspanelet **Betalingskonti** under **Connector** skal du bekræfte, at **Dynamics 365 Payment Connector for Adyen**-connector vises. Hvis den ikke er vist, skal du følge instruktionerne i [Opsætning af Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md) for at tilføje den.

    > [!NOTE]
    > I de fleste tilfælde skal **Dynamics 365 Payment Connector for Adyen**-connector være angivet som det første connector til kanalen (den første connector kaldes også det primære connector). Den skal derefter efterfølges af andre connectorer, der vil blive brugt, f.eks. **Dynamics 365 Payment Connector til PayPal** og **Dynamics 365 Payment Connector for GooglePay**-connectorer.

1. Når **Dynamics 365 Payment Connector for Adyen**-connector er blevet tilføjet, skal du vælge **Tilføj** for at tilføje **Dynamics 365 Payment Connector for Google Pay**-connector. Angiv derefter følgende egenskaber for connectoren.

    | Felt                  | Beskrivende tekst | Obligatorisk | Indstil automatisk | Eksempelværdi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Navn på assembly          | Navnet på assemblyen for Dynamics 365 Payment Connector til Google Pay. | Ja | Ja | *Binært navn* |
    | Tjenestekonto-id     | Det entydige id for opsætningen af de handlendes egenskaber. Dette id påstemples på betalingstransaktioner og identificerer de handlendes egenskaber, som downstream-processer (som f.eks. fakturering) skal bruge. | Ja | Ja | *GUID* |
    | Google-forhandler-id     | Angiv det Google Merchant-id, der er tildelt din Google Merchant-konto. Denne egenskab kræves i produktionsmiljøer, men er valgfri i testmiljøer. Yderligere oplysninger finder du i <https://pay.google.com/>. | Ja | Nej | *Numerisk id* |
    | Handlendes konto-id    | Indtast et entydigt Adyen forhandler-id Denne værdi kan du få, når du tilmelder dig Adyen som beskrevet i [Tilmelding til Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nej | *Forhandler-id* |
    | API-nøgle til skyen          | Angiv Adyen API-nøgle til skyen. Du kan hente denne nøgle ved at følge instruktionerne i [Sådan henter du API-nøglen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ja | Nej | "abcdefg" |
    | Gatewaymiljø    | Det Adyen gateway-miljø, der skal knyttes til. Mulige værdier er **Test** og **Live**. Du skal kun indstille dette felt til **Live** for produktionsenheder og transaktioner. | Ja | Ja | "Live" |
    | Understøttede valutaer   | De valutaer, som connectoren skal behandle. I scenarier, der indeholder kort, kan Adyen understøtte yderligere valutaer via [Dynamisk valutaomregning](https://www.adyen.com/pos-payments/dynamic-currency-conversion), efter at transaktionsanmodningen er sendt til betalingsterminalen. Kontakt Adyen for at få en liste over understøttede valutaer. | Ja | Ja | "USD;EUR" |
    | Understøttede betalingsmiddeltyper | De valutaer, som connectoren skal behandle. | Ja | Ja | "GooglePay" |

1. Når du er færdig med at angive connector-egenskaberne, skal du køre **1070 (kanal-konfiguration**) distributionsplanlægningsjob.

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigurer Google Pay for Commerce POS.

POS-konfigurationen bruger indstillingen i hardwareprofilens **EFT-servicefelt** til Dynamics 365 Payment Connector for Adyen. Du kan finde oplysninger om, hvordan du konfigurerer den elektroniske pengeoverførselstjeneste (EFT) til Dynamics 365 Payment Connector for Adyen i Commerce Headquarters, i [Afsnittet Konfigurere en Dynamics 365 POS-hardwareprofil](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Processortilknytningen for Adyen-connector registrerer de kontantkorttyper, som Google Pay bruger på POS-terminalen.

### <a name="use-the-payment-express-module-with-google-pay"></a>Brug betalingsekspresmodul med Google Pay

Commerce-ekspresbetalingsmodulet fungerer sammen med understøttende betalingsmåder for at give netkunder mulighed for at betale hurtigere ved at forhåndsudfylde deres betalingstjenestekontooplysninger under betalingsprocessen. Ekspresbetalingsmodulet bruger den konfigurerede betalings-connectorknap og returnerer brugervalgte ordreoplysninger (adresse, kontaktoplysninger og betalingsmetode) til at forhåndsudfylde formularen til betaling ved kassen.

Når modulet til ekspresbetalings bruges sammen med Google Pay, åbnes vinduet Google Pay-knap i sektionen **Ekspresbetaling** i google Pay iframe-vinduet. Brugere kan derefter logge på sin Google-konto for at bruge kontoens leveringsadresse, faktureringsadresse, mailadresse og den valgte Google Pay-betalingsmetode til at betale for transaktionen.

Når brugerne har fuldført handlingen i Google Pay-vinduet, dirigeres de tilbage til Commerce-siden til betaling ved kassen på webstedet, hvor formularen til betaling med deres Google Pay-kontooplysninger. Når brugerne vender tilbage til siden til betaling ved kassen fra Google Pay-vinduet, får de vist følgende oplysninger:

- I ekspresbetalingsflowet er den første leveringsmulighed, der er tilgængelig for den leveringsadresse, der returneres, forhåndsudfyldt for kunden.
- Når Google Pay bruges, returneres der ingen e-mail-adresse til kontaktpersoner. Brugere, der checker ud, skal angive en e-mail-adresse i kontaktsektionen på siden til betaling ved kassen. Brugere, der er logget på, får automatisk deres kontaktdata udfyldt fra deres Dynamics-kundekonto (den primære e-mail-adresse, de har brugt til godkendelse).

Brugeren har derefter mulighed for at gennemse ordren og ændre betalingsoplysningerne ved kassen, før brugeren vælger **Afgiv ordre** for at færdiggøre ordren.

### <a name="configure-google-pay-in-site-builder"></a>Konfigurere Google Pay i site builder 

Før du konfigurerer dine fragmenter eller sider med Google Pay, skal du sikre dig, at sikkerhedspolitikkerne for indhold for dit websted er angivet i Commerce-webstedsgenerator.

Benyt følgende fremgangsmåde for at sikre, at sikkerhedspolitikkerne for indhold er angivet i Site Builder.

1. Gå til **Webstedsindstillinger \> Udvidelser** på webstedet.
1. På fanen **Sikkerhedspolitik for indhold** tilføjes in line for `*.google.com` til vejledningerne **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** og **style-src**.
1. Vælg **Gem og publicér alle**, når du er færdig.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigurere payment express-fragmenter med Google Pay i webstedsgenerator

Benyt følgende fremgangsmåde for at konfigurere betalingsekspresfragmentet med Google Pay til onlinebutikken.

1. Naviger til **Fragmenter** i webstedsgeneratoren.
1. Vælg **Ny**.
1. I dialogboksen **Nyt fragment** skal du vælge modulet **Container**, angive et navn for fragmentet (f.eks. **Ekspresbetaling**) og derefter vælge **OK**. 
1. Vælg det nye fragments **Standardcontainerplads**.
1. Angiv egenskaber for containermodulet i ruden Egenskaber til højre.

    - **Overskrift** – Angiv en overskrift, der skal vises i sektionen til betaling ved express-betaling på dit websted (f.eks. **Ekspresbetaling**).
    - **Containerlayout** – Vælg **Flow**.
    - **Bredde** – Vælg **Udfyld container**.
    - **Underordnede vist** – Vælg **Tre** for at angive det antal underordnede, der skal være i en række af sektionen til ekspresbetaling på siden til betaling ved kassen (f.eks. et tekstfelt, ekspresbetaling til PayPal, og ekspresbetaling til Google Pay).
    - **CSS-klassenavn** – Angiv **msc-express-payment-container** (påkrævet).

    > [!IMPORTANT]
    > - Værdien **CSS-klassenavn** skal angives til **msc-express-payment-container** for at styre funktionaliteten af containeren under betaling ved kassen. Denne funktionsmåde omfatter at skjule, sammenfolde og andre handlinger, der gælder for afsnittet om ekspresbetaling under betalingsflowet ved kassen. Klassen **msc-express-payment-container** fungerer sammen med de standardoperationer, der frigives med modulet til betaling af modulbiblioteket.
    > - Yderligere typografier kan medtages i forhold til **CSS-klassenavn**. Hvis du tilpasser funktionaliteten af modulet, skal du krydskontrollere typografien, hvis du bruger samme modulbibliotekskodefunktion i modulet til betaling ved kassen for funktionaliteten ved hurtig betaling.

1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Ekspresbetaling** og derefter **OK**.
1. I egenskabsruden **Ekspresbetailing** skal du indstille eller justere værdien for **Højde på iFrame** i pixels (f.eks. **60**).
1. I feltet **Understøttede betalingsmiddeltyper** skal du angive **GooglePay**. Værdien skal svare til strengen **Understøttede betalingsmiddeltyper** i den connector, der er konfigureret til kanalen (som beskrevet i afsnittet [Konfigurere en Commerce onlinebutik for Google Pay](#configure-a-commerce-online-store-for-google-pay) i denne artikel).

    > [!NOTE]
    > Du kan gentage trin 6 til 9 for at tilføje **Ekspresbetaling**-moduler til andre betalingsmåder. Juster værdien af de **Understøttede betalingsmiddeltyper** med de yderligere konfigurerede betalingstyper (f.eks. **Paypal**).

1. Valgfrit: Du kan føje et tekstblokmodul til standardcontainermodulet for at medtage instruktioner eller oplysninger om offentliggørelse. Når du har tilføjet modulet, skal du angive den ønskede tekst i feltet **RTF**. Du kan placere teksten over eller under ekspresbetalingsmoduler ved at vælge ellipsen (**...**) i **Tekstblok** og derefter vælge **Flyt op** eller **Flyt ned**.
1. Vælg **Gem** for at gemme finde ændringer, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere fragmentet.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Føje betalingsekspresfragmentet til siden for betaling ved kassen

Udfør følgende trin for at tilføje betalingsekspresfragmentet til siden for betaling ved kassen.

1. Vælg **Sider** i webstedsgenerator, og vælg derefter siden til betaling ved kassen på dit websted.
1. Vælg **Rediger**.
1. På pladsen **Hoved** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. Angiv egenskaber for containermodulet i ruden Egenskaber til højre.

    - **Containerlayout** – Vælg **Stablet**.
    - **Bredde** – Vælg **Udfyld container**.
    - **Underordnede vist** – Vælg **Tre** for at angive det antal underordnede, der skal være i en række af sektionen til ekspresbetaling på siden til betaling ved kassen (f.eks. et tekstfelt, ekspresbetaling til PayPal, og ekspresbetaling til Google Pay).

1. På modulpladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj fragment**.
1. I dialogboksen **Vælg et fragment** skal du vælge det ekspresbetalingsfragment, som du har oprettet, og derefter vælge **OK**.
1. Vælg **Gem** for at gemme finde ændringer, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere siden.

> [!NOTE]
> Hvis siden til betaling ved kassen allerede indeholder en container, der har udtjekning, og du ønsker, at modulet til ekspresbetaling skal gengives over den almindelige betalingscontainer, kan du placere den over eller under den eksisterende udtjekningsbetaling ved at vælge ellipsen (**...**) i **Hoved** og derefter vælge **Flyt op** eller **Flyt ned**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Føje betalingsekspresfragmentet til indkøbskurvens side

Udfør følgende trin for at tilføje betalingsekspresfragmentet til siden for betaling ved kassen.

1. Vælg **Sider** i webstedsgenerator, og vælg derefter siden til indkøbsvognen på dit websted.
2. Vælg **Rediger**.
3. I dispositionsvisningen kan du udvide **Hoved** i trævisningen og finde den container, der indeholder modulet **Indkøbsvogn**.
4. I modulet **Indkøbsvogn** skal du vælge **Ekspresbetaling**, vælge ellipsen (**...**) og derefter vælge **Tilføj modul**.
5. I dialogboksen **Vælg moduler** skal du vælge modulet **Ekspresbetaling** og derefter **OK**.
6. Vælg modulet **Ekspresbetaling**. I egenskabsruden til højre kan du derefter angive **GooglePay** under **Understøttede betalingsmiddeltyper**. Værdien skal svare til strengen **Understøttede betalingsmiddeltyper** i den connector, der er konfigureret til kanalen (som beskrevet i afsnittet [Konfigurere en Commerce onlinebutik for Google Pay](#configure-a-commerce-online-store-for-google-pay) i denne artikel).
1. Vælg **Gem** for at gemme finde ændringer, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere siden.

Brugere kan medtage op til tre understøttede **Ekspresbetalingsmoduler** (med andre ord tre tilgængelige understøttede betalingsindstillinger) i **Ekspresbetaling** til indkøbsvognen.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Opsætning af Google Pay som en mulighed i betalingssektionen til betaling ved kassen

Du kan konfigurere Google Pay som en mulighed i betalingssektionen til betaling ved kassen, hvis det kun er betalingsfunktionen, der ikke er ekspres. Formen til betaling ved kassen udfyldes af brugeren, og betalingssiden til Google Pay vil kun være klar til betaling af Google Pay. Der bruges ingen Google Pay-kontooplysninger til at overskrive de udfyldte oplysninger om check ud.

> [!NOTE]
> I følgende procedure antages det, at dit websted bruger et fragtfragment til betaling ved kassen, som er konfigureret med afhentningsoplysninger, en leveringsadresse, leveringsindstillinger, kontaktoplysninger, valgfrie vilkår og betingelser samt et område til elementer i forbindelse med udtjekning. Standardmodulmodulet til betaling ved kassen frigives med en container til udtjekning, som har tekstblok, fordelskundepoint, gavekort og betalingsmoduler. Du kan få flere oplysninger i [Betalingsmodul](../payment-module.md).

Hvis du vil konfigurere Google Pay som en almindelig betalingsmåde i afsnittet **Betalingsmåde** på kassens side, skal du følge disse trin.

1. Vælg **Fragmenter** i webstedsgenerator, og vælg derefter fragmentet til betaling ved kassen på dit websted.
1. Vælg **Rediger**.
1. På pladsen **Betalingsoplysninger** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Betaling** og derefter **OK**.
1. Angiv egenskaber for containermodulet i egenskabsruden til højre **Betaling**.

    - **Overskrift** – Angiv en overskrift, der skal vises i sektionen til betaling ved ekspresbetaling på dit websted (f.eks. **Google Pay**).
    - **Højde for iFrame** - Rediger værdien til din foretrukne designhøjde i pixel (f.eks. **75**). 
    - **Understøttede betalingsmiddeltyper** – Angiv **Beløb**, der svarer til konfigurationen af Google Pay-connector i Commerce Headquarters.
    - **Er primær betaling** – Lad afkrydsningsfeltet være ryddet. (Denne egenskab er typisk aktiveret for Adyen-modulet til betaling ved kassen)
    - **Tilsidesæt betalingstype** – Denne egenskab er ikke understøttet til konfigurationen af Google Pay.
    - **Brug connector-id** – Denne egenskab skal vælges, hvis der bruges flere betalings-connectorer på siden.

1. Du kan placere modulet over eller under andre betalingsmoduler ved at vælge ellipsen (**...**) i **Betaling** og derefter vælge **Flyt op** eller **Flyt ned**.
1. Vælg **Gem** for at gemme finde ændringer, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

### <a name="modes-of-delivery"></a>Leveringsmåder

Når modulet Ekspresbetaling konfigureret til at bruge Google Pay, udfyldes den første leveringsmulighed, der returneres for den leveringsadresse, der blev valgt til Google Pay-kontoen, på forhånd. Brugerne har mulighed for at justere leveringsadressen til en anden indstilling, hvis det er nødvendigt.

Den rækkefølge, leveringsmetoderne vises i modulet Ekspresbetaling, er konfigureret på kanalens side med **leveringsmåder** i Commerce Headquarters. Gå til **Detail og Commerce \> Kanaler \> Onlinebutikker**, og vælg **Detail-kanal-id**-værdien for din butik i Commerce headquarters. I handlingsruden skal du på fanen **Opsætning** vælge **Leveringsmåder**. De angivne leveringsmåder vises i samme rækkefølge i modulet Payment Express. Hvis du vil tilføje eller fjerne leveringsmåder for en detailkanal eller et produkt, skal du vælge **Administrer leveringsmåder** i handlingsruden. Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden, under [Konfigurere leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

I modulet til betaling ved kassen bruges også modulet til leveringsindstillinger, når leveringsmåder gengives under betaling ved kassen. Der er flere oplysninger i [Leveringsindstillingsmodul](../delivery-options-module.md).

Leveringsmåder vises, når de føjes til listen **Leveringsmåder** i onlinebutikken.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](payments-retail.md)

[Betalingsmodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
