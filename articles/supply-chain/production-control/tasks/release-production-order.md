---
title: Frigive en produktionsordre
description: Denne procedure viser, hvordan du frigiver en produktionsordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0db7f93e113d8f41effd68ce19aa065b031fd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573651"
---
# <a name="release-a-production-order"></a>Frigive en produktionsordre

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du frigiver en produktionsordre. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den fjerde procedure ud af syv, der beskriver produktionsordrens livscyklus.

1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
    * Vælg en produktionsordre med status Planlagt i gitteret.  
2. Klik på Produktionsordre i handlingsruden.
3. Klik på Frigiv.
    * På denne side kan du bekræfte frigivelsen af det markerede område af produktionsordrer. Klik på Vælg, hvis du vil tilføje ordrer.  
    * Trinnet Frigiv angiver, hvornår produktionsordren er frigivet til produktionen, så operatører i produktionen kan rapportere status for produktionsjob. Der kan udstedes produktionspapirer, der indeholder relevante oplysninger om behandling af job. Lagerstedsarbejde til pluk af råvarer genereres for de varer, der er defineret for lagerstedsprocessen.  
4. Klik på fanen Generelt.
    * Vælg, hvilke produktionsrapporter der skal udskrives. Jobkortrapporten udskriver en side for hvert planlagt job og kræver, at produktionsordren planlægges på jobniveau. Rapporten indeholder oplysninger om planlagt start- og sluttidspunkt, antallet, der skal produceres, og hvilken ressource der behandler jobbet. Rapporten Rutejob indsamler de samme oplysninger på den samme side, men udskriver ikke en side for hvert job. Rapporten Rutekort viser kun handlingerne, men ikke jobbene. Derfor kræver denne rapport ikke finplanlægning, men kan bruges, når produktionsordrer planlægges på driftsniveau.  
5. Markér afkrydsningsfeltet Udskriv rutekort.
6. Klik på OK.
7. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]