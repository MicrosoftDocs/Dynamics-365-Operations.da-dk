---
title: Konfigurer momsafregningsperioder
description: Denne artikel beskriver, hvordan du konfigurerer momsafregningsperioder i Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f8514494b5d3534fc236def817df0d58fe80d70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846677"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Konfigurer momsafregningsperioder

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer momsafregningsperioder. Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for. Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval. Alle momskoder, der er knyttet til afregningsperioden, udlignes. Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.

Denne opgave bruger demofirmaet USMF.

1. Gå til **Moms > Indirekte skatter > Moms > Momsafregningsperioder**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Afregningsperiode**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. I feltet **Momsmyndighed** skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.
6. Find og vælg den ønskede post på listen.
7. I feltet **Betalingsbetingelser** skal du vælge den ønskede post i rullemenuen. De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura. Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.  
8. Vælg en type for intervaller for afregningsperioder.
9. Angiv antallet af enheder i periodeintervallet pr. periode. For eksempel har en kvart 3 måneder.
10. Markér eller fjern markeringen af afkrydsningsfeltet **Brug batchbehandling til afregning af moms**. Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden. Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.
11. Marker eller fjern markeringen i afkrydsningsfeltet **Undgå at generere modregning af momsposteringer**. Som standard genererer systemet modregning af momsposteringer under udligningsprocessen, hvilket kan give problemer med ydeevnen, hvis der er et stort antal momsposteringer inden for et periodeinterval. Marker dette afkrydsningsfeltet for at undgå, at der genereres modregning af momsposteringer.
12. Udvid fanen **Periodeintervaller**.
13. Vælg **Tilføj**.
14. Indtast en dato i feltet **Fra dato**.
15. Indtast en dato i feltet **Til dato**.
16. Vælg **Nyt periodeinterval**. Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder. Du kan vende tilbage og tilføje nye periodeintervaller efter behov.  
17. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
