---
title: Oversigt over indtægtsføring (indeholder video)
description: Denne artikel indeholder oplysninger om funktionen Indtægtsføring. Denne funktion giver en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen for ordrer med flere elementer.
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5bf07356b5613f438034f8dabac7db197e69a6c8
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644024"
---
# <a name="revenue-recognition-overview"></a>Oversigt over indtægtsføring

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Denne funktion udfases i oktober 2023, og nye brugere skal bruge abonnementsfakturering.

Virksomheder i brancher, der sælger flere elementer, f. eks. produkter, tjenester, abonnementer osv., skal være i stand til at opdele ordrer med flere elementer, så omsætningen kan genkendes på grundlag af en række firmaspecifikke og branchespecifikke retningslinjer.

Indtægtsføring, herunder bundtfunktionalitet, understøttes ikke til brug i Commerce-kanaler (e-handel, POS, callcenter). Varer, der er konfigureret med indtægtsføring, bør ikke føjes til ordrer eller transaktioner, der er oprettet i Commerce-kanaler.

Generelt kan processen til indtægtsføring bruges til at udføre disse opgaver:

* Fordele omsætning som en hjælp til at sikre, at den relevante indtægtspris genkendes på basis af værdien af komponenterne i ordrer med flere elementer.
* Udskyde omsætning på basis af en indtægtstidsplan, der repræsenterer den kontraktmæssige tidsramme og procentdele til indtægtsføring over tid.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Videoen [Sådan bruges indtægtsføring i Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vist ovenfor) er inkluderet i den [Finans og drift-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

Funktionen Indtægtsføring indeholder en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen.

Frigivne produkter bruges til at understøtte indtægtsføring på salgsordredokumenter. De frigivne produkter indeholder den opsætning, der skal bruges til at bestemme indtægtsprisen og indtægtstidsplanen. Salgsordren kan stamme fra et Tid og materialer-projekt.

Virksomheder kan bruge funktionen Indtægtstidsplan uden at bruge funktionen Indtægtspris. Derfor bruges prisen på salgsordrelinjerne som enten omsætning eller udskudt omsætning. Hvis der findes en indtægtstidsplan på salgsordrelinjen, udskydes prisen på salgsordrelinjen. Hvis der ikke findes en indtægtstidsplan på salgsordrelinjen, bogføres prisen på salgsordrelinjen på en indtægtskonto, når den faktureres.

Indtægtsprisen beregnes enten, når salgsordren bekræftes, eller når fakturaen bogføres. Hvis du vil se en prøveversion af indtægtsprisen, før fakturaen bogføres, skal du bekræfte salgsordren.

Når salgsordren bekræftes, oprettes der også en forventet indtægtstidsplan, hvis nogen af salgsordrelinjerne indeholder en indtægtstidsplan. Når salgsordren faktureres, slettes den forventede indtægtstidsplan, og den forventede indtægtstidsplan erstattes af den faktiske indtægtsføringstidsplan.

Oplysningerne om indtægtsføringstidsplanen vedligeholdes for hver salgsordrelinje. Den ansvarlige for indtægtsføring kan derfor få vist detaljerne og frigive linjer til omsætning, når kontraktforpligtelsen er fuldført. Ved afslutningen af hver periode kan den ansvarlige for indtægtsføringen oprette en omsætningskladde for at frigive alle tidsplanlinjer, der forfalder på eller før en dato, som pågældende definerer. Denne omsætningskladde bogføres ikke med det samme. Derfor kan den ansvarlige for indtægtsføringen kontrollere, at de korrekte beløb frigives fra udskudt indtægt til faktisk indtægt.

Hvis en kontraktmæssig ændring medfører, at en ny salgsordrelinje føjes til enten den eksisterende salgsordre eller en ny salgsordre, kan der køres en omfordelingsproces for at rette indtægtsprisen på alle linjer på salgsordrerne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

