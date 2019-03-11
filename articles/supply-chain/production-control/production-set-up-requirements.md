---
title: Krav til produktionsopsætning
description: Denne artikel indeholder oplysninger om opsætningskrav, før du kan arbejde med Produktionsstyring.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b811c11271097f4bb7910c34f7775955abba526d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "366621"
---
# <a name="production-setup-requirements"></a>Krav til produktionsopsætning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om opsætningskrav, før du kan arbejde med Produktionsstyring. 

Produktionsstyring er integreret med funktioner i andre moduler. Denne integration giver dig mulighed for at ændre produktionsordrer og sikre, at de automatisk opdateres i alle andre relaterede processer og beregninger i systemet. Følgende opsætningsprocesser er angivet i den rækkefølge, du skal udføre dem i.

## <a name="required-baseline-setup-in-other-modules"></a>Nødvendig grundlæggende opsætning i andre moduler
Der skal angives oplysninger i andre moduler, før du kan arbejde i Produktionsstyring. Opsætningen omfatter følgende opgaver:

-   Opsætning af generelle firmaoplysninger.
-   Opsætning af finansmodulet.
-   Definition af varegrupper.
-   Opsætning af finanskonti for varegrupper.
-   Opsætning af lagervaretabellen i Lagerstyring.
-   Oprette styklister og styklisteversioner i Lagerstyring.

## <a name="required-calendar-and-resource-setup"></a>Krævet kalender- og ressourceopsætning
Før du bruger Produktionsstyring, skal du åbne Virksomhedsadministration og oprette og definere kalender- og operationsressourcer i følgende rækkefølge:

1.  **Arbejdstidsskabeloner** – Opret arbejdstidsskabeloner for at definere de tider, der er tilgængelige til produktionsplanlægning.
2.  **Kalendere** – Opret arbejdstidskalendere for at definere, hvilke dage i året der er tilgængelige for produktionsplanlægning.
3.  **Ressourcegrupper**– Opret ressourcegrupper til gruppering af operationsressourcer, så du kan få et overblik over eventuel ledig kapacitet, når du kører planlægning. Du behøver ikke at oprette ressourcegrupper, før du opretter operationsressourcer. Det anbefales dog, at du forstår, hvordan du kan gruppere ressourcer, når du konfigurerer Produktionsstyring.
4.  **Ressourcer** – Opret operationsressourcer for at definere de forskellige ressourcer, der skal bruges til at fuldføre produktionsprocessen og til at planlægge med henblik på kapacitet.

## <a name="required-production-parameters-setup"></a>Nødvendig opsætning af produktionsparametre
**Produktionsstyringsparametre** – Konfigurer grundlæggende produktionsparametre for at definere, hvordan systemet skal håndtere og behandle produktionsordrer. Angive, hvordan produktionsordrer oprettes, forkalkuleres, planlægges og forbruges. Du kan også vælge, hvilken form for feedback du ønsker, og hvordan omkostningsregnskabet skal udføres.

## <a name="required-journal-name-identification"></a>Nødvendigt id for kladdenavn
**Produktionskladdenavne** – Angiv de produktionskladdenavne, der bruges til at registrere og bogføre posteringer.

## <a name="setup-if-you-use-operations"></a>Opsætning, hvis du bruger operationer
Operationer repræsenterer de bestemte aktiviteter, der udføres for at producere færdigvaren. **Bemærk!** Du skal kende de aktivitetstyper, der er nødvendige for at producere varen, og rækkefølgen og prioriteter for disse aktiviteter. Du skal også vide, hvilke ressourcer der er involveret, og hvor mange.

1.  **Operationer** – Angiv parametre, der repræsenterer de opgaver, som skal udføres for at producere færdigvaren.
2.  **Relationer** – Opret operationsrelationer for at angive detaljerede egenskaber. Hvis du vil definere operationsrelationer, skal du klikke på **Relationer** på siden **Operationer**.

## <a name="setup-if-you-use-routes"></a>Opsætning, hvis du bruger ruter
Hvis du arbejder med ruter, skal der defineres operationer for hver produktionsrute, du opretter. Ruten repræsenterer den sti, varen følger fra operation til operation, lige fra starten af produktionsprocessen til slutningen.

1.  **Omkostningskategorier** – Opret omkostningsarter for at definere omkostningerne for hver time i de angive processer og opsætningstider.
2.  **Kostprisgrupper** – Definer omkostningsgrupper for at oprette og vedligeholde forskellige typer af efterkalkulationer.
3.  **Rutegrupper** – Opret rutegrupper for at definere parametre, der er relateret til rutegrupper. Du skal oprette rutegrupper, før du kan oprette produktionsruter.
4.  **Ruter** – Opret produktionsruter, og definer standardindstillinger for at styre planlægning, efterkalkulation og prissætning af ruteoperationer og for at køre rapportering.
5.  **Ruter** – Opret ruteversioner for at muliggøre varevariationer i produktionen.

## <a name="optional-advanced-settings"></a>Valgfrie avancerede indstillinger
1.  **Produktionsgrupper** – Opret produktionsgrupper for at angive relationer mellem produktionsordren og finanskontiene. Finanskontiene bruges til at bogføre eller gruppere ordrer til rapportering.
2.  **Produktionspuljer** – Opret produktionspuljer for at gruppere produktionsordrer til behandling af presserende produktionsordrer og for at slette og bogføre grupper af ordrer.
3.  **Egenskaber** – Definer egenskaber til at oprette specielle attributter, som du kan tildele ressourcer for at styre produktionsrækkefølgen. Disse attributter er forbundet til arbejdstidsskabelonen.




