---
title: Oprette Commerce-kataloger til B2B-websteder
description: Denne artikel indeholder en beskrivelse af, hvordan du kan oprette handelskataloger for Microsoft Dynamics 365 Commerce business-to-business (B2B)-websteder.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 2cc9014d273b4ab6f23a38140d0cfcd3ffa4d630
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027026"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Oprette Commerce-kataloger til B2B-websteder

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan oprette Commerce-produktkataloger for Microsoft Dynamics 365 Commerce business-to-business (B2B)-websteder. Du kan finde svar på ofte stillede spørgsmål om Commerce-kataloger til B2B-websteder i [Commerce-kataloger til B2B Ofte stillede spørgsmål](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Denne artikel gælder for Dynamics 365 Commerce version 10.0.27 og senere.

Du kan bruge Commerce-kataloger til at identificere de produkter, du vil tilbyde i dine B2B-onlinebutikker. Når du opretter et katalog, skal du identificere de onlinebutikker, produkterne skal tilbydes i, tilføje de produkter, der skal medtages og forbedre produkttilbuddene ved at tilføje oplysninger. Du kan oprette flere kataloger til hver B2B-onlinebutik.

Commerce-produktkataloger giver dig mulighed for at definere følgende oplysninger:

- **Katalogspecifikt navigationshierarki** – Organisationer kan oprette en specifik kategoristruktur til deres specifikke katalog.
- **Katalogspecifikke attributmetadata** – Attributter indeholder oplysninger om et produkt. Ved at tildele en kategori i navigationshierarkiet attributter kan du definere værdier for disse attributter på produktniveau, der er tildelt den pågældende kategori. Organisationer kan derefter fuldføre disse opgaver:

    - Definer katalogspecifikke attributværdier.
    - Kontroller synligheden af attributter på katalogniveau.
    - Vælg de afgrænsningerne, der er specifikke for det enkelte katalog.

- **Kanaler** – Organisationer kan tilknytte mere end én B2B-onlinekanal til et katalog. Slut til slut-understøttelse af kataloger er i øjeblikket kun tilgængelig for B2B-onlinebutikker.
- **Debitorhierarkier** – For en bestemt B2B-kanal kan organisationer gøre et specifikt katalog tilgængeligt for udvalgte B2B-partnere ved at knytte debitorhierarkier til kataloget.
- **Prisgrupper** – Du kan konfigurere priser og kampagner, der er specifikke for et bestemt katalog. Denne egenskab er en kerneårsagen til definition af et katalog til en B2B-kanal. Prisgrupper for kataloger sætter organisationer i stand til at gøre produkter tilgængelige for deres ønskede B2B-organisationer og anvende deres foretrukne priser og rabatter. B2B-kunder, der bestiller fra et konfigureret katalog, kan med fordel modtage særlige priser og kampagner, efter at de har logget på et commerce B2B-websted. Du kan konfigurere specifikke priser for kataloget ved at vælge indstillingen **Prisgrupper** under fanen **Kataloger** for at knytte en eller flere prisgrupper til kataloget. Alle handelsaftaler, prisjusteringskladder og særlige rabatter (tærskel, antal, mix og match), der er blevet knyttet til den samme prisgruppe, anvendes, når kunder bestiller fra dette katalog. (Særlige rabatter omfatter grænseværdi, antal og mix og match-rabatter). Yderligere oplysninger om prisgrupper finder du i [Prisgrupper](price-management.md#price-groups).

> [!NOTE]
> Denne funktion er tilgængelig pr. Dynamics 365 Commerce-version 10.0.27-udgaven. Hvis du vil konfigurere katalogspecifikke konfigurationer, f.eks. navigationshierarkiet og kundehierarkiet, skal du åbne arbejdsområdet til **funktionsstyring** (**Systemadministration \> Arbejdsområder \> Funktionsstyring**), aktivere **brug af flere kataloger på funktionen for detailkanaler** og derefter køre **1110 CDX**-jobbet.

## <a name="catalog-process-flow"></a>Katalogprocesflow

Processen til oprettelse og behandling af et katalog har fire generelle trin. De enkelte trin forklares detaljeret i næste afsnit.

1. **[Konfiguration](#configure-the-catalog)**

    - Tilknytte navigationshierarki.
    - Angiv ikrafttrædelses- og udløbsdato for tid, hvis de er gældende.
    - Tilføje og kategorisere produkter.
    - Tilknytte prisgrupper.
    - Tilknyt et kundehierarki, der er specifikt for B2B-organisationerne. 
    - Tilknyt standarddimensionsattributgruppe til afgrænsninger, f.eks. størrelse, typografi og farve.
    - Angiv attributmetadata.

1. **[Validering](#validate-the-catalog)** – I dette trin kører du valideringsregler, der gennemtvinger en bestemt funktionsmåde. Her er nogle eksempler:

    - Sørg for, at der ikke er nogen ikke-kategoriserede produkter.
    - Kontroller, at alle de varer, der er sorteret efter hver kanal, er tilknyttet et katalog.

1. **[Godkendelse](#approve-the-catalog)**
1. **[Publicering](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Konfigurere kataloget

Du kan bruge oplysningerne i dette afsnit til at oprette kataloget.

### <a name="configure-the-catalog"></a>Konfigurere kataloget

I Commerce headquarters skal du gå til **Detail og handel \>Kataloger og sortimenter \> Alle kataloger** for at konfigurere dit katalog.

Når du opretter et nyt katalog, skal du først knytte kataloget til en eller flere kanaler. Kun varer, der er knyttet til den valgte kanals [udvalg](/dynamics365/unified-operations/retail/assortments) kan bruges, når du opretter kataloget. Hvis du vil knytte kataloget til en eller flere kanaler, skal du vælge **Tilføj** i oversigtspanelet **Handelskanaler** på **katalogopsætningssiden**.

#### <a name="associate-the-navigation-hierarchy"></a>Tilknytte navigationshierarki

Hvis du vil føje produkter til et katalog, skal du vælge et navigationshierarki. Navigationshierarkiet understøtter kategoristrukturen for kataloget. Du skal vælge et af de navigationshierarkier, der er knyttet til kanaler, der er valgt i oversigtspanelet **Commerce-kanaler** på siden **Katalogopsætning**. Hvis du vil knytte et standardnavigationshierarki til hver af dine kanaler, skal du gå til **Detail og handel \> Kanalopsætning \> Kanalkategorier og produktattributter**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Angiv ikrafttrædelses- og udløbsdatoer

Hvis du vil angive ikrafttrædelses- og udløbsdatoer for et katalog, skal du vælge kataloghierarkiets topnode for at vende tilbage til hovedkatalogets overskriftsvisning. Konfigurer ikrafttrædelses- og slutdatoer efter behov i oversigtspanelet **Generelt**.

#### <a name="add-and-categorize-products"></a>Tilføje og kategorisere produkter

I Commerce headquarters skal du gå til **Detail og handel \> Kataloger og sortimenter \> Alle kataloger** for at konfigurere produkter til at tilføje til kataloget. Vælg derefter **Tilføj produkter** under fanen **Kataloger**.

Du kan også vælge en node i navigationshierarkiet. Derefter kan du føje produkter direkte til en kategori i kataloget.

#### <a name="associate-price-groups"></a>Tilknytte prisgrupper

Hvis du vil konfigurere katalogspecifikke priser, skal du knytte en eller flere prisgrupper til kataloget. I Commerce headquarters skal du gå til **Detail og handel \> Kataloger og sortimenter \> Alle kataloger** for at tilknytte prisgrupper til et katalog. Vælg derefter **Prisgrupper** under **Pris** under fanen **Kataloger**. Alle handelsaftaler, prisjusteringskladder og særlige detailrabatter (tærskel, antal, mix og match), der er blevet knyttet til den samme prisgruppe, anvendes, når kunder bestiller fra dette katalog.

Du kan finde flere oplysninger om prisgrupper i [Prisgrupper](price-management.md#price-groups).

> [!NOTE]
> Du kan ikke oprette en ny prisgruppe fra siden **Alle kataloger**. Du skal i stedet oprette den fra siden **Alle prisgrupper**. Du skal derefter knytte det til kataloget på siden **Alle kataloger**.

#### <a name="associate-a-customer-hierarchy"></a>Tilknyt et debitorhierarki

I Commerce headquarters skal du gå til **Detail og handel \>Kataloger og sortimenter \> Alle kataloger** for at konfigurere dit katalog. Under kundehierarkiet under fanen **Kataloger** skal du derefter vælge **Tildel hierarkier** under **Kundehierarki** for at knytte en eller flere debitorhierarkier til kataloget.

> [!NOTE]
> Du kan ikke oprette et nyt kundehierarki fra siden **Alle kataloger**. Du skal i stedet oprette den fra siden **Kundehierarkier**. Du skal derefter knytte det til kataloget på siden **Alle kataloger**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Tilknyt standarddimensionsattributgruppe til afgrænsninger, f.eks. størrelse, typografi og farve

Hvis du vil knytte en standarddimensionsattributgruppe til sortimenter, f.eks. størrelse, typografi og farve, skal du gå til Kataloger for **Detail og handel \> Kataloger og sortimenter \> Alle kataloger** i Commerce Headquarters. Vælg derefter **Attributgrupper** under **Attributter** under fanen **Kataloger**.

#### <a name="set-attribute-metadata"></a>Angiv attributmetadata

I Commerce headquarters skal du gå til **Detail og handel \>Kataloger og sortimenter \> Alle kataloger** for at konfigurere attributmetadata. Vælg derefter **Indstil attributmetadata** under **Attributter** under fanen **Kataloger**. Vælg en kategori i det tilknyttede katalogspecifikke navigationshierarki, og vælg derefter en attribut under **Katalogproduktattributter**, hvis du vil vælge de attributter, der skal kunne vises og kan vælges. Vælg derefter **Vis attribut på kanal**. Som standard kan der også søges i alle attributter, der kan vises. Du kan vælge at gøre attributter foruddefinerede ved at vælge **Kan være forskellige**.

### <a name="validate-the-catalog"></a>Validere kataloget

Før et nyt katalog er tilgængeligt for brug, skal det valideres og udgives.

Følg disse trin for at validere et katalog.

1. Vælg **Valider katalog** under **Valider** under fanen **Kataloger** på siden **Alle kataloger** for at køre en validering. Dette trin er påkrævet. Det validerer, at den nødvendige konfiguration er korrekt.
1. Vælg **Vis resultater** for at få vist detaljerne om valideringen. Hvis der findes fejl, skal du rette dataene og køre valideringen igen, indtil valideringen er godkendt.

### <a name="approve-the-catalog"></a>Godkend kataloget

Når et katalog er valideret, skal det godkendes.

Udfør følgende trin for at starte processen til kataloggodkendelse.

1. Vælg derefter siden **Alle kataloger**, vælg **Arbejdsproces \> Send**.
1. Konfigurer trinnene og de godkendte brugere for arbejdsprocessen i **Detail og handel \> Konfiguration af Headquarters \> Commerce-arbejdsproces**. Arbejdsgangen definerer de trin, der er nødvendige for at få vist kataloget med status **Godkendt**.

### <a name="publish-the-catalog"></a>Udgiv kataloget

Når et katalog har status **Godkendt**, kan du udgive det ved at vælge **Udgiv** i **menuen** Kataloger. Når kataloget har status **Udgivet**, kan det bruges i call center-ordreindtastning og katalogafsendelsesprocesser. Du kan udgive et katalog manuelt eller ved hjælp af en batchproces. Den ikrafttrædelsesdato, du har defineret for kataloget, bestemmer, hvornår produkterne er tilgængelige i onlinebutikken. Den udløbsdato, du har defineret, bestemmer, hvornår produkterne fjernes fra onlinebutikken.

> [!NOTE]
> Du kan udgive et katalog, der indeholder produkter med advarsler. Produkterne vises dog ikke i onlinebutikken.

## <a name="additional-resources"></a>Yderligere ressourcer

[Udvidet virkning af Commerce-kataloger til B2B-tilpasninger](catalogs-b2b-sites-dev.md)

[Handelskataloger for B2B Ofte stillede spørgsmål](catalogs-b2b-sites-FAQ.md)
