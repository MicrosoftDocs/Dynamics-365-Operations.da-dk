---
title: Planlæg vedligeholdelsesplaner
description: I dette emne beskrives tidsplaner for vedligeholdelse i Styring af aktiver.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bd5192f727c83c017148405fb1b3ee587c118542450d46b5822d86cd1676d8fd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731313"
---
# <a name="schedule-maintenance-plans"></a>Planlæg vedligeholdelsesplaner

[!include [banner](../../includes/banner.md)]

 

Forebyggende vedligeholdelsesplanlægning opretter kalenderposter for aktiver, baseret på de vedligeholdelsesplaner, der er konfigureret for aktiverne. Du kan planlægge kalenderposter på basis af udvalgte vedligeholdelsesplaner, aktivtyper og aktiver.

1. Klik på **Styring af aktiver** > **Periodisk** > **Forebyggende vedligeholdelse** > **Planlægge vedligeholdelsesplaner**.

2. Du kan vælge et tidsinterval i felterne **Periode** og **Periodefrekvens**.

>[!NOTE]
>Felterne **Periode** og **Periodefrekvens** angiver, hvor langt forud i tiden du ønsker, at der skal oprettes vedligeholdelsesplanlægningslinjer baseret på de vedligeholdelsesplaner, du har oprettet (tidsbaseret eller tællerbaseret). I nedenstående figur oprettes vedligeholdelsesplanlægningslinjer (= arbejdsordreforslag) fra dags dato og tre måneder frem.

3. Vælg "Ja" på til/fra-knappen **Opret automatisk, hvis det er angivet på linjen**, hvis der automatisk skal oprettes arbejdsordrer i henhold til vedligeholdelsesplanlinjen.

>[!NOTE]
>Hvis denne til/fra-knap er indstillet til **ja**, og afkrydsningsfeltet til *automatisk oprettelse* også er markeret på vedligeholdelsesplanlinjer i **Vedligeholdelsesplaner**, oprettes arbejdsordrer baseret på vedligeholdelsesplanlinjerne, og der oprettes også vedligeholdelsestidsplanslinjer med status "Oprettet af arbejdsordre ". Hvis der kun er valgt én indstilling (på knappen **Opret automatisk, hvis det er angivet på linjen** i denne dialogboks eller i afkrydsningsfeltet til **automatisk oprettelse** i formularen **Vedligeholdelsesplaner**), oprettes kun vedligeholdelsestidsplanslinjer med status "Oprettet". Hvis det er tilfældet, oprettes der ingen arbejdsordrer.

4. Det er muligt at generere kalenderposter, der er baseret på vedligeholdelsesplaner (tid eller tæller), aktiver, aktivtyper, arbejdssteder og arbejdsstedstyper. Klik på knappen **Filter**, og foretag dine valg, hvis det er nødvendigt.

- Med hensyn til planlægning af vedligeholdelsesplaner på arbejdssteder: Hvis du opdaterer opsætningen af aktivtyper, producenter og modeller på vedligeholdelsesplaner i **Alle arbejdssteder** >  oversigtspanelet **Vedligeholdelsesplaner**, når du har planlagt vedligeholdelsesplaner, bliver eksisterende poster i vedligeholdelsesplanen, der er relateret til dette arbejdssted, automatisk slettet. Hvis du vil oprette nye kalenderposter, der svarer til den opdaterede opsætning af vedligeholdelsesplanen på arbejdsstedet, skal du køre en ny tidsplan for vedligeholdelsesplanen for dette arbejdssted. Du kan finde flere oplysninger om opsætning af aktivtyper, producenter og modeller i forbindelse med arbejdssteder i [Oprette arbejdssteder](../functional-locations/create-functional-locations.md).

>*Eksempel:* Du vil oprette en vedligeholdelsesplan for et bestemt arbejdssted, hvilket betyder, at alle aktiver, der er konfigureret på dette arbejdssted på et givet tidspunkt, medtages, når du planlægger vedligeholdelsesplanen. I dette tilfælde skal du oprette en vedligeholdelsesplan og vælge det specifikke arbejdssted, men du må IKKE tilføje nogen aktiver i vedligeholdelsesplanen. Resultatet er, at når du planlægger denne vedligeholdelsesplan, oprettes der vedligeholdelsestidsplanslinjer for alle de aktiver, der er knyttet til arbejdsstedet på det pågældende tidspunkt.

- Hvis du foretager ændringer af aktivtyper, producenter og modeller i **Aktivtyper**, påvirker disse ændringer kun nye aktiver, der bruger den opdaterede aktivtype. Læs mere om opsætning af aktivtype under [Aktivtyper](../setup-for-objects/object-types.md).  

5. Klik på **OK** for at starte genereringen af poster i vedligeholdelsesplanen for aktiver. De genererede poster bliver vist på listesiden **Alle vedligeholdelsestidsplaner**. I følgende illustration vises et eksempel på dialogboksen **Planlæg vedligeholdelsesplaner**.

![Figur 1.](media/09-preventive-maintenance.png)

- I dialogboksen **Planlæg vedligeholdelsesplaner** kan du definere batchjob, der skal køres i oversigtspanelet **Kør i baggrunden**, så der automatisk genereres kalenderposter med jævne mellemrum.  
- Når du planlægger en forebyggende vedligeholdelse, oprettes der ikke vedligeholdelsestidsplanslinjer med forventet startdato og -klokkeslæt før systemdatoen og -klokkeslættet.  

I figuren nedenfor vises en grafisk illustration af en tidsbaseret beregning af vedligeholdelsesplanen.  

![Figur 2.](media/10-preventive-maintenance.jpg)

Vedrørende tællerbaserede vedligeholdelsesplaner: I nedenstående figurer vises to forskellige cyklusser for tællerregistrering. De er baseret på en vedligeholdelsesplan, der er konfigureret for aktivet "V0001", og det forventes, at aktivet (en bil) kører ca. 2.000 km hver måned.

I det første eksempel nås de forventede 2.000 km ikke hver måned. Ifølge den tællerbaserede vedligeholdelsesplan er grænsen 2.000 km, hvilket betyder, at når du kører en planlægning af en vedligeholdelsesplan, skal der oprettes en vedligeholdelsestidsplanslinje, hver gang grænsen på 2.000 kilometer nås. I eksempel 1 er der fire registreringslinjer, men 2.000 kilometergrænsen nås kun én gang. Det betyder, at når du kører planlægning af vedligeholdelsesplaner for dette aktiv, f.eks. i en periode på tre måneder, oprettes der kun én vedligeholdelsestidsplanslinje.

I den næste figur registreres 2.000 km eller mere hver måned. Derfor oprettes der tre vedligeholdelseslinjer, hvis du planlægger vedligeholdelsesplaner for dette aktiv for en 3-måneders periode. 

De eksempler, der beskrives her, viser, at alle de tællerregistreringer, der udføres på et aktiv, viser en tendens, der beskriver slitagen på aktivet. Denne tendens bruges som beregningsgrundlag på tidspunktet for planlægningen af vedligeholdelsesplanen.

![Figur 3.](media/11-preventive-maintenance.png)

![Figur 4.](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]