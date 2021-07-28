---
title: Politik for omkostningstotaler og beregning af fast omkostning
description: Dette emne indeholder oplysninger om, hvordan du bestemmer det korrekte niveau af sekundære omkostningselementer og opretter regler for omkostningstotaler, der passer til organisationsrapportering og omkostningssporing.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6eb052b640d2418f6ddd1a06b1b0d529074b7f89
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355053"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Politik for omkostningstotaler og beregning af fast omkostning 

[!include [banner](../includes/banner.md)]

Med omkostningsregnskab kan du få indsigt i, hvordan omkostningsforløbet er relateret til de produkter og tjenester, der leveres i en organisation. For at få vist gennemsigtigheden for omkostninger er det vigtigt at opnå omkostningsfordeling mellem omkostningsobjekter baseret på et passende fordelingsgrundlag. Som standard opnås omkostningstildelingen for det primære omkostningselement, der er behov for i nogle situationer, men det har nogle konsekvenser, som bør overvejes.

-   Hjælpeomkostningsobjekter slutter med en saldo på nul for det primære omkostningselement efter beregning af faste omkostninger.

-   Omfanget af omkostningsposter, der er genereret ved beregning af faste omkostninger, kan være meget omfattende.

-   Det er ikke muligt at spore omkostningsforløbet mellem omkostningsobjekter.

For at undgå disse virkninger kan du i Omkostningsregnskab konfigurere omkostningstildeling, så det passer til din organisations ledelsesmæssige rapporteringskrav. I dette emne beskrives, hvordan du bestemmer det korrekte niveau af sekundære omkostningselementer og opretter regler for omkostningstotaler, der passer til organisationsrapportering og omkostningssporing.

> [!NOTE]
> Du kan ændre konfigurationer, hvis rapporteringskrav ændres.

## <a name="example-of-cost-rollup-policy-setup"></a>Eksempel på opsætning af politik for omkostningstotaler

Forestil dig, at en organisation har følgende struktur med 4 bærere.

![Eksempel på en organisationsstruktur.](./media/dimension-hierarchy-org.png)

**Dimension for omkostningsobjekt**

| Bærere | Betegnelse          |
|--------------|-----------|
| CC001        | HR        |
| CC002        | Finans   |
| CC003        | Samling  |
| CC004        | Emballage |

**Dimension for omkostningselement**

| Omkostningselementer | Beskrivelse | Type    |
|---------------|-------------|---------|
| 1001          | Elektricitet | Primær |
| 1002          | Lønninger    | Primær |
| 1003          | Annoncer | Primær |

Et dimensionshierarki, der opfylder de organisatoriske rapporteringskrav, kan konfigureres på følgende måde.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension    | Navn på dimensionshierarkitype      | Adgangslistehierarki |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Bærere | Klassifikationshierarki for dimension | Nr.                    |

**Dimensionshierarki**

|    &nbsp;    | Intervaller for dimensionsmedlemmer | &nbsp;              |
|--------------|-------------------------|---------------------|
| **Noder**        | **Fra dimensionsmedlem**   | **Til dimensionsmedlem** |
| Organisation |                         |                     |
| &nbsp;&nbsp;Administration             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;HR               | CC002                   | CC002               |
| &nbsp;&nbsp;Produktion               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Emballage              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling             | CC004                   | CC004               |

Et dimensionshierarki, der opfylder kravene i politikken, kan konfigureres på følgende måde.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension     | Navn på dimensionshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Driftsregnskab  | Omkostningselementer | Klassifikationshierarki for dimension |

**Dimensionshierarki**

|      &nbsp;             | Intervaller for dimensionsmedlemmer |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| Noder                   | Fra dimensionsmedlem   | Til dimensionsmedlem |
| Driftsregnskab |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primære omkostninger                    | 10001                   | 10003               |

Når finansposterne er behandlet, ser omkostningssaldoposten efter omkostningsobjekt sådan ud.

|      &nbsp;          | **Omkostningsobjekt** | &nbsp;    |  &nbsp;   |  &nbsp;   | **Sum**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Omkostningselement**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektricitet** | 100,00          | 200.00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Lønninger**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Annoncer** | 0.00            | 4.000,00  | 0.00      | 0.00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistisk dimension**

| Statistiske elementer |    Beskrivelse   |
|----------------------|------------------|
| SE-1                 | HR-tjenester      |
| SE-2                 | Finans-tjenester |

Omkostningsobjektet CC001 personale bidrager med personaletjenester til flere omkostningsobjekter.

HR-tjenester forbruges ud fra følgende distribution af størrelsesorden.

| Omkostningsobjekt | Beskrivelse |   HR-tjenester |
|-------------|-------------|----|
| CC002       | Finans     | 35 |
| CC003       | Samling    | 55 |
| CC004       | Emballage   | 10 |

Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.

Finans-tjenester forbruges ud fra følgende distribution af størrelsesorden.

| Omkostningsobjekt |   Beskrivelse    |  Finans-tjenester   |
|-------------|------------------|----|
| CC003       | Samling         | 65 |
| CC004       | Emballage        | 35 |

Politikker for omkostningsfordeling kan konfigureres på følgende måde.

| Navn på politik | Beskrivelse     | Dimensionshierarki for omkostningsobjekt | Statistisk dimension | Dimension for omkostningselement |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Omkostningstildeling | Organisation                    | Statistiske elementer  | Omkostningselementer          |

Regler for omkostningsfordeling kan konfigureres på følgende måde.

| Dimensionshierarkinode for omkostningsobjekt | Funktionalitet af omkostning | Tildelingsgrundlag        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Samlet         | **HR-tjenester**        |
| CC002                                | Samlet         | **Finansielle tjenester** |

## <a name="brhow-cost-flows-between-cost-centers"></a><br>Hvordan omkostninger flyder mellem bærere 

Hvis du vil vide, hvordan omkostninger flyder mellem bærerne i organisationen, kan du oprette omkostningselementer af typen **Sekundær** for hver bærer. Disse omkostningselementer kan derefter bruges til at overføre saldi mellem bærerne under beregningen af faste omkostninger.

Dimensionsmedlemmer for omkostningselement kan konfigureres på følgende måde.

| Omkostningselementer | Type          |     &nbsp;    |
|---------------|---------------|---------------|
| 1001          | Elektricitet   | Primær       |
| 1002          | Lønninger      | Primær       |
| 1003          | Annoncer   | Primær       |
| **SC-CC001**  | **HR**        | **Sekundære** |
| **SC-CC002**  | **Finans**   | **Sekundære** |
| **SC-CC003**  | **Samling**  | **Sekundære** |
| **SC-CC004**  | **Emballage** | **Sekundære** |

Dimensionshierarkiet **Driftsregnskab** skal opdateres med de nye dimensionsmedlemmer, så dimensionshierarkiet indeholder de korrekte data, der kan bruges til at definere rapportering og politikker.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension     | Navn på dimensionshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Driftsregnskab  | Omkostningselementer | Klassifikationshierarki for dimension |

**Dimensionshierarki**

|      &nbsp;             | Intervaller for dimensionsmedlemmer |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| Noder                   | Fra dimensionsmedlem   | Til dimensionsmedlem |
| Driftsregnskab |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primære omkostninger                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sekundære omkostninger                         | **SC-CC001**            | **SC-CC004**        |

Opret en **Politik for omkostningstotaler**, hvor hver bærer er knyttet til et tilsvarende omkostningselement af typen **Sekundære**.

**Politikker for omkostningstotaler**

| Navn på politik | Beskrivelse | Dimensionshierarki for omkostningsobjekt | Dimensionshierarki for omkostningselement |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Omkostningsforløb   | Organisation                    | Driftsregnskab          |

**Regler for omkostningstotaler**

| Dimensionshierarkinode for omkostningsobjekt | Dimensionshierarkinode for omkostningselement | Sekundært omkostningselement |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Driftsregnskab               | **SC-CC001**           |
| CC002                                | Driftsregnskab               | **SC-CC002**           |
| CC003                                | Driftsregnskab               | **SC-CC003**           |
| CC004                                | Driftsregnskab               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Udfør beregning af fast omkostning

**Kladde**

| Kladden | Kladdetype            | Regnskabskalenderperiode | År | Termin | Version       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Kladde for omkostningsfordeling | Regnskabsår                 | 2017    | 1. Periode | Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1 |

Systemet anvender nu **Politik for omkostningstotaler**, når det opretter **Kladdeposteringer for omkostningsobjektsaldo**.

**Kladdeposteringer for omkostningsobjektsaldo**

| Regnskabsdato | Omkostningsobjekt | Beskrivelse  | Omkostningselement | Beskrivelse |  Beløb |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 01-31-2017      | CC001       | HR           | SC-CC001 | HR        | 10.100,00 |
| 01-31-2017      | CC002       | Finans      | SC-CC002 | Finans   | 17.735,00 |
| 01-31-2017      | CC003       | Samling     | SC-CC003 | Samling  | 31.082,75 |
| 01-31-2017      | CC004       | Emballage    | SC-CC004 | Emballage | 15.717,25 |

> [!NOTE]
> Kladdeposteringerne oprettes ud fra reglerne i **Politik for omkostningstotaler**, hvis der findes en politik. Saldoen, der vises, er saldoen for beregningen af faste omkostninger.

Siden **Oplysninger om kladdepost for omkostningssaldo for omkostningsobjekt**, der åbnes fra kladdeposteringerne, viser, hvordan saldoen opnås.

**Eksempel: Kladdepostering for omkostningsobjekt CC002 Finans**

**Oplysninger om kladdepost for omkostningssaldo for omkostningsobjekt**

| Dimensionsmedlem for omkostningselement | Beskrivelse |  Beløb   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektricitet | 200.00    |
| 1002                          | Lønninger    | 10.000,00 |
| 1003                          | Annoncer | 4.000,00  |
| SC-CC001                      | HR          | 3.535,00  |

**Omkostningsposter, der er genereret af beregningen af fast omkostning**

| Omkostningsobjekt | Beskrivelse  | Omkostningselement   | Beskrivelse  |        Beløb     |       Regnskabsdato     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | HR           | SC-CC001 | HR              | 10.100,00. \- | 01-31-2017 |
| CC002       | Finans      | SC-CC001 | HR              | 3.535,00    | 01-31-2017 |
| CC003       | Samling     | SC-CC001 | HR              | 5.555,00    | 01-31-2017 |
| CC004       | Emballage    | SC-CC001 | HR              | 1.010,00    | 01-31-2017 |
| CC002       | Finans      | SC-CC002 | Finans         | 17.735,00. \- | 01-31-2017 |
| CC003       | Samling     | SC-CC002 | Finans         | 11.527,75   | 01-31-2017 |
| CC004       | Emballage    | SC-CC002 | Finans         | 6.207,25    | 01-31-2017 |

Når **Beregning af fast omkostning** er fuldført, kan du rapportere resultaterne ved hjælp af værktøjer som Microsoft SharePoint Workspace, Excel eller Power BI.

## <a name="view-reporting-in-excel"></a>Vise rapportering i Excel 

Dimensionshierarkierne gør det muligt at få vist data på forskellige aggregeringsniveauer.

Her er et eksempel på en Power Pivot-rapportering i Excel.

| **Driftsregnskab** | **Omkostningsobjekt** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **Sum**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Primære omkostninger**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| 1001. &nbsp;&nbsp;&nbsp;&nbsp;                            | 100,00          | 200.00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0.00            | 4.000,00       | 0.00          | 0.00          | **4.000,00**  |
|**Sekundære omkostninger**                            | **-10.100,00**  | **-14.200,00** | **17.082.75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | 10.100,00. \-     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0.00            | 17.735,00. \-    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
| **Sum**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Ved hjælp af **Politik for omkostningstotaler** og **Omkostningselementer af typen Sekundær** kan du lade den primære omkostning pr. omkostningsobjekt til intern afrapportering være som den primære omkostning, der er tilbage efter **Beregning af fast omkostning**.

Hvis det samme eksempel var foretaget uden at oprette **Politik for omkostningstotaler**, ville være rapporteringsresultatet være som vist nedenfor. Omkostningen flyder korrekt, men sporbarhed og indsigt i, hvordan omkostningen forløber mellem bærerne, går tabt.

| **Driftsregnskab** | **Omkostningsobjekt** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **Sum**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Primære omkostninger**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|1001. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0.00            | 0.00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0.00            | 0.00      | 22.275,00     | 12.225,00     | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0.00            | 0.00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Sekundære omkostninger**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
| **Sum**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Afhængigt af krav til rapportering og sporbarhed i organisationen kan du bestemme det korrekte niveau af sekundære omkostningselementer og oprette regler for omkostningstotaler, der passer til dine behov.

Den klare adskillelse mellem **Omkostningstildeling** og **Politikker for omkostningstotaler** giver fleksibilitet til at foretage løbende opdateringer, uden at de påvirker hinanden.



## <a name="additional-resources"></a>Yderligere ressourcer
-  [Dimensioner for omkostningsobjekt](cost-objects.md)
-  [Dimensioner for omkostningselement](cost-elements.md)
-  [Dimensionshierarki](dimension-hierarchy.md)
-  [Beregning af faste omkostninger](overhead-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]