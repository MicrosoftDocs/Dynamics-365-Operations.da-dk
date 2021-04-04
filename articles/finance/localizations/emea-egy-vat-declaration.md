---
title: Momsopgørelse for Egypten
description: Dette emne forklarer, hvordan du konfigurerer og genererer momsindberetningsformular til Egypten.
author: sndray
manager: AnnBe
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7859d5a5e3273cd6e55edd1c1ce9fc4699d7ab33
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574317"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Momsopgørelse for Egypten (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du kan oprette og generere formularen til momsangivelse og salgs- og indkøbsbøger for juridiske enheder i Egypten.

Formularen til momsindberetning i Egypten er det officielle dokument, der opsummerer det samlede udgående momsbeløb, det samlede indgående momsbeløb, der kan inddrives, og det relaterede skyldige momsbeløb. Formularen bruges til alle typer skatteydere og skal udfyldes manuelt via momsmyndighedsportalen. Formularen til momsindberetning kaldes normalt momsindberetningsregistrering.

Formularen Momsindberetning i Dynamics 365 Finance omfatter følgende rapporter:

- Formularen momsindberetning nummer 10, som indeholder en opdeling af beløb, reguleringer og momsbeløb pr. linjevare i formen momsindberetning, som det beskrives i lovgivningen.
- Salgstransaktionsbog
- Købstransaktionsbog

## <a name="prerequisites"></a>Forudsætninger
Den primære adresse for den juridiske enhed være i Egypten.
I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktion:

   - (Egypten) Kategorihierarki for rapporten Salgs- og købsmoms.

Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

I arbejdsområdet for **elektronisk rapportering** skal du importere følgende format for elektronisk rapportering fra lageret:

- Momsopgørelse Excel (EG)

> [!NOTE]
> Formatet ovenfor er baseret på **Momsopgørelsesmodel** og bruger **Tilknytning til momsopgørelsesmodel**. Der importeres automatisk yderligere konfigurationer.

Du kan finde flere oplysninger om, hvordan du importerer konfigurationer af elektronisk rapportering, i [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Hent konfigurationer for elektronisk rapportering

Implementeringen af formularen til momsindberetning for Egypten er baseret på konfigurationen af Elektronisk rapportering (ER). Du kan finde flere oplysninger om egenskaberne og koncepterne ved konfigurerbar rapportering under [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Se i forbindelse med produktions- og brugermodtagelsestestmiljøer (UAT) [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere formularen til momsindberetning og relaterede rapporter i en juridisk enhed til rapportering af moms, skal du overføre følgende konfigurationer:

- Momsopgørelsesmodel.version.70.xml eller senere version
- Momsopgørelsesmodel mapping.version.70.120.xml eller senere version
- Momsopgørelse Excel (EG).version.70.32 eller en senere version

Når du har hentet ER-konfigurationerne fra Lifecycle Services (LCS) eller det globale lager, skal du gennemføre følgende trin.

1. Gå til arbejdsområdet **Elektronisk rapportering** og vælg feltet **Rapporteringskonfigurationer**.
1. Gå til siden **Konfigurationer**, og vælg **Kurs** > **Indlæs fra XML-fil** i handlingsruden.
1. Overfør filerne i den rækkefølge, de er angivet ovenfor. Når alle konfigurationerne er overført, skal konfigurationstræet være til stede i Finans.

## <a name="set-up-application-specific-parameters"></a>Oprette ansøgningsspecifikke parametre

De applikationsspecifikke parametre giver dig mulighed for at fastlægge kriterierne for, hvordan momstransaktioner skal klassificeres og beregnes på hver linje, når rapporten genereres. Fastsættelsen er baseret på konfigurationen af varemomsgruppe, momsgruppe, momskode og andre kriterier, der er defineret i opslagsdefinitionen.

Rapporter for salgs- og indkøbskartotek for indkøbsordrer indeholder et sæt kolonner, der svarer til bestemte transaktionsklassifikationer som operationstyper, produkter og dokumenter, der er specifikke for inddelingen. I stedet for at medtage disse nye klassifikationer som nye postdata, når posteringerne bogføres, vil klassifikationerne blive fastlagt på basis af forskellige opslag, der er indført i **Konfigurationer** > **Konfigurer programspecifikke parametre** > **Konfiguration** for at opfylde kravene i momsrapporter for Egypten. 

![Side med ansøgningsspecifikke parametre](media/egypt-vat-declaration-setup1.png)

Følgende opslagskonfigurationer bruges til at klassificere transaktionerne i rapporter over indkøbs- og salgsmomsbøger:

- **PurchaseItemTypeLookup** > Kolonne O: Varetype
- **VATRateTypeLookup** > Kolonne B: Momstype
- **VATRateTypeLookup** > Kolonne C: Tabelvaretype
- **PurchaseOperationTypeLookup** > Kolonne A: dokumenttype
- **SalesOperationTypeLookup** > Kolonne N: Operationstype
- **SalesItemTypeLookup** > Kolonne O: Varetype

Gennemfør følgende trin for at konfigurere de forskellige opslag, der bruges til at oprette momsopgørelser og relaterede bograpporter. 

1. I arbejdsområdet for **elektronisk rapportering** skal du vælge **Konfigurationer** > **Opsætning** for at oprette regler, der identificerer momsposteringen i det relaterede felt i formularen til momsangivelse.
2. Vælg den aktuelle version, og vælg opslagsnavnet på oversigtspanelet **Opslag**. F.eks. **SalesItemTypeLookup**. Dette opslag identificerer listen over klassifikationer i momsbogen, der kræves af skattemyndighederne.
3. I oversigtspanelet **Betingelser** skal du vælge **Tilføj** og på den nye linje i kolonnen **Opslagsresultat** vælge den relaterede linje, der repræsenterer klassifikationen i **Kolonne O**.
4. Vælg den **Momsgruppe**, der bruges til at identificere klassifikationen, i kolonnen Momsgruppe. F.eks. **Indenlandsk salgsfaktura**. Du kan også bruge varemomsgruppe, momskode eller kombinationen af træattributter, hvis konfigurationen er defineret på en anden måde. 
5. Vælg momsposteringsklassifikationen i kolonnen **Navn**.
6. Gentag trin 3-5 for alle tilgængelige opslag.
7. Vælg **Tilføj** for at medtage den sidste postlinje, og vælg **Ikke relevant** i kolonnen **Opslagsresultat**. 
8. Vælg **Ikke tom** i resten af kolonnerne. 

> [!NOTE]
> Når du tilføjer den sidste post, **Ikke relevant**, definerer du følgende regel: Når momsgruppen, varemomsgruppe, momskode og navn, der er overskredet som et krav, ikke opfylder nogen af de tidligere regler, indgår transaktionerne ikke i momsbogen. Selvom denne regel ikke bruges, når rapporten genereres, hjælper reglen med at undgå fejl ved generering af rapporter, når der mangler en regelkonfiguration.

Følgende tabeller repræsenterer et eksempel på en foreslået konfiguration til de beskrevne opslagskonfigurationer. 

**SalesItemTypeLookup**

| Opslagsresultat         | Type | Momsgruppe    | Varemomsgruppe    | Momskode (kode) | Navn                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Indland              | 1    | Lokal moms          | *Ikke tom*             | *Ikke tom*     | Sales                 |
| Indland              | 2    | Lokal moms          | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Indland              | 3    | VAT_FINALC         | *Ikke tom*             | *Ikke tom*     | Sales                 |
| Indland              | 4    | VAT_FINALC         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Indland              | 5    | VAT_PUBLIO         | *Ikke tom*             | *Ikke tom*     | Sales                 |
| Indland              | 6    | VAT_PUBLIO         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Eksport                | 7    | VAT_EXPORT         | *Ikke tom*             | *Ikke tom*     | Sales                 |
| Eksport                | 8    | VAT_EXPORT         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Maskine og udstyr | 9    | *Ikke tom*        | VAT_M og E                 | *Ikke tom*     | Sales                 |
| Maskine og udstyr | 10   | *Ikke tom*        | VAT_M og E                 | *Ikke tom*     | SalesCreditNote       |
| Maskine til dele        | 11   | *Ikke tom*        | VAT_PARTS               | *Ikke tom*     | Sales                 |
| Maskine til dele        | 12   | *Ikke tom*        | VAT_PARTS               | *Ikke tom*     | SalesCreditNote       |
| Fritagelser            | 13   | VAT_EXE            | *Ikke tom*           | *Ikke tom*     | SaleExempt            |
| Fritagelser            | 14   | VAT_EXE            | *Ikke tom*           | *Ikke tom*     | SalesExemptCreditNote |
| Ikke anvendelig        | 15   | *Tom*            | *Tom*                 | VAT_ADJ         | *Ikke tom*           |
| Ikke anvendelig        | 16   | *Ikke tom*        | *Ikke tom*             | *Ikke tom*     | *Ikke tom*           |

 **SalesOperationTypeLookup**

| Opslagsresultat  | Type | Varemomsgruppe    | Skattekode    | Navn                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Varer          | 1    | VAT_GOODS               | *Ikke tom* | Sales                 |
| Varer          | 2    | VAT_GOODS               | *Ikke tom* | SalesCreditNote       |
| Varer          | 3    | VAT_GOODS               | *Ikke tom* | SaleExempt            |
| Varer          | 4    | VAT_GOODS               | *Ikke tom* | SalesExemptCreditNote |
| Ydelser       | 5    | VAT_SERV                | *Ikke tom* | Sales                 |
| Ydelser       | 6    | VAT_SERV                | *Ikke tom* | SalesCreditNote       |
| Ydelser       | 7    | VAT_SERV                | *Ikke tom* | SaleExempt            |
| Ydelser       | 8    | VAT_SERV                | *Ikke tom* | SalesExemptCreditNote |
| Reguleringer    | 9    | *Tom*                 | VAT_ADJ     | Sales                 |
| Reguleringer    | 10   | *Tom*                 | VAT_ADJ     | Indkøb              |
| Ikke anvendelig | 11   | *Ikke tom*             | *Ikke tom* | *Ikke tom*           |

**PurchaseItemTypeLookup**

| Opslagsresultat          | Type | Varemomsgruppe    | Skattekode    | Navn                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Varer                  | 1    | VAT_GOODS               | *Ikke tom* | Indkøb                 |
| Varer                  | 2    | VAT_GOODS               | *Ikke tom* | PurchaseCreditNote       |
| Ydelser               | 3    | VAT_SERV                | *Ikke tom* | Indkøb                 |
| Ydelser               | 4    | VAT_SERV                | *Ikke tom*  | PurchaseCreditNote       |
| Maskine og udstyr  | 5    | VAT_M og E                 | *Ikke tom* | Indkøb                 |
| Maskine og udstyr  | 6    | VAT_M og E                 | *Ikke tom* | PurchaseCreditNote       |
| Maskine til dele         | 7    | VAT_PARTS               | *Ikke tom* | Indkøb                 |
| Maskine til dele         | 8    | VAT_PARTS               | *Ikke tom* | PurchaseCreditNote       |
| Fritagelser             | 9    | VAT_EXE                 | *Ikke bank*  | PurchaseExempt           |
| Fritagelser             | 10   | VAT_EXE                 | *Ikke tom* | PurchaseExemptCreditNote |
| Ikke anvendelig         | 11   | *Tom*                 | VAT_ADJ     | *Ikke tom*              |
| Ikke anvendelig         | 12   | *Ikke tom*             | *Ikke tom* | *Ikke tom*              |
| Ikke anvendelig         | 13   | *Tom*                 | *Ikke tom* | *Ikke tom*              |

**PurchaseOperationTypeLookup**

| Opslagsresultat  | Type | Momsgruppe  | Skattekode    | Navn                     |
|----------------|------|------------------|-------------|--------------------------|
| Indland       | 1    | Lokal moms        | *Ikke tom* | Indkøb                 |
| Indland       | 2    | Lokal moms        | *Ikke tom* | PurchaseCreditNote       |
| Indland       | 3    | Lokal moms        | *Ikke tom* | PurchaseExempt           |
| Indland       | 4    | Lokal moms        | *Ikke tom* | PurchaseExemptCreditNote |
| Importeret       | 5    | VAT_IMPORT       | *Ikke tom* | Indkøb                 |
| Importeret       | 6    | VAT_IMPORT       | *Ikke tom* | PurchaseCreditNote       |
| Importeret       | 7    | VAT_IMPORT       | *Ikke tom* | PurchaseExempt           |
| Importeret       | 8    | VAT_IMPORT       | *Ikke tom* | PurchaseExemptCreditNote |
| Reguleringer    | 9    | *Tom*          | VAT_ADJ     | PurchaseCreditNote       |
| Reguleringer    | 10   | *Tom*          | VAT_ADJ     | Indkøb                 |
| Ikke anvendelig | 11   | *Ikke tom*      | *Ikke tom* | *Ikke tom*              |

**VATRateTypeLookup**

| Opslagsresultat  | Type | Momskode (kode) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Ikke tom*     |
| SecondTable    | 4    | *Ikke tom*     |
| Ikke anvendelig | 5    | *Ikke tom*     |


## <a name="set-up-general-ledger-parameters"></a>Konfigurer økonomiparametre

Hvis du vil generere momsindberetningsformularrapporten i Microsoft Excel-format, skal du definere et ER-format på siden **Økonomiparametre**.

1. Gå til **Moms** > **Opsætning** > **Finansparametre**.
2. På fanen **Salgsmoms** i sektionen **Momsindstillinger** i feltet **Tilknytningsformat for momsindberetning** skal du vælge **VAT Declaration Excel (EG)**. Hvis du lader feltet stå tomt, genereres standardrapporten for moms i SSRS-format.
3. Vælg **Kategorihierarki**. Denne kategori gør det muligt for varekoden i posteringer under fanen Udenrigshandel at give brugerne mulighed for at vælge og klassificere varer og tjenester. Denne klassifikation beskrives i salgs- og indkøbsposteringsrapporter. Denne konfiguration er valgfri.

![Rapport formular](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Generér en momsindberetningsrapport
Den proces, der er med til at forberede og sende en rapport over momsindberetning for en periode, er baseret på momsbetalingstransaktioner, der er bogført under jobbet Afregn og bogfør moms. Yderligere oplysninger om afregning og rapportering af moms finder du i [Oversigt over moms](../general-ledger/indirect-taxes-overview.md).

Fuldfør følgende trin, hvis du vil generere den elektroniske momsopgørelse:

1. Gå til **Moms** > **Afregninger** > **Moms** > **Rapport for moms i afregningsperiode** eller **Afregn og bogfør moms**.
2. Vælg **Afregningsperiode**.
3. Vælg fra-datoen, og vælg derefter momsbetalingsversionen.
5. Vælg **OK**. 
6. Angiv kreditbeløbet fra den forrige periode, hvis det er relevant, eller lad beløbet være nul.
7. Vælg én af følgende tilgængelige indstillinger i feltet **Rapportdetaljer**. 
   - **Momsbog for indkøb** Opret rapporten med oplysninger om købsmomsposteringer.
   - **Momsbog for salg**: Opret rapporten med oplysninger om salgsmomsposteringer.
   - **Momsopgørelse**: Generer kun formularen til momsopgørelse.
8. Angiv navnet på den person, der er registreret til tildeling af formularen.
9. Vælg sprog. Alle rapporter oversættes i **en-us** og **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


