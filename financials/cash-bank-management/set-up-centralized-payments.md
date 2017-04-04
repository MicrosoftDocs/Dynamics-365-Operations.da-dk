---
title: Oprette centraliserede betalinger
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Oprette centraliserede betalinger



Følg disse trin for at forberede til at behandle betalinger i én juridisk enhed på vegne af andre juridiske enheder i organisationen. Før du begynder, skal være afsluttet følgende opsætning:

-   Opret juridiske enheder.
-   Definer finansparametre og kontoplaner.
-   Opret Kreditorparametre og Debitorparametre (afhængigt af de moduler, der bruger centraliserede betalinger).
-   Konfigurer mellemregning.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Konfigurere et organisationshierarki til centraliserede betalinger
Du skal konfigurere et organisationshierarki til centraliserede betalinger. Samme organisationshierarki bruges til at behandle centraliserede kreditorbetalinger og centraliserede debitorbetalinger. **Bemærk!** Til centraliserede betalinger er hierarkiets struktur underordnet. Enhver juridisk enhed i hierarkiet kan behandle betalinger på vegne af enhver anden juridisk enhed i hierarkiet. På siden **Organisationshierarkier** kan du oprette et nyt organisationshierarki.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Konfigurer en mellemregningskonto for centraliserede betalinger
Når betalingsposteringer i den aktuelle juridiske enhed udlignes mod fakturaer i andre juridiske enheder, oprettes de relevante skyldig til- og skyldig fra-posteringer for de enkelte juridiske enheder. Du skal angive den juridiske enhed, hvor alle gældende kontantrabatter og alle realiserede tab eller gevinster bogføres. Før du går i gang, skal du afgøre, hvilken juridisk enhed du vil bruge til behandling af kreditor- og debitorbetalinger. Hvis én juridisk enhed behandler kreditorbetalinger, mens en anden juridisk enhed behandler betalinger fra debitorer, skal du skifte mellem de enkelte juridiske enheder. På den **mellemregning** side, kan du vælge en intern relationspost for en juridisk enhed, du vil behandle betalinger på vegne af. På den **centraliserede betalinger** under fanen kan du vælge om du vil bogføre kontant rabatter til den juridiske enhed for betalingen (eller en anden postering, der reducerer saldoen på kreditorkontoen) eller den juridiske enhed for fakturaen (eller en anden postering, der øger saldoen for kreditorkontoen). Denne indstilling bruges sammen med feltet **Håndtering af kasserabat** på siderne **Kreditorparametre** og **Debitorparametre**. I forbindelse med tolerancer for overbetalinger og øredifferencer bruges indstillingen i betalingens juridiske enhed. I forbindelse med tolerancer for underbetalinger og øredifferencer bruges indstillingen i fakturaens juridiske enhed.

## <a name="map-vendor-accounts-across-legal-entities"></a>Tilknytte kreditorkonti på tværs af juridiske enheder
Hvis du betaler en kreditor fra én juridisk enhed, og du vil vælge fakturaer til denne kreditor i andre juridiske enheder, skal du sikre dig, at alle de tilsvarende kreditorkonti i de enkelte juridiske enheder alle bruger det samme adressekartoteks-id. Hvis du modtager en betaling fra en debitor, der betaler fakturaer i mere én juridisk enhed, skal du sikre dig, at de tilknyttede debitorkonti i de enkelte juridiske enheder alle bruger det samme adressekartoteks-id.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Konfigurere posteringsprofiler for centraliserede betalinger
Når du opretter en betaling i én juridisk enhed, der udligner fakturaer i andre juridiske enheder, skal posteringsprofil-id'erne være de samme i begge juridiske enheder. Du kan sikre, at betalingerne oprettes korrekt, ved i hver juridisk enhed til fakturaen at konfigurere en posteringsprofil i de enkelte fakturaers juridiske enheder, der svarer til de posteringsprofiler, der bruges i betalingens juridiske enhed. Skift til den første juridiske enhed for fakturaen, og klik på den **kreditorposteringsprofiler** side, kan du oprette en ny posteringsprofil eller redigere en eksisterende posteringsprofil. De valg, du foretager for posteringsprofilen i den juridiske enhed for fakturaen har ikke stemmer overens med opsætningen af posteringsprofilen i betalingens juridiske enhed.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Konfigurere betalingsmåder for centraliserede betalinger
Når du opretter en betaling i én juridisk enhed, der udligner fakturaer i andre juridiske enheder, skal betalingsmåde-id'erne være de samme i begge juridiske enheder. Du kan sikre, at betalingerne oprettes korrekt, ved i hver juridisk enhed af fakturaen at konfigurere en betalingsmåde, der svarer til de betalingsmåder, der bruges i betalingens juridiske enhed. Skift til den første juridiske enhed for fakturaen. På siden **Betalingsmåder **kan du derefter oprette en ny betalingsmåde eller redigere en eksisterende betalingsmåde. De indstillinger, du angiver for betalingsmåden i fakturaens juridiske enhed, behøver ikke at stemme overens med den måde, betalingsmåden er konfigureret på i betalingens juridiske enhed.

## <a name="set-up-default-descriptions"></a>Konfigurere standardbeskrivelser
Du kan definere standardbeskrivelser af interne udligningsbilag. Standardbeskrivelsen medtages i skyldig til- og skyldig fra-posteringer i løbet af udligningsprocessen på tværs af virksomheder. På siden **Standardbeskrivelser** kan du oprette nye beskrivelser til både **Intern kundeudligning **og **Intern kreditorudligning** ved at vælge et sprog og derefter indtaste teksten.


