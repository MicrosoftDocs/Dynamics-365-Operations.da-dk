---
title: Problemer med dataafstemningen af en Z-rapport
description: Denne artikel beskriver problemer, som brugerne kan komme ud for i forbindelse med dataafstemningen af en Z-rapport i Commerce Headquarters. Den beskriver også mulige rodårsager og løsninger, der kan hjælpe med at forhindre fremtidige forekomster.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832123"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Problemer med dataafstemningen af en Z-rapport

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der opstår problemer med dataafstemningen af en Z-rapport i Microsoft Dynamics 365 Commerce headquarters. Den indeholder en beskrivelse af de problemer, brugerne kan have med dataafstemningen, mulige rodårsager og løsninger, der kan hjælpe med at forhindre fremtidige forekomster.

## <a name="description"></a>Beskrivende tekst

- Der er uoverensstemmelse mellem de beløb, der vises i Z-rapporten, og de totaler, der vises på den beregnede opgørelse.
- Posteringen i headquarters har et forkert antal linjeelementer, eller der er uoverensstemmelse mellem linjetotalen og totalen for posteringen.
- Antallet af posteringer, der vises på et skiftehold i hovedkontoret, er mindre end antallet af posteringer i Z-rapporten.
- Bogføringen af opgørelsen mislykkedes af en af de foregående årsager.

### <a name="root-cause"></a>Årsagen

Den mest almindelige rodsårsag til de tidligere beskrevne symptomer er generering af identiske posterings-i kanaldatabasen. Duplikerede transaktions-id'er kan genereres af følgende årsager:

- Den lokale database til lagring af MPOS (Modern Point of Sale) er ødelagt.
- MPOS har nogle transaktioner i offlinetilstand, og den genaktiveres ved hjælp af en konto, der ikke har adgang til offlinedatabasen.
- Der er et problem med tilpasning, der er knyttet til generering af posterings-id'er.

## <a name="resolution"></a>Løsning

Normalt benytter handel en nummerserie til at generere fortløbende transaktions-sekvens-sekvens-sekvenser. Hvis systemet ikke kan bestemme, at der er brugt en nummerserie af en eller anden grund, genereres der et identisk posterings-id. 

Du kan løse problemet med det identiske posterings-id ved at oprette en supportbillet, der kontrollerer, om transaktionsdataene kan rettes. I nogle tilfælde, f.eks. når der ikke er tab af data i hovedkontoret, er der ikke mulighed for eller kræves datarettelser.

Hvis du vil forhindre dette problem i fremtiden, skal du **aktivere funktionen Aktiver nyt posterings-id for at undgå funktionen for identiske posterings-id'er** i hovedkontoret. Denne funktion blev tilføjet i Commerce version 10.0.19. Den hjælper med at forhindre oprettelse af sekvensposterings-id'er ved at sikre, at der oprettes et entydigt posterings-id for hver postering. Yderligere oplysninger finder du under [Forhindre duplikering af transaktions-id'er](../channel-setup-retail.md#ensure-unique-transaction-ids).
