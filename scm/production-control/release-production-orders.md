---
title: Frigive produktionsordrer
description: "En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c4ebedab6d7de62479d3bc80583afadbe780aac4
ms.lasthandoff: 03/31/2017


---

# <a name="release-production-orders"></a>Frigive produktionsordrer

En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser. 

<a name="characteristics-of-the-released-state"></a>Egenskaber for tilstanden Frigivet
-------------------------------------

Tilstanden **Frigivet** er en af tilstandene i produktionsordrens levetid. Produktionsordrer, der er i tilstanden **Frigivet**, er tilgængelige til udførelse i produktionen og for lagerprocesser. Tilstanden **Frigivet** har følgende egenskaber:

-   En produktionsordre kan ændres til tilstanden **Frigivet** fra produktionsordren eller ved hjælp af en batchproces. Produktionsordren kan også opdateres automatisk fra produktionsordreforslaget, der er autoriseret ved hjælp af feltet **Autorisationstidshorisont** på siden **Behovsplan**.
-   Tilstanden **Frigivet** er signalet til produktionen (operatører) om at starte produktionsjob i produktionen.
-   Produktionspapirer som rutekort, rutejob og jobkort indeholder oplysninger om produktionsjob og kan udstedes.
-   I forbindelse med materialer, der er fysisk reserveret, genereres lagerarbejde til at plukke materialer til produktionsordren.

## <a name="releasing-jobs-to-the-shop-floor"></a>Frigive job til produktionen
Når en produktionsordre er blevet frigivet, er produktionsjob, der vedrører ordren, synlige og klar til registrering. Erhvervsdrivende kan foretage jobregistreringer, Start, Stop og afslutning på enten den **Job card terminal** side eller **Job card-enhed** side. Den registrerede tid og antal overføres automatisk fra registreringssider til produktionskladder for at holde styr på den forbrugte tid og antal.

## <a name="route-cards"></a>Rutekort
Et rutekort giver en oversigt over oplysninger, der stammer fra opsætninger af rute og operation og fra metoder til grovplanlægning og finplanlægning.

## <a name="route-jobs"></a>Rutejob
Et jobkort viser hvert job for en handling i detaljer og omfatter opsætning, proces, kø og transporttider. En handling, f.eks maling, kan kræve individuelle job som installationstid, køretid til maleprocessen og køtid til tørring.

## <a name="job-cards"></a>Jobkort
Et jobkort viser de enkelte jobnumre for en bestemt handling. Der vises et job på hver side. De job, der findes på et jobkort, og deres forventede tidspunkter stammer fra opsætningsoplysninger om rute og drift. Fra et jobkort kan du åbne siden **Produktionskladdelinjer**, **jobkort**. De personer, der kører operationsressourcer, kan give tilbagemeldinger om produktionsprocessen. Der er felter, hvor du kan angive forbrugsstatistikker og oplysninger som f.eks antallet af fejl.

## <a name="warehouse-work-for-raw-material-picking"></a>Lagersted for pluk af råvarer
Arbejde til pluk af råvarer genereres under frigivelse. Arbejde oprettes kun for den mængde materialer, der er fysisk reserveret for produktionsordren, før ordren er frigivet. Der kræves følgende opsætning til at generere lagersted arbejde til råvarer pluk:

-   En bestemmelse for placering for pluk af råvarer, som bestemmer, hvilken lagerlokalitet materialerne skal plukkes i
-   En bølgeskabelon for råvarer, hvor politikkerne for udførelse af lagerarbejde konfigureres
-   En indlagringslokation for produktion, der bestemmer, hvor materialer lægges på lager


