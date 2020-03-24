---
title: Konfigurere en callcenter-kanal
description: Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 14cee020cc8aead627180343c82bf23534ae83c4
ms.sourcegitcommit: 0681a00d60c9f8cc8f7b9888b8c5ddf07279fc04
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3131725"
---
# <a name="set-up-a-call-center-channel"></a>Konfigurere en callcenter-kanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt


I Dynamics 365 Commerce er et callcenter en type detailkanal, som kan defineres i programmet. Hvis du definerer en kanal til dit callcenter, kan systemet binde specifikke data og ordrebehandlingstandarder til salgsordrer. Mens en virksomhed kan definere flere callcenter-kanaler i Commerce, er det vigtigt at bemærke, at en individuel bruger kun kan knyttes til én callcenter-kanal. 

Før du opretter en ny callcenter-kanal, skal du sikre dig, at du har fuldført [Forudsætningerne for kanalopsætning](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Oprette og konfigurere en ny callcenter-kanal

Følg disse trin for at oprette en ny callcenter-kanal.

1. Gå til **Retail og Commerce \> Kanaler \> Call centre \> Alle call centre** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Skriv et navn til den nye kanal i feltet **Navn**.
1. Vælg den relevante **Juridisk enhed** fra rullelisten.
1. Vælg placeringen af det relevante **Lagersted** fra rullelisten. Dette sted bruges som standard på salgsordrer, som oprettes for denne call centerkanal, medmindre der er defineret andre standarder på kunde- eller vareniveau.
1. Angiv en gyldig standardkunde i feltet **Standardkunde**. Disse data bruges til automatisk udfyldelse af standarder, når der oprettes nye kundeposter. Når du opretter call center-ordrer, er det ikke tilrådeligt at oprette ordrer til standardkunden.
1. Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**. Når der oprettes og behandles call center-ordrer, bruges profilen til mailbeskeder for at udløse automatiske mailpåmindelser til kunder med oplysninger om deres ordrestatus.
1. Angiv en oplysningskode for **Prisændring**. Du skal måske oprette en oplysningskode til dette først. Denne oplysningskode indeholder de sæt årsagskoder, som brugeren vil blive bedt om at vælge mellem, når hun/han bruger funktionaliteten for prisændring på en call center-ordre.
1. Angiv en oplysningskode for **Venteposition**. Du skal måske oprette en oplysningskode til dette først. Denne oplysningskode indeholder de sæt valgfrie årsagskoder, som brugeren vil blive bedt om at vælge mellem, når hun/han sætter en ordre på hold.
1. Angiv en oplysningskode for **Kredit**. Du skal måske oprette en oplysningskode til dette først. Denne oplysningskode indeholder det sæt årsagskoder, som brugeren kan vælge imellem, når hun/han bruger call centerets ordrekreditfunktion for at give kunden diverse refunderinger for årsagen til kundeservice.
1. Valgfrit: Konfigurer økonomiske dimensioner på oversigtspanelet **Økonomiske dimensioner**. De dimensioner, der angives her, vil som standard være i en salgsordre, der er oprettet i denne call center-kanal.
1. Klik på **Gem**.

Følgende billede viser oprettelsen af en ny callcenter-kanal.

![Ny callcenter-kanal](media/channel-setup-callcenter-1.png)

Følgende billede viser et eksempel på en callcenter-kanal.

![Eksempel på call center-kanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Yderligere kanalopsætning

Yderligere opgaver, der kræves til konfiguration af callcenter-kanalen, omfatter opsætning af betalingsmetoder og leveringsmåder.

I følgende billede vises konfigurationsindstillinger til **Leveringsmetoder** og **Betalingsmetoder** under fanen **Opsætning**.

![Yderligere handlinger til konfiguration af callcenter-kanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Hvis du vil oprette betalingsmetoder, skal du følge disse trin for hver af de betalingstyper, der understøttes på denne kanal. Brugerne skal vælge fra foruddefinerede betalingsmetoder for at kæde dem sammen med call center-kanalen. Før du konfigurerer dine call center-betalingsmetoder, skal du først konfigurere dine stambetalingsmåder i **Retail og Commerce \> Konfiguration af kanal \> Betalingsmetoder \> Betalingsmetoder**.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I navigationsruden skal du vælge en betalingsmetode fra de foruddefinerede tilgængelige betalinger.
1. Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen. Ved kreditkort, gavekort eller fordelskundekort skal du udføre yderligere opsætning ved at vælge funktionen **Opsætning af kort**. 
1. Konfigurer korrekte bogføringskonti for betalingstypen i afsnittet **Bogføring**.
1. Klik på **Gem** i handlingsruden.

Følgende billede viser et eksempel på en metode til kontantbetaling.

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Konfigurer leveringsmåder

Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.  

Hvis du vil ændre eller tilføje en leveringsmåde, der skal knyttes til call center-kanalen, skal du følge disse trin.

1. Vælg **Administrer leveringsmåder** i formularen Call centerets leveringsmåder
1. Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.
1. Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje call center-kanalen. Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.
1. Sørg for, at leveringsmåden er konfigureret med data i oversigtspanelet **Produkter** og oversigtspanelet **Adresser**. Hvis ingen produkter eller leveringsadresser er gyldige i forbindelse med leveringsmåden, vil der opstå fejl, hvis du vælger den under ordreindtastning.
1. Når der er foretaget ændringer i call center-tilstanden for leveringskonfigurationer, skal jobbet **Behandling af leveringsmåder** køres for at udfolde ændringsmatrixen. Dette job kan findes ved at navigere til **Retail og Commerce \> Retail og Commerce IT \> Behandling af leveringsmåder**.

Følgende billede viser et eksempel på en leveringsmetode.

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Konfigurer kanalbrugere

Hvis en bruger vil oprette en salgsordre, der er knyttet til call center-kanalen fra Commerce Headquarters, skal denne bruger, der opretter salgsordren, være knyttet til call center-kanalen. Brugeren kan ikke manuelt sammenkæde en salgsordre, der er oprettet i Commerce Headquarters, til call center-kanalen. Sammenkædningen er systematisk og baseret på brugeren og brugerens forhold til call center-kanalen. En bruger kan kun være knyttet til én call center-kanal.

1. Vælg fanen **Kanal** i handlingsruden, og vælg derefter **Kanalbrugere**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg et eksisterende **Bruger-id** på rullelisten for at knytte denne bruger til call center-kanalen

Når kanabrugeren er konfigureret, og brugeren opretter en ny salgsordre i Commerce Headquarters, vil denne salgsordre blive sammenkædet med brugerens tilknyttede call center-kanal. Eventuelle konfigurationer til denne kanal anvendes systematisk på salgsordren. En bruger kan bekræfte, hvilken call center-kanal salgsordren er knyttet til, ved at få vist referencen til kanalnavnet i salgsordrehovedet.


### <a name="set-up-price-groups"></a>Konfigurer prisgrupper

Prisgrupper er valgfrie, men hvis de bruges, kan man styre, hvilke salgspriser der tilbydes til kunder, som placerer ordrer i call center-kanalen. Hvis der ikke er konfigureret en prisgruppe for kunden, eller hvis der ikke anvendes katalogprisgrupper på salgsordren (ved hjælp af feltet **Kildekode-id** i call center-ordrens overskrift), bruges kanalens prisgruppe til at finde varepriser. Hvis der ikke findes en prisgruppe på call center-kanalen, bruges standardvarens stampriser. 

Gør følgende for at oprette en prisgruppe.

1. Klik på fanen **Kanal** i handlingsruden, og vælg derefter **Prisgrupper**.
1. Klik på **Ny** i handlingsruden.
1. Vælg en **Detailprisgruppe** på rullelisten.

## <a name="additional-resources"></a>Yderligere ressourcer

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Funktionalitet til callcenter-salg](call-center-functionality.md)

[Konfigurere indstillinger for callcenter-ordrebehandling](set-up-order-processing-options.md)

[Callcenter-kataloger](call-center-catalogs.md)

[Konfigurere og arbejde med advarsler om svindel](set-up-fraud-alerts.md)

[Oprette kontinuitetsprogrammer for callcentre](set-up-continuity-program.md)
