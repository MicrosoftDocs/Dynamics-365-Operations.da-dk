--- 
title: "Administrere måleenhed"
description: "Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a>Administrere måleenhed

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


