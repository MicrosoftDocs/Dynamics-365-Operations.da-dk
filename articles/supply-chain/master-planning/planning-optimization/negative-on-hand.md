---
title: Planlægning med negative disponible lagerantal
description: I dette emne beskrives, hvordan negative lagerbeholdninger håndteres, når du bruger planlægningsoptimering.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: bb837a38485bad2b9b76a5e4f20d311c0281e192
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625380"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planlægning med negative disponible lagerantal

[!include [banner](../../includes/banner.md)]

Hvis systemet viser et negativt samlet disponibelt lagerantal, behandler planlægningsmotoren antallet som 0 (nul) for at undgå overforsyning. Funktionen fungerer på følgende måde:

1. Planlægningsoptimeringsfunktionen aggregerer de disponible antal i det laveste niveau af disponeringsdimensioner. (Hvis f.eks. *sted* ikke er en disponeringsdimension, aggregerer planlægningsoptimering antallet på *lagersteds*-niveau.)
1. Hvis det samlede disponible antal på det laveste niveau af disponeringsdimensionen er negativt, antager systemet, at den disponible mængde er 0 (nul).

> [!IMPORTANT]
> Planlægningssystemet kan være så præcist som inputdata. Hvis inputdataene er unøjagtige, vil negative poster i den disponible beholdning angive, at lageroplysningerne i Microsoft Dynamics 365 Supply Chain Management ikke er synkroniseret med den virkelige verden. Derfor vil planlægningsresultatet være fejlbehæftet. Hvis du vil have et præcist planlægningsresultat, skal du minimere antallet af poster, der viser et negativt antal.

## <a name="example-1"></a>Eksempel 1

Lagersted 13 er konfigureret på følgende måde:

- **Dækningskode:** Min./Maks.
- **Minimum:** 15 stk.
- **Maksimum:** 25 stk.

Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:

- **Sted 1, lagersted 13, sted 1** : 20 stk.
- **Sted 1 lagersted 13, sted 2:** &minus;8 stk.

Den samlede disponible beholdning for lagersted 13 er derfor 12 stk. (= 20 stk. &minus; 8 stk.).

I dette tilfælde bruger planlægningsprogrammet et samlet disponibelt antal på 12 stk. til lagersted 13.

Resultatet er en planlagt ordre på 13 stk. (= 25 stk. &minus; 12 stk.) til påfyldning af lagersted 13 fra 12 stk. til 25 stk.

## <a name="example-2"></a>Eksempel 2

Lagersted 13 er konfigureret på følgende måde:

- **Dækningskode:** Min./Maks.
- **Minimum:** 15 stk.
- **Maksimum:** 25 stk.

Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:

- **Sted 1, lagersted 13, sted 1** : 4 stk.
- **Sted 1 lagersted 13, sted 2:** &minus;8 stk.

Den samlede disponible beholdning for lagersted 13 er derfor &minus;4 stk. (= 4 stk. &minus; 8 stk.). Den er med andre ord mindre end 0 (nul).

I dette tilfælde antager planlægningsprogrammet, at den disponible beholdning for lagersted 13 er 0 stk. I stedet for &minus;4 stk.

Resultatet er en planlagt ordre på 25 stk. (= 25 stk. &minus; 0 stk.) til påfyldning af lagersted 13 fra 0 stk. til 25 stk.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Planlægge, når der er en reservation i forhold til negativ lagerbeholdning

Hvis du justerer lageret, mens der findes fysiske reservationer, kan du forårsage en situation, hvor en ordre fysisk reserveres mod negativt lager. I dette tilfælde skal du levere til dækning af det reserverede antal, da der findes en fysisk reservation. Derfor er opfyldning påkrævet, så systemet enten opretter et ordreforslag for at genopfylde det antal, der ikke kunne dækkes af den eksisterende disponible lagerbeholdning, eller dække det med en eksisterende ordre på varen.

Følgende eksempelscenarie illustrerer dette.

### <a name="example"></a>Eksempel

Systemet konfigureres på følgende måde:

- Produkt *FG* findes og har *10* stk. i disponibel lagerbeholdning.
- Produktkonfigurationen tillader fysisk negativt lager.
- Der findes en salgsordre på et antal af *10* stk. af produkt *FG*.
- Salgsordreantallet reserveres fysisk i forhold til den eksisterende disponible lagerbeholdning.

Du skal derefter justere antallet af produkt *FG*, så den disponible lagerbeholdning bliver 5. Da den disponible produktbeholdning er 5, reserveres salgsordreantallet nu i forhold til antal, der ikke er tilgængeligt i beholdningen (det ville være ens, hvis den disponible lagerbeholdning var 0. I så fald ville salgsordren blive reserveret mod negativt lager). Hvis du kører varedisponering nu, oprettes der planlagt ordre for antallet 5 for *FG* til forsyning af salgsordren, da Planlægningsoptimering altid anvender eksisterende lagerbeholdning eller opretter en ny planlagt ordre til at supplere den fysiske reservation.

## <a name="related-resources"></a>Tilknyttede ressourcer

- [Oversigt over planlægningsoptimering](planning-optimization-overview.md)
- [Start her med planlægningsoptimering](get-started.md)
- [Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)
- [Få vist planhistorik og planlægningslogs](plan-history-logs.md)
- [Annullere et planlægningsjob](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
