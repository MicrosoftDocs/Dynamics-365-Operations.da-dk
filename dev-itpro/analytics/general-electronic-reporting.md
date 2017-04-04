---
title: Oversigt over elektronisk rapportering
description: "Denne artikel indeholder en oversigt over værktøjet Elektronisk rapportering (ER). Den indeholder oplysninger om centrale koncepter, de scenarier, som ER understøtter, samt en liste over formater, der er designet og udgivet som del af løsningen."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Oversigt over elektronisk rapportering

Denne artikel indeholder en oversigt over værktøjet Elektronisk rapportering (ER). Den indeholder oplysninger om centrale koncepter, de scenarier, som ER understøtter, samt en liste over formater, der er designet og udgivet som del af løsningen.

Elektronisk rapportering (ER) er et værktøj, du kan bruge til at konfigurere formater for elektroniske dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande. Med ER du administrere disse formater i løbet af deres livscyklus. For eksempel kan du overholde nye lovgivningsmæssige krav og kan oprette forretningsdokumenter i det krævede format for at udveksle oplysninger elektronisk med offentlige myndigheder, banker og andre parter. ER-programmet henvender sig til virksomhedsbrugere i stedet for udviklere. Da du konfigurerer formater, og ikke kode, udføres processer til oprettelse og tilpasning af formater for elektroniske dokumenter hurtigere og nemmere. ER understøtter i øjeblikket regnearksformaterne TEXT, XML og OPENXML. Men der er mulighed for understøttelse af flere formater.

## <a name="capabilities"></a>Egenskaber
ER-programmet har følgende funktioner:

-   Det repræsenterer et enkelt fælles værktøj til elektronisk indberetning i forskellige domæner, og erstatter mere end 20 forskellige motorer, som har en form for elektronisk indberetning til Microsoft Dynamics 365 for operationer.
-   Det er et rapportformat, isoleret fra det aktuelle Dynamics 365 for gennemførelsen af operationer. (Med andre ord formatet, der er gældende for forskellige versioner af Dynamics 365 for operationer).
-   Det understøtter oprettelse af et brugerdefineret format, der er baseret på et oprindeligt format. Det indeholder funktioner til automatisk at opgradere det tilpassede format, når der sker ændringer af det oprindelige format, fordi lokaliserings-/tilpasningskrav introduceres.
-   Det bliver det primære standardværktøj til understøttelse af lokaliseringskrav i forbindelse med elektronisk rapportering, for både Microsoft og MS-partnere.
-   Det understøtter muligheden for at distribuere formater til partnere og debitorer via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Begreber
### <a name="components"></a>Komponenter

ER understøtter to komponenttyper: **Datamodel **og **Format**.

#### <a name="data-model-components"></a>Datamodelkomponenter

En datamodelkomponent er en abstrakt gengivelse af en datastruktur og skal bruges til at beskrive et bestemt forretningsområdedomæne med nok detaljer til at tilgodese kravene til rapportering i dette domæne. En data modelkomponent består af følgende dele:

-   En datamodel som et sæt af domænespecifikke forretningsenheder samt en hierarkisk struktureret definition af relationerne mellem enhederne:
-   En model, tilknytning, links markeret Dynamics 365 for operationer datakilder for individuelle elementer af en datamodel, der angiver på kørselstidspunktet datastrømmen og reglerne for dataangivelse til Løsningsadministration business til en data-model komponent.

En forretningsenhed af en datamodel er repræsenteret som en beholder (post). Egenskaber for forretningsenheden er repræsenteret som dataelementer (felter). Hvert dataelement har et entydigt navn, etiket, beskrivelse og værdi. Værdien af hvert dataelement kan være udformet, så den kan genkendes som en streng, heltal, reelt tal, dato, optællingstype, Boolesk osv. Desuden kan det være en anden post eller postliste. En enkelt datamodelkomponent kan indeholde flere hierarkier af domænespecifikke forretningsenheder og også modeltilknytninger, der understøtter et særligt rapportspecifikt dataflow under kørsel. Hierarkierne afpasses efter en enkelt post, der er valgt som en rod for modeltilknytningen. Datamodellen for betalingsdomæneområdet kan f.eks. understøtte følgende tilknytninger:

-   Virksomhed -&gt; kreditor -&gt; betalingstransaktioner for AP-domæne
-   Debitor -&gt; virksomhed -&gt; betalingstransaktioner for AR-domæne

Bemærk forretningsenheder (f.eks firma- og betalingsposteringer) angives én gang. Forskellige tilknytninger genbruger dem. En modeltilknytning har følgende funktioner:

-   Det kan bruge forskellige Dynamics 365 for operationer datatyper som datakilder til en datamodel. Den kan for eksempel bruge tabeller, dataenheder, metoder eller fasttekster.
-   Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.
-   Det understøtter omdannelsen af Dynamics 365 for operationer i nødvendige grupper, filtrering, sortering og opsummere data, og også tilføje med logiske beregnede felter, der er udviklet til Microsoft Excel-lignende formler (Yderligere oplysninger finder du under [formel designer i elektronisk indberetning](general-electronic-reporting-formula-designer.md)).

[![Excel-lignende formeleditor](./media/pic-formula-1024x615.png)](./media/pic-formula.png) en komponent til data model er udviklet til hvert business-domæne, der skal bruges som en datakilde, der er samlet til rapportering, der isolerer rapporter fra den fysiske gennemførelse af Dynamics 365 for operationer datakilder, og repræsenterer domæne-specifikke forretningsmæssige begreber og funktioner i en formular, der gør en rapportering format indledende design og yderligere vedligeholdelse af mere effektiv.

#### <a name="format-components"></a>Formatkomponenter

En formatkomponent er skemaet for rapporteringsoutput, der skal oprettes på kørselstidspunktet. Et skema består af følgende elementer:

-   Et format, der definerer strukturen og indholdet af det elektroniske dokument til rapportering, der af oprettet på kørselstidspunktet
-   Datakilder som et sæt brugerinputparametre og en domænespecifik datamodel, der bruger valgt modeltilknytning
-   En formattilknytning som et sæt bindinger af formatdatakilder, der har enkelte elementer af et format, der angiver dataflow og regler for formatoutputgenerering på kørselstidspunktet
-   Validering af et format som et sæt konfigurerbare regler, der styrer oprettelse af rapporter på kørselstidspunktet, afhængigt af kørselskonteksten (for eksempel en regel, der stopper outputgenerering af en kreditors betalinger og medfører en undtagelse, når bestemte attributter for den valgte kreditor mangler, som f.eks. bankkontonummer).

En formatkomponent understøtter følgende funktioner:

-   Oprettelse af rapporteringsoutput som separate filer i forskellige formater: tekst, XML eller regneark
-   Separat oprettelse af flere filer og også indkapsling af disse filer i zip-filer

En formatkomponent leverer funktioner til at vedhæfte bestemte filer, der kan bruges i rapporteringsoutputtet:

-   Excel-projektmapper, der indeholder et regneark, der kan bruges som skabelon for output i regnearksformat OPENXML:
-   Andre filer kan indgå i formatets output som foruddefinerede filer.

#### <a name="component-versioning"></a>Komponentversioner

Versionering understøttes for ER-komponenter. Følgende arbejdsgang findes til håndtering af ændringer i ER-komponenter:

-   Den oprindelige version, der blev oprettet, er markeret som en **KLADDE** version. Denne version kan redigeres og er tilgængelig for testkørsler.
-   **KLADDE** versionen kan konverteres til en **FULDFØRT** version. Denne version kan bruges i lokale rapporteringsprocesser.
-   Den **fuldført** version kan konverteres til en **delte** version. Denne version er udgivet på Remburser og kan bruges i global reporting processer.
-   Versionen **DELT **kan konverteres til en **ANNULLERET** version. Denne version kan derefter slettes.

Versioner, som har enten ** fuldført ** eller **delte** status er tilgængelig for andre dataudveksling. Der kan udføres følgende handlinger på en komponent, der har disse statusser:

-   De kan serialiseres i XML-format og eksporteret fra Dynamics 365 for operationer som en fil i XML-format.
-   De kan reserialized fra en XML-fil og importeret til Dynamics 365 for operationer, som en ny version af en komponent ER.

#### <a name="component-date-effectivity"></a>Komponentens datogyldighed

ER-komponentversioner har en ikrafttrædelsesdato. Datoen **Gyldig fra** kan defineres for en ER-komponent for at angive startdatoen, hvor komponenten træder i kraft for rapporteringsprocesser. Dynamics-365 for operationer sessionsdatoen bruges til at definere, om en komponent er gyldig til udførelse. Hvis mere end én version er gyldig for en bestemt dato, bruges den nyeste version til rapporteringsprocesser.

#### <a name="component-access"></a>Komponentadgang

Adgang til ER-formatkomponenter afhænger af indstilling af ISO-lande/områdekoden. Når denne indstilling er tom for en valgt version af en formatkonfiguration, kan en komponent format åbnes fra enhver Dynamics 365 for firma operationer på kørselstidspunktet. Når denne indstilling indeholder ISO-landekoder, er en format-komponent kun tilgængelig fra Dynamics 365 for operationer virksomheder, som har en primær adresse, der er defineret for en af en komponent på et format ISO landekoder. Forskellige versioner af en dataformatkomponent kan have forskellige indstillinger for ISO-lande/områdekoder.

#### <a name="configuration"></a>Konfiguration

En ER-konfiguration er wrapperen for en bestemt ER-komponent: enten **Datamodel** eller **Format**. En konfiguration kan omfatte forskellige versioner af en bestemt ER-komponent. Hver konfiguration er markeret som ejet af en bestemt konfigurationsudbyder. Den **udkast til** version af en komponent i en konfiguration, der kan redigeres, når ejeren af konfigurationen, der er valgt som en aktiv udbyder i indstillingerne ER i Dynamics 365 for operationer. Hver modelkonfiguration indeholder en **Datamodel**-komponent. En ny formatkonfiguration kan stamme fra (være afledt af) en bestemt datamodelkonfiguration. Den formatkonfiguration, der oprettes, bliver præsenteret i konfigurationstræet som underordnet til den oprindelige modeldatakonfiguration. Den formatkonfiguration, der oprettes, indeholder en **Format**-komponent. **Datamodel**-komponenten for den oprindelige modelkonfiguration indsættes automatisk i **Format**-komponenten i den underordnede formatkonfiguration som en standarddatakilde. En ER konfigurationen deles for Dynamics 365 for operationer virksomheder.

#### <a name="provider"></a>Udbyder

ER-udbyderen er den partsidentifikator, der bruges til at angive forfatteren (ejeren) af hver ER-konfiguration. Med ER kan du administrere listen over udbydere af konfigurationen. Formatere konfigurationer, der er overgået til elektroniske dokumenter som en del af den Dynamics 365 for operationer løsning er markeret som ejes af den **Microsoft** konfiguration-udbyder.

#### <a name="repository"></a>Lager

Et ER-lager indeholder ER-konfigurationer. Følgende typer ER lagre understøttes i øjeblikket: **operationsressourcer** og **LCS projekt**. En ** operationer ressourcer ** lager giver adgang til listen over de konfigurationer, der er udgivet som en del af den Dynamics 365 for operationer løsning af Microsoft som udbyder ER konfiguration. Disse konfigurationer kan importeres til den aktuelle Dynamics 365 for forekomst af operationer og bruges til elektronisk indberetning. De kan også bruges til flere yderligere sprogversioner eller tilpasninger. Et **LCS-projektlager **giver adgang til listen over konfigurationer af et LCS-projekt (LCS-projektets aktivbibliotek), der blev valgt på stadiet for lagerregistrering. ER kan du overføre delte konfigurationer fra den aktuelle Dynamics 365 for forekomst af handlinger til en bestemt **LCS projekt** lager. Du kan også importere konfigurationer fra en bestemt **LCS projekt** lager i den aktuelle Dynamics 365 for forekomst af operationer. Der kræves **LCS projekt** lagre kan registreres individuelt for hver søgemaskine, konfiguration af den aktuelle Dynamics 365 for forekomst af operationer. Hvert lager kan dedikeres til en bestemt konfigurationsudbyder.

## <a name="supported-scenarios"></a>Understøttede scenarier
### <a name="building-a-data-model"></a>Opbygning af en datamodel

ER leverer en modeldesigner, som du kan bruge til at bygge en datamodel for et bestemt virksomhedsdomæne. Alle domænespecifikke forretningsenheder og relationerne mellem dem kan præsenteres i en datamodel som en hierarkisk struktur. I følgende illustration vises et eksempel på denne type datamodel (betalingsdomæne-datamodellen). [![Eksempel på en datamodel](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) for at blive fortrolig med detaljerne i denne situation, kan du afspille den **ER Design domænemodel bestemte data** opgave vejledning (en del af den **7.5.4.3 Hent/udvikle IT service/opløsning-komponenter (10677)** forretningsproces).

### <a name="translating-data-model-content"></a>Oversættelse af datamodelindhold

Data model indhold (etiketter og beskrivelser) kan oversættes til andre sprog, der understøtter Dynamics 365 for operationer. Du kan oversætte datamodelindhold af følgende årsager:

-   På designtidspunktet for at gøre indholdet mere forståeligt for formatdesignere, der taler et andet sprog og som bruger en datamodel til datatilknytning af formatkomponenter
-   Ved at køre tid til at gøre indholdet mere brugervenligt ved at præsentere prompter og hjælp til kørsel parametre og valideringsmeddelelser (fejl og advarsler) også er konfigureret på det sprog, som foretrækker Dynamics aktuelt er logget på 365 for operationer bruger

I følgende illustration vises et eksempel på, hvordan datamodelindhold kan oversættes fra engelsk til japansk. [![Data model indhold på engelsk](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![Data model indhold, der er oversat til japansk](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Konfiguration af datamodeltilknytninger

ER her en model tilknytning designer, så brugerne kan knytte datamodeller, der er designet til specifikke Dynamics 365 for operationer datakilder. I følgende illustration vises et eksempel på denne type datamodeltilknytning vises i nedenstående billede (**SEPA-overførsel**-modeltilknytningen i datamodellen for betalingsdomæne). [![Eksempel på en data-model-tilknytning ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png)for at blive fortrolig med detaljerne i dette scenario, afspilles den **model ER definere datakilder for tilknytning, og vælg** og **ER kort datamodel til markerede datakilder** opgave hjælpelinjer (en del af den **7.5.4.3 Hent/udvikle IT service/opløsning-komponenter (10677)** forretningsproces).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagring af en designet modelkomponent som en modelkonfiguration

ER kan gemme en datamodel, der er designet med tilknyttede datatilknytninger som en konfiguration af model for den aktuelle Dynamics 365 for forekomst af operationer. I følgende illustration vises et eksempel på denne type datamodelkonfiguration (betalingsdomæne-datakonfigurationen). [![Eksempel på en konfiguration af model for data ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png)for at blive fortrolig med detaljerne i dette scenario, afspilles den **ER kort datamodel til markerede datakilder** opgave vejledning (en del af den **7.5.4.3 Hent/udvikle IT service/opløsning-komponenter (10677)** forretningsproces).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Opbygning af et format, der bruger en datamodel som udgangspunkt

ER understøtter en formatdesigner, som du kan bruge til at bygge formatet for et bestemt elektronisk dokument for et valgt forretningsdomæne ved at vælge modelkomponenten som udgangspunkt. Med samme ER-formatdesigner kan du knytte et format, som du opretter, til et markeret domænes datamodeltilknytning som en datakilde. I følgende illustration vises et eksempel på denne type format (den formatkonfiguration, der understøtter **BACS**-betalingsformatet for Storbritannien). [![Eksempel på et format, som har en datamodel som udgangspunkt](./media/pic-format-1024x690.png)](./media/pic-format.png) for at blive fortrolig med detaljerne i dette scenario, afspilles den **ER Design domæne bestemt format** opgave vejledning (en del af den **7.5.4.3 Hent/udvikle IT service/opløsning-komponenter (10677)** forretningsproces).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Oprettelse af en konfiguration for at generere elektroniske dokumenter i OPENXML-regnearksformat

ER-formatdesigner kan bruges til at oprette en bestemt elektronisk dokument i OPENXML-regnearksformat. I følgende illustration vises et eksempel på denne type format (en formatkonfiguration til at generere OPENXML-regneark med oplysninger om en valgte betalingskladde):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) for at blive fortrolig med detaljerne i dette scenario, afspilles den **ER oprette en konfiguration til rapporter i OPENXML-formatet** opgave vejledning (en del af den **7.5.4.3 Hent/udvikle IT service/opløsning-komponenter (10677)** forretningsproces). Bruge refereres under Excel-fil som en skabelon i formatet design ER for at fuldføre trin i formatet skabelon import af denne opgave vejledning: [skabelon af betaling rapport (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagring af en designet formatkomponent i en formatkonfiguration

ER kan gemme et format, der er udviklet med de konfigurerede datatilknytninger som et formatkonfigurationen af den aktuelle Dynamics 365 for forekomst af operationer. Ovenstående illustration viser et eksempel på denne type formatkonfiguration (**BACS (UK)**, som er underordnet i forhold til **Betalingsmodel **-konfigurationen). For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifikt format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Konfiguration af Dynamics 365 for operationer til at begynde at bruge et format, der er oprettet internt

Dynamics 365 for operationer kan konfigureres til at begynde at bruge et format, der er oprettet til at generere elektroniske rapporter. Referencen til den oprettede formatkonfigurationen bør fastlægges i indstillingerne for et bestemt domæne. For eksempel for at begynde at bruge en konfiguration af ER formatet for elektroniske kreditorbetalinger i BACS format, formatkonfigurationen skal henvises til i bestemte betalingsmåder, som vist i følgende illustrationer: 

[![Formatkonfiguration af BACS (UK)](media/ger-bacs-uk-format-configuration.png) 

[![Refererer til formatet BACS (UK) i en betalingsmetode](media/ger-bacs-uk-format-method.png) 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille **ER Brug format til at generere elektronisk dokument til betalinger** (del af forretningsprocessen **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)**).

## <a name="handling-er-components"></a>Håndtering af ER-komponenter
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Udgive en ER-komponent i LCS for at tilbyde den eksternt (lokalisering)

Ejeren af en komponent (model eller format), der er oprettet, kan bruge ER til udgivelse af den færdige version af en ER-komponenten til LCS. Et lager af typen **LCS-projekt **for den aktuelle ER-konfigurationsudbyder er nødvendigt. Når statussen for den færdige version af en komponent er ændret fra **FULDFØRT** til **DELT**, udgives denne version LCS. Når en komponent er udgivet til LCS, bliver ejeren af denne komponent en udbyder af tjenesten til at understøtte komponenten. Hvis formatkomponenten f.eks. er designet til at generere et elektronisk dokument, der er juridisk påkrævet (f.eks. i henhold til et lokaliseringsscenarie), antages det, at formatet fortsat er kompatibelt med lovgivningsmæssige ændringer, og at udbyderen vil udsende nye versioner af komponenten, hver gang der kommer nye lovgivningsmæssige krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Overføre ER-konfiguration til Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere ER-komponent fra LCS for at bruge det internt

ER kan du importere ER komponenter fra LCS til den aktuelle Dynamics 365 for forekomst af operationer. Et lager af typen **LCS-projekt **er påkrævet. Når en komponent ER blevet importeret fra LCS til den aktuelle Dynamics 365 for forekomst af operationer, bliver ejer af forekomsten af en forbruger af tjenesten, der er angivet af komponenten importerede ejer (forfatter). For eksempel hvis en komponent i formatet er designet til at generere et bestemt elektronisk dokument fra Dynamics 365 for operationer i en lande-/ regionsspecifikke format (lokalisering scenario), antages det, at forbrugeren service vil kunne hente opdateringer, der foretages i dette format, så de er kompatible med lovfæstede krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **ER-import af en konfiguration fra Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Opbygge et format ved at vælge et andet format som udgangspunkt (tilpasning)

Med ER kan du oprette (aflede) en ny komponent fra den aktuelle version af en komponent (basis), der er importeret fra LCS. For eksempel ønsker en bruger at aflede et nyt format for at implementere nogle særlige krav til et elektronisk dokument (f.eks. et ekstra felt eller en omfattende beskrivelse) til understøttelse af et tilpasningsscenario. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af det** (del af **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)** for forretningsproces).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Opgradering af et format ved at vælge en ny version af basisformat (rebasere)

Med ER kan du automatisk implementere ændringer af den nyeste version af basiskomponenten i den aktuelle kladdeversion af den afledte komponent. Denne proces kaldes *rebasering*. F.eks. kan en ny lovmæssig ændring, der er indført i den nyeste version af formatet, der blev importeret fra LCS, automatisk flettes med den tilpassede version af dette format af det elektroniske dokument. Ændringerne, der ikke kan flettes automatisk, anses for konflikter. Disse konflikter præsenteres for manuel løsning i designerværktøjet for den pågældende komponent. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af det** (del af **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)** for forretningsproces).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Oversigt over ER de konfigurationer, der er leveret i Dynamics-365 for løsning af operationer
| Domænespecifikke datamodelkonfigurationer: titel | Domæne                | Datamodel-afhængige formatkonfigurationer: titel | Beskrivelse                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Revisionsfilmodel                                 | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | Revisionsfil (NL)                                   | Revisionsfilformat for Nederlandene                                  |
| BAS-model                                        | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS-format for Australien                                           |
| Skemamodel til konstruktionsbranchen               | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | CIS månedlig returnering (UK)                           | CIS månedligt returformat for Storbritannien                   |
| Rykkermodel                          | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-rykker (DK)                     | OIOUBL-rykkerformat for Danmark                        |
| Elektronisk finansregnskabsmodel (MX)          | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Supplerende finans-XML (MX)                         | Supplerende finanstransaktioner pr. kontorapportformat for Mexico |
|                                                  |                       | Kontoplan XML (MX)                         | Diagram over kontorapportformat for Mexico                          |
|                                                  |                       | Kladder XML (MX)                                 | Kladdeposteringsrapportformat for Mexico                      |
|                                                  |                       | Råbalance XML (MX)                            | Råbalance-rapportformat for Mexico                             |
| Elster-model                                     | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-format for Tyskland                                          |
| EU-listesystemmodel                              | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | EU-listesystem (DE)                                | EU-listesystem, TXT-format for Tyskland                               |
|                                                  |                       | EU-listesystem (DK)                                | EU-listesystem, TXT-format for Danmark                               |
|                                                  |                       | EU-listesystem (FR)                                | EU-listesystem, XML-format for Frankrig                                |
|                                                  |                       | EU-listesystem (NL)                                | EU-listesystem, XML-format for Nederlandene                           |
|                                                  |                       | EU-listesystem TXT (UK)                            | EU-listesystemet, TXT-format for Storbritannien                    |
|                                                  |                       | EU-listesystem XML (UK)                            | EU-listesystemet, XML-format for Storbritannien                    |
|                                                  |                       | Rapport for EU-listesystem efter kolonne                   | Rapport for EU-listesystem efter kolonne                                    |
|                                                  |                       | Rapport over EU-listesystem efter rækker                      | Rapport over EU-listesystem efter rækker                                       |
| FEC regnskabsmodel (FR)                        | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | FEC-regnskabsdata XML (FR)                      | XML-format for eksport af FEC regnskabsdata for Frankrig                   |
| Tysk revisionsfil                                | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | Output af tysk revisionsfil                          | Output af revisionsfil for Tyskland og Østrig                          |
| Intrastat-modul                                  | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat-format for Tyskland                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat-format for Danmark                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM-format for Frankrig                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC-format for Frankrig                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat-format for Nederlandene                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastat-format for Storbritannien                            |
|                                                  |                       | Intrastat-rapport                                  | Intrastat Excel-kontrolrapport                                     |
| Debitorfakturamodel                           | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL projektkreditnota (DK)                   | OIOUBL format for projektkreditnota for Danmark                      |
|                                                  |                       | OIOUBL projektfaktura (DK)                       | OIOUBL format for projektfaktura for Danmark                          |
|                                                  |                       | OIOUBL salgskreditnota (DK)                     | OIOUBL format for salgskreditnota for Danmark                        |
|                                                  |                       | OIOUBL salgsfaktura (DK)                         | OIOUBL format for salgsfaktura for Danmark                            |
| OB-opgørelsesmodel                             | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | OB-opgørelse (NL)                               | OB-opgørelsesformat for Nederlandene                          |
| Betalingsmodel                                    | Betalinger              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice-betalingsformat for Danmark                        |
|                                                  |                       | Vekselremittering (FR)                  | Vekselremitteringsformat for Frankrig                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91-kreditorbetalingsformat for Nederlandene                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB format for direkte debetbetalinger for Frankrig                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB format for indenlandsk kreditorbetaling for Frankrig                    |
|                                                  |                       | Nordea kreditor (DK)                                | Kreditorbetalingsformatet Nordea Corporate Netbank for Danmark         |
|                                                  |                       | ANZ direkte kreditydelsesformat (AU)                    | Formatet for ANZ kreditydelsesformat for Australien                 |
|                                                  |                       | CBA direkte kreditydelsesformat (AU)                    | Format for CBA direkte kreditydelse for Australien                 |
|                                                  |                       | NAB direkte kreditydelsesformat (AU)                    | Format for NAB direkte kreditydelse for Australien                 |
|                                                  |                       | STG direkte kreditydelsesformat (AU)                    | Format for STG direkte kreditydelse for Australien                 |
|                                                  |                       | WBC direkte indtastningssystemformat (AU)                      | Format for WBC direkte indtastningssystem for Australien                   |
|                                                  |                       | DirectLink (NZ)                                   | Formatet for DirectLink for New Zealand                              |
|                                                  |                       | JBA-betalingsfil (JP)                             | JBA betalingsformat for Japan                                       |
|                                                  |                       | ISO20022 overførsel                          | SEPA kreditoverførselsformat for Europa                             |
|                                                  |                       | ISO20022-overførsel (FR)                     | SEPA kreditoverførselsformat for Frankrig                             |
|                                                  |                       | ISO20022-overførsel (DE)                     | SEPA kreditoverførselsformat for Tyskland                            |
|                                                  |                       | ISO20022-overførsel (NL)                     | SEPA kreditoverførselsformat for Nederlandene                    |
|                                                  |                       | ISO20022 direkte debet                             | SEPA direkte debetformat for Europa                                |
|                                                  |                       | ISO20022 direkte debet (FR)                        | SEPA direkte debetformat for Frankrig                                |
|                                                  |                       | ISO20022 direkte debet (DE)                        | SEPA direkte debetformat for Tyskland                               |
|                                                  |                       | ISO20022 direkte debet (NL)                        | SEPA direkte debetformat for Nederlandene                       |
|                                                  |                       | BACS (UK)                                         | BACS kreditorbetalingsformat for Storbritannien                  |
| Modtagermoms                                   | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Salgsliste med modtagermoms                         | Salgsliste med modtagermomsformat                                   |
| Nederlandsk XBRL-integrationsmodel                     | XBRL-rapportering        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL eksportformat for Nederlandene                    |
| GAF-model (MY)                                   | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | GAF-fil (MY)                                     | Format for GAF for Malaysia                                         |
| Aldersfordelt saldoliste for kreditor (CN)                         | Kreditordataanalyse |                                                   |                                                                    |
|                                                  |                       | Aldersfordelt saldoliste for kreditor (CN)                   | Aldersfordelt saldoliste for kreditorer for Kina                               |
| Opgørelsesmodel for kreditorfaktura                 | Kreditordataanalyse |                                                   |                                                                    |
|                                                  |                       | Kreditorfakturadeklaration (IS)                   | Opgørelse for kreditorfaktura, format for Island                      |
|                                                  |                       | Kreditorfakturadeklaration, rapport (IS)            | Opgørelse for kreditorfaktura, rapport for Island                      |



<a name="see-also"></a>Se også
--------

[Lokaliseringskrav – oprette en elektronisk rapporteringskonfiguration](electronic-reporting-configuration.md)

[Administrere livscyklus for elektroniske indberetningskonfigurationer](general-electronic-reporting-manage-configuration-lifecycle.md)


