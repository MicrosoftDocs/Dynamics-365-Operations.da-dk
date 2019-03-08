---
title: Betalingsmetoder i callcentre
description: Dette emne beskriver de forskellige betalingsmetoder, du kan bruge i et callcenter i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 825ad4ba3e72e5b34c2ff29f36f88a518810ce49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "355374"
---
# <a name="payment-methods-in-call-centers"></a>Betalingsmetoder i callcentre

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 for Retail omfatter konfigurationen af callcenter-kanalen indstillingen **Aktivér ordrefuldførelse**. Denne indstilling er med til at sikre, at alle ordrer, som brugere af kanalen opretter, kun frigives til ordrebehandling, hvis de har en forudbetalt eller forhåndsgodkendt betaling, der ligger inden for godkendte tolerancer. Hvis indstillingen **Aktivér ordrefuldførelse** er aktiveret, kan callcenter-brugere angive betalinger i forhold til salgsordrer for debitorer ved hjælp af funktionerne til behandling af betalinger for Callcenter. Hvis indstillingen er slået fra, kan callcenter-brugere ikke bruge funktionerne til behandling af betaling, men de kan stadig anvende forudbetalinger på salgsordrer ved hjælp af standardfunktioner for Debitor.

Som en del af kanalkonfigurationen kan et firma definere de betalingsmetoder, der er tilladt for callcenter-kanal. Callcenter-kanalen bruger de samme betalingsmetoder, der er defineret for detailbutikskanalerne.

Du kan konfigurere betalingsmetoder for en callcenter-kanal ved at gå til **Retail** \> **Kanaler** \> **Callcentre** \> **Alle callcentre** og derefter klikke i menuen **Opsætning** på indstillingen **Betalingsmetoder**.

Når du opretter en betalingsmetode, kan du tildele fem funktioner for betalingsmetoder.

| Funktion            | Betegnelse |
|---------------------|-------------|
| Almindelig              | Brug funktionen **Normal** for betalingsmetoden, når du definerer betalingsmetoder som f.eks. kontantbetaling eller med bilag. Når disse typer af betalinger anvendes til en salgsordre i callcenteret, anvendes standardværdien **Ja** til flaget **Forudbetaling**. Herved bogføres med det samme et forudbetalingsbilag på debitors konto, når denne ordre sendes. Brugerne kan ændre flaget **Forudbetaling** til **Nej**, så betalingsbilaget ikke oprettes før fakturabogføring. Forudbetalingsbilaget bogføres i debitorens transaktionshistorik, hvor det systematisk udlignes mod fakturaen for salgsordren. |
| Check               | Brug funktionen **Check**, når du definerer en bankcheck som en del af betalingen. Når denne type betaling anvendes til en salgsordre, skal brugeren angive debitorens checknummer som en del af programmets betalingsbehandling. Betalinger med check behandles altid som forudbetalinger, når de udlignes, og betalingsbilag oprettes med det samme ved afsendelse af ordren. Disse forudbetalingsbilag udlignes systematisk mod de fakturaer, der er oprettet for ordren. |
| Kort               | Kortbetalingstyper repræsenterer alle betalinger, der kræver indtastning af et kortnummer, der er defineret på debitorens betalingskort. Eksempler omfatter kreditkort og gavekort. Når du konfigurerer disse betalingstyper, skal du bruge menuen **Opsætning af kort** til at definere de kort-id'er, der er tilknyttet denne betalingsmetode. På tidspunktet for ordreindtastning kan brugere angive, om kortbetalingen skal forudbetales, ved hjælp af indstillingen **Forudbetal**, som vises på siden for betalingsindtastning. Medmindre virksomheden kræver forudbetalinger, består den typiske proces for en ægte kreditkortbetaling af to trin, hvor godkendelsen indhentes på tidspunktet for ordreindtastningen, og betalingen udlignes derefter og indhentes fra kundens kort på faktureringstidspunktet. Gavekortbetalinger anbefales forudbetaling, fordi gavekortets saldo skal reduceres med det samme, så kunden ikke kan anvende den samme værdi et andet sted. |
| Kunde            | Funktionen **Debitor** for en betalingsmetode indebærer, at betalingen udlignes mod kundens kreditmaksimum eller sættes "på konto". I Retail kan en debitor få tildelt et kreditmaksimum, som kan være godkendt på tidspunktet for ordreindtastning. Betalinger, der foretages ved hjælp af en betalingsmåde, der er knyttet til funktionen **Debitor**, opretter et passiv på debitorens konto. Når salgsordren er faktureret, vises derefter en forfalden saldo. I disse situationer kan debitorer typisk sende en betaling i henhold til de oplyste betingelser. Du kan også anvende et kreditbilag på debitorens konto, som tidligere har været åbnet, til udligning af den forfaldne saldo. Bemærk, at selvom du definerer denne betalingsmetode, vises den ikke blandt valgmulighederne for betaling i callcenterets ordreindtastning, medmindre flaget **Tillad aconto** er angivet i debitorposten for den debitor, du arbejder med. Dette flag findes på fanen **Betalingsstandarder** i debitorposten. |
| Betalingsmiddel fjern/variabel | Funktionen **Betalingsmiddel fjern/variabel** bruges ikke af callcenteret. Det er kun relevant, når du definerer de betalingsmetoder, som salgsstedet (POS) bruger i en butikskanal. |

Når der defineres betalingsmåder, skal de knyttes til en finanskonto eller bankkonto. Hvis du udelader dette trin, får brugerne vist fejl, når de forsøger at gemme betalingstypen.

## <a name="refund-payment-methods"></a>Refusionsbetalingsmetoder

For refusionsbehandlingsscenarier bruger Callcenter også nogle af de betalingsmåder, der er defineret i Debitor. Hvis du vil konfigurere disse betalingsmetoder, skal du gå til **Retail** \> **Konfiguration af kanal** \> **Call center-konfiguration** \> **Call center-refusionsmetoder**. Du skal udføre denne konfiguration for at behandle refusionschecks til debitorer. Hvis en debitor oprindeligt har betalt for en ordre ved hjælp af kontanter eller en check, vil brugeren muligvis sende debitoren en refusionscheck gennem Debitor. I så fald skal betalingstyperne for kontanter og check knyttes til den rette betalingsmetode i Debitor for at sikre, at refusionen behandles korrekt.

Hvis en bruger behandler en returordre som en callcenter-bruger i Retail, men han eller hun ikke kan knytte returneringen til et oprindeligt salg, skal betalingsmetoden **Returnering** defineres i parametrene for Callcenter. Gå til **Retail** \> **Konfiguration af kanal** \> **Call center-konfiguration** \> **Call center-parametre**, og klik derefter på fanen **RMA/returnering** for at sikre i feltet **Betalingsmetode**, at der er defineret en betalingsmetode. Betalingsmetoden, bliver den betalingsmåde, der bruges til refusioner. Den vil typisk være defineret enten som betaling med check eller kundekonto.
