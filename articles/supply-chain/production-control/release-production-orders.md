---
title: Frigive produktionsordrer
description: En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 740ac516ffa01d8930aedabb9873834b07b7debf700dc61b14d93ac8d6dcd086
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718864"
---
# <a name="release-production-orders"></a>Frigive produktionsordrer

[!include [banner](../includes/banner.md)]

En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser.

## <a name="characteristics-of-the-released-state"></a>Egenskaber for tilstanden Frigivet

Tilstanden **Frigivet** er en af tilstandene i produktionsordrens levetid. Produktionsordrer, der er i tilstanden **Frigivet**, er tilgængelige til udførelse i produktionen og for lagerprocesser. Tilstanden **Frigivet** har følgende egenskaber:

- En produktionsordre kan ændres til tilstanden **Frigivet** fra produktionsordren eller ved hjælp af en batchproces. Produktionsordren kan også opdateres automatisk fra produktionsordreforslaget, der er autoriseret ved hjælp af feltet **Autorisationstidshorisont** på siden **Behovsplan**.
- Tilstanden **Frigivet** er signalet til produktionen (operatører) om at starte produktionsjob i produktionen.
- Produktionspapirer som rutekort, rutejob og jobkort indeholder oplysninger om produktionsjob og kan udstedes.
- I forbindelse med materialer, der er fysisk reserveret, genereres lagerarbejde til at plukke materialer til produktionsordren.

## <a name="releasing-jobs-to-the-shop-floor"></a>Frigive job til produktionen

Når en produktionsordre er blevet frigivet, er produktionsjob, der vedrører ordren, synlige og klar til registrering. Operatørerne kan foretage jobregistreringer, f.eks. Start, Stop og Færdiggørelse på enten siden **Jobkortsterminal** eller siden **Jobkortenhed**. Den registrerede tid og det registrerede antal overføres automatisk fra registreringssiderne til produktionskladder for at holde styr på den forbrugte tid og det forbrugte antal.

## <a name="route-cards"></a>Rutekort

Et rutekort giver en oversigt over oplysninger, der stammer fra opsætninger af rute og operation og fra metoder til grovplanlægning og finplanlægning.

## <a name="route-jobs"></a>Rutejob

Et jobkort viser hvert job for en handling i detaljer og omfatter opsætning, proces, kø og transporttider. En handling, f.eks maling, kan kræve individuelle job som installationstid, køretid til maleprocessen og køtid til tørring.

## <a name="job-cards"></a>Jobkort

Et jobkort viser de enkelte jobnumre for en bestemt handling. Der vises et job på hver side. De job, der findes på et jobkort, og deres forventede tidspunkter stammer fra opsætningsoplysninger om rute og drift. Fra et jobkort kan du åbne siden **Produktionskladdelinjer**, **jobkort**. De personer, der kører operationsressourcer, kan give tilbagemeldinger om produktionsprocessen. Der er felter, hvor du kan angive forbrugsstatistikker og oplysninger som f.eks antallet af fejl.

## <a name="warehouse-work-for-raw-material-picking"></a>Lagersted for pluk af råvarer

Arbejde til pluk af råvarer genereres under frigivelse. Arbejde oprettes kun for den mængde materialer, der var fysisk reserveret til produktionsordren, før ordren blev frigivet. Der kræves følgende opsætning for at generere lagerstedsarbejde til råvarepluk:

- En bestemmelse for placering for pluk af råvarer, som bestemmer, hvilken lagerlokalitet materialerne skal plukkes i
- En bølgeskabelon for råvarer, hvor politikkerne for udførelse af lagerarbejde konfigureres
- En indlagringslokation for produktion, der bestemmer, hvor materialer lægges på lager

Ved brug af lokationer, der styres af nummerplader, kan du vælge, om det bestilte antal eller det fulde antal, der er til rådighed for varen, skal plukkes under behandlingen af plukarbejdet med råmaterialerne. Sådan angiver du dette:

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**, og åbn den relevante vare.
1. Udvid oversigtspanelet **Lagersted**.
1. Vælg en af følgende indstillinger for feltet **Materialepluk i nummerpladelokationer**:
    - *Ordrepluk*: Kun det bestilte antal skal plukkes.
    - *Midlertidig* Når det er muligt, skal hele det disponible antal plukkes fra nummerpladen. Hvis en arbejder skal kunne plukke hele nummerpladeantallet, må nummerpladen ikke indeholde blandede varer og må ikke have blandede dimensioner. Hvis nummerpladen indeholder blandede dimensioner eller varer, fortsætter plukningen, som om den var indstillet til *Ordrepluk*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]