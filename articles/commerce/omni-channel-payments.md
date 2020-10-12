---
title: Oversigt over omni-kanalbetalinger
description: Dette emne giver en oversigt over omni-kanalbetalinger i Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 80eaf36fb382e0ebe0a66383ea17ab76faa07dfa
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819807"
---
# <a name="omni-channel-payments-overview"></a>Oversigt over omni-kanalbetalinger

[!include [banner](../includes/banner.md)]

Dette emne giver en oversigt over omni-kanalbetalinger i Dynamics 365 Commerce. Det indeholder en omfattende liste over understøttede scenarier, oplysninger om funktionalitet, opsætning og fejlfinding samt beskrivelser af nogle typiske problemer.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivelse |
|---|---|
| Tokenet | En datastreng, som en betalingsprocessor har som reference. Tokens kan repræsentere betalingskortnumre, betalingsgodkendelser og tidligere betalingsregistreringer. Tokens er vigtige, fordi de er med til at holde følsomme data ude af POS-systemet (Point of Sale). De kaldes undertiden også *referencer*. |
| Korttoken | Et token, som en betalingsprocessor leverer med henblik på lagring i POS-systemet. Et korttoken kan kun bruges af den handlende, der modtager det. Korttokens kaldes undertiden også *kortreferencer*. |
| Godkendelsestoken | Et entydigt id, som en betalingsproces indeholder som en del af det svar, der sendes til et POS-system, når POS-systemet foretager en anmodning om godkendelse. Et godkendelsestoken kan bruges senere, hvis processoren kaldes for at udføre handlinger, f.eks. tilbageførsel eller annullering af godkendelsen. Men det bruges ofte til at registrere midler, når en ordre er opfyldt, eller en transaktion afsluttes. Godkendelsestokens kaldes undertiden også *godkendelsesreferencer*. |
| Registreringstoken | En reference, som en betalingsprocessor leverer til et POS-system, når en betaling er fuldført eller registreret. Registreringstokenet kan derefter bruges til at henvise til betalingsregistreringen i efterfølgende handlinger, f.eks. refusionsanmodninger. | 
| Der findes ikke et kort | En betegnelse, der henviser til betalingstransaktioner, hvor der ikke bruges et fysisk kort. Disse transaktioner kan f.eks. forekomme i e-handels- eller callcenterscenarier. Ved disse transaktioner angives betalingsrelaterede oplysninger manuelt på et e-handelswebsted, i et callcenterflow eller på en POS- eller betalingsterminal. |
| Der findes et kort | Et udtryk, der henviser til betalingstransaktioner, hvor der vises et fysisk kort, som bruges på en betalingsterminal, der er forbundet til Microsoft Dynamics 365 POS-systemet. |

## <a name="overview"></a>Overblik

Generelt beskriver begrebet *omni-kanalbetalinger* muligheden for at oprette en ordre i én kanal og udføre den i en anden kanal. Nøglen til understøttelse af omni-kanalbetalinger er at opbevare betalingsoplysninger sammen med resten af ordredetaljerne og derefter bruge disse betalingsoplysninger, når ordren tilbagekaldes eller behandles i en anden kanal. Et klassisk eksempel er scenariet "Køb online, og afhent i butikken". I dette scenario tilføjes betalingsoplysningerne, når ordren oprettes online. De kaldes derefter ved POS for at debitere kundens betalingskort på afhentningstidspunktet. 

Alle de scenarier, der er beskrevet i dette emne, kan implementeres ved hjælp af standard-SDK'et (Software Development Kit), der leveres med Commerce. [Dynamics 365-betalingsconnector til Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) indeholder en out-of-box-implementering af hvert af de scenarier, der beskrives her. 

### <a name="prerequisites"></a>Forudsætninger

Alle de scenarie, der beskrives i dette emne, kræver en betalingsconnector, der understøtter omni-kanalbetalinger. Adyen out-of-box-connectoren kan også bruges, fordi den understøtter de scenarier, der stilles til rådighed via betalings-SDK'et. Yderligere oplysninger om, hvordan du implementerer betalingsconnectorer og om Retail SDK generelt, finder du på [Startside for detail for professionelle it-folk og udviklere](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Understøttede versioner

De funktioner til omni-kanalbetaling, der er beskrevet i dette emne, blev udgivet som en del af Microsoft Dynamics 365 for Retail version 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Connectorerne "Der findes et kort" og "Der findes ikke et kort"

Betalings-SDK'et er baseret på to sæt API'er (Application Programming Interfaces) til betalinger. Det første sæt API'er hedder **iPaymentProcessor**. Det bruges til at implementere "Der findes ikke et kort"-betalingsconnectorer, der kan bruges i callcentre og med Microsoft Dynamics e-handelsplatformen. Yderligere oplysninger om **iPaymentProcessor**-grænsefladen finder du i dette whitepaper [Implementering af en betalingsconnector og betalingsenhed](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf), som dækker betalinger. 

Det andet sæt API'er hedder **iNamedRequestHandler**. Det understøtter implementering af "Der findes et kort"-betalingsintegrationer, der bruger en betalingsterminal. Du kan finde flere oplysninger om **iNamedRequestHandler**-grænsefladen under [Oprette integration af betaling for en betalingsterminal](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Installation og konfiguration

Der kræves følgende komponenter og opsætningstrin:

- **eCommerce-integration** : Der kræves integration med Commerce for at understøtte scenarier, hvor en ordre stammer fra en onlinebutik. Yderligere oplysninger om SDK'et til Retail E-commerce finder du i [SDK'et (Software Development Kit) til Retail E-commerce](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). I et demomiljø understøtter referencebutikken omni-kanalbetalingsscenarier. 
- **Konfiguration af onlinebetalinger:** Konfigurationen af onlinekanalen skal indeholde en betalingsconnector, der er opdateret til at understøtte omni-kanalbetalinger. Alternativt kan der bruges en out-of-box-betalingsconnector. Du kan finde oplysninger om, hvordan du konfigurerer Adyen-betalingsconnectoren til onlinebutikker, i [Betalingsconnector til Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Ud over de trin til eCommerce-opsætning, der er beskrevet i dette emne, skal indstillingen **Tillad lagring af betalingsoplysninger under e-handel**-parameteren sættes til **True** i indstillingerne for Adyen-connectoren. 
- **Konfiguration af omni-kanalbetalinger**: Gå i administrationen til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Delte parametre for Commerce**. Indstil derefter **Brug omni-kanalbetalinger** til **Ja** under fanen **Omni-kanalbetalinger**. I Commerce version 10.0.12 og nyere findes denne indstilling i arbejdsområdet **Funktionsstyring**. Vælg funktionen **Omni-kanalbetalinger**, og klik på **Aktivér nu**. 
- **Betalingstjenester:** Callcenteret bruger standardbetalingsconnectoren på siden **Betalingstjenester** til at behandle betalinger. For at understøtte scenarier som f.eks. "Køb i callcenter, og afhent i butik" skal denne standardbetalingsconnector være Adyen-betalingsconnectoren eller en betalingsconnector, der opfylder implementeringskravene til omni-kanalbetalinger.
- **Autorisationskodetjeneste**: Betalinger via en betalingsterminal skal være konfigureret i oversigtspanelet **Autorisationskodetjeneste** i hardwareprofilen. Adyen-connectoren understøtter omni-kanalbetalingsscenarier out of the box. Andre betalingsconnectorer, der understøtter **iNamedRequestHandler**-grænsefladen, kan også bruges, hvis de understøtter omni-kanalbetalinger.
- **Tilgængelighed af betalingsconnector:** Når en ordre tilbagekaldes, omfatter de betalingsmiddellinjer, der tilbagekaldes sammen med ordren, navnet på den betalingsconnector, der blev brugt til at oprette de godkendelser, der er knyttet til den pågældende ordre. Når ordren er opfyldt, forsøger betalings-SDK'et at bruge den samme connector, som blev brugt til at oprette den oprindelige godkendelse. Derfor skal en betalingsconnector med de samme forhandleregenskaber være tilgængelig for registrering. 
- **Korttyper:** Hvis omni-kanalscenarierne skal fungere korrekt, skal hver kanal have samme opsætning for betalingsmiddeltyper, der kan bruges til omni-kanalen. Denne opsætning omfatter betalingsmetode-id'er og korttype-id'er. Hvis betalingsmiddeltypen **Kort** f.eks. har id'et **2** i opsætningen af onlinebutikken, skal det have samme id i opsætningen af detailbutikken. Det samme krav gælder for korttype-id'er. Hvis kortnummer **12** er indstillet til **Visa** i onlinebutikken, skal det samme id defineres for detailbutikken. 
- Retail Modern POS til Windows eller Android med indbygget hardwarestation -eller-
- Modern POS til iOS eller Cloud POS med tilsluttet delt hardwarestation. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Grundlæggende princip, der understøtter omni-kanalbetalinger

Betalingsconnectorer og betalingsprocessorer bruger tokens, eller referencer, til at henvise til de interaktioner, der er relateret til kortbetalinger. Når der f.eks. anmodes om en betalingsgodkendelse, gives der en reference til den pågældende godkendelse. Derfor kan der senere refereres til godkendelsen, når der registreres midler på tidspunktet for opfyldelsen. Denne godkendelse er entydig for den handlende, betalingsconnectoren og processoren. 

Hvis en ordre, der er oprettet online, plukkes i butikken, skal de samme betalingsoplysninger tilbagekaldes og bruges. Når de oprindelige oplysninger angives som en del af anmodningen om at registrere en betaling i forhold til den oprindelige godkendelse, vil betalingsprocessoren kunne håndtere anmodningen og registrere betalingen. 

For at henvise korrekt til onlineordren skal der også være en "Der findes ikke et kort"-betalingsconnector, der understøtter den samme processor. På denne måde kan POS-systemet have én processor til "Der findes et kort"-betalinger, men det kan også have adgang til andre betalingsconnectorer, så det kan opfylde ordrer, der oprettes i andre kanaler ved hjælp af andre betalingsprocessorer. 

## <a name="supported-scenarios"></a>Understøttede scenarier

Følgende scenarier til omni-kanalbetaling understøttes:

- Køb online, afhent i butikken
- Køb i callcenter, og afhent i butik
- Køb i butik A, og afhent i butik B
- Køb i butik A, og levér til kunde

    > [!NOTE]
    > Betalinger, der foretages i callcenteret, som er knyttet til betalingsfunktionen "Normal", skal markeres som **Forudbetaling** = **Ja**, hvis de skal afspejles i det forfaldne beløb ved tilbagekald af ordren i POS. Ikke-forudbetalte betalinger af typen "Normal" genkendes ikke, når ordren tilbagekaldes i POS. 

Variationer af disse scenarier understøttes også. En onlineordre kan f.eks. indeholde både linjer, der skal afsendes til kunden, og de linjer, der skal afhentes i en butik. Alle indstillinger for ordreopfyldning understøttes via omni-kanalbetalinger. 

I følgende afsnit beskrives trinnene for hvert scenarie, og hvordan du kan køre scenariet ved hjælp af demonstrationsdata. 

### <a name="buy-online-pick-up-in-store"></a>Køb online, afhent i butikken

Før du går i gang, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du har en referencebutik, hvor Adyen-connectoren er konfigureret.
- Indstillingen **Omni-kanalbetalinger** på siden **Delte parametre for Commerce** er angivet til **Sand**. I senere versioner flyttes denne indstilling til arbejdsområdet **Funktionsstyring**, hvor du kan vælge funktionen **Omni-kanalbetalinger** og klikke på **Aktivér nu**. 
- Adyen-betalingsconnectoren er konfigureret til Houston POS-kasseapparatet.
- Retail Modern POS til Windows eller Android med indbygget hardwarestation -eller-
- Modern POS til iOS eller Cloud POS med tilsluttet delt hardwarestation. 

Følg disse trin for at køre scenariet.

1. I referencebutikken kan du oprette en ordre for afhentning i butikken. Sørg for at vælge butikken **Houston**. 
2. Gennemgå trinnene til udtjekning, og betal med et prøvekreditkortnummer. Du kan finde prøvekreditkortnumre på [siden med Adyen-prøvekortnumre](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. I Commerce kan du bruge batchjobbet **Synkroniser ordrer** og **P-001**-distributionsplanen til at oprette ordrerne i administrationen.
4. Vælg handlingen **Ordrer til afhentning** på velkomstsiden i POS for at se ordrerne til afhentning i butik. 
5. Vælg en eller flere linjer fra den ordre, der blev oprettet i referencebutikken, og vælg derefter **Hent**.

    Ordren hentes fra administrationskontoret. 

6. Når ordrelinjeoplysningerne er hentet fra kontoret, og der er registreret en kortbetaling, der kan bruges til omni-kanal, får du besked om, at der findes en betalingsmetode.
7. Vælg **Brug tilgængelig betalingsmetode** til at fuldføre transaktionen ved hjælp af de kortdetaljer, der blev angivet i referencebutikken.

    Ordrelinjerne indlæses på transaktionssiden, og den forfaldne saldo er 0 (nul). 

8. Vælg fanen **Betalinger** for at få vist den betalingsmiddellinje, der blev hentet fra onlineordren. 
9. Vælg en betalingsmåde for at fuldføre transaktionen. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Køb i callcenter, og afhent i butik

1. På siden **Kundeservice** i Commerce skal du angive **Karen Berg** i søgepanelet og derefter vælge **Søg**. 
3. Vælg **Karen Berg** i søgeresultaterne.
4. Når Karen er indlæst på siden **Kundeservice**, skal du vælge **Ny salgsordre**.
5. Vælg **Hoved** på siden for den nye salgsordre for at få vist ordrehovedet. 
6. Indstil stedet til **Central** og lagerstedet til **Houston** på siden **Ordrehoved**.
7. Indstil feltet **Leveringsmåde** til **60** for kundeafhentning under fanen **Levér**.
8. Vælg **Linjer**, og føj derefter en eller flere linjer til ordren. 
9. Vælg **Fuldført** for at angive forløbet for færdiggørelse af ordren.
10. Rul ned til betalingsafsnittet, vælg **Tilføj**, og vælg derefter en linje, hvor betalingsmetodetypen er indstillet til **Kort**. 
11. Vælg plustegnet (**+**) for at tilføje en kortbetaling. 
12. Angiv detaljerne for et prøvekreditkortnummer, som du fandt på [siden med Adyen-prøvekortnumre](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description), og vælg derefter **OK**.

    > [!NOTE]
    > Betalingen gennemføres, selvom kortmærket for det angivne kortnummer er forskelligt fra det mærke, der blev valgt, da betalingen blev startet. Den vil dog blive bogført på de konti, der er knyttet til det kortmærke, du valgte i trin 10.

12. Vælg **OK** igen for at lukke dialogboksen **Betalinger til ordrefuldførelse**.
13. Vælg **Send** på siden **Salgsordreoversigt**.
14. Vælg handlingen **Ordrer til afhentning** på velkomstsiden i POS for at se ordrerne til afhentning i butik. 
15. Vælg en eller flere linjer fra den ordre, der blev oprettet i referencebutikken, og vælg derefter **Hent**.

    Ordren hentes fra administrationskontoret. 

16. Når ordrelinjeoplysningerne er hentet fra kontoret, og der er registreret en kortbetaling, der kan bruges til omni-kanal, får du besked om, at der findes en betalingsmetode.
17. Vælg **Brug tilgængelig betalingsmetode** til at fuldføre transaktionen ved hjælp af de kortdetaljer, der blev angivet i referencebutikken.

    Ordrelinjerne indlæses på transaktionssiden, og den forfaldne saldo er 0 (nul).

18. Vælg fanen **Betalinger** for at få vist den betalingsmiddellinje, der blev hentet fra onlineordren. 
19. Vælg en betalingsmåde for at fuldføre transaktionen. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Køb i butik A, og afhent i butik B

1. Start POS for Houston-butikken.
2. På siden **Transaktion** skal du føje Karen Berg til transaktionen ved at bruge det numeriske tastatur til at skrive **2001**.
3. Føj en eller flere linjer til transaktionen.
4. Vælg **Ordrer** for at få vist ordreindstillingerne.
5. Vælg **Afhent alle**, og når du bliver bedt om det, skal du vælge **Kundeordre**.
6. Skriv **Seattle** i søgepanelet, og vælg derefter afhenting i **Seattle**-butikken. 
7. Vælg **OK** for at acceptere dags dato som datoen for afhentning.
9. Vælg **Kortbetaling** for at starte betalingen.
10. Betal det beløb, der er forfaldent for indbetalingen, via kortbetalingen. 
11. Fuldfør betalingen af indbetalingen på betalingsterminalen. 
12. Når indbetalingen er foretaget, skal du vælge indstillingen for at bruge samme kort til opfyldelse og vente på, at ordren færdiggøres. 
13. Start POS for Seattle-butikken.
14. Vælg handlingen **Ordrer til afhentning** på velkomstsiden i POS for at se ordrerne til afhentning i butik. 
15. Vælg en eller flere linjer fra den ordre, der blev oprettet i referencebutikken, og vælg derefter **Hent**.

    Ordren hentes fra administrationskontoret. 

16. Når ordrelinjeoplysningerne er hentet fra kontoret, og der er registreret en kortbetaling, der kan bruges til omni-kanal, får du besked om, at der findes en betalingsmetode.
17. Vælg **Brug tilgængelig betalingsmetode** til at fuldføre transaktionen ved hjælp af de kortdetaljer, der blev angivet i referencebutikken.

    Ordrelinjerne indlæses på transaktionssiden, og den forfaldne saldo er 0 (nul).

18. Vælg fanen **Betalinger** for at få vist den betalingsmiddellinje, der blev hentet fra onlineordren. 
19. Vælg en betalingsmåde for at fuldføre transaktionen. 

### <a name="buy-in-store-a-ship-to-customer"></a>Køb i butik A, og levér til kunde

1. Start POS for Houston-butikken.
2. På siden **Transaktion** skal du føje Karen Berg til transaktionen ved at bruge det numeriske tastatur til at skrive **2001**.
3. Føj en eller flere linjer til transaktionen.
4. Vælg **Ordrer** for at få vist ordreindstillingerne.
5. Vælg **Send alle**, og vælg derefter **Kundeordre**, når du bliver bedt om det.
6. Vælg **Om natten som standard** på siden med forsendelsesmetode, og vælg derefter **OK** for at acceptere dags dato som forsendelsesdato. 
7. Vælg **OK** for at acceptere dags dato som datoen for afhentning.
8. Vælg **Kortbetaling** for at starte betalingen.
9. Betal det beløb, der er forfaldent for indbetalingen, via kortbetalingen. 
10. Fuldfør betalingen af indbetalingen på betalingsterminalen. 
11. Når indbetalingen er foretaget, skal du vælge indstillingen for at bruge samme kort til opfyldelse og vente på, at ordren færdiggøres.

Når ordren er plukket, pakket og faktureret på administrationskontoret, bruges de betalingsoplysninger, der findes på POS, til at registrere betalingsmidlerne for de varer, der skal leveres til kunden. 

## <a name="scenario-details"></a>Scenariedetaljer

Ud over de grundlæggende scenarier, der netop er beskrevet, er der foretaget adskillige forbedringer af betalings-SDK'et for at understøtte omni-kanalbetalinger. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Føre kort gennem kortlæser én gang for kundeordrer

Før funktionen Omni-kanalbetalinger blev implementeret, da kundeordrer, som indeholdt indbetalinger, blev oprettet ved POS, var kunderne nødt til at føre deres kort gennem kortlæseren to gange: én gang for at betale indbetalingen og én gang for at opdele kortet i tokens til efterfølgende ordreopfyldning. Når funktionen til opdeling i tokens for omni-kanaler er slået til, skal kunderne kun føre kortet gennem kortlæseren én gang for at foretage både indbetalingen og autorisere det beløb, der er forfaldent for varer, der skal opfyldes senere. På tidspunktet for opfyldelse registreres de godkendte midler. Før funktionen til opdeling i tokens for omni-kanaler blev implementeret, blev der kun oprettet et gentagent korttoken til efterfølgende ordreopfyldelse. Derfor blev betalingsmidlerne til den ventende opfyldelse ikke godkendt, og da disse midler endnu ikke var modtageren i hænde for det pågældende indkøb, var det mindre sandsynligt, at de kunne indhentes senere.

> [!NOTE]
> At føre kort gennem kortlæseren én gang understøttes ikke i Retail version 8.1.3. Kundeordrer i version 8.1.3 bruger samme flow, som blev brugt, før funktionen til opdeling i tokens for omni-kanaler blev implementeret. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kort, som ikke kan udstede gentagende korttokens

Nogle kort kan ikke bruges til Omni-kanalbetalinger, da de ikke understøtter udstedelse af gentagende korttokens. Når en ordre oprettes ved POS, og indbetalingen foretages ved hjælp af et kort, der ikke understøtter gentagende korttokens, bruges det forrige korts flow for opdeling i tokens. Derfor skal en kunde, der vil lægge en betaling, som skal bruges til efterfølgende ordreopfyldning, have et andet kort. Hvis dette andet kort ikke understøtter gentagende korttokens, vil handlingen til opdeling i tokens blive afvist, og kassereren må bede kunden om at benytte et andet kort. 

### <a name="using-a-different-card"></a>Bruge et andet kort

En kunde, der kommer med butikken for at afhente sin ordre, har mulighed for at bruge et andet kort. Når kassereren får vist en prompten **Brug tilgængelig betalingsmetode** på tidspunktet for afhentning af ordren, kan han eller hun spørge, om kunden ønsker at bruge det samme kort. Hvis kunden har mistet det kort, der blev brugt til at oprette ordren, og ønsker at betale ordren ved hjælp af et andet kort, kan kassereren vælge **Brug en anden betalingsmetode**. Hvis kunden senere kommer for at hente flere varer til samme ordre, og hvis den oprindelige kortgodkendelse stadig er gyldig, kan kassereren igen spørge, om kunden ønsker at bruge det pågældende kort.

### <a name="invalid-authorizations"></a>Ugyldige godkendelser

Hvis det kort, der blev brugt til at oprette en ordre, ikke længere er gyldigt, når der er valgt produkter til afhentning, vil anmodningen om hentning af betaling mislykkes. POS-betalingsconnectoren vil derefter forsøge at oprette en ny godkendelse og hentning ved hjælp af de samme kortdetaljer. Hvis den nye godkendelse eller hentning mislykkes, bliver kassereren informeret om, at betalingen ikke kan behandles. Kassereren skal derefter få en ny betaling fra kunden. 

### <a name="multiple-available-payments"></a>Flere tilgængelige betalinger

Når en ordre med flere betalingsmidler og flere linjer afhentes, modtager kassereren først en prompten **Brug tilgængelig betalingsmetode**. Hvis der er flere kort, når kassereren vælger **Brug tilgængelig betalingsmetode**, hentes eksisterende kortudbetalingslinjer, indtil saldoen er opfyldt for de varer, der afhentes i øjeblikket. Kassereren har ikke mulighed for at vælge det kort, der skal bruges til de varer, der afhentes. 

## <a name="related-topics"></a>Relaterede emner

- [Ofte stillede spørgsmål om betalinger](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365-betalingsconnector til Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](https://docs.microsoft.com/dynamics365/commerce/cpe-bopis)

