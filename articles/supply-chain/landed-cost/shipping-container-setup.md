---
title: Forsendelsescontainere
description: Dette emne beskriver, hvordan du konfigurerer forsendelsescontainere for modulet Landingsomkostninger.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500952"
---
# <a name="shipping-container-setup"></a>Opsætning af forsendelsescontainere

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne beskriver, hvordan du konfigurerer forsendelsescontainere for modulet **Landingsomkostninger**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Konfigurere forsendelsescontainertyper

Forsendelsescontainertyper definerer de typer forsendelsescontainere, der er tilgængelige for brug under forsendelse og fragt.

Du kan arbejde med forsendelsescontainertyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Forsendelsescontainertyper**. Her kan du se, tilføje og fjerne poster for dine containertyper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Forsendelsescontainertype | Angiv et entydigt id-navn/-nummer for forsendelsescontainertypen. |
| Beskrivelse | Angiv en beskrivelse af forsendelsescontainertypen. |
| Mængde | Angiv den maksimale mængde, der er tilladt i denne forsendelsescontainertype. |
| Tykkelse | Angiv den maksimale vægt, der er tilladt i denne forsendelsescontainertype. |
| Kan returneres | Angiv, om denne forsendelsescontainertype kan returneres til leverandøren, når den er brugt under en fragt. Hvis denne indstilling er angivet til *Ja*, kan der gælde yderligere omkostninger for returnering af denne forsendelsescontainertype til oprindelseshavnen. |

## <a name="set-up-shipping-containers"></a>Konfigurere forsendelsescontainere

Du bruger forsendelsescontainerposter til at identificere hver container, du bruger under fragt. Når du opretter en fragt, kan du vælge en bestemt container til den på listen over alle de forsendelsescontainerposter, du her har defineret. Denne funktion er især nyttig, hvis dit firma ejer egne forsendelsescontainere.

Du behøver ikke at angive forsendelsescontainernumre for forsendelsescontainere, der kun bruges én gang. Du kan i stedet tilføje forsendelsescontainernummeret, når du opretter en fragt.

Forsendelsescontainerposter bruges kun i Landingsomkostninger. De er ikke tilgængelige i standardmodulet **Transportstyring** (TMS).

Du kan arbejde med forsendelsescontainere ved at gå til **Landingsomkostninger \> Opsætning af containere \> Forsendelsescontainere**. Her kan du se, tilføje og fjerne poster for dine forsendelsescontainere. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Forsendelsescontainer | Angiv et entydigt id-navn/-nummer for forsendelsescontaineren. |
| Forsendelsescontainertype | Vælg typen af forsendelsescontainer. Yderligere oplysninger kan du se i afsnittet [Konfigurere forsendelsescontainertyper](#shipping-container-types) tidligere i dette emne. |

> [!NOTE]
> - Opsætningen af forsendelsescontaineren er valgfri. Du vil typisk kun bruge den, hvis dit firma ejer sine egne forsendelsescontainere eller ofte genbruger de samme forsendelsescontainere.
> - Der beregnes ingen kontrolcifre for forsendelsescontainernumre.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Konfigurere enhedstyper

Enhedstyper opretter yderligere grupperinger og identifikationsmetoder for forsendelsescontainere. Enhedstypen bruges typisk til at identificere den type container, som varer pakkes i, f.eks. paller eller tønder. Du kan vælge en enhedstype, når du konfigurerer en container på siden **Alle forsendelsescontainere**.

Enhedstyper bruges kun i Landingsomkostninger. De er ikke tilgængelige i TMS.

Du kan arbejde med enhedstyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Enhedstyper**. Her kan du se, tilføje og fjerne poster for dine enhedstyper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Enhedstype | Angiv et entydigt id-navn/-nummer for enhedstypen. |
| Beskrivelse | Angiv en beskrivelse af enhedstypen. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Definere afkølingstyper

Afkølingstyper opretter yderligere grupperinger og identifikationsmetoder for forsendelsescontainere (normalt afkølede containere). Du kan vælge en afkølingstype, når du konfigurerer en container på siden **Alle forsendelsescontainere**.

Du kan arbejde med afkølingstyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Afkølingstyper**. Her kan du se, tilføje og fjerne poster for dine afkølingstyper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Afkølingstype | Angiv et entydigt id-navn/-nummer for afkølingstypen. |
| Beskrivelse | Angiv en beskrivelse af afkølingstypen. |