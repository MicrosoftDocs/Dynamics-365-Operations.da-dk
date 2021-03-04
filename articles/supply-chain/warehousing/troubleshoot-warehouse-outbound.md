---
title: Foretage fejlfinding af udgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med udgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645430"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Foretage fejlfinding af udgående lagerstedsoperationer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med udgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Jeg får vist følgende fejlmeddelelse: "Salgsordren kunne ikke frigives".

### <a name="issue-description"></a>Problembeskrivelse

Dette problem kan opstå af flere årsager. Ordren er f.eks. på kreditstyringshold, og der kan ikke oprettes forsendelser, før der angives en gyldig postadresse for alle salgslinjer, der er knyttet til en salgsordre. Alternativt er der et ordrehold, der skal håndteres, før ordren kan frigives til lagerstedet. Dette hold kan være ordrespecifikt, eller det kan være på kundekontoen.

### <a name="issue-resolution"></a>Problemløsning

Tilføj eller opdater adressen på salgsordren og ordrelinjerne, og frigiv derefter ordren til lagerstedet. Ordrer kan kun frigives til lagerstedet, hvis de har en gyldig leveringsadresse (pr. adresseformatopsætningen i modulet **Organisationsadministration**).

Undersøg ordreholdet, og løs problemerne. Fjern derefter holdet fra ordren eller kunden, og frigiv ordren til lagerstedet.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Jeg får vist følgende meddelelse: "Forsendelsen for lasten 1% er bekræftet". Der bogføres dog ingen linjer.

### <a name="issue-description"></a>Problembeskrivelse

En forsendelse på en last blev bekræftet, men der opstod ikke en efterfølgende bogføring.

### <a name="issue-resolution"></a>Problemløsning

Forsendelsesbekræftelse påvirker ikke bogføringen. Den opdaterer blot status for afsendelse og last. Bogføring skal finde sted i en separat proces.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Jeg får vist følgende fejlmeddelelse: "Direkte levering kan ikke behandles for lagersted 1%, da lokationsstyring er aktiveret. Angiv et andet lagersted, der ikke er aktiveret til lokationsstyring."

### <a name="issue-description"></a>Problembeskrivelse

En vare føjes til en salgslinje til direkte levering fra et lagersted, der er aktiveret til lokationsstyring (WMS). Du får vist denne fejlmeddelelse, når salgslinjen opdateres. 

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. I øjeblikket understøtter WMS ikke direkte levering. Hvis du derfor vil bruge direkte levering, skal du vælge en ikke-WMS-vare og et lagersted.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]