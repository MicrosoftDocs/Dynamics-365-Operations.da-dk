--- 
title: "Administrere måleenhed"
description: "Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>Administrere måleenhed

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder. Du kan gennemgå denne procedure ved at bruge demodataene eller dine egne data.

1. Gå til Vedligeholdelse af frigivet produkt.
2. Klik på enheder.

## <a name="create-a-unit-of-measure"></a>Opret en måleenhed
1. Klik på Ny.
2. Skriv en værdi i feltet Enhed.
    * Angiv det id eller symbol, der skal bruges i forbindelse med måleenheden.  
3. Skriv en værdi i feltet Beskrivelse.
    * Indtast et beskrivende navn for måleenheden i systemsproget.  
4. Vælg en indstilling i feltet Enhedsklasse.
    * Enhedsklassen definerer, hvilken logisk gruppering, f.eks. område, masse eller mængde, måleenheden er del af.  
5. Angiv et tal i feltet Decimalpræcision.
    * Angiv antallet af decimaler, som den omregnede måleenhed skal afrundes til, når der er fuldført en beregning for måleenheden.  
6. Klik på Gem.

## <a name="define-unit-translations"></a>Definer enhedsoversættelser
1. Klik på Enhedstekster.
2. Klik på Ny.
    * Brug enhedstekst til at oprette en oversættelse af id'et eller et symbol, der repræsenterer måleenheden, til brug på eksterne dokumenter på debitor- eller kreditorspecifikke sprog.  
3. Indtast eller vælg en værdi i feltet Sprog.
4. Skriv en værdi i feltet Tekst.
5. Klik på Gem.
6. Luk siden.
7. Klik på Oversatte beskrivelser af enheder.
8. Klik på Ny.
    * Definer sprogspecifikke beskrivelser af måleenheden.  
9. Indtast eller vælg en værdi i feltet Sprog.
10. Skriv en værdi i feltet Beskrivelse.
11. Klik på Gem.
12. Luk siden.

## <a name="define-unit-conversion-rules"></a>Definer omregningsregler for enhed
1. Klik på Vis enhedsomregninger.
    * Definer regler for konvertering af måleenheden til og fra andre enheder i den valgte enhedsklasse.  
2. Klik på Ny for at åbne dialogboksen Fjern.
3. Angiv et tal i feltet Faktor.
    * Omregningsfaktor mellem Fra enhed og Til enhed. Omregningsfaktoren fra centimeter til meter er f.eks. 100, fordi der går 100 centimeter på 1 meter.  
4. Indtast eller vælg en værdi i feltet Til-enhed.
5. Vælg en indstilling i feltet Afrunding.
    * Definer, hvordan den omregnede værdi skal afrundes.  
6. Klik på OK.
7. Luk siden.


