---
title: Konfigurer momsafregningsperioder
description: Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862982"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Konfigurer momsafregningsperioder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for. Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval. Alle momskoder, der er knyttet til afregningsperioden, udlignes. Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.



Denne opgave bruger demofirmaet USMF.



1. Gå til Moms > Indirekte skatter > Moms > Momsafregningsperioder.
2. Klik på Ny.
3. Skriv en værdi i feltet Afregningsperiode.
4. Skriv en værdi i feltet Beskrivelse.
5. I feltet Momsmyndighed skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Betalingsbetingelse for at åbne opslaget.
    * De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura. Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.  
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Vælg en type for intervaller for afregningsperioder.
12. Angiv antallet af enheder i periodeintervallet pr. periode. For eksempel har en kvart 3 måneder.
13. Markér eller fjern markeringen af afkrydsningsfeltet Brug batchbehandling til afregning af moms.
    * Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden. Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.  
    > [!NOTE]
    > I øjeblikket er understøttes dette ikke i Østrig, Belgien, Spanien, Italien, Japan og Nederlandene.
14. Marker eller fjern markeringen i afkrydsningsfeltet Undgå at generere modregning af momsposteringer.
    * Som standard genererer systemet modregning af momsposteringer under udligningsprocessen, hvilket kan give problemer med ydeevnen, hvis der er et stort antal momsposteringer inden for et periodeinterval. Marker dette afkrydsningsfeltet for at undgå, at der genereres modregning af momsposteringer.
15. Udvid fanen Periodeintervaller.
16. Klik på Tilføj.
17. Markér den valgte række på listen.
18. Indtast en dato i feltet Fra dato.
19. Indtast en dato i feltet Til dato.
20. Klik på Nyt periodeinterval.
    * Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder. Du kan vende tilbage og tilføje nye periodeintervaller efter behov.  
21. Luk siden.

