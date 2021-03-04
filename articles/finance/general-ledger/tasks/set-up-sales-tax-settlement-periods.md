---
title: Konfigurere momsafregningsperioder
description: I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5068c121e921c1586dc6ae003c0021bf41d2254
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441565"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Konfigurere momsafregningsperioder

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder. Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for. Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval. Alle momskoder, der er knyttet til afregningsperioden, udlignes. Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.

Denne opgave bruger demofirmaet USMF.

1. I navigationsruden skal du gå til **Moduler > Moms > Indirekte skatter > Moms > Momsafregningsperioder**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Afregningsperiode**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. I feltet **Momsmyndighed** skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.
6. Find og vælg den ønskede post på listen.
7. I feltet **Betalingsbetingelser** skal du vælge den ønskede post i rullemenuen. De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura. Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.  
8. Vælg en type for intervaller for afregningsperioder.
9. Angiv antallet af enheder i periodeintervallet pr. periode. For eksempel har en kvart 3 måneder.
10. Markér eller fjern markeringen af afkrydsningsfeltet **Brug batchbehandling til afregning af moms**. Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden. Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.  
    > [!NOTE]
    > I øjeblikket understøttes dette ikke i Spanien, Japan og Nederlandene.
11. Marker eller fjern markeringen i afkrydsningsfeltet **Undgå at generere modregning af momsposteringer**. Som standard genererer systemet modregning af momsposteringer under udligningsprocessen, hvilket kan give problemer med ydeevnen, hvis der er et stort antal momsposteringer inden for et periodeinterval. Marker dette afkrydsningsfeltet for at undgå, at der genereres modregning af momsposteringer.
12. Udvid fanen **Periodeintervaller**.
13. Vælg **Tilføj**.
14. Indtast en dato i feltet **Fra dato**.
15. Indtast en dato i feltet **Til dato**.
16. Vælg **Nyt periodeinterval**. Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder. Du kan vende tilbage og tilføje nye periodeintervaller efter behov.  
17. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]