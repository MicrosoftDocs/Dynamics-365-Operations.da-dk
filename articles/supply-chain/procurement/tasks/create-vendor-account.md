--- 
title: Oprette en kreditorkonto
description: "Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>Oprette en kreditorkonto

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger. Fremgangsmåden viser ikke, hvordan du udfylder alle felter med henblik på købsformål og økonomiske formål. Hvis du vil vide mere om disse felter, skal du læse i feltbeskrivelserne. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Der oprettes typisk kreditorkonti af en indkøber eller debitorpersonale.


## <a name="create-a-vendor-account"></a>Oprette en kreditorkonto
1. Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.
2. Klik på Ny.
3. Skriv en værdi i feltet Kreditorkonto.
    * Værdien udfyldes eventuelt automatisk. Hvis det er tilfældet, kan du springe dette trin over.  
    * Du kan oprette kreditorkonti for en person eller organisation. Dette påvirker, hvilke felter der er tilgængelige. I dette eksempel opretter vi en kreditorkonto for en organisation.   
4. Indtast eller vælg en værdi i feltet Navn.
    * Hvis din kreditor allerede er en registreret part i dit system, kan du bruge rullelisten og vælge den i dette felt. Den nye kreditorkonto arver adresse og kontaktoplysninger, der allerede er registreret.  
5. Indtast eller vælg en værdi i feltet Gruppe.
    * Kreditorgruppen bruges til at gruppere kreditorer, der har en eller flere af følgende parametre til fælles: Betalingsbetingelse, afregningsperiode, finanskonti til lagerbogføring – inklusive momsgruppen, standardfinanskonti, produktfilterkoder eller konfiguration af forsyningsprognose.  
6. Indtast et tal i feltet Antal medarbejdere.
7. Indtast en værdi i feltet Organisationsnummer.

## <a name="add-an-address"></a>Tilføj en adresse
1. Udvid sektionen Adresser.
2. Klik på Tilføj.
3. Indtast eller vælg en værdi i feltet Formål.
    * Du kan vælge ét eller flere formål. Disse bruges til at vælge den korrekte adresse til et bestemt formål. Hvis formålet f.eks. er "Faktura", vil denne adresse blive brugt, når du sender fakturaer.  
4. Skriv en værdi i feltet Navn eller beskrivelse.
5. Indtast eller vælg en værdi i feltet Land/område.
    * Indtast adresseoplysninger. Det land/område, du har valgt, bestemmer de felter, der vises, og de svarer til adresseformatet for landet/området.   
6. Klik på OK.

## <a name="add-contact-information"></a>Tilføj kontaktoplysninger
1. Klik på Tilføj.
2. Skriv en værdi i feltet Beskrivelse.
3. Vælg en indstilling i feltet Type.
4. Skriv en værdi i feltet Kontaktpersons nummer/adresse.
    * Du kan markere afkrydsningsfeltet Primær, hvis dette er den primære kontakt.  
5. Klik på Gem.
6. Luk siden.
7. Luk siden.


