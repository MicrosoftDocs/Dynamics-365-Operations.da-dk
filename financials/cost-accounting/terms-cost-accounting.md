---
title: Omkostningsregnskab terminologi
description: "Dette emne definerer nøgleudtryk, der bruges i omkostningsregnskabet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 87c13e268ab8825e06095d24e03694cf0f271a63
ms.openlocfilehash: 1ae6b43bdc1812ca822a1abe2a0e823cb797a511
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-terminology"></a>Omkostningsregnskab terminologi

Dette emne definerer nøgleudtryk, der bruges i omkostningsregnskabet.

**Cost accounting**

I omkostningsregnskabet kan du indsamle data fra forskellige kilder, f.eks. finans, underfinanskonti, budgetter og statistiske oplysninger. Du kan derefter analysere, opsummere og evaluere omkostningsdata, så ledelsen kan tage de bedst mulige beslutninger om prisopdateringer, budgetter, omkostningsstyring og så videre. De kildedata, der bruges til omkostningsanalyse, behandles uafhængigt af hinanden i omkostningsregnskab. Opdateringer i omkostningsregnskabet påvirker derfor ikke kildedataene. Når du indsamler omkostningsdata fra forskellige kilder, og især når du importerer hovedkontiene fra finansmodulet i Microsoft Dynamics 365 for Operations som omkostningselementer, er der dog dataredundans, fordi de samme data findes i både finansmodulet og omkostningsregnskabet. Denne redundans er påkrævet, fordi du bruger økonomistyring til ekstern rapportering og omkostningsregnskab til intern afrapportering.

**Cost accounting ledger**

Omkostningsregnskabets finans er en speciel struktur, der bestemmer, hvordan processer, værdier og mængder angives og præsenteres for et bestemt område i omkostningsregnskab. Omkostningsregnskabets finans definerer processer og regler for måling af omkostninger på omkostningsobjekter. Den håndterer omkostningsposteringer og administrerer dokumenter, der registrerer ændringerne i værdier og mængder, som omkostningsposteringer producerer.

**Cost entry**

Omkostningsposter er resultatet af en overførsel via dataforbindelser fra finansposter, omkostningsfordelinger og bogførte omkostningsposter i omkostningskladder.

**Cost object**

Omkostningsobjekter er en hvilken som helst type objekt, som omkostningerne fordeles til. Her er nogle typiske omkostningsobjekter:

-   Produkter
-   Projekter
-   Ressourcer
-   Afdelinger
-   Bærere
-   Geografiske områder

Ledelsen bruger omkostningsobjekter til at kvantificere omkostninger, men også oprette rentabilitetsanalyser.

**Cost element**

Omkostningselementer bruges som en funktion til at registrere og kategorisere, hvor omkostninger føres hen. Der findes to typer omkostningselementer: primære omkostninger og sekundære omkostninger. **Primære omkostninger** de primære omkostningselementer repræsenterer flow af omkostninger fra regnskab til omkostningsregnskabet. Strukturen af omkostningselementet svarer til driftskontostrukturen i Finans, hvor et omkostningselement kan svare til en hovedkonto. Ikke alle hovedkonti skal nødvendigvis være repræsenteret som omkostningselementer, afhængigt af virksomhedens krav. Her er eksempler på primære omkostningselementer:

-   Vareforbrug
-   Indirekte materialeomkostninger
-   Personaleomkostninger
-   Energiomkostninger

**Secondary cost element** 

De sekundære omkostningselementer repræsenterer internt flow af omkostninger, da disse omkostninger kun oprettes og bruges i omkostningsregnskab. Sekundære omkostningselementer er med til at garantere, at kilden til omkostningerne kan spores. Disse omkostningselementer bruges i omkostningsfordelinger og beregninger af faste omkostninger. Her er eksempler på sekundære omkostningselementer:

-   Produktionsomkostninger
-   Indirekte produktions-, materiale- og marketingomkostninger

**Cost control unit**

En omkostningskontrolenhed repræsenterer omkostningsstruktur. Den skal være forbundet med omkostningers objektdimensioner i omkostningsregnskabets finans.

**Version**

Versioner, der bruges til at simulere, se og sammenligne forskellige udfald. Som standard vises alle faktiske omkostninger i en grundlæggende version, der er kendt som *faktisk*. I budgetter og beregninger kan du arbejde med så mange versioner, som du har brug for. Du kan eksempelvis importere budgetdata i en oprindelig version og derefter ændre budgettet i en revideret version. Du kan oprette flere versioner for beregninger. Du kan derefter oprette beregninger ved hjælp af andre beregningsregler, der skal udlignes for omkostningstildeling i disse forskellige versioner.

**Statement**

Opgørelser er visninger for de ledere, der er ansvarlige for styring af omkostninger. Opgørelser er defineret af en omkostningscontroller, og de giver et hurtigt overblik over aktuelle og budgetterede omkostninger, og endda afvigelser og beregningsversioner. For at sikre, at ledere kun ser de data, som de er ansvarlige for, er data, der vises i opgørelser, underlagt adgangsregler.

**Datatilslutning**

Data kan importeres til omkostningsregnskabet fra eksterne systemer via dataconnectorer. Du kan f.eks. importere kontostrukturer, dimensioner, finansposter og budgetposter. Du kan bruge forudkonfigurerede dataconnectorer eller brugerdefinerede connectorer til at importere data og oprette dataforbindelser.

**Cost classification**

Omkostningsklassifikation grupperer omkostninger i henhold til deres fælles karakteristika. For eksempel kan omkostninger grupperes efter elementer, sporbarhed og funktionsmåde.

-   **Efter elementer** – materialer, arbejdsløn og udgifter.
-   **Efter sporbarhed** – direkte og indirekte omkostninger. Direkte omkostninger tildeles omkostningsobjekter direkte. Indirekte omkostninger kan ikke direkte spores til omkostningsobjekter. Indirekte omkostninger fordeles til omkostningsobjekter.
-   **Efter funktionalitet** – faste, variable og delvist variable.

**Cost behavior**

Omkostningers funktionsmåde klassificerer omkostninger efter deres funktionsmåde i forhold til ændringer i virksomhedens aktiviteter. For at styre omkostninger effektivt skal ledelsen forstå funktionsmåden for omkostninger. Der findes tre typer funktionsmønstre for omkostninger: faste, variable og delvist variable.

- **Faste omkostninger** -faste omkostninger, der er en omkostning, der ikke varierer på kort sigt, uanset ændringer i aktivitetsniveau. Faste omkostninger kan eksempelvis være grundlæggende driftsudgifter for en virksomhed, der ikke bliver berørt, selvom aktivitetsniveau forøges eller formindskes.

- **Variable omkostninger** -en variabel omkostning ændres i overensstemmelse med ændringer i aktivitetsniveau. For eksempel er en bestemt direkte materialeomkostning knyttet til hvert produkt, der sælges. Jo flere produkter, der sælges, jo flere direkte materialeomkostninger er der.

- **Delvis variable omkostninger** -delvis variable omkostninger er omkostninger, der er delvist faste og variable delvist. For eksempel omfatter et internetadgangsgebyr et månedligt standardgebyr for adgang og et brugsgebyr af bredbånd. Det månedlige standardadgangsgebyr er faste omkostninger, mens gebyret for bredbåndsforbrug er en variabel omkostning.

**Overhead cost**

Faste omkostninger vedrører de løbende udgifter til drift af en virksomhed. Det er de omkostninger, der ikke kan knyttes direkte til virksomhedens konkrete aktiviteter. Følgende er eksempler på faste omkostninger:

-   Regnskabsgebyrer
-   Afskrivninger
-   Forsikring
-   Interesser
-   Advokatsalærer
-   Moms
-   Forbrugsomkostninger

**Cost allocation**

Omkostningsfordeling er processen for tildeling og fordeling af omkostninger, der er baseret på hovedårsagerne til de almindelige omkostninger. Du kan allokere omkostningsbeløb og antal fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter. For eksempel fordeles alle facilitetsserviceomkostninger til de forskellige afdelinger, der bruger den fælles kontorbygning.

**Cost allocation policy**

En politik til fordeling af omkostninger definerer de beløb og mængder, der skal fordeles. Fordelingsregler omfatter regler for fordeling af kilde, som bestemmer de omkostninger, der er fordelt, og fordelingsmålsregler, som bestemmer, hvor omkostningerne fordeles. For eksempel er alle omkostninger for facilitetsservices en fordelingskilde, der kan fordeles på forskellige afdelinger i en organisation (det vil sige til fordelingsmål).

**Allocation base**

Fordelingsbasis er det grundlag, der kan bruges til at måle og kvantificere aktiviteter som maskintimer, der bruges, kilowatt-timer, der forbruges, direkte arbejdstimer, der er brugt, eller areal, der er optaget. Det bruges til at fordele omkostninger til et eller flere omkostningsobjekter.

**Allocation principle**

En af fordelingsprincipperne er at fordele omkostningerne efter omkostningssats. Du kan vælge at tildele omkostninger ved hjælp af den faktiske periodesats eller en historisk sats. Fordeling, der bruger den reciprokke metode, hjælper med at sikre, at fordelingsbasis bestemmes af en række samtidige ligninger, før tildeling sker ved hjælp af den faktiske periodesats.

**Cost roll-up**

Formålet med omkostningstotaler er at medtage alle omkostninger for et givet omkostningsobjekt. Niveauet af aggregering er brugerdefineret. Ved hjælp af omkostningstotal kan du aggregere elementer af omkostninger, der skal fordeles fra ét omkostningsobjekt til et andet. Når omkostningstotal ikke bruges, tildeles hvert element af omkostninger fra ét omkostningsobjekt til et andet.

**Omkostningssats politik**

Omkostningssatsen bruges til at beregne prisen pr. omkostningsobjekt. For at forstå elementerne af prisen definerer du politikker for omkostningssats. Der findes to typer omkostningssatser: historisk omkostningssats og planlagt omkostningssats. En historisk omkostningssats er en beregnet sats, der bruges som multiplikator for fordelingsbasis af et omkostningsobjekt. Satsen beregnes på basis af omkostningsfordelinger i den foregående periode. En planlagt sats er en brugerdefineret sats.

**Dimensionelle hierarki**

Dimensionshierarkier bruges som rapporteringsstrukturer, når du definerer regler for fordeling, omkostningssats og omkostningstotal, får vist opgørelser eller data i Microsoft Excel og definerer adgang til de aggregerede data. Der er to dimensionshierarkier: kategorihierarki og klassifikationshierarki. Et kategorihierarki er defineret ud fra omkostningselementer, mens et klassifikationshierarki defineres ud fra omkostningsobjekter.

**Statistical dimension**

En statistisk dimension er udtryk for et antal eller en sum af et objekt, der kan bruges som grundlag for tildelinger eller omkostningsberegninger. Den er oprettet manuelt eller importeret fra kildesystemer. Eksempler på statistiske dimensioner er antallet af medarbejdere, antallet af licenssoftware på hver enhed, strømforbruget på hver maskine eller kvadratmeter for en bærer.

**Statistical entry**

Statistiske poster indeholder den registrerede sum eller antalsværdi for en given statistisk dimension. Den registrerede sum eller antalsværdi kaldes også størrelsesorden.

