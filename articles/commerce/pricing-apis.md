---
title: API'er til Commerce-prissætning
description: Denne artikel beskriver forskellige API'er til prissætning, der leveres af Microsoft Dynamics 365 Commerce-prissætningsprogrammet.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294109"
---
# <a name="commerce-pricing-apis"></a>API'er til Commerce-prissætning

[!include [banner](../includes/banner.md)]

Denne artikel beskriver forskellige API'er til prissætning, der leveres af Microsoft Dynamics 365 Commerce-prissætningsprogrammet.

Prissætningsprogrammet Dynamics 365 Commerce indeholder følgende Retail Server-API'er, der kan forbruges af eksterne programmer for at understøtte forskellige prissætningsscenarier:

- **GetActivePrices** – Denne API henter et produkts beregnede pris, herunder simple rabatter.
- **CalculateSalesDocument** – Denne API beregner priser og rabatter for produkter i et bestemt antal, hvis de købes sammen.
- **GetAvailablePromotions – Denne API får gældende rabatter på produkter i indkøbsvognen**. 
- **AddCoupons** – Denne API føjer kuponer til en indkøbsvogn.
- **RemoveCoupons** – Denne API fjerner kuponer fra en indkøbsvogn.

Du kan finde flere oplysninger om, hvordan du forbruger Retail Server-API'er i eksterne programmer, i [Bruge Retail Server-API'er i eksterne programmer](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

API'en *GetActivePrices* blev introduceret i Commerce version 10.0.4. Denne API henter et produkts beregnede pris, herunder simple rabatter. Der beregnes ikke samkøbsrabatter, og det antages, at hvert produkt i en API-anmodning har et antal på 1. Denne API kan også tage en liste over produkter som input og forespørge på prisen på de enkelte produkter i store mængder.

API'en *GetActivePrices* understøtter rollerne **Medarbejder**, **Kunde**, **Anonym** og **Program** i Commerce.

Hovedanvendelsen af API'en *GetActivePrices* er siden med produktdetaljer (PDP), hvor detailhandlere viser den bedste pris for et produkt, herunder eventuelle gældende rabatter.

I følgende tabel vises inputparametrene for API'en *GetActivePrices*.

| Navn                                    | Undernavn | Type | Obligatorisk/valgfri | Beskrivende tekst |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Obligatorisk | |
|                                         | ChannelId | langt format | Obligatorisk | |
|                                         | CatalogId | langt format | Obligatorisk | |
| productIds                              | | IEnumerable\<long\> | Obligatorisk | Listen over produkter, der skal beregnes priser for. |
| activeDate                              | | DateTimeOffset | Obligatorisk | Den dato, hvor priserne beregnes. |
| customerId                              | | streng | Valgfri | Debitors kontonummer. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Valgfri | Niveau for tilknytning og fordelskunde. |
|                                         | AffiliationId | langt format | Obligatorisk | Tilknytnings-id. |
|                                         | LoyaltyTierId | langt format | Valgfri | Fordelskundeniveau-id. |
| includeSimpleDiscountsInContextualPrice | | bool | Valgfri | Angiv denne parameter til **sand**, så den medtager simple rabatter i prisberegningen. Standardværdien er **falsk**. |
| includeVariantPriceRange                | | bool | Valgfri | Angiv denne parameter til **sand** for at få minimum- og maksimumpriser blandt alle varianter af et masterprodukt. Standardværdien er **falsk**. |
| includeAttainablePricesAndDiscounts     | | bool | Valgfri | Angiv denne parameter til **sand** for at få opnåelige priser og rabatter. Standardværdien er **falsk**. |

**Eksempel på anmodningstekst**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Eksempel på svartekst**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

API'en *CalculateSalesDocument* blev introduceret i Commerce version 10.0.25. Denne API beregner priser og rabatter for produkter i et bestemt antal, hvis de købes sammen i en ordre. Prisberegningen bag API'en *CalculateSalesDocument* tager højde for både rabat på enkelte linjer og samkøbsrabatter.

Hovedanvendelsen af API'en *CalculateSalesDocument* er prisberegningen i scenarier, hvor hele indkøbsvognskonteksten ikke består (f.eks. salgstilbud). Scenarier i POS og e-handel kan også udnytte denne anvendelse. En lavere samlet pris, når varerne i indkøbsvognen beregnes som et sæt (f.eks. til adskilte bundter, sammenkædede eller anbefalede produkter eller produkter, der allerede er føjet til indkøbsvognen), kan overtale kunder til at føje produkter til indkøbsvognen.

Datamodellen for både anmodningen og svaret fra API'en *CalculateSalesDocument* er **indkøbsvogn**. I forbindelse med denne API kaldes datamodellen dog **SalesDocument**. Da de fleste egenskaber er valgfrie, og kun nogle få af dem har indflydelse på prisberegningen, vises der kun prisrelaterede felter i følgende tabel. Vi fraråder, at der involveres andre felter i API-anmodningen.

Området for API'en *CalculateSalesDocument* er kun beregningen af priser og rabatter. Skatter og gebyrer er ikke involveret.

Følgende tabel viser inputparametrene i det objekt, der kaldes **salesDocument**.

| Navn             | Undernavn | Type | Obligatorisk/valgfri | Beskrivende tekst |
|------------------|----------|------|-------------------|-------------|
| Id               | | streng | Obligatorisk | Identifikatoren for salgsdokumentet. |
| CartLines        | | IList\<CartLine\> | Valgfri | Listen over linjer, der skal beregnes priser og rabatter for. |
|                  | ProductId | langt format | Påkrævet i området CartLine | Post-id for produkt. |
|                  | ItemId | streng | Valgfri | Vareidentifikator. Hvis der er angivet en værdi, skal den svare til værdien af parameteren **ProductId**. |
|                  | InventoryDimensionId | streng | Valgfri | Lagerdimensionens identifikator. Hvis der er angivet en værdi, skal kombinationen af værdierne for **ItemId** og **InventoryDimensionId** svare til værdien af parameteren **ProductId**. |
|                  | Quantity | decimal | Påkrævet i området CartLine | Antallet af produktet. |
|                  | UnitOfMeasureSymbol | streng | Valgfri | Produktets enhed. Hvis der ikke er angivet en værdi, anvender API som standard produktets salgsenhed. |
| CustomerId       | | streng | Valgfri | Debitors kontonummer. |
| LoyaltyCardId    | | streng | Valgfri | Fordelskundekortets identifikator. Alle debitorkonti, der er tilknyttet fordelskundekortet, skal svare til værdien for parameteren **CustomerId** (hvis den er angivet). Fordelskundekortet tages ikke i betragtning, hvis det ikke findes, eller dets status er **Blokeret**. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Valgfri | Niveaulinjer for tilknytning af fordelskunde. Hvis der er angivet værdier for **CustomerId** og/ eller **LoyaltyCardId**, flettes de tilsvarende linjer på fordelskundeniveau med linjer, der er angivet i værdien for **AffiliationLines**. |
|                  | AffiliationId | langt format | Påkrævet i området af AffiliationLoyaltyTier | Tilknytningspost-id. |
|                  | LoyaltyTierId | langt format | Påkrævet i området af AffiliationLoyaltyTier | Fordelskundeniveaupost-id. |
|                  | AffiliationTypeValue | int | Påkrævet i området af AffiliationLoyaltyTier | En værdi, der angiver, om tilknytningslinjen er af typen **Generelt** (**0**) eller **Fordelskunde** (**1**). Hvis denne parameter er angivet til **0**, bruger API værdien **AffiliationId** som identifikator og ignorerer værdien af **LoyaltyTierId**. Hvis den er angivet til **1**, bruger API værdien **LoyaltyTierId** som identifikator og ignorerer værdien af **AffiliationId**. |
|                  | ReasonCodeLines | Kollektion\<ReasonCodeLine\> | Påkrævet i området af AffiliationLoyaltyTier | Linjer i årsagskode. Denne parameter har ingen indflydelse på prisberegningen, men er påkrævet som del af objektet **AffiliationLoyaltyTier**. |
|                  | CustomerId | streng | Påkrævet i området af AffiliationLoyaltyTier | Debitors kontonummer. |
| Kuponer          | | IList\<Coupon\> | Valgfri | Kuponer, der ikke gælder (inaktive, udløbne eller ikke findes), tages ikke med i betragtning ved prisberegningen. |
|                  | Kode | streng | Påkrævet i området af Kupon | Kuponkode. |
|                  | CodeId | streng | Valgfri | Kuponkodens identifikator. Hvis der er angivet en værdi, skal den svare til værdien af parameteren **Kode**. |
|                  | DiscountOfferId | streng | Valgfri | Rabatidentifikatoren. Hvis der er angivet en værdi, skal den svare til værdien af parameteren **Kode**. |

**Eksempel på anmodningstekst**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Hele indkøbsvognsobjektet returneres som svartekst. Hvis du vil kontrollere priser og rabatter, skal du fokusere på felterne i følgende tabel.

| Navn           | Undernavn | Type | Beskrivende tekst |
|----------------|----------|------|--------------|
| NetPrice       | | decimal | Nettoprisen for hele salgsdokumentet, før rabatterne anvendes. |
| DiscountAmount | | decimal | Det samlede rabatbeløb på hele salgsdokumentet. |
| TotalAmount    | | decimal | Det samlede beløb på hele salgsdokumentet. |
| CartLines      | | IList\<CartLine\> | Beregnede linjer, der indeholder pris- og rabatoplysninger. |
|                | Pris | decimal | Produktets enhedspris. |
|                | NetPrice | decimal | Nettoprisen for linjen, før rabatterne anvendes (= *pris* &times; *antal*). |
|                | DiscountAmount | decimal | Rabatbeløbet. |
|                | TotalAmount | decimal | Det endelige samlede prissætningsresultat for linjen. |
|                | PriceLines | IList\<PriceLine\> | Prisdetaljer, herunder kilden til prisen (basispris, prisjustering eller samhandelsaftale) og beløbet. |
|                | DiscountLines | IList\<DiscountLine\> | Rabatoplysninger. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Hvis der findes en indkøbsvogn med flere indkøbsvognslinjer, returnerer API'en *GetAvailablePromotions* alle gældende rabatter for indkøbslinjerne. 

Hovedanvendelsen af API'en *GetAvailablePromotions* er indkøbsvognens side, hvor detailhandlere ønsker at vise anvendte rabatter eller tilgængelige kuponer til den aktuelle indkøbsvogn.

I følgende tabel vises inputparametrene for API'en *GetAvailablePromotions*.

| Navn        | Type | Obligatorisk/valgfri | Beskrivende tekst |
|-------------|------|-------------------|-------------|
| nøgle         | streng | Obligatorisk | indkøbsvognens id. |
| cartLineIds | IEnumerable\<string\> | Valgfri | Angiv kun denne parameter for at returnere rabatter for udvalgte indkøbsvognslinjer. |

**Eksempel på svartekst**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

API'en *AddCoupons* understøtter tilføjelse af en liste over kuponer til en indkøbsvogn. Det returnerer indkøbsvognsobjektet, når kuponerne er tilføjet.

I følgende tabel vises inputparametrene for API'en *AddCoupons*.

| Navn                 | Type | Obligatorisk/valgfri | Beskrivende tekst |
|----------------------|------|-------------------|-------------|
| nøgle                  | streng | Obligatorisk | Indkøbsvognens id. |
| couponCodes          | IEnumerable\<string\> | Obligatorisk | De kuponkoder, der skal føjes til indkøbsvognen. |
| isLegacyDiscountCode | bool | Valgfri | Angiv denne parameter til **sand** for at angive, at kuponen er en ældre rabatkode. Standardværdien er **falsk**. |

## <a name="removecoupons"></a>RemoveCoupons

API'en *RemoveCoupons* understøtter fjernelse af en liste over kuponer fra en indkøbsvogn. Det returnerer indkøbsvognsobjektet, når kuponerne er fjernet.

I følgende tabel vises inputparametrene for API'en *RemoveCoupons*.

| Navn        | Type | Obligatorisk/valgfri | Beskrivende tekst |
|-------------|------|-------------------|-------------|
| nøgle         | streng | Obligatorisk | Indkøbsvognens id. |
| couponCodes | IEnumerable\<string\> | Obligatorisk | De kuponkoder, der skal fjernes fra indkøbsvognen. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
