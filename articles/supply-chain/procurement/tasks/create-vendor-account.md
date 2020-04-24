---
title: Oprette en kreditorkonto
description: Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aca23db2a0cc86a2c12ea74d3b1e491643b7efec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207686"
---
# <a name="create-a-vendor-account"></a>Oprette en kreditorkonto

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger. Fremgangsmåden viser ikke, hvordan du udfylder alle felter med henblik på købsformål og økonomiske formål. Hvis du vil vide mere om disse felter, skal du læse i feltbeskrivelserne. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Der oprettes typisk kreditorkonti af en indkøber eller debitorpersonale.


## <a name="create-a-vendor-account"></a>Oprette en kreditorkonto
1. Gå til **navigationsruden > Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Kreditorkonto**.
    - Værdien udfyldes eventuelt automatisk. Hvis det er tilfældet, kan du springe dette trin over.  
    - Du kan oprette kreditorkonti for en person eller organisation. Dette påvirker, hvilke felter der er tilgængelige. I dette eksempel opretter vi en kreditorkonto for en organisation.   
4. Indtast eller vælg en værdi i feltet **Navn**. Hvis din kreditor allerede er en registreret part i dit system, kan du bruge rullelisten og vælge den i dette felt. Den nye kreditorkonto arver adresse og kontaktoplysninger, der allerede er registreret.
5. Indtast eller vælg en værdi i feltet **Gruppe**. Kreditorgruppen bruges til at gruppere kreditorer, der har en eller flere af følgende parametre til fælles: betalingsbetingelse, afregningsperiode, finanskonti til lagerbogføring – inklusive momsgruppen, standardfinanskonti, produktfilterkoder eller konfiguration af forsyningsprognose.
6. Indtast et tal i feltet **Antal medarbejdere**.
7. Indtast en værdi i feltet **Organisationsnummer**.

## <a name="add-an-address"></a>Tilføj en adresse
1. Udvid sektionen **Adresser**.
2. Klik på **Tilføj**.
3. Indtast eller vælg en værdi i feltet **Formål**. Du kan vælge ét eller flere formål. Disse bruges til at vælge den korrekte adresse til et bestemt formål. Hvis formålet f.eks. er "Faktura", vil denne adresse blive brugt, når du sender fakturaer.
4. Skriv en værdi i feltet **Navn eller beskrivelse**.
5. Indtast eller vælg en værdi i feltet **Land/område**. Indtast adresseoplysninger. Det land/område, du har valgt, bestemmer de felter, der vises, og de svarer til adresseformatet for landet/området. 
6. Klik på **OK**.

## <a name="add-contact-information"></a>Tilføj kontaktoplysninger
1. Udvid sektionen **Kontaktoplysninger**.
2. Klik på **Tilføj**.
3. Indtast en værdi i feltet **Beskrivelse**.
4. Vælg en indstilling i feltet **Type**.
5. Skriv en værdi i feltet **Kontaktpersons nummer/adresse**. Du kan markere afkrydsningsfeltet Primær, hvis dette er den primære kontakt.  
6. Klik på **Gem**.
7. Luk siden.
8. Luk siden.

