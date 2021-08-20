---
title: Planlægning med negative disponible lagerantal
description: I dette emne beskrives, hvordan negative lagerbeholdninger håndteres, når du bruger planlægningsoptimering.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 97688e09aae9706dd85e7965aa08c7ea873a44d81391c39406e2e6367660e0d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758538"
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

Hvis du justerer lageret, mens der findes fysiske reservationer, kan du forårsage en situation, hvor en ordre fysisk reserveres mod negativt lager. Da der findes en fysisk reservation, antager Planlægningsoptimering i dette tilfælde, at den understøttes af en lagerbeholdning, selvom tilgangen af en lagerbeholdning endnu ikke er registreret i systemet. Det antages derfor, at der ikke kræves genopfyldning, og der ikke oprettes et ordreforslag til genopfyldning af ordreantallet.

Følgende eksempelscenarie illustrerer dette.

### <a name="example"></a>Eksempel

Systemet konfigureres på følgende måde:

- Produkt *FG* findes og har *10* stk. i disponibel lagerbeholdning.
- Produktkonfigurationen tillader fysisk negativt lager.
- Der findes en salgsordre på et antal af *10* stk. af produkt *FG*.
- Salgsordreantallet reserveres fysisk i forhold til den eksisterende disponible lagerbeholdning.

Du skal derefter justere antallet af produkt *FG*, så den disponible lagerbeholdning bliver 0 (nul). Da den disponible produktbeholdning er nul, reserveres salgsordreantallet nu til negativt lager. Men hvis du kører varedisponering nu, oprettes der ikke et ordreforslag til forsyning af salgsordren, da Planlægningsoptimering antager, at den påkrævede lagerbeholdning findes til forsyning af den fysiske reservation.

## <a name="related-resources"></a>Tilknyttede ressourcer

- [Oversigt over planlægningsoptimering](planning-optimization-overview.md)
- [Start her med planlægningsoptimering](get-started.md)
- [Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)
- [Få vist planhistorik og planlægningslogs](plan-history-logs.md)
- [Annullere et planlægningsjob](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
