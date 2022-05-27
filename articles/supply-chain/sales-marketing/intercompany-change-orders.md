---
title: Ændre interne ordrer
description: Dette emne forklarer ændring af funktionen interne ordrer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 10efc397c64833785f286983987fd05854a69c0f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672900"
---
# <a name="change-intercompany-orders"></a>Ændre interne ordrer

[!include [banner](../../includes/banner.md)]

Hvis du ændrer en intern salgs- eller indkøbsordre, afspejles ændringen i den tilsvarende salgs- eller indkøbsordre i den tilsvarende virksomhed.

## <a name="adding-new-lines"></a>Tilføje nye linjer

Du kan føje nye linjer til en intern salgs- og indkøbsordre, hvis den oprindelige salgsordre er en del af den interne ordrekæde. Du kan også tilføje nye linjer, hvis den oprindelige salgsordre ikke er en direkte levering. Hvis den oprindelige salgsordre er en direkte levering, kan du kun føje nye ordrelinjer til den interne salgs- og indkøbsordre, hvis feltet **Tillad indirekte oprettelse** er valgt i oversigtspanelet **Interne indstillinger** i den oprindelige salgsordre.

## <a name="changing-prices-and-discounts"></a>Ændre priser og rabatter

Du kan ændre priserne og rabatterne, hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** er markeret på siden **Intern handel**.

Hvis du ændrer enhedsprisen på en eller flere eksisterende linjer i den interne salgsordrelinje, ændres enhedsprisen i den interne indkøbsordre også.

Hvis du ændrer et af rabatfelterne i den interne salgsordrelinje, opdateres de relevante rabatfelter i den interne indkøbsordre.

## <a name="changing-and-adding-new-charges"></a>Ændre og tilføje nye gebyrer

Du kan ændre gebyrerne, hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** er markeret på siden **Intern handel**.

Hvis du føjer et nyt gebyr til hovedet i den interne salgsordre og et nyt gebyr til den interne salgslinje, kopieres begge gebyrer til den interne indkøbsordre. Det samlede beløb er derfor det samme i den interne salgsordre og den interne indkøbsordre. Gebyrerne kopieres aldrig til den oprindelige salgsordre.

## <a name="copying-a-fee"></a>Kopiere et gebyr

Hvis du vil kopiere et gebyr til den oprindelige salgsordre, skal du oprette den som en ny salgslinje med varetypen **Service**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Ændre antal og slette linjer i interne indkøbs- og salgsordrer

Du kan kun ændre antallet eller slette en linje i en intern indkøbs- eller salgsordre, hvis linjen er oprettet direkte fra formen **Salgsordre** eller **Indkøbsordre**. Denne ændring gør den interne indkøbs- eller salgsordre eller de interne indkøbs- eller salgsordrelinjer til kilden.

## <a name="origins-of-orders-and-order-lines"></a>Ordrers og ordrelinjers oprindelse

Interne ordrer og ordrelinjer kan have en af følgende to oprindelser:

- **Afledt** – Ordren er oprettet automatisk fra en intern ordrekæde.
- **Kilde** – Ordren er oprettet manuelt af en bruger.

Oprindelsen angives i ordrehovedet til interne indkøbs- og salgsordrer i feltet **Oprindelig**. Dette felt findes i oversigtspanelet **Interne indstillinger** på salgsordren og i oversigtspanelet **Konfiguration** på indkøbsordren.

Oprindelserne **Afledt** og **Kilde** gælder kun for interne ordrer. Feltet **Oprindelig** er tomt for alle andre salgsordrer, indkøbsordrer og ordrelinjer. Feltet er også tomt i den oprindelige salgsordre.

## <a name="example-derived-origin"></a>Eksempel: oprindelsen Afledt

Du opretter en oprindelig salgsordre for en ekstern kunde. Denne salgsordre indeholder en ordrelinje. Denne oprindelige salgsordrer opretter en intern indkøbsordre, der indeholder en ordrelinje, som opretter en intern salgsordre, der indeholder en ordrelinje. Hovedet i den interne indkøbsordre og ordrelinjen oprettes automatisk ud fra den oprindelige salgsordre.

Værdien i feltet **Oprindelig** i oversigtspanelet **Konfiguration** til den interne indkøbsordre og oversigtspanelet **Interne indstillinger** til overskrifterne i de interne salgsordrer er **Afledte**. Værdien i feltet **Oprindelig** under fanen **Linjedetaljer** i indkøbsordre- og salgsordrelinjerne er også **Afledt**.

Hvis en ordrelinje har oprindelsen **Afledt**, kan du ikke slette ordrelinjen direkte. Du kan kun slette ordrelinjen fra den kilde, hvor ordrelinjen er oprettet. Du kan også kun ændre det bestilte antal fra den kilde, hvor ordrelinjen er oprettet.

Hvis en oprindelig salgsordre og en oprindelig salgsordrelinje er en del af den interne ordrekæde, kan du ændre de bestilte antal fra den oprindelige salgsordre, og du kan slette ordrelinjer fra den oprindelige salgsordre.

## <a name="example-source-origin"></a>Eksempel: oprindelsen Kilde

Du opretter en indkøbsordre for en intern kreditor. Den interne indkøbsordre og ordrelinje har begge oprindelsen **Kilde**. Denne interne indkøbsordre er derfor controlleren, og den interne salgsordre, der oprettes automatisk i kreditorvirksomheden, har oprindelsen **Afledt**.

De bestilte antal i en ordrelinje, som oprettes i den interne indkøbsordre, kan heller ikke ændres i den interne salgsordre. Ordrelinjen kan kun slettes fra den interne indkøbsordre. Hvis en ny linje føjes til den interne salgsordre, får den interne salgsordrelinje oprindelsen **Kilde**.

Når en oprindelig salgsordre er en del af den interne ordrekæde, kan du altid styre de interne ordrer og de interne ordrelinjer fra den oprindelige salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
