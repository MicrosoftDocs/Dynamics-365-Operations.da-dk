---
title: Foretage fejlfinding af reservationer i lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773099"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Foretage fejlfinding af reservationer i lokationsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.

Se [Fejlfinde batch- og seriereservationshierarkier for lagersteder](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) for emner, der er relateret til batch- og serienummerregistreringer.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Jeg modtager fejlen "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, der er afhængig af reservationerne".

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke annullere lagerreservation på en salgslinje, fordi der er åbent arbejde i forhold til linjen.

### <a name="issue-resolution"></a>Problemløsning

Undersøg, om åbent pakkegruppearbejde findes for at bringe varen fra en pakkestation til et andet sted (f.eks. *Lagerport*). Gennemse posterne på siden **Historik for oprettelse af arbejde** og **Arbejdsdetaljer** for at bestemme, hvad der fysisk reserverer lageret, og fuldfør eller slet derefter arbejdet for at frigøre reservationen.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Jeg modtager følgende fejlmeddelelse: "Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2...."

### <a name="issue-description"></a>Problembeskrivelse

Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner. Her er hele teksten i den fulde fejlmeddelelse:

> Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2 med dimensionsstørrelse=%3, farve=%4, tillæg=%5, sted=%6, lagersted=%7, lokation=%8, lagerstatus=tilgængelig, nummerplade=%9, batchnummer=%10 for reference-id %11 på parti-id %12.

### <a name="issue-resolution"></a>Problemløsning

Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet. Disse transaktioner kan f.eks. have åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Jeg får vist følgende fejlmeddelelse: "Fysisk beholdning...kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret".

### <a name="issue-description"></a>Problembeskrivelse

Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner. Her er hele teksten i den fulde fejlmeddelelse:

> Fysisk disponibel sted=%1, lagersted=%2, lagerstatus=tilgængelig, batchnummer=%3, ejer=%4: %5 kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret.

### <a name="issue-resolution"></a>Problemløsning

Dette problem skyldes sandsynligvis åbent arbejde. Du skal enten fuldføre arbejdet eller modtage uden arbejdsoprettelse. Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet. Disse transaktioner kan f.eks. være åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
