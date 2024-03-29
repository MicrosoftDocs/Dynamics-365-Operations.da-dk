---
title: Udskudt behandling af lagerstedsarbejde
description: Denne artikel beskriver de funktioner, der gør udskudt behandling af lagerstedets læg på lager-handlinger tilgængelig i Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f4eeea0805c2cecedbd6b42926191ab02022df9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899289"
---
# <a name="deferred-processing-of-warehouse-work"></a>Udskudt behandling af lagerstedsarbejde

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de funktioner, der gør udskudt behandling af lagerstedets læg på lager-handlinger tilgængelig i Dynamics 365 Supply Chain Management.

Med den udskudte behandlingsfunktion kan lagermedarbejderne fortsætte med at udføre andet arbejde, mens læg på lager-operationen behandles i baggrunden. Udskudt behandling er nyttig, når mange arbejdslinjer skal behandles, og arbejderen kan lade dette arbejde blive behandlet asynkront. Det er også nyttigt, når serveren kan have ad hoc eller ikke-planlagte stigninger i behandlingstiden, og den øgede behandlingstid kan påvirke brugerens produktivitet.

Baggrundsbehandling opnås ved hjælp af SysOperations-strukturen. Du kan finde flere oplysninger under [Oversigt over SysOperation-struktur](/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Konfiguration af politikker for arbejdsbehandling

Hvis du vil bruge udskudt behandling, skal du konfigurere og bruge en arbejdsbehandlingspolitik.

Politikker konfigureres på siden **Politikker for arbejdsbehandling**. I følgende tabel forklares felterne på siden.

| Felt                           | Beskrivelse |
|---------------------------------|-------------|
| Navn på politik for arbejdsbehandling     | Navnet på arbejdsbehandlingspolitikken. |
| Arbejdsordretype                 | Den arbejdsordretype, som politikken anvendes på. |
| Handling                       | Den handling, der behandles ved hjælp af politikken. |
| Arbejdsbehandlingsmetode          | Den metode, der bruges til at behandle arbejdslinjen. Hvis metoden er indstillet til **Øjeblikkelig**, ligner funktionsmåden den, der bruges, når ingen databehandlingspolitikker bruges til at behandle linjen. Hvis metoden er indstillet til **Udskudt**, bruges udskudt behandling, der bruger batchstrukturen. |
| Tærskel for udskudt behandling   | En værdi på **0** (nul) angiver, at der ikke er en tærskel. I dette tilfælde bruges udskudt behandling, hvis den kan bruges. Hvis den specifikke tærskelberegning er under tærsklen, anvendes metoden Øjeblikkelig. Ellers bruges den udskudte metode, hvis den kan bruges. For salgs- og overførselsrelateret arbejde beregnes tærsklen som antallet af tilknyttede kildelastlinjer, der behandles for arbejdet. For genopfyldningsarbejde beregnes tærsklen som antallet af arbejdslinjer, der genopfyldes af arbejdet. Ved at sætte en tærskel på for eksempel **5** for salg, vil mindre arbejde, der har færre end fem oprindelige kildebelastningslinjer, ikke bruge udskudt behandling, men større arbejde vil bruge den. Tærsklen har kun virkning, hvis arbejdsbehandlingsmetoden er indstillet til **Udskudt.** |
| Batchgruppe for udskudt behandling |Den batchgruppe, der bruges til behandling. |

Ved udskudt put-behandling understøttes følgende typer af arbejdsordre: salgsordre, problem med overførsel af ordre og genopfyldning.

## <a name="assigning-the-work-creation-policy"></a>Tildeling af politikken for oprettelse af arbejde

Politikken for oprettelse af arbejde kan tildeles i lokationsstyringsparametrene. Den kan også tildeles på niveau for de enkelte lagersteder. Hvis politikken er tildelt et lagersted, anvendes den kun på det arbejde, der er oprettet for det pågældende lagersted. Hvis der ikke er tildelt en politik på lagerstedsniveau, anvendes politikken fra lokationsstyringsparametrene.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Visning af udskudte Læg på lager-behandlingsopgaver

Du kan få vist udskudte Læg på lager-behandlingsopgaver på siden **Udskudte Læg på lager-behandlingsopgaver**.

Som standard vises de **fuldførte** opgaver.

| Felt            | Beskrivelse |
|------------------|-------------|
| Status           | Status for opgaven. |
| Status for batchjob | Status for det relaterede batchjob. Hvis batchjobbet er blevet behandlet, indeholder batchhistorikken loggen og oplysningerne fra batchjobbet. |

Her er en forklaring på mulige statustyper:

- **Afventer** – Det relaterede batchjob afventer behandling på batchserveren.
- **Lykkedes ikke** – Behandlingen mislykkedes. Opgaven kan behandles igen ved hjælp af handlingen **Start udskudt Læg på lager**, eller den kan annulleres ved hjælp af handlingen **Annuller udskudt Læg på lager**.
- **Fuldført** – Jobbet blev fuldført.

## <a name="impact-on-closed-work-dates"></a>Påvirkning af datoer for lukket arbejde

Når udskudt Læg på lager-behandling bruges, angives datoen for lukket arbejde som oprettelsesdato/-tid for de udskudte Læg på lager-behandlingsopgaver. Datoen for lukket arbejde bruges, fordi det er det bedste estimat for, hvornår Læg på lager-handlingen blev fuldført.

## <a name="reprocessing-a-failed-task"></a>Genbehandling af en mislykket opgave

Du kan genbehandle en mislykket opgave ved at vælge den på siden og derefter vælge **Start udskudt Læg på lager**. Genbehandling svarer til en situation, hvor brugeren afslutter Læg på lager fra mobilenheden, som om den var indstillet til øjeblikkelig behandling.

## <a name="canceling-failed-tasks"></a>Annullering af mislykkede opgaver

Kun mislykkede opgaver kan annulleres. Når du annullerer en opgave, kan du tildele den en ny bruger. Alternativt kan opgaven forblive tildelt den bruger, der har behandlet arbejdet. Annullering svarer til en situation, hvor arbejdet er bragt tilbage til mobilenheden, som om det sidste pluktrin var netop fuldført, og arbejdet skal lægges på lager. Brugeren kan dog bestemme, at arbejdet er "anderledes", fordi det kun har et læg på lager-trin, og lokationen svarer til den lokation, som den første bruger, der behandlede arbejdet, havde som en endelig placeringslokation.

Når en opgave annulleres, blokeres arbejdet ikke længere af årsagen til spærringen af den udskudte læg på lager-behandling. Den kan behandles igen ved hjælp af mobilenheden.

Opgaveposten slettes, når opgaven annulleres.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfiguration af mobilenhedens menu til at springe over politikken for udskudt behandling

Du kan konfigurere menupunktet på mobilenheden, så politikken for udskudt behandling ikke bruges. Arbejdet behandles derefter, som det er, når der ikke anvendes en udskudt behandlingspolitik. Denne funktion giver en tilsynsførende mulighed for at bruge et bestemt menupunkt, hvor udskudt læg på lager ikke bruges. Hvis du vil konfigurere den, skal du angive feltet **Politik for udskudt læg på lager-behandling** til **Tilsidesæt indstillinger, og kør læg på lager synkront**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Begrænsninger, når udskudt læg på lager-behandling ikke anvendes

Der er flere scenarier, hvor udskudt læg på lager-behandling ikke anvendes, selvom politikken er konfigureret. Her er nogle eksempler:

- Manuel færdiggørelse af arbejdet anvendes.
- Arbejdet fuldføres automatisk.
- Der bruges revisionsskabeloner.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Overvågning af udskudte behandlingsopgaver fra arbejdsområdet Overvågning af udgående arbejde

Arbejdsområdet **Overvågning af udgående arbejde** har to felter, der hjælper dig med at overvåge udskudte læg på lager-behandlingsopgaver:

- **Mislykkede udskudte læg på lager-behandlingsopgaver** – Dette felt viser antallet af mislykkede opgaver. Hvis der er mislykkede opgaver, skal lagerchefen enten genbehandle dem eller annullere dem, fordi de ikke vil blive genbehandlet automatisk.
- **Afventer udskudte læg på lager-behandlingsopgaver** – Dette felt viser antallet af opgaver, der har været i **Afventer**-status i mere end 10 minutter. Hvis feltet viser et tal, kan det indikere, at der opstod et problem under batchprocessen. Du kan manuelt behandle de **afventende** opgaver. Hvis batchjobbet for en opgave behandles senere, mislykkes det bare, fordi det allerede er blevet behandlet. Der vil ikke være nogen effekt.

## <a name="deleting-completed-tasks"></a>Sletning af fuldførte opgaver

Du kan slette udskudte læg på lager-behandlingsopgaver, der er fuldført, ved at markere dem og slette dem på siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Udskudt behandling af manuel lagerbevægelseshandling](deferred-processing-manual-inventory-movement.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]