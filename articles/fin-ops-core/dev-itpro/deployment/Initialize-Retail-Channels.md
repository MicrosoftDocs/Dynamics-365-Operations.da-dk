---
title: Initialisere Commerce Scale Unit (sky)
description: Denne artikel forklarer, hvordan du initialiserer Commerce Scale Unit (sky) i Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 6b42252a37f01a2b387c2393760998a6b2e4761d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271509"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Initialisere Commerce Scale Unit (sky)

[!include[banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du initialiserer Commerce Scale Unit (sky) i Microsoft Dynamics 365 Commerce.

Hvis du bruger et sandkasse- eller produktionsmiljø på niveau 2, der har programversion 8.1.2.x eller senere, skal du initialisere Commerce Scale Unit (sky), før du kan bruge detailkanalfunktionalitet til POS-handlinger eller til handlinger for e-handel, der bruger Retail Server i skyen. Initialisering implementerer en Commerce Scale Unit (sky).

> [!IMPORTANT]
> For eksisterende kunder, der bruger detailkanalfunktioner i skyen, kræver vi, at du opdaterer dine detailkanaler til at bruge Commerce Scale Unit for at sikre fortsat og ubrudt understøttelse af dit firma. Nye miljøer, der implementeres uden Commerce Scale Unit, modtager ikke længere kvalitets- og tjenesteopdateringer til detailkanalkomponenter, der har vært i skyen. Der er ingen handling påkrævet for kunder, der udelukkende bruger Commerce Scale Unit (selvhostet). Kontakt din Microsoft FastTrack Solution Architect, hvis du vil have en udvidelse.

## <a name="prerequisites"></a>Forudsætninger

1. Udrul et sandkasse- eller produktionsmiljø på niveau 2, der har version 8.1.2.x eller en senere version.
2. Du kan selv udrulle op til Commerce Scale Unit pr. miljø. Hvis du har brug for mere end to Commerce Scale Unit pr. miljø, skal du i Microsoft Dynamics Lifecycle Services (LCS) oprette en supportanmodning og angive **Anmodning om yderligere Commerce Scale Unit** og angive miljø-id, antal Commerce Scale Unit og de ønskede datacenterområder. Anmodningen fuldføres inden for fem arbejdsdage. Hvis du ikke kræver mere end to Commerce Scale Unit pr. miljø, behøver du ikke oprette en supportanmodning. 
3. Du skal have rettigheden Projektejer i Lifecycle Services, før du kan initialisere Commerce Scale Unit.
4. Kontrollér, at konfigurationsnøgler til Retail-licens er aktiveret i dit miljø. Du kan få flere oplysninger i [Rapport over licenskoder og konfigurationsnøgler](../sysadmin/license-codes-configuration-keys-report.md). Du skal have følgende nøgler aktiveret for at kunne bruge Commerce Scale Unit.

    - RetailBasic
    - RetaileCommerce – Hvis du planlægger at bruge e-handel til Dynamics 365 Commerce.
    - RetailGiftCard – Hvis du planlægger at bruge gavekort.
    - RetailInvent – Hvis du planlægger at bruge lager.
    - RetailModernPos – Hvis du planlægger at bruge POS.
    - RetailReplenishment – Hvis du planlægger at bruge genopfyldninger.
    - RetailScheduler
    - RetailStores – Hvis du planlægger at bruge POS.


## <a name="region-availability"></a>Områdetilgængelighed
Commerce Scale Unit kan installeres i følgende områder.

| Global placering | Område              | Tilgængelighed        | Bemærkninger                  |
|-----------------|---------------------|---------------------|---------------------------|
| Nord- og Sydamerika        | Det østlige USA             | Generelt tilgængelig |  Ingen kommentarer.                         |
| Nord- og Sydamerika        | Det østlige USA 2           | Generelt tilgængelig |  Ingen kommentarer.                          |
| Nord- og Sydamerika        | Den nordlige del af det centrale USA    | Begrænset kapacitet    |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Den sydlige del af det centrale USA    | Begrænset kapacitet    |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Det centrale USA          | Generelt tilgængelig |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Det vestlige USA             | Generelt tilgængelig |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Det vestlige USA 2           | Generelt tilgængelig |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Det centrale Canada      | Begrænset kapacitet    |  Ingen kommentarer.                            |
| Nord- og Sydamerika        | Det østlige Canada         | Begrænset kapacitet    |   Ingen kommentarer.                           |
| Nord- og Sydamerika        | Det vestlige centrale USA     | Begrænset kapacitet    |   Ingen kommentarer.                           |
| APAC            | Østaustralien      | Generelt tilgængelig |   Ingen kommentarer.                           |
| APAC            | Sydøstasien      | Kapacitetsbegrænsede | Ingen installationer tilladt.    |
| APAC            | Østjapan          | Generelt tilgængelig |  Ingen kommentarer.                            |
| APAC            | Vestjapan          | Generelt tilgængelig |   Ingen kommentarer.                           |
| APAC            | Sydøstaustralien | Generelt tilgængelig |   Ingen kommentarer.                           |
| APAC            | Østasien           | Begrænset kapacitet    |   Ingen kommentarer.                           |
| APAC            | Det sydlige Indien         | Kapacitetsbegrænsede | Ingen installationer tilladt.    |
| APAC            | Det centrale Indien       | Begrænset kapacitet    | Kræver godkendelsesproces. |
| EMEA            | Vesteuropa         | Begrænset kapacitet    | Ingen tilgængelige i LCS i øjeblikket. |
| EMEA            | Nordeuropa        | Begrænset kapacitet    | Ingen tilgængelige i LCS i øjeblikket. |
| EMEA            | Det sydlige Storbritannien            | Generelt tilgængelig |    Ingen kommentarer.                          |
| EMEA            | Det vestlige Storbritannien             | Generelt tilgængelig |    Ingen kommentarer.                          |
| Schweiz     | Det nordlige Schweiz   | Begrænset kapacitet    | Kræver godkendelsesproces. |
| Forenede Arabiske Emirater             | Det nordlige Forenede Arabiske Emirater           | Begrænset kapacitet    | Kræver godkendelsesproces. |

Udrulningskapacitet i områder med begrænset kapacitet er særdeles begrænset. Anmodninger om udrulning evalueres fra sag til sag. Hvis du har et vigtigt forretningsbehov for udrulning i områder med begrænset kapacitet, kan du indsende en supportanmodning, der skal føjes til ventelisten. Kapacitetsbegrænsede områder tillader i øjeblikket ikke udrulning af Commerce Scale Unit. 

![Kort, der viser tilgængelighed i området.](media/Commerce-Scale-Unit-Region-Availability.png "Kort, der viser tilgængelighed i området")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Initialisere Commerce Scale Unit som del af en ny miljøudrulning

Kontrollér, at hovedkontoret er tilgængeligt. Dette kræves for at registrere skalaenheden hos hovedkontoret under initialiseringsprocessen. Det anbefales ikke at initialisere en skalaenhed, når hovedkontoret er under servicering, da det muligvis ikke bliver tilgængeligt under serviceringsprocessen.

1. Kontrollér, at hovedkontormiljøet er tilgængeligt og ikke i [vedligeholdelsestilstand](../sysadmin/maintenance-mode.md).
2. I LCS skal du vælge **Miljøfunktioner \> Commerce** på siden med miljødetaljer.
3. Vælg **Initialiser** på udrulningssiden Konfiguration af Commerce.
4. Vælg den version af Commerce Scale Unit, der skal initialiseres.
5. Vælg et område, hvor Commerce Scale Unit skal initialiseres.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurere kanaler til brug af Commerce Scale Unit

Når Commerce Scale Unit er blevet implementeret, skal du sikre dig, at dine kanaler er konfigureret til at bruge databasen for den. 

Hvis du vil konfigurere kanalerne til at bruge Commerce Scale Unit-databasen, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Commerce headquarters \> Commerce-planlægger \> Kanaldatabase**.
1. Vælg en kanaldatabase i venstre rude.
1. Vælg **Tilføj** i oversigtspanelet **Detailkanal**, og vælg derefter din detailkanal på rullelisten.
1. Vælg **Tilføj**, og vælg derefter onlinekanalen på rullelisten. 

Gå derefter til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**, og kør job 9999.

> [!NOTE] 
> Job 9999 synkroniserer alle nye produkter og kunder til Commerce Scale Unit. Denne proces kan tage lang tid. Hvis kanalen kun skal være tilgængelig for konfiguration af webstedsgenerator for e-handel, kan du køre job 1070 i stedet for job 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Databaseopdatering og Commerce Scale Unit

Før du går i gang, skal du sørge for, at du er fortrolig med [Trin, der skal fuldføres, efter at du har opdateret databasen for miljøer, der bruger funktionen Commerce](../database/database-refresh.md).

Databaseposterne for skalaenhedskanalen (i formen Kaneldatabase) kan ikke flyttes på tværs af miljøer som en del af databaseopdateringen. Det skyldes, at posterne repræsenterer en miljøspecifik konfiguration.

Efter databaseopdateringen kan du generere skalaenhedens kanaldatabasepost igen ved at udstede en ny implementering af skalaenheden i LCS. Alle implementerings- og servicehandlinger i skalaenheden forsøger at registrere skalaenheden hos hovedkontoret, hvis registreringen mangler.

Du kan udstede en ny implementering af skalaenheden uden at ændre komponenter ved at vælge at implementere den samme version, som din skalaenhed er i. Dette kan gøres i LCS ved hjælp af følgende trin:

1. I LCS skal du vælge **Miljøfunktioner \> Detail** på siden med miljødetaljer.
2. Vælg den skalaenhed, du vil implementere igen, på udrulningssiden.
3. Vælg **Opdater** i skalaenhedens handlingsmenu.
4. Vælg indstillingen **Angiv en version** på rullelisten for **Vælg version** på skyderen.
5. I tekstboksen under **Angiv en version** skal du angive den version, der vises for skalaenheden, som står ud for navnet **Aktuel version**.
6. Klik på knappen **Opdater**.

Du behøver ikke at vælge **Opdater udvidelser**, heller ikke selvom du tidligere har anvendt udvidelser, da den sidste udvidelsespakke, der er anvendt på skalaenheden, automatisk plukkes, når du opdaterer en skalaenhed.

Hvis du har flere skalaenheder, skal du udføre operationen ovenfor for hver skalaenhed. Du kan udføre disse operationer parallelt, hvis du ønsker det.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Udrulle yderligere Commerce Scale Unit (valgfrit)

Når du har initialiseret Commerce Scale Unit, kan du slev udrulle endnu en Scale Unit, hvis din licens giver dig ret til at gøre det. Hvis du vil udrulle mere end to Commerce Scale Unit, skal du oprette en supportanmodning. I supportanmodningen skal du angive det antal Commerce Scale Unit, du har brug for, navnet på miljøet og de ønskede områder. Du kan finde flere oplysninger om licenser i [Licensvejledning til Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

For hver ekstra Commerce Scale Unit, du udruller, anbefales det, at du opretter en separat kanaldatabasegruppe ved at følge disse trin.

1. Gå i Commerce-hovedkontoret til **Retail og Commerce > Retail Headquarters > Konfiguration af Retail planlægger > Kanaldatabasegruppe**.
2. Opret en ny kanaldatabasegruppe.
3. Gå til **Retail og Commerce > Retail Headquarters > Konfiguration af Retail planlægger > Kanaldatabase**, og vælg den kanaldatabase, der svarer til den nyoprettede Commerce Scale Unit.
4. Vælg **Rediger,** og vælg den nye kanaldatabasegruppe.
5. Vælg **Gem**.
6. Vælg **Kør fuld datasynkronisering** for den valgte kanaldatabase.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Ekstra overvejelser, hvis du initialiserer Commerce-kanalkomponenter, der er hostet skyen, i et eksisterende miljø

Hvis du allerede bruger Commerce-kanalkomponenter, der er hostet skyen, i et miljø, reducerer initialiseringen af Commerce Scale Unit nedetiden, når disse komponenter opdateres. Der kræves yderligere planlægning, før Commerce Scale Unit initialiseres.

Når du initialiserer den første Commerce Scale Unit i et miljø, der bruger Commerce-kanalkomponenter, der er hostet i skyen, overfører initialiseringsprocessen de kanaler, der er knyttet til de kanalkomponenter, der er hostet i skyen, til den første skaleringsenhed. Kanaler, der er tilknyttet Store Scale Unit, ændres ikke.

Overførselsprocessen er transparent for kanalerne. Når initialiseringen af skalaenheden er startet, udføres følgende operationer automatisk:

1. Der oprettes en ny Commerce Scale Unit, som knyttes til miljøet.
2. Denne Commerce Scale Unit registreres som en tilgængelig kanaldatabase i hovedkontoret.
3. Alle de kanaler, der er tilknyttet **Standard**-kanaldatabasen i hovedkontoret, opdateres, så de knyttes til den nye Commerce Scale Unit.
4. Der udføres fuld Commerce Data Exchange-datasynkronisering (CDX) for at føre kanaldataene til den nye skalaenhed.

**Planlægning og test af initialisering af Commerce Scale Unit** Som en generel regel skal du, når du initialiserer Commerce Scale Unit, planlægge en fem timers nedetidsramme for butikshandlinger og eventuelle e-handelskanalhandlinger, der bruger Retail Server eller Cloud POS.

1. Udfør en databaseopdatering fra produktionsmiljøet til et sandkasse-UAT-miljø. 
2. Initialiser Commerce Scale Unit i sandkasse-UAT-miljøet. 
3. Bemærk initialiseringens fuldførelsestid for Commerce Scale Unit. Dette vil være sammenligneligt med den tid, som denne operation tager i produktionsmiljøet, hvor butikshandlinger og e-handel ikke vil være tilgængelige.

Du skal udføre følgende yderligere trin, før du initialiserer Commerce Scale Unit.

- **Luk alle POS-skifter** – Efter overflytningen vil brugere af POS ikke kunne lukke skifter, der var aktive under overflytningsprocessen.
- **Kontrollér, at alle P-job er fuldført korrekt** – Det anbefales, at P-job til synkronisering af ventende transaktioner er fuldført, inden CSU initialiseres.
- **Log af alle POS-enheder** – POS-handlinger understøttes ikke under overflytningen.
- **Tilbagekald og ugyldiggør alle suspenderede transaktioner i POS** – Suspenderede transaktioner bevares ikke som en del af initialiseringen.

> [!IMPORTANT]
> Som en del af initialiseringen af Commerce Scale Unit vil tidligere suspenderede transaktioner gå tabt og kan ikke tilbagekaldes. 

Her kan du se, hvad der sker i initialiseringsperioden:

- Commerce-kanaler, der er hostet i skyen, fungerer ikke, medmindre du aktiverer POS-offlinefunktionaliteten.
- POS-enheder med offlinefunktionalitet aktiveret vil have reduceret funktionalitet.
- Alle e-handelsklienter, der er afhængige af Retail Server, vil blive afbrudt.
- Kanaler, der er hostet på Commerce Scale Units (selvhostet), påvirkes ikke.
- Hovedkontorets funktionalitet påvirkes ikke.

Her kan du se, hvad der sker, efter at initialiseringen er fuldført:

- Enhedaktiveringstilstanden for alle aktiverede POS-enheder bevares, hvilket betyder, at enhederne ikke behøver at blive genaktiveret.
- Enkeltstående hardwarestationsforekomster vil fortsat fungere.
- Rapporter på POS-kanalsiden nulstilles og viser ikke data fra før initialiseringen.
- Vis kladde-handlingen nulstilles også og viser ikke data fra før initialiseringen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
