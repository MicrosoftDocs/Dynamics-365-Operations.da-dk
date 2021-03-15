---
title: Foretage fejlfinding af lastopbygning og forsendelser
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lastopbygning og forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
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
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994023"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Foretage fejlfinding af lastopbygning og forsendelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lastopbygning og forsendelser i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Jeg får vist følgende fejlmeddelelse: "Du kan ikke oprette en lastlinje for denne ordrelinje, fordi den indeholder lagerdimensioner, der er ugyldige..."

### <a name="issue-description"></a>Problembeskrivelse

Du får vist følgende fejlmeddelelse, når du forsøger at frigive en retursalgsordre til lagerstedet:

> Du kan ikke oprette en lastlinje for denne ordrelinje, fordi den indeholder lagerdimensioner, der er ugyldige. Du kan ikke referere til lagerdimensioner, der findes under lokationsdimensionen i reservationshierarkiet. Fjern de ugyldige dimensioner fra ordrelinjen.

### <a name="issue-resolution"></a>Problemløsning

Desværre understøtter produktet ikke lastbehandling af en salgsreturproces. Derfor kan du ikke frigive retursalgsordren til lagerstedet.

På salgsordretransaktioner kan du ikke referere til lagerdimensioner, der findes under dimensionen **Lokation** i reservationshierarkiet. Løsningen er at fjerne de ugyldige dimensioner fra ordrelinjen.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Jeg får vist følgende fejlmeddelelse: "En af linjerne er allerede på en last. Kan ikke frigive til lagersted".

### <a name="issue-description"></a>Problembeskrivelse

Hvis du opretter laster manuelt, eller hvis du konfigurerer processen, så der allerede er oprettet laster før indtastning af salgsordrelinjer, forudsættes det, at den efterfølgende frigivelse udføres manuelt, og at ruten og vurderingen fra lasten vil blive anvendt.

I et andet muligt scenario forsøger du at foretage automatisk frigivelse til lagerstedet, men bølgeprocessen kunne ikke oprette arbejde. Derfor oprettes der stadig en åben forsendelse eller last. Denne åbne forsendelse eller last blokerer derefter efterfølgende forsøg på automatisk at frigive ordren, indtil du enten sletter den åbne forsendelse eller last eller manuelt genbehandler bølgen.

### <a name="issue-resolution"></a>Problemløsning

Du kan frigive fra salgsordresiden, eller automatisk frigivelse kan udføres fra siden Frigiv salgsordre, hvis der ikke findes en last før frigivelsen til lagerstedet. Lasten oprettes automatisk, når bølgen er behandlet.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Jeg får vist følgende fejlmeddelelse: "Ændringen af følgeseddel kan ikke behandles. Følgeseddel indeholder kun varer, der er underlagt lokationsstyringsprocesser, da disse ikke understøttes af korrektion af følgeseddel".

### <a name="issue-description"></a>Problembeskrivelse

Når du har bogført en følgeseddel, kan du ikke annullere den, fordi knappen **Annuller** ikke er tilgængelig. Du kan heller ikke rette følgesedlen. Hvis du forsøger, får du vist denne fejlmeddelelse.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for avanceret lokationsstyring (WMS), skal bogføringen ske fra lasten, ikke direkte fra ordren.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Hvordan kan jeg oprette arbejde ud fra udgående laster i stedet for bølger?

### <a name="issue-description"></a>Problembeskrivelse

Her er en måde at genskabe dette problem på.

1. Opret en udgående last ved hjælp af en salgsordre eller flytteordre.
2. Frigiv lasten til lagerstedet.
3. Bemærk, at der endnu ikke er genereret noget plukarbejde.

### <a name="issue-resolution"></a>Problemløsning

Hvis arbejdet skal genereres med det samme, når lasten frigives, skal du konfigurere bølgeskabelonen i overensstemmelse hermed. Angiv følgende indstillinger til *Ja* på bølgeskabelonen:

- Automatiser bølgeoprettelse
- Udfør behandling af bølgen ved frigivelse til lagerstedet
- Automatiser frigivelse af bølge

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Jeg kan ikke frigive en delvist leveret last igen.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke frigive en delvist leveret last til lagerstedet. Når du foretager frigivelsen til lagerstedet, vises meddelelsen "Handlingen er fuldført", men der sker ingenting, og der oprettes ikke noget arbejde for det resterende antal. Dette problem opstår, når du bruger funktionaliteten til transport af last, og der er en ufuldstændig reservation.

### <a name="issue-resolution"></a>Problemløsning

[KB-fejl 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Delvist leverede laster kan få ny bølge og genbehandles") er løst [version 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]