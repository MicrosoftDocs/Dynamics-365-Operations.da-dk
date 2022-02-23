---
title: Grænser for lokationslagring
description: I dette emne beskrives funktionerne til grænser for lokationslagring.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607273"
---
# <a name="location-stocking-limits"></a>Grænser for lokationslagring

[!include [banner](../includes/banner.md)]

Du kan bruge siden **Grænser for lokationslagring** (**Lokationsstyring \> Konfiguration \> Lagersted \> Grænser for lokationslagring**) til at styre lastkapaciteten på lagersteder uden at skulle bruge de mere avancerede processer til volumenberegninger af fysiske produkter.

Formålet med lokationslagergrænsen er at evaluere den maksimale mængde, som en lokation kan indeholde. Du kan konfigurere funktionen på et af tre niveauer, der hver især har egen fane på siden **Grænser for lokationslagring**:

- Produkter
- Produktvarianter
- Containertyper

Du kan definere forskellige feltværdier for hvert niveau. Systemet evaluerer derefter kapaciteten for en bestemt lokation, baseret på **Antal** og **Enhed**-værdierne for hver række. På den måde vælges den mest detaljerede matchningspost først. En række, der har en værdi i feltet **Lokationsprofil-id**, vil f.eks. blive evalueret før en række, der kun har en værdi i feltet **Lagersted**. Den resterende kapacitet evalueres også på grundlag af **Antal**-værdien i den post med grænse for lokalitetslagring, der bruges.

I afsnittet **Produkter** på siden kan du definere følgende feltværdier for søgningen efter grænser for lokationslagring:

- Lagersted
- Id for lokationsprofil
- Adresse
- Kategori-id for pakkestørrelse
- varenummer
- Enhed

> [!NOTE]
> Du behøver ikke at definere en **Enhed**-værdi for hver post med grænse for lokationslagring. Beregningerne af lokationskapaciteten baseres på antallet af lagerenheder. Hvis der ikke er defineret en enhedskonvertering for en værdi, der bruges, springes posten med grænsen for lokationslagring over, som om der er defineret en anden værdi af **Varenummer** for den.

## <a name="example--purchase-order-receiving"></a>Eksempel – Købsordre, der modtages

Dette eksempel er baseret på et rent *USMF*-demodatasæt, hvor følgende værdier er angivet under fanen **Produktvarianter** på siden **Grænser for lokationslagring**.

| Lagersted | Id for lokationsprofil | varenummer | Størrelse | Kvantitet | Enhed |
|-----------|---------------------|-------------|------|----------|------|
| 24        | Etage               | D0013       | M    | 300      | Styk   |
| 24        | Etage               | D0013       | L    | 240      | Styk   |
| 24        | Etage               | D0013       | L    | 360      | Styk   |

Der er defineret forskellige måleenheder for produktvarianterne. Disse varianter justeres med grænser for lokalitetslagring for tre paller (PL):

- **Størrelse M:** 1 PL = 100 hver (Styk)
- **Størrelse L:** 1 PL = 80 hver
- **Størrelse S:** 1 PL = 120 hver

Derfor kan hver lokation, hvor **Lokationsprofil-id**-værdien er angivet til *Etage*, indeholde *3* *PL* af varenummer *D0013*.

### <a name="prepare-for-the-example"></a>Forberede eksemplet

I dette eksempel skal du køre en indkøbsordre, der modtager flow for to linjer. Du skal dog først opdatere demodataene på følgende måde for at sikre, at lokationerne tillader, at der kan udføres blandede varer, men det er kun de tomme lokationer *FL-002* til *FL-004*, der bruges, og der er ikke noget åbent indgående arbejde.

1. For lokationen *FL-001* skal du ændre værdien i feltet **Lokationsprofil** fra *Etage* til *Etage-05*.
1. For *Etage* lokationsprofilen skal du angive indstillingen **Tillad blandede vare** til *Ja*.
1. Opret en indkøbsordre, der har følgende to linjer:

    | Lagersted | varenummer | Størrelse | Kvantitet | Enhed |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | L    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Behandle eksemplet

Du modtager først antallet *4* af enhed *PL* i størrelse *S*, og du kan gennemse lokationer af læg på-linje for det arbejde, der oprettes. Du modtager derefter antallet *4* af enhed *PL* i størrelse *L*, og du kan gennemse lokationer af læg på-linje for det arbejde, der oprettes.

1. I lagerstedsappen skal du logge på ved at bruge *24* som bruger-id og *1* som adgangskode.
1. Vælg **Indgående** \> **Købsmodtagelse**.
1. Modtag *4* *PL* af varenummer *D0013* i størrelse *S*.
1. Gennemgå det læg på lager-arbejde, der er oprettet. Du bør se følgende resultat:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Modtag *4* *PL* af varenummer *D0013* i størrelse *L*.
1. Gennemgå det læg på lager-arbejde, der er oprettet. Du bør se følgende resultat:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

På baggrund af resultaterne kan du konkludere, at systemet ikke kunne allokere de korrekte læg på lager-lokationer. Hvorfor ville systemet ellers kun tilføje *1* *PL* af størrelse *L* til lokation *FL-003* i sidste trin, og ikke *2* *PL*? Med andre ord, hvorfor er der i alt *3* *PL* for læg på lager på den pågældende lokation?

For at forklare denne tilsyneladende fejl skal du forstå udvælgelseskriterierne for grænserne for lokationslagring. Systemet udvælger den mest detaljerede matchningspost. I dette eksempel er den mest detaljerede matchningspost den linje, hvor **Størrelse**-værdien er *L*, **Antal**-værdien er *240*, og **Enhed**-værdien er *Hver*. Da du allerede har åbnet arbejde fra den forrige modtagelse af et antal på *120* *Hver* af størrelse *S*, beregnes den resterende kapacitet som *240* – *120* = *120* *Hver*. Derfor kan den resterende kapacitet kun indeholde *1* *PL* af *80* *Hver*.

> [!NOTE]
> Du kan ikke bruge grænser for lokalitetslagring til at styre f.eks. genopfyldning af varer, der har forskellige antal på samme lokation. I dette tilfælde skal du bruge en *genopfyldningsskabelon*.
