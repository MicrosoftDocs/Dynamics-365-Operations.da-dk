---
title: Administrere opdateringer af standardomkostninger
description: Opdateringer til standardomkostningsoplysninger kan administreres ved hjælp af to forskellige metoder – metoden med én version eller metoden med to versioner.
author: AndersGirke
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 166d12d707deabc59f7613a5016851b30fcc42d8
ms.sourcegitcommit: 41baf654a2553cfe5c715feb9cc03e48cfc12598
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024664"
---
# <a name="manage-standard-cost-updates"></a>Administrere opdateringer af standardomkostninger

[!include [banner](../includes/banner.md)]

Opdateringer til standardomkostningsoplysninger kan administreres ved hjælp af to forskellige metoder – metoden med én version eller metoden med to versioner.

Med metoden med én version bruges en enkelt efterkalkulationsversion, der indeholder alle omkostningsposter. Disse poster indeholder de oprindelige omkostninger og alle omkostningsopdateringer.

Med metoden med to versioner bruges én version, der indeholder posterne med de oprindelige omkostninger, og en anden version, der indeholder poster med alle omkostningsopdateringer. En væsentlig fordel ved metoden med to versioner er den klare fremstilling og sporing af omkostningsopdateringer i en særskilt efterkalkulationsversion, uden at den oprindelige efterkalkulationsversion påvirkes. Metoden med to versioner kan bruges til at identificere flere trinvise opdateringer, hvor de enkelte trinvise opdateringer har en særskilt efterkalkulationsversion, der indeholder de trinvise omkostningsposter.

## <a name="example"></a>Eksempel

I det følgende eksempel illustreres, hvordan metoderne med én version og to versioner kan bruges til opdatering af standardomkostninger i et produktionsmiljø. Det kan f.eks. være opdateringer, der afspejler nye varer eller fejlrettelser. Det antages, at en enkelt efterkalkulationsversion repræsenterer det aktuelle års standardomkostninger. Id'et for denne version er 2020-STD. Version 2020-STD indeholder de aktuelle aktive omkostninger for alle varer. Derudover indeholder den alle ruterelaterede omkostningskategorier og beregningsformler for indirekte omkostninger, som er kendt ved starten af år 2020. 2020-STD er den oprindelige efterkalkulationsversion.

- **Metoden med én version til opdateringer af omkostningsoplysninger** – I metoden med én version indeholder den oprindelige efterkalkulationsversion 2020-STD alle omkostningsposter. Omkostningsopdateringer registreres i 2020-STD og angives til status Afventer. De ventende omkostninger kan angives manuelt for nye købte varer, eller de kan beregnes for en produceret vare for at afspejle rettelser. Når metoden med én version bruges, kræver styklisteberegningerne ikke en reservedatakilde, da alle aktive omkostninger er indeholdt i efterkalkulationsversionen. Når de ventende omkostninger bliver aktive, indeholder den oprindelige efterkalkulationsversion 2020-STD igen alle de aktuelle aktive omkostninger.
- **Metoden med to versioner til opdateringer af omkostningsoplysninger** – I metoden med to versioner kræves en ekstra efterkalkulationsversion, der kun indeholder omkostningsopdateringerne. Id'et for denne version er 2020-STD-CHANGES. Omkostningsopdateringer registreres i 2020-STD-CHANGES og angives til status Afventer. I metoden med to versioner kræves en reservedatakilde til styklisteberegningerne af ventende omkostninger for producerede varer. Det skyldes, at den ekstra efterkalkulationsversion 2020-STD-CHANGES kun indeholder en delmængde af omkostningsoplysninger. Reservedatakilden kan udtrykkes som de aktive omkostninger eller som efterkalkulationsversionen 2020-STD, da begge identificerer kilden til omkostningsoplysninger, når de ikke er medtaget i 2020-STD-CHANGES. Når de ventende omkostninger bliver aktive, indeholder efterkalkulationsversionen 2020-STD-CHANGES de aktuelle aktive omkostninger, der afspejler opdateringerne, mens den oprindelige efterkalkulationsversion 2020-STD ikke påvirkes. Når metoden med to versioner bruges, skal der angives blokeringspolitikker for den oprindelige efterkalkulationsversion for at forhindre opdateringer. Der skal angives identiske blokeringspolitikker for den ekstra efterkalkulationsversion med undtagelse af den angivne fra-dato og den særlige brug af blokeringspolitikker, der tillader opdateringer. Den angivne fra-dato skal opdateres sammen med alle ændringsbatch for at afspejle den planlagte aktiveringsdato.

I dette eksempel er brugt én ekstra efterkalkulationsversion til at administrere opdateringer i hele år 2020. Der kan bruges mere end én ekstra efterkalkulationsversion, f.eks. en separat version til hver opdateringsbatch. Når der bruges mere end én ekstra efterkalkulationsversion, skal reservedatakilden udtrykkes som de aktive omkostninger, da de aktive omkostninger spredes ud over flere efterkalkulationsversioner.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Økonomiske dimensioner for standardomkostningsregulering

Aktivering af en ny standardpris vil typisk værdiregulere den disponible lagerbeholdning ud fra værdireguleringstransaktioner med standardomkostninger. Normalt bogføres varens økonomiske dimensioner på posteringerne. Men hvis du vil styre, om og hvordan de økonomiske dimensioner bogføres, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionen *Indstillinger for økonomiske dimensioner, der benyttes som standard for værdiregulering af lagerbeholdning til standardomkostninger*. Når du har aktiveret denne funktion, skal du gå til **Omkostningsstyring > Konfiguration af regnskabspolitik for lager > Parametre** og angive den nye rulleliste **Grundlaget for økonomiske dimensioner** til en af følgende værdier:

- **Ingen** – Der bogføres ingen økonomiske dimensioner på værdireguleringsposteringerne. Hvis din kontostruktur har en påkrævet økonomisk dimension, køres værdireguleringsprocessen stadig, men der oprettes regnskabsposter, som ikke har nogen økonomiske dimensioner. I dette tilfælde modtager brugerne en advarsel først, så de kan annullere værdireguleringen, hvis det er nødvendigt.
- **Tabel** – Normalt bogføres varens økonomiske dimensioner på værdireguleringsposteringerne. Dette er standardindstillingen og er i overensstemmelse med den oprindelige systemfunktionsmåde uden at deaktivere funktionen *Indstillinger for økonomiske dimensioner, der benyttes som standard for værdiregulering af lagerbeholdning til standardomkostninger*.
- **Bogføring** – De økonomiske dimensioner for den postering, der værdireguleres, bogføres på værdireguleringsposteringerne. De økonomiske dimensioner fra den oprindelige posterings lagerkonto bruges som standard til både beholdningskontoen og værdireguleringskontoen.
