---
title: Warehouse Management-processer bruges i øjeblikket
description: Når du reserverer eller frigiver arbejde, kan du få vist en meddelelse om, at der aktuelt bruges Warehouse Management-processer. Løs problemet med et af disse trin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475856"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Du kan ikke reservere eller frigive arbejde, da der er processer i brug i øjeblikket

## <a name="symptoms"></a>Symptomer

Når du arbejder med separat fremstilling, vises følgende fejl:

> Warehouse Management-processer bruges i øjeblikket. Hvis der endnu ikke er registreret arbejdslinjer, kan du annullere det oprettede arbejde og eventuelle last- og forsendelseslinjer og derefter fortsætte pluk- eller forsendelsesprocessen.

## <a name="cause"></a>Årsag

Dette problem opstår, hvis du forsøger at reservere eller frigive arbejde for en linje, men lagertransaktionen har statussen *Plukket*, hvilket angiver, at materialet er plukket.

## <a name="resolution"></a>Løsning

Følg et af disse trin for at løse dette problem.

- Skift status for produktionsordren tilbage til *Forkalkuleret* eller *Frigivet*.
- Åbn detaljesiden for den relevante produktionsordre. I handlingsruden under fanen **Lagersted** i gruppen **Stop** skal du vælge **Stop og fortryd pluk** for at fortryde alle plukkede transaktioner. Vælg derefter **Fjern stop** for at behandle produktionsordren.

Her er en forklaring på funktionerne *Fortryd pluk* og *Stop*:
  
- **Fortryd pluk** – Denne funktion tilbagefører status for lagertransaktioner for styklistelinjer formellinjer, der har status fra *Plukket* til *I bestilling*. Når arbejdet for pluk af råmaterialer er fuldført, angives status for linjerne til *Plukket*. Denne status forhindrer, at produktionsordren nulstilles til statussen *Oprettet*. I dette tilfælde kan du bruge funktionen *Fortryd pluk* til at tilbageføre transaktionerne fra *Plukket* status og derefter nulstille produktionsordren til statussen *Oprettet*.
- **Stop** – Denne funktion angiver et **Stoppet** flag på produktionsordren for at forhindre enhver statusopdatering på ordren. Du kan finde flaget **Stoppet** i oversigtspanelet **Lagersted** på siden med oplysninger om produktionsordre.

> [!NOTE]
>
> - Knapperne kan kun ses, når produktionsordren er oprettet for varer, der er aktiveret til lagerprocesser.
> - **Stop**-gruppen kan kun ses under fanen **Lagersted** i handlingsruden på siden med oplysninger om produktionsordre. Den vises ikke i oversigtspanelet **Lagersted** på listesiden **Produktionsordrer**.
