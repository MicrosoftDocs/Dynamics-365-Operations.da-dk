---
title: Kalendere og varedisponering
description: Dette emne indeholder en oversigt over forsyningskædekalendere, og hvordan de påvirker varedisponeringen.
author: t-benebo
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dcc66549bf6bdd67438bea9ac3c29c3f01e2674e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841761"
---
# <a name="calendars-and-master-planning"></a>Kalendere og varedisponering

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over forsyningskædekalendere, og hvordan de påvirker varedisponeringen.  De forskellige kalendere, der bruges i varedisponeringsprogrammet, gennemgås, herunder hvordan de påvirker datoerne for afsendelse og modtagelse i de planlagte ordrer. Til slut får du anbefalinger vedrørende tildeling, brug og opdatering af kalenderne.

## <a name="definition-of-a-calendar"></a>Definition af en kalender

Du kan definere en kalender, der skal bruges i organisationen, på siden i **Organisationsadministration > Opsætning > Kalendere > Kalendere**. 

Hver datoangivelse i en kalender kan være **åben** eller **lukket** eller **basiskalender**. Dette angives i kolonnen **Kontrol** på siden **Arbejdstider**. For hver dato: 
- **Åben** - Angiver, at der udføres arbejde på den valgte dag. Kalenderen opdateres i overensstemmelse med skabelonen for arbejdstiden.
- **Lukket** - Angiver arbejde, der ikke udføres arbejde den valgte dag. 
- **Basiskalender** - Angiver, at en bestemt dato arver arbejdstider og åben/lukket fra basiskalenderen. Når basiskalenderen opdateres, arver den valgte kalender derfor operationstider fra den. 

Ved lukkede datoer tildeles afkrydsningsfeltet **Lukket for afhentning** automatisk. Ved åbne datoer kan du manuelt vælge indstillingen **Lukket for afhentning**. Dette angiver, at der udføres arbejde på datoen, men ikke afsendelse. 

## <a name="calendars-that-affect-master-planning"></a>Kalendere, der påvirker varedisponering

### <a name="calendar-for-a-coverage-group"></a>Kalender for en disponeringsgruppe
En disponeringsgruppe angiver et fælles sæt parametre, der bruges til genopfyldning af de varer, der hører til den angivne disponeringsgruppe. 

Hvis du vil tilføje en kalender for en disponeringsgruppe, skal du gå til **Overordnet planlægning > Konfiguration > Disponering > Disponeringsgrupper**. Find den disponeringsgruppe, som du vil tildele kalenderen til, og vælg den derefter i feltet **Kalender**.

Disponeringsgruppen kan tildeles på forskellige sider: 
    - På siden **Frigivne produktdetaljer** for en vare. Du kan se disponeringsgruppen for en vare ved at gå til **Administration af produktoplysninger > Produkter > Frigivne produkter** og vælge varen for at gå til siden **Oplysninger om frigivne produkter**. Du kan se disponeringsgruppen for varen i oversigtspanelet **Plan**.
    - På siden **Varedisponering**. På siden med oplysninger om frigivne produkter skal du klikke på **Varedisponering** for at gå til varedisponeringssiden. Du kan se forskellige parametre for genopfyldning under oversigtsfanen afhængigt af lokation, lagersted og produktdimensioner. Disponeringsgruppen for hver vare nedarves fra disponeringsgruppen på siden **Frigivne produktdetaljer**. Dette kan tilsidesættes ved hjælp af **Brug bestemte indstillinger** eller **Tilsidesæt indstilling for gruppe** under fanen **Generelt**.
    - På siden **Varedisponeringsparametre**. Hvis der ikke er angivet en disponeringsgruppe for en vare på de foregående sider, tager varedisponeringen den standarddisponeringsgruppe, der er angivet under varedisponeringsparametrene. Dette er angivet i **Varedisponering > Opsætning > Varedisponeringsparametre** i feltet **Standarddisponeringsgruppe**. 

### <a name="calendar-for-a-vendor"></a>Kalender for en leverandør
For at angive arbejdsdagene for en leverandør kan du tildele en indkøbskalender til leverandøren på siden **Standardindstillinger for indkøbsordrer** for en leverandør. 

Hvis du vil angive en kalender for en leverandør, skal du oprette kalenderen i **Organisationsadministration > Kalendere > Kalendere**. Når kalenderen er oprettet, skal du tildele den til leverandøren. Gå til **Kreditor > Kreditorer > Alle kreditorer** og vælge den leverandør, du vil tildele kalenderen til. Tildel derefter den nye indkøbskalender ved hjælp af rullemenuen på leverandørens side i oversigtspanelet **Standardindstillinger for indkøbsordrer**. 

Kalenderen for en leverandør angiver de dage, hvor leverandøren accepterer placeringen af indkøbsordren, og de datoer, hvor leverandøren kan levere ordrerne til dit firma. Derfor er ordredatoerne for indkøbsordrer for leverandøren med en indkøbskalender de datoer, der er defineret som åbne i kalenderen. Leveringsdatoerne for disse ordrer er også på åbne dage og påvirker derfor leveringstiden for den købte vare. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Definere leveringstiden for en købt vare

For at angive leveringstiden for købet af en vare (og om der kun skal medtages arbejdsdage) skal du gå til siden med standardordreindstillinger for produktet, som du finder under **Administration af produktoplysninger > Produkter > Frigivne produkter**, og vælge **Standardindstillinger for ordre**. 

> [!Note]
> **Arbejdsdage** under leveringstiden for købet angiver arbejdsdage for leverandøren. F.eks. angiver en kalender til levering kun på tirsdage med en leveringstid på 10 dage og markering i afkrydsningsfeltet Arbejdsdage, at det vil tage ti uger (10 tirsdage), før varen kan leveres.
I de fleste tilfælde kan det således ikke anbefales at vælge arbejdsdage for leveringstider for indkøbsordrer.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Definere leveringstider fra siden for samhandelsaftaler

Varedisponering kan konfigureres til at medtage alle samhandelsaftaler for leverandører. Samhandelsaftaler er fastpris- eller rabataftaler, der er oprettet for en eller flere kunder eller leverandører for salg eller køb af et eller flere produkter. Gå til **Varedisponering > Opsætning > Varedisponeringsparametre**, og vælg under fanen **Ordreforslag** **Søg købsprisaftaler** for at medtage samhandelsaftaler, når du planlægger. Varedisponering kan vælge leverandøren med **Kortest leveringstid** eller med **Laveste stykpris**.

### <a name="calendar-for-a-warehouse"></a>Kalender for et lagersted
Du kan tildele en kalender til et lagersted for at angive de datoer, der er åbne for modtagelse og levering. Hvis der ikke er tilknyttet en kalender til et lagersted, antages det, at den er åben alle dage. 

> [!Note]
> Det har ikke nogen indflydelse at tildele en kalender til et transitlagersted. Transitlagersteder bruges til understøttelse af flytteordrer. De forsendelses- eller modtagelsesdatoer, der gælder for ordrerne, er defineret af de åbne dage i "Fra"-lagersted og "Til"-lagersted og leveringskalenderens leveringsmåde.

#### <a name="closed-for-pickup-policy"></a>Politikken Lukket for afhentning
Hvis du vil angive, at et lagersted er åbent for modtagelse, men afhentning ikke er muligt, kan du bruge **Politikken Lukket for afhentning** i lagerstedskalenderen. Det samme gælder for afhentning af kundeordrer. 

### <a name="transport-calendar"></a>Transportkalender 
Hvis du vil angive de datoer, der er tilgængelige for afsendelse af flytteordrer fra et **Fra-lagersted**, kan du tildele en **Transportkalender**. Du kan konfigurere en transportkalender pr. leveringsmåde eller pr. leveringsmåde fra lagersted. Transportkalenderen konfigureres i **Salg og marketing > Opsætning > Distribution > Leveringsmåder**. Vælg en leveringsmåde, og klik på knappen **Transportkalender**.

Der kan oprettes en linje for hvert lagersted og hver leveringsmåde, hvor kalenderen tilføjes i kolonnen **Transportkalender**. Linjen angiver den transportkalender, der skal anvendes, når der afsendes varer fra lageret ved hjælp af den angivne leveringsmåde. Hvis du vil anvende en transportkalender på alle de forsendelser, der bruger en bestemt leveringsmåde, kan du oprette en linje uden at angive lageret.  Den påvirker alle de forsendelser, der bruger den angivne leveringsmåde, uanset lokationen. 

Hvis der ikke er tildelt en transportkalender, antages det, at alle dage er åbne for transport.

### <a name="calendar-for-a-customer"></a>Kalender for en kunde
Du kan angive de datoer, hvor en kunde kan acceptere leverancer, ved at tildele en tilgangskalender til kunden. Hvis der ikke er tildelt en kalender til en kunde, antages det, at kunden kan modtage ordrer på alle dage. Dette påvirker modtagelsesdatoen på salgsordrelinjerne. Hvis du vælger en dato i de salgsordrelinjer, der ikke er "åbne" i kundekalenderen, angiver systemet, at modtagelsesdatoen ikke er gyldig. 

Bemærk, at det kun er muligt at medtage én kalender pr. kunde. Hvis du vil medtage en kalender for hver anden adresse for en kunde, kan du oprette én kunde pr. adresse og derefter tildele dens respektive kalender. 

Den ønskede modtagelsesdato på salgsordrelinjerne påvirkes af kundekalenderen og kontrolmetoden for leveringsdatoen. Du kan læse mere om, hvordan den tidligste leveringsdato beregnes i [Ordretilsagn](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Forsendelseskalender for en juridisk enhed
Hvis du vil angive de datoer, hvor en juridisk enhed kan afsende varer, kan du konfigurere en forsendelseskalender under **Virksomhedsadministration > Organisationer > Juridiske enheder**. Vælg den juridiske enhed, og tilføj kalenderen under fanen **Udenrigshandel og logistik** i feltet **Forsendelseskalender**. Forsendelseskalenderen fungerer som kilde til standardindstillinger for alle lagerstedskalendere i den juridiske enhed. 

## <a name="how-calendars-affect-dates-in-planning"></a>Sådan påvirker kalendere datoer i planlægningen

### <a name="order-date-of-a-planned-purchase-order"></a>Bestillingsdato for et indkøbsordreforslag 
Ordredatoen i et indkøbsordreforslag angiver den dato, hvor ordren er afgives. Det er en åben dato både i leverandørkalenderen og kalenderen for varedisponeringsgruppen. Leverandører skal nogle gange have et par dages margen mellem, hvornår de modtager indkøbsordren, og hvornår de kan sende varerne. Disse datoer er angivet i leverandørens dage i sikkerhedsmargener. Men hvis den købte vare tildeles til en disponeringsgruppe med dage i sikkerhedsmargener, tilsidesætter disse dage i sikkerhedsmargener leverandørens dage i sikkerhedsmargener.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Leveringsdato for et indkøbsordreforslag
Modtagelsesdatoen for et køb angiver den dato, hvor du vil modtage varerne. Det er en åben dato i kalenderen. Den kalender, der vil blive taget i betragtning med hensyn til angivelse af, hvilke dage indkøbsordrerne kan modtages, er følgende i rækkefølge fra højeste til laveste prioritet: 
1. Leverandørens kalender
1. Kalender for disponeringsgruppe
1. Lagerstedkalender for tilgangslagerstedet

Bemærk, at kalenderen for disponeringsgruppen kan angives på forskellige sider, og at de prioriteres i følgende rækkefølge:
1. Varedisponeringsgruppe på siden **Varedisponering**
1. Varedisponeringsgruppe på siden **Oplysninger om frigivne produkter**.
1. Standardvaredisponeringsgruppe i **Varedisponeringsparametre**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Forsendelsesdato for et flytteordreforslag
Når du opretter en flytteordre mellem to lagersteder, medtages afsendelsesdatoen og modtagelsesdatoen i flytteordrens hoved sammen med "Fra"-lagersted og "Til"-lagersted. Forskellen mellem disse to datoer er den forventede transporttid (i dage) mellem lagerstederne.

Afsendelsesdatoen for et flytteordreforslag angiver den dato, hvor varerne sendes fra "Fra"-lagerstedet. De kalendere, der bruges til at angive den tilgængelige afsendelsesdato, er angivet efter prioritet: 
1. Lagerstedskalenderen for "Fra"-lagersted
1. Kalender for disponeringsgruppe (se reserverækkefølgen for denne kalender ovenfor) Hvis der er defineret en lagerstedskalender, bliver afsendelsesdatoen en åben dato i kalenderen. Hvis der ikke er defineret en lagerstedskalender, anvendes kalenderen for disponeringsgruppen. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Modtagelsesdato for et flytteordreforslag
Modtagelsesdatoen for et flytteordreforslag angiver den dato, hvor varerne modtages på "Til"-lagerstedet.

De kalendere, der bruges til at angive modtagelsesdatoen, er dem, der er angivet efter prioritet: 
1. Kalender for disponeringsgruppe 
1. Lagerstedkalender for "Til"-lagerstedet Hvis der er angivet en disponeringskalender, er modtagelsesdatoen automatisk en åben dato i kalenderen. Hvis der ikke er defineret en kalender for disponeringsgruppen, anvendes lagerstedskalenderen. 

Når der skal findes forsendelses- og modtagelsesdatoer for flytteordreforslag, bliver margener, der er defineret af brugeren for afsendelse og modtagelse, også taget i betragtning. 

## <a name="using-calendars-in-master-planning"></a>Bruge kalendere i varedisponering

### <a name="assignment-of-scm-calendars"></a>Tildeling af SCM-kalendere
Det er vigtigt at angive kalendere for at identificere arbejdsdagene i firmaet. Den bedste implementering er at oprette en kalender for hvert element med forskellige arbejdsdage. Med andre ord alle eksterne kalendere (kunde, leverandør) og alle interne (lagersted, disponeringsgruppe og leveringsmåde), der er relateret til firmaet.

### <a name="recommendation-on-warehouse-calendars"></a>Anbefaling for lagerstedskalendere
Det anbefales at bruge én kalender pr. lagersted for at medtage de ændringer, der kun påvirker lageret. To eller flere lagersteder kan f.eks. have de samme arbejdsdage, men forskellig politik for afhentning. I så fald er en kalender for de enkelte lagersteder med dets respektive afhentningspolitik bedst at implementere, hvis systemet skal medtage de bedste datoer for indkøbsforslag, flytteforslag og produktionsordreforslag. Hvis der ikke er angivet nogen kalendere for lagerstedet, kan kalenderen for den juridiske enhed bruges som kilde til standardindstillingerne for lagerstedskalenderen. 

### <a name="recommendation-of-coverage-group-calendars"></a>Anbefaling for kalendere for disponeringsgrupper
Med hensyn til kalendere for disponeringsgrupper er det vigtigt at tænke på, at de har en tilsidesættelsesfunktion for modtagelsesdatoer i varedisponeringen. Det anbefales derfor at bruge dem med forsigtighed. Det er især vigtigt i tilfælde af, at opfyldning skal udføres på bestemte dage i ugen. 

### <a name="updating-scm-related-calendars"></a>Opdatering af SCM-relaterede kalendere
Det er vigtigt, at alle relevante kalendere tildeles på deres respektive sted (leverandør, kunde, lagersted, leveringsmåde eller disponeringsgruppe), men det er samtidig lige så vigtigt at opdatere dem, så de afspejler ændringerne. Systemet definerer produktions-, overførsels-, købs- og salgsordredatoerne afhængigt af kombinationen af de tildelte kalendere. Det er den bedste fremgangsmåde at tydeliggøre, hvem der har ansvaret for at tildele og opdatere kalenderne i deres tilsvarende områder. I tilfælde af nedbrud eller andre usædvanlige ændringer i arbejdsdagene er det vigtigt at opdatere kalenderne i henhold til den. Alle opgaver, der afhænger af kalendere, f.eks. varedisponering og planlægning af produktionen, skal køres igen, når kalendere opdateres. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]