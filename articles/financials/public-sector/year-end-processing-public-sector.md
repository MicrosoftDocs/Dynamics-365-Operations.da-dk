---
title: Årsafslutningen i den offentlige sektor
description: Denne artikel indeholder oplysninger om årsafslutningen for organisationer i den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchYearEndClose
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 19601
ms.assetid: ba9a7abc-bd18-47c2-b745-96cdcec8ac98
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9a89bd38feac2e580c3d1511d3bee8eca04115d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370236"
---
# <a name="year-end-processing-in-the-public-sector"></a>Årsafslutningen i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om årsafslutningen for organisationer i den offentlige sektor.

I dette emne beskrives de årsafslutningsfunktioner, som er tilgængelige for den offentlige sektor. Ved udgangen af regnskabsåret skal du generere ultimoposter og forberede alle konti til det næste regnskabsår.  Kunder i den offentlige sektor har følgende muligheder:

-   Vælg konti efter midler for ultimo ved årsafslutning.
-   Luk midler til forskellige konti. For eksempel kan du lukke nominelle konti, der er knyttet til statslige midler til pengebalancer. Du kan også lukke nominelle konti, der er forbundet med egne midler til overførte resultater.
-   Angive ultimo ved årsafslutning for alle midler og ikke-midler. Ikke-midler har ikke dimensionen midler i kontostrukturen.
-   Konfigurere flere ultimoperioder for at adskille forskellige former for ultimoposter, f.eks. generel lukning i forbindelse med ultimo ved årsafslutning og revisionsjusteringer.

## <a name="can-the-year-end-process-be-run-more-than-one-time-on-the-same-data"></a>Kan årsafslutningsprocessen køres mere end én gang med de samme data?
Ja, årsafslutningsprocessen kan køres flere gange for det samme sæt af data. Typisk, hvis flere transaktioner skal behandles, når der er kørt en årsafslutningsproces for Finans, kan årsafslutningsprocessen køres igen for at lukke de nominelle konti og angive startsaldiene korrekt i det nye år.

## <a name="how-do-i-set-up-funds-for-year-end-processing"></a>Hvordan konfigurerer jeg midler til behandling af årsafslutning?
Behandling af årsafslutningen for finanskonti styres af konfigurationsindstillingerne for midler på to steder:

-   Årsafslutningsprocessen for ultimofinanssaldi i det gamle regnskabsår og oprettelse af startsaldi for det nye år sker ved hjælp af siden **Primoposter** side. Et enkelt middel eller en række af midler, der kræves til behandling.
-   Årsafslutningens behandlingsindstilling for behæftelser for indkøbsordrer angives på siden **Proces for indkøbsordrers årsafslutning**. Du kan tilsidesætte indstillingen for bestemte midler, forudsat at de finansparametrene er indstillet til at tillade tilsidesættelse. Hvis du vil vide mere om parameterindstillingerne, skal du se under [Finans i den offentlige sektor](general-ledger-public-sector.md).

## <a name="how-do-i-set-up-main-accounts-for-year-end-processing"></a>Hvordan konfigurerer jeg hovedkonti til behandling af årsafslutning?
Du skal vælge en lukketype for hver konto i din kontoplan. Lukketypen bestemmer, hvordan årsafslutningsprocessen håndterer denne hovedkonto. Der findes fire lukketyper:

-   **Real** – Saldoen bruges til at etablere primosaldoer i det nye år.
-   **Nominel** – Kontoen lukkes af årsafslutningsprocessen.
-   **Nominel – luk ikke** – Kontoen administreres af andre processer til lukning, som behæftelseskonti for indkøbsordrelukning.
-   **Ikke relevant** – Kontoen medtages ikke i årsafslutningsprocessen.

Bogføringsdefinitioner styrer de regnskaber, der forekommer på ultimoposterne, og de hjælper også oprette primoposterne for det nye år. Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).



