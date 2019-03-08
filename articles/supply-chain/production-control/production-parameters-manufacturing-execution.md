---
title: Produktionsparametre i Produktionsudførelse
description: Dette emne indeholder oplysninger om konfiguration af produktionsparametre i Produktionsudførelse.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bf1afd18132e92cf081b7bde5067e1be90314467
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "339458"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Produktionsparametre i Produktionsudførelse

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om konfiguration af produktionsparametre i Produktionsudførelse.

Modulet **Produktionsudførelse** er primært beregnet til produktionsfirmaer. Det kan bruges til at registrere tids- og vareforbrug på produktionsjob eller projekter. Før du går i gang med at bruge modulet Produktionsudførelse til jobregistreringer, skal du konfigurere forskellige produktionsparametre, der definerer, hvordan og hvornår registreringer skal bogføres under produktionsprocessen. Indstillinger af produktionsparametre påvirker lagerstyring, produktionsstyring og omkostningsberegning.

Før arbejderne går i gang med at foretage registreringer på produktionsjob, skal du nøje overveje alle indstillinger på siden **Produktionsordreparametre**. Klik på **Produktionsstyring** &gt; **Opsætning** &gt; **Produktionsudførelse** &gt; **Produktionsordrestandarder**. Hvis dit firma bruger funktionalitet med flere steder, skal du måske konfigurere forskellige produktionsparametre for hvert sted. Integrationsparametrene til modulet **Produktion** konfigureres under følgende faner på siden **Produktionsparametre**:

- **Generelt** – Generelle parameterindstillinger for produktionsjob i Produktionsudførelse.
- **Start** – Parametre, der bruges, når produktionsoperationerne er gået i gang.
- **Operationer** – Parametre, der anvendes på produktionsoperationer og tilbagemeldinger om operationer i produktionsprocessen.
- **Færdigmeld** – Parametre, der bruges, når varer færdigmeldes i den sidste operation for en produktionsordre.
- **Validering af antal** – Parametre, der bruges til at validere start- og tilbagemeldingsantal på produktionsordrer.

## <a name="types-of-production-jobs"></a>Typer af produktionsjob
Under fanen **Operationer** skal du vælge, hvilke typer af produktionsjob, der kræver registrering på siden **Jobregistrering**.

Arbejderne foretager typisk registreringer på opstillingsjob og procesjob. Men hvis der anvendes finplanlægning, kan du vælge andre jobtyper, hvor arbejderne skal foretage registreringer for, hvornår produktionsordrer behandles. Du kan for eksempel kræve registreringer på transportjob.

> [!IMPORTANT]
> Sørg for at vælge alle relevante jobtyper. Ellers er job muligvis ikke tilgængelige til registrering på siden **Jobregistrering**. Dine valg skal svare til valgene i kolonnen **Jobstyring** under fanen **Opsætning** på siden **Rutegrupper** (**Produktionsstyring** &gt; **Opsætning** &gt; **Ruter** &gt; **Rutegrupper**).

Hvis **Jobstyring** er valgt i rutegruppen, færdigmeldes denne jobtype på produktionsordren, når jobbet færdigmeldes i Produktionsudførelse. Når alle jobtyper, som **Jobstyring** er valgt for, er færdigmeldt for en operation, færdigmelder Produktionsudførelse operationen.

> [!NOTE]
> Visse jobtyper kan færdigmeldes manuelt via produktionskladder. I dette tilfælde skal du vælge **Jobstyring** for jobtypen, men ikke vælge jobtypen for registrering under fanen **Operationer** på siden **Produktionsparametre** i Produktionsudførelse.

## <a name="bom-consumption-and-picking-list-journals"></a>Styklisteforbrug og pluklistekladder
En ensartet opsætning for styklisteforbrug er vigtig, fordi den hjælper med at sikre, at lagerstyringen bliver effektiv. Hvis parametrene for styklisteforbrug f.eks. ikke er konfigureret korrekt i Produktionsudførelse, kan materialer blive fratrukket fra lageret to gange eller slet ikke.

På siden **Produktionsparametre** konfigureres automatisk styklisteforbrug i tre stadier:

- Ved starten af en produktion. Konfigurer dette stadie under fanen **Start**.
- I produktionsprocessen, når en operation er fuldført. Konfigurer dette stadie under fanen **Operationer**.
- Når en produktionsordre færdigmeldes. Konfigurer dette stadie under fanen **Færdigmeld**.

For hvert stadie kan du i feltet **Auto-styklisteforbrug** vælge en af tre metoder til pluk af varer til en produktionsordre:

- **Varetrækprincip** – Denne indstilling bruges sammen med en indstilling, der er defineret for styklisten i modulet **Produktion**. Klik på **Produktionsstyring** &gt; **Almindelige** &gt; **Produktionsordrer** &gt; **Alle produktionsordrer**. Vælg en produktionsordre i listen på siden **Alle produktionsordrer**, og klik derefter på **Stykliste** i handlingsruden. På siden **Stykliste** under fanen **Opsætning** skal du vælge i feltet **Varetrækprincip** vælge en af følgende indstillinger:

  - **Igangsæt**
  - **Afslut**
  - **Manuel**
  - Tom (der er ikke valgt nogen indstilling).
  - **Disponibel på lokation**

    I Produktionsudførelse, hvis **Varetrækprincip** er valgt i feltet **Auto-styklisteforbrug** under fanen **Start**, trækkes alle materialer, der er indstillet til **Start** i styklisten fra lageret, når operationen startes. Indstillingen **Disponibel på lokation** bruges til produkter, der er aktiveret til avancerede lagerprocesser. Hvis du vælger dette varetrækprincip, ryddes materialet, når lagerstedsarbejde til pluk af råmateriale er fuldført. Materiale ryddes også, når en styklistelinje, bruger dette varetrækprincip, frigives til lagerstedet, og materialet disponibelt på produktionsindlagringsstedet.

    > [!NOTE]
    > Hvis feltet **Varetrækprincip** er angivet under fanen **Start** i Produktionsudførelse, skal du vælge det samme princip under fanen **Operationer** eller under fanen **Færdigmeld**. Dette krav er med til at sikre, at materialer fratrækkes på lageret for de styklister, der bruger **Afslut** som varetrækprincip på produktionsordren. Hvis det samme varetrækprincip ikke er valgt under fanen **Operationer** eller fanen eller **Færdigmeld**, kan materialer blive trukket fra lageret to gange.

- **Altid** – Hvis du vælger denne indstilling for et stadie, bliver materiale altid fratrukket på lager i dette stadie. Materiale til produktionen fratrækkes f.eks., når produktionsordren startes. Denne indstilling kræver, at **Aldrig** er markeret under fanen **Operationer** og fanen **Færdigmeld**. Dette krav er med til at forhindre, at varer bliver fratrukket to gange på lageret.
- **Aldrig** – Hvis du vælger denne indstilling for et stadie, finder der intet styklisteforbrug sted i dette stadie. Hvis du f.eks. vælger **Aldrig** under alle tre faner (**Start**, **Operationer** og **Færdigmeld**), skal materialer fratrækkes manuelt på lageret.

> [!IMPORTANT]
> Overvej omhyggeligt konfigurationen af produktionsparametrene, og sørg for, at de parametre, der er valgt under forskellige faner på siden **Produktionsparametre**, ikke er indbyrdes modstridende.

I følgende eksempler vises nogle parameterindstillinger, der understøtter forskellige principper for styklisteforbrug. Parametrene indstilles på siden **Produktionsparametre** i Produktionsudførelse.

### <a name="example-1-backflushing-on-operations"></a>Eksempel 1: Varetræk ved operationer

Brug følgende indstillinger, hvis pluklistekladderne og forbruget af styklistevaren skal oprettes, når varer færdigmeldes i en operation.

| Fane                | Felt                          | Indstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Opdater igangsætning online           | **Status** eller **Status + antal** |
| Start              | Automatisk styklisteforbrug      | **Aldrig**                           |
| Operations         | Automatisk styklisteforbrug      | **Altid**                          |
| Færdigmelding | Automatisk styklisteforbrug      | **Aldrig**                           |
| Færdigmelding | Opdater færdigmelding online | **Status + antal**               |

### <a name="example-2-backflushing-on-production"></a>Eksempel 2: Varetræk ved produktion

Brug følgende indstillinger, hvis pluklistekladderne og forbruget af styklistevaren skal oprettes, når varer færdigmeldes i produktionsordren.

| Fane                | Felt                          | Indstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Opdater igangsætning online           | **Status** eller **Status + antal** |
| Start              | Automatisk styklisteforbrug      | **Aldrig**                           |
| Operations         | Automatisk styklisteforbrug      | **Aldrig**                           |
| Færdigmelding | Automatisk styklisteforbrug      | **Altid**                          |
| Færdigmelding | Opdater færdigmelding online | **Status + antal**               |

### <a name="example-3-flushing-principle"></a>Eksempel 3: Varetrækprincip

Brug følgende indstillinger, hvis pluklistekladder og forbruget af styklistevaren skal oprettes i henhold til det varetrækprincip, der er indstillet for styklistevarerne.

| Fane                | Felt                          | Indstilling                |
|--------------------|--------------------------------|------------------------|
| Start              | Opdater igangsætning online           | **Status + antal**  |
| Start              | Automatisk styklisteforbrug      | **Varetrækprincip** |
| Operations         | Automatisk styklisteforbrug      | **Varetrækprincip** |
| Færdigmelding | Automatisk styklisteforbrug      | **Aldrig**              |
| Færdigmelding | Opdater færdigmelding online | **Status + antal**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Eksempel 4: Fratræk af materialer under start af en produktionsordre

Brug følgende indstillinger, hvis pluklistekladderne og forbruget af styklistevaren skal oprettes, når en produktion startes.

| Fane                | Felt                          | Indstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Opdater igangsætning online           | **Status + antal**               |
| Start              | Automatisk styklisteforbrug      | **Altid**                          |
| Operations         | Automatisk styklisteforbrug      | **Aldrig**                           |
| Færdigmelding | Automatisk styklisteforbrug      | **Aldrig**                           |
| Færdigmelding | Opdater færdigmelding online | **Status** eller **Status + antal** |

Ud fra de valg, der er beskrevet tidligere i dette afsnit, bogføres pluklistekladder på forskellige stadier af produktionsordreprocessen:

- Når en operation startes
- Når antalstilbagemeldingen rapporteres for en operation
- Når varer færdigmeldes i produktionsordren

### <a name="example-5-manual-bom-consumption"></a>Eksempel 5: Manuelt styklisteforbrug

Du kan bruge følgende indstillinger, hvis materiale altid skal fratrækkes lageret manuelt. I så fald bogføres ingen pluklistekladder.


|        Fane         |             Felt              |         Indstilling         |
|--------------------|--------------------------------|-------------------------|
|       Start        |      Opdater igangsætning online      | <strong>Status</strong> |
|       Start        |   Automatisk styklisteforbrug    | <strong>Aldrig</strong>  |
|     Operations     |   Automatisk styklisteforbrug    | <strong>Aldrig</strong>  |
| Færdigmelding |   Automatisk styklisteforbrug    | <strong>Aldrig</strong>  |
| Færdigmelding | Opdater færdigmelding online | <strong>Status</strong> |

