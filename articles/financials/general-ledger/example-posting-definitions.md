---
title: "Bogføringsdefinitioner"
description: "Denne artikel indeholder eksempler på, hvordan bogføringsdefinitioner bruges for behæftelser i indkøbsordrer og budgetdisponeringer."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 10015952773ce0ae6ab36912df636919b572704d
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="posting-definition-examples"></a>Eksempler på bogføringsdefinitioner

[!include [banner](../includes/banner.md)]

Denne artikel indeholder eksempler på, hvordan bogføringsdefinitioner bruges for behæftelser i indkøbsordrer og budgetdisponeringer.

Inden du læser dette emne, skal du være fortrolig med bogføringsdefinitioner og posteringsbogføringsdefinitioner. Du kan finde flere oplysninger i [Bogføringsdefinitioner](posting-definitions.md). Følgende eksempler kan konfigureres på siden **Bogføringsdefinitioner**. Hvert eksempel indeholder følgende områder:

-   Bogføringsdefinition – søgekriterier
-   Bogføringsdefinition – genererede poster
-   Posteringer med konti, dimensionsværdier og beløb
-   Finansposter genereret fra bogføringsdefinitionen

Når der er en match mellem kontiene og dimensionsværdierne i ruden **Sammenlign kriterier** for bogføringsdefinitionen og dimensionsværdierne i posteringen, genereres der finansposter med udgangspunkt i ruden **Genererede poster** for bogføringsdefinitionen. 
> [!NOTE]
> Knyt en bogføringsdefinition til en bestemt posteringstype ved brug af siden **Definitioner af posteringsbogføring**. Efter at du har knyttet en bogføringsdefinition til en posteringstype og valgt **Brug bogføringsdefinitioner** på siden **Finansparametre**, skal alle posteringer med den valgte posteringstype bruge bogføringsdefinitioner.

## <a name="example-purchase-order-encumbrances"></a>Eksempel: Behæftelser for indkøbsordrer
Når du aktiverer behandling af behæftelser ved at vælge **Aktivér behæftelse** på siden **Finansparametre**, skal der bruges bogføringsposteringer til registrering af behæftelser i finans for alle konti, der skal hensættes. I de fleste tilfælde hensættes alle udgiftskonti på balancen. 

Bogføringsdefinitioner for behæftelser konfigureres for modulet **Køb** på siden **Bogføringsdefinitioner**. I området **Køb** på siden **Definitioner af posteringsbogføring** kan du derefter vælge den posteringstype for **Indkøbsordre**, der skal bruges for at knytte bogføringsdefinitionen til indkøbsordrer. 

Alle bilagsposteringer for indkøbsordrebehæftelser skal være afstemt (dvs. debet skal være lig med kredit) inden for hver enkelt dimension på et bilag.

### <a name="posting-definition--match-criteria"></a>Bogføringsdefinition – søgekriterier

| Kontostruktur       | Sammenlign kontonummer | Prioritet  |
|-------------------------|----------------------|----------|
| Kontostruktur – drift | \*                   | 1        |

<em>En tom værdi i feltet **Sammenlign kontonummer</em>* betyder, at alle tilsvarende konti i den definerede kontostruktur vil indgå i sammenholdningsreglen.

### <a name="posting-definition--generated-entries"></a>Bogføringsdefinition – genererede poster

| Kontostruktur | Genereret kontonummer                    | Genereret debet/kredit |
|-------------------|---------------------------------------------|------------------------|
| Saldo           | 300143 - -(Behæftelseskonto)             | Samme                   |
| Saldo           | 300144 - -(Reservér til behæftelseskonto) | Balancere              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Posteringer med konti, dimensionsværdier og beløb

Konti og dimensionsværdier hentes enten fra de regnskabsfordelinger, som du angiver for en indkøbsordrelinje, eller de kommer fra de konti og dimensioner, som genereres automatisk på grundlag af standardindstillingerne for leverandører, varer, kategorier og dimensionsskabeloner.

| Konto + dimensioner           | Debet  | Kredit | Kommentar |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Uddannelse | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansposter genereret fra bogføringsdefinitionen

Genererede finansposter oprettes til registrering af behæftelserne.

| Konto + dimensioner           | Debet  | Kredit | Kommentar |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Uddannelse | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Uddannelse |        | 250,00 |         |

I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen. Når 606500-OU\_1-OU\_3566-Uddannelse evalueres, oprettes der derfor genererede poster for de konti, der er defineret for bogføringsdefinitionen i ruden **Genererede poster**.

## <a name="example-budget-appropriations"></a>Eksempel: Budgetdisponeringer
Når du aktiverer budgetdisponering ved at vælge **Aktivér budgetdisponering** på siden **Finansparametre**, skal bogføringsdefinitionerne bruges til registrering af budgetregisterposter i finans. Når der findes en aktiv budgetstyringskonfiguration, som er aktiveret, kan der bruges bogføringsdefinitioner og posteringsbogføringsdefinitioner som et led i registreringen af poster vedrørende disponering, revision, overførsel, projekt, anlægsaktiv samt udbuds- og efterspørgselsprognoser i finans. 

Hvis du vil konfigurere en bogføringsdefinition for budgetregisterposter med budgettypen **Oprindeligt budget**, hvor der er aktiveret disponeringer, kan du vælge modulet **Budget** på siden **Bogføringsdefinitioner**. I området **Budget** på siden **Definitioner af posteringsbogføring** kan du derefter bruge budgetkoderne til at knytte bogføringsdefinitionen til budgetregisterposter med budgettypen **Oprindeligt budget**. 

Når budgetdisponeringer og bogføringsdefinitioner er aktiveret, registreres budgetregisterposter for budgetstyring og i finans.

### <a name="posting-definition--match-criteria"></a>Bogføringsdefinition – søgekriterier

| Kontostruktur       | Sammenlign kontonummer | Prioritet  |
|-------------------------|----------------------|----------|
| Kontostruktur – drift | \*                   | 1        |

<em>En tom værdi i feltet **Sammenlign kontonummer</em>* betyder, at alle tilsvarende konti i den definerede kontostruktur vil indgå i sammenholdningsreglen.

### <a name="posting-definition--generated-entries"></a>Bogføringsdefinition – genererede poster

| Kontostruktur | Genereret kontonummer              | Genereret debet/kredit |
|-------------------|---------------------------------------|------------------------|
| Kontostruktur | 300145 - (Forventet omsætningskonto) | Samme                   |
| Kontostruktur | 300146 - (Disponeringskonto)     | Balancere              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Posteringer med konti, dimensionsværdier og beløb

Du kan angive konti, dimensionsværdier og beløb for budgetkontoposten på siden **Budgetregisterpost**.

| Konto + dimensioner           | Debet | Kredit | Kommentar |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Uddannelse |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansposter genereret fra bogføringsdefinitionen

Genererede finansposter oprettes til registrering af de oprindelige budget i hver dimension.

| Konto + dimensioner           | Debet  | Kredit | Kommentar |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Uddannelse |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Uddannelse | 250,00 |        |         |

I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen. Derfor oprettes de genererede finansposter, når 606400-OU\_1-OU\_3566-Uddannelse evalueres.






