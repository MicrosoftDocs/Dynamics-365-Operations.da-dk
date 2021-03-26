---
title: Oversigt over indtægtsføring
description: Dette emne indeholder oplysninger om funktionen Indtægtsføring. Denne funktion giver en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen for ordrer med flere elementer.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b21cf04674d01df31dc3304886e7cda035bdcce2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238250"
---
# <a name="revenue-recognition-overview"></a>Oversigt over indtægtsføring

[!include [banner](../includes/banner.md)]

Virksomheder i brancher, der sælger flere elementer, f. eks. produkter, tjenester, abonnementer osv., skal være i stand til at opdele ordrer med flere elementer, så omsætningen kan genkendes på grundlag af en række firmaspecifikke og branchespecifikke retningslinjer.

> [!NOTE]
> Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring. I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.

> Indtægtsføring, herunder bundtfunktionalitet, understøttes ikke til brug i handelskanaler (e-handel, POS, callcenter). Varer, der er konfigureret med indtægtsføring, bør ikke føjes til ordrer eller transaktioner, der er oprettet i Commerce-kanaler.

Generelt kan processen til indtægtsføring bruges til at udføre disse opgaver:

* Fordele omsætning som en hjælp til at sikre, at den relevante indtægtspris genkendes på basis af værdien af komponenterne i ordrer med flere elementer.
* Udskyde omsætning på basis af en indtægtstidsplan, der repræsenterer den kontraktmæssige tidsramme og procentdele til indtægtsføring over tid.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Videoen [Sådan bruges indtægtsføring i Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

Funktionen Indtægtsføring indeholder en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen.

Frigivne produkter bruges til at understøtte indtægtsføring på salgsordredokumenter. De frigivne produkter indeholder den opsætning, der skal bruges til at bestemme indtægtsprisen og indtægtstidsplanen. Salgsordren kan stamme fra et Tid og materialer-projekt.

Virksomheder kan bruge funktionen Indtægtstidsplan uden at bruge funktionen Indtægtspris. Derfor bruges prisen på salgsordrelinjerne som enten omsætning eller udskudt omsætning. Hvis der findes en indtægtstidsplan på salgsordrelinjen, udskydes prisen på salgsordrelinjen. Hvis der ikke findes en indtægtstidsplan på salgsordrelinjen, bogføres prisen på salgsordrelinjen på en indtægtskonto, når den faktureres.

Indtægtsprisen beregnes enten, når salgsordren bekræftes, eller når fakturaen bogføres. Hvis du vil se en prøveversion af indtægtsprisen, før fakturaen bogføres, skal du bekræfte salgsordren.

Når salgsordren bekræftes, oprettes der også en forventet indtægtstidsplan, hvis nogen af salgsordrelinjerne indeholder en indtægtstidsplan. Når salgsordren faktureres, slettes den forventede indtægtstidsplan, og den forventede indtægtstidsplan erstattes af den faktiske indtægtsføringstidsplan.

Oplysningerne om indtægtsføringstidsplanen vedligeholdes for hver salgsordrelinje. Den ansvarlige for indtægtsføring kan derfor få vist detaljerne og frigive linjer til omsætning, når kontraktforpligtelsen er fuldført. Ved afslutningen af hver periode kan den ansvarlige for indtægtsføringen oprette en omsætningskladde for at frigive alle tidsplanlinjer, der forfalder på eller før en dato, som pågældende definerer. Denne omsætningskladde bogføres ikke med det samme. Derfor kan den ansvarlige for indtægtsføringen kontrollere, at de korrekte beløb frigives fra udskudt indtægt til faktisk indtægt.

Hvis en kontraktmæssig ændring medfører, at en ny salgsordrelinje føjes til enten den eksisterende salgsordre eller en ny salgsordre, kan der køres en omfordelingsproces for at rette indtægtsprisen på alle linjer på salgsordrerne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]