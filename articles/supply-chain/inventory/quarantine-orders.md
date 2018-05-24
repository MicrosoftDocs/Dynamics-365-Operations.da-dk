---
title: "Karantæneordrer"
description: "I dette emne beskrives, hvordan karantæneordrer bruges til at blokere for lager."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9a05c35d2e4a9e3ad81421eac863d182e8a6b499
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="quarantine-orders"></a>Karantæneordrer

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan karantæneordrer bruges til at blokere for lager.

Karantæneordrer kan bruges til at blokere lager. Det kan f.eks. være, at du vil sætte varer i karantæne af kvalitetskontrolmæssige årsager. Lager, der er blevet sat i karantæne, overføres til et karantænelagersted. **Bemærk!** Hvis du anvender avancerede lagerstyringsprocesser (i Lagerstedsstyring), bruges karantæneordrebehandling kun til retursalgsordrer.

## <a name="quarantine-on-hand-inventory-items"></a>Sæt disponible lagervarer i karantæne
Når du sætter varer i karantæne, kan du enten oprette karantæneordrerne manuelt eller definere, at systemet skal oprette karantæneordrer automatisk under indgående behandling. Du kan oprette karantæneordrer automatisk ved at vælge indstillingen **Karantænestyring** under fanen **Lagerpolitikker** på siden **Varemodelgrupper**. Du skal også angive et standardkarantænelagersted i feltet **Karantænelagersted** for de modtagende lagersteder. Når den fysisk disponible lagerbeholdning bliver registreret i en indkøbsordre eller produktionsordre, flyttes varerne i karantæne automatisk til et karantænelagersted i Microsoft Dynamics 365 for Finance and Operations. Denne bevægelse opstår, fordi status for karantæneordren ændres til **Startet**. Når du opretter karantæneordrer manuelt, behøver varen ikke at være sat op til karantænestyring i den tilknyttede varemodelgruppe. For denne proces skal du angive den disponible lagerbeholdning, der skulle sættes i karantæne, og det karantænelagersted, der skal bruges. Du kan bruge karantæneordrestatusser til at planlægge processen.

## <a name="quarantine-order-statuses"></a>Karantæneordrens status
Karantæneordrer kan have følgende statusværdier:

-   Oprettet
-   Startet
-   Færdigmeldt
-   Afsluttet

### <a name="created"></a>Oprettet

Når en karantæneordre er oprettet manuelt, men varen endnu ikke er på karantænelagerstedet, har karantæneordren statussen **Oprettet**. Der oprettes to lagerposteringer. Én transaktion er en afgangspostering, der kan have statussen **I bestilling**, **Reserveret fysisk** eller **Plukket**. Den anden transaktion er en tilgangspostering, der kan have statussen **Bestilt** eller **Registreret** på karantænelagerstedet. Du kan reservere, plukke og registrere opdateringer til lageret ved hjælp af de sædvanlige processer.

### <a name="started"></a>Startet

Når en karantæneordren har statussen **Startet**, overføres lageret fra det almindelige lagersted til karantænelagerstedet, og der genereres to lagerposteringer. Den ene postering har statussen **Trukket**, og den anden postering har statussen **Modtaget**. Samtidig oprettes der to lagertransaktioner til håndtering af tilbageflytningen. Disse transaktioner dateres ikke. Den ene postering har statussen **Reserveret fysisk**, og den anden postering har statussen **Bestilt**.

### <a name="reported-as-finished"></a>Færdigmeldt

Hvis du klikker på **Færdigmeld**, kan du færdigmelde en igangsat karantæneordre. Varen frigives fra karantæne, men den er endnu ikke flyttet tilbage til det almindelige lagersted. Flytningen tilbage til det almindelige lagersted kan behandles via en varemodtagelseskladde, som kan initialiseres under færdigmeldingsprocessen.

### <a name="ended"></a>Afsluttet

Når en karantæneordre afsluttes, flyttes varen fra karantænelagerstedet tilbage til det almindelige lagersted. Status for varebevægelsen er angivet til **Solgt** på karantænelagerstedet og **Købt** på det almindelige lagersted.

## <a name="quarantine-order-scrap"></a>Kassering af karantæneordre
Du kan kassere lageret som en del af karantæneordreprocessen. Når du behandler en kassering, indstilles lagerstatus til **Solgt** med en afgangspostering fra karantænelagerstedet.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Lagerblokering](inventory-blocking.md)

