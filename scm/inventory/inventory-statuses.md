---
title: Lagerstatusser
description: "I denne artikel beskrives det, hvordan du kan bruge lagerstatus til at kategorisere og holde styr på lageret."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Lagerstatusser

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du kan bruge lagerstatus til at kategorisere og holde styr på lageret.

Du kan bruge lagerstatus til at kategorisere lager. Du kan derefter iværksætte foranstaltninger som genopfyldning eller læg-på-lager-arbejde. 

Her er nogle eksempler på måder, du kan bruge lagerstatusser på:

-   Oprette lagerstatusser for den disponible lagerbeholdning, indgående transaktioner og udgående transaktioner.
-   Angive en standardlagerstatus for posteringer på lageret.
-   Ændre en lagerstatus for varer før ankomst, ved ankomst, eller når varer lægges på lager ved lagerbevægelser.
-   Bruge en lagerstatus til at prissætte varer, der returneres, og for at planlægge varedisponering.

En lagerstatus er en af dimensionerne i lagringsdimensionsgruppen. Lagerstatusser kan kategoriseres som disponible eller ikke-gængelige, og du kan bruge parameteren **Lagerspærring** til at spærre varer, der har en ikke-tilgængelig lagerstatus. Varer, der har status spærret, betragtes som fysiske lagervarer, og de kan ikke bruges i en produktionsordre, salgsordre, overflytningsordre eller udgående transaktion. 

Du kan bruge lagerstedsvarer, der enten har disponibel eller ikke-disponibel lagerstatus for indgående arbejde. For eksempel skal du oprette en disponibel status, som hedder **Klar**, en ikke-tilgængelig status, som hedder **Beskadiget** og en spærret status, som hedder **Spærret**. Når du opretter en indkøbsordre for modtagne eller returnerede varer, og hvis nogle af varerne er beskadiget eller ødelagt, kan du ændre lagerstatus for varerne til **Beskadiget **på indkøbsordrelinjen. Når disse varer modtages, angives status automatisk til **Spærret**. Hvis du scanner de beskadigede varer ved hjælp af en mobilenhed, kan Microsoft Dynamics 365 for Operations bruge lokationsvejledninger og arbejdsskabeloner til at vise oplysninger om en passende lokation eller en række lokationer, hvor du kan de lægge disse varer på lager. For returnerede varer oprettes afgangstypen **Reservation** på siden **Lagertransaktioner**. 

Brug varer, der har lagerstatus disponibel, til udgående arbejde. Hvis du har varer med status **Ødelagt**, og der køres varedisponering på disse varer, anses varerne for manglende, og lageret genopfyldes automatisk. 

Når du har oprettet lagerstatusser, kan du angive standardlagerstatus for et sted, vare og lagersted. Du kan også angive en standardstatus for salg, overdragelse og indkøbsordrer. Standardstatus for salgsordrer og udgående overflytningsordre kan ikke have indstillingen **Lagerspærring** angivet til **Ja**. Lagerstatus, der er nedarvet fra standardindstillinger for et websted, lagersted, vare, indkøbsordre, flytteordre eller salgsordre, kan ændres ved hjælp af den mobile enhed, eller på indkøbsordren, salgsordren eller flytteforslagslinjen. 

For at planlægge dækningen for varer, der har status af disponibel lagerbeholdning, skal du vælge indstillingen **Disponer pr. dimension** for en lagerdimension på siden **Lagringsdimensionsgrupper**. Når du åbner guiden **Varedisponering **, vises varer med en disponibel status på siden **Status**. Du kan oprette disponeringsindstillinger for disse varer ved at vælge ID for lagerstatus for de disponible lagerstatusser. Baseret på disponeringsindstillingerne, kan du beregne varebehovene og budgettere udbud og efterspørgsel for tilgængelige varer under varedisponering. Du kan ikke oprette en opsætning af en varedisponering, der har spærret lagerstatus. Du kan også bruge siden **Varedisponering** til at oprette eller redigere disponeringsparametrene for varen.




