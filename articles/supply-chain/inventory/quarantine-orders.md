---
title: Karantæneordrer
description: Dette emne beskriver, hvordan du bruger karantæneordrer til at blokere lagerbeholdning.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7676c6520fd7ed6e66dad11b23fae23f15ecba53c8bc4b62c193ee3643fb798e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718029"
---
# <a name="quarantine-orders"></a>Karantæneordrer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du bruger karantæneordrer til at blokere lagerbeholdning.

Du kan blokere lagerbeholdning ved hjælp af karantæneordrer. Det kan f.eks. være, at du vil sætte varer i karantæne af kvalitetskontrolmæssige årsager. Lager, der er blevet sat i karantæne, overføres til et karantænelagersted.

> [!NOTE]
> Hvis du anvender avancerede lagerstyringsprocesser (i Lagerstedsstyring), bruges karantæneordrebehandling kun til retursalgsordrer.

## <a name="quarantine-on-hand-inventory-items"></a>Sæt disponible lagervarer i karantæne

Når du sætter varer i karantæne, kan du enten oprette karantæneordrerne manuelt eller definere, at systemet skal oprette dem automatisk under indgående behandling.

Benyt følgende fremgangsmåde, hvis du vil konfigurere systemet til automatisk at generere karantæneordrer.

1. Gå til **Lagerstyring \> Opsætning \> Lagerbeholdning \> Varemodelgrupper**.
1. Vælg en relevant modelgruppe i listeruden, eller opret en ny modelgruppe.
1. I oversigtspanelet **Lagerpolitikker** skal du markere afkrydsningsfeltet **Karatænestyring**.
1. Luk siden.
1. Du skal angive et standardlagersted for karantænen i feltet **Karantænelagersted** for de modtagende lagersteder.

Når en vare, der er registreret som modtaget på lagerstedet, tilhører en modelgruppe, hvor afkrydsningsfeltet **Karantænestyring** er markeret, genererer systemet en karantæneordre for den. Karantæneordren beder arbejderne om at flytte varen til karantænelagerstedet.

Når du opretter karantæneordrer manuelt på siden **Karantæneordrer**, behøver varen ikke at være indstillet til karantænestyring i den tilknyttede varemodelgruppe. For denne proces skal du angive den disponible lagerbeholdning, der skulle sættes i karantæne, og det karantænelagersted, der skal bruges. Du kan bruge karantæneordrestatusser til at planlægge processen.

## <a name="quarantine-order-statuses"></a>Karantæneordrens status

Karantæneordrer kan have følgende statusværdier:

- Oprettet
- Startet
- Færdigmeldt
- Afsluttet

### <a name="created"></a>Oprettet

Når en karantæneordre er oprettet manuelt, men varen endnu ikke er på karantænelagerstedet, har karantæneordren statussen **Oprettet**. Der oprettes to lagerposteringer. Én transaktion er en afgangspostering, der kan have statussen **I bestilling**, **Reserveret fysisk** eller **Plukket**. Den anden transaktion er en tilgangspostering, der kan have statussen **Bestilt** eller **Registreret** på karantænelagerstedet. Du kan reservere, plukke og registrere opdateringer til lageret ved hjælp af de sædvanlige processer.

### <a name="started"></a>Startet

Når en karantæneordren har statussen **Startet**, overføres lageret fra det almindelige lagersted til karantænelagerstedet, og der genereres to lagerposteringer. Den ene postering har statussen **Trukket**, og den anden postering har statussen **Modtaget**. Samtidig oprettes der to lagertransaktioner til håndtering af tilbageflytningen. Disse transaktioner dateres ikke. Den ene postering har statussen **Reserveret fysisk**, og den anden postering har statussen **Bestilt**.

### <a name="reported-as-finished"></a>Færdigmeldt

Hvis du vil færdigmelde en igangsat karantæneordre, skal du åbne ordren og vælge **Færdigmeld** i handlingsruden. Varen frigives fra karantæne, men den er endnu ikke flyttet tilbage til det almindelige lagersted. Flytningen tilbage til det almindelige lagersted kan behandles via en varemodtagelseskladde, som kan initialiseres under færdigmeldingsprocessen.

### <a name="ended"></a>Afsluttet

Når en karantæneordre afsluttes, flyttes varen fra karantænelagerstedet tilbage til det almindelige lagersted. Status for varebevægelsen er angivet til *Solgt* på karantænelagerstedet og *Købt* på det almindelige lagersted.

## <a name="quarantine-order-scrap"></a>Kassering af karantæneordre

Du kan kassere lageret som en del af karantæneordreprocessen. Når du behandler en kassering, indstilles lagerstatus til *Solgt* med en afgangstransaktion fra karantænelagerstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Lagerblokering](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
