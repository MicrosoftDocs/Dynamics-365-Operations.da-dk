---
title: Konfigurer en detailkanal
description: Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113822"
---
# <a name="set-up-a-retail-channel"></a>Konfigurer en detailkanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Dynamics 365 Commerce understøtter flere detailkanaler. Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker). Hver detailbutikskanal kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere. Du skal oprette alle disse elementer, for at du kan oprette en detailbutikskanal. 

Før du opretter en detailkanal, skal du sikre dig, at du følger [kanalens forudsætninger](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Oprette og konfigurere en ny detailkanal

1. Gå til **Moduler \> Kanaler \> Butikker \> Onlinebutikker** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Skriv et navn til den nye kanal i feltet **Navn**.
1. Angiv et entydigt butiksnummer i feltet **Butiksnummer**. Nummeret kan være alfanumerisk med højst 10 tegn.
1. Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.
1. Angiv det relevante **Lagersted** på rullelisten Lagersted.
1. Vælg den relevante tidszone i feltet **Lagertidszone**.
1. Vælg en relevant for momsgruppe butikken på rullelisten **Momsgruppe**.
1. Vælg den relevante valuta i feltet **Valuta**.
1. Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.
1. Angiv en gyldig standardkunde i feltet **Standardkunde**.
1. Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil**, hvis det er relevant.
1. Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser oprettelsen af en ny detailkanal.

![Ny detailkanal](media/channel-setup-retail-1.png)

Følgende billede viser et eksempel på en detailkanal.

![Eksempel på detailkanal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Andre indstillinger

Der er adskillige andre valgfrie indstillinger, du kan angive i sektionerne **Opgørelse/ultimo** og **Diverse**, afhængigt af behovene i detailbutikken.

Du kan også se [Skærmlayout til POS](pos-screen-layouts.md) for at få oplysninger om, hvordan du konfigurerer standardskærmlayoutet, i afsnittet **Skærmlayout** og [Konfigurerer og installerer Retail hardware Station](retail-hardware-station-configuration-installation.md) for at få oplysninger om installation af afsnittet **Hardwarestationer**.

Følgende billede viser et eksempel på konfiguration af en detailkanal.

![Eksempel på detailkanalkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Yderligere kanalopsætning

Der er flere elementer der skal konfigureres for en kanal, som kan findes i **Handlingsrude** under sektionen **Konfigurer**.

Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, kontantopgørelse, leveringsmetoder, indtægts/udgiftskonto, sektioner gruppetildeling for opfyldelse og pengeskabe.

I følgende billede vises de yderligere indstillinger for opsætning af detailkanal under fanen **Opsætning**.

![Konfigurer kanal](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg den ønskede betalingsmetode i navigationsruden.
1. Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.
1. Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en metode til kontantbetaling.

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Opsætning af kontantopgørelse

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Kontantopgørelse**.
1. Vælg **Ny** i handlingsruden, og opret derefter alle relevante **Mønter** og **Pengesedler**.

Følgende billede viser et eksempel på en kontantopgørelse.

![Opsætning af kontantopgørelser](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Konfigurer leveringsmåder

Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.  

Udfør følgende trin for at ændre eller tilføje en leveringsmetode.

1. Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.
1. Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.
1. Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen. Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.

Følgende billede viser et eksempel på en leveringsmetode.

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Konfigurer indtægts/udgiftskonto

Gør følgende for at konfigurere en indtægts/udgiftskonto.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Indtægts/udgiftskonto**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et navn under **Navn**.
1. Angiv et søgenavn under **Søgenavn**.
1. Angiv kontotypen under **Kontotype**.
1. Angiv tekst for **Meddelelseslinje 1**, **Meddelelseslinje 2**, **Bilag 1** og **Bilag 2** efter behov.
1. Angiv bogføringsoplysninger under **Bogføring**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en indtægts/udgiftskonto.

![Konfigurer indtægts/udgiftskonti](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Konfigurere sektioner

Gør følgende for at konfigurere sektioner.

1. I handlingsruden skal du vælge **Sektioner** under **Opsætning**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et sektionsnummer under **Sektionsnummer**.
1. Indtast en beskrivelse under **Beskrivelse**.
1. Angiv en sektionsstørrelse under **Sektionsstørrelse**.
1. Konfigurer yderligere indstillinger for **Generelt** og **Salgsstatistik** efter behov.
1. Gå til handlingsruden, og vælg **Gem**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Konfigurer en gruppetildeling for opfyldelse

Gør følgende for at konfigurere en gruppetildeling for opfyldelse.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.
1. Indtast en beskrivelse i rullelisten **Beskrivelse**.
1. Gå til handlingsruden, og vælg **Gem**

Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.

![Konfigurer gruppetildelinger for opfyldelse](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Konfigurer pengeskabe

Gør følgende for at konfigurere pengeskabe.

1. I handlingsruden skal du vælge **Pengeskabe** under **Opsætning**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et navn til pengeskabet.
1. Gå til handlingsruden, og vælg **Gem**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurere en onlinekanal](channel-setup-online.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)

