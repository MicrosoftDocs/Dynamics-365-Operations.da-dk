---
title: Lagerstatusser
description: I denne artikel beskrives det, hvordan du kan bruge lagerstatus til at kategorisere og holde styr på lageret.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca9d3e4e15d11d2a9a1b531028de230ffc43913
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594596"
---
# <a name="inventory-statuses"></a>Lagerstatusser

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du kan bruge lagerstatus til at kategorisere og holde styr på lageret.

## <a name="set-up-and-use-inventory-statuses"></a>Konfigurere og bruge lagerstatusser

Du kan bruge lagerstatus til at kategorisere lager. Du kan derefter iværksætte foranstaltninger som genopfyldning eller læg-på-lager-arbejde.

Her er nogle eksempler på måder, du kan bruge lagerstatusser på:

- Oprette lagerstatusser for den disponible lagerbeholdning, indgående transaktioner og udgående transaktioner.
- Angive en standardlagerstatus for posteringer på lageret.
- Ændre en lagerstatus for varer før ankomst, ved ankomst, eller når varer lægges på lager ved lagerbevægelser.
- Bruge en lagerstatus til at prissætte varer, der returneres, og for at planlægge varedisponering.

En lagerstatus er en af dimensionerne i lagringsdimensionsgruppen. Lagerstatusser kan kategoriseres som disponible eller ikke-gængelige, og du kan bruge parameteren **Lagerspærring** til at spærre varer, der har en ikke-tilgængelig lagerstatus. Varer, der har status spærret, betragtes som fysiske lagervarer, og de kan ikke bruges i en produktionsordre, salgsordre, overflytningsordre eller udgående transaktion.

Du kan bruge lagerstedsvarer, der enten har disponibel eller ikke-disponibel lagerstatus for indgående arbejde. For eksempel skal du oprette en disponibel status, som hedder *Klar*, en ikke-tilgængelig status, som hedder *Beskadiget* og en spærret status, som hedder *Spærret*. Når du opretter en indkøbsordre for modtagne eller returnerede varer, og hvis nogle af varerne er beskadiget eller ødelagt, kan du ændre lagerstatus for varerne til *Beskadiget* på indkøbsordrelinjen. Når disse varer modtages, angives status automatisk til *Spærret*. Hvis du scanner de beskadigede varer ved hjælp af en mobilenhed, kan Supply Chain Management bruge placeringsinstruktioner og arbejdsskabeloner til at vise oplysninger om en passende placering eller en række placeringer, hvor du kan de lægge disse varer på lager. For returnerede varer oprettes afgangstypen *Reservation* på siden **Lagertransaktioner**.

Brug varer, der har lagerstatus disponibel, til udgående arbejde. Hvis du har varer med status *Ødelagt*, og der køres varedisponering på disse varer, anses varerne for manglende, og lageret genopfyldes automatisk.

Når du har oprettet lagerstatusser, kan du angive standardlagerstatus for et sted, vare og lagersted. Du kan også angive en standardstatus for salg, overdragelse og indkøbsordrer. Standardstatus for salgsordrer og udgående overflytningsordre kan ikke have indstillingen **Lagerspærring** angivet til *Ja*. Lagerstatus, der er nedarvet fra standardindstillinger for et websted, lagersted, vare, indkøbsordre, flytteordre eller salgsordre, kan ændres ved hjælp af den mobile enhed, eller på indkøbsordren, salgsordren eller flytteforslagslinjen.

For at planlægge dækningen for varer, der har status af disponibel lagerbeholdning, skal du vælge indstillingen **Disponer pr. dimension** for en lagerdimension på siden **Lagringsdimensionsgrupper**. Når du åbner guiden **Varedisponering**, vises varer med en disponibel status på siden **Status**. Du kan oprette disponeringsindstillinger for disse varer ved at vælge ID for lagerstatus for de disponible lagerstatusser. Baseret på disponeringsindstillingerne, kan du beregne varebehovene og budgettere udbud og efterspørgsel for tilgængelige varer under varedisponering. Du kan ikke oprette en opsætning af en varedisponering, der har spærret lagerstatus. Du kan også bruge siden **Varedisponering** til at oprette eller redigere disponeringsparametrene for varen.

## <a name="change-inventory-statuses"></a>Ændre lagerstatus

Du kan ændre lagerstatus enten ved hjælp af siden **Disponibel efter lokation** eller ved at bruge *Ændring af lagerstatus* som periodisk opgave.

- Når du bruger den periodiske opgave *Ændring af lagerstatus*, kan du vælge, hvilke poster der skal medtages, og angive, hvilken opgave der skal køres i batchen med det ønskede interval.
- Hvis du vil ændre lagerstatus som en ad hoc-proces, skal du gå til siden **Disponibel efter lokation**, vælge de relevante poster og derefter vælge knappen **Ændring af lagerstatus**.

> [!NOTE]
> Funktionen *Ændre lagerstatussen for varer, der styres af sporingsdimensioner* giver dig mulighed for at ændre lagerstatus for varer, der styres af sporingsdimensioner, herunder muligheden for kun at opdatere udvalgte poster. Brug [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionen efter behov. Når funktionen er aktiveret, kan du gøre følgende:
>
> - På siden **Disponibel efter lokation** kan du gruppere linjer baseret på de viste dimensioner ved hjælp af knappen **Vis dimensioner** og ændre status for de valgte linjer.
> - På siden **Disponibel efter lokation** kan du vælge flere poster og derefter bruge knappen **Ændring af lagerstatus** til at ændre dem alle på én gang.
> - I den periodiske opgave **Ændring af lagerstatus** kan du filtrere efter sporingsdimensioner.
