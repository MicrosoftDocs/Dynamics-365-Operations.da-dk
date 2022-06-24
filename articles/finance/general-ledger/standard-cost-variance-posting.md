---
title: Bogføring af standardomkostningsafvigelse
description: Denne artikel giver oplysninger om opsætning af bogføringsprofiler for standardefterkalkulation.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894871"
---
# <a name="standard-cost-variance-posting"></a>Bogføring af standardomkostningsafvigelse

Når du bruger standardefterkalkulation for et eller flere produkter i organisationen, skal du konfigurere [forudsætningerne for standardefterkalkulation](/supply-chain/cost-management/prerequisites-standard-costs.md). Denne artikel forklarer de bogføringskonti, der kræves i trin 3 af forudsætningerne, "Tildele finanskonti til varebogføringer, der vedrører standardomkostningsafvigelser".

Der kan forekomme forskellige typer afvigelser for indkøbs- og produktionsordrer. Du kan se eksempler på produktionsafvigelser i [Almindelige kilder til produktionsafvigelser](/supply-chain/cost-management/common-sources-of-production-variances.md). Der opstår prisafvigelser i indkøbsordrer, når du bruger standardomkostninger for en købt vare, og der er forskel mellem produktets standardkostpris og det fakturerede beløb på indkøbsordren.

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfiguration af posteringsprofil

I følgende tabel vises eksempler på standardbogføringstyperne. Den viser eksempler på hovedkonti og beskrivelser.

- Kolonnen "Debet/Kredit?" angiver, om transaktionen typisk er et debet- eller kreditbeløb. I nogle tilfælde kan en transaktion enten bogføre et debet- eller kreditbeløb.
- I kolonnen "Clearingkonto" angives, at bogføringstypen er en clearingkonto. Det betyder, at det beløb, der bogføres på denne konto, automatisk tilbageføres, når en senere transaktion bogføres.
- I kolonnen "P/F" angives bogføringstypen. "P" repræsenterer fysisk bogføring, og "F" repræsenterer økonomisk bogføring.
- I kolonnen "Følg" angives, om hovedkontoen for bogføringstypen typisk er den samme som hovedkontoen for en anden bogføringstype. Den angiver specifikt den bogføringstype, der typisk bruges.

> [!NOTE]
> Hovedkonti og hovedkontonavne i tabellen er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Afvigelse i købspris | 510310 | Afvigelse i købspris | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er en afvigelse mellem købsprisen og standardkostprisen på en indkøbsordre. |
| Værdiregulering af lageromkostninger | 510330 | Værdiregulering af lageromkostninger | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der aktiveres en ny efterkalkulationsversion for en standardomkostningsvare for at værdiregulere lagerbeholdningen. |
| Ændring for omkostningsafvigelse | 510320 | Ændring for omkostningsafvigelse | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er forskel på standardomkostninger mellem lokationer, eller når en vare returneres, og der er en ændring mellem den oprindelige standardkostpris og den aktuelle standardomkostning for et produkt. |
| Afvigelse i produktionspartistørrelse | 510370 | Afvigelse i produktionspartistørrelse | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er forskelle mellem beregningsgrundlaget for styklisterne og det faktiske antal for omkostningsberegningen til produktionsordren. |
| Afvigelse i produktionspris | 510340 | Afvigelse i produktionspris | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er prisforskelle mellem forkalkuleret omkostning og de faktiske omkostninger for en produktionsordre. |
| Afvigelse i produktionsantal | 510350 | Afvigelse i produktionsantal | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er antalsforskelle mellem forkalkuleret omkostning og de faktiske omkostninger for en produktionsordre. |
| Afvigelse i produktionserstatning | 510360 | Afvigelse i produktionserstatning | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, når der er uventet forbrug på en produktionsordre. |
| Afvigelse i afrunding | 618160 | Afrundingsdifference | Udgift | Enten | Nej | F | Ikke relevant | Denne konto bruges, hvis der er en afrundingsdifference, når produktionsomkostningerne beregnes ud fra standardomkostningerne. |
