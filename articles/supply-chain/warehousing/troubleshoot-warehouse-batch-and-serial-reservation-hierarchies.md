---
title: Fejlfinde batch- og seriereservationshierarkier for lagersteder
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med reservationshierarkier, der bruger batch- eller seriedimensioner.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838172"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Fejlfinde batch- og seriereservationshierarkier for lagersteder

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med reservationshierarkier, der bruger batch- eller seriedimensioner.

Du kan finde flere oplysninger under [Fleksibel reservationspolitik for dimension på lagerstedsniveau](flexible-warehouse-level-dimension-reservation.md).

Reservationshierarkiet for en vare angiver behovet for lagringsdimensioner, der skal opfyldes, for at der kan knyttes en lokation til en behovsordre. Disse dimensioner kan beskrives som *dimensioner over lokation* for alle de dimensioner, der skal opfyldes, før lokationen tildeles, og *dimensioner under lokation* for dimensioner, der kan tildeles, når der er tildelt en lokation til behovsordren. Disse reservationshierarkier kaldes også *batch over*- og *batch under*-reservationshierarkier eller *serie over*- og *serie under*-reservationshierarkier.

Lageret kan kun fordeles, hvis der ikke er huller i dimensionerne over lokationen. I et *batch over*-reservationshierarki kan du f.eks. forvente, at dimensionerne **Lokation**, **Lagersted** og **Batchnummer** angives i behovsordren. Hvis nogen af disse dimensioner mangler, mislykkes fordelingsprocessen. Modsat kan der i et *batch under*- eller *serie under*-reservationshierarki angives et batch- eller serienummer på behovsordren, men det kræver fordelingsprocessen ikke.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Jeg får vist følgende fejlmeddelelse: "For at blive tildelt en bølge skal lastlinjer angive dimensionerne over lokationen. Du kan tildele disse dimensioner ved at reservere og genoprette lastlinjen".

### <a name="issue-description"></a>Problembeskrivelse

Når du bruger en vare, der har et *batch over*-reservationshierarki, vil kommandoen **Frigiv til lagersted** på siden **Panelet Lastplanlægning** ikke fungere, hvis du prøver at frigive en last for en delmængde. Du får vist denne fejlmeddelelse, og der oprettes ikke noget arbejde for delmængden.

Men, hvis du bruger en vare, der har et *batch under*-reservationshierarki, kan du frigive en last for en delmængde fra siden **Panelet Lastplanlægning**.

### <a name="issue-cause"></a>Problemårsag

Når en dimension er over **Lokation**-dimensionen i reservationshierarkiet, skal den angives før frigivelsen til lagerstedet. Delmængder kan ikke frigives, hvis en eller flere dimensioner over **Lokation** ikke er angivet.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Prompten til automatisk reservation af et batchnummer udløses, selvom der er tilgængelig lagerbeholdning.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruger en vare, der har et *batch over*-reservationshierarki på et lagersted, hvor der ikke er aktiveret lagerstedsprocesser, og automatisk reservation er aktiveret, vises prompten for automatisk reservation af et batchnummer, også selvom der kun er ét tilgængeligt batch til plukning.

Men når du bruger den samme vare på et lagersted, hvor lagerprocesser er aktiveret, vises prompten for automatisk reservation ikke.

### <a name="issue-cause"></a>Problemårsag

Hvis et reservationshierarki defineres som *batch over* eller *serie over*, skal den dimension, der refereres til (**Batchnummer** eller **Serienummer**), altid angives ved behovsordrer. Lagerstedsprocesserne kan muligvis fuldføre oplysningerne, hvis der er et enkelt batch- eller serienummer tilgængeligt. Men da lagerstedet ikke er aktiveret for lagerstedsprocesser, skal brugeren altid angive alle dimensionerne over **Lokation**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Allokeringsskabeloner med Overvej beholdning som kriterium tager ikke den aktuelle disponible lagerbeholdning i betragtning for batchaktiverede varer.

Du kan finde flere oplysninger under [Lagerstedsallokering](warehouse-slotting.md).

### <a name="issue-description"></a>Problembeskrivelse

Allokeringsskabeloner med *Overvej beholdning* som kriterium tager ikke den aktuelle disponible lagerbeholdning i betragtning for *batch over*-varer. De tager kun højde for det, hvis batchnummeret er angivet på salgsordrelinjen.

Men når du bruger *batch under*-varer, anses den aktuelle lagerbeholdning for at være forventet.

### <a name="issue-cause"></a>Problemårsag

Hovedet til allokeringsskabelonen kan defineres for behovsstrategien *Bestilt*, *Reserveret* eller *Frigivet*. I strategien *Bestilt* gælder de samme reservationshierarkikrav, der gælder for reservation eller frigivelse til lagerprocesser. Derfor skal der for *batch over*- og *serie under*-reservationshierarkier angives batch- eller serienummer på behovsordren (salg eller flytning). Du kan også bruge behovsstrategien *Reserveret* til at vælge batch- eller serienummer, før der genereres behov for lagerstedsallokering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
