---
title: Opdater opgaven Produktkvittering bekræfter ikke-bekræftede ordrer
description: Når du har kørt Opdater produktkvitteringerne, bekræfter systemet ikke-bekræftede ordrer, der har statussen Registreret. Få mere at vide om den funktion, der løser dette problem.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475869"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Ikke-bekræftede indkøbsordrer bekræftes når der kører opdatering af produktkvitteringer

## <a name="symptoms"></a>Symptomer

Når du har kørt den periodiske opgave *Opdater produktkvitteringer*, bekræfter systemet automatisk ubekræftede indkøbsordrer, der har lagertransaktionstatus *Registreret*.

## <a name="resolution"></a>Løsning

En ny funktion til håndtering af indgående last, *Overtilgang af lastantal*, løser dette problem. Hvis du aktivere denne funktion, skal du gå til arbejdsområdet [Funktionsstyring](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) og aktivere følgende funktioner i deres viste rækkefølge:

1. Tilknyt lagertransaktioner med belastning for indkøbsordre
2. Overtilgang af lastantal

Du kan finde flere oplysninger under [Bogføre registrerede produktantal i forhold til indkøbsordrer](/dynamics365/supply-chain/warehousing/inbound-load-handling).
