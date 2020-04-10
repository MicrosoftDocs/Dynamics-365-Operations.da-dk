---
title: Generere et overførselsdokument for en intern lageroverførsel
description: Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cb0d3d51bf30717f05a4daf1a098565d5d48621
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143403"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Generere et overførselsdokument for en intern lageroverførsel

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed. Denne procedure er kun tilgængelig for juridiske enheder med en primær adresse i Litauen. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Litauen. Før du kan udføre denne procedure, skal du fuldføre proceduren "Konfiguration af overførselsdokumenter for transport af varer inden for virksomheden". Denne procedure er kun beregnet til lagerregnskabsmedarbejdere. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-a-transfer-order"></a>Oprette en flytteordre
1. Gå til Lagerstyring > Indgående ordrer > Overførselsordre.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Fra lagersted.
4. Indtast eller vælg en værdi i feltet Til lagersted.
5. Klik på Tilføj.
6. Markér den valgte række på listen.
7. Indtast eller vælg en værdi i feltet Varenummer.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Angiv transportdetaljer for flytteordren
1. Klik på Gem.
2. Klik på Send i handlingsruden.
3. Klik på Transportdetaljer.
4. Vælg Ja i feltet Udskriv transportdetaljer.
5. Indtast eller vælg en værdi i feltet Afgang af varer udført af.
6. Skriv en værdi i feltet Pakke.
7. Skriv en værdi i feltet Risikoniveau for indlæsning.
8. Indtast eller vælg en værdi i feltet Fragtmand.
9. Indtast eller vælg en værdi i feltet Model.
10. Skriv en værdi i feltet Registreringsnummer.
11. Skriv en værdi i feltet Trailernummer.
12. Indtast eller vælg en værdi i feltet Chauffør.
13. Angiv en værdi i feltet Chauffør.
14. Klik på Gem.
15. Luk siden.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Vis følgesedlen for den ikke-bogførte overførselsordre
1. Klik på følgeseddel.
2. Klik på OK.
3. Luk siden.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Vis følgesedlen for den bogførte overførselsordre
1. Klik på Overførselsordre i handlingsruden.
2. Klik på Send i handlingsruden.
3. Klik på Forsendelsesflytteordre.
4. Klik på fanen Generelt.
5. Vælg en indstilling i feltet Opdater.
6. Klik på fanen Oversigt.
7. Skriv en værdi i feltet Følgeseddel.
8. Klik på OK.
9. Klik på Send i handlingsruden.
10. Klik på følgeseddel.
11. Klik på OK.

