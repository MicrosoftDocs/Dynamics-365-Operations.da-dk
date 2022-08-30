---
title: Forespørgsler og rapporter om farligt materiale
description: Denne artikel forklarer, hvordan du kan arbejde med forskellige rapporter, der er relateret til farlige materialer. Mange af disse rapporter er påkrævet, så du overholder angivne standarder i forordninger for forskellige farlige materialet under forsendelse og opbevaring på lager.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 784361f4e715921890ecff784b62935988732464
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335159"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Forespørgsler og rapporter om farligt materiale

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management leverer forskellige rapporter, der er relateret til farlige materialer. Mange af disse rapporter er påkrævet, så du overholder angivne standarder i forordninger for forskellige farlige materialet under forsendelse og opbevaring på lager.

Alle disse rapporter, bortset fra rapporten **Multimodalt farligt gods**, kan bruge den leveringsmåde, der er defineret for forsendelsen, til at finde den forordning, der skal bruges til at udskrive forsendelsesteksten for varer. Leveringsmåden er tilknyttet fragtmanden og fragttjenesten. Derfor skal du oprette en fragtmand og fragttjeneste og knytte dem til en leveringsmåde. Leveringsmåden er relateret til forordningen om farligt materiale.

I følgende illustration vises sekvensen af aktiviteter, der finder sted, når systemet genererer rapporter over skadelige materialer.

![Serie af aktiviteter for rapporter over farligt materiale.](media/hazmat-report-sequence.png "Serie af aktiviteter for rapporter over farligt materiale")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Konfigurere rapportering af farlige materialer

Hvis du leverer varer, der indeholder farligt materiale, skal du normalt generere bestemte rapporter, der er med til at skabe sikkerhed og overholde bestemmelser for farlige materialer. Benyt følgende fremgangsmåde for at konfigurere rapporter:

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
2. Åbn fanen **Rapporter**. Angiv følgende felter i oversigtspanelet **Rapportparameter for farligt materiale**.

    | Sektion | Felt | Beskrivelse |
    |---|---|---|
    | Multimodalt farligt gods | Forordningskode | Vælg den forordning, der skal bruges, når der genereres en rapport over **Multimodalt farligt gods**. |
    | Lagergrænser for farligt materiale | Forordningskode | Vælg den forordning, der skal anvendes ved evaluering af lagergrænser. |
    | Transport af varer ad vej | Produkt i CMR-gruppe | "CMR" står for "carcinogenic, mutagenic, and reprotoxic substances" (kræftfremkaldende, mutagene og reproduktionstoksiske stoffer). Angiv denne indstilling til **Ja** for at konfigurere systemet til at udskrive bestemte advarsler og meddelelser, der er relateret til håndteringen af disse stoffer. |
    | Transport af varer ad vej | Beskrivelse af gruppe for farligt materiale | Angiv teksten til specifikke advarsler, der er relateret til CMR og transport af varer på vejene. Denne tekst medtages i rapporten. |
    | Afsenders deklaration | Advarsel! | Indtast teksten for en advarselsmeddelelse, der skal udskrives på afsenderens deklarationsformular (f.eks. "Advarsel: farligt gods, brændbart"). |
    | Afsenders deklaration | Sidefodsdeklaration | Indtast teksten i en meddelelse, der skal udskrives nederst i forsendelsesdeklarationens dokument. |
    | Sprog for rapport om farligt gods | Sprog for indenlandsk rapport om farligt gods | Vælg standardsprog til rapporter om farligt materiale, der er tilknyttet indenrigsforsendelser. |
    | Sprog for rapport om farligt gods | Sprog for rapport om eksport af farligt gods | Vælg standardsprog til rapporter om farligt materiale, der er tilknyttet udenrigsforsendelser. |

## <a name="hazardous-materials-report"></a>Rapport over farlige materialer

Rapporten **Farlige materialer** indeholder en oversigt over alle de varer, der er blevet oprettet og defineret, så de har oplysninger om farligt gods. Du kan bruge denne rapport til at overvåge og gennemse de oplysninger, du skal håndtere. Siden til rapporten viser et begrænset udvalg af felter fra opsætningen af farligt materiale. Du kan dog tilpasse den, hvis du vil tilføje flere felter efter behov.

Hvis du vil have vist denne rapport, skal du gå til **Administration af produktoplysninger \> Forespørgsler og rapporter \> Forsendelsesdokumentation til farligt materiale \> Farlige materialer**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Rapporten Grænse for farlig lagerbeholdning

Med rapporten **Grænse for farlig lagerbeholdning** kan du overvåge lagerbeholdningsniveauerne for de farlige materialer på lagerlokationer og sikre, at de forbliver under de fastsatte sikkerhedsgrænser. Disse grænser kommer fra de grænser, der er defineret for de enkelte frigivne produkter.

Hvis du vil have vist denne rapport, skal du gå til **Administration af produktoplysninger \> Forespørgsler og rapporter \> Forsendelsesdokumentation til farligt materiale \> Lagergrænser for farligt materiale**.

Du kan finde flere oplysninger om, hvordan du konfigurerer lagergrænser for en frigivet produkt, under [Angive lagerbeholdningsgrænser for farlige produkter](hazmat-items.md#stock-limits).

Den forordning, der bruges til lagergrænser, defineres på siden **Parametre til lokationsstyring**. Gå til **Lokationsstyring \> Konfiguration \> Parametre til lokationsstyring**, og brug fanen **Rapporter** i **Grænse for farlig lagerbeholdning** til at angive en forordningskode. Yderligere oplysninger finder du i afsnittet [Konfigurere rapportering af farlige materialer](#set-up) tidligere i denne artikel.

## <a name="verified-gross-mass-report"></a>Rapporten Bekræftet bruttomasse

Du kan bruge rapporten **Bekræftet bruttomasse** til at udskrive oplysninger om en forsendelses vægt.

Hvis du vil generere og udskrive denne rapport, skal du gå til **Lokationsstyring \> Forsendelser \> Alle forsendelser** og åbne den relevante forsendelse. Vælg derefter **Bekræftet bruttomasse** i gruppen **Dokument for farligt materiale** under fanen **Forsendelser** i handlingsruden.

## <a name="multimodal-dangerous-goods-report"></a>Rapporten Multimodalt farligt gods

Rapporten **Multimodalt farligt gods** er beregnet til forsendelser, der skal flyttes ved hjælp af en kombination af transportmåder. Den bruges typisk, når en forsendelse først flyttes ad vejene og senere ad søvejen.

Hvis du vil generere og udskrive denne rapport, skal du gå til **Lokationsstyring \> Forsendelser \> Alle forsendelser** og åbne den relevante forsendelse. Vælg derefter **Multimodalt farligt gods** i gruppen **Dokument for farligt materiale** under fanen **Forsendelser** i handlingsruden.

Når du genererer denne rapport, gemmes oplysningerne, så du kan redigere dem og/eller udskrive rapporten igen, hvis det er nødvendigt. Hvis du vil redigere en genereret rapport, skal du gå til **Lokationsstyring \> Forespørgsler og rapporter \> Forsendelsesdokumentation til farligt materiale \> Multimodalt farligt gods** og finde den relevante rapport på listen. Når du er færdig med at redigere indholdet efter behov, skal du vælge **Udskriv** i handlingsruden for at udskrive rapporten.

## <a name="shippers-declaration-report"></a>Rapporten Afsenders deklaration

Med rapporten **Afsenders deklaration** kan du udskrive oplysninger, der er knyttet til en deklaration af de materialer, der er medtaget i forsendelsen.

Hvis du vil generere og udskrive denne rapport, skal du gå til **Lokationsstyring \> Forsendelser \> Alle forsendelser** og åbne den relevante forsendelse. Vælg derefter **Afsenders deklaration** i gruppen **Dokument for farligt materiale** under fanen **Forsendelser** i handlingsruden.

## <a name="carriage-of-merchandise-by-road-report"></a>Rapporten Transport af varer ad vej

**Transport af varer ad vej** ligner en fragtseddel, men anvendes typisk til vejtransport i Europa i henhold til aftalen om international transport af farligt gods ad vej (ADR-regler). Denne rapport bruger forsendelsesudskrivningsteksten til en vare, medmindre du har angivet feltet **Beskrivelse af farlig materialegruppe** på siden **Parametre til lokationsstyring**.

Hvis du vil generere og udskrive denne rapport, skal du gå til **Lokationsstyring \> Forsendelser \> Alle forsendelser** og åbne den relevante forsendelse. Vælg derefter **Transport af varer ad vej** i gruppen **Dokument for farligt materiale** under fanen **Forsendelser** i handlingsruden.

Når du genererer denne rapport, gemmes oplysningerne, så du kan redigere dem og/eller udskrive rapporten igen, hvis det er nødvendigt. Hvis du vil redigere en genereret rapport, skal du gå til **Lokationsstyring \> Forespørgsler og rapporter \> Forsendelsesdokumentation til farligt materiale \> Transport af varer ad vej** og finde den relevante rapport på listen. Når du er færdig med at redigere indholdet efter behov, skal du vælge **Udskriv** i handlingsruden for at udskrive rapporten.

## <a name="shipment-summary-report"></a>Oversigtsrapport for forsendelse

Rapporten **Forsendelsesoversigt** indeholder oplysninger, der er opsummeret efter den transportkategori, der er relateret til de frigivne varer.

Hvis du vil generere og udskrive denne rapport, skal du gå til **Lokationsstyring \> Forsendelser \> Alle forsendelser** og åbne den relevante forsendelse. Vælg derefter **Forsendelsesoversigt** i gruppen **Dokument for farligt materiale** under fanen **Forsendelser** i handlingsruden.

## <a name="bill-of-lading-report"></a>Rapporten Fragtseddel

Når funktionen for farligt materiale er aktiveret for systemet, indeholder rapporten **Fragtseddel** kolonnen **Farlige materialer**, der angiver, om en last indeholder farligt materiale. Denne rapport er tilgængelig på siden **Alle laster** som normalt.

## <a name="packing-list-report"></a>Rapporten Plukliste

Når funktionen for farligt materiale er aktiveret for systemet, indeholder pakkelister yderligere oplysninger vedrørende forsendelsesudskrivningsteksten for en vare. Denne rapport er tilgængelig på siden **Alle laster** som normalt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]