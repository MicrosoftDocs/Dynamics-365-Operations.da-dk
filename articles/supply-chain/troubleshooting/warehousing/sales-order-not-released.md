---
title: Salgsordre kunne ikke frigives med udgående lagersteds-ops
description: Der kan være flere årsager til, at du modtager en fejlmeddelelse om, at en salgsordre ikke kunne frigives. Denne side forklarer, hvorfor og hvordan du reducerer problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475919"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Salgsordre kunne ikke frigives med udgående lagersteds-ops

## <a name="symptoms"></a>Symptomer

Når du arbejder med udgående lagerstedshandlinger, kan du få vist følgende fejlmeddelelse:

> Salgsordren kunne ikke frigives.

## <a name="cause"></a>Årsag

Dette problem kan opstå af flere årsager. Ordren er f.eks. på kreditstyringshold, og der kan ikke oprettes forsendelser, før der angives en gyldig postadresse for alle salgslinjer, der er knyttet til en salgsordre. Alternativt er der et ordrehold, der skal håndteres, før ordren kan frigives til lagerstedet. Dette hold kan være ordrespecifikt, eller det kan være på kundekontoen.

## <a name="resolution"></a>Løsning

Tilføj eller opdater adressen på salgsordren og ordrelinjerne, og frigiv derefter ordren til lagerstedet. Ordrer kan kun frigives til lagerstedet, hvis de har en gyldig leveringsadresse (pr. adresseformatopsætningen i modulet **Organisationsadministration**).

Undersøg ordreholdet, og løs problemerne. Fjern derefter holdet fra ordren eller kunden, og frigiv ordren til lagerstedet.
