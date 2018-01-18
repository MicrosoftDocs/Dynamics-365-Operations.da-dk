---
title: Terminologi for omkostningsregnskab
description: "Dette emne definerer nøgleudtryk, der bruges i omkostningsregnskabet."
author: YuyuScheller
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 957acdbbc6bba83b8b2e2b83fdf266524385141d
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="cost-accounting-terminology"></a>Terminologi for omkostningsregnskab

[!include[banner](../includes/banner.md)]


Dette emne definerer nøgleudtryk, der bruges i omkostningsregnskabet.

**Tildelingsgrundlag**

Fordelingsgrundlaget bruges til at måle og kvantificere aktiviteter, f.eks. maskintimer, der bruges, kilowatttimer (kWh), der forbruges eller areal, der er optaget. Det bruges som basis for fordeling af omkostninger til et eller flere omkostningsobjekter.

**Driftsregnskab**

I omkostningsregnskabet kan du indsamle data fra forskellige kilder, f.eks. finans, underfinanskonti, budgetter og statistiske oplysninger. Du kan derefter analysere, opsummere og evaluere omkostningsdata, så ledelsen kan tage de bedst mulige beslutninger om prisopdateringer, budgetter, omkostningsstyring og så videre. De kildedata, der bruges til omkostningsanalyse, behandles uafhængigt af hinanden i omkostningsregnskab. Opdateringer i omkostningsregnskabet påvirker derfor ikke kildedataene. Når du indsamler omkostningsdata fra forskellige kilder, og især når du importerer hovedkontiene fra finansmodulet i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition som omkostningselementer, er der dog dataredundans, fordi de samme data findes i både finansmodulet og omkostningsregnskabet. Denne redundans er påkrævet, fordi du bruger økonomistyring til ekstern rapportering og omkostningsregnskab til intern afrapportering.

**Finanspost for omkostningsregnskab**

Det defineres af kalenderen, valuta og omkostningselementdimension og styrer processer og politikker til måling af omkostninger. 

**Omkostningspostering**

Omkostningsposter er resultatet af en overførsel via dataforbindelser fra finansposter, omkostningsfordelinger og bogførte omkostningsposter i omkostningskladder.

**Omkostningsobjekt**

Enhver type objekt, der er valgt til omkostningsstyring. Omkostninger eller indtægter bogføres enten direkte eller allokeres til omkostningsobjekter. Nogle typiske omkostningsobjekter er:

-  Produkter
-  Projekter
-  Afdelinger
-  Bærere

Ledelsen bruger omkostningsobjekter til at kvantificere omkostninger, men også oprette rentabilitetsanalyser.

**Omkostningselement**

Bruges som en funktion til at registrere og kategorisere omkostninger. Der findes to typer omkostningselementer: primære og sekundære.

Primære omkostningselementer repræsenterer strømmen af omkostninger fra finansregnskab til omkostningsregnskab. Strukturen svarer typisk til driftskontostrukturen i Finans, hvor et omkostningselement kan svare til en hovedkonto. Ikke alle hovedkonti skal nødvendigvis være repræsenteret som omkostningselementer, afhængigt af virksomhedens krav. 

Sekundære omkostningselementer repræsenterer det interne flow af omkostninger, da disse omkostninger kun bruges i omkostningsregnskab. De bruges i regler for omkostningsakkumulering til at samle omkostninger i meningsfyldte sæt, der bruges ved beregning af indirekte produktionsomkostninger. 

**Klassificering af omkostninger**

Omkostningsklassifikation grupperer omkostninger i henhold til deres fælles karakteristika. For eksempel kan omkostninger grupperes efter elementer, sporbarhed og funktionsmåde.

-   **Efter elementer** – materialer, arbejdsløn og udgifter.
-   **Efter sporbarhed** – direkte og indirekte omkostninger. Direkte omkostninger tildeles omkostningsobjekter direkte. Indirekte omkostninger kan ikke direkte spores til omkostningsobjekter. Indirekte omkostninger fordeles til omkostningsobjekter.
-   **Efter funktionalitet** – faste, variable og delvist variable.

**Funktionalitet af omkostning**

Omkostningers funktionsmåde klassificerer omkostninger efter deres funktionsmåde i forhold til ændringer i virksomhedens aktiviteter. For at styre omkostninger effektivt skal ledelsen forstå funktionsmåden for omkostninger. Der findes tre typer funktionsmønstre for omkostninger: faste, variable og delvist variable.

- **Fast omkostning** – Faste omkostninger er en omkostning, der ikke varierer på kort sigt, uanset ændringer i aktivitetsniveau. Faste omkostninger kan eksempelvis være grundlæggende driftsudgifter for en virksomhed, der ikke bliver berørt, selvom aktivitetsniveau forøges eller formindskes.

- **Variabel omkostning** – En variabel omkostning ændres i overensstemmelse med ændringer i aktivitetsniveau. For eksempel er en bestemt direkte materialeomkostning knyttet til hvert produkt, der sælges. Jo flere produkter, der sælges, jo flere direkte materialeomkostninger er der.

- **Delvist variabel omkostning** – Delvist variable omkostninger er delvist faste og delvist variable omkostninger. For eksempel omfatter et internetadgangsgebyr et månedligt standardgebyr for adgang og et brugsgebyr af bredbånd. Det månedlige standardadgangsgebyr er faste omkostninger, mens gebyret for bredbåndsforbrug er en variabel omkostning.

**Omkostningskontrolenhed**

Omkostningskontrolenheden repræsenterer omkostningsstrukturen. Strukturen bestemmer, hvordan omkostninger flyder i en hierarkisk struktur mellem omkostningsobjektdimensioner og deres respektive omkostningsobjekter. 

**Omkostningsfordeling**

Bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende et relevant fordelingsgrundlag. Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement for den oprindelige omkostning, og der sker ingen reciprok behandling.

**Omkostningstildeling**

Bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag. Finance and Operations understøtter den gensidige fordelingsmetode. I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud. Systemet bestemmer automatisk rækkefølgen, som tildelingerne skal udføre i og gentages over den. Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag. Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes. Fordelingsrækkefølgen styres af omkostningskontrolenheden.

**Politik for omkostningsfordeling**

En politik til fordeling af omkostninger definerer de beløb og mængder, der skal fordeles. Fordelingsregler omfatter regler for fordeling af kilde, som bestemmer de omkostninger, der er fordelt, og fordelingsmålsregler, som bestemmer, hvor omkostningerne fordeles. For eksempel er alle omkostninger for facilitetsservices en fordelingskilde, der kan fordeles på forskellige afdelinger i en organisation (det vil sige til fordelingsmål).

**Omkostningstotaler**

Formålet med regler for akkumulering af omkostninger er at samlede omkostninger i beskrivende filsæt. Aggregationsniveauet er brugerdefineret, og involverer tildelingen af et sekundært omkostningselement. Hvis omkostningstotal ikke bruges, tildeles hvert element af en omkostning fra ét omkostningsobjekt til et andet.

**Politik for omkostningssats**

Omkostningssatsen bruges til at beregne prisen pr. omkostningsobjekt. For at forstå elementerne af prisen definerer du politikker for omkostningssats. Der findes to typer omkostningssatser: historisk omkostningssats og planlagt omkostningssats. En historisk omkostningssats er en beregnet sats, der bruges som multiplikator for fordelingsbasis af et omkostningsobjekt. Satsen beregnes på basis af omkostningsfordelinger i den foregående periode. En planlagt sats er en brugerdefineret sats.

**Dimensionshierarki**

Der er to dimensionshierarkier: kategorihierarki og klassifikationshierarki. Kategoriseringshierarki for dimensionstype bruges til rapporteringsformål. Den understøtter kun omkostningselementdimensioner. Klassifikationshierarki for dimension-typen bruges til at definere politikker og til rapporteringsformål. Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner. 

**Dataconnector**

Omkostningsregnskab understøtter integration af data fra andre kildesystemer via en række dataconnectorer. Følgende dataconnectorer er tilgængelige:

-  Importerede transaktioner (konfigureret på forhånd)
-  Dynamics 365 for Finance and Operations, Enterprise Edition (konfigureret på forhånd)
-  Dynamics AX (konfiguration kræves)

**Bemærk:** Transaktioner importeret via dataconnector er baserede på dataenheder.

**Dataprovider**

De fleste kildesystemer kan levere data, der svarer til en eller flere datakilder i omkostningsregnskab. Hvis du vil justere data fra kildesystemer med datakilden i omkostningsregnskabet, skal en dataprovider konfigureres. I følgende tabel vises tilgængeligheden af dataprovidere pr. dataconnector og datakilde.

|  **Tabeller** |  **Dataconnector for importerede transaktioner** | **Dynamics 365 for Finance and Operations, Enterprise Edition-dataconnector**  | **Dynamics AX-dataconnector**  |
|---|---|---|---|
| Dimensionsmedlemmer for omkostningselement  |  Ja | Ja  | Ja  |
|  Dimensionsmedlemmer for omkostningsobjekt |  Ja | Ja  | Ja  |
|  Statistiske dimensionsmedlemmer | Ja  | Nr.  | Nr.  |
|  Finans | Ja  | Ja  | Ja  |
|  Budgetposter  | Ja  | Ja  | Ja  |
|  Statistiske målinger | Ja  | Ja  | Ja  |

**Formel**

Med fordelingsbaser for formler kan du definere særlige formler for at opnå den korrekte fordelingsbasis. Du kan manuelt oprette fordelingsbaser for formler. Du kan bruge følgende operatorer til at definere formlen.

|  **Symboler** | **Tekst**  |
|---|---|
|  ( ) | Parenteser  |
|  < |  Mindre end |
|  > |  Større end |
|  + |  Tilføjelse |
|  – |  Subtraktion |
| *  | Multiplikation  |
    
Traditionelle IF-sætninger understøttes ikke. Du kan dog oprette sætninger og kontrollere, om de er sande.

|  **Kontoudtogsvalidering** | **Resultat**  |
|---|---|
|  a > b| Sand  |
|  a > b |  Falsk |
    
**Faste omkostninger**

Faste omkostninger vedrører de løbende udgifter til drift af en virksomhed. Det er de omkostninger, der ikke kan knyttes direkte til virksomhedens konkrete aktiviteter. Følgende er eksempler på faste omkostninger:

-   Regnskabsgebyrer
-   Afskrivninger
-   Forsikring
-   Interesser
-   Advokatsalærer
-   Moms
-   Forbrugsomkostninger

**Sats for faste omkostninger**

Satser defineres for hvert omkostningsobjekt og omkostningselement. Der findes to typer satser: regnskabsperiode og brugerdefineret. Satser for regnskabsperiode beregnes ved beregningen af indirekte produktionsomkostninger. En brugerspecifik sats er brugerdefineret og kan bruges til at allokere omkostninger mellem omkostningsobjekter med en foruddefineret sats i beregningen af indirekte produktionsomkostninger.

**Publiceret**

Hvis du indstiller dette felt til Ja, kan en bruger, der er tildelt en af følgende roller, få vist rapporten i arbejdsområdet Omkostningsstyring:

-  Vedligehold regnskabschef for omkostning
-  Lagerbogholder
-  Lagerregnskabsassistent
-  Controller til omkostningsobjekt

Hvis du indstiller dette felt til Nej, er det kun brugere, der er tildelt en af følgende roller, der kan få vist rapporten i arbejdsområdet Omkostningsstyring:

-  Vedligehold regnskabschef for omkostning
-  Lagerbogholder
-  Lagerregnskabsassistent

**Statistisk dimension**

En statistisk dimension og dens medlemmer bruges til registrering og kontrol af ikke-pengemæssige poster i omkostningsregnskab. Statistiske dimensionsmedlemmer kan bruges til to formål:

-  Som fordelingsbasis i politikker, f.eks. omkostningstildeling eller omkostningsdistribution.
-  Til rapportering af ikke-pengemæssigt forbrug.

En statistisk dimension er udtryk for et antal eller en sum af et aktivitet, der kan bruges som grundlag for tildelinger eller omkostningsberegninger. Den er oprettet manuelt eller importeret fra kildesystemer. Eksempler på statistiske dimensioner er antallet af medarbejdere, antallet af licenssoftware på hver enhed, strømforbruget på hver maskine eller kvadratmeter for en bærer.

**Sætning**

Opgørelser er visninger for de ledere, der er ansvarlige for styring af omkostninger. Opgørelser er defineret af en omkostningscontroller, og de giver et hurtigt overblik over aktuelle og budgetterede omkostninger og afvigelser. En chef kan finde yderligere detaljer, hvis det er nødvendigt. For at sikre, at chefer kun ser de data, som de er ansvarlige for, er data, der vises i opgørelser, underlagt adgangsregler.

**Version**

Versioner, der bruges til at simulere, se og sammenligne forskellige udfald. Som standard vises alle faktiske omkostninger i en grundlæggende version, der er kendt som *faktisk*. I budgetter og beregninger kan du arbejde med så mange versioner, som du har brug for. Du kan eksempelvis importere budgetdata i en oprindelig version og derefter ændre budgettet i en revideret version. Du kan oprette flere versioner for beregninger. Du kan derefter oprette beregninger ved hjælp af andre beregningsregler, der skal udlignes for omkostningstildeling i disse forskellige versioner.



