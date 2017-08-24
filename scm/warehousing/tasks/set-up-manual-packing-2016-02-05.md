--- 
title: Konfigurere manuel emballering (kun februar og maj 2016)
description: "Pakningsprocessen gør det muligt at validere og pakke af produkter i containere."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Konfigurere manuel emballering (kun februar og maj 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Pakningsprocessen gør det muligt at validere og pakke af produkter i containere. I denne proces plukker lagermedarbejdere produkter fra lagerplaceringerne og flytter dem til en pakkestation, hvor de kan kontrollere vareantal og -typer og tildele dem til passende containere. Når en container er helt pakket, kan de lukke den og flytte den til forsendelsesområderne, og produkterne er klar til afsendelse. Denne procedure bruger demofirmaet USMF. Denne procedure er kun for februar 2016- og maj 2016-versionerne af Dynamics 365 for Operations.


## <a name="set-up-location-profiles"></a>Konfigurer lokationsprofiler
1. Gå til Lagerstedsstyring > Konfiguration > Lagersted > Lokationsprofiler.
2. Klik på Ny.
    * Lokationsprofilen bruges til pakkestationer og indeholder oplysninger om og regler for en lokation.  
3. Skriv en værdi i feltet Id for lokationsprofil.
4. Skriv en værdi i feltet Navn.
5. Indtast eller vælg en værdi i feltet Lokationsformat.
6. Indtast eller vælg en værdi i feltet Lokationstype.
7. Vælg Ja i feltet Tillad blandede varer.
8. Vælg Ja i feltet Tillad blandede lagerstatusser.
9. Vælg Ja i feltet Tilsidesæt regler for batchdage.
10. Luk siden.

## <a name="set-up-warehouse-management-parameters"></a>Konfigurere lagerstyringsparametre 
1. Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.
2. Klik på fanen Emballage.
3. Indtast eller vælg en værdi i feltet Profil-id for pakkelokation.
    * Vælg den lokationsprofil, du vil bruge til pakning.  
4. Luk siden.

## <a name="set-up-container-types"></a>Konfigurere containertyper
1. Gå til Lagerstedsstyring > Konfiguration > Containere > Containertyper.
2. Klik på Ny.
    * Du kan definere de containertyper, der skal bruges. Du kan angive containerens fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde og vægt.  Attributterne er brugerdefinerede felter, der gør det muligt at tilføje ekstra dimensioner til containertypen.     
3. Indtast en værdi i feltet Containertypekode.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Taravægt.
6. Angiv et tal i feltet Maksimal vægt.
7. Angiv et tal i feltet Volumen.
8. Angiv et tal i feltet Længde.
9. Indtast et tal i feltet Bredde.
10. Indtast et tal i feltet Højde.
11. Klik på Gem.
12. Luk siden.

## <a name="set-up-packing-profiles"></a>Konfigurere pakkeprofiler
1. Gå til Lagerstedsstyring > Konfiguration > Emballage > Pakkeprofiler.
2. Klik på Ny.
3. Skriv en værdi i feltet Pakkeprofil-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Indtast eller vælg en værdi i feltet Profil-id for lukning af container.
    * Det er valgfrit at angive et profil-id for containerlukning, og det er standardprofilen for containerlukning for denne pakkeprofil.  
6. Vælg en indstilling i feltet Tilstanden Container-id.
    * Denne indstilling bestemmer, om der automatisk genereres et container-id, når der oprettes en container, eller der oprettes et container-id manuelt.  
7. Indtast eller vælg en værdi i feltet Containertype.
    * Containertypen vil blive brugt som standard, når der oprettes en ny container.  
8. Markér afkrydsningsfeltet Opret automatisk container ved containerlukning.
9. Klik på Gem.
10. Luk siden.

## <a name="set-up-container-closing-profiles"></a>Konfigurere profiler for containerlukning
1. Gå til Lagerstedsstyring > Konfiguration > Containere > Profiler for lukning af container.
    * Containerlukningsprofiler definerer, hvad der sker, når en container er lukket. Du kan oprette flere containerlukningsprofiler.       
2. Klik på Ny.
3. Skriv en værdi i feltet Profil-id for lukning af container.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Manifest kl.
    * Angiv, om der bruget et manifest ved lukning af containere eller bekræftelse af leverancen. Bemærk, at brug af et manifest kræver transportstyring. Der skal implementeres et manifest i transportprogrammer, for at det kan fungere.  
6. Indtast eller vælg en værdi i feltet Lagersted.
7. Indtast eller vælg en værdi i feltet Standardlokation til endelig forsendelse.
    * Dette er den lokation, som produkter skal flyttes til, når containerne er lukkede. Denne lokation skal have en lokationsprofil, der er defineret i Lagerstedsparametre.  
8. Indtast eller vælg en værdi i feltet Vægtenhed.
9. Klik på Gem.


