---
title: Ændre eller slette en oprindelig intern salgsordre
description: I dette emne forklares det, hvordan du kan ændre og slette en oprindelig salgsordrefunktionalitet
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548168"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Ændre eller slette en oprindelig intern salgsordre

[!include [banner](../../includes/banner.md)]

Når du ændrer en salgsordre, synkroniseres ændringerne automatisk med både den relevante interne indkøbsordre og den interne salgsordre.

> [!NOTE]
> Indkøbsordrer for eksterne leverandører påvirkes ikke af de ændringer, du foretager, og det gør de oprindelige salgsordrelinjer, der er tilknyttet indkøbsordrelinjerne for eksterne leverandører, heller ikke.

I følgende tabel opsummeres de ændringer, du kan foretage, og de forventede resultater.

| Operation | Resultat |
|---|---|
| Slette&nbsp;en&nbsp;oprindelig&nbsp;salgsordre. | Den relaterede interne indkøbsordre og den interne salgsordre slettes også. Hvis ordrens status er **Plukliste**, eller hvis salgsordren er nået længere i processen, kan salgsordrelinjen ikke slettes. |
| Slette en oprindelig salgsordrelinje. | Den relaterede interne indkøbsordrelinje og den interne salgsordrelinje slettes. Hvis ordrens status er **Plukliste**, eller hvis salgsordren er nået længere i processen, kan salgsordrelinjen ikke slettes. |
| Føje en ny salgsordrelinje til en oprindelig salgsordre. | Den nye salgslinje oprettes både på den interne indkøbsordre og den interne salgsordre. |
| Ændre antal på en oprindelig salgsordrelinje. | Antallet synkroniseres med både den interne indkøbsordrelinje og den interne salgsordrelinje. Nettobeløbet genberegnes for alle ordrerne. |
| Deaktivere direkte levering på en oprindelig salgsordre. | Du kan ikke redigere feltet **Direkte levering** på den oprindelige salgsordre, hvis den interne salgsordrelinje har nået minimumsstatus for **plukliste**, **outputordre** eller **pluklistekladde**. Leveringsadressen på den interne indkøbsordre ændres til standardleveringsadressen (standardleveringsadressen til indkøbsordren). De interne indkøbsordrelinjer ændres også til den leveringsadresse, der er standard for linjerne. De synkroniseres begge med den interne salgsordre og linjerne. Leveringstypen på alle linjerne i den oprindelige salgsordre ændres til **Ingen**, og feltet synkroniseres med de interne indkøbsordrelinjer. Indkøbsordrerne for eksterne leverandører påvirkes ikke, og det gør de oprindelige salgsordrelinjer, der er tilknyttet indkøbsordrelinjerne for eksterne leverandører, heller ikke. Leveringsdatoen på den interne indkøbsordre og linjerne – samt datoerne for ønsket modtagelse/afsendelse på den interne salgsordre og linjerne – opdateres. |
| Aktivere direkte levering på en oprindelig salgsordre. | Du kan ikke redigere feltet **Direkte levering** på den oprindelige salgsordre, hvis den interne salgsordrelinje har nået minimumsstatus for **plukliste**, **outputordre** eller **pluklistekladde**. Leveringsadressen på den interne indkøbsordre ændres til leveringsadressen fra den oprindelige salgsordre og synkroniseres med den interne salgsordre. Leveringstypen på alle linjerne i den oprindelige salgsordre ændres til **Direkte levering**, og feltet synkroniseres med de interne indkøbsordrelinjer. Leveringsadressen på hver af de oprindelige salgsordrelinjer synkroniseres med både de interne indkøbsordrelinjer og de interne salgsordrelinjer. Leveringsdatoen på den interne indkøbsordre og linjerne – samt datoerne for ønsket modtagelse/afsendelse på den interne salgsordre og linjerne – opdateres. |
| Føje en note til både en oprindelig salgsordreoverskrift og linjerne. | Noten kopieres til den interne indkøbsordre og den interne salgsordre. |
| Ændre eller slette en note. | Hvis du ændrer eller sletter en note, ændres eller slettes den tilsvarende note på den interne indkøbsordre og den interne salgsordre også. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
