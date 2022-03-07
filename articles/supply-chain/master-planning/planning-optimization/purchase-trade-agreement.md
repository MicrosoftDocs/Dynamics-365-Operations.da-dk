---
title: Varedisponering med handelsaftaler om indkøb
description: Dette emne beskriver, hvordan planlægningsoptimering kan finde leverandøren og/eller gennemløbstiden for et ordreforslag baseret på den bedste pris eller leveringstid, der er fundet i handelsaftaler om indkøb.
author: ChristianRytt
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 138bf58e07d4d6df3c2106e4176e02fcdb0a6dba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820412"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Varedisponering med handelsaftaler om indkøb

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan planlægningsoptimering kan finde leverandøren og/eller leveringstiden for et ordreforslag baseret på den bedste pris eller leveringstid, der er fundet blandt alle handelsaftaler om indkøb, som er blevet specificeret for et givet produkt.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Aktivér funktionen Handelsaftaler om indkøb til planlægningsoptimering

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *Handelsaftaler om indkøb til planlægningeoptimering*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Forbered systemet til evaluering af handelsaftaler om indkøb under varedisponering

Udfør følgende trin for at konfigurere systemet til at foretage planlægningsoptimering, der evaluerer handelsaftaler om indkøb.

1. Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**. På fanen **Ordreforslag** i sektionen **Leverandør** skal du indstille følgende værdier:

    - **Find handelsaftale** – Angiv denne indstilling til **Ja** for at medtage handelsaftaler om indkøb i varedisponering.
    - **Søgekriterium** – Vælg den faktor, som du vil prioritere for hver handelsaftale om indkøb: **Kortest leveringstid** eller **Laveste stykpris**.

1. Gå til **Indkøb og forsyning \> Konfiguration \> Priser og rabatter \> Aktivering af pris/rabat**, og kontrollér, at indstillingen **Leverandør** er angivet til **Ja**.
1. Gå til **Administration af produktoplysninger \> Konfiguration \> Dimensions- og variantgrupper \> Lagringsdimensionsgrupper**, og vælg en lagringsdimensionsgruppe, der gælder for produkter, som varedisponering skal evaluere handelseaftaler om indkøb for. Kontrollér, at alle relevante lagringsdimensioner i denne gruppe er markeret i kolonnen **Ved indkøbspriser**. Gentag dette trin for enhver anden relevant lagringsdimensionsgruppe.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Forbered et frigivet produkt på at evaluere handelsaftaler om indkøb under varedisponering

Når systemet er forberedt som beskrevet i forrige afsnit, skal du følge disse trin for at sikre, at de produkter, du vil bruge sammen med denne funktion, er konfigureret korrekt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**, og åbn et målprodukt.
1. I oversigtspanelet **Indkøb** skal du kontrollere, at der ikke er tildelt nogen leverandør i feltet **Leverandør**.
1. I handlingsruden på fanen **Plan** i gruppen **Disponering** skal du vælge **Varedisponering** for at åbne siden **Varedisponering** for det valgte produkt. Kontrollér følgende indstillinger:

    - På fanen **Generelt** kan du konfigurere tilsidesættelse af leverandører. Hvis du ønsker, at planlægningsoptimering bruger handelsaftaler om indkøb til at vælge en leverandør, skal du forhindre tilsidesættelse af leverandører ved at fjerne markeringen i afkrydningsfeltet **Brug specifik indstilling**.
    - På fanen **Leveringstid** kan du konfigurere tilsidesættelse af leveringstider. Hvis du ønsker, at planlægningsoptimering skal bruge handelsaftaler om indkøb til at vælge leveringstider, skal du forhindre tilsidesættelse af leveringstider. Fjern markeringen i afkrydsningsfeltet for hver type leveringstid, du vil vælge ved hjælp af handelsaftaler om indkøb (**Indkøb**, **Produktion** og/eller **Overførsel**).

1. Luk siden **Varedisponering** for at vende tilbage til siden med detaljer for det valgte produkt.
1. I handlingsruden på fanen **Plan** i gruppen **Prognose** skal du vælge **Forsyningsprognose** for at åbne siden **Forsyningsprognose**. Sørg for, at ingen af de rækker, der vises her, har en værdi i kolonnen **Kreditorkonto**.
1. Luk siden **Forsyningsprognose** for at vende tilbage til siden med detaljer for det valgte produkt.
1. I handlingsruden på fanen **Indkøb** i gruppen **Handelsaftaler** skal du vælge **Vis handelsaftaler**. Kontroller, at alle relevante handelsaftaler om indkøb er angivet. Kontrollér også, at indstillingen **Ignorer leveringstid** er angivet til **Nej** for hver aftale, hvor du vil bruge planlægningsoptimering til at anvende den leveringstid, der er angivet for den pågældende aftale.
1. I handlingsruden på fanen **Plan** i gruppen **Ordreindstillinger** skal du vælge **Standardindstillinger for ordre** for at åbne siden **Standardindstillinger for ordre** for det valgte produkt. I oversigtspanelet **Indkøbsordre** kan du få vist værdien for feltet **Leveringstid for indkøb**. Hvis der ikke er defineret tilsidesættelse af leveringstid ved varedisponering, vil planlægningsoptimering bruge denne værdi, når der vælges handelsaftaler, hvor indstillingen **Ignorer leveringstid** er angivet til **Ja**. Derfor bør du justere denne værdi efter behov.
1. Gentag denne procedure for hvert relevant produkt.

> [!NOTE]
> Valutaen i linjen på handelsaftalen om indkøb skal svare til valutaen for den valgte leverandør. Varedisponering omfatter kun oplysninger fra linjer i handelsaftaler om indkøb, hvor valutaen svarer til valutaen for leverandøren.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Eksempler på, hvordan planlægningsoptimering finder leverandør og leveringstider

Følgende tabel indeholder eksempler, der viser, hvordan forskellige indstillinger for et frigivet produkt og de tilknyttede handelsaftaler om indkøb påvirker de værdier, der findes for det resulterende indkøbsordreforslag. Værdierne med **fed** skrift i de to kolonner længst til højre er de værdier, der er valgt ved planlægningsoptimering. Værdierne **_fed og kursiv_** i de andre kolonner er de indstillinger, der frembragte de resulterende værdier for hver række.

| Frigivet produkt: Leverandør | Standardindstillinger for ordre: Leveringstid | Varedisponering: Tilsidesæt leverandør | Varedisponering: Tilsidesæt leveringstid | Handelsaftale: Leverandør | Handelsaftale: Leveringstid | Handelsaftale: Ignorer leveringstid | Resulterende leverandør | Resulterende leveringstid |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Ingen | Ingen | US003 | 3 | Ingen | **US001** | **1** |
| US001 | 1 | ***Ja: US002** _ | _*_Ja: 2_*_ | US003 | 3 | Ingen | **US002** | **2** |
| *(Tom)* | 1 | Ingen | Ingen | ***US003** _ | _*_3_*_ | Ingen | **US003** | **3** |
| *(Tom)* | ***1** _ | Ingen | Ingen | _*_US003_*_ | 3 | Ja | **US003** | **1** |
| *(Tom)* | ***1** _ | _*_Ja: US002_*_ | Ingen | US003 | 3 | Ingen | **US002** | **1** |
| *(Tom)* | ***1** _ | _*_Ja: US002_*_ | Ingen | US003 | 3 | Ingen | **US002** | **1** |
| *(Tom)* | 1 | Ingen | Ja: 2 | ***US003** _ | _*_3_*_ | Ingen | **US003** | **3** |
| *(Tom)* | 1 | Ingen | ***Ja: 2** _ | _*_US003_*_ | 3 | Ja | **US003** | **2** |

## <a name="additional-resources"></a>Yderligere ressourcer

[Købsaftaler](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]